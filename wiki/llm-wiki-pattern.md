---
type: concept
tags: [knowledge-management, llm, core-pattern]
created: 2026-07-07
updated: 2026-07-07
aliases: [LLM Wiki, llm-wiki, LLM Knowledge Base]
---

# LLM Wiki Pattern

A knowledge-base architecture where an LLM incrementally builds and maintains a persistent, interlinked wiki from raw sources, rather than re-deriving answers from raw documents at every query.

## Core idea

Most AI document systems use [[rag]]: upload files, retrieve relevant chunks at query time, generate an answer. Nothing accumulates. The LLM Wiki pattern inverts this: the LLM reads each source once, extracts key information, and integrates it into a living wiki — updating entity pages, revising topic summaries, flagging contradictions. The wiki is the product; the chat is the interface.

> "Obsidian is the IDE, the LLM is the programmer, the wiki is the codebase." — [[andrej-karpathy]]

## Why it works

The bottleneck in personal knowledge bases is maintenance, not reading or thinking. Humans abandon wikis because the maintenance burden grows faster than the value. LLMs don't get bored, don't forget to update a cross-reference, and can touch 15 files in one pass. Cost of maintenance is near zero.

## Three layers

1. **Raw sources** — immutable source documents. The LLM reads but never edits.
2. **The wiki** — LLM-generated and maintained markdown pages. Entity pages, concept pages, source summaries, a synthesis overview.
3. **The schema** — a document (e.g. `CLAUDE.md`) telling the LLM how the wiki is organized, what conventions to follow, how to handle contradictions.

## Operations

- **Ingest** — drop a source, LLM processes it, touches 10-15 wiki pages per source.
- **Query** — answer from the wiki with citations; answers with lasting value get filed back as pages so [[compounding-knowledge]] continues.
- **Lint** — health-check: broken links, orphans, contradictions, stale claims, missing concept pages.

## Origin

Published by [[andrej-karpathy]] as a public GitHub gist on April 2, 2026. Quickly spawned multiple open-source implementations: [[obsidian-second-brain]] by [[eugeniu-ghelbur]], [[claude-obsidian]] by [[agrici-daniel]], and others.

## Relationship to prior art

The pattern is related in spirit to Vannevar Bush's Memex (1945) — a personal knowledge store with associative trails. Also draws from [[tiago-forte]]'s [[second-brain]] and [[pkm]] traditions, but differs in that the LLM does all the maintenance the human was supposed to do.

## Key debate: append-only vs. rewrite

**Contradiction:** [[andrej-karpathy]]'s original gist treats ingest as append-only — new pages and backlinks are added, existing pages stay frozen. [[eugeniu-ghelbur]] argues this fails past ~100 sources: stale claims accumulate, contradictions multiply, person pages describe someone at their old job. His rebuild rewrites pages with the latest evidence while preserving old versions as dated entries. Both approaches are in active use.

## Key debate: human-readable vs. AI-first notes

**Contradiction:** The original pattern and all PKM traditions ([[zettelkasten]], [[second-brain]]) optimize notes for human reading — Wikipedia-style prose. [[eugeniu-ghelbur]]'s [[ai-first-vault-principle]] inverts this: notes should be optimized for LLM retrieval, not human reading, since the LLM does most of the reading. This is the most contrarian extension of the pattern.

## Related

[[compounding-knowledge]] · [[rag]] · [[second-brain]] · [[obsidian]] · [[claude-code]] · [[schema-file]] · [[obsidian-second-brain]] · [[claude-obsidian]]
