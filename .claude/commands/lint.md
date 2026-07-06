---
description: Health-check the wiki for structural and content problems
argument-hint: [optional area or page to focus on]
---

Review the entire `wiki/` folder and produce a structured report. If $ARGUMENTS specifies a page or area, focus there.

## Checks

1. **Contradictions** — passages that conflict between two different articles.
2. **Orphan pages** — articles with no incoming `[[backlinks]]` from any other page (excluding `index.md`).
3. **Broken links** — `[[PageName]]` references pointing to a non-existent page or undeclared alias.
4. **Stale index** — entries in `index.md` missing from `wiki/`, pointing to deleted pages, or with outdated summaries.
5. **Concepts without pages** — terms recurring across multiple articles that warrant their own page.

## Output

For each problem: indicate the file, describe the issue, propose a fix.

Group findings as:
- **Structural** (broken links, orphans, stale index) — safe to auto-apply; offer to fix in one pass.
- **Content** (contradictions, missing concept pages) — present findings and proposed fixes, then ask for confirmation before applying any changes.

Append `## [YYYY-MM-DD] lint | <one-line summary>` to `log.md` after the report.
