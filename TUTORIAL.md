# Tutorial: Build a Second Brain with Claude Code

**Prerequisites:** Claude Code & Obsidian installed, an empty folder.

---

## Step 1 — Create the folder and open Claude Code

```bash
mkdir my-second-brain && cd my-second-brain
claude
```

---

## Step 2 — Copy Karpathy's original gist

Go to the gist he published in April 2026 and copy the full content:

👉 [gist.github.com/karpathy/442a6bf555914893e9891c11519de94f](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f)

This text describes the full pattern: `raw/` / `wiki/` / schema structure, ingest / lint / query workflows, the role of the log and the index. It's the conceptual contract that Claude will implement.

---

## Step 3 — Delegate to Claude Code

Paste the gist into Claude Code, followed by this prompt:

```
Based on the concept described above, initialize a second brain
in the current folder.

Create:
- raw/ (empty, for raw sources)
- wiki/ with an empty index.md
- empty log.md
- CLAUDE.md that captures this contract as rules for the agent
- .claude/commands/ with the four commands /ingest, /lint, /query
  and /save, whose content faithfully implements the concept described

Confirm the creation of each file.
```

Claude reads Karpathy's concept, understands the expected structure, and generates the files:

```
my-second-brain/
├── raw/
├── wiki/
│   └── index.md
├── log.md
├── CLAUDE.md
└── .claude/commands/
    ├── ingest.md
    ├── lint.md
    ├── query.md
    └── save.md
```

### What each command does

**`ingest.md`** — reads `raw/`, compiles wiki pages, moves processed files to `raw/processed/`:

```
---
description: Read a raw source and integrate it into the wiki
argument-hint: [path in raw/ or which source to process]
---

Read all files in `raw/` (ignore `raw/processed/`). If $ARGUMENTS specifies a file or pattern, process only those.

For each source:

1. **Identify** the key concepts, people, tools, and ideas.
2. **Create or enrich** the corresponding page in `wiki/` for each significant element. Use `type: source` for summaries of raw files; `type: entity` for people/orgs/tools; `type: concept` for ideas and themes.
3. **Weave `[[backlinks]]`** between related pages on first mention.
4. **Flag contradictions.** If two sources conflict, note both claims and their sources in the relevant article rather than overwriting.
5. **Move** each processed file to `raw/processed/`.

Once all sources are processed:

6. **Update `wiki/index.md`** — add new pages and refresh changed summaries, grouped by `type`.
7. **Append to `log.md`:** `## [YYYY-MM-DD] ingest | <N> files, <M> pages created/modified` followed by a bullet list of created/updated pages.
```

**`lint.md`** — health-checks the wiki and asks before applying fixes:

```
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

```

**`query.md`** — answers from the wiki only, cites sources, flags general knowledge:

```
---
description: Answer a question using the wiki as the knowledge source
argument-hint: <question>
---

$ARGUMENTS

Answer the question above using the content of the `wiki/` folder.

1. **Find relevant pages.** Read `wiki/index.md` first to locate candidates, then read the linked pages.
2. **Answer from the wiki.** Cite source pages in parentheses for each piece of information (e.g. `([[transformer]])`). If the answer is not in the wiki, say so clearly — do not fill in from general knowledge without explicitly flagging it as such.
3. **Suggest capitalizing.** If the answer has lasting value, suggest running `/save` on it to turn it into a wiki page.
```

**`save.md`** — turns any text or conversation answer into a wiki page:

```
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
```

> **Note on `$ARGUMENTS`:** in `query.md` and `save.md`, `$ARGUMENTS` captures everything you type after the slash command. Running `/query why doesn't RAG scale for personal use?` injects the question directly into the prompt.

The `/ingest` / `/lint` split is deliberate: one grows the brain, the other keeps it healthy.

---

## Step 4 — Open `wiki/` as a vault in Obsidian

Point Obsidian at the `wiki/` folder (not the repo root). As the wiki grows, the graph view shows the shape of your knowledge: which pages are hubs, which are orphans, how concepts cluster.

---

## Step 5 — Capture sources with Obsidian Web Clipper

[Obsidian Web Clipper](https://obsidian.md/clipper) is a Chrome extension that converts any web page into a local Markdown file — article text, metadata, and images saved to disk, readable offline.

Install it and point it at your `raw/` folder. When you find an article worth ingesting: one click, and it lands in `raw/` as a clean `.md` file ready for `/ingest`. No copy-pasting, no broken URLs.

---

## Step 6 — Drop a file into `raw/` and run `/ingest`

Add any source — an article clipped with Obsidian Web Clipper, a PDF, a transcript, your own notes — to `raw/` and run:

```
/ingest
```

Claude reads it, extracts concepts and entities, creates or enriches wiki pages, weaves `[[backlinks]]`, and moves the file to `raw/processed/`. A single source typically touches 10–15 pages. Check the result in Obsidian, then keep going.
