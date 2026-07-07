---
type: entity
tags: [person, ai-engineer, llm-wiki-pattern]
created: 2026-07-07
updated: 2026-07-07
aliases: [Ghelbur]
---

# Eugeniu Ghelbur

AI Automation Engineer at Single Grain; author of [[obsidian-second-brain]], the most-starred open-source implementation of the [[llm-wiki-pattern]].

## Background

- AI Automation Engineer at Single Grain
- Writes at The AI Operator (theaioperator.io)
- Built and open-sourced `obsidian-second-brain` on 2026-03-24

## obsidian-second-brain

An open-source Claude Code skill that gives Claude persistent memory through an Obsidian vault. As of 2026-05-10:
- 1,024 GitHub stars
- 99 forks
- 1,374 unique clones in the prior 14 days
- 5,910 unique visitors in 14 days
- MIT licensed

The first external code contributor shipped 695 lines of code adding a `/podcast` command.

## Key contributions to the pattern

Ghelbur published "I rebuilt Karpathy's LLM Wiki gist: what's missing" (April 2026), identifying five limitations of the original append-only design and proposing extensions:

1. **Ingest must rewrite, not just append** — existing pages get updated with the latest evidence; old version preserved as dated entry below.
2. **Contradictions must be resolved automatically** — not just flagged for manual resolution.
3. **Patterns surfaced without being asked** — synthesis runs on its own, not only on query.
4. **Scheduled maintenance agents** — nightly/weekly automation so maintenance happens without being triggered.
5. **[[ai-first-vault-principle]]** — notes written for LLM retrieval, not human reading.

Also introduced the concept that "the right level of automation is not 'everything always,' it is 'everything reversibly'" — every scheduled agent logs its changes and waits 24 hours before making them permanent.

## Related

[[obsidian-second-brain]] · [[llm-wiki-pattern]] · [[ai-first-vault-principle]] · [[andrej-karpathy]] · [[obsidian]] · [[claude-code]]
