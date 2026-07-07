---
type: source
tags: [llm-wiki-pattern, obsidian, implementation]
created: 2026-07-07
updated: 2026-07-07
source: "raw/llm-wiki/How I Built a Local LLM Wiki in Obsidian.md"
---

# How I Built a Local LLM Wiki in Obsidian (HackerNoon)

First-person account (HackerNoon, May 7, 2026) of building a personal [[llm-wiki-pattern]] wiki for homelab/infrastructure notes using [[claude-code]] and [[obsidian]].

## Setup

Three-layer structure:
```
captures/  → immutable raw sources
wiki/       → LLM-maintained projects, systems, runbooks, concepts
CLAUDE.md  → schema
```

Subdirectories inside wiki: `projects/`, `systems/`, `runbooks/`, `reference/concepts/`, `blog/`, `assets/`.

## Operations used

- `/capture-url <url>` — strips ads and navigation via `defuddle` CLI, wraps in frontmatter, files under `captures/`.
- `/research <topic>` — three rounds of searching, up to fifteen captures, ends in a synthesis page.
- `/audit` — read-only health check (broken YAML, stale dates, broken wikilinks, orphan notes, status drift).
- `/close` — author's own addition: at session end, updates project next-lookup field, writes dated session log, captures feedback into LLM memory.

## Key insight

The `/close` command (not in Karpathy's original) is "the thing that actually keeps the vault current. Without it, the system half-works."

## Resources cited

- `claude-obsidian` by [[agrici-daniel]]: github.com/AgriciDaniel/claude-obsidian
- `obsidian-second-brain` by [[eugeniu-ghelbur]]: github.com/eugeniughelbur/obsidian-second-brain
- [[eric-j-ma]]'s PKM post
