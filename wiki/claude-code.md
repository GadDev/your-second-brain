---
type: entity
tags: [tool, ai-agent, anthropic]
created: 2026-07-07
updated: 2026-07-07
aliases: [Claude Code CLI, claude]
---

# Claude Code

An AI coding agent by Anthropic, operated from the terminal, that reads and writes files in a local directory and executes shell commands.

## Role in the LLM Wiki Pattern

Claude Code is the most common agent used to implement the [[llm-wiki-pattern]]. It:
- Reads the [[schema-file]] (`CLAUDE.md`) at every session start
- Executes slash commands defined in `.claude/commands/` (e.g., `/ingest`, `/lint`, `/query`, `/save`)
- Reads raw sources, writes and updates wiki pages, maintains `index.md` and `log.md`

As of April 2026: most-used AI coding tool in a Pragmatic Engineer survey of 15,000 developers, with 46% "most loved" rating and 22,000+ GitHub stars.

## Slash commands

Any `.md` file in `.claude/commands/` becomes a slash command. `$ARGUMENTS` in the file captures everything typed after the command name. This is the mechanism that makes `/ingest raw/article.md` and `/query why doesn't RAG scale?` work — the argument is injected directly into the prompt.

## Plugin ecosystem

340 plugins and 1,367 agent skills as of April 2026, with an official marketplace hosting 101 plugins (33 from Anthropic). Notable wiki-related skills: [[obsidian-second-brain]] by [[eugeniu-ghelbur]], [[claude-obsidian]] by [[agrici-daniel]].

## Related

[[llm-wiki-pattern]] · [[obsidian]] · [[schema-file]] · [[obsidian-second-brain]] · [[claude-obsidian]] · [[andrej-karpathy]]
