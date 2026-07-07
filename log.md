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

---

## [2026-07-07] ingest | 1 file, 5 pages created/updated

**Source processed:** "The Complete Guide to Karpathy's Second Brain" by Aakash Gupta → moved to `raw/processed/`

**Concept pages created (2):**
- [[raw-sources]] — the immutable input layer
- [[wiki]] — the LLM-owned output layer

**Entity pages created (2):**
- [[aakash-gupta]] — AI analyst and writer
- [[claude-managed-agents]] — Anthropic's agent orchestration platform

**Source pages created (1):**
- [[source-complete-guide-aakash]] — comprehensive applied guide with four use cases

**Pages updated:**
- [[llm-wiki-pattern]] — now explicitly distinguishes raw/wiki/schema layers
- [[compounding-knowledge]] — Aakash's 30-day outlook provides concrete examples

**New insights:**
- Four concrete use cases beyond research: stakeholder memory (PMs), side projects, team onboarding, solutions that stick
- Recommendation reinforced: ingest one source at a time, not batches; guides better LLM emphasis
- Validation that the pattern works at 50-80 pages within 30 days
