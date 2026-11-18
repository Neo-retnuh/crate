---
name: swarm-deliberation
description: >
  Runs isolated parallel reasoning across multiple agent perspectives with
  blind synthesis, for decisions where the value is in the disagreement
  between perspectives rather than any single perspective's quality. Supports
  three patterns: persona_panel (stakeholder viewpoints on one artifact),
  futures_fork (scenario branches from shared starting conditions),
  adversarial_dialectic (opposing theses resolved by a blind judge). Use when
  the request says "persona panel", "swarm review", "stress-test across
  scenarios", "opposing positions", "dialectic", "panel of personas", or
  names any decision where multi-perspective tension is the point. Do NOT use
  for single-answer questions, routine execution, or reviews a single
  reviewer can handle alone.
metadata:
  author: Hunter Marshall (https://www.mesteezo.com)
  license: MIT
---

# Swarm Deliberation

This skill runs structured multi-agent deliberation. It produces decision-relevant output by forcing isolated parallel reasoning and blind synthesis — the opposite of a single shared reasoning context.

## When to use

- The output's value is in the disagreement between perspectives, not in any single perspective's quality.
- The task is analysis where the tension between perspectives is itself the insight.
- One of the three patterns fits: reviewing one artifact through several stakeholder lenses, stress-testing a decision across scenarios, or resolving two opposing theses.
- Literal asks: "persona panel", "swarm review", "stress-test across scenarios", "opposing positions", "dialectic", "panel of personas".

## When not to use

- Single correct answer exists → use a single agent.
- The task is execution, not analysis → use a single agent.
- A single-reviewer approach would catch the issue alone → use that reviewer; swarm is high-cost (N× tokens).

## Inputs

- The artifact or question to deliberate on.
- The chosen pattern (persona_panel | futures_fork | adversarial_dialectic).
- The set of perspectives (persona descriptions, scenarios, or the two opposing positions + a judge).
- A fixed output schema every agent must answer, set before agents are spawned.

## Method

Copy this checklist and check items off as you go:
- [ ] Step 1 — Classify the request (pattern, artifact/question, agent count, fixed schema)
- [ ] Step 2 — Apply the validation rules; abort and route to a single agent if they fail
- [ ] Step 3 — Record deliberation start (pattern, agent count, schema fingerprint, artifact reference)
- [ ] Step 4 — Spawn agents in full isolation, in parallel
- [ ] Step 5 — Collect, shuffle, and anonymize outputs
- [ ] Step 6 — Run blind synthesis (signal matrix, tensions, implications, verdict)
- [ ] Step 7 — Validate before delivery (at least one decision-relevant disagreement, actionable-or-explicitly-unresolved verdict)
- [ ] Step 8 — Deliver using the output schema

### Core Principle

**The output's value is in the disagreement.** If there's a single correct answer, use a single agent. If the task is execution, use a single agent. Swarm deliberation is for analysis where the tension between perspectives is itself the insight.

### Three Supported Patterns

#### 1. persona_panel
Multiple agents embody different stakeholder viewpoints on the SAME artifact. Each works in full isolation with identical input. Synthesizer receives shuffled, anonymized outputs and identifies disagreement patterns — not consensus.

**Use cases:**
- Creative or campaign review (per asset, on a regular cadence)
- Content calendar review (monthly)
- Proposal review from client/competitor/team perspectives

#### 2. futures_fork
Multiple agents explore different scenarios from the same starting conditions. Each develops a complete timeline, impact assessment, and required actions. Synthesizer finds decisions that are robust across all futures.

**Use cases:**
- Quarterly scenario planning
- Risk assessment for major decisions
- "What if" analysis for system changes

#### 3. adversarial_dialectic
Two agents take opposing positions on a thesis. A third (judge/connector) receives both arguments blind, evaluates them on their merits, and returns either a recommendation or an explicitly unresolved tension — surfacing connections neither side made and contradictions that locate the real disagreement.

**Use cases:**
- Self-improvement deliberation (on a regular cadence)
- Research deliberation (per installment)
- Strategy stress-testing

### Validation Rules (mandatory — enforce before synthesis)

1. **Disagreement-informative check.** If the question has a single correct answer or the task is execution (not analysis), abort and route to a single agent. Log a validation failure with reason `wrong_tool`.
2. **Single-agent sufficiency check.** If a single-reviewer approach alone would catch the issue, abort. Swarm is high-cost (N× tokens); don't spend it where one reviewer works. Failure code: `single_agent_sufficient`.
3. **Fixed output schema per agent.** Every agent in a deliberation answers the SAME questions in the SAME format. No free-form responses. Schema is set before agents are spawned. Failure code: `schema_violation`.
4. **Blind synthesis.** The synthesizer receives shuffled, anonymized outputs. It must not know which agent produced which response or the order of generation. Failure code: `blind_synthesis_violation`.
5. **Concrete verdict.** Synthesis ends with either a specific recommendation OR an explicit statement of unresolved tensions with their decision implications. "Interesting perspectives" is not an acceptable output — return `verdict.type: unresolved` with reason if you reach that point. Failure code: `no_concrete_verdict`.

Every mandatory rule has exactly one failure code. Full set: `wrong_tool` (rule 1), `single_agent_sufficient` (rule 2), `schema_violation` (rule 3), `blind_synthesis_violation` (rule 4), `no_concrete_verdict` (rule 5), plus `insufficient_divergence` from the delivery-time divergence check in Step 6.

### Step-by-Step Process

#### 1. Classify the request
- Which pattern? (persona_panel | futures_fork | adversarial_dialectic)
- What's the artifact or question?
- How many agents? persona_panel: 3–5. futures_fork: 3–4. adversarial_dialectic: exactly two position advocates plus a separate judge (3 agents total) — the judge is never one of the two advocates and never counts toward them.
- What's the fixed schema each agent must answer?

If classification fails or the request would be better served by a single agent, stop and recommend that alternative. Do not run swarm theater.

#### 2. Record deliberation start
Note the pattern, agent count, schema fingerprint, and artifact reference.

#### 3. Spawn agents in full isolation
Use a subagent for each perspective. Each agent gets:
- Identical artifact/question input
- Its own perspective framing (persona description, scenario, or position)
- The fixed output schema
- Explicit instruction: do not reference other perspectives (it cannot see them anyway)

Run agents **in parallel** — a single batch of N agent calls. Parallel execution reduces anchoring (no agent's output is available to shape a later one) and cuts latency. What actually prevents leakage is isolation, not scheduling: a sequential run of genuinely isolated agents is still valid, but it is easier to accidentally carry context forward, so parallel is the default.

#### 4. Collect + shuffle outputs
Receive each agent's response. Shuffle the list. Strip identifying metadata (perspective name, order, anything that leaks who said what) and assign anonymous handles (Agent A, Agent B, …) in shuffled order before passing to synthesis. Keep the handle→perspective mapping outside the synthesis context; it may be revealed only after the verdict is finalized.

#### 5. Blind synthesis
Synthesize from the shuffled, anonymized outputs. Produce:
- **Signal matrix** — table of agent-response-per-question, columns labelled with anonymous handles (Agent A, Agent B, …) assigned after the shuffle. Perspective identity is NOT restored here; it may be mapped back only after the verdict is finalized, and only if naming who said what adds decision value.
- **Key tensions** — numbered genuine disagreements with evidence quotes
- **Decision implications** — what these tensions mean for the actual decision
- **Verdict** — specific recommendation OR explicit unresolved with decision-relevant reason

#### 6. Validate before delivery
- Is at least one material disagreement decision-relevant — i.e. resolving it would change the recommended action? If no disagreement clears that bar → validation failure, reason `insufficient_divergence`, verdict becomes `unresolved`, recommend fallback. Report the divergence count as a quality signal alongside the verdict (a single decisive disagreement can carry a deliberation; three cosmetic ones cannot). Never invent or inflate a disagreement to clear this check.
- Verdict is actionable (specific recommendation) OR explicitly unresolved with named blocker? If not, revise until it is. Never ship "the perspectives are interesting" as a verdict.

#### 7. Deliver the output
Write the deliberation result using the output schema below.

### Important Rules

- Never fabricate an agent response. If an agent fails to return, log it and either respawn or reduce N — but never below the pattern's floor: adversarial_dialectic requires both advocates plus the separate judge (no reduction below that structure), panel/fork require 3 agents.
- Never let agents see each other's work mid-deliberation. Isolation is the whole point.
- Never skip the shuffle + anonymize step before synthesis.
- Never ship a verdict that doesn't either recommend an action or explicitly name what's blocking the decision.

### Quality Bar (check each run before trusting its verdict)

- [ ] A fixed schema was enforced per agent (never free-form)
- [ ] Agents ran in isolation, with no shared context mid-deliberation
- [ ] The blind synthesis protocol was followed (outputs shuffled, anonymized)
- [ ] The validation rules were applied (a run with too little real divergence returns "unresolved," not a fabricated answer)
- [ ] The verdict either recommends an action or names what's blocking the decision

## Output

```
## Deliberation Summary

**Pattern:** persona_panel | futures_fork | adversarial_dialectic
**Artifact:** [what was reviewed/analyzed]
**Agents:** [count and brief descriptions]

### Signal Matrix
| Question | Agent A | Agent B | Agent C | ... |
|----------|---------|---------|---------|-----|
| Q1       | ...     | ...     | ...     | ... |

### Key Tensions
1. [Disagreement] — evidence: "[quote from agent output]" vs "[quote from other agent]"
2. ...

### Decision Implications
- [What tension #1 means for the actual decision]
- ...

### Verdict

**Verdict type:** recommendation | unresolved
**Validation:** pass | wrong_tool | single_agent_sufficient | schema_violation | blind_synthesis_violation | no_concrete_verdict | insufficient_divergence

[Specific recommendation OR explicit "unresolved — here's the blocker"]
```

`Verdict type` and `Validation` are required fields, not optional garnish. `recommendation` requires a specific action; `unresolved` requires a named blocker. `Validation` is `pass` when every validation rule held, otherwise the reason code of the rule that failed — one code per mandatory rule, listed in full under Validation Rules.

## Example

Input: "Run a persona panel on our new pricing page before it ships. I want to know if the tiers land." (Attaches the pricing-page draft: three tiers — Starter, Growth, Scale — with a "best value" badge on Growth and a launch-discount banner across the top.)

Output:

```
## Deliberation Summary

**Pattern:** persona_panel
**Artifact:** Pricing page draft (3 tiers: Starter / Growth / Scale)
**Agents:** 5 — price-sensitive buyer, premium buyer, competitor, sales lead, finance owner

### Signal Matrix
| Question | Agent A | Agent B | Agent C | Agent D | Agent E |
|----------|---------|---------|---------|---------|---------|
| Where does the price anchor land? | On Growth | On Starter | On Scale | On Scale | On Growth |
| Are the tier names clear? | No | No | Yes | No | No |
| Is "best value" believable? | Weak | No | No | No | No |
| Does the discount fit positioning? | Signals desperation | Yes | Erodes margin | Undercuts premium | Helps close |

(Columns are post-shuffle anonymous handles; the persona behind each is not mapped back until the verdict is final.)

### Key Tensions
1. Price-anchor split — evidence: "my eye goes straight to the cheapest option" vs "the top tier is what tells me you're serious."
2. Tier-naming confusion — evidence: "I can't tell what 'Growth' includes over 'Starter'" — echoed by 4 of 5 agents.
3. Discount vs premium positioning — evidence: "a launch discount reads as a company that isn't sure of its price" vs "the discount is what gets the deal signed this quarter."

### Decision Implications
- The anchor is doing three different jobs for three buyers; the page needs one deliberate anchor, not an accidental one.
- "best value" is unsupported by any persona — remove it or back it with a concrete comparison.
- The discount banner and the premium framing actively contradict; pick one before launch.

### Verdict

**Verdict type:** recommendation
**Validation:** pass

Do not ship as-is. Set a single intended anchor (recommend Growth) and make the layout serve it, rename tiers around the value each unlocks, drop the unsupported "best value" badge, and resolve the discount-vs-premium contradiction.
```

## Notes

- Cost: N agents × input size per deliberation. Do not run swarm on every review — a single-reviewer approach handles most cases alone.
- A simpler multi-view method that runs everything in one shared context is contamination-prone. Use swarm-deliberation when the isolation requirement matters.
- Minimum agent counts: adversarial_dialectic = two advocates plus a separate judge (3 total, no reduction below that structure); panel/fork = 3. If an agent fails to return, respawn or reduce N within those floors — never fabricate a response.
