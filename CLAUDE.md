# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

This repo is a **second brain**: an LLM-maintained wiki. Unstructured sources are dropped into `raw/`; the agent compiles them into an interlinked set of encyclopedia articles under `wiki/` that stays current as sources accumulate. Unlike RAG (which re-derives knowledge from raw chunks on every query), **the wiki is a persistent, compounding artifact** — cross-references, contradictions, and synthesis are computed once and then kept up to date.

**This file is the schema** — the contract for how the brain is organized. It is co-evolved with the user over time. Every rule below is an invariant the agent upholds and that `/lint` checks. When a rule and a command's wording disagree, this file wins; change it deliberately.

## Three layers

| Layer | Path | Ownership |
|-------|------|-----------|
| **Raw sources** | `raw/` | The user's source of truth. The agent reads from it and never edits or deletes files. After ingest, processed files are moved to `raw/processed/`. Images may live under `raw/assets/`. |
| **The wiki** | `wiki/` | **Owned entirely by the agent.** The user reads it (via Obsidian); the agent writes and maintains every page. |
| **The schema** | `CLAUDE.md` (this file) | The contract. Co-evolved; the agent proposes refinements as conventions settle. |

Supporting files: `wiki/index.md` (catalog), `log.md` (timeline), `.claude/commands/` (the four operations).

## Division of labor

The user curates sources, directs analysis, and asks questions. The agent does **all** the bookkeeping — summarizing, cross-referencing, filing, flagging contradictions, keeping the index and log current. Ingest is collaborative by default: surface key takeaways and let the user steer before writing a batch of pages. Never make the user hand-edit the wiki.

## Page types (`wiki/*.md`)

- **source** — a summary of one raw source; `source:` points to its path in `raw/`.
- **entity** — a person, place, org, product, or other named thing.
- **concept** — an idea, theme, method, or topic.
- **comparison / analysis** — a synthesized page, often the filed-back result of a `/query`.
- **overview** — the evolving thesis / top-level synthesis of the whole brain.

## Article invariants

1. **One subject per file.** Filename is lowercase `kebab-case.md` naming the subject (e.g. `retrieval-augmented-generation.md`). No spaces, no capitals. Obsidian resolves `[[wikilinks]]` by filename, so names must be stable and unique.
2. **Frontmatter (YAML) is required.** Keys consumed by `index.md` grouping and Obsidian's Dataview plugin:
   ```yaml
   ---
   type: concept            # source | entity | concept | comparison | overview
   tags: [topic, topic]     # ≥1
   created: 2026-07-06
   updated: 2026-07-06      # bump on every content change
   aliases: []              # optional: alternate names that resolve to this page
   source: raw/foo.md       # source pages only: path to the raw file
   ---
   ```
3. **Body** opens with an `# H1` matching the subject, then a **one-sentence summary** (the definition). That sentence is what `index.md` reproduces — keep it self-contained and current.
4. **Link densely.** On the *first* mention of any other subject that has (or warrants) its own page, wrap it in an Obsidian `[[wikilink]]`. These links are the graph edges. Do not maintain a manual "Related" section — Obsidian derives backlinks from inline links.
5. **Flag contradictions in place.** When a new source conflicts with an existing claim, note both and their sources on the relevant page rather than silently overwriting. The overview page carries the current thesis and its open questions.

## `index.md` — content catalog

Content-oriented and always complete. Lists **every** page, grouped by `type`, each as `[[link]] — one-line summary` (optionally with date or source count). Regenerated on every ingest and on `/save`. The agent reads it first when answering a `/query`, then drills into the linked pages.

## `log.md` — chronological timeline

Append-only, newest at the bottom. One entry per operation. Every entry starts with a fixed, greppable prefix so `grep "^## \[" log.md | tail -5` yields recent activity:

```
## [2026-07-06] ingest | Attention Is All You Need
- Added [[transformer]], [[self-attention]] (source: raw/attention.md)
- Updated [[sequence-model]] (noted RNN comparison), refreshed index.md
```

Operations: `ingest`, `query`, `lint`, `save`.

## Operations → commands (`.claude/commands/`)

- `/ingest [source]` — read unprocessed sources in `raw/`, compile wiki pages, weave backlinks, flag contradictions, move processed files to `raw/processed/`, refresh `index.md`, append to `log.md`.
- `/query <question>` — answer from the wiki with citations; offer to file durable answers back as new pages so explorations compound.
- `/lint` — health-check: broken links, orphans, missing pages/frontmatter, contradictions, stale claims, data gaps; suggest next questions and sources.
- `/save <content>` — capitalize: turn text or a conversation answer into a new wiki page, update `index.md`, append to `log.md`.

## Global invariants (enforced by `/lint`)

- No broken links: every `[[target]]` resolves to an existing page filename or a declared alias.
- No orphans: every page is reachable from another page or from `index.md`.
- `index.md` lists every page exactly once with a current summary.
- Required frontmatter, `# H1`, and summary sentence present on every page.
- `updated` reflects the last content change.
- `raw/` files are never edited or deleted — only moved to `raw/processed/` after ingest.

## Notes

The wiki is just a git repo of markdown files — version history and diffing come for free (`/save` commits). At larger scale a dedicated markdown search tool (e.g. `qmd`) can supplement `index.md`; add it to the query workflow if/when it exists. This schema is intentionally minimal — extend it here as the domain demands.
