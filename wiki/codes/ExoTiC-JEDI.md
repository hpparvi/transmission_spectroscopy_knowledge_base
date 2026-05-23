---
type: code
aliases: [ExoTiC-JEDI pipeline, Exoplanet Timeseries Characterisation — JWST Extraction and Diagnostic Investigator]
tags: [jwst-pipeline, data-reduction, time-series, nirspec, hub]
---

# ExoTiC-JEDI

An end-to-end JWST time-series reduction pipeline (Alderson et al. 2022, 2023; not yet ingested; github.com/Exo-TiC/ExoTiC-JEDI), performing full extraction, reduction, and light-curve fitting from `_uncal` files through to planetary spectra. Common configuration: custom destriping for 1/f noise removal at the group level, custom bias subtraction, and column-by-column outlier rejection. The Bristol-group pipeline of choice; the canonical second pipeline in the [[JWST-GO-2512-COMPASS]] workflow alongside [[Eureka]], and a standard cross-check in BOWIE-ALIGN, DREAMS, and ERS-era hot-Jupiter analyses. Generalized into the **RPF-PCA systematics model** (PCA of relative pixel fluxes) for low-groups-per-integration G395H observations in the COMPASS uniform reanalysis ([[2025_Gordon_COMPASS-G395H]]).

## Variants

The wiki sees four ExoTiC-JEDI deployment patterns:

- **COMPASS dual-reduction primary.** ExoTiC-JEDI + Eureka is the canonical [[JWST-GO-2512-COMPASS]] pairing; small-planet G395H transits run both pipelines as primaries with joint-fit final spectra:
  - [[2024_Scarsdale_L98-59c]], [[2024_Alderson_TOI-836b]], [[2025_Alderson_TOI-776b]] — all use this two-pipeline COMPASS workflow.
  - [[2025_Teske_TOI561b]] — same workflow extended to the four TOI-561 b secondary eclipses.
- **BOWIE-ALIGN three-pipeline cross-check.** ExoTiC-JEDI + [[Eureka]] + [[Tiberius]]:
  - [[2025_Ahrer_KELT7b]] — KELT-7 b NIRSpec G395H BOWIE-ALIGN transit; consistent with Eureka and Tiberius within ~50 ppm; parametric systematic model with cross-correlated trace position.
- **DREAMS GTO transmission cross-check.** ExoTiC-JEDI + [[transitspectroscopy]]:
  - [[2025_Gressier_HATP26b]] — HAT-P-26 b NIRSpec G395H BOTS; least-squares + parametric systematic model (no GP); both reductions agree at 1σ on transmission spectrum.
- **TRAPPIST-1 PRISM three-pipeline cross-check.** ExoTiC-JEDI + [[Eureka]] + [[transitspectroscopy]]:
  - [[2025_Espinoza_TRAPPIST1e]] — one of three independent reductions for four TRAPPIST-1 e PRISM transits.

Plus several primary or three-way roles:
- [[2025_Bennett_GJ1132b]] — one of three independent reductions for four-visit GJ 1132 b G395H+G395M coadd.
- [[2025_Fisher_TOI1685b]] — one of three (Eureka primary, ExoTiC-JEDI, transitspectroscopy) for five TOI-1685 b G395H transits.
- [[2023_May_GJ1132b]] — one of three independent reductions for two GJ 1132 b G395H transits.
- **Population-level reanalysis with RPF-PCA.** [[2025_Gordon_COMPASS-G395H]] is the **sole pipeline** for the uniform reanalysis of seven COMPASS NIRSpec G395H targets; introduces the **RPF-PCA systematics model** (PCA of relative pixel fluxes, fit as a 6-vector basis) as a new default for low-groups-per-integration G395H observations. The RPF-PCA workflow is now the COMPASS standard.

## History

- **2022–2023** — ExoTiC-JEDI introduced (Alderson 2022, 2023). Adopted as the COMPASS second pipeline alongside Eureka.
- **2023** — first wiki appearances on rocky-planet G395H transits ([[2023_May_GJ1132b]], plus the early COMPASS rocky-planet papers).
- **2024** — solidifies as the COMPASS dual-pipeline workhorse ([[2024_Alderson_TOI-836b]], [[2024_Scarsdale_L98-59c]]).
- **2025** — uniform reanalysis paper [[2025_Gordon_COMPASS-G395H]] establishes RPF-PCA as a forward-leaning systematics model; ExoTiC-JEDI extends to BOWIE-ALIGN, DREAMS, and TRAPPIST-1 PRISM contexts.

## Trade-offs

- **Strength: COMPASS-program standardization.** Identical reduction setup across COMPASS targets enables population-level reanalysis ([[2025_Gordon_COMPASS-G395H]]). Reduction-uniformity is hard to achieve with Eureka alone because each user reconfigures the ECF.
- **Strength: RPF-PCA innovation.** The relative-pixel-fluxes PCA basis ([[2025_Gordon_COMPASS-G395H]]) is now a community-standard alternative to single-trace decorrelation for low-groups-per-integration NIRSpec G395H — a methodology contribution that originated in this pipeline.
- **Strength: Independence from Eureka.** ExoTiC-JEDI parametric systematics models are simpler and use distinct light-curve-fitting machinery (least-squares vs. emcee/dynesty); Bayes-factor cross-checks against Eureka are statistically meaningful.
- **Limitation: Less downstream-integrated than Eureka.** Light-curve fitting and retrieval-input formatting require user-built glue code; Eureka's stage-5/6 modules are tighter.
- **Limitation: NIRISS/SOSS support secondary.** ExoTiC-JEDI's NIRSpec focus is dominant; NIRISS reductions live elsewhere ([[exoTEDRF]], [[supreme-SPOON]]).

## Open issues

- **NRS1/NRS2 detector-offset handling.** [[2025_Alderson_TOI-776b]] explicitly documents NIRSpec G395H NRS1/NRS2 detector offsets that ExoTiC-JEDI handles via per-detector free parameter; the practice is now standard but introduces an extra fitting parameter that other pipelines treat differently.
- **PandExo under-prediction of uncertainties.** [[2025_Gordon_COMPASS-G395H]] documents that PandExo predicts ~30% lower uncertainties than ExoTiC-JEDI delivers for low-groups-per-integration COMPASS observations; calibrating PandExo against this discrepancy is open.

## Papers

### COMPASS dual-reduction primary
- [[2025_Alderson_TOI-776b]] — TOI-776 b joint primary with Eureka.
- [[2024_Alderson_TOI-836b]] — TOI-836 b joint primary with Eureka.
- [[2024_Scarsdale_L98-59c]] — L 98-59 c joint primary with Eureka.
- [[2025_Teske_TOI561b]] — four TOI-561 b secondary eclipses; Eureka cross-check.

### COMPASS uniform reanalysis
- [[2025_Gordon_COMPASS-G395H]] — sole pipeline; introduces RPF-PCA; quantifies NRS1/NRS2 detector offsets and PandExo under-prediction across seven targets.

### BOWIE-ALIGN / DREAMS / single-target cross-checks
- [[2025_Ahrer_KELT7b]] — three-pipeline cross-check (Eureka + ExoTiC-JEDI + Tiberius); ~50 ppm consistency.
- [[2025_Gressier_HATP26b]] — primary [[transitspectroscopy]], ExoTiC-JEDI cross-check; 1σ agreement.

### Multi-pipeline rocky-planet cross-checks
- [[2025_Bennett_GJ1132b]] — one of three reductions for four-visit GJ 1132 b coadd.
- [[2025_Fisher_TOI1685b]] — one of three for five TOI-1685 b G395H transits.
- [[2023_May_GJ1132b]] — one of three for two GJ 1132 b G395H transits.
- [[2025_Espinoza_TRAPPIST1e]] — one of three for four TRAPPIST-1 e PRISM transits.

### GEMS
- [[2025_Canas_TOI5205b]] — primary reduction (with [[Eureka]] cross-check at <1σ) for 3 NIRSpec PRISM transits of TOI-5205 b under [[JWST-GO-3171]]; downstream retrievals use ExoTiC-JEDI co-added spectrum.
