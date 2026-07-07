---
type: entity
tags: [tool, obsidian, capture]
created: 2026-07-07
updated: 2026-07-07
aliases: [Web Clipper, Obsidian Clipper]
---

# Obsidian Web Clipper

A browser extension (Chrome and others) by the [[obsidian]] team that converts web pages to local Markdown files and saves them directly into a vault.

## What it does

One click on any web article captures: clean article text, metadata (title, author, source URL, date), and optionally images. The output is a `.md` file saved to a chosen folder in the vault — typically `raw/` in the [[llm-wiki-pattern]] workflow.

## Why it matters for LLM wikis

Web Clipper is the primary intake mechanism for the [[llm-wiki-pattern]]. Rather than manually copying/pasting web content, one click produces a clean, LLM-readable markdown file ready for `/ingest`. Reduces friction in the capture-to-wiki pipeline dramatically.

> "Obsidian Web Clipper is a browser extension that converts web articles to markdown. Very useful for quickly getting sources into your raw collection." — [[andrej-karpathy]]'s gist

Also works on YouTube pages, saving the full transcript alongside the video metadata.

## Image handling tip

In Obsidian Settings → Files and links, set "Attachment folder path" to `raw/assets/`. Then bind "Download attachments for current file" to a hotkey (e.g., Ctrl+Shift+D). After clipping, hit the hotkey to download all referenced images locally — useful for LLM image analysis, since LLMs can't read markdown with inline images in one pass (text first, then images separately).

## Related

[[obsidian]] · [[llm-wiki-pattern]] · [[claude-code]]
