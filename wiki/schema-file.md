---
type: concept
tags: [llm-wiki-pattern, configuration, agent]
created: 2026-07-07
updated: 2026-07-07
aliases: [CLAUDE.md, AGENTS.md, schema, wiki schema]
---

# Schema File

A configuration document (typically `CLAUDE.md` for [[claude-code]] or `AGENTS.md` for OpenAI Codex) that tells the LLM how a wiki is organized — naming conventions, page format, linking rules, and workflows for ingesting, querying, and maintaining the wiki.

## Role

The schema is what makes the LLM a disciplined wiki maintainer rather than a generic chatbot. Without it, each session starts from scratch with no knowledge of the vault's conventions.

> "You and the LLM co-evolve this over time as you figure out what works for your domain." — [[andrej-karpathy]]

## Typical contents

- Directory structure and layer definitions (`raw/`, `wiki/`, etc.)
- Page types and required frontmatter fields
- Linking rules (e.g., `[[wikilinks]]` on first mention of each concept)
- How to handle contradictions between sources
- `index.md` and `log.md` update conventions
- Definitions of the four slash commands

## Co-evolution

The schema is intentionally minimal at first and grows as conventions settle. The LLM proposes refinements; the user accepts, rejects, or adjusts. When a command's behavior and the schema conflict, the schema wins — commands are updated, not the schema.

[[eric-j-ma]] documents his vault structure in `AGENTS.md` and links it to a `HEARTBEAT.md` health-check file. [[eugeniu-ghelbur]]'s rebuild uses ~200 lines of schema.

## Related

[[llm-wiki-pattern]] · [[claude-code]] · [[obsidian]] · [[obsidian-second-brain]]
