---
name: hook-generator
description: >
  Generates and ranks opening hooks for posts, emails, ads, and video, then
  explains why the top-ranked ones win so the user can write the next one
  unaided. Use when the idea is solid but the first line isn't earning
  attention, or on asks like "write me some hooks", "my opener is weak, fix
  it", "why isn't this first line landing?", "give me subject lines for this
  email".
metadata:
  author: Hunter Marshall (https://www.mesteezo.com)
  license: MIT
---

# Hook Generator

The first line is a major factor in whether the rest gets read — often the one that decides it. Most hooks fail the same way: they warm up, they summarize, or they announce the topic instead of creating a reason to keep going. This skill generates a spread of hooks across distinct psychological angles, ranks them against the specific audience and channel, and shows the reasoning — so it's a teacher, not just a vending machine.

## When to use

- The content is solid but flat at the top — a post that opens with context, an email with a subject line that describes instead of pulls, an ad that leads with the product.
- The user asks "write me some hooks," "my opener is weak, fix it," or "why isn't this first line landing?"

## When not to use

- You don't yet know the one idea underneath. A hook for a piece with no point is just clickbait. Sharpen the idea first with `content-sharpener` (the "is this worth writing at all" pass); if you're running this skill standalone without the rest of the gallery, write the one-sentence point and the proof you have for it before generating hooks.

## Inputs

- The core idea or the piece it's opening.
- Channel (LinkedIn, X, email subject, cold email, ad, video) — hooks are channel-shaped.
- Audience: who they are and what they already believe.
- Optional: brand voice guide (see `brand-voice-extractor`) so hooks match your register.

## Method

Copy this checklist and check items off as you go:

- [ ] Find the tension the hook will exploit
- [ ] Generate across distinct angles, not variations
- [ ] Cut the tells (throat-clearing, topic announcements, AI patterns)
- [ ] Score all five criteria, disqualify anything the piece can't pay off, rank
- [ ] Explain why the top three win

1. **Find the tension.** Many strong hooks exploit a gap — between what the reader expects and what's true, between the pain and the promise. Others earn attention a different way: recognition (naming something the reader has felt but never seen written down), humor, beauty, or plain utility. Name the mechanism this hook is using — tension where there is one, otherwise the attention mechanism it's actually running on — before generating.
2. **Generate across angles, not variations.** Produce hooks from distinct angles rather than ten rewrites of one. **Allocation:** one hook per angle (six), plus two to four extras in the two angles that fit this audience and channel best. That lands the default 8–10.
   - **Contrarian** — challenge a belief the audience holds.
   - **Specific result** — a concrete number or outcome; avoid vague or misleading rounding (clean shorthand for a real figure is fine, "a lot" or a number rounded past recognition is not).
   - **Curiosity gap** — open a loop the reader needs closed.
   - **Named problem** — say the reader's pain more precisely than they would.
   - **Story cold-open** — drop them mid-scene.
   - **Stakes** — what it costs to keep doing it the current way.
3. **Cut the tells.** No throat-clearing ("In today's world…"), no topic announcements ("I want to talk about…"), no rhetorical questions that answer themselves. Strip AI patterns (see `stop-slop`).
4. **Score and rank for this audience.** Rank them; don't just list. Score every hook on five criteria, each **1–5** (1 = absent, 3 = present but generic, 5 = sharp and specific to this audience):
   - **Payoff-match** — can the piece actually deliver what this hook promises?
   - **Audience relevance** — does it land on what these readers already believe or fear?
   - **Tension strength** — how strong is the pull it creates? Usually the width of the gap it opens; for a recognition, humor, beauty, or utility hook, how hard the mechanism it runs on actually lands.
   - **Specificity** — concrete detail and real numbers, with no hedging and no vague or misleading rounding.
   - **Channel fit** — does it work in this channel's format and reading posture?

   **Total = the unweighted sum of the five scores (max 25).** No weighting; each criterion counts once. **Tie-break: higher tension strength wins.** If still tied, higher specificity.

   **Hard disqualifier:** a hook the piece cannot pay off scores **payoff-match 0, total 0**, regardless of how well it punches, and is cut from the ranked set rather than listed low. Punch never buys back a broken promise. Note the cut and why, so the user can either fix the piece or drop the angle.
5. **Explain the top three.** For each winner, one line on *why* it works — the angle and the tension it pulls. This is what lets the user write the next one without the skill.

## Output

A ranked set of hooks (default 8–10: one per angle plus extras in the strongest two), listed in rank order — best first — with each hook labeled with the angle it came from, carrying its total score out of 25, and the top three annotated with the reason they win. The same angle can appear more than once in the list; rank order wins over grouping. Any hook disqualified on payoff-match is listed separately with the promise the piece can't keep. Each surviving hook is channel-ready.

If a brand voice guide was provided, use it as a **constraint and a check, not a generator**: it sets the register the hooks must stay inside and it is grounds for rejecting off-voice output. It is not license to impersonate the author's first-hand voice — never use voice samples to make an AI-originated line read as the author's own lived speech. (Same rule as `content-sharpener`'s "the voice check is a check, not a generator.")

## Example

**Input:** a consultant's post arguing that most companies buy AI tools before fixing their process. Channel: LinkedIn. Audience: ops leaders who just bought (or are about to buy) AI tooling.

**Output:**

- **Contrarian (#1, 23/25):** "Buying an AI tool before fixing your process is how you automate a mess faster." → *Why it wins: challenges the exact decision the audience is mid-way through making, and the tension is immediate and personal. Payoff 5, relevance 5, tension 5, specificity 4, channel 4.*
- **Specific result (#2, 22/25):** "We watched a team spend $40k on AI tooling to solve a problem a one-page checklist fixed." → *Why: a concrete number against an absurdly cheap alternative opens a loop the reader wants closed. Payoff 5, relevance 4, tension 4, specificity 5, channel 4.*
- **Named problem (#3, 21/25):** "Six people on your team have six different versions of the process your AI rollout is supposed to run." → *Why: names the real pain more precisely than the reader has, and the number makes it concrete. Payoff 5, relevance 5, tension 4, specificity 4, channel 3.*
- **Contrarian (#4, 19/25):** "Most AI rollouts stall at a step that happens before anyone opens the tool."
- **Named problem (#5, 18/25):** "You bought the tool in March. Nobody can yet tell you who owns the workflow it replaced."
- **Curiosity gap (#6, 17/25):** "The most expensive line in an AI budget never shows up on the invoice."
- **Stakes (#7, 16/25):** "Every month you run the old process through a new tool, you pay for both."
- **Story cold-open (#8, 14/25):** "Three weeks after go-live, the ops lead was still rebuilding the report by hand."

**Cut on payoff-match (0/25):** "The four AI tools every ops leader will be running by 2027." The piece makes no forecast and names no tools, so it cannot pay this off. Punchy, but a broken promise. Fix the piece or drop the angle.

## Notes

- Hooks are promises. A great hook on a weak piece damages trust — rank honesty over punch. That principle is enforced by the payoff-match criterion and its zero-score disqualifier in Step 4, not left to taste.
- The curiosity-gap angle is the closest thing here to clickbait. It is legitimate only when the piece closes the loop it opens; if it doesn't, payoff-match scores 0 and the hook is cut.
- Re-rank if the channel changes; a winning LinkedIn hook is often a weak email subject line.
