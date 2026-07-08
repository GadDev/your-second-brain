---
description: Read a raw source and integrate it into the wiki
argument-hint: [path in raw/ or which source to process]
---

Read all files in `raw/` (ignore `raw/processed/`). If $ARGUMENTS specifies a file or pattern, process only those.

For each source:

1. **Identify** the key concepts, people, tools, and ideas.
2. **Create or enrich** the corresponding page in `wiki/` for each significant element. Use OKF-compliant frontmatter with Obsidian extensions:
   - `type:` (REQUIRED) — source | entity | concept | comparison | overview
   - `title:` (RECOMMENDED) — Explicit display name extracted from content or filename
   - `description:` (RECOMMENDED) — One-sentence summary (first paragraph)
   - `tags:` (RECOMMENDED) — ≥1 relevant topic tags
   - `timestamp:` (RECOMMENDED) — ISO 8601 datetime of processing
   - `created:` (EXTENSION) — YYYY-MM-DD creation date
   - `updated:` (EXTENSION) — YYYY-MM-DD last modified date
   - `aliases:` (EXTENSION) — Optional alternate names
   - `source:` (EXTENSION) — For source pages only: path to raw file
3. **Weave `[[backlinks]]`** between related pages on first mention.
4. **Flag contradictions.** If two sources conflict, note both claims and their sources in the relevant article rather than overwriting.
5. **Move** each processed file to `raw/processed/`.

Once all sources are processed:

6. **Update `wiki/index.md`** — add new pages and refresh changed summaries, grouped by `type`.
7. **Append to `log.md`:** `## [YYYY-MM-DD] ingest | <N> files, <M> pages created/modified` followed by a bullet list of created/updated pages.
