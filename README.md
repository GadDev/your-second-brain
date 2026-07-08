# LLM Wiki — Second Brain Scaffold

A workshop scaffold for building a personal knowledge base maintained by an LLM agent, inspired by Andrej Karpathy's vision of a personal wiki.

The core idea: instead of querying raw documents at every turn (RAG), the LLM **incrementally builds and maintains a persistent wiki** — a structured, interlinked collection of Markdown pages that compounds over time. Cross-references, contradictions, and synthesis are computed once and kept current, not re-derived on every question.

## What you need

- [Obsidian](https://obsidian.md/) (free)
- [Obsidian Web Clipper](https://obsidian.md/clipper) (Chrome extension)
- Claude Code


## How it works

```
raw/              ← you drop sources here (articles, notes, transcripts, PDFs)
wiki/             ← the LLM writes and maintains all pages here
  └── index.md   ← auto-generated table of contents
log.md            ← append-only operation history
CLAUDE.md         ← the schema: naming conventions, page format, linking rules
.claude/commands/ ← the four slash commands
```

**You** curate sources and ask questions. **The LLM** does all the bookkeeping — summarizing, cross-referencing, flagging contradictions, keeping the index current.

Open `wiki/` in [Obsidian](https://obsidian.md) to browse the knowledge graph as the LLM builds it.

## The four commands

| Command | What it does |
|---------|-------------|
| `/ingest` | Read new sources in `raw/`, compile wiki pages, weave backlinks, flag contradictions, move processed files to `raw/processed/` |
| `/query <question>` | Answer from the wiki with citations; flag anything sourced from general knowledge |
| `/save <content>` | Turn a conversation answer or any text into a new wiki page |
| `/lint` | Health-check: broken links, orphans, contradictions, concepts missing their own page |

## Getting started

1. Clone or copy this repo as your wiki folder.
2. Open it in [Claude Code](https://claude.ai/code) (or any agent that reads `CLAUDE.md`).
3. Drop a source file into `raw/` and run `/ingest`.
4. Open `wiki/` in Obsidian to explore the result.

Edit `CLAUDE.md` to adapt the schema to your domain — page types, frontmatter fields, linking conventions. The schema is intentionally minimal; co-evolve it with your agent as conventions settle.

## Workshop

This scaffold is used in the **AI Club LLM Wiki workshop**. The session covers:

- The difference between RAG and a compounding wiki
- How `CLAUDE.md` acts as a contract between you and the agent
- Live demo: ingesting sources and querying the result in Obsidian
- Designing your own schema for a domain of your choice

## Credits

Concept inspired by Andrej Karpathy's writing on personal knowledge management and the broader idea of LLMs as tireless wiki maintainers.
