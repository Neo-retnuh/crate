---
name: parallel-perspectives
description: >
  Stress-tests a question, strategy, content draft, or decision by analyzing it
  from multiple distinct perspectives at once, then synthesizes convergence,
  tension, and blind spots into a decision recommendation. Use when 2+ competing
  options exist, stakeholders would disagree, or the output will drive a real
  decision, or when the user says "devil's advocate", "what am I missing",
  "compare perspectives", or "look at this from different angles". Also fires
  on "stress test this" when the user is weighing options or stakeholder
  tradeoffs — if the target is instead one finished artifact to critique,
  route to adversarial-review. Scope — decisions and drafts with meaningful
  tradeoffs; not simple factual lookups or single-path execution.
metadata:
  author: Hunter Marshall (https://www.mesteezo.com)
  license: MIT
---

# Parallel Perspectives

Multi-lens decision stress-test. Fan out a task to distinct perspectives, collect independent structured analyses, synthesize convergence/tension/blind spots, and produce a decision recommendation — not just insight.

## When to use
- 2+ competing strategies or options exist, with meaningful tradeoffs
- different stakeholders would disagree
- output will influence a real decision
- content faces an open choice between audiences, angles, or versions and the audience lenses will decide it (a single finished draft that just needs critique goes to adversarial-review)
- strategy needs a financial/brand/operational pressure-test
- Literal asks: "devil's advocate", "what am I missing", "compare perspectives", "look at this from different angles", "audit against multiple criteria"
- "Stress test this" is shared with adversarial-review. It routes here when the object is a set of options or stakeholder tradeoffs to weigh; it routes to adversarial-review when the object is one finished artifact to critique. If the ask is generic, confirm which before starting.

## When not to use
- simple factual questions → answer directly
- single-path execution tasks → just do the task
- already well-structured decision with clear criteria → apply the criteria
- low-impact reversible choices → pick one and move
- critique of a single finished artifact rather than a decision between options → use adversarial-review

## Inputs
- The decision, question, strategy, or draft under review
- Its domain and decision type (strategy / pricing / content / architecture / hiring / other)
- Success criteria (what a good answer looks like) and stakes (how reversible)
- Optionally: specific lenses the user wants applied

## Method

Copy this checklist and check items off as you go:
- [ ] Step 1 — Frame the decision (objective, domain, type, success criteria, stakes)
- [ ] Step 2 — Determine perspectives (user-specified / pre-built set / auto-decompose)
- [ ] Step 3 — Run the fan-out (each lens as an independent analysis)
- [ ] Step 4 — Present per-perspective results, then the synthesis
- [ ] Step 5 — Run the reviewer check
- [ ] Step 6 — Capture the synthesis if it's worth keeping (optional)
- [ ] Step 7 — Close: offer to drill deeper, refine, or save

### Step 1: Frame the Decision

Before fan-out, clarify the decision frame:

1. **Objective:** What decision or question are we stress-testing?
2. **Domain:** What area does this touch? (product / marketing / finance / operations / etc.)
3. **Decision type:** Strategy / pricing / content / architecture / hiring / other
4. **Success criteria:** What would a good answer look like?
5. **Stakes:** How reversible is this? (guides depth — low stakes = 2 perspectives, high = 4)

If the opening message already answers these, extract and confirm. Don't re-ask.

### Step 2: Determine Perspectives

**If the user specifies lenses:** use them directly.
**If the decision type matches a known set:** use the pre-built set from [`references/perspective-sets.md`](references/perspective-sets.md)
(decision stress test, business evaluation, content review, pricing, architecture, hiring, research).
**If neither:** auto-decompose — pick lenses that are independent (each grounded in its own criteria and evidence) and genuinely capable of disagreeing, not different framings of the same conclusion. Capability to disagree is the requirement; if independent lenses honestly converge, that convergence is a real signal — report it, don't manufacture a split.

**Scaling rules:**
- Low stakes / reversible: 2 perspectives (lite mode)
- Standard: 3 perspectives (default)
- High stakes / irreversible: 4 perspectives (max)
- Four is the default cap — returns usually diminish past that. Exceed it only with a stated justification (e.g. a genuinely multi-stakeholder decision where a fifth lens holds veto power), and name the extra lens's distinct decision role.

Common perspective sets (full library in [`references/perspective-sets.md`](references/perspective-sets.md)):

- **Content review:** Target customer, Competitor, Internal team member, Casual browser
- **Strategy evaluation:** Financial lens, Brand/positioning lens, Operational feasibility, Competitive response
- **Decision stress-test:** Advocate (strongest case for), Skeptic (strongest case against), Pragmatist (implementation reality)
- **Research synthesis:** Themes extractor, Contradictions finder, Gaps identifier, Implications mapper

### Step 3: Run the Fan-Out

Run each perspective as an independent analysis — in parallel where possible, so no lens is anchored by another's conclusions. Give each worker the same task and context but a distinct role brief, and instruct it to argue its lens honestly rather than hedge toward consensus. Each worker produces one structured analysis (format below).

### Step 4: Present Results

For each perspective, the worker returns:

```
--- [Perspective Name] ---

CORE POSITION: [One sentence — what this perspective believes]

KEY ARGUMENTS:
- [argument 1]
- [argument 2]
- [argument 3]

RISKS / CONCERNS:
- [risk this perspective sees]

WHAT OTHERS ARE MISSING:
- [blind spot this perspective uniquely catches]
```

Then the synthesis:

```
SYNTHESIS

CONVERGENCE: Where perspectives agree (strong signal)
TENSION: Where they disagree (worth exploring)
BLIND SPOTS: What one perspective sees that others miss

DECISION IMPLICATION: What this means for the original decision
RECOMMENDED ACTION: proceed / adjust / test / hold
  - [concrete next step 1]
  - [concrete next step 2]
CONFIDENCE: High / Medium / Low — [1-line rationale]
```

### Step 5: Reviewer Check

After synthesis, verify:
- Were the lenses independent and capable of disagreeing? (If they all say the same thing because they share criteria or evidence, the decomposition failed — flag it. If they converge despite independent criteria, record it as genuine convergence and say so.)
- Did the synthesis collapse nuance? (If tensions were identified but the recommendation ignores them — flag it)
- Is the recommended action specific enough to execute? (If it says "consider further" — that's not actionable, push for a real recommendation)

If any check fails, note it explicitly.

### Step 6: Capture (optional)

If the analysis produced:
- A strong tension between perspectives (genuine disagreement worth tracking), OR
- A novel insight no single perspective would have found alone

Then offer to save the synthesis and decision recommendation for later reference.

### Step 7: Close

Ask the user:
- "Any perspective you want to drill deeper on?"
- "Want me to refine any single output further?"
- "Should I save this for reference?"

### Refinement Loop

If any perspective output is weak (generic, doesn't actually differ from others, not opinionated enough), run it through a short evaluate-and-improve loop against explicit criteria, for example:

- Must stake out a position specific enough that another perspective could disagree with it on a named point
- Core position must be a clear, testable claim — not a hedge
- Risks section must name something the other perspectives missed
- Under 300 words

Also apply this to the synthesis if the reviewer check flags issues:
- Perspectives not materially different because they shared criteria → re-run decomposition with independent lenses
- Recommendation not actionable → revise the synthesis with "must include concrete next steps"

## Output

Two blocks: one structured analysis per perspective (CORE POSITION / KEY ARGUMENTS / RISKS / WHAT OTHERS ARE MISSING), followed by a single SYNTHESIS block (CONVERGENCE / TENSION / BLIND SPOTS / DECISION IMPLICATION / RECOMMENDED ACTION / CONFIDENCE) — exact templates above.

## Example

Input: "Should we raise our flagship service from a flat $5k project fee to a $2k/month retainer?" Domain: pricing. Stakes: moderate, reversible within a quarter → 3 perspectives (Financial, Brand/positioning, Operational feasibility).

Output:

```
--- Financial lens ---

CORE POSITION: The retainer is worth it only if average engagement runs past 2.5 months.

KEY ARGUMENTS:
- $2k/mo beats $5k flat at month 3 and compounds after.
- Recurring revenue smooths cash flow and lifts company valuation multiples.
- Predictable MRR makes hiring and forecasting tractable.

RISKS / CONCERNS:
- Short engagements (<2.5 mo) earn less than the flat fee did.

WHAT OTHERS ARE MISSING:
- Nobody priced the churn month — the first cancel-heavy month can wipe the gain.

--- Brand / positioning lens ---

CORE POSITION: A retainer repositions us from vendor to embedded partner — a level up.

KEY ARGUMENTS:
- "Partner on retainer" outranks "agency you hired once" in buyer perception.
- Ongoing relationship compounds referrals and case-study depth.
- Signals confidence in delivering continuous value.

RISKS / CONCERNS:
- Buyers wary of "endless invoice" may bounce at the word retainer.

WHAT OTHERS ARE MISSING:
- The financial lens treats price as a number; it's also a positioning signal.

--- Operational feasibility lens ---

CORE POSITION: We can't staff a retainer book at current headcount without dropping quality.

KEY ARGUMENTS:
- Retainers demand steady monthly output; project work let us batch and rest.
- Every active retainer is a standing capacity claim, not a one-time push.
- Onboarding overhead repeats if churn is high.

RISKS / CONCERNS:
- Overselling retainers before hiring produces missed deliverables and churn.

WHAT OTHERS ARE MISSING:
- Both other lenses assume delivery capacity we haven't confirmed.

SYNTHESIS

CONVERGENCE: Financial and brand both see upside — financial conditional on engagements
  running past 2.5 months, brand unconditional. Operations does not dispute the upside;
  it disputes that we can staff it today.
TENSION: Conditional financial upside (long engagements) plus brand upside vs an
  operational capacity gate that must clear before either can be realized.
BLIND SPOTS: Churn-month economics (financial) and staffing ceiling (ops) — each invisible to the others.

DECISION IMPLICATION: The retainer is a strong move gated on delivery capacity, not on pricing math alone.
RECOMMENDED ACTION: test
  - Pilot the retainer with 3 existing clients before repricing the public offer.
  - Model the churn month explicitly and confirm staffing for a full retainer book.
CONFIDENCE: Medium — upside is real but hinges on an unverified capacity assumption.
```

Then close (Step 7):

> Any perspective you want to drill deeper on — the operational capacity gate is the
> one carrying the decision. Want me to refine any single lens further, or save this
> synthesis for reference when the pilot results come back?

## Notes
- If all perspectives converge, check why: shared criteria or shared evidence means the decomposition failed — pick independent lenses and re-run. Independent lenses that still agree are a genuine strong signal; report the convergence rather than inventing a dissent.
- A recommendation of "consider further" is not actionable; push every synthesis to a real proceed / adjust / test / hold call.
- Pairs well with: **decision frameworks** (present a converged recommendation as a weighted decision matrix with user-supplied weights, or an argument map when there are no weights — tag any AI-filled judgments with an uncertainty marker either way); **planning workflows** (validate execution plans before committing); **content review** (run audience perspectives before a full editorial scorecard); **formal dialectic reviews** (this is the lightweight version — use a full Advocate/Skeptic/Referee process for the highest-stakes decisions); **research synthesis** (fan out as themes / contradictions / gaps / implications workers).
