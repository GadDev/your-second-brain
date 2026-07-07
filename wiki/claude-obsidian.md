---
type: entity
tags: [tool, llm-wiki-pattern, open-source]
created: 2026-07-07
updated: 2026-07-07
aliases: [claude-obsidian plugin]
---

# claude-obsidian

An open-source [[claude-code]] plugin by [[agrici-daniel]] implementing the [[llm-wiki-pattern]] with 10 specialized skills, a hot cache for session memory, and multi-agent support.

## Stats (as of April 2026)

- 358 GitHub stars
- MIT licensed, free
- Works across Claude Code, Gemini CLI, Codex CLI, OpenCode, Cursor, Windsurf

## 10 skills

| Skill | Purpose |
|-------|---------|
| `wiki` | Setup vault, scaffold structure |
| `wiki-ingest` | Extract entities, create cross-referenced pages |
| `wiki-query` | Search vault with citations |
| `wiki-lint` | Find orphans, dead links, contradictions, gaps |
| `save` | File conversations as structured wiki notes |
| `autoresearch` | Autonomous multi-round web research |
| `canvas` | Visual reference boards |
| `defuddle` | Strip web page clutter (saves 40-60% tokens on URLs) |
| `obsidian-markdown` | Obsidian syntax reference |
| `obsidian-bases` | Create Obsidian Bases database views |

## Hot cache

A file at `wiki/hot.md` (~500 words) stores the most recent session context. Read first on every new session — restores working memory without a recap. Cost: ~500 tokens. Benefit: eliminates 2,000-3,000 tokens of re-establishing context.

## Key differentiator vs. Smart Connections / Copilot

Smart Connections and Copilot are chat interfaces over static notes. `claude-obsidian` is a knowledge engine — it creates, organizes, maintains, and evolves notes autonomously. It cites specific wiki pages, not training data.

## Install

```bash
git clone https://github.com/AgriciDaniel/claude-obsidian.git my-wiki
bash my-wiki/bin/setup-vault.sh
```

## Related

[[agrici-daniel]] · [[llm-wiki-pattern]] · [[obsidian]] · [[claude-code]] · [[obsidian-second-brain]]
