---
type: concept
tags: [knowledge-management, core-pattern]
created: 2026-07-07
updated: 2026-07-07
aliases: [Compounding Wiki, Persistent Wiki]
---

# Compounding Knowledge

The property of a [[llm-wiki-pattern]] wiki where each new source makes the entire system more valuable — cross-references are already present, contradictions have been flagged, and synthesis reflects everything ingested so far.

## Why it matters

In [[rag]] systems, the 50th source is not dramatically more useful than the first — each query reconstructs from scratch. In a compounding wiki, the 50th source gets cross-referenced against everything already there. Dense link meshes emerge: an article about automation connects to a podcast about AI coding workflows, which connects to an essay on writing and thinking — threads the user would never have drawn manually.

> "The wiki keeps getting richer with every source you add and every question you ask." — [[andrej-karpathy]]

## Queries compound too

An important mechanism: good query answers can be filed back into the wiki as new pages (via `/save`). A comparison, an analysis, a discovered connection — these are as valuable as ingested sources and should not disappear into chat history. This is how exploration compounds into the knowledge base.

## Failure mode: append-only rot

**Contradiction with Eugeniu Ghelbur's analysis:** [[andrej-karpathy]]'s original design is append-only, which means the wiki grows but doesn't stay current. Past ~100-200 sources, stale claims accumulate invisibly (a fact written in 2024 sits alongside a 2026 correction with no clear winner). [[eugeniu-ghelbur]] argues a compounding wiki must *rewrite* pages with the latest evidence, not just append. This is an open design debate.

## Related

[[llm-wiki-pattern]] · [[rag]] · [[second-brain]] · [[ai-first-vault-principle]]
