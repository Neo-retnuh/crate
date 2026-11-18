---
name: campaign-brief-builder
description: >
  Turns a loose campaign idea into a one-page, executable campaign brief
  (objective, audience, core message, channel plan, metrics, owners) so the
  team can start work without a follow-up meeting to figure out what we're
  running. Open questions are carried explicitly rather than hidden. Use when
  kicking off a marketing campaign, content sprint, product launch, or
  promotion; when someone says "let's run a campaign for X," "we need a brief
  for this launch," or "write up the campaign plan"; or when a good idea is
  stuck as a chat thread instead of a plan.
metadata:
  author: Hunter Marshall (https://www.mesteezo.com)
  license: MIT
---

# Campaign Brief Builder

A campaign dies in the gap between "we should do a campaign for this" and "here's exactly what we're running, who owns it, and how we'll know it worked." This skill closes that gap: it takes a rough idea and forces it into a single-page brief specific enough to execute and honest enough to trust. The output is a plan, not a wish.

## When to use
- Kicking off a marketing campaign, content sprint, product launch, seasonal promotion, or announcement.
- A campaign idea is scattered across a chat thread or a call and needs to become one actionable document.
- Handing execution to a team, a freelancer, or an agency who wasn't in the room.
- Literal asks: "let's run a campaign for X", "write me a campaign brief", "we need a plan for this launch", "brief the team on this promo".

## When not to use
- You haven't decided *whether* to run it. Decide first with `strategic-planning` (the pre-commitment stress-test), then brief. Running standalone without the rest of the gallery, answer "what has to be true for this to be worth doing, and is it?" before you fill a single field.
- It's one piece of content, not a campaign. The boundary: `content-sharpener` shapes a single piece; this skill plans one multi-asset campaign (several assets, several channels, one objective). One post with a repost is not a campaign.
- You need brand voice or tone rules — extract those separately with a voice guide.
- You need the individual assets written — brief first, then draft the content.

## Inputs
- The campaign idea, in whatever rough form it exists (a sentence, a thread, call notes).
- What you know so far: the goal, the audience, the timing, the offer. Gaps are fine — the method surfaces them.
- Optional: a brand voice guide, past campaign results, budget ceiling, hard deadlines.

## Method
Copy this checklist and check items off as you go:
- [ ] Draft each field of the brief from what's known; mark unknowns explicitly
- [ ] Prompt for the missing must-haves (objective, audience, timing, owner)
- [ ] Run the four quality tests and fix any failures
- [ ] Deliver the one-page brief with confidence flags on anything assumed

**Step 1 — Draft the brief.** Fill the output template below from the raw input. Where a field is unknown, write `[NEEDS INPUT: <question>]` rather than guessing — a visible gap is safer than a confident invention.

**Step 2 — Close the must-have gaps.** A brief cannot ship without: a measurable objective, a specific audience, a timeframe, and a named campaign owner. If any is missing, ask for it before proceeding. Everything else can carry an assumption flag.

**Step 3 — Run the four quality tests.** The brief must pass all four:
- **One-Page test** — hard budget: **≤ 400 words total, ≤ 2 lines per field.** One exemption: the Content plan is a repeating list, so each per-asset entry counts as one line and the field's budget is one line per asset. Count them. Over budget means the thinking isn't done; cut until it fits rather than shrinking the type.
- **Why-Now test** — is there a real reason this campaign runs *now* (a launch, a season, a moment)? If "now" is arbitrary, say so; arbitrary timing is a weak campaign.
- **Ownership test** — ownership is checked at two levels, and both must pass. Campaign level: does the **Campaign owner** field name exactly one person accountable end to end? Asset level: does every deliverable name exactly one owner, inline in the Content plan? At either level, an owner is a person by name, or a single named role held by one person (e.g. "lifecycle marketer"). Explicitly: a role counts only when one person holds it. "The team", "marketing", or two names on one asset all fail. "The team" owns nothing.
- **Honesty test** — are the metrics ones you'll actually track, and the budget real? Strip vanity metrics and aspirational numbers you won't measure.

**Step 4 — Deliver.** Present the one-page brief. Two markers, used literally in the delivered text:

- `⚑ assumed` — appended to any value you inferred rather than were told. Every invented number, segment definition, discount, date, and owner carries it. A brief with no flags on a thin input is lying about how much it knows.
- `[NEEDS INPUT: <question>]` — for anything you could not responsibly invent at all.

Then list the open questions that still need a decision. A brief the reader can trust shows its seams.

## Output
A one-page campaign brief in this structure. Fill every field; **≤ 2 lines each, ≤ 400 words total** (Content plan excepted: one line per asset).

```
# Campaign Brief: <name>

**Campaign owner**   <the one named person accountable for this campaign end to end>
**Objective**        <the one measurable outcome; e.g. "300 waitlist signups by launch">
**Why now**          <the reason this runs at this time>
**Target audience**  <who, specifically, and what they currently believe/do>
**Core message**     <the single idea the audience should walk away with>
**Offer / CTA**      <what you're asking them to do>
**Strategy & angle** <the approach and the hook that makes it land>
**Channel plan**     <channels + what runs on each + cadence>
**Content plan**     <each asset: shape · owner · the proof it clears the bar with>
**Success metrics**  <2–3 metrics you will actually track>
**Budget**           <real spend / resource ceiling, or "none">
**Timeline**         <key dates: start, milestones, launch, end>
**Risks**            <what could sink it + the mitigation>
**Open questions**   <decisions still needed>
```

### Field guidance — Content plan and the PROOF BAR

Every content shape carries an evidence requirement. **The proof bar is a gate, not a guideline: if an asset can't clear the bar for its shape, change the shape or cut the asset.** Never lower the bar to keep the asset.

Each asset in the Content plan names three things: its **shape**, its single **owner**, and the **proof** it will clear the bar with.

- **High-proof shapes** (case study, outcome teardown, benchmark, before/after) require a real, verifiable number that someone can point to a source for. Fabricating or estimating that number is never acceptable, in a draft or anywhere else. No number in hand means the asset becomes a lower-proof shape or gets cut.
- **Low-proof shapes** (lesson, point of view, explainer, behind-the-scenes) require only genuine specificity: a real moment, a named constraint, a concrete detail. They don't need a metric, and dressing them up with a fake one converts a fine asset into a liability.
- **Curation and roundup shapes** carry an extra requirement: first-hand familiarity with every item listed, meaning you have personally read, used, or watched each one. A second-hand summary, a description lifted from the item's own page, or an item you have only heard about does not clear it. If you cannot say that of every item, cut the ones you cannot and shorten the list.

Ownership sits at two levels and they are not interchangeable. The **Campaign owner** field names the single person accountable for the campaign end to end. Asset owners live here in the Content plan, inline, one per asset, and nowhere else. Neither level substitutes for the other, and a cross-reference is not an owner.

## Example
Input: "We should do a campaign around the new pricing tier launching next month. Want to drive upgrades from existing free users."

That input gestures at three of the four must-haves without landing any of them. There is a goal (drive upgrades) but no target number, an audience (existing free users) but no defined segment, and rough timing (next month) but no firm date. Ownership is absent entirely. So the honest output is a **Step 1 draft, not a shippable brief**: every inferred value is flagged, and the four gaps are asked, not invented.

Output:
```
# Campaign Brief: Pro Tier Upgrade Push (draft, must-haves open)

**Campaign owner**   [NEEDS INPUT: who is accountable for this campaign end to end?]
**Objective**        Working target: 200 free→Pro upgrades in the 30 days post-launch ⚑ assumed
                     [NEEDS INPUT: what number or rate actually counts as success?]
**Why now**          Pro ships next month and the free base is the warmest audience available ⚑ assumed
**Target audience**  Free users who have hit a plan limit ⚑ assumed. Proposed cut: 3+ sessions in
                     the last 30 days ⚑ assumed [NEEDS INPUT: real activity threshold and segment size?]
**Core message**     "You have already outgrown the free plan. Pro removes the ceiling you keep hitting." ⚑ assumed
**Offer / CTA**      Upgrade to Pro. 20% off the first 3 months during launch week ⚑ assumed
                     [NEEDS INPUT: is any discount approved, and at what depth?]
**Strategy & angle** Lead with the specific limit each user hit, not a feature list ⚑ assumed
**Channel plan**     In-app banner (fires on limit hit) · 3-email sequence (day 0, +3, +7) · one
                     founder post on launch day ⚑ assumed · cadence mirrors the Timeline field
**Content plan**     In-app copy [product copy · PM ⚑ assumed · proof: the user's own limit event]
                     Emails [lesson · lifecycle marketer ⚑ assumed · proof: the named limits users hit]
                     Founder post [point of view · founder ⚑ assumed · proof: why the ceiling exists]
                     Customer outcome story: CUT. High-proof shape with no verifiable result yet.
**Success metrics**  Upgrade count · upgrade rate of the emailed segment · discount uptake ⚑ assumed
**Budget**           None beyond existing tools ⚑ assumed
**Timeline**         Assets T-5 · email 1 launch day · email 2 +3d · email 3 +7d · close +30d ⚑ assumed
                     [NEEDS INPUT: what is the actual launch date?]
**Risks**            Discount pulls in users who would have paid full price. Cap it to launch week ⚑ assumed
**Open questions**   Campaign owner · discount approval · launch date · whether 3+ sessions
                     is the right segment cut
```

Four must-haves are still open (objective number, audience definition, launch date, campaign owner), so this draft does not pass Step 2 and cannot ship. The proof bar also bit once: the customer outcome story was cut rather than given an invented result. The flags are the point. A version of this brief with the same invented specifics and no markers would read more confident and be worth less.

## Notes
- One page is the discipline, and it's measurable: 400 words, 2 lines a field, one line per asset in the Content plan. If it won't fit, the campaign isn't focused enough yet.
- The four tests are the value. Passing them doesn't guarantee the campaign is feasible or that it will work; they check that the plan is specific, owned, timed, and honest. A brief that passes them improves execution readiness; one that fails hides the work you skipped.
- Flags are not weakness. An unflagged invention reads as a decision someone made, and it will be executed as one.
- Pair with a voice guide for on-brand assets, a hook generator for the openers, and a copy-review pass before anything ships.
