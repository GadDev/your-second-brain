---
type: source
tags: [llm-wiki-pattern, karpathy, primary-source]
created: 2026-07-07
updated: 2026-07-07
source: raw/llm-wiki/llm-wiki.md
---

# LLM Wiki (Karpathy Gist)

The original public description of the [[llm-wiki-pattern]] by [[andrej-karpathy]], published April 2, 2026 as a GitHub gist.

## Key points

- Defines the three-layer architecture: raw sources (immutable), wiki (LLM-maintained markdown), schema (configuration document).
- Describes three operations: **Ingest**, **Query**, **Lint**.
- `index.md` is content-oriented (catalog); `log.md` is chronological (timeline, greppable with `## [YYYY-MM-DD] op | title` prefix).
- Notes optional CLI tooling: `qmd` for hybrid BM25/vector search at larger scale.
- Tips: [[obsidian-web-clipper]], image downloads, Marp for slides, Dataview for frontmatter queries.
- Explicitly abstract: "the document's only job is to communicate the pattern. Your LLM can figure out the rest."

## Use cases given

Personal (goals, health), research (papers over months), reading a book (character/theme pages), business/team (internal wiki fed by Slack/transcripts).

## Primary source

gist.github.com/karpathy/442a6bf555914893e9891c11519de94f
