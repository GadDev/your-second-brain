---
description: Turn content into a new wiki page
argument-hint: <text or conversation content to capitalize>
---

$ARGUMENTS

Turn the content above into a new wiki page:

1. **Determine a title.** Short, precise, kebab-case filename (e.g. `attention-mechanism.md`).
2. **Write the page** in encyclopedic format: `# H1`, one-sentence summary, sections, `[[backlinks]]` to relevant existing pages.
3. **Create the file** in `wiki/` with required frontmatter (`type`, `tags`, `created`, `updated`).
4. **Update `wiki/index.md`** — add the new page under the appropriate `type` group.
5. **Append to `log.md`:** `## [YYYY-MM-DD] save | [[page-name]]`.
