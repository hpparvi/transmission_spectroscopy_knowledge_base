# Transmission Spectroscopy Wiki

A personal, LLM-maintained encyclopedic reference on transmission spectroscopy of exoplanet atmospheres.

## How to use this vault

- **Sources** live in `raw/papers/` as PDFs. Don't edit them — they're the source of truth.
- **Reference material** lives in `wiki/`, organized by entity type (targets, instruments, methods, species, concepts, papers, codes, programs).
- **The catalog** is `index.md` — your starting point for browsing.
- **The log** is `log.md` — chronological record of what's been ingested, asked, and lint-checked.
- **Analyses** (LLM-generated answers to your questions) accumulate in `analyses/` when worth keeping.

## Workflow

1. Drop a new paper PDF into `raw/papers/` and ask the LLM to ingest it.
2. Ask the LLM questions; file interesting answers into `analyses/`.
3. Periodically ask the LLM to lint the wiki.

All writes are done by the LLM. You curate sources, direct the analysis, and review the results.

## The rules

The LLM's contract with this vault is `CLAUDE.md`. If behavior drifts, that's the file to edit.

## Design docs

- Spec: `docs/superpowers/specs/2026-04-22-llm-wiki-design.md`
- Plan: `docs/superpowers/plans/2026-04-22-llm-wiki-scaffold.md`
