---
description: Export wiki pages to OKF format for sharing
argument-hint: [page-name or 'all' for full export]
---

Convert wiki pages to OKF v0.1 format:

1. **Target**: If $ARGUMENTS is 'all', convert entire wiki/
   Otherwise convert specified pages

2. **For each page**:
   - Extract H1 as title
   - Extract first paragraph as description
   - Convert updated → timestamp (ISO 8601)
   - Convert [[wikilinks]] → /wiki/page.md absolute paths
   - Keep all other frontmatter (extensions allowed by OKF)

3. **Output** to okf-export/ directory (gitignored)

4. **Create okf-export/index.md** listing all exported concepts

5. **Log**: "Exported N pages to OKF format in okf-export/"

Usage:
  /export-okf all              # Full export
  /export-okf llm-wiki-pattern # Single page