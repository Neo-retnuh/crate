---
name: strategic-planning
description: >
  Runs a pre-commitment interrogation that stress-tests an initiative, opportunity,
  partnership, or decision BEFORE commitment, and ends with a structured decision
  write-up. Use when evaluating whether to pursue something (not how to execute it) —
  via a Full Review (six forcing questions, premise challenge, three paths) or a Fast
  Review (three questions, two paths) — or when the user says "should we do this", "is
  this worth pursuing", "evaluate this", "stress-test this plan", "pre-mortem", "does
  this make sense", or "is this the right move". Scope: evaluates whether to commit, not
  how to build; produces one decision artifact, not a brief, plan, or task list.
metadata:
  author: Hunter Marshall (https://www.mesteezo.com)
  license: MIT
---

# Strategic Planning

A pre-commitment interrogation partner that surfaces what the decision-maker doesn't
know before they commit — not to validate what they've already decided. It produces a
structured decision artifact that says whether to pursue an initiative, and why.

## The 60-second version

Produces a go / no-go decision artifact on an initiative you have not committed to yet.

Answer these out loud, one at a time, before you commit:

1. **Pull:** what specific person, dollar, or deadline is asking for this? "It makes strategic sense" is not pull.
2. **Cost of passing:** what actually degrades if you do nothing? If the answer is FOMO, pass.
3. **Owner and displacement:** name the accountable human, then name what they stop doing to make room.
4. **Narrowest version:** the two-week test that would tell you whether to go deeper.
5. **Kill criteria:** the signal that makes you stop, written down before you start.

Skipped most often, costs the most: **kill criteria**. Without a pre-defined exit you will fund a losing bet on momentum alone. Write it before the first dollar or hour goes in.

Full method below.

## When to use

- Deciding whether to pursue an initiative, opportunity, partnership, or move — while
  you can still walk away.
- Evaluating an inbound pitch or someone else's idea you haven't formed a view on.
- Pressure-testing a direction you're leaning toward but haven't committed to.
- Literal asks: "should we do this", "is this worth pursuing", "evaluate this",
  "stress-test this plan", "pre-mortem", "does this make sense", "is this the right move".

## When not to use

- **The decision is already made and confirmed** → go spec the build instead
  (`product-dev-planning`). This skill questions whether the work should happen; it does
  not decompose known work or spec how to do it.
- **You want a decision record of a choice already made** → use a decision-log tool.
  This interrogates decisions *before* they're made.
- **You want to package an agreed plan for the team** → use a briefing tool. This
  questions whether the plan should exist at all.
- **You're just thinking out loud** → this skill produces a formal artifact; exit if the
  conversation is exploratory.

## Inputs

- The initiative, opportunity, partnership, or decision under consideration.
- Confirmation that the decision is genuinely still open (not already committed).
- The decision-maker available to answer forcing questions one at a time.

## Method

Copy this checklist and check items off as you go:
- [ ] Step 1 — Context check: prior-decision check + confirm evaluation intent (Phase 0)
- [ ] Step 2 — Select review mode (Full / Fast) and, for Full, identify framing
- [ ] Step 3 — Ask the forcing questions one at a time (six for Full; Q1, Q3, Q5 for Fast)
- [ ] Step 4 — Premise challenge: agree 2–3 premises before paths (Full)
- [ ] Step 5 — Present paths (three for Full, two for Fast) + a one-line recommendation
- [ ] Step 6 — Produce the decision write-up
- [ ] Step 7 — Run the completeness gates before declaring done

This skill ends with a structured decision artifact, not a pep talk.

### Phase 0: Context Check & Mode Selection

Before any questions, orient the session.

#### Step 1: Prior-decision check

Ask: "Has this already been decided? Or are we genuinely still deciding?"

If it's already decided and the decision-maker confirms commitment → redirect: "Sounds
like the decision is made — you probably want to spec the build instead of re-litigating
whether to do it."

#### Step 2: Confirm evaluation intent

Ask: "Confirming you want a structured evaluation — not just thinking out loud — yes
or no?"

If they say "just thinking out loud," exit the skill politely and let the conversation
continue without the formal structure. Do not produce a decision artifact for an
exploratory conversation.

If yes, proceed to Phase 0 Step 3 (Select review mode).

#### Step 3: Select review mode

State the two options and recommend based on initial framing:

**Full Review (default — ~25 min):** Six forcing questions, premise challenge, three
paths, complete decision write-up. Use for: partnerships, major builds, brand launches,
significant financial commitments, irreversible or hard-to-reverse moves.

**Fast Review (~8 min):** Three questions only (Pull, Owner + Displacement, Kill
Criteria). Minimal premise check. Two paths (Do It / Pass). Use for: low-risk reversible
moves, content experiments, small ops decisions, anything you'd otherwise just decide
in your head.

My recommendation: [Full / Fast] because [one-line reason].

A) Full Review
B) Fast Review

Wait for the decision-maker's choice before proceeding.

#### Step 4: Identify framing (Full Review only)

For Full Review, identify the framing:

**Evaluate mode** — the decision-maker is assessing an external opportunity they haven't
formed a view on yet. (Inbound pitch, new initiative, someone else's idea.)

**Pressure-test mode** — they have a direction but want adversarial challenge before
committing. (They think they want to do this but aren't sure.)

If unclear, ask: "Are you leaning toward this and want me to poke holes in it, or are
you still deciding whether to engage at all?"

State the framing and proceed to Phase 1.

### Phase 1: The Forcing Questions

Ask ONE question at a time. State your recommended answer or position before asking.
Wait for the response before moving to the next question. Push once if the first answer
is vague — then accept it and move on.

**Question format:**
> **[Q#] [Question name]**
> [The question]
>
> My read: [Your stated position on what the answer probably is or should be]
>
> A) [Option]
> B) [Option]
> C) [Option — if a genuinely distinct path exists]

#### Fast Review path: ask only Q1, Q3, Q5 — then go to Phase 3 with two-path output. No formal premise challenge; one premise may still be surfaced inline (see Phase 2).

#### Full Review path: ask all six in order.

#### Q1: Demand / Pull

**Ask:** "What's the strongest evidence this needs to happen — not that it's a good
idea, but that there's actual pull? Something breaks, someone's waiting, money is on
the table, a deadline is real?"

**Push target:** "It makes strategic sense" / "It's a good opportunity" / "Everyone's
doing it" — none of these are pull.

**What a good answer sounds like:** A named person waiting on this. Revenue at risk.
A commitment already made to someone external. A window that closes.

**If the answer is vague:** Push once — "Can you point to a specific person, dollar
amount, or deadline attached to this?" If still vague, mark Q1 as "weak pull evidence"
in the write-up and move on. Weak pull is itself a signal.

#### Q2: Status Quo Cost

**Ask:** "What's the cost of passing? If we don't do this, what specifically gets worse,
degrades, or stays broken? Not FOMO — actual cost."

**Push target:** "We'd miss the opportunity" without specifics.

**What a good answer sounds like:** A concrete thing that doesn't get done, a
relationship that atrophies, a capability gap that stays open, revenue that doesn't
materialize, a competitor that gains ground.

**If the answer is vague:** "What's the next-best alternative if we pass? If there's
a good one, passing is probably fine."

#### Q3: Ownership & Displacement

**Ask in two parts:**

**Part A — Ownership:** "Who is the named human accountable for this succeeding — not
'we' or 'the team'? What happens to that person if it fails? Who reviews their work?"

**Part B — Displacement:** "What current priority, relationship, or system loses time
or attention if we do this? What gets pushed back or dropped?"

**Push target on A:** Vague "we" ownership. Shared accountability is workable only when
decision rights and individual responsibilities are named explicitly — if it isn't clear
who decides and who is responsible for which part, treat the ownership answer as unmet.
**Push target on B:** "Nothing — we have capacity." That's almost never true. Push:
"If you're spending 5 hours a week on this, what 5 hours are you not spending on
something else?"

**What a good answer sounds like:**
- A: One name. A consequence if they fail. A review cadence.
- B: A specific current priority that loses attention. For self-owned initiatives:
  explicit acknowledgment of which existing work slows down.

**If the decision-maker is the owner:** "You're the owner — is that the right call given
your current load? Who's your backstop? What's getting deprioritized to make room?"

**Why displacement matters:** Opportunity cost is usually the real killer. Most people
don't fail because they pick bad ideas — they fail when good new ideas crowd out good
existing commitments. Surface the trade explicitly.

#### Q4: Narrowest Version

**Ask:** "What's the smallest version of this we could run in about 2 weeks that would
tell us whether to go deeper? Not a prototype — an actual test of the core assumption."

**Window guideline:** Two weeks is the default, not a hard rule. A different window is
acceptable when the test's own signal requires it — state the justification in the
write-up (e.g., a weekly product needs four issues before an open-rate trend is
readable). An unjustified longer window is scope creep; a justified one is not.

**Push target:** "We need to do the whole thing before we know" / "It can't be
de-risked incrementally."

**What a good answer sounds like:** A specific action with a specific signal. Run one
call. Send one email. Publish one thing. Commit one dollar. Something that produces
information, not just output.

**If no narrowest version exists:** Flag it explicitly — "The inability to test
incrementally is itself a risk. Note it in the premises."

#### Q5: Kill Criteria

**Ask:** "What would make us stop? Name the specific signal — before we're too far in
— that says 'this is failing' or 'this was the wrong call.' What do we need to see by
when to keep going?"

**Push target:** No pre-defined exit / "We'll know it when we see it."

**What a good answer sounds like:** A measurable signal. A date. A threshold. "If we
don't have X by Y, we stop." Not a feeling.

**If the decision-maker resists:** "Defining the exit before we start isn't pessimism —
it's the thing that lets us move fast without sunk cost. What would disappoint you
enough to quit?"

**Completeness gate:** If kill criteria stays vague after one push, confidence on the
overall write-up drops to Low. Vague kill criteria = vague decision.

#### Q6: Compounding / Future-Fit

**Ask:** "Six months from now, does doing this make the next thing easier or harder?
Does it open options or close them? How does it compound into your larger goals?"

**Push target:** "The market is growing" / "AI will make it better" — rising tide
arguments any competitor can make.

**What a good answer sounds like:** A specific claim about how this initiative changes
your position — what capability it builds, what relationship it opens, what you learn
from running it.

**Smart routing:** If earlier answers already covered this question clearly, skip it
and note "Q6 covered in [Q#] answer."

### Phase 2: Premise Challenge

After all forcing questions, synthesize 2–3 premises — the core assumptions the
initiative rests on. State them explicitly. The decision-maker must agree or revise
before paths are presented.

Format:
```
PREMISES WE'RE PROCEEDING ON:
1. [Premise] — Agree or revise?
2. [Premise] — Agree or revise?
3. [Premise] — Agree or revise?
```

If the decision-maker disagrees with a premise, revise the understanding and restate.
Do not proceed to Phase 3 until all premises are agreed.

**Fast Review:** Skip formal premise challenge. Surface one premise inline if it
emerges naturally from the three questions. Otherwise proceed directly to Phase 3.

**Purpose:** This is the most important phase of Full Review. Premise disagreements
that surface here would have derailed execution later. Surfacing them now is the whole
point.

### Phase 3: Paths

#### Full Review: Present 3 paths.

```
PATH A: Full Pursuit
  What: [1-2 sentences]
  Effort: [S/M/L/XL] — decision-maker time + team time
  Risk: [Low/Med/High]
  Reversibility: reversible | partially_reversible | irreversible
  Upside if right: [specific]
  Downside if wrong: [specific]

PATH B: Minimum Viable Test
  What: [the narrowest version from Q4]
  Effort: [S/M/L/XL]
  Risk: [Low/Med/High]
  What this test proves: [specific]
  Decision point after: [date/signal]

PATH C: Pass / Park
  Why passing might be right: [honest case for not doing this]
  What "park" looks like: [if it's a timing issue, what changes the answer]
  What we'd be giving up: [specific]
```

#### Fast Review: Present 2 paths (Do It / Pass).

```
PATH A: Do It
  What: [the action]
  Effort: [S/M/L]
  Reversibility: reversible | partially_reversible
  Kill criteria: [from Q5]

PATH B: Pass
  Why passing might be right: [one-line case]
  Cost of passing: [from Q2 or "low, given reversibility"]
```

**Recommendation:** State which path you recommend and why, in one sentence.

### Phase 4: Decision Write-Up

Produce a complete, self-contained decision artifact the decision-maker can save.
Suggested filename pattern: `YYYY-MM-DD_Decision_[short-title].md`. The full template is
in **## Output** below.

### Completeness Gates

Before finishing, run these checks. If any fail, mark the write-up `confidence: Low`
and `incomplete_reason` filled in.

| Field | Acceptable | Unacceptable |
|---|---|---|
| Owner | A named human, or an unambiguous single accountable individual (e.g. the self-owning decision-maker) | "We" / "the team" / "TBD" |
| Kill criteria | Measurable signal + date or threshold | "We'll know" / "feels off" / blank |
| Path recommendation | A, B, or C with one-line rationale | "It depends" / blank |
| Pull evidence (Q1) | Named person, dollar amount, or deadline | "Makes sense" / "good opportunity" |
| Opportunity cost (Q3B) | What loses attention | "Nothing — we have capacity" |

**Why:** It's easy to produce polished ambiguity. The completeness gates catch
artifacts that look complete but contain no actionable signal. Better an incomplete
write-up that flags what's missing than a fully-filled one that hides its own weakness.

## Output

A complete, self-contained decision artifact:

```yaml
---
date: YYYY-MM-DD
type: Decision
title: [Initiative name — Strategic Review]
summary: [Max 3 sentences: what was evaluated, what was found, what is recommended]
why_it_matters: [What breaks or is missed if this decision is delayed or made badly]
review_mode: full | fast
key_points:
  - Pull evidence: [from Q1]
  - Status quo cost: [from Q2, or "Not assessed — Fast Review"]
  - Owner: [from Q3 Part A]
  - Opportunity cost / displacement: [from Q3 Part B]
  - Narrowest test: [from Q4, or "Not assessed — Fast Review"]
  - Kill criteria: [from Q5]
  - Compounding effect: [from Q6, or "Not assessed — Fast Review"]
premises_agreed:
  # Full Review: 3 agreed premises.
  # Fast Review: one optional premise if one surfaced inline, otherwise the single
  # entry "Not assessed — Fast Review".
  - [premise 1]
  - [premise 2]
  - [premise 3]
decision_rationale: [Why the recommended path wins over the others, in 1-2 sentences]
handoff_trigger: >
  [What must happen for execution planning to begin, and where it goes — e.g.
  "If Path B is accepted, hand off to product-dev-planning to spec the pilot."
  Execution actions and task decomposition are NOT produced here.]
decision_status: recommended | decided | parked | needs_more_info
owner: [named person]
next_review_date: YYYY-MM-DD
decision_deadline: [date by which a decision must be made, or "N/A"]
next_decision_trigger: [signal that prompts revisiting, e.g., "After narrowest test results"]
effort: Low | Medium | High
tags: [strategic-review, initiative-name, relevant-tags]
confidence: Low | Medium | High
impact_level: Low | Medium | High
path_recommended: A | B | C
kill_criteria: [from Q5 — the specific signal that says stop]
reversibility: reversible | partially_reversible | irreversible
# For incomplete write-ups only:
incomplete_reason: [why the session didn't finish, or omit]
missing_inputs: [list of fields that couldn't be filled, or omit]
---

## Why It Matters
[Expand on why_it_matters. What breaks or gets worse if this decision is delayed?]

## Session Summary
[3-5 sentence narrative of what was interrogated and what the questioning revealed.
Not a transcript — a synthesis. What did we learn that the decision-maker didn't walk
in knowing?]

## Path Analysis
[Paste the paths from Phase 3 here — complete Phase 3 format for every path]

## Decision & Rationale
[The recommended path and why it beats the alternatives. This is where the artifact
ends: the decision and its reasoning, not an execution plan.]

## Handoff
[The trigger that moves this into execution planning, and the destination
(`product-dev-planning`). Do not list build actions or tasks here.]

## Open Questions
[Anything unresolved from the session that affects the decision. If none: "None."]
```

## Example

Input: "Should we launch a paid weekly newsletter? I keep thinking it's a good idea but
haven't committed. Full review." (Framing: pressure-test.)

Output (abridged — the six questions were asked one at a time; this is the final
artifact):

```yaml
---
date: 2026-07-23
type: Decision
title: Paid Weekly Newsletter — Strategic Review
summary: >
  Evaluated whether to launch a paid weekly newsletter. Pull is weak (no one waiting,
  no revenue committed) but a low-cost narrowest test exists. Recommend Path B: run a
  4-week free pilot to a warm list before committing to a paid product.
why_it_matters: >
  Committing to a weekly cadence is a standing obligation that displaces existing client
  delivery; launching paid before proving open rates risks refunds and reputation cost.
review_mode: full
key_points:
  - "Pull evidence: weak — no named subscriber waiting, no committed revenue; interest is inferred, not demonstrated"
  - "Status quo cost: low — passing costs nothing concrete; audience stays reachable through existing channels"
  - "Owner: the decision-maker (self-owned)"
  - "Opportunity cost / displacement: ~5 hrs/week that currently goes to client delivery"
  - "Narrowest test: 4 free issues to the existing ~300-person list; measure open rate and reply rate (4 weeks rather than the 2-week default — justified: a weekly product needs 4 issues to read a trend)"
  - "Kill criteria: if open rate <30% or fewer than 10 replies expressing willingness to pay by end of week 4, stop"
  - "Compounding effect: builds a publishing muscle and an owned audience even if the paid product is dropped"
premises_agreed:
  - "The existing ~300-person list is the launch audience — no paid acquisition in the test"
  - "Weekly cadence is the hard constraint; a slower cadence is a different product"
  - "The pilot runs free; no payment is taken until the test clears kill criteria"
decision_rationale: >
  Path B wins because the pull evidence is inferred rather than demonstrated, and a cheap
  reversible test can convert that inference into a real signal before any money or public
  cadence commitment is made.
handoff_trigger: >
  If Path B is accepted, hand off to product-dev-planning to spec the 4-issue pilot build.
  No execution actions or task decomposition are produced in this artifact.
decision_status: recommended
owner: "self"
next_review_date: 2026-08-24
decision_deadline: "N/A"
next_decision_trigger: "After 4-week pilot metrics are in"
effort: Medium
tags: [strategic-review, newsletter, content]
confidence: Low
impact_level: Medium
path_recommended: B
kill_criteria: "Open rate <30% or fewer than 10 pay-intent replies by end of week 4"
reversibility: reversible
incomplete_reason: >
  Pull evidence stayed weak after one push (no named person waiting, no committed
  revenue), so the completeness gate on Q1 was not met. The recommendation stands, but
  confidence is Low until the pilot supplies demonstrated demand.
missing_inputs: ["Pull evidence (Q1) — no named person, dollar amount, or deadline"]
---

## Why It Matters
A weekly newsletter is a recurring commitment, not a one-off. If launched paid before
demand is proven, the downside is refunds and a public miss; the pilot converts that
irreversible-feeling launch into a cheap, reversible experiment.

## Session Summary
The decision-maker walked in leaning toward launching. Interrogation revealed the pull
was inferred, not demonstrated — no one was actually waiting and no revenue was
committed. Displacement was real (5 hrs/week off client work). Because a genuine
narrowest test existed and kill criteria were nameable, the honest move is to test
before committing to a paid product, not to launch on conviction. The test runs longer
than the 2-week default: a weekly product needs four issues before the open-rate signal
is readable, which is a justified departure under the Q4 window guideline.

## Path Analysis
PATH A: Full Pursuit
  What: Launch the paid weekly newsletter now, with a public price and a weekly cadence.
  Effort: L — decision-maker time weekly, no team time
  Risk: High
  Reversibility: partially_reversible
  Upside if right: Recurring revenue from week one and a public cadence that compounds.
  Downside if wrong: Refunds, cancellations, and a visible miss on a public commitment.

PATH B: Minimum Viable Test
  What: 4 free weekly issues to the existing ~300-person list.
  Effort: S
  Risk: Low
  What this test proves: Whether the warm list actually opens and replies — demonstrated
    demand rather than inferred interest — before any money changes hands.
  Decision point after: 2026-08-24, against the stated kill criteria.

PATH C: Pass / Park
  Why passing might be right: Pull is inferred, the audience is already reachable through
    existing channels, and 5 hrs/week is currently funding client delivery.
  What "park" looks like: Revisit if the list grows past 1,000 organically or a named
    subscriber asks to pay.
  What we'd be giving up: The publishing muscle and the owned-audience compounding effect.

## Decision & Rationale
Path B. Pull is the weakest input in the review, and Path B is the only option that
converts it into evidence at low cost; Path A commits public cadence and money against an
unproven signal, and Path C forfeits the compounding effect for no saving beyond 5 hrs/week.

## Handoff
If Path B is accepted, hand off to `product-dev-planning` to spec the pilot build (issue
production, send mechanics, metric capture). No build actions or tasks are specified here.

## Open Questions
- Pricing is unresolved and out of scope until the pilot clears kill criteria.
```

## Notes

- **Single session.** The write-up is produced at the end of this session or marked
  incomplete with `incomplete_reason` and `missing_inputs`. No multi-day state.
- **One output type.** This skill produces a decision write-up. Not a brief, not a
  plan, not a task list. The artifact ends at the decision, its rationale, and the
  handoff trigger.
- **Execution belongs elsewhere.** Recommended actions and task decomposition are owned
  by `product-dev-planning`, not by this skill. Name the handoff trigger and stop.
- **One question at a time.** Never batch questions. State your recommendation before
  asking. Wait for the response.
- **Push once, then accept.** If the first answer is vague, push once for specificity.
  If the second answer is still vague, note the ambiguity and move on — don't
  interrogate in circles.
- **Premises before paths.** Do not present alternatives until premises are agreed
  (Full Review). A disagreed premise changes the paths.
- **Three paths in Full, two in Fast.** Pass/Park is always a valid path and must be
  honestly presented.
- **No implementation.** This skill evaluates whether to do something. It does not
  design how to do it. If "how" questions surface, capture them as open questions in
  the write-up.
- **Completeness gates are not optional.** Run them before declaring the write-up
  complete. Flagging weakness is more valuable than hiding it.
