# Log

## [2026-04-22] schema | initial vault setup
**Created:** CLAUDE.md, README.md, index.md, log.md, and directory structure (raw/papers/, wiki/{targets,instruments,methods,species,concepts,papers,codes,programs}/, analyses/)
**Reason:** initial scaffold per docs/superpowers/specs/2026-04-22-llm-wiki-design.md
**Status:** ready for first ingest

## [2026-04-22] ingest | 2023_May_GJ1132b
**Paper:** May, MacDonald, Bennett et al. 2023, ApJL 959:L9 — "Double Trouble: Two Transits of the Super-Earth GJ 1132 b Observed with JWST NIRSpec G395H" (doi:10.3847/2041-8213/ad054f)
**PDF renamed:** raw/papers/2023_May_GJ1132b.pdf
**Created:** wiki/papers/2023_May_GJ1132b.md, wiki/targets/GJ1132b.md (stub), wiki/targets/GJ1132.md (stub), wiki/instruments/JWST-NIRSpec.md (stub), wiki/methods/{transmission-spectroscopy,atmospheric-retrievals,stellar-contamination-modeling}.md (stubs), wiki/species/{H2O,CH4,N2O,CO2}.md (stubs), wiki/codes/{Eureka,POSEIDON}.md (stubs), wiki/programs/JWST-GO-1981-CHAMPs.md (stub), wiki/concepts/{transmission-spectrum,stellar-contamination}.md (stubs)
**Updated:** index.md
**Tension flagged:** [[GJ1132b]] atmosphere — H₂-dominated atmosphere with HCN/CH₄ (Swain et al. 2021, HST/WFC3; not yet ingested) vs no H₂/HCN atmosphere at >4.2σ ([[2023_May_GJ1132b]], JWST NIRSpec G395H). Prior HST featureless results (Mugnai et al. 2021; Libby-Roberts et al. 2022; not yet ingested) are consistent with the JWST non-detection. Recorded in wiki/papers/2023_May_GJ1132b.md § Tensions.
**Emphasis decisions (user-approved "go with your recommendations"):**
- TL;DR framed as (A) null/cautionary + (C) overturning prior work; deferred (B) tentative detection framing.
- Code stubs limited to Eureka! and POSEIDON; FIREFLy, ExoTiC-JEDI, CHIMERA, PICASO, batman, ExoTiC-LD, PyMultiNest, Dynesty, lmfit, lacosmic mentioned in prose only.
- Concept seeding limited to transmission-spectrum and stellar-contamination.
- HCN species page deferred (ruled-out-only in this paper).

## [2026-04-22] schema | add planet `class:` taxonomy with unit convention and star spectral `class:`
**Change:**
- Target (planet) frontmatter: add `class: terrestrial | sub-neptune | neptune | gas-giant`. Mass/radius unit convention tied to class — terrestrial/sub-neptune use `mass_mearth`/`radius_rearth`; neptune/gas-giant use `mass_mjup`/`radius_rjup`.
- Target (star) frontmatter: add `class: A | F | G | K | M | other` (MK spectral type).
- Both `class:` fields are strongly recommended but not strictly required (only `type:` remains strictly required).
**Reason:** Ingesting the 1.66 M⊕ super-Earth GJ 1132 b surfaced that the previous Jupiter-only unit convention is unreadable for terrestrial planets (0.0052 M_J). The `class:` field also enables future lint rules and cross-target queries to aggregate by category. Star class added symmetrically at user request so planet and star pages follow parallel conventions.
**Retroactive migration:** None, per CLAUDE.md § Schema evolution ("this file is the contract for new work"). `wiki/targets/GJ1132b.md` already uses `mass_mearth`/`radius_rearth` (written as an off-schema workaround during ingest) and conforms to the new schema except for a missing `class: terrestrial` field; left as-is. `wiki/targets/GJ1132.md` similarly lacks `class: M`; left as-is. A future lint pass can surface both as findings for opt-in per-page migration.

## [2026-04-22] ingest | 2025_Bennett_GJ1132b
**Paper:** Bennett, MacDonald, Peacock, Perez, May et al. 2025, AJ 170:205 — "Additional JWST/NIRSpec Transits of the Rocky M Dwarf Exoplanet GJ 1132 b Reveal a Featureless Spectrum" (doi:10.3847/1538-3881/adf198)
**PDF renamed:** raw/papers/2025_Bennett_GJ1132b.pdf
**Created:** wiki/papers/2025_Bennett_GJ1132b.md, wiki/codes/PICASO.md (stub), wiki/codes/CHIMERA.md (stub), wiki/methods/multi-visit-stacking.md (stub), wiki/concepts/cosmic-shoreline.md (stub)
**Updated:** wiki/targets/GJ1132b.md (added `## Observations to date` section covering the 2023-tentative → 2025-retired arc), wiki/targets/GJ1132.md (new paper bullet), wiki/instruments/JWST-NIRSpec.md (new paper bullet), wiki/programs/JWST-GO-1981-CHAMPs.md (new paper bullet), wiki/methods/transmission-spectroscopy.md (new paper bullet), wiki/methods/stellar-contamination-modeling.md (new paper bullet), wiki/species/{H2O,CH4,CO2}.md (new paper bullets), wiki/codes/Eureka.md (new paper bullet), wiki/concepts/transmission-spectrum.md (new paper bullet), wiki/concepts/stellar-contamination.md (new paper bullet), index.md
**Supersession note:** [[2023_May_GJ1132b]] Visit-1 tentative H₂O + CH₄ + N₂O inference is superseded by [[2025_Bennett_GJ1132b]]'s four-visit coadded flat spectrum + leave-one-out analysis; Visit-1 deviation reattributed to evolving stellar heterogeneity (a large cool spot that rotated out of view before Visit 2). Per CLAUDE.md § Stale claims, the May 2023 paper page is preserved as-is; [[GJ1132b]] target page carries the updated synthesis.
**Tension update:** [[GJ1132b]] atmosphere — H₂/HCN claim (Swain et al. 2021, HST/WFC3; not yet ingested) remains ruled out; this paper strengthens the rejection (1000× solar H₂/He now ruled out at > 4σ on 4-visit coadd) and cites independent CRIRES+ ground-based follow-up (Palle et al. 2025; not yet ingested) that also rules out the HCN signature. Tension reinforced rather than resolved — full closure awaits ingest of Swain 2021 and/or Palle 2025.
**Promotion candidacy:** [[GJ1132b]] now has 2 direct paper references and >5 inbound links from wiki/ pages — crosses the stub-promotion threshold (≥3 papers OR ≥5 inbound links). NOT promoted during ingest per "never automatic" rule; surfaces as a promotion candidate at the next lint pass for user approval.
**Emphasis decisions (user-approved "go"):**
- TL;DR framed as (A) bare-rock confirmation + (C) resolution of May 2023 tentative detection.
- New stubs: PICASO, CHIMERA, multi-visit-stacking, cosmic-shoreline.
- GJ1132b target page kept as stub (not hub-promoted); added short `## Observations to date` paragraph.
- `atmospheric-retrievals` method page NOT updated — Bennett 2025 interprets via forward-model χ²ν + Bayes-factor comparison rather than full retrievals.
- HCN, CO, POSEIDON, JWST GTO 1274 pages still deferred (ruled-out-only, speculative, or single-paper).

## [2026-04-22] schema | codify conventions from first two ingests
**Change:** seven additive edits to CLAUDE.md, all codifying patterns that emerged during the 2023_May_GJ1132b and 2025_Bennett_GJ1132b ingests:
- Paper frontmatter: document optional `species_tentative`, `species_ruled_out`, `codes` fields.
- Page templates: add "Target (stub + synthesis — intermediate state)" template for 2-paper targets not yet hub-promoted.
- Operations § ingest step 3: loosen the "~10-line summary" guidance to "~10–15 bullets plus focused framing questions."
- Operations § preamble: one-line note that wiki operations are sequential and do not need subagents or `superpowers:*` skills.
- Edge cases: add "Referencing not-yet-ingested papers" subsection codifying the prose-with-`(not yet ingested)` convention.
- Stale claims: explicit bullet that paper pages are frozen at ingest time; supersessions go on target/hub pages + superseding paper's `## Tensions`.
- log.md conventions: canonicalize `**Tension update:**`, `**Supersession note:**`, `**Promotion candidacy:**`, `**Emphasis decisions:**` alongside the existing `**Tension flagged:**`.
**Reason:** CLAUDE.md § Schema evolution — "propose a schema edit rather than silently working around it." All seven conventions had already been used organically across both ingests; codifying them reduces drift and makes the schema self-documenting for the next ingest. Triggered by a /claude-md-improver audit that scored the file 87/100 (Grade B) and flagged these as gaps.
**Retroactive migration:** None. Existing pages and log entries remain as written; new work follows the codified conventions.

## [2026-04-22] ingest | batch — 4 papers (Lustig-Yaeger 2023, Alderson 2024, Alam 2025, Alderson 2025)
**Papers:**
- [[2023_Lustig-Yaeger_LHS475b]] — Lustig-Yaeger et al. 2023, Nature Astronomy — first JWST transmission spectrum of an Earth-sized exoplanet (LHS 475 b); featureless; rules out H₂/He atmospheres at >10σ.
- [[2024_Alderson_TOI-836b]] — Alderson et al. 2024, AJ — JWST COMPASS NIRSpec G395H on super-Earth TOI-836 b; flat spectrum rules out H₂-dominated atmospheres at <250× solar.
- [[2025_Alam_L168-9b]] — Alam et al. 2025, AJ — JWST COMPASS first broadband 3–12 μm (NIRSpec + MIRI) transmission spectrum of a rocky exoplanet (L 168-9 b); featureless; rules out <100× solar metallicity.
- [[2025_Alderson_TOI-776b]] — Alderson et al. 2025, arXiv:2501.14596 — JWST COMPASS NIRSpec G395H on super-Earth TOI-776 b; flat after detector-offset correction; rules out <100× solar.
**File hygiene:** deleted 2 byte-identical duplicate PDFs from raw/papers/ (" 1." suffixed); renamed 2 files with `.14596` arXiv-ID extension to `.pdf`; all 4 final filenames now in bibkey.pdf form.
**Created:** 4 paper pages, 8 target stubs (wiki/targets/{L168-9b,L168-9,LHS475b,LHS475,TOI-776b,TOI-776,TOI-836b,TOI-836}.md — all with `class:` per the 2026-04-22 schema edit), wiki/instruments/JWST-MIRI.md (new instrument), wiki/programs/JWST-GO-2512-COMPASS.md (new program), wiki/codes/{ExoTiC-JEDI,FIREFLy,Tiberius}.md (3 new code stubs).
**Updated:** wiki/programs/JWST-GO-1981-CHAMPs.md (added [[2023_Lustig-Yaeger_LHS475b]] bullet AND resolved the prose reference "(Lustig-Yaeger et al. 2023)" in the lede paragraph to a [[link]]), wiki/instruments/JWST-NIRSpec.md, wiki/methods/{transmission-spectroscopy,atmospheric-retrievals,stellar-contamination-modeling,multi-visit-stacking}.md, wiki/species/{H2O,CH4,CO2}.md, wiki/concepts/{transmission-spectrum,stellar-contamination,cosmic-shoreline}.md, wiki/codes/{Eureka,PICASO,CHIMERA}.md, index.md.
**Prose-reference resolutions deferred to lint (per CLAUDE.md § Stale claims, paper pages are frozen at ingest time):** prose references "(Lustig-Yaeger et al. 2023; not yet ingested)" on wiki/papers/2023_May_GJ1132b.md and wiki/papers/2025_Bennett_GJ1132b.md intentionally NOT updated during this ingest. They surface as lint findings for user approval at next lint pass (per the "Referencing not-yet-ingested papers" mechanism codified in the 2026-04-22 CLAUDE.md update). This is the first time that mechanism is exercised for real.
**Promotion candidacies:** none newly introduced — each of the 4 new targets has 1 paper; below both thresholds.
**Emphasis decisions (user-approved "go"):**
- TL;DR framings per paper: Alam → "first NIR + MIR transmission spectrum of a rocky planet; featureless"; Alderson 2024 TOI-836b → "flat; no H₂; contrast with sub-Neptune sibling TOI-836 c"; Alderson 2025 TOI-776b → "flat after detector-offset correction; rules out <100× solar"; Lustig-Yaeger 2023 → "first JWST transit of an Earth-sized planet; rules out H₂/He at >10σ; no NIRSpec noise floor above 5 ppm."
- Alam 2025 year = 2025 (matches AJ volume 169; literature often cites as "2024" — preprint date; consistent with journal-year convention).
- Alderson 2025 TOI-776b: DOI pending publication; arxiv ID recorded in frontmatter instead.
- Code stubs created: ExoTiC-JEDI (now 4 papers), FIREFLy (3 papers), Tiberius (2 papers). Aesop and ExoTiC-MIRI still deferred (single-use).
- No new concept pages created; existing cosmic-shoreline absorbs the photoevaporation framing from Alam 2025.
- New entities deferred to prose (with "(not yet ingested)" suffix): Hawthorn 2023, Wallack 2024 TOI-836c, Fridlund 2024, Luque 2021, Astudillo-Defru 2020, Teske & Batalha submitted TOI-776c, Ment in-prep LHS475b, Moran 2023 GJ486b, Alderson 2022/2023 ExoTiC-JEDI papers, Rustamkulov 2022/2023 FIREFLy papers, Kirk 2018/2019/2021 Tiberius papers, Rieke 2015 / Kendrew 2015 / Bouwman 2023 MIRI, N. E. Batalha 2023 COMPASS.

## [2026-04-23] schema | broaden wiki scope to include emission spectroscopy
**Change:** CLAUDE.md lede updated from "personal, encyclopedic wiki on transmission spectroscopy of exoplanet atmospheres" to "personal, encyclopedic wiki on exoplanet atmospheric characterization — primarily transmission spectroscopy, with emission (secondary-eclipse and phase-curve) results included when they bear directly on the same targets or questions."
**Reason:** ingesting [[2024_Wachiraphan_LTT1445Ab]] (MIRI/LRS emission on LTT 1445 A b) and [[2024_WeinerMansfield_GJ486b]] (MIRI/LRS emission on Gl 486 b) surfaced the need for emission results to live alongside transmission. These papers directly constrain the same targets and atmospheric questions as the wiki's existing transmission corpus (cosmic shoreline, bare-rock vs atmosphere, rocky-planet retention). Scope expansion is additive — transmission remains primary.
**Retroactive migration:** None. Existing pages and prose remain as-is.

## [2026-04-23] ingest | batch — 5 papers (Banerjee 2024, Gressier 2024, Scarsdale 2024, Wachiraphan 2024, Weiner Mansfield 2024)
**Papers:**
- [[2024_Banerjee_L98-59d]] — Banerjee et al. 2024, ApJL 975:L11 — retrievals on L 98-59 d NIRSpec transit favor H₂S/SO₂ secondary atmosphere (~2σ each; combined 2.2σ stellar+atmo vs stellar-only). Companion "Paper II" to Gressier.
- [[2024_Gressier_L98-59d]] — Gressier et al. 2024, ApJL 975:L10 — companion "Paper I" on the same transit; atmospheric feature at 3.3–4.8 μm preferred at 2.6σ–5.6σ with H₂S driving the fit.
- [[2024_Scarsdale_L98-59c]] — Scarsdale et al. 2024, AJ 168:276 — JWST COMPASS two-visit NIRSpec G395H on L 98-59 c; featureless; rules out <300× solar metallicity.
- [[2024_Wachiraphan_LTT1445Ab]] — Wachiraphan et al. 2024, arXiv:2410.10987 — first MIRI/LRS emission paper in the wiki; three eclipses of LTT 1445 A b; T_day=525 K; rules out thick CO₂ atmospheres at >6σ.
- [[2024_WeinerMansfield_GJ486b]] — Weiner Mansfield et al. 2024, ApJL 975:L22 — two MIRI/LRS eclipses of Gl 486 b; T_day=865 K, R=0.97; airless body; retires the water-rich atmosphere interpretation from Moran 2023 transmission.
**File hygiene:** renamed 5 PDFs to bibkey.pdf form; no duplicates.
**Created:** 5 paper pages, 7 target stubs (L98-59d, L98-59c, L98-59, LTT1445Ab, LTT1445A, GJ486b, GJ486 — all with `class:` per schema; GJ486 uses aliases to cover "Gl 486" variant), 3 program stubs (JWST-GTO-1224, JWST-GO-1743, JWST-GO-2708), 2 species stubs (H2S, SO2), 1 method stub (secondary-eclipse-spectroscopy — the emission-side analog of transmission-spectroscopy), 2 code stubs (SPARTA at 2 papers, transitspectroscopy at 2 papers).
**Updated:** wiki/instruments/JWST-NIRSpec.md, wiki/instruments/JWST-MIRI.md, wiki/programs/JWST-GO-2512-COMPASS.md, wiki/methods/{transmission-spectroscopy,atmospheric-retrievals,stellar-contamination-modeling,multi-visit-stacking}.md, wiki/concepts/{stellar-contamination,transmission-spectrum,cosmic-shoreline}.md, wiki/codes/{Eureka,FIREFLy,ExoTiC-JEDI,PICASO}.md, wiki/species/{H2O,CO2}.md, index.md, CLAUDE.md (scope lede).
**Tension flagged:** [[GJ486b]] atmosphere — water-rich atmosphere claim (Moran et al. 2023 NIRSpec/G395H transmission; not yet ingested) vs airless body (R = 0.97±0.01 from MIRI/LRS emission in [[2024_WeinerMansfield_GJ486b]]). The emission constraint is directly incompatible with a water-rich atmosphere; Moran 2023 transmission features must be attributed to stellar contamination rather than atmosphere. **First case in the wiki where an emission observation retires a tentative transmission-based atmospheric detection.** Full closure awaits ingest of Moran 2023.
**System-level pattern (not a tension):** the L 98-59 system now has differing atmospheric outcomes for two of its planets — [[L98-59c]] featureless ([[2024_Scarsdale_L98-59c]]) vs [[L98-59d]] with sulfur hints ([[2024_Banerjee_L98-59d]], [[2024_Gressier_L98-59d]]). Genuine astrophysical difference between planets around the same star, likely driven by differences in tidal heating and bulk composition.
**Companion-paper cross-linking:** Banerjee 2024 (Paper II) and Gressier 2024 (Paper I) on the same L 98-59 d transit are cross-linked in both paper pages' `## Related` and `## Tensions` sections; treated as methodology cross-check, not disagreement.
**Promotion candidacies:** [[L98-59]] (3 papers, 6+ inbound links) crosses the stub-promotion threshold. Not promoted during ingest per "never automatic" rule; surfaces as candidate at next lint.
**Emphasis decisions (user-approved "go"):**
- Scope: option (A) — emission papers accepted; CLAUDE.md lede edit as schema entry (above).
- TL;DR framings per paper: Banerjee → "retrievals favor H₂S/SO₂ secondary atmosphere"; Gressier → "2.6σ–5.6σ atmospheric detection with H₂S primary"; Scarsdale → "featureless, rules out <300× solar"; Wachiraphan → "first MIRI emission in wiki; bare rock, no thick CO₂"; Weiner Mansfield → "airless; retires Moran 2023 water-rich claim".
- Gl 486 b filename = GJ486b.md, aliases include `Gl 486 b` + `Gl486b` (matches GJ1132b convention).
- Code stubs: SPARTA (2 papers) and transitspectroscopy (2 papers) created. NEMESISPY, TauREx3, exoretrievals, Exo-REM, EXOFASTv2, HELIOS deferred (single-use).
- Program stubs: all three new programs (GTO 1224, GO 1743, GO 2708) created despite being single-paper — they are concrete, named, and likely to host future papers.
- Gl 486 b tension formally flagged; Moran 2023 prose reference awaits ingestion.

## [2026-04-24] ingest | 2023_Moran_GJ486b
**Paper:** Moran, Stevenson, Sing, MacDonald, Kirk, Lustig-Yaeger et al. 2023, ApJL 948:L11 — "High Tide or Riptide on the Cosmic Shoreline? A Water-rich Atmosphere or Stellar Contamination for the Warm Super-Earth GJ 486 b from JWST Observations" (doi:10.3847/2041-8213/accb9c)
**PDF renamed:** raw/papers/2023_Moran_GJ486b.pdf
**Created:** wiki/papers/2023_Moran_GJ486b.md. No new entity stubs — all target/instrument/method/species/code/program pages already exist.
**Updated:** wiki/targets/GJ486b.md (converted Tensions prose reference to [[link]], rewrote `## Observations to date` to use both [[links]]), wiki/targets/GJ486.md (new paper bullet), wiki/programs/JWST-GO-1981-CHAMPs.md (resolved "(Moran et al. 2023; not yet ingested)" prose reference to [[2023_Moran_GJ486b]]; added new paper bullet), wiki/instruments/JWST-NIRSpec.md, wiki/methods/{transmission-spectroscopy,atmospheric-retrievals,stellar-contamination-modeling,multi-visit-stacking}.md, wiki/concepts/{stellar-contamination,transmission-spectrum,cosmic-shoreline}.md, wiki/codes/{Eureka,FIREFLy,Tiberius,POSEIDON,PICASO,CHIMERA}.md, wiki/species/{H2O,CH4,CO2}.md, index.md. Also converted the existing `## stellar-contamination` page's Weiner Mansfield bullet to cite "[[2023_Moran_GJ486b]]" in place of the prior "Moran 2023" prose reference (non-paper page; safe to update).
**Tension resolved:** [[GJ486b]] water-rich atmosphere vs starspot contamination — **status changed from "flagged awaiting Moran ingest" to "resolved in favor of starspot contamination"**. Moran 2023 presented both scenarios as equally Bayesian; [[2024_WeinerMansfield_GJ486b]] emission (R=0.97, airless) rules out water-rich. Both papers now [[linked]] on the target page's `## Tensions` entry.
**Prose-reference resolutions (to paper pages, deferred to lint per § Stale claims):** the following paper pages contain prose references to "Moran et al. 2023 (not yet ingested)" or "S. E. Moran et al. 2023" that are NOT updated during this ingest because paper pages are frozen. Lint pass can convert: wiki/papers/{2023_May_GJ1132b, 2025_Bennett_GJ1132b, 2025_Alam_L168-9b, 2024_Gressier_L98-59d, 2024_Banerjee_L98-59d, 2024_Scarsdale_L98-59c, 2024_WeinerMansfield_GJ486b}.md.
**Promotion candidacies:** [[GJ486b]] (2 papers, many inbound links) crosses stub-promotion threshold; [[GJ486]] (2 papers) on the borderline. Not promoted during ingest per "never automatic" rule.
**Emphasis decisions (user-approved "go"):**
- TL;DR framed honestly as Moran's **two-scenario presentation**; resolution narrative lives on [[GJ486b]] target page, with a Tensions entry on the Moran paper page noting the later supersession by [[2024_WeinerMansfield_GJ486b]].
- No new entities created — all referenced entities already exist.
- POSEIDON stub, previously single-use, is now at 2 papers; a candidate for more prominent visibility at next lint pass.
- Ridden-Harper 2022, Caballero 2022, Trifonov 2021 (GJ 486 b ground-based + discovery references) still deferred (prose with `(not yet ingested)`).

## [2026-04-24] ingest | 2025_Rathcke_TRAPPIST1bc
**Paper:** Rathcke et al. 2025, ApJL 979 L19 — JWST/NIRSpec PRISM back-to-back transits of TRAPPIST-1 b and c; proof-of-concept empirical stellar-contamination correction
**Created:** wiki/papers/2025_Rathcke_TRAPPIST1bc.md, wiki/targets/TRAPPIST-1.md, wiki/targets/TRAPPIST-1b.md, wiki/targets/TRAPPIST-1c.md, wiki/methods/back-to-back-transit-correction.md, wiki/codes/Frida.md, wiki/codes/speclib.md, wiki/codes/spotter.md, wiki/codes/SPHINX.md, wiki/programs/JWST-GO-2420.md
**Updated:** wiki/instruments/JWST-NIRSpec.md (added PRISM mode + paper), wiki/concepts/stellar-contamination.md (added Tensions entry on geometry; paper ref), wiki/methods/stellar-contamination-modeling.md (paper ref + cross-link to back-to-back-transit-correction), wiki/methods/multi-visit-stacking.md (paper ref), index.md
**Tension flagged:** [[stellar-contamination]] — fully-unocculted-spot geometry (Rackham et al. 2018, not yet ingested) predicts ~1740 ppm peak-to-peak >2.5 μm contamination on TRAPPIST-1; well-mixed-photosphere geometry ([[2025_Rathcke_TRAPPIST1bc]]) predicts ~280 ppm. Different geometric assumptions, not a contradiction in principle, but materially reframes the long-wavelength contamination budget.
**Emphasis decisions (user-approved "go"):**
- New `back-to-back-transit-correction` method page — kept distinct from `stellar-contamination-modeling` because the technique is empirical and model-independent, not a variant of forward/retrieval modeling.
- SPHINX filed under `codes/` per category-rule 3 (software implementation), with a stub noting the 2000 K grid floor.
- Frida, speclib, spotter all given dedicated stubs — likely to recur in future TRAPPIST-1 / Rackham-group papers.
- TRAPPIST-1 b/c target stubs reference Greene 2023 / Zieba 2023 in prose with `(not yet ingested)` per the schema rule, rather than fabricated paper stubs.
- `species_detected` / `species_tentative` / `species_ruled_out` all empty: this is a methods paper, no species claims.
- Gillon 2016/2017 (TRAPPIST-1 discovery), Agol 2021 (system parameters), Rackham 2018, Wakeford 2019, Garcia 2022, Iyer 2023 (SPHINX), TRAPPIST-1 JWST Community Initiative 2024, Greene 2023, Zieba 2023, Lim 2023, Lincowski 2018/2023, Ducrot 2018/2024, Radica 2024, Burdanov 2019, Morris 2018, Zhang 2018, Davoudi 2024, Narrett 2024, Triaud 2023, Turbet 2023, Witzke 2021, Berardo 2024, Roettenbacher & Kane 2017, Zahnle & Catling 2017, Fauchez 2019, Skrutskie 2006, Kipping 2013, Foreman-Mackey 2013, Bushouse 2024 — all referenced via prose `(not yet ingested)` where needed.

## [2026-04-25] ingest | 2025_Teske_TOI776c
**Paper:** Teske, Batalha et al. 2025, AJ 169:249 — "JWST COMPASS: NIRSpec/G395H Transmission Observations of TOI-776 c, a 2 R⊕ M Dwarf Planet" (doi:10.3847/1538-3881/adb975)
**PDF renamed:** raw/papers/2025_Teske_TOI776c.pdf
**Created:** wiki/papers/2025_Teske_TOI776c.md, wiki/targets/TOI-776c.md (new stub — planet was previously mentioned in prose but had no page)
**Updated:** wiki/targets/TOI-776.md (prose reference to "TOI-776 c" upgraded to [[TOI-776c]] link; added Teske paper; updated description), wiki/targets/TOI-776b.md (upgraded "(Teske & Batalha et al., submitted; not yet ingested)" to [[2025_Teske_TOI776c]] + [[TOI-776c]] links), wiki/methods/transmission-spectroscopy.md (paper ref), wiki/methods/atmospheric-retrievals.md (paper ref), wiki/methods/multi-visit-stacking.md (paper ref), wiki/codes/Eureka.md (paper ref), wiki/codes/Tiberius.md (paper ref), wiki/codes/PICASO.md (paper ref), wiki/programs/JWST-GO-2512-COMPASS.md (paper ref), index.md
**Emphasis decisions (user-approved "go with preferred approaches"):**
- species_ruled_out left empty: constraints are on metallicity/MMW regime, not named species in isolation.
- UltraNest (Buchner 2021), Cantera (Goodwin et al. 2022), ExoTiC-LD (Grant & Wakeford 2024), mc3, emcee, batman — all treated as prose-only ancillary tools; no stubs created, consistent with prior pattern.
- Planet class set to `sub-neptune` (2.02 R⊕, 5.3 M⊕); unit convention `mass_mearth` / `radius_rearth` per schema.
- TOI-776 c TL;DR highlights both the metallicity limit AND the model-dependence caveat, per the paper's own emphasis.
- TOI-270 d (Benneke et al. 2024) referenced in prose as "(not yet ingested)" in the paper page.

## [2026-04-24] ingest | 2025_Redai_GJ357b
**Paper:** Redai, Wogan, Wallack, Alam et al. 2025, arXiv:2507.07165 — JWST COMPASS NIRSpec G395H transmission spectrum of the super-Earth GJ 357 b; featureless 2.87–5.14 μm; rules out MMW < 8 g/mol at 3σ and metallicity < 300–500× solar
**PDF renamed:** raw/papers/2025_Redai_GJ357b.pdf
**Created:** wiki/papers/2025_Redai_GJ357b.md. No new target, instrument, or program stubs required — all already exist.
**Updated:** wiki/targets/GJ357b.md (added `## Observations to date` section narrating Taylor + Redai arc; updated See also papers list), wiki/targets/GJ357.md (added paper ref), wiki/methods/transmission-spectroscopy.md (paper ref), wiki/methods/atmospheric-retrievals.md (paper ref), wiki/codes/Tiberius.md (paper ref), wiki/codes/Eureka.md (paper ref), wiki/programs/JWST-GO-2512-COMPASS.md (paper ref), wiki/concepts/cosmic-shoreline.md (paper ref), index.md
**Emphasis decisions (user-approved "go with preferred approaches"):**
- equilibrate (Wogan et al. 2024 Photochem) and Ultranest (Buchner 2021) treated as ancillary tools; cited in prose with `(not yet ingested)` rather than given code stubs — consistent with the dynesty/MultiNest/batman precedent.
- species_ruled_out left empty: constraint is a mean-molecular-weight / metallicity regime rather than a named species; captured in key findings prose.
- GJ357b promoted to stub+synthesis (intermediate state) per the schema: 2 papers, "Observations to date" section added, hub promotion deferred pending threshold.

## [2026-04-24] ingest | 2024_Xue_GJ1132b
**Paper:** Xue, Bean, Zhang, Mahajan, Ih, Eastman, Lunine, Weiner Mansfield, Coy, Kempton, Koll, Kite 2024, ApJL 973:L8 — JWST MIRI/LRS secondary eclipse of GJ 1132 b; T_day = 709 ± 31 K, R = 0.95 ± 0.04; bare-rock consistent
**PDF renamed:** raw/papers/2024_Xue_GJ1132b.pdf
**Created:** wiki/papers/2024_Xue_GJ1132b.md, wiki/programs/JWST-GTO-1274.md, wiki/codes/HELIOS.md, wiki/codes/EXOFASTv2.md
**Updated:** wiki/targets/GJ1132b.md (upgraded "(Xue et al. 2024; not yet ingested)" prose ref to [[2024_Xue_GJ1132b]] in Observations to date; added to See also), wiki/targets/GJ1132.md (added paper ref), wiki/papers/2025_Bennett_GJ1132b.md (upgraded three Xue prose references to [[2024_Xue_GJ1132b]] wiki-links; final Related bullet reformatted), wiki/methods/secondary-eclipse-spectroscopy.md (paper ref), wiki/instruments/JWST-MIRI.md (paper ref), wiki/codes/SPARTA.md (paper ref), wiki/codes/Eureka.md (paper ref), index.md
**Emphasis decisions (user-approved "go with preferred approaches"):**
- HELIOS stub created: primary emission forward-model code, likely to recur in future MIRI/LRS emission papers.
- EXOFASTv2 stub created: well-known system-parameter code used as prior-setting tool; likely to recur.
- species_ruled_out left empty: exclusions are atmospheric pressure/composition regimes (CO₂ < 0.006 bar, H₂O < 0.16 bar, Earth/Venus-like), not named species in isolation.
- EXOFASTv2 standalone paper (Eastman et al. 2019) and HELIOS papers (Malik et al. 2017, 2019) cited in prose with `(not yet ingested)` per schema rule.
**Promotion candidacy:** [[GJ1132b]] now at 3 papers ([[2023_May_GJ1132b]], [[2025_Bennett_GJ1132b]], [[2024_Xue_GJ1132b]]); [[GJ1132]] (star) also at 3 papers. Both cross the stub-promotion threshold (≥3 papers). Not promoted per "never automatic" rule — awaiting user approval at next lint.

## [2026-04-24] ingest | 2025_Taylor_GJ357b
**Paper:** Taylor et al. 2025, MNRAS (accepted 2025-05-30) — JWST NIRISS/SOSS transmission spectrum of the super-Earth GJ 357 b; featureless; case for atmospheric retention
**Created:** wiki/papers/2025_Taylor_GJ357b.md, wiki/targets/GJ357b.md, wiki/targets/GJ357.md, wiki/instruments/JWST-NIRISS.md, wiki/codes/exoTEDRF.md, wiki/codes/juliet.md, wiki/programs/JWST-GTO-1201.md
**Updated:** wiki/concepts/cosmic-shoreline.md (paper ref), wiki/methods/transmission-spectroscopy.md (paper ref), wiki/methods/stellar-contamination-modeling.md (paper ref), wiki/papers/2024_Gressier_L98-59d.md (juliet wiki-link upgrade + frontmatter codes update), index.md
**Emphasis decisions (user-approved "go"):**
- AGNI emission model (Hammond et al. 2024) skipped — only used for MIRI forward-modelling predictions, not primary data analysis; deferred until a paper uses it on actual data.
- MAGRATHEA interior code skipped — outside the atmospheric characterisation scope of the wiki.
- species_ruled_out left empty: constraint is a regime/scenario ("≤100× solar metallicity with cloud-top pressure > 0.01 bar") not a named species; captured in key findings prose.
- juliet back-reference added to 2024_Gressier_L98-59d.md (prose + frontmatter codes) since it was already used there without a wiki link.
- JWST-GTO-1201 (NEAT) program page notes multi-target scope including L 98-59 b (Damiano et al. 2024, not yet ingested) as referenced in prior ingested papers.

## [2026-04-25] ingest | 2025_Glidden_TRAPPIST1e
**Paper:** Glidden, Ranjan, Seager, Espinoza, MacDonald et al. 2025, ApJL 990:L53 — DREAMS GTO 1331 four-visit NIRSpec PRISM transmission spectroscopy of TRAPPIST-1 e; featureless; H₂-CO₂ ruled out at 5σ; thick CO₂ at 6.9σ; μ > 8.6 u; N₂-rich atmospheres consistent; stellar models (~1800 ppm) dominate over measurement precision (~89 ppm)
**PDF renamed:** raw/papers/2025_Glidden_TRAPPIST1e.pdf
**Created:** wiki/papers/2025_Glidden_TRAPPIST1e.md, wiki/targets/TRAPPIST-1e.md (stub), wiki/programs/JWST-TST-GTO-1331.md, wiki/codes/petitRADTRANS.md
**Updated:** wiki/targets/TRAPPIST-1.md (added TRAPPIST-1e link; added paper refs), wiki/methods/multi-visit-stacking.md, wiki/methods/stellar-contamination-modeling.md, wiki/methods/transmission-spectroscopy.md, wiki/methods/atmospheric-retrievals.md, wiki/concepts/stellar-contamination.md, index.md
**Emphasis decisions (user-approved "go with preferred approaches"):**
- MEAC photochemistry code (Rajan et al. 2022) skipped — prose-only; single use.
- transitspectroscopy cited in prose only (via companion Espinoza et al. 2025, not yet ingested).
- petitRADTRANS stub created: primary forward-modeling code, widely used, likely to recur.

## [2026-04-25] ingest | 2023_Lim_TRAPPIST1b
**Paper:** Lim, Benneke, Doyon, MacDonald, Piaulet et al. 2023, ApJL 955:L22 — two NIRISS/SOSS transits of TRAPPIST-1 b; stellar contamination dominates; H₂-dominated atmospheres rejected at 16–29σ; secondary atmospheres unconstrained
**PDF renamed:** raw/papers/2023_Lim_TRAPPIST1b.pdf
**Created:** wiki/papers/2023_Lim_TRAPPIST1b.md, wiki/programs/JWST-GO-2589.md, wiki/codes/supreme-SPOON.md, wiki/codes/NAMELESS.md, wiki/codes/SOSSISSE.md, wiki/codes/SCARLET.md
**Updated:** wiki/targets/TRAPPIST-1b.md (added Observations to date section, added Lim paper; count 1→2), wiki/targets/TRAPPIST-1.md (added paper ref; count 1→3), wiki/instruments/JWST-NIRISS.md (added paper ref), wiki/codes/POSEIDON.md (added paper ref), wiki/methods/multi-visit-stacking.md, wiki/methods/stellar-contamination-modeling.md, wiki/methods/transmission-spectroscopy.md, wiki/methods/atmospheric-retrievals.md, wiki/concepts/stellar-contamination.md, index.md
**Emphasis decisions (user-approved "go with preferred approaches"):**
- ExoTEP, MSG stellar models skipped — prose-only; single use each.
- Tension entry added to 2023_Lim_TRAPPIST1b.md: NIRISS/SOSS contamination amplitude (~750–1000 ppm) vs NIRSpec/PRISM (~280 ppm from Rathcke 2025); explained by wavelength range + epoch differences, not a fundamental contradiction.
**Promotion candidacy:** [[TRAPPIST-1]] (star) now at 3 papers ([[2025_Rathcke_TRAPPIST1bc]], [[2023_Lim_TRAPPIST1b]], [[2025_Glidden_TRAPPIST1e]]). Crosses the stub-promotion threshold (≥3 papers). Not promoted per "never automatic" rule — awaiting user approval at next lint.

## [2026-04-25] ingest | 2025_Xue_GJ3929b
**Paper:** Xue, Zhang, Park Coy, Brady, Ji, Bean et al. 2025, ApJL 995:L52 — two MIRI F1500W photometric eclipses of GJ 3929 b; T_day = 782 ± 79 K, R ≈ 1.07; bare-rock; CO₂ > 100 mbar excluded; new MAROON-X RVs refine mass to 1.13 ± 0.09 M⊕
**PDF renamed:** raw/papers/2025_Xue_GJ3929b.pdf
**Created:** wiki/papers/2025_Xue_GJ3929b.md, wiki/targets/GJ3929b.md (stub), wiki/targets/GJ3929.md (stub), wiki/programs/JWST-DD-9235.md
**Updated:** wiki/instruments/JWST-MIRI.md (added paper ref; fixed merged-entry formatting bug; added note on photometric imaging vs LRS distinction), wiki/codes/SPARTA.md (paper ref), wiki/codes/HELIOS.md (paper ref), wiki/codes/juliet.md (paper ref), wiki/methods/secondary-eclipse-spectroscopy.md (paper ref; note photometric not spectroscopic), index.md
**Emphasis decisions (user-approved "go with preferred approaches"):**
- smint (interior composition code) skipped — prose-only; outside atmospheric-characterization scope.
- SPHINX code page already exists; added GJ3929b note in paper page only (no separate SPHINX page update needed for single new use).
- Photometry-vs-spectroscopy distinction explicitly noted in paper page, JWST-MIRI page, and secondary-eclipse-spectroscopy method page.
**Promotion candidacy:** [[POSEIDON]] now at 3 papers ([[2023_May_GJ1132b]], [[2023_Moran_GJ486b]], [[2023_Lim_TRAPPIST1b]]). Crosses stub-promotion threshold (≥3 papers). Not promoted per "never automatic" rule — awaiting user approval at next lint.

## [2026-04-27] ingest | 2025_Espinoza_TRAPPIST1e
**Paper:** Espinoza, Allen, Glidden, Lewis, Seager et al. 2025, ApJL 990:L52 — DREAMS GTO 1331 four-visit NIRSpec PRISM of TRAPPIST-1 e; data reduction + GP stellar contamination companion to Glidden et al. 2025 (L53); PHOENIX models fail for TRAPPIST-1; novel GP marginalization (celerite Matèrn 3/2) over contamination without assuming specific photospheric model; cloudy H₂-dominated (≥80%) atmospheres ruled out >3σ
**PDF renamed:** raw/papers/2025_Espinoza_TRAPPIST1e.pdf
**Created:** wiki/papers/2025_Espinoza_TRAPPIST1e.md
**Updated:** wiki/targets/TRAPPIST-1e.md (added Espinoza paper ref; count 1→2), wiki/targets/TRAPPIST-1.md (added Espinoza ref; count 3→4), wiki/programs/JWST-TST-GTO-1331.md (added Espinoza paper ref; count 1→2), wiki/papers/2025_Glidden_TRAPPIST1e.md (resolved 3 "(not yet ingested)" Espinoza prose refs → [[2025_Espinoza_TRAPPIST1e]] wiki-links; added to Related section), wiki/instruments/JWST-NIRSpec.md, wiki/codes/Eureka.md, wiki/codes/ExoTiC-JEDI.md, wiki/codes/transitspectroscopy.md, wiki/codes/juliet.md, wiki/methods/multi-visit-stacking.md, wiki/methods/stellar-contamination-modeling.md, wiki/methods/transmission-spectroscopy.md, wiki/concepts/stellar-contamination.md, index.md
**Emphasis decisions (user-approved "go with preferred approaches"):**
- GP marginalization approach (not explicit stellar model) is the key methodological contribution; surfaced as a new tension with model-based approaches in the stellar-contamination pages.
- dynesty (Speagle 2020) skipped — prose-only; single use; already appears in other paper pages.
- MPS-ATLAS-1 limb-darkening grid (Kostogryz et al. 2022) skipped — prose-only.
- ExoTiC-LD limb-darkening code skipped — prose-only; single use in this context.

## [2026-04-27] ingest | 2025_Fisher_TOI1685b
**Paper:** Fisher, Hooton, Gressier, Zgraggen, Tian, Heng et al. 2025, MNRAS (arXiv:2512.15338) — GO 4195 five-visit NIRSpec G395H transmission spectroscopy of the M2.5V super-Earth TOI-1685 b; flat; MMW ≳ 10 at ~5σ; CO₂, SO₂, H₂O pure atmospheres ruled out; bare rock likely
**PDF renamed:** raw/papers/2025_Fisher_TOI1685b.pdf
**Created:** wiki/papers/2025_Fisher_TOI1685b.md, wiki/targets/TOI-1685b.md (stub), wiki/targets/TOI-1685.md (stub), wiki/programs/JWST-GO-4195.md
**Updated:** wiki/instruments/JWST-NIRSpec.md, wiki/codes/Eureka.md, wiki/codes/ExoTiC-JEDI.md, wiki/codes/transitspectroscopy.md, wiki/codes/juliet.md, wiki/methods/multi-visit-stacking.md, wiki/methods/transmission-spectroscopy.md, wiki/concepts/stellar-contamination.md, wiki/methods/atmospheric-retrievals.md, wiki/species/SO2.md (fixed pre-existing `//## Papers` typo → `## Papers`; added Fisher ruled-out entry; count 2→3), index.md
**Emphasis decisions (user-approved "go with preferred approaches"):**
- BeAR retrieval code (ETH Zurich / Kitzmann group) skipped — prose-only citation; no published standalone description yet ingested.
- Luque et al. 2025 GO 3263 phase-curve paper cited in prose as `(not yet ingested)` per schema rule.
- Burt et al. 2024 system parameters paper cited in prose as `(not yet ingested)`.
- Sep 1 visit quasi-sinusoidal 200 ppm systematics noted in stellar-contamination concept page as an ambiguous systematic.
**Promotion candidacy:** [[SO2]] now at 3 papers ([[2024_Gressier_L98-59d]], [[2024_Banerjee_L98-59d]], [[2025_Fisher_TOI1685b]]). Crosses stub-promotion threshold (≥3 papers). Not promoted per "never automatic" rule. Species section in index.md split SO2 to per-line per schema (≥3 paper threshold).

## [2026-04-27] ingest | 2025_PiauletGhorayeb_TRAPPIST1d
**Paper:** Piaulet-Ghorayeb, Benneke, Radica, Lafrenière et al. 2025, ApJ 989:181 — NEAT GTO 1201 two-visit NIRSpec PRISM transmission spectroscopy of TRAPPIST-1 d; flat ±100–150 ppm; H₂ excluded >3σ; cloud-free Venus/early Mars/modern Earth excluded >95%; N₂-rich consistent; stellar contamination modeled with stctm
**PDF renamed:** raw/papers/2025_PiauletGhorayeb_TRAPPIST1d.pdf
**Created:** wiki/papers/2025_PiauletGhorayeb_TRAPPIST1d.md, wiki/targets/TRAPPIST-1d.md (stub), wiki/codes/stctm.md
**Updated:** wiki/targets/TRAPPIST-1.md (added TRAPPIST-1d link; added Piaulet-Ghorayeb paper ref; count 4→5), wiki/programs/JWST-GTO-1201.md (added Piaulet-Ghorayeb paper ref; updated description to reflect both NIRISS/SOSS and NIRSpec PRISM usage; count 1→2), wiki/codes/Eureka.md, wiki/codes/SCARLET.md, wiki/methods/multi-visit-stacking.md, wiki/methods/stellar-contamination-modeling.md, wiki/methods/transmission-spectroscopy.md, wiki/methods/atmospheric-retrievals.md, wiki/concepts/stellar-contamination.md, index.md
**Emphasis decisions (user-approved "go with preferred approaches"):**
- exotune sub-framework (embedded in stctm) mentioned in stctm stub prose but no separate page (subordinate tool).
- JWST-GTO-1201 description updated to reflect the discovery that NEAT uses both NIRISS/SOSS and NIRSpec PRISM — program page and index.md description corrected.
**Promotion candidacy:** [[TRAPPIST-1]] (star) now at 5 papers ([[2025_Glidden_TRAPPIST1e]], [[2025_Espinoza_TRAPPIST1e]], [[2025_PiauletGhorayeb_TRAPPIST1d]], [[2023_Lim_TRAPPIST1b]], [[2025_Rathcke_TRAPPIST1bc]]). Reinforces the promotion candidacy first flagged in the 2026-04-25 Lim ingest. Not promoted per "never automatic" rule — awaiting user approval at next lint.

## [2026-04-27] schema | TRAPPIST-1 hub promotion
**Promoted:** [[TRAPPIST-1]] stub → hub (user-approved)
**Trigger:** ≥5 inbound wiki-links AND 5 direct paper references ([[2025_Glidden_TRAPPIST1e]], [[2025_Espinoza_TRAPPIST1e]], [[2025_PiauletGhorayeb_TRAPPIST1d]], [[2023_Lim_TRAPPIST1b]], [[2025_Rathcke_TRAPPIST1bc]])
**Hub sections added:** Basic properties, Atmospheric composition, Observations to date, Open questions, Tensions, Papers (grouped by instrument/era)
**Key synthesis:** No atmospheric detections across b, c, d, e to date; three distinct contamination-mitigation strategies (explicit photospheric model, GP marginalization, empirical back-to-back correction); N₂-dominated secondary atmospheres remain consistent for d and e; stellar-model fidelity is the dominant bottleneck.

## [2026-04-28] ingest | 2021_Mugnai_GJ1132b
**Paper:** Mugnai, Modirrousta-Galian, Edwards, Changeat et al. 2021, AJ 161:284 — "ARES V: No Evidence For Molecular Absorption in the HST WFC3 Spectrum of GJ 1132 b" (doi:10.3847/1538-3881/abfc3)
**PDF renamed:** raw/papers/2021_Mugnai_GJ1132b.pdf
**Created:** wiki/papers/2021_Mugnai_GJ1132b.md, wiki/instruments/HST-WFC3.md (stub), wiki/codes/Iraclis.md (stub), wiki/codes/TauREX3.md (stub)
**Updated:** wiki/targets/GJ1132b.md (added pre-JWST HST context paragraph to Observations to date; added paper to See also; count 3→4), wiki/targets/GJ1132.md (added paper ref; count 3→4), wiki/papers/2023_May_GJ1132b.md (resolved 2 prose references "Mugnai et al. 2021" → [[2021_Mugnai_GJ1132b]]; added "(not yet ingested)" to Libby-Roberts 2022 reference for consistency), wiki/methods/transmission-spectroscopy.md, wiki/methods/atmospheric-retrievals.md, index.md
**Emphasis decisions (user-approved "go with preferred approaches"):**
- HST-WFC3 instrument stub created: first HST instrument in the wiki; relevant to GJ 1132 b pre-JWST history.
- Iraclis and TauREX3 code stubs created: Iraclis is the standard WFC3 pipeline (likely to appear in other HST-era papers); TauREX3 already referenced in 2024_Gressier_L98-59d (now linked).
- ExoTETHyS (limb-darkening), MultiNest (sampler), CASCADe (secondary pipeline) skipped: prose-only; single references; general-purpose tools.
- Species ruled out in frontmatter limited to H2O, CH4, CO2 (existing wiki species); CO, NH3, HCN mentioned in prose.
- No HST program stub: wiki programs section covers JWST programs only.
**Tension resolved:** [[GJ1132b]] — Swain et al. 2021 HCN/H₂ claim (not yet ingested) vs. featureless HST spectrum; [[2021_Mugnai_GJ1132b]] provides a fully cited wiki anchor for the pre-JWST featureless result that [[2023_May_GJ1132b]] and [[2025_Bennett_GJ1132b]] subsequently confirmed and extended with JWST data.
**Promotion candidacy:** [[GJ1132b]] now at 4 papers ([[2023_May_GJ1132b]], [[2025_Bennett_GJ1132b]], [[2024_Xue_GJ1132b]], [[2021_Mugnai_GJ1132b]]); [[GJ1132]] likewise at 4 papers. Both remain above the promotion threshold; not promoted per "never automatic" rule.

## [2026-04-28] ingest | 2025_Tusay_K2-22b
**Paper:** Tusay, Wright, Beatty, Desch, Colon et al. 2025, ApJL 987:L6 — "A Disintegrating Rocky World Shrouded in Dust and Gas: Mid-infrared Observations of K2-22 b Using JWST" (doi:10.3847/2041-8213/adf60f)
**PDF renamed:** raw/papers/2025_Tusay_K2-22b.pdf
**Created:** wiki/papers/2025_Tusay_K2-22b.md, wiki/targets/K2-22b.md (stub), wiki/targets/K2-22.md (stub), wiki/instruments/CHEOPS.md (stub), wiki/codes/Pegasus.md (stub), wiki/concepts/disintegrating-planet.md, wiki/species/NO.md, wiki/programs/JWST-GO-3315.md
**Updated:** wiki/instruments/JWST-MIRI.md (added paper ref; count 5→6), wiki/codes/Eureka.md (added paper ref; count 17→18), wiki/methods/transmission-spectroscopy.md, index.md
**Emphasis decisions (user-approved "go with preferred approaches"):**
- disintegrating-planet concept page created: a qualitatively new target class distinct from all prior wiki targets; warrants its own concept page linking to future papers.
- NO species stub created: tentative detection in the most significant transit epoch; first non-atmospheric species in the wiki.
- CHEOPS instrument stub created: simultaneous optical observations; likely to recur in MIRI/CHEOPS joint papers.
- Pegasus code stub created (brief): used as independent verification; may recur in future MIRI work.
- Chexoplanet, PIPE (CHEOPS packages) and Mie-scattering modeling tools skipped: prose-only; highly specialized to this paper.
- K2-22 stellar parameters marked as approximate from Sanchis-Ojeda et al. 2015 (not yet ingested).
- Tusay 2025 placed in transmission-spectroscopy method page with explicit note that the "spectrum" comes from dust/gas tails, not a retained atmosphere — distinguishing it from all prior entries.
- NO listed as species_tentative (not detected): the paper identifies a feature consistent with NO but the LRS spectral resolution (R≈17) prevents a definitive identification.

## [2026-04-27] ingest | 2025_Teske_TOI561b
**Paper:** Teske, Lustig-Yaeger, Ih, Kempton et al. 2025, ApJL 995:L39 — GO 3860 four NIRSpec G395H secondary eclipses of the USP super-Earth TOI-561 b; T_day = 1800–2150 K vs. bare-rock ~2950 K; first detection consistent with thick volatile-rich atmosphere on a dense rocky planet; challenges cosmic shoreline; ancient (~10 Gyr) thick-disk K-dwarf host
**PDF renamed:** raw/papers/2025_Teske_TOI561b.pdf
**Created:** wiki/papers/2025_Teske_TOI561b.md, wiki/targets/TOI-561b.md (stub), wiki/targets/TOI-561.md (stub), wiki/programs/JWST-GO-3860.md, wiki/codes/HyDRo.md, wiki/codes/GENESIS.md
**Updated:** wiki/instruments/JWST-NIRSpec.md, wiki/codes/Eureka.md, wiki/codes/ExoTiC-JEDI.md, wiki/methods/secondary-eclipse-spectroscopy.md, wiki/methods/atmospheric-retrievals.md, wiki/concepts/cosmic-shoreline.md, index.md
**Emphasis decisions (user-approved "go with preferred approaches"):**
- Detection characterized as thermodynamic (dayside cooling relative to bare-rock baseline), not a molecular spectral feature detection; no species_detected in frontmatter.
- High surface albedo remains an unexcluded alternative to thick atmosphere interpretation; explicitly noted in caveats.
- GENESIS and HyDRo stubs created: both specialized codes for hot rocky planet emission modeling; likely to recur in future Teske-type analyses.
- No phase-curve data available; heat redistribution inference is indirect; noted as key open question.

## [2026-04-27] ingest | 2026_Coy_HD3167b
**Paper:** Coy, Weiner Mansfield et al. 2026, ApJ (arXiv:2604.11911) — "An Atmosphere on the Ultra-Short Period super-Earth HD 3167 b"; JWST MIRI/LRS secondary eclipse 2025 June 25 under LAVA LAMPS (GO 4818); eclipse depth 38±11 ppm vs. 104±3 ppm bare-rock; R=0.57; ~5σ atmospheric evidence on the first true USP super-Earth (P<1 d) with such a result
**PDF renamed:** raw/papers/2026_Coy_HD3167b.pdf
**Created:** wiki/papers/2026_Coy_HD3167b.md, wiki/targets/HD3167b.md (stub), wiki/targets/HD3167.md (stub), wiki/programs/JWST-GO-4818.md, wiki/codes/FastChem.md
**Updated:** wiki/codes/SPARTA.md, wiki/codes/Eureka.md, wiki/codes/exoTEDRF.md, wiki/codes/GENESIS.md, wiki/codes/EXOFASTv2.md, wiki/instruments/JWST-MIRI.md, wiki/methods/secondary-eclipse-spectroscopy.md, wiki/concepts/cosmic-shoreline.md, index.md
**Emphasis decisions (user-approved "go with preferred approaches"):**
- Atmospheric detection is thermodynamic (R=0.57 eclipse deficit), not spectral-feature; no species_detected in frontmatter; high-albedo alternative not excluded.
- HD 3167 stellar Teff corrected from agent extraction error (~2500 K, implausible for a K dwarf) to ~5300 K, consistent with published Christiansen et al. 2017 characterization of HD 3167 as a K0 star.
- FastChem stub created (chemical equilibrium code used with GENESIS); MultiNest stub deferred to Roy-Perez ingest.

## [2026-04-27] ingest | 2026_RoyPerez_WASP39b
**Paper:** Roy-Perez et al. 2026, A&A 707:A297 (DOI: 10.1051/0004-6361/202558193) — "The effect of JWST/NIRSpec data reduction on the retrieval of WASP-39b atmospheric properties"; four pipelines / six reductions of the ERS 1366 PRISM transit (2022 July 10); retrieved abundances vary by up to 2 dex depending on pipeline choices; Na, K, H₂O, CO₂, CO, SO₂ confirmed; H₂S tentative
**PDF renamed:** raw/papers/2026_RoyPerez_WASP39b.pdf
**Created:** wiki/papers/2026_RoyPerez_WASP39b.md, wiki/targets/WASP-39b.md (stub), wiki/targets/WASP-39.md (stub), wiki/programs/JWST-ERS-1366.md, wiki/codes/PSG.md, wiki/codes/Tshirt.md, wiki/codes/MOPSMAP.md, wiki/codes/MultiNest.md, wiki/species/CO.md (stub), wiki/species/Na.md (stub), wiki/species/K.md (stub)
**Updated:** wiki/codes/FIREFLy.md, wiki/codes/Tiberius.md, wiki/codes/Eureka.md, wiki/instruments/JWST-NIRSpec.md, wiki/methods/atmospheric-retrievals.md, wiki/species/H2O.md, wiki/species/CO2.md, wiki/species/SO2.md, wiki/species/H2S.md, index.md
**Emphasis decisions (user-approved "go with preferred approaches"):**
- WASP-39b is a new hot Jupiter target in the wiki (only rocky/sub-Neptune targets prior to this); added to targets section without special treatment since the schema accommodates gas giants.
- Carter pipeline reduction mentioned in paper but not given a stub: insufficient information to establish whether "Carter" refers to a standalone named code vs. a custom Eureka!-based reduction by author Aarynn Carter.
- ExoTEP (used as a variant in Eureka!+ExoTEP) not given a separate stub: treated as a light-curve fitting module within the Eureka pipeline, not a standalone code.
- Species CO, Na, K stubs created: first appearances in the wiki; all confirmed across multiple pipelines in Roy-Perez.

## [2026-04-27] lint | full-pass
**Findings:** 2 orphans, 41 stub-promotion candidates (≥5 inbound links; 14 also ≥3 papers), 2 broken wiki-links, 0 frontmatter violations, 0 index/filesystem sync errors, several tag-hygiene issues including a singular/plural split (`atmospheric-retrieval` vs `atmospheric-retrievals`) and overlapping facility tags (`hst`, `hst-wfc3`, `wfc3`).
**Actions:** none — pending user review per item.

## [2026-04-27] lint | fixes-applied
**Orphans resolved (2):**
- wiki/papers/2025_Rathcke_TRAPPIST1bc.md: added body wiki-links for [[SPHINX]], [[speclib]], [[spotter]] in the Methods photospheric-modeling bullet (previously only in `codes:` frontmatter).
- wiki/papers/2025_Tusay_K2-22b.md: converted one prose "NO" mention to [[NO]] wiki-link in the Key Findings bullet.

**Broken wiki-links resolved (2):**
- wiki/papers/2024_Gressier_L98-59d.md: rewrote two `[[Exo-REM]]` references to plain prose with "(Baudino et al. 2015; not yet ingested)" annotation.
- wiki/papers/2023_May_GJ1132b.md: rewrote `[[HCN]]` to plain prose; HCN is not detected on any wiki target so a stub would be premature.

**Hub promotions (8):**
- wiki/codes/Eureka.md (57 inbound, 20 papers) — Variants, History, Trade-offs, Open issues, grouped Papers.
- wiki/instruments/JWST-NIRSpec.md (26 inbound, 19 papers) — Modes, History, Trade-offs, Open issues, Papers grouped by mode.
- wiki/concepts/stellar-contamination.md (17 inbound, 6 papers) — Mitigation strategies, History, Open questions, expanded Tensions, Papers.
- wiki/species/CO2.md (11 inbound, 8 papers) — Detection status (per target, with confirmed / ruled out / compatible categories), Open issues, Papers.
- wiki/species/CH4.md (11 inbound, 8 papers) — Detection status with the recurring "tentative → retired" pattern, Open issues, Papers.
- wiki/targets/GJ1132b.md (9 inbound, 5 papers) — Basic properties table, Atmospheric composition (all rule-outs), Observations to date, Open questions, resolved Tensions, Papers.
- wiki/methods/multi-visit-stacking.md (10 inbound, 8 papers) — Variants, Trade-offs, Open issues, Papers.
- wiki/codes/FIREFLy.md (20 inbound, 7 papers) — Variants, Trade-offs, Open issues, Papers.

**Tag hygiene (6 fixes):**
- wiki/codes/HyDRo.md: `atmospheric-retrieval` → `atmospheric-retrievals`.
- wiki/concepts/stellar-contamination.md: `systematic` → `systematics`.
- wiki/codes/Iraclis.md: `wfc3` → `hst-wfc3`.
- wiki/instruments/HST-WFC3.md: `hst` → `hst-wfc3`.
- wiki/programs/JWST-GTO-1274.md: removed over-specific `gj1132b` tag.
- wiki/papers/2025_Rathcke_TRAPPIST1bc.md: removed over-specific `jwst-go-2420` tag.

**Index updated:** added `(hub)` annotation to all 8 promoted pages.

**Deferred (lower-priority promotion candidates, ~33 remaining):** Tiberius (18/6), POSEIDON (17), PICASO (17/7), ExoTiC-JEDI (17/6), SPARTA (13/5), stellar-contamination-modeling (12/6), CHIMERA (11/5), and ~26 others at counts 5–9. Will revisit at next lint pass; lower-traffic hubs gain less from formal promotion until they accumulate more papers.

**Frontmatter / index sync / contradictions / remaining tag singletons:** no actions needed.

## [2026-04-29] ingest | 2025_Connors_MIRI-15um
**Paper:** Connors, Monaghan, Benneke, Dang 2025, ApJL 989:L11 (DOI: 10.3847/2041-8213/adee0d) — methodology + uniform reanalysis. Introduces frame-normalized principal component analysis (FN-PCA) for MIRI F1500W eclipse photometry; reanalyzes 17 published eclipses on 5 rocky planets (TRAPPIST-1 b/c, LHS 1478 b, TOI-1468 b, LHS 1140 c) and characterizes the MIRI 15 μm detector-settling timescale.
**PDF renamed:** raw/papers/2025_Connors_MIRI-15um.pdf
**Created:** wiki/papers/2025_Connors_MIRI-15um.md, wiki/targets/{LHS1478b,LHS1478,TOI-1468b,TOI-1468,LHS1140c,LHS1140}.md (stubs), wiki/programs/JWST-GO-3730.md, wiki/codes/Erebus.md
**Updated:** wiki/codes/{Eureka,SCARLET,SPHINX}.md, wiki/targets/{TRAPPIST-1b,TRAPPIST-1c,TRAPPIST-1}.md (hub), wiki/instruments/JWST-MIRI.md, wiki/methods/{secondary-eclipse-spectroscopy,multi-visit-stacking}.md, wiki/concepts/cosmic-shoreline.md, index.md
**Tension flagged:** [[TRAPPIST-1c]] — FN-PCA T_day = 344 +43/−52 K vs Zieba et al. 2023 (not yet ingested) 380 ± 31 K; ~1σ but consistently in the atmosphere-favoring direction.
**Emphasis decisions (user-approved "preferred approaches"):**
- 5 new target stubs created (3 planets + 3 hosts; LHS 1140 host shared with LHS 1140 b, the latter not stubbed since out of scope).
- JWST-GO-3730 stub (Hot Rocks Survey) created since 3 reanalyzed targets feed from it; original target-by-target Hot Rocks papers (August 2025, Valdés 2025, Fortune 2025) cited as "(not yet ingested)".
- GTO-1177 (Greene TRAPPIST-1 b) and GO-2304 (Zieba TRAPPIST-1 c) not stubbed — only mentioned in TRAPPIST-1 b/c target pages with original-paper "(not yet ingested)" annotations.
- JESTER (Monaghan et al., in prep) bare-rock surface modeling code not stubbed: in prep.
- 8 systematics-only targets in Connors Fig. 4/5 (GJ 3473 b, LTT 3780 b, etc.) not stubbed: paper uses them only for detector-settling characterization, not atmospheric analysis.

## [2026-04-29] ingest | 2025_LustigYaeger_WASP17b
**Paper:** Lustig-Yaeger, Sotzen, Stevenson, Tsai et al. 2025, arXiv:2510.06169 — JWST-TST DREAMS nightside emission and chemistry of WASP-17 b. Introduces iESR (in-Eclipse Spectrum Removal) PIE technique on a back-to-back NIRSpec G395H transit + secondary eclipse pair; first JWST nightside emission spectrum of a hot Jupiter. Tentative nightside SO₂ at 2.3σ; A_B = 0.42; recirculation f = 0.54.
**PDF renamed:** raw/papers/2025_LustigYaeger_WASP17b.pdf
**Created:** wiki/papers/2025_LustigYaeger_WASP17b.md, wiki/targets/{WASP-17b,WASP-17}.md (stubs; first F-dwarf host in wiki), wiki/programs/JWST-TST-GTO-1353.md, wiki/codes/VULCAN.md, wiki/methods/planetary-infrared-excess.md
**Updated:** wiki/codes/{Eureka,POSEIDON,MultiNest}.md, wiki/instruments/JWST-NIRSpec.md (hub), wiki/methods/{secondary-eclipse-spectroscopy,atmospheric-retrievals}.md, wiki/species/{H2O,SO2,CH4,CO2}.md, index.md
**Emphasis decisions:**
- New method page `planetary-infrared-excess.md` covers both PIE (general framework) and the iESR variant introduced here; Sotzen 2025 (HAT-P-26 b null result, not yet ingested) flagged as a method-applicability boundary case.
- Tentative species (SO₂, CH₄, H₂O, CO₂ all 0.9σ–2.3σ) listed in `species_tentative` rather than `species_detected` per the paper's conservative reporting under noise-floor inflation.
- VULCAN code stub created (photochemistry); the 2D Tsai 2024 variant cited in prose with "(not yet ingested)".

## [2026-04-29] ingest | 2025_Gressier_WASP17b
**Paper:** Gressier, MacDonald, Espinoza, Wakeford et al. 2025, AJ 169:57 (DOI: 10.3847/1538-3881/ad97bf) — JWST-TST DREAMS NIRISS/SOSS dayside secondary eclipse of WASP-17 b. H₂O detected at 6.4σ with supersolar abundance (3σ lower limit > 3× solar); non-inverted T–P profile; FeH tentative at 3σ; sub-1 μm brightness-temperature rise consistent with high T_int or reflected light. Companion to Lustig-Yaeger 2025 nightside paper.
**PDF renamed:** raw/papers/2025_Gressier_WASP17b.pdf
**Created:** wiki/papers/2025_Gressier_WASP17b.md, wiki/codes/{ATMO,Ahsoka}.md, wiki/species/FeH.md (stub)
**Updated:** wiki/codes/{transitspectroscopy,supreme-SPOON,juliet,POSEIDON,TauREX3,MultiNest}.md, wiki/instruments/JWST-NIRISS.md, wiki/methods/{secondary-eclipse-spectroscopy,atmospheric-retrievals}.md, wiki/species/H2O.md, wiki/targets/WASP-17b.md, wiki/programs/JWST-TST-GTO-1353.md, index.md
**Emphasis decisions:**
- Same first author as 2024_Gressier_L98-59d (Amélie Gressier, now at STScI); confirmed identity, no disambiguation needed.
- ATMO stub created: forward-model grid; will likely recur in hot-Jupiter retrievals.
- Ahsoka stub created (composite NIRISS pipeline introduced in this paper).
- FeH species stub created at 3σ tentative threshold; first wiki appearance.
- Wakeford 2025 panchromatic dayside, Grant 2023 MIRI/LRS clouds, and Louie 2024 NIRISS transmission cited in prose as "(not yet ingested)".

## [2026-04-29] ingest | 2026_Radica_WASP96b
**Paper:** Radica, Taylor, Rotman, Blecic, Welbanks, Ahrer, Christie, Coulombe, et al. 2026, arXiv:2604.05049 — new JWST NIRSpec G395H + archival NIRISS/SOSS + VLT/FORS2 panchromatic transit of WASP-96 b. H₂O, CO₂, Na detected; tentative SO₂ at lnB=2.69; super-stellar metallicity (~2–6× stellar); near-stellar C/O. Places WASP-96 b on the proposed Crossfield+2025 SO₂ photochemical shoreline.
**PDF renamed:** raw/papers/2026_Radica_WASP96b.pdf
**Created:** wiki/papers/2026_Radica_WASP96b.md, wiki/targets/{WASP-96b,WASP-96}.md (stubs), wiki/programs/JWST-GO-4082.md, wiki/instruments/VLT-FORS2.md, wiki/codes/{PyratBay,NEMESISPY,Aurora,ScCHIMERA,Photochem}.md, wiki/concepts/SO2-photochemical-shoreline.md
**Updated:** wiki/codes/{Eureka,exoTEDRF,NAMELESS,POSEIDON,MultiNest,juliet,FastChem,CHIMERA}.md, wiki/instruments/JWST-NIRSpec.md (hub), wiki/instruments/JWST-NIRISS.md, wiki/methods/{transmission-spectroscopy,atmospheric-retrievals}.md, wiki/species/{H2O,CO2,Na,SO2}.md, wiki/papers/2024_Banerjee_L98-59d.md (NEMESISPY prose→wiki-link), index.md
**Tension flagged:** [[WASP-96b]] — sub-stellar (Wang et al. 2026 not yet ingested) vs. super-stellar (Radica) metallicity; reduction-pipeline and retrieval-prior choices both contribute.
**Emphasis decisions (user-approved "preferred approaches"):**
- Five new code stubs reflect the multi-pipeline cross-comparison style of this paper.
- VLT-FORS2 instrument stub: archival ground-based optical data is central to the Na detection; first non-JWST/non-HST instrument in the wiki.
- SO2-photochemical-shoreline concept stub created since the paper centrally invokes the framework; treats Crossfield et al. 2025 as the originating reference (not yet ingested).
- Wiki-linked the Banerjee 2024 NEMESISPY references that were prose-only (lint cleanup).

## [2026-04-29] ingest | 2026_Holmberg_GJ3473b
**Paper:** Holmberg, Diamond-Lowe, Mendonça, Kitzmann, Espinoza, Allen, August, Fortune, et al. 2026, arXiv:2604.02332 — Hot Rocks Survey V; four JWST MIRI F1500W secondary eclipses of GJ 3473 b; joint depth 186 ± 45 ppm; T_day = 820 ± 120 K; R = 0.82 ± 0.12. Both bare-rock and atmosphere consistent; thick CO₂ atmospheres excluded above 1.2–6.5 bar surface pressure (95% upper limit).
**PDF renamed:** raw/papers/2026_Holmberg_GJ3473b.pdf
**Created:** wiki/papers/2026_Holmberg_GJ3473b.md, wiki/targets/{GJ3473b,GJ3473}.md (stubs), wiki/codes/JExoRES.md
**Updated:** wiki/programs/JWST-GO-3730.md (PI corrected from "P. C. August" to "H. Diamond-Lowe" per the Holmberg paper itself), wiki/codes/{HELIOS,SPHINX,MultiNest}.md, wiki/instruments/JWST-MIRI.md, wiki/methods/{secondary-eclipse-spectroscopy,multi-visit-stacking}.md, index.md
**Schema correction:** [[JWST-GO-3730]] PI updated. Connors 2025 had attributed the Hot Rocks Survey GO-3730 to P. C. August (likely confused with paper I lead author August); Holmberg as paper V identifies PI as H. Diamond-Lowe with Co-PI J. M. Mendonça.
**Emphasis decisions:**
- No alternate-pipeline cross-check exists in this paper (JExoRES is the sole reduction); flagged in caveats.
- The four series companion papers (August 2025, Meier Valdés 2025, Fortune 2025, Allen 2025) cited as "(not yet ingested)" — could be ingested independently if the user provides PDFs.

## [2026-04-29] ingest | 2026_Heinke_HATP12b
**Paper:** Heinke, Min, Bouwman, Crouzet, Konings, Decin, Waters, Lagage, et al. 2026, A&A submitted (arXiv:2604.01219) — panchromatic 0.36–12.4 μm JWST NIRISS+NIRSpec G395M+MIRI/LRS combined with HST STIS+WFC3 transit of HAT-P-12 b. H₂O (>12σ), CO₂ (>10σ), CO (~8σ), H₂S (~3.7σ TEATRO) detected; metallicity 11–15× solar in multi-instrument retrievals; non-gray cloud preferred at >7.5σ when NIRISS is included. Information-content study quantifies what each instrument contributes via Bayesian Δln Z.
**PDF renamed:** raw/papers/2026_Heinke_HATP12b.pdf
**Created:** wiki/papers/2026_Heinke_HATP12b.md, wiki/targets/{HAT-P-12b,HAT-P-12}.md (stubs), wiki/programs/JWST-GTO-1281.md, wiki/instruments/HST-STIS.md, wiki/codes/{ARCiS,CASCADe,TEATRO,spotrod}.md, wiki/methods/information-content-analysis.md
**Updated:** wiki/codes/{exoTEDRF,juliet,MultiNest}.md, wiki/instruments/{JWST-NIRSpec,JWST-NIRISS,JWST-MIRI,HST-WFC3}.md, wiki/methods/{transmission-spectroscopy,atmospheric-retrievals}.md, wiki/species/{H2O,CO2,CO,H2S}.md, index.md
**Emphasis decisions:**
- New method page `information-content-analysis.md` covers the Bayesian leave-one-out instrument-attribution framework.
- spotrod stub created for the HAT-P-12 b possible spot-crossing fit (also serves the upcoming Ashtari ingest).
- Decision to give CASCADe and TEATRO separate stubs since the C/O conclusion shifts between them — exemplifying pipeline-driven systematics in line with [[2026_RoyPerez_WASP39b]].
- Companion Bouwman et al. (in prep) MIRI-LRS detailed analysis cited as "(not yet ingested)".

## [2026-04-29] ingest | 2026_Ashtari_HATS75b
**Paper:** Ashtari, Lustig-Yaeger, Libby-Roberts, Müller, Kanodia, Stevenson, Cañas, Guzmán Caloca, et al. 2026, AJ accepted (arXiv:2604.07268) — first wiki paper on a Giant Exoplanet around an M-dwarf Star (GEMS): three JWST NIRSpec PRISM transits of HATS-75 b. CH₄, CO, CO₂ detected at >3σ in a TLS framework; H₂O upper limit only (likely masked by spots). Atmospheric metallicity log [M/H] = −1.74 (sub-solar, ~1% solar) but bulk planetary metallicity Z_p ≈ 0.20 — implies inefficient vertical mixing.
**PDF renamed:** raw/papers/2026_Ashtari_HATS75b.pdf
**Created:** wiki/papers/2026_Ashtari_HATS75b.md, wiki/targets/{HATS-75b,HATS-75}.md (stubs), wiki/programs/JWST-GO-3171.md, wiki/codes/fleck.md, wiki/concepts/GEMS.md
**Updated:** wiki/codes/{Eureka,POSEIDON,MultiNest,spotrod}.md, wiki/instruments/JWST-NIRSpec.md (hub), wiki/methods/{transmission-spectroscopy,atmospheric-retrievals,multi-visit-stacking,stellar-contamination-modeling}.md, wiki/concepts/stellar-contamination.md (hub), wiki/species/{CH4,CO,CO2}.md, index.md
**Emphasis decisions:**
- New concept page `GEMS.md` introduces the class label since this is the first such target in the wiki.
- HATS-75 b classified as `class: gas-giant` per CLAUDE.md taxonomy; mass_mjup/radius_rjup units used.
- Detected species listed in `species_detected` despite the fundamental TLS/atmosphere degeneracy because the TLS framework is preferred by independent stellar-activity evidence and reproducible across both reduction pipelines.
- Bulk-vs-atmospheric metallicity tension flagged in target page open-questions and paper Tensions.
- fleck stub created: spot-modeling code likely to recur in future M-dwarf-host papers.

## [2026-04-29] note | scope decision: 2026_Ravet_COCONUTS2b skipped
**Paper not ingested.** Ravet et al. 2026, A&A accepted — directly imaged spectroscopy of the wide-orbit (~7500 au) planetary-mass companion COCONUTS-2 b. Per CLAUDE.md scope ("transmission, with emission included when [it] bear[s] directly on the same targets or questions"), this paper is out of scope: COCONUTS-2 b has no transit observations and no overlap with any current wiki target; the observing technique (spatially resolved spectro-photometry of a wide-orbit companion) is closer to brown-dwarf characterization than to transit/eclipse spectroscopy. Cool-giant chemistry (CH₄, NH₃, PH₃, K_zz) is methodologically related but no transmission paper currently in the wiki probes this regime. The PDF is left unrenamed in `raw/papers/` to clearly signal "not ingested" status. **User can override:** rerun the ingest with explicit instruction if cool-giant atmospheric chemistry becomes in-scope.

## [2026-04-29] schema | added optional `species_predicted` frontmatter field for theory papers
**Reason:** Theory papers like Seager & Sasselov 2000 and Brown 2001 make species-specific predictions but make no detections. The existing optional fields (`species_detected`, `species_tentative`, `species_ruled_out`) all carry observational connotations. `species_predicted` cleanly captures "this paper computed predicted feature depths for these species" without conflating with detection status.
**Status:** Optional, theory-paper-specific. Not a required field. Leave unset for observational papers. Existing pages need no migration.

## [2026-04-29] ingest | 2000_Seager_TheoryTransmission
**Paper:** Seager & Sasselov 2000, ApJ 537:916 (DOI: 10.1086/309088) — foundational theory paper. First quantitative predictions for transmission spectroscopy of close-in extrasolar giant planets, computed for HD 209458 b. Na I D doublet at 589.4 nm identified as the strongest expected feature; K I and metastable He I 1083 nm also predicted. Geometric framework (limb tangential rays through cloud-top atmosphere) established the foundation for every subsequent transmission paper.
**PDF renamed:** raw/papers/2000_Seager_TheoryTransmission.pdf
**Created:** wiki/papers/2000_Seager_TheoryTransmission.md, wiki/targets/{HD-209458b,HD-209458}.md (stubs), wiki/species/He.md (stub)
**Updated:** wiki/methods/transmission-spectroscopy.md (added Foundational theory section), wiki/species/{Na,K}.md (foundational predictions added), index.md
**Emphasis decisions (user-approved "preferred approaches"):**
- Theory papers ingested with empty `instruments: []` and new optional `species_predicted` frontmatter field (see schema entry above).
- HD 209458 b — first non-JWST hot-Jupiter target in the wiki; tagged `pre-jwst` and `theoretical-archetype`. No JWST observation ingested for HD 209458 b yet, so the target page documents only the theoretical predictions.
- Charbonneau et al. 2002 (HST/STIS Na I first detection) cited as "(not yet ingested)" throughout — would close the loop if/when added.
- He species stub created (first noble-gas / atomic-helium entry); reflects the metastable 1083 nm prediction.

## [2026-04-29] ingest | 2001_Brown_TransmissionDiagnostics
**Paper:** Brown 2001, ApJ 553:1006 (DOI: 10.1086/320950) — foundational theory paper. Introduces the formal "spectrum ratio" R(λ) = F_transit/F_out as the natural transmission observable; adds parameterized cloud decks, Doppler diagnostics from height-dependent winds and planetary rotation, Na/K UV photoionization, refraction, and a systematic diagnostic catalog (cloud height, metallicity, T(P), thermal inversions, winds). Predictions computed for HD 209458 b. Single author: T. M. Brown.
**PDF renamed:** raw/papers/2001_Brown_TransmissionDiagnostics.pdf
**Created:** wiki/papers/2001_Brown_TransmissionDiagnostics.md
**Updated:** wiki/concepts/transmission-spectrum.md (added Brown's spectrum-ratio framing as equivalent observable; foundational papers in Papers section), wiki/species/{Na,K,H2O,CO,CH4}.md (foundational predictions added), index.md
**Emphasis decisions:**
- No new target / host stubs needed (HD 209458 b/host already created in the Seager 2000 ingest).
- No code stub for Brown's bespoke forward model (single-paper ad hoc code; not a named or recurring tool).
- HIRES/NIRSPEC/NGST mentioned in Brown's feasibility analysis but not given instrument stubs (NGST → JWST is already covered; HIRES/NIRSPEC are ground-based facilities not central to any wiki paper's data).
- The companion-relationship between [[2000_Seager_TheoryTransmission]] and [[2001_Brown_TransmissionDiagnostics]] documented in both papers' Related sections; Brown 2001 builds substantially on Seager & Sasselov 2000 and is the source of the still-current "spectrum ratio" terminology and diagnostic catalog.

## [2026-04-29] query | "Rocky planets observed with JWST during both primary transit and secondary eclipse, with systematics."
**Answer filed as:** analyses/2026-04-29_rocky-planets-jwst-transit-and-eclipse.md
**Sources consulted:** 2023_May_GJ1132b, 2025_Bennett_GJ1132b, 2024_Xue_GJ1132b, 2023_Moran_GJ486b, 2024_WeinerMansfield_GJ486b, 2023_Lim_TRAPPIST1b, 2025_Rathcke_TRAPPIST1bc, 2025_Connors_MIRI-15um
**Result:** Four rocky planets qualify — GJ 1132 b, GJ 486 b, TRAPPIST-1 b, TRAPPIST-1 c. GJ 486 b is the cleanest "emission-breaks-transmission-degeneracy" case in the wiki. Notable systematics catalogued: NRS2 superbias offsets (GJ 486 b → GJ 1132 b → multiple G395H targets), spots/faculae alternation between visits (TRAPPIST-1 b), spot rotation between visits (GJ 1132 b), Connors 2025 FN-PCA reanalysis cooling on TRAPPIST-1 c (potential tension with Zieba 2023), single-band F1500W's inability to break atmosphere-vs-high-albedo degeneracy.

## [2026-05-03] ingest | 2025_Crouzet_HATP12b
**Paper:** Crouzet, Edwards, Konings, Bouwman, Min, Lagage, Waters, Pye, et al. 2025, A&A 703:A264 (DOI: 10.1051/0004-6361/202450690) — foundational JWST NIRSpec G395M transmission paper for HAT-P-12 b under [[JWST-GTO-1281]]; combines a single 6.34-h transit (2023 Feb 11–12) with two archival HST WFC3 G141 transits. CO₂ at 12.2σ, H₂O at 6.0σ, CO at 4.1σ; H₂S marginal in CASCADe (3.2σ) only. Metallicity ~10× solar with photochemistry, ~60× without.
**PDF renamed:** raw/papers/2025_Crouzet_HATP12b.pdf
**Created:** wiki/papers/2025_Crouzet_HATP12b.md
**Updated:** wiki/targets/HAT-P-12b.md (substantial rewrite into atmosphere-composition + tensions hub-style), wiki/programs/JWST-GTO-1281.md, wiki/codes/{ARCiS,CASCADe,TEATRO,TauREX3,VULCAN,MultiNest,petitRADTRANS}.md, wiki/species/{H2O,CO2,CO,H2S}.md, index.md
**Tension flagged:** [[HAT-P-12b]] — metallicity 10× vs 60× solar depending on whether photochemistry is included in ARCiS (methodological tension explicitly highlighted by the paper); CASCADe vs TEATRO disagreement on H₂S detection significance.
**Emphasis decisions (user-approved "preferred approaches"):**
- Crouzet 2025 is treated as the foundational NIRSpec G395M paper for HAT-P-12 b — Heinke 2026 is the panchromatic follow-up that builds on this. HAT-P-12 b target page was rewritten into hub-style with cross-paper consensus on detected species.
- No new code stubs needed (ARCiS, CASCADe, TEATRO, VULCAN, petitRADTRANS, MultiNest, TauREX3 all exist from prior ingests).

## [2026-05-03] ingest | 2025_Howard_TRAPPIST1_flares
**Paper:** Howard, Kowalski, Radica, Flagg, Vasilyev, Rackham, Tovar Mendoza, MacGregor, et al. 2025, arXiv:2512.04265 — methodology paper introducing both empirical and [[RADYN]] physics-based flare-mitigation pipelines for JWST NIR transmission spectroscopy. Six >10³⁰ erg flares characterized on TRAPPIST-1 from 11 visits across [[JWST-GO-2589]] (Lim) and [[JWST-GTO-1201]] (Lafrenière). Residual transit-spectrum noise drops to 54 ± 14 ppm (empirical) or 65 ± 17 ppm (RADYN); injection-recovery 3σ CO₂ feature detection at 150–250 ppm post-mitigation.
**PDF renamed:** raw/papers/2025_Howard_TRAPPIST1_flares.pdf
**Created:** wiki/papers/2025_Howard_TRAPPIST1_flares.md, wiki/targets/{TRAPPIST-1f,TRAPPIST-1g}.md (stubs — first wiki characterization), wiki/codes/{RADYN,llamaradas-estelares}.md, wiki/methods/flare-mitigation.md
**Updated:** wiki/targets/TRAPPIST-1.md (hub; added MIRI methodology section), wiki/programs/{JWST-GO-2589,JWST-GTO-1201}.md, wiki/codes/exoTEDRF.md, wiki/concepts/stellar-contamination.md (hub; added flare-mitigation as fourth strategy), index.md
**Emphasis decisions:**
- New `flare-mitigation.md` method page distinct from existing `stellar-contamination-modeling.md`: flares are stochastic per-visit phenomena requiring a different mitigation paradigm than stable spot/facula modeling.
- TRAPPIST-1 f and g get target stubs even though Howard 2025 makes no atmospheric claim — they are first-time JWST characterizations (flare-monitoring) and likely future-paper anchors.
- Did **not** create stubs for batman (very widely used; minor) or PHOENIX (stellar models; minor).

## [2026-05-03] ingest | 2025_AcunaAguirre_WASP80b
**Paper:** Acuña-Aguirre, Kreidberg, Mollière, Bachmann 2025, A&A submitted (arXiv:2511.13483) — joint interior + atmosphere Bayesian retrieval on WASP-80 b panchromatic HST + JWST data (HST/STIS+WFC3, JWST/NIRCam transmission and emission, JWST/MIRI/LRS emission). Couples [[GASTLI]] (interior) with [[petitRADTRANS]] (atmosphere) into a single likelihood. Two fiducial scenarios: secular-cooling (Z_p = 0.12 ± 0.02; M/H = 2.75× solar) or additionally-heated (Z_p = 0.28 ± 0.11; M/H = 10× solar). Both prefer sub-solar C/O.
**PDF renamed:** raw/papers/2025_AcunaAguirre_WASP80b.pdf
**Created:** wiki/papers/2025_AcunaAguirre_WASP80b.md, wiki/targets/{WASP-80b,WASP-80}.md (stubs; first wiki characterization), wiki/codes/{GASTLI,easyCHEM}.md, wiki/instruments/JWST-NIRCam.md, wiki/methods/joint-interior-atmosphere-retrieval.md
**Updated:** wiki/codes/{petitRADTRANS,MultiNest}.md, wiki/species/{H2O,CH4,CO,CO2}.md, index.md
**Emphasis decisions:**
- Created `joint-interior-atmosphere-retrieval.md` as a new method page — methodologically distinct from atmospheric-retrievals; explicitly applicable to the [[2026_Ashtari_HATS75b]] bulk-vs-atmospheric metallicity tension as future work.
- Created JWST-NIRCam instrument stub (first wiki appearance of this mode).
- WASP-80 b uses datasets from Bell et al. 2023, Wiser et al. 2025, Jacobs et al. 2023, Wong et al. 2022 — all cited as "(not yet ingested)". Wilkinson et al. 2024 (the joint-retrieval predecessor on WASP-39 b) also "(not yet ingested)".

## [2026-05-03] ingest | 2025_Roy_LP791-18c
**Paper:** Roy, Benneke, Fournier-Tondreau, Coulombe, Piaulet-Ghorayeb, Lafrenière, Allart, Cowan, et al. 2025, Nature Astronomy (DOI: 10.1038/s41550-025-02723-3) — JWST NIRSpec PRISM transmission spectrum of the temperate sub-Neptune LP 791-18 c (T_eq ≈ 355 K) under [[JWST-GTO-1201]]. Strong Rayleigh-scattering haze (5.4σ) + CH₄ (4.5σ) + **no CO₂** (CH₄/CO₂ > 12 at 2σ); 250–400× solar metallicity; comparative discussion frames an intrinsic atmospheric **diversity** in temperate sub-Neptunes (LP 791-18 c vs K2-18 b vs TOI-270 d).
**PDF renamed:** raw/papers/2025_Roy_LP791-18c.pdf
**Created:** wiki/papers/2025_Roy_LP791-18c.md, wiki/targets/{LP-791-18c,LP-791-18,K2-18b,K2-18,TOI-270d,TOI-270}.md (stubs)
**Updated:** wiki/programs/JWST-GTO-1201.md, wiki/codes/{Eureka,exoTEDRF,SCARLET,VULCAN,spotrod}.md, wiki/species/{CH4,CO2}.md, index.md
**Emphasis decisions:**
- Bibkey choice: `2025_Roy_LP791-18c` (single-target framing per agent recommendation) over `2025_Roy_subNeptunes` — the paper's primary observation is LP 791-18 c; comparative material is in Discussion.
- Created K2-18 b/host and TOI-270 d/host stubs as comparative references (no JWST observation directly ingested in wiki); flagged K2-18 b's DMS / Hycean controversy prominently in its stub.
- Did not create stubs for ruled-out haze precursors (HCN, C₂H₂, C₂H₄, C₂H₆, SO₂, SO) — listed in `species_ruled_out:` only.

## [2026-05-03] ingest | 2025_Gordon_COMPASS-G395H
**Paper:** Gordon, Batalha (N. M.), Batalha (N. E.), Aguichine, Gagnebin, Kirk, Lopez-Morales, Meech, Scarsdale, Teske, Wallack, Wogan 2025, arXiv:2511.18196 — uniform [[ExoTiC-JEDI]] reanalysis of the first seven [[JWST-GO-2512-COMPASS]] NIRSpec G395H transmission spectra ([[GJ357b]], [[TOI-836b]], [[TOI-836c]], [[TOI-776b]], [[TOI-776c]], [[L98-59c]], [[L168-9b]]). Introduces the **RPF-PCA systematics model** (PCA of relative pixel fluxes, fit as a 6-vector basis) — strongly preferred for low-groups-per-integration observations. PandExo under-prediction quantified; NRS1/NRS2 detector-offset statistics characterized.
**PDF renamed:** raw/papers/2025_Gordon_COMPASS-G395H.pdf
**Created:** wiki/papers/2025_Gordon_COMPASS-G395H.md, wiki/targets/TOI-836c.md (stub — first wiki characterization)
**Updated:** wiki/programs/JWST-GO-2512-COMPASS.md, wiki/codes/{ExoTiC-JEDI,PICASO,Photochem,easyCHEM,petitRADTRANS}.md, wiki/targets/{TOI-836b,TOI-776b,TOI-776c,GJ357b,L98-59c,L168-9b}.md (added Gordon as second paper to See also), index.md
**Emphasis decisions:**
- Only one new target stub created: [[TOI-836c]] (the seven targets in this paper include five already in wiki + TOI-836 c + L 168-9 b which already had a stub).
- `data-reduction-systematics` not promoted to a method page yet — Gordon 2025 joins [[2025_Connors_MIRI-15um]] and [[2026_RoyPerez_WASP39b]] as the third pillar of the systematics theme; promotion candidate at next lint pass.

## [2026-05-03] lint | full-pass
**Findings:** 2 orphans (information-content-analysis, llamaradas-estelares), 1 real broken link ([[Rocky-Worlds-DDT]] in 2025_Connors_MIRI-15um.md), 0 frontmatter violations, 0 index/filesystem mismatches, 132 singleton tags (cleanup deferred), 57 promotion candidates above threshold.
**Actions:** None on orphans/broken-links/tags pending user approval.

## [2026-05-03] schema | promoted 7 candidate hubs to hub-template pages
**Promoted:** [[H2O]] (species), [[transmission-spectroscopy]] (method), [[atmospheric-retrievals]] (method), [[stellar-contamination-modeling]] (method), [[JWST-MIRI]] (instrument), [[POSEIDON]] (code), [[JWST-GO-2512-COMPASS]] (program).
**Updated:** wiki/species/H2O.md, wiki/methods/{transmission-spectroscopy,atmospheric-retrievals,stellar-contamination-modeling}.md, wiki/instruments/JWST-MIRI.md, wiki/codes/POSEIDON.md, wiki/programs/JWST-GO-2512-COMPASS.md, index.md (added `(hub)` markers).
**Promotion candidacy (deferred — still over threshold, awaits user approval):** [[PICASO]] (14/8), [[juliet]] (8/8), [[ExoTiC-JEDI]] (10/7), [[MultiNest]] (9/7), [[exoTEDRF]] (11/6), [[transitspectroscopy]] (9/6), [[Tiberius]] (8/6), [[JWST-NIRISS]] (7/6), [[SO2]] (14/5), [[CO]] (9/5), [[cosmic-shoreline]] (8/5), [[CHIMERA]] (7/5), [[SPARTA]] (7/5), [[JWST-GTO-1201]] (9/4), [[TRAPPIST-1b]] (9/4), [[L98-59c]] (8/4), [[petitRADTRANS]] (8/4), [[TauREX3]] (7/4), [[VULCAN]] (7/4), [[SCARLET]] (6/4), [[JWST-GO-1981-CHAMPs]] (5/4), [[HST-WFC3]] (4/4), and ~30 more at threshold (≥5 inbound or ≥3 papers). Counts shown as inbound/papers.
**Emphasis decisions:**
- Hub structure varies by type per CLAUDE.md: species/concept hubs lead with `## Detection status` or equivalent + `## History` + `## Open issues`; method hubs use `## Variants` + `## Trade-offs` + `## Open issues`; instrument and program hubs add `## History` and a structured papers section grouped by mode/era.
- Paper sections are structured (era / instrument / planet class) rather than flat lists where the page has ≥10 papers.
- Cross-hub links surfaced: H2O ↔ stellar-contamination-modeling ↔ atmospheric-retrievals ↔ JWST-MIRI ↔ JWST-GO-2512-COMPASS form an internally consistent network on the small-planet bare-rock-vs-atmosphere thread.
- The seven foundational candidates were promoted as a coherent batch (per user direction) rather than one-at-a-time; future ingests can extend rather than rewrite these hubs.

## [2026-05-03] query | "What do we know about terrestrial planets so far?"
**Answer filed as:** analyses/2026-05-03_terrestrial-planets-state-of-the-field.md
**Sources consulted:** 29 papers covering 24 terrestrial planets across 17 M-dwarf and 4 K-dwarf hosts; the [[cosmic-shoreline]], [[stellar-contamination]], [[multi-visit-stacking]] hubs and the [[TRAPPIST-1]] / [[GJ1132b]] target hubs.
**Updated:** index.md (added analysis to Analyses section, count now 2).
**Synthesis structure:**
- Catalogue by result class: 6 emission-confirmed bare rocks, 2 transmission-strong bare rocks, 8 featureless-transmission-only, 5 inconclusive single-band F1500W cases, 3 tentative positive detections (TOI-561 b, HD 3167 b, L 98-59 d), plus the disintegrating K2-22 b.
- Methodological framework: multi-visit floor, emission as arbiter, four stellar-contamination strategies, stellar-model fidelity bottleneck, NRS1/NRS2 detector offsets.
- Surprises: USP K-dwarf atmosphere candidates challenging cosmic shoreline (TOI-561 b, HD 3167 b); sulfur volcanism on tidally heated L 98-59 d; K2-22 b interior-composition probe via dust.
- Cosmic-shoreline picture: airless-side anchors solid; three challengers; demographic-survey phase via Connors 2025 + Hot Rocks + LAVA LAMPS.
**Defects flagged (non-actionable in this query):**
- wiki/targets/TRAPPIST-1.md line 12 contains a stray "What pa" between frontmatter and H1 — apparent partial-typed query saved by accident; should be removed in next lint or by user.

## [2026-05-03] ingest | 2025_Gressier_HATP26b
**Paper:** Gressier, Batalha (N. E.), Wogan, Alderson, Doud, Espinoza, MacDonald, Wakeford, Valenti, Lewis, Seager, Stevenson, et al. 2025, AJ 170:292 (DOI: 10.3847/1538-3881/ae0929) — JWST-TST DREAMS NIRSpec G395H transmission spectrum of warm Neptune-mass HAT-P-26 b under [[JWST-TST-GTO-1312]]. SO₂ at lnB = 13.46 (≥5σ; first SO₂ in a Neptune-mass exoplanet), CO₂ at lnB = 85.64, H₂O at lnB = 4.06; tentative H₂S ~2σ; CO ruled out at 3σ. ~10× solar metallicity, sub-solar C/O = 0.14. Population reanalysis of 11 JWST giant-planet transmission spectra empirically validates Crossfield 2023 SO₂–metallicity trend; WASP-107 b 7σ outlier flagged.
**PDF renamed:** raw/papers/2025_Gressier_HATP26b.pdf
**Created:** wiki/papers/2025_Gressier_HATP26b.md, wiki/targets/{HAT-P-26b,HAT-P-26}.md (stubs — first wiki characterization), wiki/programs/JWST-TST-GTO-1312.md
**Updated:** wiki/concepts/SO2-photochemical-shoreline.md (substantial rewrite — Crossfield 2023 prediction now empirically tested across 11 planets; WASP-107 b outlier flagged), wiki/species/{SO2,CO2,H2O,H2S}.md, wiki/codes/{transitspectroscopy,ExoTiC-JEDI,TauREX3,POSEIDON,PICASO,Photochem,MultiNest,juliet}.md, wiki/instruments/JWST-NIRSpec.md, wiki/methods/{atmospheric-retrievals,transmission-spectroscopy,stellar-contamination-modeling}.md, index.md (target count 66→68, program count 21→22, paper count 42→43, H2S 4→5 papers).
**Tension flagged:** [[SO2-photochemical-shoreline]] — WASP-107 b 7σ below Crossfield 2023 trend (constraint from a single G395H reanalysis, Sing et al. 2024 not yet ingested; combined NIRSpec + NIRCam + MIRI retrieval pending).
**Emphasis decisions (preferred approaches, no user pause):**
- Bibkey `2025_Gressier_HATP26b` follows the standard convention; same first author as `2025_Gressier_WASP17b` and `2024_Gressier_L98-59d` — disambiguated by target slug.
- Class for HAT-P-26 b chosen as `neptune` (mass_mjup = 0.0585, radius_rjup = 0.565) per the wiki's mass-class table; Neptune-mass with super-Neptune radius is borderline gas-giant by radius alone but mass governs the unit convention.
- New JWST-TST-GTO-1312 program stub created — distinct from JWST-TST-GTO-1331 (TRAPPIST-1 DREAMS) and JWST-TST-GTO-1353 (WASP-17 b DREAMS); PI N. Lewis, Warm Neptune class.
- Substantive rewrite of [[SO2-photochemical-shoreline]] rather than a single-bullet append: the Gressier paper transforms the page from "Crossfield prediction + 1 tentative target" into "11-planet empirical population test with one outlier"; this reframing was the central contribution and warrants the structural change.
- H₂S given a tentative-only entry (frontmatter `species_tentative`); the 2σ posterior peak with 3σ upper limit is below the wiki's normal "detection" threshold and the band overlaps H₂O.
- Did not create stubs for: GJ 3470 b (Beatty 2024 not yet ingested; comparator only), HD 189733 b (HST-era + JWST cited but not ingested), HIP 67522 b, WASP-107 b, WASP-121 b, WASP-127 b (population-test sample only — none with their own JWST paper here yet), pysynphot, MUSCLES, celerite, batman (sub-component dependencies).
- Did not stub Crossfield 2023 (ApJL 952:L18) as a paper page — it's the foundational prediction but not a JWST observation; cited via the [[SO2-photochemical-shoreline]] concept page with the "(not yet ingested)" suffix per § Referencing not-yet-ingested papers.

## [2026-05-03] ingest | 2025_Ahrer_KELT7b
**Paper:** Ahrer, Fairman, Kirk, Wakeford, Barstow, Penzlin, Alderson, Booth, Christie, Claringbold, Esparza-Borges, Gascón, López-Morales, Meech, Mayne, McCormack, Mollière, Owen, Panwar, Sergeev, Valentine, Wheatley, Zamyatina 2025, MNRAS 543:2442 — JWST NIRSpec G395H transmission of aligned hot Jupiter KELT-7 b under BOWIE-ALIGN ([[JWST-GO-3838]]). Weak features: H₂O at Δ ln Z = 1.0–1.9 (~2–2.5σ), CO₂ at Δ ln Z = 0.9–1.5; CO not detected; high-T species (SiO, VO, TiO, AlO, SH) ruled out. Two competing scenarios: high cloud deck OR low-metallicity atmosphere; equilibrium chemistry preferred at Δ ln Z = 1.6–3.1. C/O = 0.43–0.74; metallicity 1–16× solar.
**PDF renamed:** raw/papers/2025_Ahrer_KELT7b.pdf
**Created:** wiki/papers/2025_Ahrer_KELT7b.md, wiki/targets/{KELT-7b,KELT-7}.md (stubs — first wiki characterization), wiki/programs/JWST-GO-3838.md (BOWIE-ALIGN program stub)
**Updated:** wiki/codes/{Eureka,ExoTiC-JEDI,Tiberius,petitRADTRANS,POSEIDON,NEMESISPY,easyCHEM,MultiNest}.md, wiki/species/{H2O,CO2,CO}.md, wiki/instruments/JWST-NIRSpec.md, wiki/methods/{atmospheric-retrievals,transmission-spectroscopy}.md, index.md (target count 68→70, program count 22→23, paper count 43→44)
**Emphasis decisions (preferred approaches, no user pause):**
- Bibkey `2025_Ahrer_KELT7b` follows the standard convention.
- Class for KELT-7 b: `gas-giant` (mass_mjup = 1.39, radius_rjup = 1.60); standard hot Jupiter.
- KELT-7 host stub class: `F` (T_eff = 6768 K, F2 spectral type) — first F-dwarf host besides [[WASP-17]] (F6V); justifies expanding F-dwarf demographic in future synthesis.
- New BOWIE-ALIGN program stub (JWST-GO-3838); included WASP-15 b and TrES-4 b as "(not yet ingested)" prose references per the schema § Referencing not-yet-ingested papers — both are foundational BOWIE-ALIGN papers (Kirk 2025, Meech 2025) that the user is likely to want ingested next.
- Frontmatter `species_detected: []` — no firm detections; H₂O and CO₂ go in `species_tentative` despite being above some Sellke 2σ thresholds because the Bayes factors hover at Δ ln Z = 1–2 and the authors explicitly frame them as "weak/tentative."
- Did NOT create stubs for: H⁻ (continuum opacity, no real species page yet; foundational HST inference now contested), VO/TiO/AlO/SiO/SH high-T species (ruled out as physically unrealistic in this paper; not a detection).
- Did NOT create stub for the spelunker tool (FGS guide-star data analysis; trace dependency).
- Mirror tilt event handling not abstracted into a method/concept page yet — second wiki paper to document one (after Alderson 2023 WASP-39 b not yet directly ingested but referenced via [[2026_RoyPerez_WASP39b]]); promotion candidate when 3+ papers document it.
- Stellar contamination: no formal TLSE retrieval performed (F-star above Kraft break); standard reasoning followed.

## [2026-05-03] ingest | 2025_Felix_TOI-270d
**Paper:** Felix, Kitzmann, Demory, Mordasini 2025, A&A 701:A296 (DOI: 10.1051/0004-6361/202555194) — independent reanalysis of JWST [[JWST-GO-4098]] NIRSpec G395H + NIRISS SOSS transits of the temperate sub-Neptune TOI-270 d using Eureka! + custom MCMC + the [[BeAR]] retrieval framework at native instrument resolution with LSF convolution. **Reproduces** Benneke et al. 2024 (not ingested) — H₂/He miscible-envelope atmosphere with MMW = 5.56 amu, [M/H] ~160× solar, T = 360 K — but **cannot reproduce** Holmberg & Madhusudhan 2024 (not ingested) hycean fit (MMW ~2 amu, [M/H] ~10× solar). CH₄ decisive (Bayes factor 3 × 10²⁵), CO₂ decisive (3 × 10⁷), tentative CS₂ (78), weak NH₃ (4); H₂O surprisingly low (~10⁻⁴, condensation hypothesized); SO₂ ruled out at 3σ — retracts Benneke et al. 2024 SO₂ inference. CS₂ at 4.6 μm is degenerate with CH₃Cl, CH₃F, H₂CS — distinguishability requires MIRI 8–14 μm. Methodological argument: native-resolution + LSF retrieval is essential; binning to ≤16 px biases Bayes factors by orders of magnitude.
**PDF renamed:** raw/papers/2025_Felix_TOI-270d.pdf
**Created:** wiki/papers/2025_Felix_TOI-270d.md, wiki/programs/JWST-GO-4098.md, wiki/codes/{BeAR,HELIOS-K}.md, wiki/species/{CS2,NH3}.md
**Updated:** wiki/targets/TOI-270d.md (substantial expansion from stub; added properties, atmospheric composition, observations, tensions sections), wiki/codes/{Eureka,MultiNest}.md, wiki/instruments/{JWST-NIRSpec,JWST-NIRISS}.md, wiki/methods/{atmospheric-retrievals,transmission-spectroscopy}.md, wiki/species/{CH4,CO2,SO2,CO,H2O}.md, index.md (target unchanged at 70; species 12→14, codes 53→55, programs 23→24, papers 44→45)
**Tension flagged:** [[TOI-270d]] — Felix et al. 2025 reduction reproduces Benneke 2024 (MMW = 5.56 amu) but cannot reproduce Holmberg & Madhusudhan 2024 (MMW ~2 amu, hycean) using same data. Independent third-party reduction sought.
**Tension flagged:** [[TOI-270d]] — SO₂ tentative inference in Benneke 2024 retracted at 3σ upper limit by Felix 2025 reanalysis. Sub-Neptune analog of WASP-39 b reduction-divergence concerns.
**Emphasis decisions (preferred approaches, no user pause):**
- Bibkey `2025_Felix_TOI-270d` follows the standard convention; retains the dash in TOI-270d slug per existing target-page filename.
- TOI-270 d target stub upgraded to a near-hub-style page (Atmospheric composition + Observations + Open questions + Tensions + See also) — Felix 2025 with three independent analyses on this target now warrants near-hub treatment, though formal hub promotion deferred per CLAUDE.md "never automatic" rule.
- New species stubs: [[CS2]] (carbon disulfide; first proposed for an exoplanet atmosphere) and [[NH3]] (ammonia; first wiki entry though appears tentatively in 3+ papers retroactively cited).
- Did **not** create stubs for CH₃Cl, CH₃F, H₂CS, OCS, SH, NS, (CH₃)₂S/DMS — only upper limits or degenerate detections; would clutter the species namespace; covered as prose on TOI-270 d page.
- Did **not** stub batman (BATMAN transit model dependency; trace), pastasoss (NIRISS trace tool; trace), MUSCLES (UV input).
- Created [[BeAR]] code stub (substantial — first wiki appearance; argues native-resolution methodology) and [[HELIOS-K]] (its opacity backend).
- Created [[JWST-GO-4098]] program stub (multi-instrument GO; PIs Benneke & Evans-Soma; first wiki ingest of a target from this program).
- Cited Benneke et al. 2024 and Holmberg & Madhusudhan 2024 in prose with "(not yet ingested)" suffix per § Referencing not-yet-ingested papers — both are foundational TOI-270 d papers that user will likely want ingested next.

## [2026-05-04] ingest | 2025_FernandezRodriguez_K2-18b
**Paper:** Fernández-Rodríguez, Morello, Tan, Pallé, Swain, Poultourtzidis, Biagini, Changeat, Jiang, Pozuelos, Amado 2025, A&A submitted (arXiv:2510.18098) — independent reanalysis of JWST [[JWST-GO-2722]] NIRISS/SOSS + NIRSpec G395H transits of habitable-zone sub-Neptune K2-18 b. Reductions: [[exoTEDRF]] (NIRISS) + [[Eureka]] (NIRSpec) + custom MCMC; produces 12 spectrum variants by varying limb-darkening, spot correction, and binning. Retrievals: [[TauREX3]] 3.1 + PyMultiNest, comprehensive 13-species + simplified 1–2-species cross-comparisons. **CH₄ robust at 4.16σ–4.62σ across all configurations**; **CO₂ marginal at ~2σ in comprehensive retrievals (non-detection in some)**; **DMS retracted** (Bayes factor < 1; ln Z = 8.52 vs 8.62 for CO₂+CH₄ alone) — confirms Schmidt et al. 2025 retraction. C/O ≈ 10–13 (super-solar by ~10–20×); MMW ≈ 2.5–10 amu spanning H₂-He primordial to high-MMW. Argues for Inside-Out Planet Formation at ~500 K formation temperature, just interior to the carbon "soot" line. Novel semi-empirical occulted-spot correction methodology.
**PDF renamed:** raw/papers/2025_FernandezRodriguez_K2-18b.pdf
**Created:** wiki/papers/2025_FernandezRodriguez_K2-18b.md, wiki/programs/JWST-GO-2722.md (Madhusudhan Hycean program), wiki/species/DMS.md (first wiki entry; biosignature candidate)
**Updated:** wiki/targets/K2-18b.md (substantial expansion from comparator-stub to full target page; added atmospheric composition, observations, open questions, tensions sections), wiki/codes/{exoTEDRF,Eureka,TauREX3,MultiNest}.md, wiki/instruments/{JWST-NIRSpec,JWST-NIRISS}.md, wiki/methods/{atmospheric-retrievals,transmission-spectroscopy,stellar-contamination-modeling}.md, wiki/species/{CH4,CO2}.md, index.md (target unchanged at 70; species 14→15, programs 24→25, papers 45→46)
**Tension flagged:** [[K2-18b]] — DMS detection (Madhusudhan 2023, 2025; not ingested) vs non-detection ([[2025_FernandezRodriguez_K2-18b]], Schmidt 2025 not ingested). Same NIRISS+NIRSpec data; comprehensive retrievals retract DMS. Madhusudhan 2025 MIRI/LRS paper (not ingested) reasserts DMS at 6–12 μm — discriminator pending.
**Tension flagged:** [[K2-18b]] — CO₂ at 2σ ([[2025_FernandezRodriguez_K2-18b]]) vs 3.7σ (Hu et al. 2025, not ingested). Same NIRISS+NIRSpec dataset; Hu et al. add MIRI/LRS. CO₂ confirmation pending.
**Emphasis decisions (preferred approaches, no user pause):**
- Bibkey `2025_FernandezRodriguez_K2-18b` — full hyphenated surname (analogous to existing `2024_WeinerMansfield_GJ486b`, `2026_RoyPerez_WASP39b`); diacritics stripped per existing convention. Long but unambiguous.
- New species stub for [[DMS]] — central to current biosignature debate; appears in 4+ papers retroactively and is the focal molecule of the Hycean controversy. Created with explicit "currently retracted" framing.
- New JWST-GO-2722 program stub (Madhusudhan PI; first wiki ingest of a target from this program).
- Did **not** create stubs for ExoTETHyS (limb-darkening package; specialized; only one wiki paper), PyLightcurve (transit modeling; trace dependency), or PyMultiNest (subclass of MultiNest, already covered).
- Cited Madhusudhan et al. 2023, 2025; Schmidt et al. 2025; Welbanks et al. 2025; Hu et al. 2025; Wogan 2024; Shorttle 2024 in prose with "(not yet ingested)" suffix per § Referencing not-yet-ingested papers — this dataset has been analyzed at least 6 times across the literature.
- Substantial K2-18 b page rewrite warranted: was a stub-with-comparative-context from Roy 2025; now becomes a near-hub with three independent reanalysis citations and an explicit Tensions section. Formal hub promotion deferred per "never automatic" rule.

## [2026-05-04] ingest | 2025_Madhusudhan_subneptunes
**Paper:** Madhusudhan, Holmberg, Constantinou, Cooke 2025, PNAS (arXiv:2509.19247) — **review/perspective article**, not a single-target observation paper. Surveys JWST sub-Neptune characterization to date and proposes a two-axis classification scheme (T_eq × atmospheric H₂ content) yielding six categories: **ice worlds, hycean worlds, mini-Neptunes, gas dwarfs, supercritical mini-Neptunes, steam worlds**. Empirical critical temperature T_crit ≳ 350 K above which atmospheric H₂O cold-trap condensation breaks down. Reviews K2-18 b, TOI-270 d, GJ 9827 d as cornerstone observations; cites GJ 3470 b, GJ 1214 b, LHS 1140 b, L 98-59 d as comparators. Biosignature candidate gases: DMS, CS₂, OCS, CH₃Cl, N₂O.
**PDF renamed:** raw/papers/2025_Madhusudhan_subneptunes.pdf
**Created:** wiki/papers/2025_Madhusudhan_subneptunes.md, wiki/concepts/sub-neptune-classification.md (volatile-rich sub-Neptune classification scheme; central new concept page)
**Updated:** wiki/targets/{K2-18b,TOI-270d}.md (added concept link to sub-neptune-classification + paper bullet to See also), wiki/species/DMS.md (Madhusudhan 2025 review entry), index.md (concepts 6→7, papers 46→47)
**Emphasis decisions (preferred approaches, no user pause):**
- Bibkey `2025_Madhusudhan_subneptunes` — first review/perspective paper in the wiki; bibkey slug "subneptunes" reflects the topic rather than a single target.
- Frontmatter: empty `species_detected`/`species_tentative`/`species_ruled_out`/`codes` — this is a synthesis paper, not a primary observation. Targets list is empty for the same reason; targets are mentioned in prose.
- Created [[sub-neptune-classification]] concept page rather than separate hycean/mini-Neptune/steam-world stubs — the scheme is unified, fragmenting it would lose the unifying logic. Single concept hub is the appropriate organization.
- Did **not** create stubs for GJ 9827 d, GJ 3470 b, LHS 1140 b, GJ 1214 b, 55 Cnc e — referenced only as comparators in this review; their primary papers are not yet ingested. Following CLAUDE.md § Referencing not-yet-ingested papers, used "(not yet ingested)" prose instead of [[link]]s.
- Removed an initial `[[GJ1214b]]` link from paper page when stub didn't exist; replaced with prose "GJ 1214 b (not yet ingested)" per the schema rule.
- Linked `[[LHS1140c]]` because the wiki has the LHS 1140 c stub from the Connors 2025 ingest (sibling planet); the Madhusudhan paper actually focuses on LHS 1140 b not c, but the host system is referenced.
- Substantial framing in the paper page: explicitly note that several of Madhusudhan 2025's claims are "contested" by [[2025_FernandezRodriguez_K2-18b]] and [[2025_Felix_TOI-270d]] (the previous two ingests). The classification scheme is useful regardless of contested target placements; the wiki captures both.
- Did **not** create stubs for OCS, CH3Cl, N2O species — the first two are biosignature candidates only (no firm detection); N2O already exists in wiki as a 1-paper stub.

## [2026-05-04] ingest | 2025_Crossfield_SO2shoreline
**Paper:** Crossfield, Ahrer, Brande, Kreidberg, Lothringer, Piaulet-Ghorayeb, Polman, Welbanks, Kirk, Powell, Khorshid 2025, AJ submitted (arXiv:2509.14318) — **theoretical / forward-modeling grid paper**, no new observations. 936 self-consistent atmospheric models ([[HELIOS]] T-p + [[VULCAN]] photochemistry + [[petitRADTRANS]] spectra) mapping the SO₂ shoreline in (T_eq = 250–2050 K) × ([M/H] = 0.3–1000× solar) × (C/O 0.30/0.55/0.80) × (K_zz 10⁵/10⁷/10⁹) × (T_int 100/300/500 K) × (XUV 0.03/1/30×) parameter space; HAT-P-26 b system parameters as fiducial. Key findings: (1) SO₂ depends strongly on [M/H] and C/O, weakly on XUV/K_zz/T_int; (2) SO₂ never the dominant sulfur species (H₂S/S₂/NS/SO/SH/S₈/atomic-S frequently equal or exceed it); (3) shoreline detection of SO₂ implies C/O ≲ stellar AND/OR high metallicity. Of 4 confirmed SO₂ detections (WASP-39 b, WASP-107 b, HAT-P-26 b, GJ 3470 b), 3 sit in or near the shoreline; GJ 3470 b at the edge.
**PDF renamed:** raw/papers/2025_Crossfield_SO2shoreline.pdf
**Created:** wiki/papers/2025_Crossfield_SO2shoreline.md
**Updated:** wiki/concepts/SO2-photochemical-shoreline.md (substantial rewrite — Crossfield 2025 now the foundational mapping paper; added Theoretical Mapping section with key dependencies; demoted Crossfield 2023 to original-conceptual-proposal status), wiki/codes/{HELIOS,VULCAN,petitRADTRANS}.md, wiki/species/SO2.md, index.md (papers 47→48; Crossfield 2025 entry references HAT-P-26 b fiducial)
**Emphasis decisions (preferred approaches, no user pause):**
- Bibkey `2025_Crossfield_SO2shoreline` — slug "SO2shoreline" reflects the theoretical content rather than a target name. Distinct convention warranted by review/theory paper status.
- Frontmatter: empty `targets`/`instruments`/`methods`/`species_*` — modeling paper without observations. `codes` includes the three modeling codes (HELIOS, VULCAN, petitRADTRANS) which is the appropriate retention.
- Did **not** create stubs for: WASP-107 b, GJ 3470 b, HD 209458 b, HD 189733 b, WASP-15 b, TrES-4 b, WASP-94 A b, HIP 67522 b, WASP-166 b, TOI-421 b, GJ 3090 b, GJ 9827 d — all comparison-sample targets cited in this paper but only via prose; their primary papers not yet ingested.
- Did **not** create stubs for SO, SH, S₂, S₈, NS, OCS, CS, atomic S — these are model-only sulfur species (no detection on any wiki target as a primary observation). N₂O and CS₂ already exist as 1-paper stubs from prior ingests.
- Restructured the [[SO2-photochemical-shoreline]] page substantively: added a "Theoretical mapping" section before the existing empirical section, clarifying that Crossfield 2023 was the conceptual proposal and Crossfield 2025 is the formal mapping. Did not alter prior Gressier 2025 + Radica 2026 + RoyPerez 2026 entries.
- Schema note: this is the wiki's first **theoretical-grid** paper outside [[2025_Madhusudhan_subneptunes]] (perspective). No new schema rules needed; both fit cleanly under the standard paper template with empty observation-related frontmatter fields.

## [2026-05-04] ingest | 2025_Jaziri_K2-18b
**Paper:** Jaziri & Drant 2025, A&A 702:L20 (DOI: 10.1051/0004-6361/202556905) — A&A Letter to the Editor on K2-18 b. Joint reanalysis of Madhusudhan 2023 (NIRISS+NIRSpec; not ingested) + Luque 2025 (MIRI/LRS Eureka! reduction; not ingested) using TauREx 3.1 + the **TauREx-PyMieScatt** aerosol Mie-scattering module with complex refractive indices for 7 photochemical haze (tholin) analogs (CH₄-only "exo1"/"exo2" PAMPRE/COSmIC + 5 N₂/CH₄ Titan-like). MIRI/LRS feature amplitudes ~2× larger than NIRISS+NIRSpec — irreconcilable with the high-metallicity nonequilibrium model alone. **CH₄-derived "exo1" tholin haze (PAMPRE)** improves the combined fit at Bayes factor 5.53; reduces CH₄ abundance by ~2 dex (log VMR -1.2 → -3.5); lowers metallicity from 20× → 0.3× solar. Highlights the metallicity-aerosol-composition degeneracy.
**PDF renamed:** raw/papers/2025_Jaziri_K2-18b.pdf
**Created:** wiki/papers/2025_Jaziri_K2-18b.md
**Updated:** wiki/targets/K2-18b.md (added "Aerosol-inclusive reanalysis" subsection + Jaziri 2025 to See also paper list), wiki/codes/{TauREX3,MultiNest}.md, wiki/instruments/JWST-MIRI.md, wiki/methods/atmospheric-retrievals.md, wiki/species/CH4.md, index.md (papers 48→49; targets/concepts/programs/codes unchanged)
**Emphasis decisions (preferred approaches, no user pause):**
- Bibkey `2025_Jaziri_K2-18b` follows the standard convention.
- Type: paper, A&A Letter; treated as a normal observation paper (frontmatter `species_detected: [CH4]`, `species_tentative: [C2H4, H2CO]` per the MIRI free-retrieval results) even though it doesn't reduce raw data — it presents new retrieval analyses on published spectra. Convention going forward: independent reanalyses qualify as observation papers if they produce new atmospheric inferences.
- Did **not** create stubs for: TauREx-PyMieScatt (specialized aerosol module, single-paper use; reference Changeat 2025 not ingested), FRECKLL (specialized nonequilibrium chemistry; reference Al-Refaie 2024 not ingested), tholins (concept-class; covered in paper page prose; if more papers use it, may warrant a stub).
- Did **not** create species stubs for C₂H₂, C₂H₄, H₂CO — they appear as alternative free-retrieval favorites in MIRI but are not statistically preferred over a flat line; tholin haze interpretation supersedes.
- The K2-18 b page now lists three independent JWST analyses: [[2025_FernandezRodriguez_K2-18b]] (comprehensive retrieval, retracts DMS), [[2025_Madhusudhan_subneptunes]] (review/perspective, hycean classification), [[2025_Jaziri_K2-18b]] (aerosol modeling, reduces inferred metallicity). With three contrasting readings on the same dataset, K2-18 b is now the most-analyzed target in the wiki.
- The wiki's first **complex-refractive-index aerosol modeling** paper — flagged in the methodology argument on the [[atmospheric-retrievals]] page; could become a methodology theme if more papers adopt this approach.

## [2026-05-04] ingest | 2025_Sikora_HD80606b
**Paper:** Sikora, Rowe, Splinter, Barat, Dang, Cowan, Barclay, Colón, Désert, Kane, Llama, Shivkumar, Stassun, Quintana 2025, AJ 170:105 (DOI: 10.3847/1538-3881/addfda) — JWST NIRSpec G395H 20.9-hr partial phase curve of the highly eccentric hot Jupiter HD 80606 b (e = 0.93, P = 111.4 d, R = 1.03 R_J, M = 4.16 M_J) under [[JWST-GO-2488]] (PI Sikora) on 2022 Nov 1, capturing the secondary eclipse and periapse passage. Two independent reductions ([[Eureka]] + custom). [[CH4]] detected at 4.1–10.7σ in NRS1 post-periapse; [[H2O]] at 4.2–5.5σ in NRS2; [[CO2]] at 3.7–4.4σ in NRS2. Pre-eclipse phases consistent with featureless blackbody (T_bright ≈ 892 K); post-periapse phases show chemical-equilibrium spectra (T_bright peaks at 1313 K). **Rules out strong temperature inversion** despite GCM predictions (Tsai 2023b; not ingested). [[petitRADTRANS]] + [[easyCHEM]] chemical-equilibrium retrievals preferred over [[PyratBay]] free-chemistry at all post-periapse phases.
**PDF renamed:** raw/papers/2025_Sikora_HD80606b.pdf
**Created:** wiki/papers/2025_Sikora_HD80606b.md, wiki/targets/{HD80606b,HD80606}.md (stubs — first wiki characterization), wiki/programs/JWST-GO-2488.md
**Updated:** wiki/codes/{Eureka,petitRADTRANS,PyratBay,easyCHEM,MultiNest}.md, wiki/instruments/JWST-NIRSpec.md, wiki/methods/{secondary-eclipse-spectroscopy,atmospheric-retrievals}.md, wiki/species/{CH4,H2O,CO2}.md, index.md (target count 70→72; program count 25→26; paper count 49→50)
**Emphasis decisions (preferred approaches, no user pause):**
- Bibkey `2025_Sikora_HD80606b` follows the standard convention.
- Class for HD 80606 b: `gas-giant` (mass_mjup = 4.16, radius_rjup = 1.032). T_eq is class-independent and listed as 1500 K (the periapse irradiation-temperature peak) per the schema convention; the apoastron T_eq ≈ 300 K is documented in prose since the schema accommodates only one value.
- HD 80606 host: G dwarf (G5V approximation; T_eff = 5565 K). First Sun-like host besides [[HD-209458]] for a JWST-observed hot Jupiter in the wiki.
- Frontmatter `species_detected` includes [CH4, H2O, CO2] — all detected at >3σ in chemical-equilibrium retrievals; treated as firm despite single-visit single-eclipse data, since this is emission spectroscopy with multiple-detector replication.
- Methods: `secondary-eclipse-spectroscopy` + `atmospheric-retrievals`. Did NOT add a new "phase-curve-spectroscopy" method page despite this being a partial-phase-curve observation; only one paper in this regime so far. Promotion candidate when 3+ papers exist.
- Did **not** create a stub for the "highly-eccentric hot Jupiter" class — adding to existing tag namespace via `tags: [highly-eccentric, eccentric-orbit, ...]` instead. If 3+ such targets accumulate, a concept stub for "tidal eccentricity-driven seasonal effects" might warrant promotion.
- The Tsai 2023b GCM prediction was a key motivator; cited as "(not yet ingested)" in prose. de Wit et al. 2016 Spitzer phase curve and Lewis et al. 2017 GCM/cloud predictions also cited as not-yet-ingested.
- Identified as the first wiki target with **phase-resolved emission spectroscopy** showing time-variable chemistry — flagged in JWST-NIRSpec instrument hub and secondary-eclipse-spectroscopy method.


## [2026-05-04] ingest | 2025_Coulombe_TOI-270b
**Paper:** Coulombe et al. 2025, AJ 170:226 — JWST/NIRSpec G395H simultaneous transit of warm super-Earth TOI-270 b and sub-Neptune TOI-270 d; updated bulk density 4.4σ below Earth-like; tentative H₂O steam atmosphere; TLS ruled out via simultaneous d transit.
**Created:** wiki/papers/2025_Coulombe_TOI-270b.md, wiki/targets/TOI-270b.md (stub), wiki/instruments/NIRPS.md (stub), wiki/codes/PACMAN-P.md (stub), wiki/codes/smint.md (stub), wiki/codes/nestle.md (stub)
**Updated:** wiki/targets/TOI-270.md (added super-Earth + abundances), wiki/targets/TOI-270d.md (cross-link to companion paper, simultaneous-visit framing), wiki/programs/JWST-GO-4098.md (added Coulombe paper), wiki/species/H2O.md (new "Tentative — current" subsection for TOI-270 b), wiki/concepts/cosmic-shoreline.md (added Coulombe as possible challenger), index.md
**Emphasis decisions (user-approved per "use your preferred approaches"):**
- TL;DR foregrounded the methodological novelty (simultaneous-d transit as TLS control) alongside the underdense-bulk and tentative-H₂O findings.
- `species_tentative: [H2O]` only; no `species_detected` (no >3σ confirmed).
- Created stubs for the new code dependencies (PACMAN-P, smint, nestle) rather than only mentioning them inline — they will be cited again when more interior-modeling papers are ingested.
- Created NIRPS as a new instrument page (counterpart to JWST hosts), not folded into a method or concept page — it is a discrete observatory with a distinct GTO program.
- Did NOT create a stub for the "water world" planet class — handled via `class: terrestrial` + `water-world` tag for now; stub-promotion threshold not reached.
**Tension flagged:** [[H2O]] / [[TOI-270b]] — Coulombe lnB = 0.3 (no offset) to 3.2 (with offset), inconclusive-to-moderate; Holmberg & Madhusudhan 2024 (not ingested) preferred H₂-rich at >3σ on the same data. Tension recorded on the paper page; will surface as a `## Tensions` block on TOI-270b.md once a hub promotion or third independent reduction lands.
**Promotion candidacy:** none triggered.


## [2026-05-04] ingest | 2025_Fu_limb-asymmetry
**Paper:** Fu et al. 2025, ApJL 989:L17 — uniform JWST/NIRISS/SOSS reanalysis of nine archival hot-Jupiter transmission datasets for morning–evening limb asymmetry; 3/9 (WASP-39 b, WASP-94 Ab, WASP-17 b) > 5σ contrast; introduces Limb Spectroscopy Metric and asymmetry-horizon empirical boundary; quantifies up to +2 dex metallicity / ½× temperature retrieval bias from limb-averaging.
**Created:** wiki/papers/2025_Fu_limb-asymmetry.md, wiki/concepts/limb-asymmetry.md (stub with LSM and asymmetry-horizon as sections), wiki/codes/Catwoman.md (stub), wiki/codes/VIRGA.md (stub), wiki/programs/JWST-GO-5924.md (stub), wiki/programs/JWST-COM-2734.md (stub), wiki/programs/JWST-GO-2062.md (stub), wiki/targets/WASP-107.md + WASP-107b.md (stubs), wiki/targets/HAT-P-18.md + HAT-P-18b.md (stubs), wiki/targets/WASP-166.md + WASP-166b.md (stubs), wiki/targets/WASP-52.md + WASP-52b.md (stubs), wiki/targets/WASP-94A.md + WASP-94Ab.md (stubs)
**Updated:** wiki/targets/WASP-39b.md (added Limb-asymmetry section), wiki/targets/WASP-17b.md (idem), wiki/targets/WASP-80b.md (idem), wiki/targets/WASP-96b.md (idem), wiki/targets/WASP-39.md / WASP-17.md / WASP-80.md / WASP-96.md (See-also cross-link), wiki/instruments/JWST-NIRISS.md (added Fu paper), wiki/methods/transmission-spectroscopy.md (limb-resolved variant + limb-averaging-bias trade-off + new Papers subsection), wiki/methods/atmospheric-retrievals.md (new tension on limb-averaging bias), wiki/codes/PICASO.md (added Fu paper), wiki/programs/JWST-ERS-1366.md / JWST-GTO-1201.md / JWST-TST-GTO-1353.md (added Fu cross-references), index.md
**Emphasis decisions (user-approved per "use your preferred approaches"):**
- TL;DR led with the population-level finding (3/9 with >5σ asymmetry) and ended with the methodological-bias warning, rather than presenting them as separate findings.
- Created **one** concept page (`limb-asymmetry`) with LSM and asymmetry-horizon as `##` sections within it, rather than three separate concept pages. Reasoning: LSM and the asymmetry horizon are useful only in the context of limb asymmetry; splitting into 3 stubs would create poorly-linked sub-stubs and inflate the concept count without adding navigation value. If a follow-up paper proposes a competing observability metric or asymmetry boundary, splitting becomes warranted.
- Did NOT create a `limb-resolved-spectroscopy` method page — added a "Limb-resolved transmission" subsection to existing [[transmission-spectroscopy]] hub. The technique is a transit-fitting variant ([[Catwoman]] + ingress/egress vs. baseline differencing), not a new method category.
- Did NOT create stubs for the per-NIRISS-target reductions (Espinoza 2024, Carter 2024, Louie 2025, etc.) cited as "not yet ingested" — followed the wiki's "name-the-paper-with-(not yet ingested)-suffix" rule for prose mentions.
- Created `WASP-94A` (not `WASP-94`) as the host page since the planet designation is `WASP-94 Ab` and the system is a binary; aliased and tagged accordingly.
- Tagged stubs with `limb-asymmetry-strongest` (WASP-94 Ab only) to flag the LSM normalization reference for future searches.
- Did NOT promote any existing entity to a hub: WASP-17 b at 3 papers crosses the "≥3 papers reference" alternative threshold for promotion candidacy — flagged below.
**Tension flagged:** [[atmospheric-retrievals]] / hot-Jupiter limb-averaged retrievals — Fu 2025 quantifies up to +2 dex metallicity and ½× temperature bias for terminator cloud fraction f = ½. Documented examples: [[WASP-39b]] (Lueber 2024 vs. Espinoza 2024 — ~2 dex spread), [[WASP-94Ab]] (Ahrer 2025 retrieved T = 700–1000 K vs. T_eq = 1543 K), [[WASP-17b]] (Louie 2025 retrieved T = 1272 K vs. T_eq = 1755 K). Logged on the atmospheric-retrievals hub Trade-offs section.
**Promotion candidacy:** [[WASP-17b]] now at 3 papers ([[2025_Gressier_WASP17b]], [[2025_LustigYaeger_WASP17b]], [[2025_Fu_limb-asymmetry]]) — crosses the "≥3 papers" alternative threshold. Not promoted per "never automatic"; awaits user approval at next lint. Same for [[WASP-39b]] (now 2 papers — below threshold but with growing thematic span: ERS reanalysis [[2026_RoyPerez_WASP39b]] + limb asymmetry).



## [2026-05-04] ingest | 2025_Murphy_WASP107b
**Paper:** Murphy, Beatty, Schlawin, Bell, Radica, Kennedy, Mehta, Welbanks, Line, Parmentier, Greene, Mukherjee, Fortney, Ohno, Wiser, Arnold, Rauscher, Edelman, Rieke 2025, AJ 170:61 (DOI 10.3847/1538-3881/addf38) — JWST 1–12 μm panchromatic limb-resolved analysis of [[WASP-107b]] using all five archival visits (NIRCam F322W2 + F444W, NIRISS/SOSS, NIRSpec G395H, MIRI/LRS) via [[Catwoman]] two-semicircle transit fits. Confirms ~180 K evening–morning T gradient and resolves chemical heterogeneity: ~5× more SO₂ on morning limb (log VMR −4.7 vs −5.4), ~40× more CO₂ on morning (log VMR −3.6 vs −5.2), uniform H₂O. Broad 6–11 μm cloud feature isolated to morning limb only. Develops [[Catwoman]] + `starry` injection-recovery model for occulted starspot bias on limb-resolved spectra (NIRISS, NIRSpec affected; NIRCam, MIRI clean) — establishes that a single spot near ingress vs. egress can flip the polarity of a retrieved limb-asymmetry signal.
**PDF renamed:** raw/papers/2025_Murphy_WASP107b.pdf
**Created:** wiki/papers/2025_Murphy_WASP107b.md
**Updated:** wiki/targets/WASP-107b.md (stub → stub+synthesis with Atmospheric composition, Observations to date, Tensions sections), wiki/targets/WASP-107.md (paper list), wiki/concepts/limb-asymmetry.md (new "Chemical heterogeneity between limbs" section), wiki/concepts/SO2-photochemical-shoreline.md (added Murphy 2025 limb-resolved validation note for WASP-107 b outlier), wiki/species/{SO2,CO2,H2O,CH4}.md (each gained a Murphy entry; SO₂/CO₂ first limb-resolved asymmetry entries), wiki/instruments/{JWST-NIRCam,JWST-MIRI,JWST-NIRISS,JWST-NIRSpec}.md (each gained a Murphy entry), wiki/methods/{transmission-spectroscopy,stellar-contamination-modeling}.md (transmission gained "Hot Jupiter — panchromatic + limb-resolved" subsection; stellar-contamination-modeling gained "Occulted-spot crossings on limb-resolved spectra — K-dwarf" subsection), wiki/codes/{Tshirt,Eureka,exoTEDRF,Catwoman,Aurora}.md (Tshirt page rewritten to correctly attribute Schlawin & Glidic 2022 origin; others gained Murphy paper entries), index.md
**Emphasis decisions (preferred approaches, no user pause):**
- WASP-107 b page promoted from pure stub (1 paper) to stub+synthesis with Atmospheric composition + Observations to date + Open questions + Tensions sections — second JWST-era paper materially updates the Fu 2025 reading. Hub-template promotion deferred to user approval per CLAUDE.md.
- Tension flagged on WASP-107 b limb-asymmetry classification: [[2025_Fu_limb-asymmetry]] places WASP-107 b in the symmetric (no asymmetry) bin via NIRISS/SOSS only, while [[2025_Murphy_WASP107b]] finds significant SO₂/CO₂/cloud asymmetry via panchromatic limb-resolved analysis. Driver: stellar-contamination correction.
- Did NOT create a stub for the `starry` stellar-surface code — single-paper use within the spot-correction injection-recovery; reference Luger et al. 2019, 2021a, 2021b cited in prose as not-yet-ingested. Same for `emcee`, `batman`, `ExoCTK`, `ExoTiC-LD` — common Python utilities mentioned only in passing.
- Did NOT create stubs for RM-GCM, SPARC/MITgcm — single-paper GCM dependencies; would warrant promotion when 3+ papers use either.
- Tshirt page (previously incorrectly attributed origin to Roy-Perez 2026) corrected to Schlawin & Glidic 2022; description and paper-list expanded.
**Promotion candidacy:** [[WASP-107b]] now at 2 papers — below 3-paper threshold; not yet promotable to hub.
**Tension flagged:** [[WASP-107b]] / [[limb-asymmetry]] — Fu 2025 (no detected asymmetry) vs. Murphy 2025 (significant SO₂ + CO₂ + cloud asymmetry). Driver: occulted-starspot correction in the NIRISS visit.

## [2026-05-04] ingest | 2025_Verma_HD209458b
**Paper:** Verma, Goyal, Avarsekar, Shukla 2025, AJ 170:69 (DOI 10.3847/1538-3881/addc5c) — introduces **SANSAR** (Suite of Adaptable plaNetary atmoSphere model And Retrieval), a Python-based Bayesian retrieval framework supporting opacity-sampling and correlated-k radiative transfer; benchmarked against [[POSEIDON]] (~6 ppm offset), [[ATMO]], [[CHIMERA]], [[Aurora]] on WASP-96 b. Applied to [[HD-209458b]] in three instrument combinations: (i) JWST/NIRCam only, (ii) HST/WFC3 + NIRCam, (iii) HST/STIS + WFC3 + NIRCam. Demonstrates that **NIRCam-only retrievals overestimate H₂O and CO₂ abundances by ~3 dex** relative to STIS+WFC3+NIRCam — the optical baseline anchors temperature and cloud properties. With full coverage: H₂O at 12.6σ, CO₂ at 7.8σ, Na at 6.9σ, K at 4.9σ; metallicity 0.8–2.1× solar; C/O = 0.54 ± 0.09 (consistent with stellar). Rejects MacDonald & Madhusudhan 2017 NH₃ tentative claim and Giacobbe et al. 2021 ground-based CH₄/HCN/NH₃/C₂H₂/CO claims (all 3σ upper limits).
**PDF renamed:** raw/papers/2025_Verma_HD209458b.pdf
**Created:** wiki/papers/2025_Verma_HD209458b.md, wiki/codes/SANSAR.md
**Updated:** wiki/targets/HD-209458b.md (theory-only stub → stub+synthesis with Atmospheric composition + Observations to date + Open questions; first JWST-era ingestion for HD 209458 b), wiki/targets/HD-209458.md (paper list), wiki/instruments/{JWST-NIRCam,HST-STIS,HST-WFC3}.md (each gained Verma entry), wiki/species/{H2O,CO2,Na,K}.md (each gained Verma entry; H₂O/CO₂ wavelength-coverage subsection), wiki/methods/atmospheric-retrievals.md (new "Frameworks introduced" subsection with SANSAR), wiki/codes/{POSEIDON,CHIMERA,ATMO,Aurora,FastChem,MultiNest}.md (benchmarking entries), index.md
**Emphasis decisions (preferred approaches, no user pause):**
- HD-209458b page promoted from theory-only stub to stub+synthesis with Atmospheric composition section — first JWST-era paper for the historical archetype.
- Treated re-analysis paper as observation paper (per Jaziri/K2-18 b convention from prior log entries).
- Did NOT create stubs for: PyFastChem, Exo_k, BT2 line list, ROEBA correction — all sub-modules / utilities; single-paper relevance.
- Did NOT create a stub for "wavelength-coverage bias" as a concept — phenomenon documented in Verma's paper and the [[atmospheric-retrievals]] hub Trade-offs section; promotion if 3+ papers explore it.
- C/O = 0.54 retained as the headline since matches stellar 0.42 ± 0.08 (Polanski 2022; not ingested) — supports clean primordial-formation interpretation. Frontmatter `species_detected` lists [H2O, CO2, Na, K] (4 species ≥ 4σ in full retrieval).

## [2026-05-04] ingest | 2025_Barat_V1298Tau-b
**Paper:** Barat, Désert, Mukherjee, Goyal, Xue, Kawashima, Vazan, Misener, Schlichting, Fortney, Taylor, Henry, Baeyens, Line, Livingston, David, Petigura, Sikora, Shivkumar, Feinstein, Oklopčić 2025, AJ 170:165 (DOI 10.3847/1538-3881/adec89) — JWST/NIRSpec G395H + HST/WFC3 panchromatic 1.0–5.2 μm transmission of the young (10–30 Myr) sub-Neptune progenitor V1298 Tau b ([[JWST-GO-2149]], PI Désert) on 2023 Feb 12. Reveals a clear haze-free atmosphere (~1500 km scale height); detects [[CO2]] at 35σ + [[H2O]] at 30σ + [[CO]] at 10σ + [[CH4]] at 6σ + [[SO2]] at 4σ; tentative OCS at 3.5σ. Mass measured from atmospheric scale height (12 ± 1 M⊕, ~10% precision) — cross-validated against WASP-107 b (Sing 2024 NIRSpec → 32 ± 3 M⊕ vs. RV-derived 30.5 ± 1.7 M⊕). Atmospheric metallicity ~0.6× solar; subsolar C/O ≈ 0.22; both ~10× lower than mature sub-Neptunes — places V1298 Tau b as a **gas-dwarf** sub-Neptune progenitor. CH₄ abundance 7σ lower than equilibrium expectation requires high T_int ≈ 500 K + K_zz ~ 10⁷–10⁸ cm² s⁻¹; high T_int **inconsistent with formation/evolution models** predicting 100–200 K at 20 Myr. Mass loss could enhance metallicity over Gyr to reconcile with mature sub-Neptunes.
**PDF renamed:** raw/papers/2025_Barat_V1298Tau-b.pdf
**Created:** wiki/papers/2025_Barat_V1298Tau-b.md, wiki/targets/V1298Tau-b.md (planet stub), wiki/targets/V1298Tau.md (host stub — first young T Tauri host in the wiki), wiki/programs/JWST-GO-2149.md (program stub)
**Updated:** wiki/instruments/{JWST-NIRSpec,HST-WFC3}.md (each gained Barat entry; G395H + young-planet subsection on NIRSpec hub), wiki/species/{H2O,CO2,CO,CH4,SO2}.md (each gained Barat entry; CH4 thermometer interpretation; CO2 35σ in sub-Neptune-mass), wiki/methods/{transmission-spectroscopy,flare-mitigation}.md (transmission gained sub-Neptune subsection entry; flare-mitigation gained empirical in-transit Barat entry — first non-M-dwarf application), wiki/concepts/sub-neptune-classification.md (V1298 Tau b added as gas-dwarf progenitor, T_eq = 670 K, age 10–30 Myr), wiki/codes/{Eureka,SPARTA,PICASO,ATMO,VULCAN,Photochem,MultiNest}.md (each gained Barat entry; PICASO + Photochem chemistry-thermometer reasoning), index.md
**Emphasis decisions (preferred approaches, no user pause):**
- Bibkey `2025_Barat_V1298Tau-b` uses dash in slug per the planet name "V1298 Tau b"; consistent with WASP-94Ab and similar designations.
- Frontmatter: `species_detected` includes [H2O, CO2, CO, CH4, SO2] (≥4σ each); `species_tentative: [OCS]` (3.5σ in 10-pixel binning, 2σ in 20-pixel; rejected to tentative tier).
- Did NOT create stubs for: AIOLOS (interior-evolution code, single-paper use); batman (transit model utility); ExoTiC-LD (limb-darkening utility, even though already exists for the wider community — the wiki has [[ExoTiC-JEDI]] but not the LD-only fork); SANSAR-like ML-component grid retrievals.
- Did NOT create a "young-planet atmospheric characterization" method stub — single paper currently; if 3+ such targets accumulate, promotion warranted.
- Did NOT create a "methane thermometer" concept stub — concept introduced by S. Mukherjee et al. 2025 (not yet ingested) and applied uniquely here; promotion when an additional independent paper applies it.
- Tagged frontmatter `class: sub-neptune` for V1298 Tau b despite its 9.85 R⊕ being unusually large — consistent with the paper's "gas-dwarf sub-Neptune progenitor" framing; the planet is mass-defined as sub-Neptune (12 M⊕), and its inflated radius is a young-age artifact.
- V1298 Tau host classified as `K` (T_eff ≈ 5050 K) per the schema; closer to G–K boundary; the paper uses 5000 K stellar photosphere model.

## [2026-05-04] ingest | 2025_Deka_WASP39b
**Paper:** Deka, Khan, Dewan, Ghosh, Das, Majumdar 2025, ApJ 989:50 (DOI 10.3847/1538-4357/add33d) — introduces **NEXOTRANS**, a hybrid Bayesian + machine-learning atmospheric retrieval framework. Bayesian inference via PyMultiNest ([[MultiNest]]) and UltraNest; four ML algorithms (Random Forest, Gradient Boosting, k-Nearest Neighbor, Stacking Regressor). Includes **NEXOCHEM**, an in-house chemical-equilibrium module benchmarked against [[FastChem]]. Four chemistry options: free, equilibrium, **modified hybrid equilibrium**, and **modified equilibrium-offset** (extending Constantinou & Madhusudhan 2024; not ingested). Applied to WASP-39 b panchromatic JWST NIRISS+PRISM+MIRI 0.6–12.0 μm data; cross-validated against eight community retrieval codes ([[ARCiS]], [[Aurora]], [[CHIMERA]], [[BeAR]], NEMESIS, [[PyratBay]], [[TauREX3]], [[POSEIDON]]) on the MIRI subset (all within 1σ). Best-fit hybrid retrieval: O/H = 14.12⁺²·⁸⁶⁻¹·⁸² × solar, C/H = 21.37⁺⁴·⁹³⁻³·¹⁸ × solar, S/H = 5.37⁺⁰·⁷⁹⁻⁰·⁶⁵ × solar, C/O = 1.35⁺⁰·⁰⁵⁻⁰·⁰¹² × solar. ML retrievals (Stacking Regressor; R² = 0.855–0.76) match Bayesian within 1σ at ~0.1× wall-clock cost.
**PDF renamed:** raw/papers/2025_Deka_WASP39b.pdf
**Created:** wiki/papers/2025_Deka_WASP39b.md, wiki/codes/NEXOTRANS.md (with NEXOCHEM as alias)
**Updated:** wiki/targets/{WASP-39b,WASP-39}.md (paper count → 3; new Methodology benchmarks subsection on planet page; programs cross-link to ERS), wiki/programs/JWST-ERS-1366.md (Deka entry), wiki/instruments/{JWST-NIRISS,JWST-NIRSpec,JWST-MIRI}.md (Deka panchromatic entry), wiki/species/{H2S,Na,K,SO2,CO2}.md (each gained Deka entry; H₂S non-tentative on WASP-39 b in NEXOTRANS), wiki/methods/atmospheric-retrievals.md ("Frameworks introduced" subsection extended with NEXOTRANS), wiki/codes/{POSEIDON,FastChem,FIREFLy,Tiberius,SPARTA,Eureka,supreme-SPOON,MultiNest}.md (each gained Deka entry; NEXOTRANS benchmarking + reductions used), index.md
**Emphasis decisions (preferred approaches, no user pause):**
- Bibkey `2025_Deka_WASP39b` follows convention; wiki's third paper on WASP-39 b (after Roy-Perez 2026 and Fu 2025).
- NEXOCHEM treated as an alias of NEXOTRANS rather than a separate code stub — internally bundled module within NEXOTRANS, not separately deployable.
- Frontmatter: full species list (Na, K, H₂O, CO₂, CO, SO₂, H₂S) detected at >3σ across all chemistry options.
- Did NOT create separate stubs for UltraNest, Random Forest, Gradient Boosting, kNN, Stacking Regressor, Ridge Regressor — all are sub-components of NEXOTRANS or generic ML algorithms; would only warrant separate stubs if multiple wiki papers used them outside NEXOTRANS.
- WASP-39 b page now hosts methodology benchmarks subsection alongside the existing limb-asymmetry section, foregrounding the paper's framework focus rather than re-detecting molecules.
- Did NOT create a stub for "modified hybrid equilibrium" / "modified equilibrium-offset" chemistry — described as NEXOTRANS-specific implementations of the Constantinou & Madhusudhan 2024 framework; promotion if a competing implementation arises.
**Promotion candidacy:** [[WASP-39b]] now at 3 papers ([[2025_Fu_limb-asymmetry]], [[2026_RoyPerez_WASP39b]], [[2025_Deka_WASP39b]]) — crosses the "≥3 papers" alternative threshold for hub promotion. Not promoted per "never automatic"; awaits user approval at next lint.


## [2026-05-04] ingest | 2008_Pont_HD189733b
**Paper:** Pont, Knutson, Gilliland, Moutou, Charbonneau 2008, MNRAS 385:109 (DOI 10.1111/j.1365-2966.2008.12852.x) — three HST/ACS G800L transits of HD 189733 b (550–1050 nm); featureless visible spectrum + 472 ± 42 km redward slope + ~1000 km IR–visible offset; **first conclusive aerosol detection in an exoplanet atmosphere**. Five-solution cross-check (different visit/spot/limb-darkening choices) verifies the slope is robust against starspot systematics at the time of analysis.
**PDF renamed:** raw/papers/2008_Pont_HD189733b.pdf
**Created:** wiki/papers/2008_Pont_HD189733b.md, wiki/targets/HD-189733b.md (stub+synthesis with Atmospheric composition + Observations to date + Tensions sections; 3 papers — crosses ≥3-paper alternative promotion threshold; promotion deferred per "never automatic"), wiki/targets/HD-189733.md (host stub), wiki/instruments/HST-ACS.md (stub), wiki/concepts/aerosols.md (concept stub)
**Updated:** wiki/species/Na.md (HD 189733 b non-detection), wiki/species/K.md (HD 189733 b non-detection)
**Emphasis decisions (preferred approaches, no user pause):**
- Bibkey `2008_Pont_HD189733b` follows convention; Pont 2007 referred to as "Paper I" but is an A&A paper (orbital parameters from white-light fit) not the transmission analysis; not separately ingested.
- HD-189733b page written as **stub+synthesis** rather than a pure stub immediately, since 3 papers + an active tension warrants the Atmospheric composition + Observations to date + Tensions sections per CLAUDE.md "stub + synthesis — intermediate state".
- Aerosols concept: created as a single concept page covering haze/cloud/condensate/dust/aerosol per the Pont 2008 footnote ("we make no fundamental distinction between clouds and haze, which differ only by their opacity"). Aliases capture the synonyms.
- Did NOT create stubs for HST programs (no JWST-program-style precedent in wiki for HST GO numbers).

## [2026-05-04] ingest | 2013_Pont_HD189733b
**Paper:** Pont, Sing, Gibson, Aigrain, Henry, Husnoo 2013, MNRAS 432:2917 (DOI 10.1093/mnras/stt651) — panchromatic 0.3–24 μm transmission spectrum of HD 189733 b combining HST STIS + ACS + WFC3 + NICMOS + Spitzer IRAC + Spitzer MIPS observations. Establishes the AC + DC unocculted-starspot decomposition via 5+ years of APT photometry + Gaussian-process interpolation; near-monotonic Rayleigh-like blueward radius increase across UV-to-NIR; narrow Na D + tentative K (2.5σ) cores only; dust-dominated atmosphere over ≥5 scale heights; antigreenhouse temperature inversion; pM/pL hot-Jupiter dichotomy reframed as clear-vs-dusty.
**PDF renamed:** raw/papers/2013_Pont_HD189733b.pdf
**Created:** wiki/papers/2013_Pont_HD189733b.md, wiki/instruments/HST-NICMOS.md (stub), wiki/instruments/Spitzer-IRAC.md (stub), wiki/instruments/Spitzer-MIPS.md (stub)
**Updated:** wiki/instruments/HST-WFC3.md (Pont 2013 entry), wiki/instruments/HST-STIS.md (Pont 2013 entry), wiki/concepts/stellar-contamination.md (Pont 2013 paper-level entry; HD 189733 b panchromatic-slope tension noted), wiki/methods/stellar-contamination-modeling.md (pre-JWST hot-Jupiter benchmarks subsection), wiki/methods/transmission-spectroscopy.md (HST UV-to-NIR panchromatic variant), wiki/species/Na.md (HD 189733 b narrow-core entry), wiki/species/K.md (HD 189733 b 2.5σ tentative entry), wiki/concepts/aerosols.md (paper-list entry), wiki/targets/HD-189733b.md (Observations to date + Tensions blocks)
**Emphasis decisions (preferred approaches, no user pause):**
- Frontmatter: `species_detected: [Na, K]` — Na from Huitson 2012 narrow-core (~4σ; cited as not-yet-ingested) confirmed by Pont 2013; K listed despite 2.5σ marginal status because Pont's pixel-by-pixel reanalysis is a positive (~tentative) detection.
- Did NOT create a separate `pM-pL-classification` concept stub — single-paper framing within Pont 2013; would warrant promotion if a follow-up extends the dichotomy.
- HST-NICMOS stub explicitly notes the Swain/Vasisht/Tinetti 2008 spectroscopic data deemed unreliable; only F166N/F187N photometric points retained — important nuance for any future user querying the wiki on NICMOS exoplanet papers.

## [2026-05-04] ingest | 2014_McCullough_HD189733b
**Paper:** McCullough, Crouzet, Deming, Madhusudhan 2014, ApJ 791:55 (DOI 10.1088/0004-637X/791/1/55) — single HST/WFC3 G141 spatial-scan transit of HD 189733 b (HST GO-12881); two H₂O features detected (200 ± 47 ppm at 1.4 μm + 83 ± 53 ppm at 1.15 μm) consistent with clear solar-composition atmosphere at H₂O ≈ 5×10⁻⁴, T ≈ 700 K. Two independent reductions (N. Crouzet, D. Deming) cross-validated. **Reinterprets the [[2013_Pont_HD189733b]] panchromatic Rayleigh slope as unocculted-starspot contamination + clear atmosphere** (T_phot = 5000 K, T_spot = 3700 K, δ ≈ 5.6 %); Na/K condensation onto KCl/Na₂S sulfides at the cool terminator explains missing alkali wings.
**PDF renamed:** raw/papers/2014_McCullough_HD189733b.pdf
**Created:** wiki/papers/2014_McCullough_HD189733b.md
**Updated:** wiki/instruments/HST-WFC3.md (McCullough entry), wiki/species/H2O.md (HD 189733 b detection subsection added), wiki/concepts/stellar-contamination.md (Tensions block + paper entry), wiki/methods/stellar-contamination-modeling.md (pre-JWST hot-Jupiter benchmarks subsection entry), wiki/methods/transmission-spectroscopy.md (TLS-as-confounder note for active K-dwarf hosts), wiki/concepts/aerosols.md (TLS-vs-dust note + paper entry), wiki/targets/HD-189733b.md (Observations to date + Tensions sections; Atmospheric composition Scenario B)
**Emphasis decisions (preferred approaches, no user pause):**
- Frontmatter: `species_detected: [H2O]` (the 1.4 μm 200 ppm feature is the headline confirmed detection; significance jumps from 4σ at 19-nm bins to ~8σ at 75-nm bins). `species_ruled_out: [Na, K]` for **broad** alkali absorption at the level predicted by clear-atmosphere models — *not* ruling out alkali presence, only their broad-wing transmission signature.
- Tension recorded on the McCullough paper (the *newer* paper per CLAUDE.md "stale claims" rule) and propagated to wiki/targets/HD-189733b.md as the canonical ledger location.
- Treated the McCullough 2014 reading as **alternative, not supersession** — both Pont and McCullough scenarios remain viable per the wiki's 2014-state-of-the-art frozen at ingest. JWST-era data on HD 189733 b would adjudicate but no JWST-target paper is in the wiki.
**Tension flagged:** [[HD-189733b]] / panchromatic transmission slope — dust haze ([[2008_Pont_HD189733b]] / [[2013_Pont_HD189733b]]) vs. unocculted-starspot TLS contamination ([[2014_McCullough_HD189733b]]). Driver: the unocculted-spot DC component (steady minimum spot dimming) — Pont applies only the AC component, McCullough adds δ ≈ 5.6 % steady background.

## [2026-05-04] ingest | 2018_Rackham_TLS
**Paper:** Rackham, Apai, Giampapa 2018, ApJ 853:122 (DOI 10.3847/1538-4357/aaa08c) — foundational paper defining and quantifying the transit-light-source-effect (TLSE) for M-dwarf planet hosts. Rotating-photosphere forward models with PHOENIX (M0V–M5V) + DRIFT-PHOENIX (M5V–M9V); four heterogeneity cases × Monte Carlo. Calibrates **A ∝ f_spot^0.5** (square-root, not linear) — variability monitoring underestimates true spot covering fraction. Typical 1 % I-band variability M dwarfs: f_spot = 8–14 % (solar-like spots) or ~1 % (giant spots). M-dwarf TLS contamination is **1–15× the transit-depth changes expected for atmospheric features in rocky planets**. TRAPPIST-1: f_spot = 8⁺¹⁸⁻⁷ %, f_fac = 54⁺¹⁶⁻⁴⁶ %; biases bulk densities by Δ(ρ) = −8⁺⁷⁻²⁰ %.
**PDF renamed:** raw/papers/2018_Rackham_TLS.pdf
**Created:** wiki/papers/2018_Rackham_TLS.md
**Updated:** wiki/concepts/stellar-contamination.md (replaced "Rackham et al. 2018; not yet ingested" with [[2018_Rackham_TLS]] link in lede; added History block entry; added Papers list entry), wiki/methods/stellar-contamination-modeling.md (idem in lede + new "Theory / framework papers" Papers subsection)
**Emphasis decisions (preferred approaches, no user pause):**
- Frontmatter: `targets: [TRAPPIST-1]` (the only specific target case study) — even though the paper is M-dwarf-population-wide; alternative `targets: []` would obscure the paper's TRAPPIST-1 quantitative findings.
- Did NOT create a separate `transit-light-source-effect.md` concept stub — the existing [[stellar-contamination]] hub already aliases "transit light source effect"; per CLAUDE.md "No redirect stubs for pure aliases — they live only in frontmatter".
- Did NOT replace the `(Rackham et al. 2018; not yet ingested)` reference in the **frozen** [[2025_Rathcke_TRAPPIST1bc]] paper page — paper pages are frozen at ingest time per "stale claims".

## [2026-05-04] ingest | 2019_Rackham_TLS-FGK
**Paper:** Rackham, Apai, Giampapa 2019, AJ 157:96 (DOI 10.3847/1538-3881/aaf892) — Paper II in the TLS series; extends [[2018_Rackham_TLS]] to F5V–K9V dwarfs. Reference activity-level spot fractions: 0.1 % (F5V) → 1 % (G dwarfs) → 1.5–2.1 % (K dwarfs). Band-averaged molecular-feature TLS offsets are NOT detectable for typically active FGK dwarfs (with TiO/VO on active late-K and atomic line wings as exceptions). **Active K dwarfs with unocculted spots produce visible blueward slopes** at the magnitude observed for HD 189733 b — explicitly cites [[2014_McCullough_HD189733b]]'s TLS reinterpretation of the [[2013_Pont_HD189733b]] panchromatic slope as quantitatively viable.
**PDF renamed:** raw/papers/2019_Rackham_TLS-FGK.pdf
**Created:** wiki/papers/2019_Rackham_TLS-FGK.md
**Updated:** wiki/concepts/stellar-contamination.md (lede + History block + Papers entry; HD 189733 b tension foregrounded), wiki/methods/stellar-contamination-modeling.md (Theory / framework papers subsection), wiki/concepts/aerosols.md (TLS-vs-dust note), wiki/targets/HD-189733.md (host description noting the K-dwarf TLS connection), wiki/targets/HD-189733b.md (Tensions block — Rackham 2019 vindicates McCullough mechanism quantitatively without adjudicating Pont vs. McCullough), index.md (new Targets section entries for HD-189733b and HD-189733; new Instruments entries for HST-ACS, HST-NICMOS, Spitzer-IRAC, Spitzer-MIPS; new Concepts entry for aerosols; 5 new Papers entries; updated stellar-contamination paper count 14 → 19)
**Emphasis decisions (preferred approaches, no user pause):**
- Frontmatter: `targets: []` (no specific case-study target — the HD 189733 b discussion is brief and embedded in the introduction, not the paper's main subject).
- Tag `hd-189733b-reinterpretation` added to flag this paper as the canonical theoretical vindication of [[2014_McCullough_HD189733b]] for future HD 189733 b queries.
- Did NOT create stubs for *Kepler* (instrument), Pecaut & Mamajek 2013 stellar parameter scale, McQuillan 2014 rotation-period catalogue — single-paper references; cited inline.
**Promotion candidacy:** [[stellar-contamination]] paper count rises 14 → 19; already a hub. [[HD-189733b]] now at 3 papers (Pont 2008, Pont 2013, McCullough 2014) — crosses the ≥3-paper alternative threshold; written as stub+synthesis with Tensions block per CLAUDE.md guidance, full hub promotion deferred to user approval at next lint.
