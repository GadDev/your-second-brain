---
type: source
tags: [llm-wiki-pattern, obsidian-second-brain, eugeniu-ghelbur, critique]
created: 2026-07-07
updated: 2026-07-07
source: "raw/llm-wiki/I rebuilt Karpathy's LLM Wiki gist what's missing.md"
---

# I Rebuilt Karpathy's LLM Wiki Gist: What's Missing (The AI Operator)

Critical analysis and rebuild by [[eugeniu-ghelbur]] (The AI Operator, April 29, 2026). Identifies five limitations of [[andrej-karpathy]]'s original append-only design.

## Key argument

Karpathy's pattern is a conceptual blueprint, not a runnable spec. Every public implementation reviewed (six on GitHub, two on Substack, one on dev.to) treats the gist as a complete spec. None solve the problems that appear past a few hundred sources.

## Five extensions

1. **Ingest must rewrite** — not just append. The live state of a page reflects the latest evidence; old version preserved as a dated entry below.
2. **Contradictions must be resolved automatically** — by source recency, authority, and confidence level. Losing claim archived with explanation. (Original: flag for manual resolution.)
3. **Patterns surfaced unsolicited** — synthesis pages written without being asked.
4. **Scheduled maintenance agents** — nightly/weekly automation. (Original: all on-demand.)
5. **[[ai-first-vault-principle]]** — notes written for LLM retrieval, not human reading. Most contrarian extension.

## Version history cited

- v1: Karpathy gist (2026-02) — append-only, manual lint, human-readable.
- v2: rohitg00's gist (2026-03) — adds confidence scoring, supersession, contradiction detection.
- v3: `obsidian-second-brain` (this rebuild) — adds scheduled agents, automatic synthesis, AI-first structure.

## Reversibility lesson

When `/research-deep` first ran, it wrote garbage (wrong model, `<think>...</think>` tags saved verbatim, Python dicts in frontmatter). Lesson: "the right level of automation is not 'everything always,' it is 'everything reversibly.'" Every scheduled agent now writes a diff log and waits 24 hours before permanence.
