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
