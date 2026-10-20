# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Type

This is an **Obsidian vault + Claude Code plugin** package. It has no build step, no compiled code, and no runtime dependencies. It is markdown-only.

## Vault Conventions

- `.raw/` — source documents. **Never modify.** Read-only.
- `wiki/` — agent-generated knowledge base. You own this directory.
- `wiki/hot.md` — recent context cache (~500 words). Read first at session start, overwrite at session end.
- `wiki/index.md` — master catalog of all wiki pages.
- `wiki/log.md` — append-only operation log. New entries go at the **top**.
- `wiki/meta/` — dashboards, lint reports, conventions.
- `_templates/` — Obsidian Templater templates for note frontmatter.
- `_attachments/` — images and PDFs referenced by wiki pages.
- `.raw/.manifest.json` — delta tracking for incremental ingest.

Every wiki page uses flat YAML frontmatter (`type`, `status`, `created`, `updated`, `tags`). Use wikilinks `[[Page Name]]`, not Markdown paths.

## PDF Ingestion Notes

User-provided course/transcript PDFs are usually text-based PDFs, not scans. Do not start with OCR for these files.

Preferred extraction path on Windows:

```bash
PYTHONIOENCODING=utf-8 python -c "
import pdfplumber, sys
sys.stdout.reconfigure(encoding='utf-8')
pdf = pdfplumber.open(r'PATH_TO_PDF')
print(f'Pages: {len(pdf.pages)}')
for page in pdf.pages:
    text = page.extract_text()
    if text:
        print(text)
        print('---PAGE_BREAK---')
pdf.close()
"
```

Operational lessons:

- Use `pdfplumber` or `pymupdf`/`fitz` for text PDFs. `PyPDF2` may be absent, and `Read` may fail if `pdftoppm` is unavailable.
- Always force UTF-8 output with `PYTHONIOENCODING=utf-8` and `sys.stdout.reconfigure(encoding='utf-8')`; otherwise Windows GBK stdout can crash on CJK compatibility glyphs.
- If output is large, redirect to a temp text file and read it in chunks instead of printing everything into the conversation.
- Only consider OCR when text extraction returns empty or near-empty pages.
- Preserve the original PDF as immutable source under `.raw/pdfs/`; write synthesized pages only under `wiki/`.

## Skills Architecture

All 10 skills live in `skills/<name>/SKILL.md` using the cross-platform Agent Skills spec (frontmatter `name` + `description`).

| Skill | Trigger | Purpose |
|-------|---------|---------|
| `wiki` | `/wiki` | Orchestrator: scaffold, hot cache, route to sub-skills |
| `wiki-ingest` | `ingest [file/URL/image]` | Read source, create 8-15 wiki pages with cross-references |
| `wiki-query` | `what do you know about X`, `query quick:`, `query deep:` | Answer from wiki with 3 depth modes |
| `wiki-lint` | `lint the wiki`, `health check` | 8-category health check: orphans, dead links, stale claims, gaps |
| `wiki-fold` | `fold the log`, `log rollup` | DragonScale Mechanism 1: log compaction |
| `save` | `/save` | File current conversation as a structured wiki note |
| `autoresearch` | `/autoresearch [topic]` | Autonomous research loop: search, fetch, synthesize, file (configurable via `skills/autoresearch/references/program.md`) |
| `canvas` | `/canvas` | Create/edit Obsidian canvas files (visual knowledge graphs) |
| `defuddle` | `clean this url`, `defuddle` | Strip web page noise before ingest (saves 40-60% tokens) |
| `obsidian-markdown` | `obsidian syntax`, `wikilink` | Obsidian Flavored Markdown reference |
| `obsidian-bases` | `obsidian bases`, `.base file` | Native database views (Obsidian v1.9.10+) |

## Hooks (Auto-automation)

`hooks/hooks.json` defines lifecycle hooks:

- **SessionStart** — Reads `wiki/hot.md` to restore recent context silently.
- **PostCompact** — Re-reads `hot.md` after context compaction (cache survives compaction).
- **PostToolUse** (Write/Edit) — Auto-commits wiki changes to git every 15 minutes.
- **Stop** — Prompts hot cache update when wiki pages changed this session.

## Scripts & Tooling

| Script | Path | Purpose |
|--------|------|---------|
| `setup-vault.sh` | `bin/` | Full vault setup: config, CSS snippets, Excalidraw download |
| `setup-multi-agent.sh` | `bin/` | Symlink skills for Codex / OpenCode / Gemini CLI |
| `setup-dragonscale.sh` | `bin/` | Install DragonScale memory extension |
| `allocate-address.sh` | `scripts/` | Deterministic page address allocation |
| `tiling-check.py` | `scripts/` | Semantic tiling validation |
| `boundary-score.py` | `scripts/` | Boundary-first autoresearch scoring |

## Testing

```bash
make test               # Run all 3 tests (address, tiling, boundary)
make test-address       # Shell script test
make test-tiling        # Python test (no ollama required)
make test-boundary      # Python test (no prereqs)
make clean-test-state   # Remove runtime lockfiles and tiling cache
```

Tests live in `tests/`. No test framework — plain shell scripts and Python scripts.

## DragonScale Memory (Optional Extension)

Documented in `docs/dragonscale-guide.md`. Adds:
- Log folds (Mechanism 1: log compaction via `wiki-fold` skill)
- Deterministic page addresses (no random file naming)
- Semantic tiling lint (`tiling-check.py`)
- Boundary-first autoresearch (`boundary-score.py`)
- Runtime state in `.vault-meta/` (locks, tiling cache)

## Cross-Platform Agent Support

Skills work with any Agent Skills compatible agent:
- **Claude Code** — primary target
- **Codex CLI** — symlink skills to `~/.codex/skills/`
- **OpenCode** — symlink skills to `~/.opencode/skills/`
- **Gemini CLI / Antigravity** — symlink skills to `~/.gemini/skills/`

See `GEMINI.md` and `bin/setup-multi-agent.sh`.

## Other AI Agent Instructions

- `.github/copilot-instructions.md` — GitHub Copilot conventions (wikilinks, flat frontmatter, `.raw/` immutability)

## Key Files for Development

- `skills/wiki/SKILL.md` — orchestrator skill (most complex, ~300 lines)
- `WIKI.md` — full schema reference (13 sections, 850+ lines)
- `AGENTS.md` — bootstrap instructions for first-run setup
- `hooks/hooks.json` — automation hooks
- `.claude-plugin/plugin.json` — Claude Code plugin manifest
- `.claude-plugin/marketplace.json` — marketplace distribution metadata
