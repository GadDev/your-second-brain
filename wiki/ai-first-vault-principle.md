---
type: concept
tags: [llm, knowledge-management, note-design]
created: 2026-07-07
updated: 2026-07-07
aliases: [AI-First Notes, AI-First Vault]
---

# AI-First Vault Principle

A note-design philosophy proposed by [[eugeniu-ghelbur]]: wiki pages should be optimized for LLM retrieval and reasoning, not for human reading — because in a [[llm-wiki-pattern]] vault, the LLM does most of the reading.

## The inversion

Every PKM tradition — [[zettelkasten]], [[second-brain]], evergreen notes — writes notes for a human reader, in flowing prose resembling Wikipedia articles. The AI-First Vault Principle argues this is wrong: *you do not re-read your own notes*. The LLM does. So notes should be written for how an LLM retrieves and parses them.

## Seven rules (Ghelbur's spec)

1. A `## For future Claude` preamble — tells the LLM in 3 sentences whether to keep reading.
2. Machine-readable YAML frontmatter with `type`, `confidence`, `ai-first: true`.
3. Mandatory wikilinks on every key entity/concept.
4. Recency marker per external claim (so the LLM knows what to verify).
5. Source URLs preserved verbatim.
6. Confidence levels where applicable.
7. Self-contained context — the note is understandable without reading its neighbors.

## Example frontmatter

```yaml
---
type: person
name: "Andrej Karpathy"
date: 2026-04-29
tags: [ai-researcher, llm-wiki-pattern]
ai-first: true
confidence: high
---
```

## Trade-off

An AI-first note is harder for a human to scan than a regular prose note. It is dramatically faster for an LLM to retrieve, parse, and reason over. Ghelbur calls this the "most contrarian" of his five extensions to the original [[llm-wiki-pattern]].

**Contradiction with [[andrej-karpathy]]'s original:** Karpathy's gist treats the wiki as serving both humans and LLMs. Ghelbur's rebuild inverts that: the LLM is the primary reader.

This wiki does not currently follow the AI-First Vault Principle — pages are written in human-readable encyclopedic format per [[CLAUDE.md]].

## Related

[[llm-wiki-pattern]] · [[eugeniu-ghelbur]] · [[obsidian-second-brain]] · [[compounding-knowledge]] · [[pkm]]
