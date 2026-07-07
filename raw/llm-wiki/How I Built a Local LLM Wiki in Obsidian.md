---
title: "How I Built a Local LLM Wiki in Obsidian"
source: "https://hackernoon.com/how-i-built-a-local-llm-wiki-in-obsidian"
author:
  - "[[ddfdfazsodifnadsoifn;aowinfsf]]"
published: 2026-05-07
created: 2026-07-07
description: "A look at how one Obsidian vault became a local LLM wiki maintained by Claude through ingest, query, audit, and close commands."
tags:
  - "clippings"
---
## Why Obsidian

[Obsidian](https://obsidian.md/?ref=hackernoon.com) is a note-taking app that stores everything as plain text markdown on your own machine. Think of it as a folder of Word documents that can link to each other.

I run two vaults in Obsidian. A personal vault for to-dos and journaling that nobody but me reads, and a homelab vault for project work and infrastructure notes. Claude only ever sees the second one. The wiki the rest of this post describes is the homelab vault.

I’ve been using Obsidian for a few years and never expected the format (plain markdown) would turn out to be the one LLMs read and write best. Eric Ma, a data scientist who also uses Obsidian, [makes the same point](https://ericmjl.github.io/blog/2026/3/6/mastering-personal-knowledge-management-with-obsidian-and-ai/?ref=hackernoon.com):

> *“When AI coding agents arrived, my vault was already in a format they could process natively. No migration needed.”* – Eric Ma

---

## What is an LLM Wiki

On April 2, 2026, Andrej Karpathy posted a [GitHub gist](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f?ref=hackernoon.com) where he described an “LLM Wiki”:

> “Instead of just retrieving from raw documents at query time, the LLM incrementally builds and maintains a persistent wiki - a structured, interlinked collection of markdown files that sits between you and the raw sources.”

The shift is from RAG to compilation. Most chatbots work via RAG (retrieval-augmented generation). RAG involves uploading files, and at query time the model searches for relevant fragments and rebuilds the answer from scraps every single time. An LLM Wiki flips that around. The model does the synthesis once, files it permanently, and queries become “look up the page that already exists” instead of “search and rebuild.”

The maintenance argument is the part that actually convinced me. Karpathy again:

> “Humans abandon wikis because the maintenance burden grows faster than the value. LLMs don’t get bored, don’t forget to update a cross-reference, and can touch 15 files in one pass.”

---

## My LLM Wiki Setup

The vault is a folder of markdown files on my Mac that syncs through Obsidian. It has three layers, in the Karpathy sense.

```
captures/    → Layer 1: Input    (immutable raw sources)
wiki/        → Layer 2: The Wiki (LLM-maintained projects, systems, runbooks, concepts)
CLAUDE.md    → Layer 3: Schema   (governs how the wiki operates)
```

**Sources** (`captures/`) Articles I’ve converted into clean markdown, podcast transcripts, screenshots, anything I want to remember. I never edit these once saved. They are the raw record.

**The wiki** (everywhere else) Project notes, system docs, runbooks, synthesis pages, and blog drafts. Claude writes most of this. I write headlines and direction.

**The schema** (`CLAUDE.md` plus a small library of skills and rules in `.claude/`) This is where I tell Claude how the vault is organized: where notes go, what frontmatter to use, how to handle freshness, when to ask before acting. It’s about 200 lines. I edit it when I notice Claude doing something I want to standardize.

```
vault/
  projects/    ← active project docs
  systems/     ← hosts and dated session logs
  runbooks/    ← repeatable procedures
  reference/
    captures/  ← raw web captures (immutable)
    concepts/  ← LLM synthesis pages
  blog/        ← drafts
  assets/      ← images
  CLAUDE.md    ← schema
```

---

## Karpathy’s “Three” Operations

### Ingest

**Ingest** is `/capture-url <url>` or `/research <topic>`. Capture pulls a single web page through `defuddle` (a CLI that strips ads and navigation), wraps the clean markdown in frontmatter, and files it under `captures/`. Research is the bigger move: three rounds of searching, up to fifteen captures, ending in a synthesis page that cites every source.

### Query

**Query** is whatever I ask Claude in a session. The vault is loaded as context automatically. The schema, memory index, and project dashboard are read at the start of every session, so I don’t have to re-explain the homelab every time we talk.

### Lint

**Lint** is `/audit`. A read-only health check that scans every note in the vault and flags problems: broken YAML, stale dates, broken `[[wikilinks]]`, orphan notes, projects whose status drifted out of sync with their ticket, and content past its last-verified date. I read the report and fix the noise; the rest stays.

### Close (my own addition)

A fourth one I added that Karpathy didn’t: `/close`. At the end of a session Claude updates the active project’s next-lookup field, writes a dated session log, and captures any feedback I gave it into LLM memory. This is the thing that actually keeps the vault current. Without it, the system half-works.

---

## Try It

The cheapest first move is to copy the [Karpathy gist](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f?ref=hackernoon.com) into a fresh folder, paste it into Claude Code, and let Claude scaffold a starter `CLAUDE.md` with you. You can modify it for your own setup from there.

---

## Resources

- Karpathy’s LLM Wiki gist: [github.com/karpathy/442a6bf555914893e9891c11519de94f](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f?ref=hackernoon.com)
- claude-obsidian by Agrici Daniel, packaged version of the pattern: [github.com/AgriciDaniel/claude-obsidian](https://github.com/AgriciDaniel/claude-obsidian?ref=hackernoon.com)
- obsidian-second-brain by Eugeniu Ghelbur, operations-heavy variant: [github.com/eugeniughelbur/obsidian-second-brain](https://github.com/eugeniughelbur/obsidian-second-brain?ref=hackernoon.com)
- Eric Ma’s PKM post: [ericmjl.github.io/blog/2026/3/6/…](https://ericmjl.github.io/blog/2026/3/6/mastering-personal-knowledge-management-with-obsidian-and-ai/?ref=hackernoon.com)
- Obsidian: [obsidian.md](https://obsidian.md/?ref=hackernoon.com)
- Claude Code: [claude.ai/code](https://claude.ai/code?ref=hackernoon.com)

---

## Proof of Usefulness

[Proof of Usefulness Hackathon](https://proofofusefulness.com/?ref=hackernoon.com) is a global 6-month developer challenge designed to reward real-world utility projects and initiatives. With 150,000+ in [cash prizes](https://proofofusefulness.com/cash-prizes?ref=hackernoon.com) and [software credits](https://proofofusefulness.com/software-prizes?ref=hackernoon.com) for winners and $1500+ worth of software and inventory for participants, this is undisputedly the biggest contest of the year. Learn more [here](https://proofofusefulness.com/?ref=hackernoon.com).

[![Player Zero](https://hackernoon.imgix.net/images/img-no63kax.jpeg?auto=format%2Ccompress&w=3840)](https://hs.playerzero.ai/multiplayer-ai-production-engineering?utm_campaign=46211499-27Q2ProofMultiplayer&utm_source=HackerNoon&utm_medium=banner&utm_content=AI3)