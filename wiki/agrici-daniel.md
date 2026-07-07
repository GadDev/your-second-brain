---
type: entity
tags: [person, ai-engineer, llm-wiki-pattern]
created: 2026-07-07
updated: 2026-07-07
aliases: [Daniel, Agrici]
---

# Agrici Daniel

Developer and author of [[claude-obsidian]], an open-source Claude Code plugin implementing the [[llm-wiki-pattern]] with 10 specialized skills.

## Background

- Writes at agricidaniel.com
- Focused on AI marketing automation and knowledge management tooling
- Built and open-sourced `claude-obsidian` (358 GitHub stars as of April 2026)

## claude-obsidian

A Claude Code plugin implementing Karpathy's [[llm-wiki-pattern]] with:
- 10 specialized skills (wiki-ingest, wiki-query, wiki-lint, autoresearch, canvas, defuddle, save, obsidian-markdown, obsidian-bases, wiki)
- A **hot cache** (`wiki/hot.md`, ~500 words) that preserves session context between conversations, solving the "recap problem"
- Works across [[claude-code]], Gemini CLI, Codex CLI, OpenCode, Cursor, Windsurf
- MIT licensed, free

In testing across 30+ sources, wiki-ingest consistently produces 8-15 wiki pages per source, with an average of 12 wikilinks per page. A 200-page vault built from 25 sources had 94% of pages connected to at least two others.

## Key insight

"The value of a knowledge base is proportional to its link density, not its note count. A vault with 100 notes and 500 cross-references is more useful than one with 1,000 notes and 50 links."

## Related

[[claude-obsidian]] · [[llm-wiki-pattern]] · [[andrej-karpathy]] · [[obsidian]] · [[claude-code]] · [[eugeniu-ghelbur]]
