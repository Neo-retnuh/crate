---
name: adversarial-review
description: >
  Adversarially reviews content and strategy from six angles — logic, evidence,
  audience reception, competitive positioning, execution risk, and
  voice/credibility — using an 8-type inline-annotation model for precise,
  fix-attached feedback. Use when a content piece, strategy doc, proposal, or
  listing needs stress-testing before it ships, or when the user says "review
  this", "attack this", "poke holes in this", or "what would a critic say".
  Also fires on "stress-test this" when the target is ONE finished artifact —
  if the user is instead weighing two or more options or stakeholder
  tradeoffs, route to parallel-perspectives. Scope — critique of a single
  written content or strategy artifact; not code review or data validation.
metadata:
  author: Hunter Marshall (https://www.mesteezo.com)
  license: MIT
---

# Adversarial Review

You are a sharp, constructive adversary. Your job is to surface the material weaknesses across the six defined lenses before the audience does — and attach a specific fix to each one. This produces a marked-up critique (inline annotations plus a verdict) that makes a piece defensible before it ships.

## When to use
- A content piece, proposal, pitch, or strategy doc needs a hard pass before it goes out
- You want per-sentence, fix-attached feedback rather than vague impressions
- Branded content needs a voice/credibility check against known anti-patterns
- Literal asks: "review this", "attack this", "poke holes in this", "what would a critic say"
- "Stress-test this" is shared with parallel-perspectives. It routes here when the object is a single finished artifact to be critiqued; it routes to parallel-perspectives when the object is a set of options or stakeholder tradeoffs to be weighed. If the ask is generic, confirm which before starting.

## When not to use
- Code correctness or data validation → use a code-review or data-validation workflow instead
- You need a decision between competing options, not a critique of one artifact → use parallel-perspectives
- The piece is a rough early draft where structure is still forming → shape it first, then review

## Inputs

**Required:**
- [ ] Content to review (copy, strategy doc, proposal, listing, brief)
- [ ] Context: what is this for? (pitch, blog post, client deliverable, internal doc)
- [ ] Audience: who will read/judge this?

**Optional but strengthens review:**
- Brand brief or voice guide
- Competitive context (what alternatives exist?)
- Style samples (approved, proven-good content for this brand or author)

### Loading a Voice Definition (Recommended When Reviewing Branded Content)

Before reviewing branded content, load whatever voice definition or brand-voice guide you have for that brand. Use its anti-patterns list as a literal `[V]` flag checklist. Different brands have distinct voice markers — one may be operator-precise, another editorial, another playful — so raise a `[V]` flag when a voice deviation is supported by the brand's voice guide or by the stated audience context, and say which one supports it. If no voice guide exists, fall back to the general credibility and register checks in the Voice & Credibility lens below.

## Method

Copy this checklist and check items off as you go:
- [ ] Step 1 — Confirm inputs (content, context, audience); load a voice definition if reviewing branded content
- [ ] Step 2 — Pick a mode (Full Adversarial / Quick Stress / Inline Annotate)
- [ ] Step 3 — Run the mode's passes, producing findings with quoted text + a fix for each
- [ ] Step 4 — Emit a verdict (STRONG / NEEDS WORK / WEAK) and an ordered top must-fix list (up to 3; fewer if fewer exist). Quick Stress is exempt — its single "one fix that would improve it most" stands in for the list.
- [ ] Step 5 — Optionally run Auto-Revision if the verdict is WEAK
- [ ] Step 6 — Run the Self-Check Gate on your own review before delivering

### Modes

#### MODE 1: FULL ADVERSARIAL

Attack from 6 angles, then synthesize:

1. **Logic & Argument** — Are claims supported? Any logical fallacies? Leaps of reasoning?
2. **Evidence & Data** — What's cited? What's assumed? What would a skeptic demand?
3. **Audience Reception** — How will the target audience actually react? What will they push back on?
4. **Competitive Positioning** — Does this differentiate? Or could a competitor claim the same thing?
5. **Execution Risk** — Can this actually be delivered? What could go wrong?
6. **Voice & Credibility** — Does the author sound credible? Any trust-breaking patterns?

For each angle: 2-3 specific findings with quoted text + suggested fix.

End with: **VERDICT: STRONG | NEEDS WORK | WEAK** and an ordered top must-fix list (up to 3).

#### MODE 2: QUICK STRESS

3 minutes, 3 bullets:
1. Strongest point (what's working)
2. Biggest vulnerability (what an opponent would attack first)
3. One fix that would improve it most

Under 200 words total.

#### MODE 3: INLINE ANNOTATE

Per-sentence walk-through using the 8 annotation types:

| Code | Type | Color | When to Use |
|------|------|-------|-------------|
| `[Q]` | Question | Blue | Unclear meaning, ambiguous claim, missing context |
| `[S]` | Suggestion | Green | Alternative phrasing, better word choice |
| `[E]` | Edit | Orange | Grammar, spelling, punctuation, syntax |
| `[V]` | Voice Note | Purple | Off-brand voice, credibility issue, register mismatch |
| `[W]` | Weakness | Red | Weak argument, logical gap, unconvincing claim |
| `[EG]` | Evidence Gap | Yellow | Unsupported claim, missing data, needs proof |
| `[WD]` | Wordiness | Gray | Verbose, could be tighter |
| `[FC]` | Fact-Check | Pink | Verifiable claim that needs checking |

### Auto-Revision (Optional)

If the verdict is **WEAK** and you want an automatic revision pass, feed the MUST-FIX annotations into an evaluate-and-optimize loop: run the content back through a rewrite that must satisfy each finding as an explicit criterion.

Example criteria pulled from the annotations:
- All `[EG]` evidence gaps must have specific data or examples
- All `[W]` weaknesses must be reframed or removed
- Voice must be credible to the target audience

Cap iterations (2 is usually enough) so the loop can't run away.

### Style Learning

When you have approved, proven-good samples for the brand or author, compare the content's voice against them and flag `[V]` Voice Notes for deviations. This calibrates the review to the specific brand rather than to generic "good writing" standards.

### Application Domains

The review adapts to the content type and audience. A few examples of how the lenses shift by domain:

| Domain | Content Types | Special Considerations |
|--------|--------------|----------------------|
| Consulting / services | Client proposals, case studies, pitch decks | Must differentiate from generic consultancy language |
| Thought leadership | Blog posts, essays, social posts | Must balance expertise with accessibility |
| Consumer / lifestyle brand | Product listings, marketing copy, brand story | Must sound authentic to the brand's culture and audience |

## Output

Inline-annotate mode uses this format (full adversarial and quick-stress modes emit the findings + verdict structure described under Modes):

```
ADVERSARIAL REVIEW — INLINE ANNOTATIONS
Content: [title/description] | Mode: inline_annotate | Date: [date]

SEVERITY: MUST-FIX

> "quoted sentence"
  [CODE] Type — what's wrong. FIX: the specific replacement.

SEVERITY: NICE-TO-HAVE

> "quoted sentence"
  [CODE] Type — what's wrong. FIX: the specific replacement.

SUMMARY:
  Must-Fix: [count] | Nice-to-Have: [count]
  Top vulnerability: [one sentence]
  TOP MUST-FIX (up to 3, ordered):
    1. [action]
    2. [action]
    3. [action]
  Overall: [STRONG / NEEDS WORK / WEAK]
```

## Example

Input: A services-company landing-page draft. Context: cold-traffic homepage hero. Audience: sophisticated B2B buyers comparing vendors.

Output:

```
ADVERSARIAL REVIEW — INLINE ANNOTATIONS
Content: Homepage hero draft | Mode: inline_annotate | Date: 2026-07-23

SEVERITY: MUST-FIX

> "We're the leading AI consultancy in the Southeast."
  [EG] Evidence Gap — "Leading" by what metric? Revenue? Clients? This invites
  challenge without proof. FIX: "We've helped 40+ Southeast companies deploy AI
  workflows since 2024" — specific, verifiable, defensible.

> "Our proprietary methodology ensures results."
  [W] Weakness — "Proprietary methodology" is a red flag for sophisticated buyers.
  It signals "we won't tell you how it works." FIX: "Our four-week Audit → Pilot →
  Deploy → Handoff process puts a working AI workflow in production before the final
  invoice."

SEVERITY: NICE-TO-HAVE

> "In today's rapidly evolving landscape..."
  [WD] Wordiness — Generic opener. Every competitor says this. FIX: "Most AI pilots
  never reach production. Ours ship in four weeks."

SUMMARY:
  Must-Fix: 2 | Nice-to-Have: 1
  Top vulnerability: Two unsupported superiority claims a buyer can dismiss in one line.
  TOP MUST-FIX (up to 3, ordered):
    1. Replace "leading AI consultancy" with the verifiable 40+ deployments claim.
    2. Replace "proprietary methodology" with the named four-stage process.
    3. Replace the generic opener with the production-rate line.
  Overall: NEEDS WORK
```

## Notes
- Be precise, not mean — every critique carries a specific fix. Criticism without a fix is a failed finding.
- **Self-Check Gate:** run the review's own output through a quality check before delivering it. A review fails if it only finds surface issues (grammar, formatting) and misses substantive weaknesses, provides criticism without fixes, uses generic feedback that could apply to any content, or goes easy on content because it's "good enough." The adversary's job is to find what others won't — including in its own work.
- Flag a voice deviation `[V]` when the voice guide or the stated audience context supports it, and cite which; without a voice guide, fall back to general credibility and register checks rather than asserting a house preference.
