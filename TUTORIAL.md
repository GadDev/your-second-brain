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
Read all files in the `raw/` folder (ignore `raw/processed/`).

For each source:
1. Identify the key concepts, people, tools and ideas
2. For each significant element: create or enrich the corresponding page in wiki/
3. Weave [[PageName]] backlinks between related pages
4. If two sources contradict each other, note the contradiction in the relevant article
5. Move processed files to raw/processed/

Once all sources are processed:
- Update wiki/index.md with new and modified pages
- Add an entry to log.md: date, number of files ingested, pages created/modified
```

**`lint.md`** — health-checks the wiki and asks before applying fixes:

```
Review the entire wiki/ folder and produce a structured report.

Check for:
1. Contradictions: passages that conflict between two different articles
2. Orphan pages: articles with no incoming backlinks from any other page
3. Broken links: [[PageName]] backlinks pointing to a non-existent page
4. Stale index: entries in index.md that are missing or point to deleted pages
5. Concepts without pages: recurring terms across multiple articles that deserve their own page

For each problem: indicate the file, describe the issue, propose a fix.
Ask for confirmation before applying any corrections.
```

**`query.md`** — answers from the wiki only, cites sources, flags general knowledge:

```
$ARGUMENTS

Answer the question above using the content of the wiki/ folder.
Cite source pages in parentheses for each piece of information.
If the answer is not in the wiki, say so clearly: do not fill in from your general
knowledge without explicitly flagging it.
```

**`save.md`** — turns any text or conversation answer into a wiki page:

```
$ARGUMENTS

Turn the content above into a new wiki page:
1. Determine a short, precise title
2. Write the page in encyclopedic format (H1, summary, sections, [[]] backlinks)
3. Create the file in wiki/ with backlinks to relevant existing pages
4. Update wiki/index.md
5. Add an entry to log.md
```

> **Note on `$ARGUMENTS`:** in `query.md` and `save.md`, `$ARGUMENTS` captures everything you type after the slash command. Running `/query why doesn't RAG scale for personal use?` injects the question directly into the prompt.

The `/ingest` / `/lint` split is deliberate: one grows the brain, the other keeps it healthy.

---

## Step 4 — Open `wiki/` as a vault in Obsidian

Point Obsidian at the `wiki/` folder (not the repo root). As the wiki grows, the graph view shows the shape of your knowledge: which pages are hubs, which are orphans, how concepts cluster.

---

## Step 5 — Drop a file into `raw/` and run `/ingest`

Add any source — an article, a PDF, a transcript, your own notes — to `raw/` and run:

```
/ingest
```

Claude reads it, extracts concepts and entities, creates or enriches wiki pages, weaves `[[backlinks]]`, and moves the file to `raw/processed/`. A single source typically touches 10–15 pages. Check the result in Obsidian, then keep going.
