---
type: entity
tags: [tool, llm-wiki-pattern, open-source]
created: 2026-07-07
updated: 2026-07-07
aliases: [obsidian-second-brain, Ghelbur's skill]
---

# obsidian-second-brain

An open-source Claude Code skill by [[eugeniu-ghelbur]] that implements and extends the [[llm-wiki-pattern]], giving [[claude-code]] persistent memory through an [[obsidian]] vault.

## Stats (as of 2026-05-10)

- Created 2026-03-24
- 1,024 GitHub stars, 99 forks
- 1,374 unique clones in the prior 14 days
- MIT licensed, free

## Architecture

31 slash commands across four capability layers:

1. **Memory** — every meeting, decision, voice memo, screenshot saved to the right place automatically.
2. **Reasoning** — the vault "argues back": before a decision, shows past failures and reversed decisions on the same topic.
3. **Identity** — loads user's projects and current state in ~10 seconds; every session picks up where the last ended.
4. **Research** — X posts, web research, YouTube transcripts go into the vault, not just a temporary chat.

Plus four **scheduled agents** that run automatically:
- Nightly: closes the day, reconciles contradictions, finds patterns, heals orphan notes, rebuilds the index.
- Weekly: full reconciliation and synthesis pass.

## Key extensions over Karpathy's original

See [[eugeniu-ghelbur]] for the full breakdown. Most significant: pages are **rewritten** (not just appended) when new evidence arrives; contradictions are **resolved automatically** (not just flagged); synthesis runs **unsolicited** (not only on query); maintenance is **scheduled** (not on-demand).

## Safety principle

> "The right level of automation is not 'everything always,' it is 'everything reversibly.'"

Every scheduled agent writes a daily diff note and waits 24 hours before any change becomes permanent. This came from a lesson learned when a `/research-deep` command wrote garbage into the vault on its first run due to model selection errors.

## Related

[[eugeniu-ghelbur]] · [[llm-wiki-pattern]] · [[ai-first-vault-principle]] · [[claude-code]] · [[obsidian]] · [[claude-obsidian]]
