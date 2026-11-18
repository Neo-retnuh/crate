---
name: content-repurposer
description: >
  Turns one strong source piece into channel-native versions for LinkedIn, X,
  email, and short-form video, each rebuilt for its platform rather than
  reformatted. Extracts the transferable core (claim, supporting points, best
  example, quotable line), sets a proof ceiling the versions cannot exceed, maps
  each channel's length target and structural shape, rotates the entry angle
  across versions, and runs a voice and slop pass on every draft. Use when a
  strong asset needs a week of distribution without reading like a repost.
  Triggers: "repurpose this", "turn this into a LinkedIn post and a thread",
  "give me channel versions of this", "atomize this piece", "make this work
  everywhere".
metadata:
  author: Hunter Marshall (https://www.mesteezo.com)
  license: MIT
---

# Content Repurposer

Most "repurposing" is copy-paste with the line breaks moved around. It reads as a repost because the *argument* was written for one channel and dragged into others. This skill does the opposite: it extracts the transferable core of a piece, then rebuilds it natively for each channel so every version feels like it was written there first.

## When to use

- You have one solid asset (an article, a talk, a case study, a long post) and want a week of channel-native content out of it.
- The user asks "turn this into a LinkedIn post and a thread," "repurpose this everywhere," or "give me channel versions of this."

## When not to use

- The source itself is weak or the idea is still unformed. Repurposing amplifies whatever's there. Send it to `content-sharpener` first, which decides whether the idea is worth writing at all and returns a shaped brief or a kill verdict. If you don't have it, answer three questions before distributing anything: what is the one contestable claim, who specifically is it for, and what first-hand proof backs it.
- You only need one channel. Repurposing has overhead; a single native draft is faster.

## Inputs

- The source content (paste it, or link it).
- The target channels (default set: LinkedIn, X/thread, email, one short-form video script).
- Optional: a brand voice guide (see `brand-voice-extractor`) — if you don't have one, paste two or three samples of the author's real writing and match their sentence length, register, and vocabulary by hand.
- Optional: the audience for each channel, and the proof assets available (real numbers, named examples, screenshots).

## Method

Copy this checklist and check items off as you go:

- [ ] Extract the core (claim, supporting points, best example, most quotable line)
- [ ] Set the proof ceiling — the strongest thing the source can actually prove
- [ ] Map each channel's job, length target, and structure before writing
- [ ] Rebuild each version natively — don't reformat
- [ ] Vary the entry angle across versions
- [ ] Clear the proof bar for the shape each version is taking, or change the shape
- [ ] Run the voice + slop check on every draft

1. **Extract the core.** Pull out the one claim the piece actually makes, the 3–5 supporting points, the best concrete example, and the single most quotable line. Everything downstream is built from this, not from the original wording.

2. **Set the proof ceiling.** Write down the strongest claim the source can actually substantiate, and with what. No channel version may claim more than this line. Repurposing inflates claims by default, because a shorter format tempts you to round a specific result into a general law.

3. **Map each channel's job.** Name what each channel rewards, how long the version runs, and what shape it takes, before writing a word.

   **LinkedIn** — 900–1,600 characters (roughly 150–250 words), 8–14 paragraphs of 1–2 sentences each, blank line between every one. Roughly the first line or two are what shows above the "see more" fold, but where that fold actually falls shifts with device, viewport, and whatever LinkedIn's current UI does. Treat it as a variable heuristic rather than a fixed count: check what truncates on your own account, then get the hook and the turn above whatever your fold turns out to be.
   > Structure: hook line · turn line ("here's what actually happened") · 3–5 short beats · one concrete number or named example · one-line takeaway · a soft CTA the reader can answer in five words.
   > In-body links have historically suppressed reach on LinkedIn, and the common convention is to put the link in the first comment. Treat that as an observed convention, not a rule; test it on your own account before committing to it.

   **X / thread** — 5–9 posts. Post 1 states the whole claim standing alone in under 200 characters, so it works with zero context. Every post after it carries one idea in 1–3 sentences and must survive being screenshotted alone.
   > Structure: post 1 the claim · post 2 the cost of getting it wrong · posts 3–N one supporting beat each, in build order · final post the takeaway plus a plain-language ask. Skip "a thread" announcements and 1/7 counters unless the thread is genuinely a numbered list.

   **Email** — subject line 4–7 words and under about 45 characters so it survives a phone inbox; preview text written as its own line that adds information rather than repeating the subject. Body 120–250 words across 3–6 short paragraphs, one takeaway, one link, one next step.
   > Structure: subject · a specific scene or claim in the first two sentences · the turn · the proof · one action. Write to one reader, singular, second person.

   **Short-form video script** — 30–45 seconds, roughly 75–110 spoken words, timestamped, with on-screen text cues that say something different from the spoken line rather than subtitling it.
   > Structure: spoken hook · on-screen cue · the turn · one concrete example · the payoff line · verbal CTA. Write for the ear: contractions, short sentences, no subordinate clauses.
   > Landing the hook in the opening seconds is the standard advice because early drop-off is the heaviest, but the exact window shifts with each platform's autoplay behavior. Treat it as a working heuristic and check your own retention curve.

4. **Rebuild, don't reformat.** Write each version from the core, in the channel's native shape. The LinkedIn post and the email should share a spine and share almost no sentences.

5. **Vary the entry angle.** Don't open all four versions the same way. Rotate across the canonical angles (see `hook-generator`, which owns this taxonomy): **Contrarian**, **Specific result**, **Curiosity gap**, **Named problem**, **Story cold-open**, **Stakes**. Assign a different angle to each channel and label it. If you don't have `hook-generator`, write one opening line per angle from that list and pick the one that fits the channel's audience.

6. **Clear the proof bar.** Every content shape carries an evidence requirement. **The proof bar is a gate, not a guideline: if a version can't clear the bar for the shape it's taking, change the shape or cut the version.** Higher-proof shapes need a real verifiable number; lower-proof shapes need only genuine specificity. Never invent the difference.

   | Shape | What it implicitly claims | Proof bar |
   |---|---|---|
   | Case study / outcome teardown | "this produced this result" | a real number you can verify, with its scope and timeframe |
   | Benchmark / trend claim | "this is generally true" | a citable source, or downgrade to a single named case |
   | Lesson / opinion | "this is how to think about it" | genuine specificity: a real situation and a named tradeoff |
   | Curation / roundup | "these are worth your time" | first-hand familiarity with every item listed (see below) |

   **Curation and roundup shapes** carry an extra requirement: first-hand familiarity with every item listed, meaning you have personally read, used, or watched each one. A second-hand summary, a description lifted from the item's own page, or an item you have only heard about does not clear it. If you cannot say that of every item, cut the ones you cannot and shorten the list.

   If a channel would require proof the source lacks, say so in the output rather than manufacturing it. Narrowing the claim to what the source proves is always available; a rounded-up statistic is not.

7. **Run the voice + slop check.** Pass each draft through the brand voice guide and strip AI tells (see `stop-slop`). If you don't have it, cut the tells by hand: em dashes doing a comma's job, three-item lists used for rhythm, "it's not X, it's Y" constructions, and any sentence that could open any article on the topic.

## Output

The extracted core first, then one fully written draft per target channel. In a delivered set, nothing is abbreviated to a hook line, and nothing is a verbatim slice of another version.

One scoped exception, for illustration only: an *example* of this skill's output may show complete drafts for a subset of channels and hooks only for the rest, provided the abbreviated ones are explicitly labeled as abbreviated. A set delivered to a user never is — every target channel gets a full draft.

```
CORE
Claim              <the one claim the source actually makes>
Supporting points  <3–5, in the order they build>
Best example       <the single most concrete example in the source>
Quotable line      <the one line worth repeating verbatim>
Proof ceiling      <the strongest claim the source substantiates, and with what>

CHANNEL       <LinkedIn / X thread / Email / Short-form script / ...>
Hook angle    <Contrarian | Specific result | Curiosity gap | Named problem | Story cold-open | Stakes>
Shape         <case study | benchmark | lesson | curation — this sets the proof bar>
Draft         <the complete channel-ready draft, written out in full>
Target length <the channel's length target, and the actual length of this draft>

<repeat the CHANNEL block once per target channel>

PROOF NOTES   <any claim that was narrowed or any version that was cut, and why>
```

## Example

**Input:** a 1,200-word article, "Why your onboarding emails get ignored."

**Output:**

```
CORE
Claim              Onboarding emails fail because they're about the product, not the user's first win.
Supporting points  1. Welcome sequences default to describing the company.
                   2. Feature tours arrive before the user has a reason to care.
                   3. In this one company's numbers, reaching the first real win
                      tracked with activation.
                   4. Cutting emails outperforms rewriting them.
Best example       One SaaS team cut a 6-email welcome sequence to 2 and activation doubled.
Quotable line      "Nobody signed up to read your changelog."
Proof ceiling      One company's before/after activation figure, self-reported, over one quarter.
                   Not a category benchmark.
```

**CHANNEL — LinkedIn** · Hook angle: Specific result · Shape: lesson · Target length: 900–1,600 characters (this draft: ~1,095)

```
A SaaS team deleted 4 of their 6 onboarding emails.

Activation doubled over the following quarter.

That's one company's own reported number, so read it as an observed result and not as a proven cause.

It's still worth looking at what they chose to cut.

The four weren't badly written. Clean design, decent subject lines, all of it.

What they had in common was subject matter. Every one was about the product.

Email 1 introduced the company. Email 2 toured the features.

Email 3 announced an integration nobody had asked for yet. Email 4 checked in to see how things were going.

By the time anything told the user what to actually do first, they were four emails deep and already gone.

The two that survived did one job each. The first asked for a single action, the one that maps to the first real win.

The second showed the user what they unlocked by taking it.

Nobody signed up to read your changelog. They signed up to get one thing done.

Go open your own welcome sequence and count how many emails describe you before one asks the user to do something.

What number did you get?
```

**CHANNEL — Short-form video script** · Hook angle: Story cold-open · Shape: lesson · Target length: 30–45 seconds (this draft: ~105 spoken words, ~40 seconds)

```
[0:00 SPOKEN]     Someone on a growth team deleted two thirds of their welcome
                  emails, and their activation rate doubled.
[0:00 ON-SCREEN]  6 emails to 2

[0:05 SPOKEN]     Here's what was in the four they cut. A company intro. A feature
                  tour. An integration announcement. And a check-in asking how
                  things were going.
[0:13 ON-SCREEN]  all about them, none about you

[0:16 SPOKEN]     Every one of those describes the product. Not one of them told the
                  user what to do first.

[0:21 SPOKEN]     The two they kept did one job each. Ask for the first action. Then
                  show the user what they unlocked by taking it.
[0:28 ON-SCREEN]  one action, one payoff

[0:31 SPOKEN]     Nobody signed up to read your changelog.

[0:34 SPOKEN]     Go open your welcome sequence. Count the emails about you. More
                  than one is too many.
```

**Remaining channels** — abbreviated to hooks only, for space. This is the scoped example exception described under Output; a delivered set would carry full drafts here.

- **CHANNEL — X thread** · Hook angle: Contrarian · Shape: lesson · Target length: 5–9 posts. Opening post: "Your onboarding emails aren't ignored because they're badly written. They're ignored because all six of them are about you."
- **CHANNEL — Email** · Hook angle: Named problem · Shape: lesson · Target length: 120–250 words. Subject: "Nobody reads your changelog" · Preview: "The four emails to delete this week."

```
PROOF NOTES
The X thread first drafted as "most welcome sequences are three times too long."
That's a benchmark claim and the source proves one company's result, not a category
norm. Narrowed to the single named case rather than inventing a statistic.
The activation figure is self-reported, so every version says "one team" and never
"teams that do this."
The source shows a before/after, not a controlled test, so no version says the
product-focused emails caused the activation failure. The LinkedIn draft states the
result and names it as an observed result rather than a proven cause.
```

Same spine, four native versions, zero copy-paste, and no version claiming more than the source proves. Two are written out in full above; the other two are shown as hooks only under the Output section's example exception.

## Notes

- Channel set is configurable — add newsletter, Instagram caption, YouTube description, etc. Give each new channel a length target and a structure line before you write in it, the same way the four defaults have one.
- Repurposing is not translation. If a channel can't carry the idea well, say so rather than forcing a weak version.
- The proof bar governs the whole set. A single inflated claim on one channel is what gets screenshotted, and it discredits the other three.
- Platform-specific conventions (link placement, hook windows, ideal thread length) decay as feeds change. Treat every number here as a starting point to test against your own analytics, not a rule.
