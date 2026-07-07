---
type: concept
tags: [llm-wiki-pattern, architecture, markdown]
created: 2026-07-07
updated: 2026-07-07
aliases: [wiki/, wiki folder, the wiki]
---

# Wiki

The second layer of the [[llm-wiki-pattern]] architecture: a collection of markdown pages owned entirely by the [[llm]], written and maintained every session.

## Role

- **LLM-written** — the human never hand-edits wiki pages (the system breaks if they do)
- **Structured output** — summaries, entity pages, concept pages, relationships via `[[wikilinks]]`
- **Persistent** — the knowledge base that grows and compounds with every source
- **Queryable** — answers come from the wiki, not reconstructed at query time

## Page types

- **Source** — summary of each raw input file
- **Entity** — person, organization, tool, or other named thing
- **Concept** — idea, method, theme, principle
- **Comparison / analysis** — synthesized pages, often filed from query results
- **Overview** — the evolving thesis of the whole brain

## Key convention

One subject per file, kebab-case filenames, required frontmatter, dense `[[wikilinks]]` on first mention. See [[llm-wiki-pattern]] for the full schema.

## The compounding effect

By week 3, contradictions get flagged automatically. By week 4, old solutions resurface in response to new problems. By week 8, you have 50-80 interconnected pages that represent your best thinking on recurring topics.

The wiki made researchers more deliberate about what they capture because they know it will compound.

## Related

[[raw-sources]] · [[schema-file]] · [[compounding-knowledge]] · [[llm-wiki-pattern]]
