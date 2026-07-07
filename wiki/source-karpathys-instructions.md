---
type: source
tags: [llm-wiki-pattern, karpathy, journalism]
created: 2026-07-07
updated: 2026-07-07
source: "raw/llm-wiki/Karpathy's Instructions for Building an AI-Driven Second Brain.md"
---

# Karpathy's Instructions for Building an AI-Driven Second Brain (Techstrong.ai)

Journalism article by Joab Jackson (Techstrong.ai, April 7, 2026) covering [[andrej-karpathy]]'s [[llm-wiki-pattern]] and early community responses.

## Key points

- Positions the pattern as an evolution of [[tiago-forte]]'s [[second-brain]] concept, with the LLM doing the indexing the human was supposed to do.
- Notes Karpathy's own implementation used "a hacky collection of Python scripts" and was not yet fully automated.
- Token efficiency argument: the wiki as a compact, refined dataset reduces per-query token cost vs [[rag]].
- "Stateless AI" problem: the wiki as a way to persist knowledge across sessions so the LLM doesn't start from scratch each time.
- Nick Spisak's X walkthrough: suggested domain-specific vaults (not one giant vault) to avoid diffuse results. Also suggested using Vercel Labs' agent-browser.
- Lex Fridman built a similar system generating "interactive podcasts" on specific topics.
- Robert Scoble built one to track AI news on X.

## Community reaction

"The AI is the librarian. You give it rules via a config file, and it maintains your entire wiki. You never manually organize a single page." — Nick Spisak
