## [2026-07-07] ingest | 11 files, 26 pages created

**Sources processed:** all files in `raw/llm-wiki/` → moved to `raw/processed/`

**Concept pages created (10):**
- [[llm-wiki-pattern]] — the central concept
- [[rag]] — retrieval-augmented generation and its limitations
- [[compounding-knowledge]] — how wiki value accumulates over time
- [[second-brain]] — Forte's concept and its LLM-era evolution
- [[pkm]] — personal knowledge management field overview
- [[para-method]] — Projects, Areas, Resources, Archives
- [[ai-first-vault-principle]] — Ghelbur's controversial extension
- [[vibe-coding]] — Karpathy's term for AI-driven development
- [[schema-file]] — the CLAUDE.md / AGENTS.md pattern
- [[zettelkasten]] — the note-linking ancestor

**Entity pages created (10):**
- [[andrej-karpathy]] — originator of the LLM Wiki pattern
- [[tiago-forte]] — second brain / PARA author
- [[eugeniu-ghelbur]] — obsidian-second-brain author
- [[agrici-daniel]] — claude-obsidian author
- [[eric-j-ma]] — professional PKM case study
- [[obsidian]] — the note-taking app / graph viewer
- [[claude-code]] — the agent runtime
- [[obsidian-web-clipper]] — the capture browser extension
- [[obsidian-second-brain]] — Ghelbur's tool
- [[claude-obsidian]] — Daniel's tool

**Source pages created (11):**
- [[source-llm-wiki-gist]], [[source-karpathys-instructions]], [[source-build-ai-second-brain-tahir]]
- [[source-forte-interview]], [[source-local-llm-wiki-hackernoon]], [[source-aimaker-wyndo]]
- [[source-i-built-this-ghelbur]], [[source-i-rebuilt-karpathy-ghelbur]]
- [[source-pkm-obsidian-eric-ma]], [[source-obsidian-ai-plugin-daniel]], [[source-para-method]]

**Contradictions flagged:**
- `raw/` immutability: original Karpathy gist and most implementations treat `raw/` as strictly immutable; this wiki's CLAUDE.md allows moving to `raw/processed/`. See [[llm-wiki-pattern]].
- Append-only vs. rewrite: Karpathy original is append-only; Ghelbur argues this fails at scale and proposes rewriting. See [[compounding-knowledge]], [[obsidian-second-brain]].
- Human-readable vs. AI-first notes: original pattern writes for humans; Ghelbur's [[ai-first-vault-principle]] writes for LLMs. See [[ai-first-vault-principle]].
