---
type: source
tags: [llm-wiki-pattern, guide, aakash-gupta]
created: 2026-07-07
updated: 2026-07-07
source: "raw/llm-wiki/The Complete Guide to Karpathy's Second Brain.md"
---

# The Complete Guide to Karpathy's Second Brain (Aakash Gupta)

Comprehensive applied guide by [[aakash-gupta]] (AI by Aakash, April 14, 2026). The most detailed walkthrough of the [[llm-wiki-pattern]] published to date.

## Structure

1. **Why second brains die** — maintenance burden, not discipline. Existing tools ([[notebook-lm]], ChatGPT uploads, Notion AI) all have the same flaw: retrieve at query time instead of building persistent knowledge.
2. **What Karpathy figured out** — three-part system: [[raw-sources]] (immutable drop box), [[wiki]] (AI-built and maintained), [[schema-file]] (CLAUDE.md rules).
3. **Four use cases** that differ from the original gist:
   - **Stakeholder memory** — PMs building relationship context from meeting notes; wiki surfaces what has landed with a stakeholder and what objections are coming.
   - **Side project context** — weekend projects; the wiki maintains running context so Saturday morning you start in 5 minutes instead of 60.
   - **Team onboarding** — new employees read the wiki, get 80% of context that would take weeks to transfer. Surviving knowledge when senior employees leave.
   - **Solutions that stick** — debugging notes and technical reference; query before debugging so solutions surface without re-solving.
4. **Setup guides** — manual folder structure and skill-based approaches; recommendation to ingest one source at a time, not batches.
5. **30-day outlook** — 50-80 interconnected pages, compounding effects, contradictions surfaced automatically.

## Key quote

> "The best builders don't just know more. They forget less. This is the first system I've used that actually delivers on that."

## Contradictions with the original

Aakash's framing of use cases (especially stakeholder memory and side projects) extends Karpathy's original concept beyond personal research into work and team contexts. This suggests the pattern scales beyond solo knowledge management.

## Also covers

[[claude-managed-agents]] launch and its market impact, [[gemma-4]], [[claude-mythos-preview]], AutoAgent, Ariso file organization tool.
