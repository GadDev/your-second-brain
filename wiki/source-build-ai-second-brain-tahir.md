---
type: source
tags: [llm-wiki-pattern, implementation, claude-code]
created: 2026-07-07
updated: 2026-07-07
source: "raw/llm-wiki/Build an AI Second Brain(LLM Wiki Pattern) With Claude Code and Obsidian.md"
---

# Build an AI Second Brain — LLM Wiki Pattern With Claude Code and Obsidian (Medium)

Practical implementation guide by Tahir Balarabe (Medium, June 1, 2026). Describes building a [[llm-wiki-pattern]] wiki using [[claude-code]] and [[obsidian]].

## Key ideas and quotes

- "Raw separate from wiki" described as the "load-bearing rule" — break it and the whole thing collapses.
- The `raw/` folder as "memory"; the `wiki/` folder as "understanding." They need each other but must not touch.
- AI does the scaffolding; human still does the climbing (judgment about what matters).
- Demonstrated with 42 Claude.ai conversations exported from JSON to Markdown, then ingested via `/ingest` — produced 42 linked wiki pages in one command.

## Practical details

- `/lint` found 17 broken links. Claude Code fixed the trivial ones automatically; broken source citation format required a human judgment call.
- Estimated 60 minutes to set up; took longer. Time was spent writing rules, not organizing.
- Daily workflow: drop → `/ingest` (once a day, or once a week, or whenever) → review.

## FAQ highlights

- Full `/ingest` on a large batch takes 10+ minutes and significant tokens; recommended to start with `/ingest 2` (2 sources) as a demo.
- After ingest, Graph View "transforms into an interconnected web."
- JSON exports (Claude, ChatGPT) need conversion to Markdown first before ingest.
- Mobile: Obsidian mobile app (iOS/Android) syncs the vault; Claude Code runs desktop-only.

## GitHub

github.com/balarabetahir/Build-an-AI-Second-Brain-LLM-Wiki-Pattern-With-Claude-Code-and-Obsidian
