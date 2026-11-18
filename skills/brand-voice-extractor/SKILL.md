---
name: brand-voice-extractor
description: >
  Turns a handful of existing content samples into a reusable brand voice
  guide — the tone, vocabulary, rhythm, and rules that make the writing sound
  like the brand. Use when onboarding a new brand or client, aligning a team,
  a freelancer, or a model on how the brand writes, or before generating
  content at scale. Also triggers on "build me a brand voice guide",
  "capture how we write", "define our tone from these samples", or when
  output quality is drifting because everyone has a different mental model of
  the voice. Do NOT use with fewer than three real samples and no owner to
  interview.
metadata:
  author: Hunter Marshall (https://www.mesteezo.com)
  license: MIT
---

# Brand Voice Extractor

Most brand-voice guides are written top-down: someone picks three adjectives ("bold, human, smart") and hopes writers can reverse-engineer sentences from them. That fails because adjectives are not instructions. This skill works bottom-up instead: it reads writing that already sounds right, then extracts the concrete, checkable patterns that produce that sound. The output is a guide a writer — or a model — can actually follow, and that a reviewer can score against.

## When to use

- You're onboarding a new brand or client and need a voice guide fast.
- You have good content but it lives in one person's head, and you're about to hand writing to a team, a freelancer, or an AI.
- Output quality is drifting because everyone has a different mental model of "our voice."
- The user asks "build me a brand voice guide," "capture how we write," or "define our tone from these samples."

## When not to use

- You have fewer than three real samples and no owner to interview — extracting a voice from one sample produces a caricature, not a guide. Gather more first, or use the Interview Fallback below.

## Inputs

Provide **3–7 samples** of content that genuinely sounds like the brand. More is not better — pick the truest examples, not the most. Mixed channels are fine and useful (a landing page, two emails, a few social posts).

For each sample, note: the channel, roughly who it was for, and whether it performed well. If you have "off-brand" counter-examples (drafts that got rejected for sounding wrong), include 1–2 — the contrast sharpens the extraction more than another good sample would.

## Method

Copy this checklist and check items off as you go:

- [ ] Pass 1 — Tone register
- [ ] Pass 2 — Vocabulary and diction
- [ ] Pass 3 — Sentence mechanics
- [ ] Pass 4 — Rhetorical moves
- [ ] Pass 5 — Point of view and stance
- [ ] Pass 6 — Counter-examples (if provided)
- [ ] Assemble the passes into the Voice Guide

Run these six passes over the samples. Each produces a section of the final guide.

### 1. Tone register
Where does the writing sit on each axis? Place it, then cite the sentence that proves it.
- Formal ↔ casual
- Serious ↔ playful
- Reserved ↔ bold
- Authoritative ↔ peer-to-peer
- Plain ↔ ornate

Don't average. If the brand is playful in social and precise in docs, record both and name the trigger that switches register.

### 2. Vocabulary and diction
- **Signature words** — terms the brand reaches for repeatedly. List them.
- **Avoid list** — corporate filler, hype, or clichés ("leverage," "seamless," "game-changing"). Absence from a 3–7 sample set is weak evidence: a small sample can miss a word the brand uses happily. So split the list in two. **Confirmed bans** are words a counter-example shows getting rejected, or the brand owner rules out on the record. **Tentative candidates** are words merely absent from the samples — flag them as candidates, and promote them to bans only once a counter-example or the owner confirms. Never enforce a candidate as a hard ban.
- **Jargon level** — how much domain vocabulary, and is it explained or assumed?
- **Naming conventions** — how the brand refers to itself, its product, and its audience (e.g. "you" vs. "our customers" vs. "users").

### 3. Sentence mechanics
- Average sentence length, and how much it varies.
- Fragments allowed? Questions? Direct address?
- Punctuation habits — em dashes, semicolons, exclamation points, Oxford comma.
- Paragraph length and shape.
- Do sentences open the same way repeatedly, or is opening variety a rule?

### 4. Rhetorical moves
The recurring *structures*, not just words:
- How does it open? (Hook type — question, claim, story, stat, provocation.)
- How does it build an argument? (Evidence-first, story-first, contrarian setup.)
- How does it handle the reader's objections?
- How does it close and call to action? (Soft, direct, none.)
- Signature devices — analogy, repetition, understatement, specific numbers.

### 5. Point of view and stance
- What does the brand *believe*? Voice without a stance is just style.
- What does it push against — the industry norm it defines itself in opposition to?
- Confidence level: does it hedge, or state things plainly?
- Emotional range it permits itself (earnest, wry, urgent, calm).

### 6. The counter-examples (if provided)
For each rejected sample, name the specific rule it broke. "This got cut because it opened with throat-clearing and used three hype words in the first sentence." These become the sharpest lines in the guide.

## Output: the Voice Guide

Assemble the passes into a single guide with these sections. Every rule must be **checkable** — a reviewer should be able to hold a new draft against it and mark pass/fail.

1. **Voice in one paragraph** — the summary a new writer reads first.
2. **Tone register** — the axes, with the switch-triggers.
3. **Do / Don't word list** — signature words, confirmed bans, and tentative avoid-list candidates, kept visibly separate.
4. **Sentence rules** — mechanics as instructions ("Vary sentence length; never three same-length sentences in a row. No em dashes.").
5. **Structural patterns** — how to open, build, and close.
6. **Stance** — what the brand believes and pushes against.
7. **Annotated example** — one of the input samples, marked up to show *representative* rules in action, with at least one annotation drawn from each category above (tone, word choice, sentence mechanics, structure, stance). Annotating every rule bloats the guide; covering each category proves the rules are real. This is the most-used part of any real guide; don't skip it.
8. **Fast checklist** — 8–12 yes/no questions a writer runs before shipping. Each must be answerable from the text itself by pointing at a word, a count, or a structure. "Any sentence over 25 words?" works. "Does it sound like us?" does not — if a reviewer needs taste to answer it, rewrite it as an observable test or drop it.

## Voice-Match Score (optional)

To use the guide as a gate on new content, score a draft against the checklist: start at 100, deduct for each rule broken, and report the specific line and rule for every deduction. Below ~70, the draft doesn't match the voice yet — revise the flagged lines rather than starting over.

## Interview Fallback

No usable samples? Extract the voice by interview instead. Ask the owner:
- "Name a brand whose writing you admire, and one whose writing makes you cringe. Why each?"
- "What's a word or phrase you never want to see in our content?"
- "Are we more the expert in the room, or the friend who happens to know this?"
- "Read me a sentence that sounds exactly like us."
- "What do we believe that most of our competitors don't?"

Then draft the guide from the answers and validate it by writing three test sentences and checking they land.

## Example

**Input:** three samples from a developer-tools brand — a landing page, a changelog entry, and a launch email — plus one rejected draft.

**Output (all eight sections, compressed):**

**1. Voice in one paragraph.** We write like the engineer sitting next to you who already solved this. Plain, specific, a little dry. We show the thing working before we explain why it matters, we never oversell, and we assume the reader is competent and busy.

**2. Tone register.** All five axes, each with the sentence that places it:
- *Formal ↔ casual* — casual, but not chatty. Proof: "You'll have this running in about four minutes."
- *Serious ↔ playful* — serious with a dry edge; jokes are asides, never the point. Proof: "Then read the docs — if you want to."
- *Reserved ↔ bold* — bold in claims, reserved in adjectives; the boldness comes from specificity. Proof: "No agents. No YAML sprawl. One command."
- *Authoritative ↔ peer-to-peer* — peer-to-peer, never authoritative-formal. Proof: "We hit the same wall on our own pipeline last year."
- *Plain ↔ ornate* — plain; nouns and verbs, almost no modifiers. Proof: "Ship your first pipeline in four minutes."

Switch-triggers — docs tighten to precise-neutral (the dry asides drop out); social loosens to wry.

**3. Do / Don't word list.** Signature: "ship," "under the hood," "actually," concrete time and number units. Confirmed avoid: "leverage," "seamless," "robust," "in today's fast-paced world" — the rejected draft used three in one sentence and was cut for it, so these are hard bans on counter-example evidence. Tentative avoid-list candidates (absent from the samples, not yet confirmed): "empower," "unlock," "best-in-class" — take these to the brand owner before enforcing them.

**4. Sentence rules.** Short-then-long rhythm; never three same-length sentences in a row. Fragments allowed for emphasis. Em dashes fine; exclamation points rare. Second person ("you"), never "our customers."

**5. Structural patterns.** Open on the concrete result, not context-setting. Build evidence-first: claim, then the command or number that proves it. Close with the next action, stated softly and once.

**6. Stance.** We believe developer tools should be judged by time-to-first-success, and we push against the category habit of selling capability lists to buyers instead of showing the work to users. We state things plainly; we don't hedge.

**7. Annotated example** — landing-page hero, marked up with representative rules, one from each category (structure, word choice, sentence mechanics, stance, tone):

- `Ship your first pipeline in four minutes.` — opens on the concrete result, not context (Structural pattern 1); specific number, not "fast" (Do-word: concrete units); second person (Sentence rule).
- `No agents. No YAML sprawl. One command.` — three fragments for emphasis (Sentence rule: fragments allowed); defines the product by what it removes (Stance: pushes against capability-list selling).
- `Then read the docs — if you want to.` — em dash plus dry aside (Tone: plain, a little wry); soft single close (Structural pattern: close with one soft action).

**8. Fast checklist.** Does the first sentence name a concrete outcome (not context or background)? Any word from the confirmed-ban list? Any sentence over 25 words without a sentence under 10 adjacent to it? Three consecutive sentences within 3 words of the same length? At least one specific number or unit in the first paragraph? Second person ("you") used, and "our customers"/"users" absent? Exactly one CTA, appearing once? At least one runnable command, code snippet, or named product step present?

## Notes on Use

- **Re-extract when the brand evolves.** A voice guide is a snapshot. Re-run it after a repositioning or a year of new content.
- **One voice, or a system?** Bigger brands need a *voice* (constant) plus *tones* (per-channel or per-moment variations on it). If the samples show clear register shifts, document the system, not a single setting.
- **The guide is only as honest as the samples.** Feeding it aspirational content produces an aspirational guide the brand doesn't actually live. Extract from what's real; set aspiration separately.
