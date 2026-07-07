---
type: concept
tags: [llm, retrieval, ai]
created: 2026-07-07
updated: 2026-07-07
aliases: [Retrieval-Augmented Generation, RAG]
---

# RAG

Retrieval-Augmented Generation — a technique where an LLM answers queries by first retrieving relevant chunks from a document store, then generating a response from those chunks.

## How it works

Documents are embedded as vectors and stored in a vector database (Pinecone, ChromaDB, etc.). At query time, the query is also embedded and semantically similar document chunks are retrieved and fed to the LLM as context.

## Limitations vs. the LLM Wiki Pattern

RAG requires rediscovering knowledge from scratch on every query. Subtle questions requiring synthesis of five documents force the LLM to piece together fragments every time — nothing accumulates. Systems like NotebookLM, ChatGPT file uploads, and most enterprise knowledge bases work this way.

The [[llm-wiki-pattern]] is the alternative: compile sources into a persistent wiki once, so cross-references and synthesis already exist when questions are asked. Queries become "look up the page that already exists" rather than "search and rebuild."

Additional drawbacks of RAG at personal scale:
- Requires a vector database (embeddings, infrastructure)
- Raw source data is full of metadata and formatting chaff the model must remove on each call
- Duplicated content across sources must be reconciled anew each session

## When RAG still applies

At very large scale (thousands of sources), even a well-maintained wiki may need a search layer. The [[llm-wiki-pattern]] proponents suggest tools like `qmd` (hybrid BM25/vector search, on-device) as a supplement once the wiki grows past ~500 pages, rather than as a replacement for the wiki architecture.

## Related

[[llm-wiki-pattern]] · [[compounding-knowledge]] · [[obsidian]]
