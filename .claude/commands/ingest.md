---
description: Read a raw source and integrate it into the wiki
argument-hint: [path in raw/ or which source to process]
---

Read all files in `raw/` (ignore `raw/processed/`). If $ARGUMENTS specifies a file or pattern, process only those.

For each source:

1. **Identify** the key concepts, people, tools, and ideas.
2. **Create or enrich** the corresponding page in `wiki/` for each significant element. Use `type: source` for summaries of raw files; `type: entity` for people/orgs/tools; `type: concept` for ideas and themes.
3. **Weave `[[backlinks]]`** between related pages on first mention.
4. **Flag contradictions.** If two sources conflict, note both claims and their sources in the relevant article rather than overwriting.
5. **Move** each processed file to `raw/processed/`.

Once all sources are processed:

6. **Update `wiki/index.md`** — add new pages and refresh changed summaries, grouped by `type`.
7. **Append to `log.md`:** `## [YYYY-MM-DD] ingest | <N> files, <M> pages created/modified` followed by a bullet list of created/updated pages.
