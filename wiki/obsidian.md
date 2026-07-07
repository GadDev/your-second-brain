---
type: entity
tags: [tool, note-taking, pkm]
created: 2026-07-07
updated: 2026-07-07
aliases: [Obsidian.md]
---

# Obsidian

A local-first, plain-text note-taking application built around bidirectional [[wikilinks]] and a visual knowledge graph.

## Key properties

- Stores all notes as plain `.md` files on local disk — no vendor lock-in, no proprietary format
- Bidirectional `[[wikilinks]]` — link between notes, Obsidian auto-generates backlinks
- Graph view — visual map of the entire vault, showing clusters, hubs, and orphans
- 1.5 million users as of early 2026 (22% YoY growth)
- Free for personal use; syncs via iCloud or any cloud storage
- 2,700+ community plugins, 100+ AI-related

## Why plain text mattered for LLMs

When AI coding agents arrived (2025-2026), Obsidian vaults were already in the format LLMs read and write best — no migration needed. This was a prescient but accidental advantage, as [[eric-j-ma]] notes.

## Role in the LLM Wiki Pattern

[[andrej-karpathy]]'s framing: "Obsidian is the IDE, the LLM is the programmer, the wiki is the codebase." The user points [[claude-code]] (or another agent) at the vault; the LLM writes and maintains the wiki pages; the user browses the result in Obsidian's graph view in real time.

Recommended setup: open `wiki/` as an Obsidian vault (not the whole repo root), so the graph view shows only the compiled wiki.

## Key plugins for LLM Wiki workflows

- **Obsidian Web Clipper** — browser extension; converts web pages to local markdown. See [[obsidian-web-clipper]].
- **Dataview** — runs queries over YAML frontmatter; generates dynamic tables.
- **Marp** — renders Markdown as presentation slides.
- **Bases** — database views over vault contents (used by [[claude-obsidian]]).
- **Excalidraw**, **Canvas** — visual whiteboards.

## Related

[[obsidian-web-clipper]] · [[llm-wiki-pattern]] · [[pkm]] · [[claude-code]] · [[obsidian-second-brain]] · [[claude-obsidian]]
