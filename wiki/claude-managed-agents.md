---
type: entity
tags: [tool, anthropic, agent-orchestration]
created: 2026-07-07
updated: 2026-07-07
aliases: [Managed Agents, Claude Agents]
---

# Claude Managed Agents

Anthropic's hosted agent orchestration platform, launched in public beta April 8, 2026. Handles sandboxed execution, state management, credential handling, and error recovery for AI agents at scale.

## Key capabilities

- Define agent behavior and tools; Anthropic manages the rest
- Production infrastructure for multi-agent fleets
- Structured file generation success rates improved ~10 points over standard prompting (internal testing)
- Pricing: $0.08 per agent runtime hour (on top of model usage)
- MCP (Model Context Protocol) connected to services like HubSpot, Slack, Notion

## Impact

Described by [[aakash-gupta]] as "Anthropic just mass-obsoleted every agent orchestration startup in a single launch." Early adopters include Notion, Rakuten, and Asana.

The platform absorbs the entire orchestration layer previously handled by startups, custom harnesses, or frameworks like LangChain. What used to take months of infrastructure work now takes days.

## Market dynamics

This move eliminated the moat for infrastructure-play startups (LangChain, Manus) that built on top of the infrastructure gap. Companies that survive have proprietary data, workflows, or distribution advantages.

## Related

[[anthropic]] · [[claude-code]] · [[llm-wiki-pattern]]
