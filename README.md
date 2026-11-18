# Crate

AI skill files for brand, marketing and strategy work, by [Hunter Marshall](https://www.mesteezo.com).

Each skill is one Markdown file that teaches an AI assistant one job: building a campaign brief, extracting a brand voice, pressure-testing a content idea, writing hooks, and more. No code, no dependencies.

## Use one
Drop a skill's folder into your assistant's skills directory and it loads when the work matches:

```
~/.claude/skills/<skill-name>/SKILL.md        # available everywhere
<your-project>/.claude/skills/<skill-name>/SKILL.md   # one project
```

The files follow the open Agent Skills format, so they also work in Cursor, Codex and VS Code. Not using an agent? Read the file as a checklist and run the steps yourself.

## Skills
| Skill | What it does |
|---|---|
| **Brand & content** | |
| `campaign-brief-builder` | Turns a loose campaign idea into a one-page brief: objective, audience, message, channels, metrics, owners |
| `brand-voice-extractor` | Turns a few content samples into a reusable voice guide: tone, vocabulary, rhythm, rules |
| `content-sharpener` | Pressure-tests a content idea before it's made; shapes it into a brief or kills it |
| `hook-generator` | Writes and ranks opening lines for posts, emails, ads and video, and explains why the winners win |
| `content-repurposer` | Rebuilds one strong piece for LinkedIn, X, email and short video, native to each |
| **Strategy & decisions** | |
| `strategic-planning` | Stress-tests an initiative before you commit, and ends with a decision write-up |
| `product-dev-planning` | Plans what to build and in what order, before anything gets built |
| `research-synthesizer` | Turns several sources into themes, contradictions, gaps and implications |
| **Review** | |
| `adversarial-review` | Argues against a plan or draft to find what breaks it |
| `parallel-perspectives` | Runs the same question past several distinct viewpoints and compares them |
| `swarm-deliberation` | A structured multi-voice debate for hard calls |

## License
MIT. See each skill's `LICENSE`.
