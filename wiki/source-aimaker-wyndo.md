---
type: source
tags: [llm-wiki-pattern, implementation, obsidian]
created: 2026-07-07
updated: 2026-07-07
source: "raw/llm-wiki/How I Took Karpathy's LLM Wiki and Built an AI-Powered Second Brain in Obsidian.md"
---

# How I Took Karpathy's LLM Wiki and Built an AI-Powered Second Brain in Obsidian (AI Maker Substack)

Implementation guide by Wyndo (aimaker.substack.com, April 16, 2026). Covers building an [[llm-wiki-pattern]] wiki using Obsidian Skills by Steph Ango (CEO of [[obsidian]]).

## Key ideas

- Three slash commands used: `/ingest-url <url>` (extracts article, compiles to wiki, touches 5-15 pages), `/process-inbox` (classifies fleeting thoughts), `/lint-wiki`.
- **Obsidian Skills** — a set of agent skills released by Steph Ango to teach [[claude-code]] Obsidian's native language: wikilinks, callouts, canvas, frontmatter, Obsidian CLI, Bases. This is described as "the missing piece" that makes Obsidian more than "a folder of markdown files."
- Compounding example: article about Tim Dettmers' framework → connected to Addy Osmani's coding workflow → connected to Dan Koe's writing essay. Three different topics, one emergent thread.

## Folder structure

```
sources/   + inbox/  → Layer 1: Input
wiki/                → Layer 2: LLM-generated pages
CLAUDE.md            → Layer 3: Schema
```

Sources organized by topic: `ai/`, `health-and-fitness/`, `human-psychology/`, `personal-productivity/`, `books/`, `podcasts/`.

## Source ingestion methods

- [[obsidian-web-clipper]] — manual, one-click for articles and YouTube transcripts.
- Obsidian CLI + agent: automated, for batch or scheduled ingestion.
