---
type: source
tags: [llm-wiki-pattern, claude-obsidian, agrici-daniel]
created: 2026-07-07
updated: 2026-07-07
source: "raw/llm-wiki/Obsidian AI Second Brain The Open-Source Plugin That Organizes Itself.md"
---

# Obsidian AI Second Brain: The Open-Source Plugin That Organizes Itself (agricidaniel.com)

Product overview and analysis of [[claude-obsidian]] by [[agrici-daniel]] (April 10, 2026).

## Key claims and metrics

- Personal knowledge base AI market: $1.65B in 2025, growing at 30.3% CAGR toward $6.15B by 2030 (Research and Markets, 2026).
- [[obsidian]] has 2,700+ community plugins; 100+ AI-related.
- wiki-ingest consistently produces 8-15 wiki pages per source, avg 12 wikilinks/page (tested across 30+ sources).
- A 200-page vault from 25 sources: 94% of pages connected to at least 2 others — zero manual linking.
- Knowledge worker time savings from AI-driven KM: 30-45% (McKinsey, 2025).
- Federal Reserve research: generative AI saves 5.4% of work hours (~2.2 hrs/week).

## Hot cache detail

`wiki/hot.md` — ~500 tokens to read. Eliminates 2,000-3,000 tokens of session re-establishment. 4-6x token return on investment.

## Key design principle

"The value of a knowledge base is proportional to its link density, not its note count. A vault with 100 notes and 500 cross-references is more useful than one with 1,000 notes and 50 links."

## Multi-agent support

Works across Claude Code, Gemini CLI, Codex CLI, OpenCode, Cursor, Windsurf via `setup-multi-agent.sh`. Local-first: if Claude goes down, the wiki still works. If you switch AI providers, knowledge comes with you.

## /autoresearch

Autonomous 3-round web research loop → structured wiki pages with citations. Example: 23 wiki pages on AI marketing automation in 15 minutes of supervision vs. a full weekend manually.
