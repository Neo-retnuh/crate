---
name: research-synthesizer
description: >
  Turns multiple sources (articles, docs, transcripts, data, interviews) into
  actionable insights — themes, contradictions, gaps, and implications — not
  just summaries. Use whenever you have 2+ sources and want to understand what
  they mean together: "what patterns do you see", "synthesize these", "compare
  these", "what are the contradictions", "pull this research together", "what
  does all this tell us", "what am I missing", or any request to analyze,
  cross-reference, or find insights across multiple inputs. Also triggers when
  the user uploads or pastes multiple documents and asks a question that
  requires looking across all of them, even without the word "synthesize". Do
  NOT use for summarizing a single source — route that to a plain summarize
  function.
metadata:
  author: Hunter Marshall (https://www.mesteezo.com)
  license: MIT
---

# Research Synthesizer

Turns a set of sources into cross-source insight — themes, contradictions, gaps, implications, and next steps — instead of a stack of per-source summaries.

## When to use

- You have **2+ sources** and want **insights, not summaries**.
- You're asking questions like: "What does all this research tell us?", "How do these sources contradict each other?", "What are the gaps in what we know?", "What themes connect these materials?", "What should we do based on all this?"
- The request involves comparing, contrasting, finding themes across, or making sense of multiple pieces of information.
- Literal asks: "what patterns do you see", "synthesize these", "compare these", "what are the contradictions", "pull this research together", "what does all this tell us", "what am I missing".
- Also triggers when the user uploads or pastes multiple documents and asks a question that requires looking across all of them, even without saying "synthesize".

## When not to use

- Only one source, or the user really wants a summary of a single source → use a plain summarize function; this skill will redirect.

## Inputs

Upload or paste any combination of:
- **Documents** (PDFs, Word docs, Google Docs)
- **Text excerpts** (pasted directly)
- **URLs** (web articles, blog posts, research sites)
- **Meeting transcripts** (exported or pasted)
- **Data/stats** (copied from spreadsheets, reports)
- **Images** (screenshots of charts, graphs, tables)

Minimum 2 sources. No maximum. The more diverse, the richer the synthesis.

## Method

Copy this checklist and check items off as you go:
- [ ] Step 1 — Confirm 2+ sources; if only one, redirect to a summary
- [ ] Step 2 — Identify cross-source themes (patterns across multiple materials)
- [ ] Step 3 — Spot contradictions and tensions (where sources disagree)
- [ ] Step 4 — Reveal knowledge gaps (what's NOT covered)
- [ ] Step 5 — Extract implications for the user's specific situation
- [ ] Step 6 — Recommend next steps (research, questions, experiments, decisions)
- [ ] Step 7 — Write the Contrarian Read (consensus, strongest opposing case, what would settle it)
- [ ] Step 8 — Run the self-review pass; revise if weak
- [ ] Step 9 — Present the synthesis, then file/save it

### What this skill does

Instead of summarizing each source separately, this skill:

1. **Identifies cross-source themes** — patterns and ideas that show up across multiple materials
2. **Spots contradictions and tensions** — where sources disagree or present conflicting views
3. **Reveals knowledge gaps** — what's NOT covered despite the breadth of sources
4. **Extracts implications for you** — what this all means for your specific situation or decisions
5. **Recommends next steps** — what research to do, questions to ask, or actions to take

### Important Constraints

- **Must synthesize, not summarize.** If you ask for this skill but you really want a summary of a single source, it will politely redirect you.
- **Requires multiple sources.** Won't work for single documents (use a regular summarize function for that).
- **Minimum output requirement (one rule, used everywhere):** the synthesis must address all three of cross-source themes, contradictions/tensions, and knowledge gaps. If a category genuinely has nothing in it, say so explicitly in that section and give the one-line reason — an empty section is a finding, silence is not. (Safe fallback: if true synthesis isn't possible at all, deliver a structured summary plus identified gaps and say why synthesis failed.)

### Self-Review (Auto-Revision)

If the synthesis output is weak (summarizes instead of synthesizes, misses contradictions, or has no actionable implications), revise it against these criteria before delivering:

- Must identify cross-source patterns, not just summarize each source
- Must address contradictions and tensions between sources — naming them, or stating explicitly that the sources do not conflict and why
- Must address knowledge gaps — naming what's NOT covered by any source, or stating explicitly that coverage is complete and why
- Implications must be specific and actionable, not generic
- Must include a Contrarian Read that states the consensus, argues the strongest evidence-backed opposing case (or uses the one-line "No credible contrarian case" escape hatch), and names what would settle it — hedged both-sidesing fails

Only trigger a revision pass when the output is flagged as weak, or when the synthesis fails the minimum output requirement above — all three of themes, contradictions, and gaps addressed, with an explicit stated reason for any category left empty.

### Failure Modes to Avoid

- Summarizing each source independently instead of finding cross-source patterns
- Missing contradictions and conflicts between sources
- Ignoring gaps and unanswered questions
- Treating all sources as equally credible without noting conflicts

### Filing / Saving the Synthesis

After presenting the synthesis, save it so it can be retrieved later. A simple structured document works well:

```
---
date: [today]
type: Insight
topic: [topic]
title: "Research Synthesis — [topic]"
summary: "[1-2 sentence summary of what was synthesized and key finding]"
why_it_matters: "[Why this synthesis matters to your goals or decisions]"
---

## Key Findings
[findings]

## Cross-Source Themes
[themes]

## Contradictions & Tensions
[contradictions]

## Knowledge Gaps
[gaps]

## Implications for You
[implications]

## Recommended Next Steps
[steps]

## Contrarian Read
[consensus in one line; strongest evidence-backed case against; what would settle it — or the one-line escape hatch]

## Sources Analyzed
[list of sources with brief identifiers]
```

## Output

You'll receive a structured analysis with these sections:

### Key Findings
The most important insights that emerge from cross-source analysis. Not just facts from individual sources, but discoveries that only emerge when you look at the collection.

### Cross-Source Themes
Patterns and ideas that appear in multiple sources, stated in different ways. Recurrence is corroboration, not proof: how much weight it carries depends on whether the sources are independent and how good each one is. Check the chain before counting — three outlets citing the same underlying study are one source, not three, and repetition of a weak source produces a confident-sounding theme with nothing behind it. Say how many *independent* sources back each theme, and flag themes that recur only through shared lineage.

### Contradictions & Tensions
Where sources disagree, contradict, or present conflicting evidence. This includes methodological conflicts, different conclusions, or competing priorities.

### Knowledge Gaps
What's conspicuously absent. What questions remain unanswered? What perspectives are missing?

### Implications for You
What this synthesis means for your specific context, decisions, or goals. This is about translating research into action.

### Recommended Next Steps
What to research next, what questions to ask, what experiments to run, or what decisions you're now ready to make.

### Contrarian Read
State the consensus this synthesis converged on, then argue the strongest evidence-backed case against it. Three parts: (1) one line stating the consensus; (2) the strongest evidence-backed case against it — specific sources or data points, steelmanned, no hedging; (3) what evidence would settle it. If the sources genuinely agree, the section body is exactly: `No credible contrarian case: <one line why>.` Never manufacture dissent, and never use the escape hatch on a genuinely contested topic.

### Sources Analyzed
The sources the synthesis drew on, each with a brief identifier so a reader can tell which material produced which claim.

## Example

Input: "I've collected three sources on hybrid-work productivity: a company engineering-team survey, an academic meta-analysis of remote-work studies, and a management-consultancy report. What do they tell us together, and what am I missing?"

Output:

```
## Key Findings
- All three link hybrid productivity to autonomy over *when* work happens, not *where* — but only one measures output directly; the other two measure self-reported satisfaction and infer productivity from it.
- The strongest cross-source signal is about coordination cost, not individual focus: gains in deep work are partly offset by slower cross-team decisions.

## Cross-Source Themes
- Autonomy-over-schedule as the real driver (all three sources).
- Onboarding and junior-employee development suffer under low in-person time (survey + consultancy report).
- Meeting load, not commute, is the dominant complaint (survey + meta-analysis).

## Contradictions & Tensions
- The meta-analysis finds a small positive productivity effect; the consultancy report claims a large one. The gap traces to method: the meta-analysis uses controlled output measures, the report uses manager estimates, which run optimistic.
- The survey says collaboration improved; the meta-analysis says cross-team collaboration measurably slowed. They are measuring different collaboration (within-team vs across-team).

## Knowledge Gaps
- None of the three isolates the effect of *fully remote* vs *hybrid* — they blur the two.
- No source covers long-run effects (>18 months); all are short-window.
- No cost data: productivity is discussed without real-estate or tooling costs.

## Implications for You
- Treat the large-effect consultancy number as a ceiling, not a planning input; the controlled meta-analysis figure is the safer base case.
- If your concern is junior-staff development, the evidence points to protecting in-person time specifically for onboarding, not blanket office mandates.

## Recommended Next Steps
- Find or run one source that measures actual output (not self-report) in a hybrid setting matching yours.
- Get a source on long-run (18+ month) effects before committing to a permanent policy.

## Contrarian Read
Consensus: hybrid work is net-positive for productivity when autonomy is preserved. Strongest case against: the only controlled-output source in the set finds only a *small* effect and a measurable cross-team-coordination penalty — the "net-positive" story leans heavily on self-reported and manager-estimated data, which is exactly the data most prone to optimism bias. What would settle it: a controlled study measuring real output and cross-team cycle time over 18+ months in a comparable org.

## Sources Analyzed
- Internal engineering-team hybrid-work survey
- Academic meta-analysis of remote-work productivity studies
- Management-consultancy hybrid-work report
```

## Notes

- Output must address all three of cross-source themes, contradictions, and gaps — an empty category is stated explicitly with its reason, never silently dropped. If true synthesis isn't possible at all, the safe fallback is a structured summary plus identified gaps, with a note on why synthesis failed.
- The Contrarian Read escape hatch (`No credible contrarian case: <why>`) is only for sources that genuinely agree — never use it to dodge a contested topic, and never manufacture dissent where none exists.
- Diverse sources produce richer synthesis than many sources that all say the same thing.
