---
name: product-dev-planning
description: >
  Runs a pre-build interrogation that stress-tests what is being built BEFORE execution
  starts — reducing material ambiguity, surfacing broken assumptions, and bounding scope —
  and ends with a build spec that aims to let a competent executor start work with minimal
  follow-up questions to the requester. Use after the decision to build is made, via a Full
  Review (six forcing questions, premise challenge, adversarial spec pass) or a Fast-Lane
  Spec (four required fields), or when the user says "let's spec this out", "we're building
  X", "plan this build", "scope this", "ready to build", "spec me", or "break this down".
  Scope: specs how to build, not whether to build; produces one build spec, including an
  initial task breakdown for the work it specs.
metadata:
  author: Hunter Marshall (https://www.mesteezo.com)
  license: MIT
---

# Product & Development Planning

A pre-build interrogation partner for work that has already been decided. It reduces
material ambiguity and surfaces broken assumptions before a single line of code, copy, or
workflow is written, and ends with a build spec that aims to minimize the follow-up
questions a competent executor has to bring back to the requester.

## The 60-second version

Produces a build spec a competent executor can start from without coming back with questions.

Confirm the decision to build is actually made, then get these on paper:

1. **Scope:** one sentence in scope, one sentence explicitly out of scope. The out-of-scope line is the one that prevents mid-build sprawl.
2. **Success:** the measurable signal that it worked, with a timeframe. Not "it shipped."
3. **Assumptions and failure mode:** top 3 assumptions, which one you trust least, and the most likely way this fails.
4. **Owner, reviewer, and the first consequential action:** who builds it, who reviews it, and the first step that touches something real or irreversible.

Skipped most often, costs the most: **the first consequential action**. Name it and state who approves it before execution starts, or the build quietly ships an external side effect nobody agreed to.

Full method below.

## When to use

- A decision to build has been made and the work needs to be specced before anyone
  executes it.
- Scoping an automated/agent build, an external launch, or multi-person execution.
- Bounding a build whose scope will otherwise expand mid-execution.
- Literal asks: "let's spec this out", "we're building X", "plan this build", "pre-build",
  "scope this", "what are we actually building", "spec me", "break this down", "ready to
  build", "design this before we start". Fast-lane triggers: "fast-lane spec", "quick
  spec", "lightweight spec".

## When not to use

- **The decision to build isn't settled** → step back and evaluate whether to build first
  (`strategic-planning`). This skill assumes the decision is made and specs how to do it.
- **You want to package a meeting into a plan for the team** → use a briefing tool. This
  interrogates a plan *before* the team gets it, to catch what's broken.
- **You need full multi-session program planning or sprint scheduling** → that runs
  *after* this skill. This skill does produce the initial task breakdown for the build it
  specs (see `Tasks proposed` in the output), but it does not sequence a program of work
  across sessions, sprints, or teams.

## Inputs

- A confirmed decision to build (not "let's build this" — an explicit yes).
- A rough description of what is being built.
- Who is executing (person or automated agent) and what governs shipping it externally.
- The requester available to answer forcing questions one at a time.

## Method

Copy this checklist and check items off as you go:
- [ ] Step 1 — Confirm the decision to build is made; redirect if it's soft (Phase 0)
- [ ] Step 2 — Select review mode (Full / Fast-Lane) + confirm executor and governance
- [ ] Step 3 — Ask the forcing questions one at a time (six for Full; Q1, Q2, Q6 for Fast-Lane)
- [ ] Step 4 — Premise challenge: agree 2–3 build premises (Full)
- [ ] Step 5 — Adversarial spec review pass (Full)
- [ ] Step 6 — Produce the build spec
- [ ] Step 7 — Run the completeness gates before declaring done

This skill ends with a build spec — including an initial task breakdown — that aims to let
a competent executor start work with minimal follow-up questions to the requester.

### Phase 0: Context Load & Mode Selection

#### Step 1: Confirm the decision is made

This skill assumes the decision to build has already been made. Before proceeding,
confirm that with the requester:

> "Confirming: the decision is made and we are speccing execution — not deciding
> whether to build. Yes or no?"

Acceptable yes responses: "Yes," "Confirmed," "We are building this." Anything softer
(including "let's build this," "I think so," "probably") triggers a redirect:

> "Sounds like the decision might not be fully settled. Do you want to step back and
> decide whether to build first? That prevents speccing the wrong thing. Or do you want
> to confirm explicitly that we are speccing, not deciding?"

If the requester explicitly re-confirms, proceed. If they want to decide first, exit
this skill.

#### Step 2: Select review mode

State the two options:

**Full Review (default — ~30 min):** Six forcing questions, premise challenge,
adversarial spec review pass, complete Build Spec. Use for: automated/agent builds,
external launches, multi-person execution, irreversible or partially-reversible work,
anything customer-facing or revenue-affecting.

**Fast-Lane Spec (~10 min):** Four required fields only (Scope, Success Signal,
Owner+Reviewer, First Consequential Action). No premise challenge. No adversarial pass.
Use for: low-risk reversible work under 2 hours, content experiments, small internal
changes, ops fixes.

My recommendation: [Full / Fast-Lane] because [one-line reason based on context].

A) Full Review
B) Fast-Lane Spec

Wait for the requester's choice before proceeding.

#### Step 3: Confirm executor and governance (both modes)

- Who is actually building this? (You / a teammate / an automated agent?)
- Does anything this build produces need human approval before it ships externally?
- State whatever applies explicitly — it will be enforced in the spec. The default
  posture: propose, get human approval before shipping anything external.

### Phase 1: The Forcing Questions

Ask ONE question at a time. State your read or a concrete recommendation before asking.
Wait for the response. Push once if the answer is too vague — then draft a proposed
answer rather than leaving the field undefined.

**Question format:**
> **[Q#] [Question name]**
> [The question]
>
> My read: [Your stated position or recommendation]
>
> A) [Option]
> B) [Option]
> C) [Option — if genuinely distinct path exists]

#### Fast-Lane Spec: ask only Q1 (Scope), Q2 (Success), Q6 (Governance)

For Fast-Lane, Q6 is modified to cover Owner + Reviewer + First Consequential Action.
Skip Q3, Q4, Q5, Phase 2, and Phase 3.

#### Full Review: ask all six in order.

#### Q1: Exact Scope

**Ask:** "Describe what's in scope in one sentence. Now describe what's explicitly
out of scope. Both have to be stated before we proceed — unbounded scope is the most
common reason builds fail."

**Push target:** Vague scope that sounds complete but expands in execution.

**What a good answer sounds like:** "In scope: [X]. Out of scope: [Y] and [Z]." If the
requester resists stating out-of-scope, push once: "What's the thing that will seem
obviously related but we are explicitly NOT doing this round?"

**If scope stays unclear after one push:** Draft a proposed scope statement based on
context and ask the requester to approve or edit. Don't leave scope undefined — undefined
scope materially increases the likelihood of failure, rework, or scope creep.

#### Q2: Success Definition

**Ask:** "How do we know this is done — not 'shipped,' but actually worked? What's
the measurable signal that confirms it achieved what it was supposed to achieve?"

**Push target:** "Done when it's live" / "When the team can use it."

**What a good answer sounds like:** A measurable outcome with a timeframe. "First
order placed within 7 days of launch." "The system processes 10 requests without
manual intervention." "Response time under 24 hours for 7 consecutive days." Specific
enough that a third party could confirm yes or no.

**If the requester struggles:** "What's the thing this build is supposed to change? How
would you know in 30 days that it changed?"

**Completeness gate:** A success signal without a measurable threshold and timeframe
is incomplete. Flag it.

#### Q3: Assumptions

**Ask:** "What has to be true for this to work? List the top 3 assumptions. Which one
are you least confident about?"

**Push target:** Unstated assumptions that blow up mid-build.

**What a good answer sounds like:** Three explicit statements with confidence ratings.
"This assumes the platform handles [X] natively (High)." "This assumes the system can
parse [Y] format (Medium)." "This assumes the reviewer has capacity for [Z] review
(Low)."

**After the answer:** "For the assumption you're least confident about — is there a
way to test it before we build the full thing, or does the build itself test it?"

#### Q4: Breaking Points

**Ask:** "What's the most likely way this fails? Not edge cases — the main scenario
where we build this and it doesn't work. What's the second most likely?"

**Push target:** Optimism bias. "It should work fine" is not an answer.

**What a good answer sounds like:** A specific failure mode with a root cause. "The
most likely failure is the system misclassifying a request and sending the wrong
response. Second most likely is the handoff between steps breaking when [X]." Concrete
enough to design a mitigation.

**After each failure mode:** "What's the mitigation? Who owns it?"

**Rollback check:** If this is irreversible or partially-reversible work, also ask:
"If we ship this and it goes wrong, what's the rollback plan? How fast can we undo it?"

#### Q5: Dependencies

**Ask:** "What does this build need that doesn't exist yet? What systems, people,
decisions, or external tools does this touch — and which of those are blockers vs.
nice-to-haves?"

**Push target:** Underestimated dependencies that get discovered mid-build.

**What a good answer sounds like:** A list, categorized as blockers or non-blockers.
"Blocker: the shared data store must be live before this runs. Non-blocker: the content
template is nice to have but not required to ship v1."

**Check against the prior decision if one exists:** Do any dependencies conflict with
the premises agreed when the decision was made? Flag if so.

#### Q6: Governance & Consequential Actions

**Ask in two parts:**

**Part A — Reviewers:** "Who reviews this before it ships? What does approval look
like — one review or a staged process?"

**Part B — First Consequential Action:** "What is the first consequential or
approval-gated action this build can take? An external message sent, a payment
processed, a public post published, a database migration, a customer-facing change?
Name the specific action that must NOT happen without explicit approval. If the build
is genuinely fully reversible with no external or customer-visible effect, record
'None — fully reversible' with a one-line justification."

**Push target on A:** Skipping the approval rule / governance that exists in someone's
head but isn't written into the spec.

**Push target on B:** "Nothing's really irreversible." That's almost never true for
customer-facing or brand-affecting work. Push: "What action, if an automated agent or
teammate took it autonomously, would you want to know about *immediately*? That's the
consequential action." Accept "None — fully reversible" only after that push and only
with a stated justification.

**What a good answer sounds like:**
- A: Named reviewers. Clear trigger for what requires human review vs. what can ship
  autonomously. Explicit statement of any auto-send prohibition.
- B: A specific action (e.g., "Sending an email to a customer," "Publishing to the
  live store," "Posting to the company's social account"). Plus: who must approve it
  before it happens. Or, for a genuinely reversible internal build, "None — fully
  reversible" plus the justification.

**If an auto-send hold applies:** State it explicitly — e.g., "Propose only; a human
approves before anything is sent externally, for the first 30 days from [start date]."

**Completeness gate:** Every build spec must name (1) a reviewer — a named human, or an
unambiguous accountable role where naming an individual isn't possible — and (2) the first
consequential or approval-gated action with its approval requirement, or the explicit
value "None — fully reversible" with a justification. If either field is blank or vague,
mark confidence Low and status incomplete.

### Phase 2: Premise Challenge

After all forcing questions, synthesize 2–3 premises — the core assumptions the build
rests on. State them explicitly. The requester must agree or revise before the spec is
written.

Format:
```
BUILD PREMISES:
1. [Premise] — Agree or revise?
2. [Premise] — Agree or revise?
3. [Premise] — Agree or revise?
```

**Example premises:**
- "The existing platform is the deployment target — no custom build."
- "This ships before [date] or it doesn't ship."
- "The team executes; a human reviews output before anything goes external."
- "v1 excludes [X] — that's a post-launch addition."

If the requester disagrees with a premise, revise and restate. Do not proceed until all
premises are agreed.

**Fast-Lane Spec:** Skip Phase 2.

### Phase 3: Adversarial Spec Review (Full Review only)

Before writing the final spec, run a lightweight adversarial check. Answer these five
questions as if you were a skeptical executor reading the spec cold:

1. **Completeness** — Is there anything an executor would need to ask about to get
   started? If yes, it goes in the spec.
2. **Scope creep risk** — Is there anything in the spec that could reasonably be
   interpreted as broader than intended? Narrow it.
3. **Assumption risk** — Is there an assumption in the spec that hasn't been stated
   explicitly? Surface it.
4. **Dependency gap** — Is there a dependency that hasn't been named? Name it.
5. **Governance gap** — Is there an output from this build that doesn't have a named
   reviewer? Is the first consequential action named with approval requirement?

If any of the five fail, loop back to the relevant forcing question before writing
the spec. Note what was caught in the spec under "Spec Review Notes."

**Fast-Lane Spec:** Skip Phase 3.

### Phase 4: Build Spec Output

Produce the build spec as a complete, standalone artifact. A good filename pattern:
`YYYY-MM-DD_[short-title]_build-spec.md`. The full template is in **## Output** below.
The spec is complete when a competent executor could pick it up and start building with no
material ambiguity left to resolve with the requester.

### Completeness Gates

Before declaring the spec done, run these checks. If any fail, mark the spec
`confidence: Low` and `status: incomplete` with `incomplete_reason` filled in.

| Field | Acceptable | Unacceptable |
|---|---|---|
| Owner / executor | Named person, agent, or unambiguous accountable role | "We" / "the team" / "TBD" |
| Reviewer | Named human, or an unambiguous accountable role (preferred over inventing a name) | "Someone eventually" / blank |
| First consequential action | Specific action + named approver, or "None — fully reversible" + justification | "Nothing's irreversible" (unjustified) / blank |
| Success signal | Measurable threshold + timeframe | "Done when it's live" / "feels right" |
| Scope out | At least one explicit exclusion | "Nothing — we'll see how it goes" |

A role is acceptable wherever a name is: "the ops lead", "the on-call engineer" — any
designation that resolves to exactly one accountable party. What fails the gate is
ambiguity ("we", "the team", "someone"), not the absence of a personal name.

For Fast-Lane Spec, the gates that apply are: Owner, Reviewer, First Consequential
Action, Success Signal. The other fields can be marked "Not assessed — Fast-Lane."

**Why:** A capable assistant can produce polished ambiguity. The completeness gates
catch artifacts that look complete but contain no actionable signal. Better an
incomplete spec that flags what's missing than a fully-filled spec that hides its own
weakness.

## Output

A complete, standalone build spec:

```
Title: [Build name — Pre-Build Spec]
Date: YYYY-MM-DD
Type: Workflow (repeatable process) | Task (one-shot build)
Review mode: full | fast-lane
Summary: [Max 3 sentences: what is being built, what it must achieve, who is executing]
Why it matters: [What breaks if this is built wrong or built ambiguously]

Key points:
  - Scope in: [from Q1]
  - Scope out: [from Q1]
  - Success signal: [from Q2 — must include measurable threshold and timeframe]
  - Key assumptions: [from Q3 — top 3 with confidence ratings, or "Not assessed — Fast-Lane"]
  - Breaking points: [from Q4 — top 2 with mitigations, or "Not assessed — Fast-Lane"]
  - Dependencies: [from Q5 — blockers vs. non-blockers, or "Not assessed — Fast-Lane"]
  - Reviewer: [from Q6 Part A]
  - First consequential action: [from Q6 Part B + approval requirement]

Premises agreed:
  - [premise 1, or "Skipped — Fast-Lane"]
  - [premise 2]
  - [premise 3]

Recommended actions:
  - [First action to start the build]
  - [Key checkpoint or review trigger]

Tasks proposed:
  - task: [Build task 1]
    owner: [named person or agent]
    due_date: YYYY-MM-DD
    priority: High | Medium | Low
    effort: Low | Medium | High
    depends_on: [dependency name or task]
    description: [What needs doing — specific enough to execute without clarification]

Governance:
  executor: [named person or agent]
  reviewer: [named human]
  first_consequential_action: [specific action + who must approve it]
  approval_checkpoint: [when in the build process approval is required]
  approval_model: [e.g., "Propose only; human approves before external send"]
  reversibility: reversible | partially_reversible | irreversible
  rollback_plan: [from Q4 if irreversible/partial — or "N/A — fully reversible"]

Confidence: Low | Medium | High
Status: complete | incomplete
# For incomplete specs only:
incomplete_reason: [why the session didn't finish, or omit]
missing_inputs: [list of fields that couldn't be filled, or omit]

--- Narrative sections (append below the structured block) ---

## Why It Matters
[Expand on why it matters. What gets built wrong or blows up if this spec is skipped?]

## Build Spec

### What We're Building
[One paragraph. No jargon. Clear enough for someone with no project context to
understand what this is and what it does.]

### Scope
**In scope:**
- [item]
- [item]

**Explicitly out of scope (v1):**
- [item]
- [item]

### Success Criteria
- [Measurable signal 1 with threshold and timeframe]
- [Measurable signal 2 with threshold and timeframe]

### Assumptions
| Assumption | Confidence | How It Gets Tested |
|---|---|---|
| [assumption] | High/Med/Low | [test or "build itself tests it"] |
| [assumption] | High/Med/Low | [test] |
| [assumption] | High/Med/Low | [test] |

### Breaking Points & Mitigations
| Failure Mode | Likelihood | Mitigation | Owner |
|---|---|---|---|
| [failure mode] | High/Med/Low | [mitigation] | [owner] |
| [failure mode] | High/Med/Low | [mitigation] | [owner] |

### Dependencies
**Blockers (must exist before build starts):**
- [dependency]

**Non-blockers (needed but not blocking):**
- [dependency]

### Governance
**Reviewer:** [Named human]
**Approval chain:** [Description of who approves what at which stage]
**First consequential action:** [Specific action that must NOT happen without explicit
approval]
**Approval checkpoint:** [When in the build process approval is required]
**Auto-send / auto-publish prohibitions:** [If an auto-send hold applies, state it
explicitly with start date]

### Rollback Plan
[If reversibility is partial or irreversible, describe how to undo if it goes wrong.
If fully reversible: "N/A — fully reversible."]

### Spec Review Notes
[What the adversarial pass caught and corrected. If nothing: "Spec review passed —
no gaps found." Fast-Lane: "Spec review skipped — Fast-Lane mode."]

## Open Questions
[Anything unresolved from the session that affects execution. If none: "None — spec
is complete."]
```

## Example

Input: "We're building an automated weekly email digest that summarizes the past week's
new support tickets for the ops lead. Decision's made, spec it. Full review." (Executor:
an automated agent. External send: yes, to one internal recipient.)

Output — **abridged excerpt, not a complete final spec.** The six questions were asked one
at a time. Shown below: the structured block in full, plus a subset of the narrative
sections. A real spec also carries `## Build Spec → Scope`, `Success Criteria`,
`Dependencies`, `Governance`, and `Rollback Plan` in narrative form; they are omitted here
only to keep the example short, and their content appears in the structured block above.

```
Title: Weekly Support-Ticket Digest — Pre-Build Spec
Date: 2026-07-23
Type: Workflow (repeatable process)
Review mode: full
Summary: An automated agent compiles the past week's new support tickets into a single
  digest email sent to the ops lead every Monday. It must reliably capture every ticket
  opened in the window and send on schedule. An automated agent executes; the ops lead
  reviews output.
Why it matters: If the digest silently drops tickets or misfires the send, the ops lead
  loses trust in it and reverts to manual review — the build's whole purpose fails.

Key points:
  - Scope in: summarize tickets opened in the trailing 7 days into one email, sent Mondays
  - Scope out: no ticket triage, no replies to customers, no analytics beyond a count
  - Success signal: 4 consecutive Mondays where the digest sends on time and its ticket
    count matches the source system exactly
  - Key assumptions: ticket source exposes a created-in-range query (High); the agent has
    send credentials for the internal mailbox (Medium); ops lead wants Monday cadence (High)
  - Breaking points: (1) missed tickets from a timezone/window boundary error;
    (2) scheduled send silently failing with no alert
  - Dependencies: blocker — read access to the ticket source; non-blocker — an HTML email
    template (plain text ships v1)
  - Reviewer: the ops lead
  - First consequential action: sending the digest email — must not send autonomously until
    the count has matched the source for the first send

Premises agreed:
  - "The ticket source is the single system of record; no manual entry is merged in"
  - "The digest is read-only — it never modifies or replies to a ticket"
  - "v1 sends plain text; formatting is a post-launch addition"

Recommended actions:
  - Build the trailing-7-day query and generate the first digest as a draft, not a send
  - Review draft against the source count with the ops lead before enabling the auto-send

Tasks proposed:
  - task: Build the query + digest generator and produce a draft for review
    owner: automated-agent
    due_date: 2026-07-28
    priority: High
    effort: Medium
    depends_on: read access to the ticket source
    description: Query tickets created in the trailing 7 days, render a plain-text digest,
      output as a draft (no send) for the ops lead to verify

Governance:
  executor: automated-agent
  reviewer: ops lead
  first_consequential_action: sending the digest email — ops lead must approve the first send
  approval_checkpoint: before the first live send; auto-send enabled only after count matches
  approval_model: Propose only; human approves the first send, then it runs autonomously
  reversibility: partially_reversible
  rollback_plan: disable the scheduled job; a sent email can't be recalled, so the count is
    verified before every send is enabled

Confidence: High
Status: complete

## Why It Matters
A digest that silently misses tickets is worse than no digest — it manufactures false
confidence. Speccing the window logic and the count-match gate up front is what keeps the
build from failing quietly.

## Build Spec

### What We're Building
A scheduled automated job that reads every support ticket opened in the past seven days
and emails a plain-text summary to the ops lead each Monday morning. It only reads and
summarizes; it never touches a ticket or contacts a customer.

### Assumptions
| Assumption | Confidence | How It Gets Tested |
|---|---|---|
| The ticket source can return every ticket created in a date range in one query | High | First draft's count is compared against the source system before any send |
| The agent has working send credentials for the internal mailbox | Medium | Send a test message to the mailbox before the first digest is generated | ops lead |
| A Monday cadence is what the ops lead actually wants | High | Confirmed at spec time; re-checked after the 4-week reconciliation window | ops lead |

### Breaking Points & Mitigations
| Failure Mode | Likelihood | Mitigation | Owner |
|---|---|---|---|
| Tickets opened near the window boundary are dropped by a timezone mismatch | Medium | Pin the query window to a single explicit timezone and reconcile counts for 4 weeks | ops lead |
| The scheduled send fails silently and no digest arrives, with no alert raised | Medium | Emit a run-stamp on every execution and alert the ops lead if no digest is recorded by Monday noon | ops lead |

### Spec Review Notes
The adversarial pass caught an unstated dependency (send credentials for the internal
mailbox) and a scope-creep risk (an early draft implied light triage). Both were pulled
back into Q5 and Q1 before finalizing.

## Open Questions
- None — spec is complete.
```

## Notes

- **Single session.** The spec is produced at the end of this session or marked
  incomplete with `incomplete_reason` and `missing_inputs`. No multi-day state.
- **Confirm the decision first.** This skill does not decide whether to build. "Let's
  build this" is not commitment until the requester says yes to the explicit
  confirmation question.
- **Mode selected at Phase 0.** Full Review or Fast-Lane Spec — chosen based on stakes.
  Cannot switch mid-session.
- **One question at a time.** Never batch questions. State your read before asking.
  Wait for the response.
- **Push once, then draft.** If the first answer is vague, push once. If still vague,
  draft a proposed answer based on context and ask the requester to approve or correct
  it. Never leave a critical field undefined.
- **Premises before spec (Full Review).** Do not write the spec until premises are
  agreed. A disagreed premise changes the spec.
- **Adversarial pass before finishing (Full Review).** Run Phase 3 before producing the
  final spec. A spec that survives the five-question adversarial check is ready for
  execution.
- **Governance is mandatory.** Every spec must name a reviewer and the first
  first consequential action with an approval requirement (or an explicit, justified "None — fully reversible"). "The requester reviews" is
  acceptable only with a defined trigger. "TBD" is not.
- **No strategy.** This skill specs the build. It does not re-evaluate whether to
  build. If the requester raises "should we be doing this at all" mid-session, note it
  as an open question and flag that a strategy step should run if the doubt is serious.
- **Completeness gates are not optional.** Run them before declaring the spec
  complete. Flagging weakness is more valuable than hiding it.
