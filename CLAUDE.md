# CLAUDE.md — Wiki Schema

This vault is a personal, encyclopedic wiki on transmission spectroscopy of exoplanet atmospheres. You (the LLM) are its maintainer. The human curates sources and asks questions; you do all writing.

**You own:** `wiki/`, `index.md`, `log.md`, `analyses/`.
**You must not modify:** `raw/` (immutable source PDFs), `CLAUDE.md` (propose edits; don't silently rewrite), `docs/` (design artifacts).

## Architecture

```
raw/papers/               # source PDFs, filename = <bibkey>.pdf
wiki/
  targets/                # planets + host stars
  instruments/            # facilities, spectrographs, missions
  methods/                # computational procedures (retrievals, detrending, modeling)
  species/                # chemical species (formula as filename)
  concepts/               # physical quantities & phenomena
  papers/                 # one summary page per ingested paper
  codes/                  # software / pipelines
  programs/               # observing programs, surveys, data releases
analyses/                 # time-stamped query outputs worth keeping
index.md                  # catalog of all wiki pages (you maintain)
log.md                    # append-only chronological record (you maintain)
```

## Entity category adjudication

When an entity could fit multiple categories, follow these rules in order:

1. **Physical observable** (a measurable quantity) → `concepts/`. E.g. transit depth, scale height.
2. **Computational procedure** (how the answer is derived) → `methods/`. E.g. atmospheric retrievals, GP detrending.
3. **Software implementation** (a specific codebase) → `codes/`. E.g. petitRADTRANS, Eureka.
4. **Chemical entity** → `species/`. E.g. SO2 — even when the paper emphasizes its photochemistry.
5. **Observing facility or mode** → `instruments/`. E.g. JWST-NIRSpec, HST-WFC3.

If still ambiguous, the page lives in the category most frequently linked from; adjacent categories may get a short `## See also` stub pointing to it. Never duplicate content across categories.

## Filename conventions

- Planet: `<designation>.md`, e.g. `WASP-39b.md`, `TRAPPIST-1e.md`.
- Star: `<star>.md` with no suffix, e.g. `WASP-39.md`.
- Instrument: `<facility>-<mode>.md` where useful, e.g. `JWST-NIRSpec.md`.
- Method: descriptive phrase, e.g. `atmospheric-retrievals.md`, `gaussian-process-detrending.md`.
- Species: chemical formula, e.g. `H2O.md`, `CO2.md`, `SO2.md`.
- Concept: descriptive phrase, e.g. `transit-depth.md`, `C-O-ratio.md`.
- Paper: `<year>_<first-author>_<shortslug>.md` = the bibkey, e.g. `2022_Rustamkulov_WASP39b.md`.
- Code: tool name, e.g. `petitRADTRANS.md`, `Eureka.md`.
- Program: short designation, e.g. `JWST-ERS-TransitingExoplanets.md`.
- Analysis: `<YYYY-MM-DD>_<slug>.md`, e.g. `2026-04-22_WASP39b-vs-WASP96b-comparison.md`.

## Frontmatter

Only `type:` is strictly required everywhere.

### Paper pages — rich frontmatter

```yaml
---
type: paper
bibkey: 2022_Rustamkulov_WASP39b
authors: [Rustamkulov, Z., Sing, D. K., et al.]
year: 2022
venue: Nature
arxiv: 2211.10487
doi: 10.1038/s41586-022-05677-y
targets: [WASP-39b]
instruments: [JWST-NIRSpec]
methods: [atmospheric-retrievals, transit-spectroscopy]
species_detected: [H2O, CO2, SO2, Na]
tags: [hot-jupiter, jwst-ers]
ingested: 2026-04-22
---
```

### Target pages — rich frontmatter

```yaml
---
type: target
kind: planet                # planet | star
host_star: WASP-39          # omit for stars
mass_mjup: 0.28
radius_rjup: 1.27
period_days: 4.055
teq_k: 1166
discovery_year: 2011
tags: [hot-jupiter, inflated]
---
```

For stars: use `kind: star`, drop `host_star`, and use `mass_msun`, `radius_rsun`, `teff_k`, `feh_dex` in place of the planetary properties.

### All other types — minimal frontmatter

```yaml
---
type: method       # or instrument | species | concept | code | program
aliases: [alt-name-1, alt-name-2]
tags: [retrieval, bayesian]
---
```

### Analyses

```yaml
---
type: analysis
date: 2026-04-22
question: "How do WASP-39b and WASP-96b H2O abundances compare?"
sources: [2022_Rustamkulov_WASP39b, 2023_Nikolov_WASP96b]
tags: [comparison, hot-jupiter, h2o]
---
```

## Page templates

### Paper

```markdown
# <Title>

**Authors:** <short author list> (<year>, <venue>) · [arXiv:<id>]
**Targets:** [[<target>]] · **Instrument:** [[<instrument>]]

## TL;DR
One-paragraph distillation: what was done, what was found, why it matters.

## Key findings
- Each bullet links to the relevant entity page(s).

## Methods
Prose summary; link to [[<method>]] pages.

## Caveats & limitations
Author-flagged caveats plus any concerns worth noting.

## Open questions / follow-ups
Questions the paper raises for future work.

## Related
Links to other papers on the same target or method.
```

### Target (stub)

```markdown
# <Target>

One-sentence placement in context (type, host, first characterization).

## See also
- Papers: [[<bibkey>]], ...
- Host: [[<star>]]
```

### Target (hub, promoted from stub)

```markdown
# <Target>

One-paragraph lede.

## Basic properties
From frontmatter + prose.

## Atmospheric composition
One bullet per detected species, linking to both the species page and the detecting paper.

## Observations to date
Chronological: instrument, program, paper.

## Open questions
Tensions flagged elsewhere in the wiki.

## Papers
All papers on this target, grouped by era or instrument.
```

### Other stubs (method / concept / species / code / instrument / program)

```markdown
# <Name>

One-sentence definition.

Short paragraph with essentials, linking to related entity pages.

## Papers
- [[<bibkey_1>]] — one-line relevance note
- [[<bibkey_2>]] — ...
```

Hubs of these types gain sections like `## Variants`, `## History`, `## Trade-offs`, `## Open issues` as appropriate.

## Citation style

- Every factual claim in `wiki/` must trace back to a paper via a `[[wiki/papers/<bibkey>]]` link.
- Inline style: `SO2 was detected in WASP-39b's atmosphere at >3σ ([[2022_Rustamkulov_WASP39b]]).`
- Never cite a paper that does not have a page in `wiki/papers/`. The link chain must resolve.

## Operations

You handle three canonical operations.

### Ingest — triggered by the user dropping a PDF into `raw/papers/` and asking you to ingest it

1. Confirm the PDF exists; read the full text.
2. Extract: authors, year, venue (journal or arXiv id), targets, instruments, methods, species, key results, caveats, open questions. Propose a bibkey (`<year>_<first-author>_<shortslug>`).
3. **Pause.** Present a ~10-line bulleted summary to the user. Ask if the emphasis is right. Accept corrections before writing anything.
4. Rename the PDF to `<bibkey>.pdf` if it isn't already.
5. Create `wiki/papers/<bibkey>.md` from the paper template.
6. For each referenced entity, create a stub if missing or update the existing page. Stubs get a stub template; hub pages get a new bullet or section, not a rewrite.
7. Append the page to `index.md` under the right category.
8. Append an entry to `log.md`: `## [YYYY-MM-DD] ingest | <bibkey>` plus the created/updated page list.
9. Report back: pages created, pages modified, any contradictions detected.

### Query — triggered by the user asking a question

1. Read `index.md` first to find candidate pages.
2. Read the candidate pages.
3. Synthesize an answer with inline `[[wiki-link]]` citations. Citations ultimately resolve to `wiki/papers/<bibkey>`.
4. If the answer is non-trivial, offer to file it to `analyses/<YYYY-MM-DD>_<slug>.md` and update `index.md` + `log.md`.
5. Never invent facts. If the wiki is silent on the topic, say so and name the kind of source that would fill the gap.

### Lint — triggered by the user asking you to lint the wiki

1. Scan for:
   1. **Orphans** — pages with zero inbound links (excluding `index.md` and `log.md`).
   2. **Over-referenced stubs** — stubs past the promotion threshold (see "Stub promotion" below).
   3. **Frontmatter violations** — missing `type:`, unknown `type:` values, malformed YAML.
   4. **Broken wiki-links** — `[[x]]` where `x` does not resolve.
   5. **Index/filesystem sync** — pages in `wiki/` not listed in `index.md`, or listed but missing on disk.
   6. **Unflagged contradictions** — sample a few hub pages and spot-check claims against their cited papers.
   7. **Tag hygiene** — singleton tags (likely typos), over-broad tags (too generic to be useful).
2. **Report only** — produce a numbered findings list. Wait for user approval per-item before fixing anything.
3. Append a `log.md` entry: `## [date] lint | <type>` with the finding counts.

## Edge cases

### Contradictions

When ingestion reveals a claim that conflicts with existing wiki prose:
- Add (or extend) a `## Tensions` subsection on the affected entity page. One bullet per tension: the two claims, the two sources, and a driver-of-the-difference note if known.
- Never silently merge or pick a winner.
- `log.md` gets: `**Tension flagged:** [[entity]] — claim A ([[paperA]]) vs claim B ([[paperB]])`.
- On hub pages, the `## Open questions` section surfaces unresolved tensions.

### Naming collisions and aliases

- One canonical page per entity; the most commonly cited name in the literature.
- Alternative names go in `aliases:` frontmatter.
- `index.md` may list aliases inline for discoverability.
- No redirect stubs for pure aliases — they live only in frontmatter.

### Stub promotion

- **Threshold:** ≥5 inbound links from pages in `wiki/` (exclude `index.md` and `log.md` — they link to everything) **OR** ≥3 papers in `wiki/papers/` reference the entity.
- **Never automatic.** During lint, list candidates. The user approves each.
- On promotion, read every paper in `wiki/papers/` that links to the entity and write the hub page using the hub template.

### Stale claims

- A new paper contradicting existing prose → tension entry, not silent rewrite.
- Hub pages maintain chronology (`## Observations to date`, `## History`) so supersessions are visible.
- Concept/method ledes may be updated in place when the newer understanding is clearly correct; log the change and add a one-line impact note on the superseding paper's page.

### Broken links

When you write a `[[link]]` to a non-existent page, create the stub immediately using the stub template. Broken links that appear later (e.g., after a rename) become lint findings, not silent drops.

## Hard rules

**MUST:**
- Maintain `index.md` and `log.md` on every state-changing operation.
- Respect the category adjudication rules above.
- Cite via `[[wiki-links]]`; never inline prose references.
- Create a stub for any `[[link]]` target that does not exist yet.

**MUST NOT:**
- Modify files in `raw/`.
- Invent facts. Every claim in `wiki/` must trace to a paper page.
- Delete pages without explicit user confirmation.
- Batch-ingest multiple papers unless explicitly asked ("ingest all PDFs in raw/papers/").
- Silently merge contradictions — they surface as `## Tensions` entries.

## `index.md` conventions

Structure: one section per entity category plus an `Analyses` section. Format per entry:

```markdown
- [[page-name]] — short description · <N> papers
```

- Hub pages get `(hub)` after the page name.
- `Papers` and `Analyses`: newest first. Other sections: alphabetical.
- Species entries may compress to inline lists until any species has ≥3 papers, then split to per-line.
- Category headers include a running page count `(N)`.
- Header line: `*Last updated: <YYYY-MM-DD>. Maintained by the LLM — do not edit by hand except to flag errors.*`

When `index.md` passes ~400 lines, propose splitting it into `index/<category>.md` files (not before — premature splitting adds complexity).

## `log.md` conventions

Append-only, grep-friendly.

**Event kinds:** `ingest`, `query`, `lint`, `schema`, `note`.

**Format:** one `## [YYYY-MM-DD] <kind> | <short-subject>` header per event, followed by free-form body lines with `**Bold:**` prefixes for structured fields.

**Examples** (canonical; reuse verbatim):

```markdown
## [2026-04-22] ingest | 2022_Rustamkulov_WASP39b
**Paper:** Rustamkulov et al. 2022, Nature — WASP-39b JWST/NIRSpec transmission
**Created:** wiki/papers/2022_Rustamkulov_WASP39b.md, wiki/targets/WASP-39b.md (stub), wiki/instruments/JWST-NIRSpec.md (stub), wiki/species/SO2.md (stub)
**Updated:** wiki/species/H2O.md (added paper ref), index.md

## [2026-04-22] query | "how does SO2 form in hot-Jupiter atmospheres?"
**Answer filed as:** analyses/2026-04-22_SO2-photochemistry-hot-jupiters.md
**Sources consulted:** 2022_Tsai_WASP39b_photochem, 2023_Polman_SO2

## [2026-04-22] lint | full-pass
**Findings:** 3 orphan stubs, 1 contradiction flagged (metallicity on WASP-39b), 2 pages with broken links
**Actions:** none — pending user review

## [2026-04-22] schema | loosened frontmatter requirements on species pages
**Reason:** ingestion was stalling on unknown abundance values; made abundance_ppm optional
```

**Rules:** append only. Never rewrite past entries. Corrections become new entries.

## Schema evolution

If a rule in this file feels wrong or incomplete during an operation (e.g., the promotion threshold is consistently too low after 50 ingests), propose a schema edit rather than silently working around it. Discuss the edit with the user, apply it, and log the change with `## [date] schema | <change>` and a reason line. Do not retroactively migrate pages written under the older schema — this file is the contract for new work.
