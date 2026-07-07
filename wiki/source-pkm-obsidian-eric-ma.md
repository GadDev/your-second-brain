---
type: source
tags: [pkm, obsidian, eric-j-ma, professional-use]
created: 2026-07-07
updated: 2026-07-07
source: "raw/llm-wiki/Mastering Personal Knowledge Management with Obsidian and AI.md"
---

# Mastering Personal Knowledge Management with Obsidian and AI (Eric J. Ma's Blog)

Detailed first-person account by [[eric-j-ma]] (March 6, 2026) of using [[obsidian]] and AI coding agents for professional [[pkm]] while managing 12 people across two teams.

## Key metrics

- PKM overhead reduced from 30-40% of work time to under 10%.
- Hallucinations rare: ~1 per 4-5 "sweeps," usually from inaccurate transcripts, not agent errors.

## Technical ingestion approach

Unusual for its breadth of source types:
- Word docs → `python-docx`
- PowerPoints → dual path: XML extraction (`python-pptx`) + image captioning via vision-language model (`libreoffice` + `PIL`)
- Excel → `openpyxl` (not pandas — handles messy real-world structure; progressive reveal: architecture first, then relevant cells)
- PDFs → text extraction for normal, image captioning for scanned
- All scripts use PEP 723 inline script metadata with `uv run` (no venv management)

## Professional ethics note

Maintains "dossiers" on colleagues (people notes) but only captures professional details; does not record personal details without consent.

## Output production

Confluence, GitHub Gists, HTML presentations, Jira tickets — all generated from markdown by AI agents. "We firmly believe that humans shouldn't be filling forms out; AI should be filling forms for us."

## Key quote on plain text

> "When AI coding agents arrived, my vault was already in a format they could process natively. No migration needed."
