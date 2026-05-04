---
type: program
aliases: [COMPASS, JWST GO 2512, Compositions of Mini-Planet Atmospheres for Statistical Study]
tags: [jwst-cycle-1, small-planets, super-earth, sub-neptune, population-level, hub]
---

# JWST GO 2512 — COMPASS

JWST Cycle 1 Guest Observer program 2512 (PIs: N. E. Batalha & J. Teske; "Compositions of Mini-Planet Atmospheres for Statistical Study"), obtaining NIRSpec/G395H transmission spectra of a statistically-motivated sample of 11 small (1–3 R⊕) planets — including six with R_p < 1.7 R⊕. Designed to build a link between planetary demographics and atmospheric characterization at the population level (N. E. Batalha et al. 2023; not yet ingested). Target selection via a merit function on R_p, insolation, T_eff, and exposure time required to reach 30 ppm precision in R~100 G395H at 4 μm. The sample includes four target pairs in the same multi-planet systems. The single largest uniform-design small-planet program in this wiki — six papers ingested on individual targets, plus [[2025_Gordon_COMPASS-G395H]] as the first uniform reanalysis covering seven of the targets.

## Targets and papers

| Target | Class | Host | Paper(s) |
|---|---|---|---|
| [[GJ357b]] | super-Earth | M2.5V | [[2025_Redai_GJ357b]] |
| [[L168-9b]] | hot super-Earth | M1V | [[2025_Alam_L168-9b]] |
| [[L98-59c]] | warm super-Earth | M3V | [[2024_Scarsdale_L98-59c]] |
| [[TOI-776b]] | warm super-Earth | M1V | [[2025_Alderson_TOI-776b]] |
| [[TOI-776c]] | warm sub-Neptune | M1V | [[2025_Teske_TOI776c]] |
| [[TOI-836b]] | super-Earth | K-dwarf | [[2024_Alderson_TOI-836b]] |
| [[TOI-836c]] | sub-Neptune | K-dwarf | (reanalysis only — [[2025_Gordon_COMPASS-G395H]]) |

The remaining four COMPASS targets have not yet been published in the wiki.

[[2025_Gordon_COMPASS-G395H]] introduces the uniform [[ExoTiC-JEDI]] reanalysis of the first **seven** COMPASS spectra (the six papers above plus [[TOI-836c]]) using the new RPF-PCA systematics model.

## Methodology

- **NIRSpec G395H BOTS** as the uniform mode (R ≈ 2700, 2.8–5.2 μm with NRS1/NRS2 detector gap).
- **Two visits per target** (typical) — preconditions for [[multi-visit-stacking]] joint or weighted-mean fits.
- **Two-pipeline cross-checks** as standard: [[Eureka]] + [[ExoTiC-JEDI]] is the canonical pairing across [[2024_Scarsdale_L98-59c]], [[2024_Alderson_TOI-836b]], [[2025_Alderson_TOI-776b]], [[2025_Teske_TOI776c]]; subsequent papers add [[Tiberius]] as a third reduction.
- **Group-level (stage 1) custom background subtraction** has become a recurring feature, particularly in Eureka! v1.11.4+ ([[2025_Teske_TOI776c]], [[2025_Alderson_TOI-776b]]).
- **Standardized retrieval frameworks:** PICASO physical models ([[2025_Teske_TOI776c]]), free + equilibrium chemistry ([[2025_Redai_GJ357b]]), H₂/CO₂ mixture exclusion ([[2024_Scarsdale_L98-59c]]).

## Results to date

All six individual-target COMPASS papers report **featureless** transmission spectra at R~100 G395H precision. The headline conclusions are uniform metallicity exclusions:

- **<100× solar metallicity ruled out:** [[L168-9b]], [[TOI-776b]].
- **<180–240× solar ruled out:** [[TOI-776c]] (model-dependent MMW limit 2.8–7.7 g/mol).
- **<250× solar ruled out:** [[TOI-836b]] (no H₂-dominated atmosphere).
- **<300× solar ruled out:** [[L98-59c]].
- **<300–500× solar ruled out:** [[GJ357b]] (MMW > 8 g/mol at 3σ).

Together these results frame the small-planet sample as **systematically high-MMW or cloudy** at the precision of current G395H retrievals — consistent with secondary atmospheres or thick aerosol decks, but not directly distinguishing the two.

## History

- **Cycle 1 (2024).** First two COMPASS papers: [[2024_Scarsdale_L98-59c]] and [[2024_Alderson_TOI-836b]] — establish the two-pipeline featureless-spectrum framing.
- **2025 surge.** Four more individual-target papers: [[2025_Alderson_TOI-776b]], [[2025_Teske_TOI776c]], [[2025_Redai_GJ357b]], [[2025_Alam_L168-9b]] (also extends to MIRI/LRS for the first 3–12 μm broadband on a rocky planet).
- **Uniform reanalysis (late 2025).** [[2025_Gordon_COMPASS-G395H]] cross-cuts the first seven targets with the new RPF-PCA systematics model; introduces NRS1/NRS2 detector-offset statistics across the sample and quantifies PandExo under-prediction. Brings TOI-836 c into the wiki as a stub-only target.

## Trade-offs

- **Single-instrument, single-mode design.** G395H gives spectroscopy at 2.8–5.2 μm only; key features (CH₄ Q-branch in the NRS gap, 1.4 μm H₂O on NIRISS, 15 μm CO₂ on MIRI) are out of band. The MIRI extension on [[L168-9b]] ([[2025_Alam_L168-9b]]) is the only multi-instrument follow-up so far.
- **NRS1/NRS2 detector offsets.** [[2025_Alderson_TOI-776b]] requires an offset for Visit-2 consistency; treatment varies across the sample; [[2025_Gordon_COMPASS-G395H]] is the first systematic characterization.
- **Featureless spectra under-determine free retrievals.** All metallicity bounds inherit forward-model assumptions; [[2025_Teske_TOI776c]] documents 2.8–7.7 g/mol MMW spread between equilibrium and mixture priors on the same TOI-776 c data.
- **Population-level inference still pending.** The wiki has six individual-target plus one survey-reanalysis paper; a unified COMPASS-wide demographic synthesis (Batalha et al. 2023 program-design paper not yet ingested) remains the natural next step.

## Open issues

- **Bare rock vs high-MMW atmosphere on the super-Earths.** Featureless transmission cannot distinguish the two; companion eclipse/MIRI follow-up is the natural arbiter (see [[secondary-eclipse-spectroscopy]] and the [[GJ486b]] template).
- **Sub-Neptune diversity context.** [[TOI-776c]] (featureless) sits alongside [[K2-18b]] (Hycean candidate), [[TOI-270d]] (clear CH₄+CO₂), and [[LP-791-18c]] (CH₄+haze, no CO₂) — the COMPASS featureless cases anchor the "aerosol/high-MMW" end of an emerging diversity picture (cf. [[2025_Roy_LP791-18c]]).
- **Remaining four targets.** Four of the eleven program targets have not yet been published in the wiki.

## Papers

### Individual-target spectra (newest first)
- [[2025_Alam_L168-9b]] — first 3–12 μm broadband (NIRSpec G395H + MIRI/LRS) on a rocky exoplanet; featureless; <100× solar excluded.
- [[2025_Redai_GJ357b]] — single G395H transit; featureless; MMW > 8 g/mol; <300–500× solar excluded.
- [[2025_Alderson_TOI-776b]] — two G395H transits; flat after detector-offset correction; <100× solar excluded.
- [[2025_Teske_TOI776c]] — two-visit joint fit; featureless 3–5 μm; <180–240× solar excluded.
- [[2024_Scarsdale_L98-59c]] — two-visit joint fit; featureless; <300× solar excluded; H₂/CO₂ ≥10% mixtures excluded at 3σ.
- [[2024_Alderson_TOI-836b]] — two-visit joint fit; flat; H₂-dominated <250× solar excluded.

### Uniform survey reanalysis
- [[2025_Gordon_COMPASS-G395H]] — uniform [[ExoTiC-JEDI]] reanalysis of seven targets; introduces RPF-PCA systematics model; NRS1/NRS2 offset statistics; PandExo under-prediction.
