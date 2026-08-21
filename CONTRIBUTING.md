# Contributing to LLM Wiki — Second Brain Scaffold

Thanks for your interest in improving this scaffold. This is a small, opinionated
project — a few guidelines keep contributions easy to review and merge.

## What this project is (and isn't)

This repo is a **scaffold**: the schema, slash commands, and folder conventions that
let an LLM agent build and maintain a personal wiki. It is not itself a wiki — `raw/`
and `wiki/` are meant to stay empty (or example-only) in the repo itself, since real
content belongs to whoever adopts the scaffold.

Good contributions generally fall into one of these buckets:

- Improvements to `CLAUDE.md` — the schema contract (naming conventions, page
  format, linking rules, frontmatter fields)
- New or improved slash commands in `.claude/commands/`
- Documentation improvements (README, this file, workshop materials)
- Bug fixes to any tooling/scripts in the repo

## Before you start

For anything beyond a small fix (typo, broken link), please open an issue first to
discuss the change. This avoids duplicated work and lets us agree on approach before
you invest time.

## Making a change

1. Fork the repo and create a branch from `main`.
2. Make your change. If you're editing `CLAUDE.md`, keep the schema minimal and
   explain any new field or convention with a short comment or example.
3. If you add or change a slash command in `.claude/commands/`, test it against a
   sample `raw/` source end-to-end (ingest → wiki page → query) before submitting.
4. Update `README.md` if your change affects setup, the four commands, or the
   folder structure.
5. Commit with a clear message describing the change and why.
6. Open a pull request. Describe what changed and, if relevant, how you tested it.

## Style

- Keep `CLAUDE.md` prose plain and unambiguous — it's read by an LLM as a contract,
  not by humans as narrative documentation.
- Prefer small, focused PRs over large ones covering multiple unrelated changes.
- No secrets, API keys, or real personal notes in example content — use clearly
  fictional or placeholder material.

## Reporting issues

Open a GitHub issue with:
- What you expected to happen
- What actually happened
- Steps to reproduce (which command, what kind of source file, etc.)

## Code of Conduct

This project follows the [Code of Conduct](./CODE_OF_CONDUCT.md). By participating,
you're expected to uphold it.
