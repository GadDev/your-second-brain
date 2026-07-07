---
type: concept
tags: [llm-wiki-pattern, architecture]
created: 2026-07-07
updated: 2026-07-07
aliases: [raw/, raw folder, raw sources]
---

# Raw Sources

The first layer of the [[llm-wiki-pattern]] architecture: an immutable drop box for source documents that the [[llm]] reads but never edits.

## Role

- **Input only** — articles, transcripts, meeting notes, PDFs, chat exports, anything worth remembering
- **Zero organization required** — the AI's job to categorize, not yours
- **Immutable** — the LLM reads and may move to `raw/processed/` after ingest, but never modifies original content
- **Source of truth** — the original record is always available for reconsideration

## Why immutability matters

Preserving the original source material preserves the ability to reconsider. What seems important today might seem less important tomorrow. If you summarize and file everything immediately, you bake in your first interpretation. By keeping raw sources untouched, you retain the option to re-read and reframe later.

As [[tahir-balarabe]] frames it: "The raw folder is my memory. The wiki folder is my understanding."

## Contrast with traditional PKM

Traditional systems require the human to organize and categorize as they capture. The [[llm-wiki-pattern]] defers all that work: capture in raw/, let the AI do the filing.

## Related

[[llm-wiki-pattern]] · [[wiki]] · [[schema-file]] · [[compounding-knowledge]]
