---
type: code
aliases: [Eureka!, Eureka pipeline]
tags: [jwst-pipeline, data-reduction, time-series, hub]
---

# Eureka!

An end-to-end open-source JWST time-series reduction pipeline (Bell et al. 2022; not yet ingested), wrapping the STScI `jwst` pipeline for stages 1–2 and providing custom background subtraction, optimal spectral extraction, light-curve fitting, and spectroscopic binning for stages 3–5. Eureka! is by a wide margin the most frequently used reduction in this wiki — appearing as primary or independent cross-check reduction in 20 of the 28 ingested papers — and has effectively become the default reference pipeline for JWST exoplanet transit and eclipse work across NIRSpec G395H/G395M, NIRSpec PRISM, NIRISS/SOSS, and MIRI/LRS.

## Variants

Eureka! is highly modular: each pipeline stage exposes an `ECF` (Eureka! Control File) so users typically configure rather than fork. The wiki sees three recurring deployment patterns:

- **Primary reduction in two-pipeline cross-checks.** Eureka! + [[ExoTiC-JEDI]] is the canonical pairing for the COMPASS program ([[JWST-GO-2512-COMPASS]]) on small-planet G395H transits. Used in [[2024_Scarsdale_L98-59c]], [[2024_Alderson_TOI-836b]], [[2025_Alderson_TOI-776b]], [[2025_Teske_TOI776c]] (joint-fit primary), [[2025_Teske_TOI561b]] (with ExoTiC-JEDI cross-check on emission), and others.
- **Primary reduction in three-pipeline cross-checks.** For higher-stakes results, Eureka! is paired with [[FIREFLy]] and [[Tiberius]] (e.g. [[2023_Lustig-Yaeger_LHS475b]], [[2023_Moran_GJ486b]]) or [[FIREFLy]] and [[ExoTiC-JEDI]] ([[2023_May_GJ1132b]]).
- **Independent cross-check** alongside reductions written from scratch (notably [[SPARTA]] for MIRI/LRS — [[2024_Xue_GJ1132b]], [[2024_WeinerMansfield_GJ486b]], [[2024_Wachiraphan_LTT1445Ab]], [[2026_Coy_HD3167b]]) — verifying that Eureka! and a STScI-pipeline-independent reduction agree.

The pipeline has also been wrapped with light-curve fitting modules from other groups; the **Eureka! + ExoTEP** variant in [[2026_RoyPerez_WASP39b]] is one example.

## History

Adoption is uniform across cycles. Versioning matters for small-planet reductions (Bennett 2025 explicitly notes updated calibrations between visits; Teske TOI-776c uses v1.11.4; Teske TOI-561b uses v1.13). Group-level (stage 1) custom background subtraction has become a recurring feature in [[JWST-GO-2512-COMPASS]] and rocky-planet eclipse work.

## Trade-offs

- **Strength:** Modularity. Reductions can be reproduced from the ECF without code modification, easing cross-team validation.
- **Strength:** Active development; cycle-aware calibration updates land quickly.
- **Limitation:** Inherits stage 1–2 behavior from the STScI `jwst` pipeline. Pipelines like [[SPARTA]], [[Frida]], and [[FIREFLy]] (custom 1/f / superbias) exist precisely to provide independent cross-checks against STScI-pipeline systematics.
- **Limitation:** [[2026_RoyPerez_WASP39b]] documents that Eureka! retrievals on the same WASP-39 b ERS PRISM dataset can differ from FIREFLy / Tiberius / Tshirt by up to 2 dex in retrieved abundances — pipeline choice within Eureka! is itself a non-trivial systematic.

## Open issues

- **Cross-pipeline reproducibility.** Several wiki papers ([[2023_May_GJ1132b]], [[2023_Moran_GJ486b]], [[2026_RoyPerez_WASP39b]]) document significant Eureka!-vs-other discrepancies. The community has no standardized comparison protocol.
- **Detector-offset handling on G395H.** Multiple small-planet papers ([[2025_Alderson_TOI-776b]], [[2023_May_GJ1132b]], [[2023_Moran_GJ486b]]) document NRS1/NRS2 detector offsets requiring per-paper correction; not yet handled uniformly.

## Papers

### Primary reduction
- [[2026_Coy_HD3167b]] — independent cross-check (primary: [[SPARTA]]) for HD 3167 b MIRI/LRS eclipse.
- [[2026_RoyPerez_WASP39b]] — Eureka!+ExoTEP variant; one of four pipelines in the WASP-39 b ERS PRISM data-reduction systematics study.
- [[2025_Tusay_K2-22b]] — primary MIRI/LRS reduction for four K2-22 b transit windows; 9.7σ detection in Obs 4.
- [[2025_Teske_TOI561b]] — primary reduction (alongside [[ExoTiC-JEDI]]) for four TOI-561 b G395H secondary eclipses.
- [[2025_PiauletGhorayeb_TRAPPIST1d]] — primary reduction for two TRAPPIST-1 d PRISM transits.
- [[2025_Fisher_TOI1685b]] — primary reduction for five TOI-1685 b G395H transits.
- [[2025_Teske_TOI776c]] — primary joint-fit reduction for both TOI-776 c visits; v1.11.4; custom group-level background subtraction.
- [[2025_Redai_GJ357b]] — cross-check reduction (primary: [[Tiberius]]) for GJ 357 b NIRSpec G395H transit.
- [[2025_Bennett_GJ1132b]] — one of three independent reductions across all four GJ 1132 b visits (G395H + G395M).
- [[2025_Alam_L168-9b]] — one of three independent NIRSpec reductions for L 168-9 b.
- [[2025_Alderson_TOI-776b]] — one of two independent reductions (alongside [[ExoTiC-JEDI]]) for TOI-776 b.
- [[2025_Espinoza_TRAPPIST1e]] — one of three independent reductions (primary: [[transitspectroscopy]]) for four TRAPPIST-1 e PRISM transits.
- [[2024_Xue_GJ1132b]] — cross-check reduction for GJ 1132 b MIRI/LRS secondary eclipse (primary: [[SPARTA]]).
- [[2024_WeinerMansfield_GJ486b]] — cross-check reduction (alongside [[SPARTA]]) for Gl 486 b MIRI/LRS eclipses.
- [[2024_Wachiraphan_LTT1445Ab]] — parallel reduction (alongside [[SPARTA]]) for LTT 1445 A b MIRI/LRS eclipses.
- [[2024_Scarsdale_L98-59c]] — primary reduction (alongside [[ExoTiC-JEDI]]) for L 98-59 c COMPASS spectrum.
- [[2024_Alderson_TOI-836b]] — one of two independent reductions (alongside [[ExoTiC-JEDI]]) for TOI-836 b joint-fit final spectrum.
- [[2023_May_GJ1132b]] — one of three independent reductions for two GJ 1132 b G395H transits; Eureka! used for the [[POSEIDON]] retrievals.
- [[2023_Moran_GJ486b]] — primary reduction for [[POSEIDON]] retrievals on GJ 486 b; most statistically significant flat-line rejection (3.20σ).
- [[2023_Lustig-Yaeger_LHS475b]] — one of three independent reductions for the LHS 475 b transmission spectrum.
- [[2025_LustigYaeger_WASP17b]] — primary reduction (Stages 1–6, pmap-locked) for the WASP-17 b NIRSpec G395H transit + secondary eclipse iESR-PIE analysis.
- [[2025_Connors_MIRI-15um]] — used for stage 2 of the TRAPPIST-1 b visit 5 reanalysis only; primary pipeline is the new [[Erebus]].
- [[2026_Radica_WASP96b]] — alternate NIRSpec G395H reduction for WASP-96 b (primary: [[exoTEDRF]]).
- [[2026_Ashtari_HATS75b]] — primary reduction for the three HATS-75 b NIRSpec PRISM transits in **two parallel variants**: optimized Eureka! + [[fleck]] + emcee, and manual Eureka! + [[spotrod]] + dynesty.
- [[2025_Ahrer_KELT7b]] — primary R = 400 reduction for KELT-7 b NIRSpec G395H BOWIE-ALIGN transit; emcee MCMC; mirror tilt event handled with step function.
- [[2025_Felix_TOI-270d]] — primary reduction (Stages 1–3 only) for TOI-270 d NIRSpec G395H + NIRISS SOSS reanalysis; uses [[BeAR]] retrieval at native resolution. Custom MCMC light-curve fitting replaces Eureka! Stage 5; smooth bias correction + 8σ jump threshold to avoid detector-offset artifacts; first wiki demonstration of Eureka! coupled with native-resolution + LSF retrieval.
- [[2025_FernandezRodriguez_K2-18b]] — primary NIRSpec G395H reduction (10σ jump threshold) for K2-18 b transit; produces 12 spectrum variants by varying limb-darkening + spot-correction + binning timing; followed by TauREx3 retrievals.
- [[2025_Sikora_HD80606b]] — primary reduction for the 20.9-hr HD 80606 b NIRSpec G395H partial phase curve; super_sample=3 for centroid stability; group-level 1/f and bias correction; HGA-jump correction via step-function model. Cross-checked against a custom difference-imaging pipeline.
- [[2025_Murphy_WASP107b]] — primary reduction for the WASP-107 b MIRI/LRS limb-resolved transit (Eureka v0.9, JWST pipeline 1.10.2, CRDS jwst_1097.pmap); chosen over [[Tshirt]] for MIRI because Eureka's tuning is better proven on MIRI noise systematics. NIRCam and NIRSpec visits used Tshirt instead.
- [[2025_Barat_V1298Tau-b]] — primary reduction for the V1298 Tau b NIRSpec G395H/SUB2048 transit (Stages 1–3); replaces refpix with column-by-column ROEBA correction; 6σ jump threshold; covariance-weighted optimal extraction. Followed by data-driven detrending of stellar variability + flare profile + post-flare oscillations. Cross-checked against the SPARTA pipeline.
- [[2025_Deka_WASP39b]] — Eureka-reduced JWST MIRI/LRS WASP-39 b spectrum is one of three pipelines (Eureka, Tiberius, SPARTA) cross-compared as input to the [[NEXOTRANS]] retrieval framework benchmark.
