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
