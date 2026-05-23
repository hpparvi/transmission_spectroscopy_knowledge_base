---
type: paper
bibkey: 2025_Connors_MIRI-15um
authors: [Connors, N. J., Monaghan, C., Benneke, B., Dang, L.]
year: 2025
venue: ApJL 989:L11
doi: 10.3847/2041-8213/adee0d
targets: [TRAPPIST-1b, TRAPPIST-1c, LHS1478b, TOI-1468b, LHS1140c]
instruments: [JWST-MIRI]
methods: [secondary-eclipse-spectroscopy, multi-visit-stacking]
codes: [Erebus, Eureka, SCARLET, SPHINX]
tags: [miri-f1500w, photometric-eclipse, rocky-planet, m-dwarf-host, methodology, reanalysis, systematics]
ingested: 2026-04-29
---

# Uniform Reanalysis of JWST MIRI 15 μm Exoplanet Eclipse Observations Using Frame-normalized Principal Component Analysis

**Authors:** Connors, Monaghan, Benneke, Dang (2025, ApJL 989:L11) · DOI: 10.3847/2041-8213/adee0d
**Targets:** [[TRAPPIST-1b]], [[TRAPPIST-1c]], [[LHS1478b]], [[TOI-1468b]], [[LHS1140c]] · **Instrument:** [[JWST-MIRI]] (F1500W photometric imaging)

## TL;DR

Introduces **frame-normalized principal component analysis (FN-PCA)** — a data-driven, non-parametric detrending method for JWST MIRI F1500W photometric eclipse light curves — and applies it uniformly to 17 published F1500W eclipse observations of 5 small rocky planets ([[TRAPPIST-1b]], [[TRAPPIST-1c]], [[LHS1478b]], [[TOI-1468b]], [[LHS1140c]]). Implemented in the new open-source pipeline [[Erebus]]. Joint-fit eclipse depths agree with published values within ~1σ on most targets but yield a notably **cooler dayside for [[TRAPPIST-1c]]** (T_day = 344 +43/−52 K vs Zieba et al. 2023's 380 ± 31 K; not yet ingested), strengthening the atmospheric / high-albedo case for that planet. Characterizes the MIRI 15 μm detector-settling timescale empirically: T_settle [hr] = 0.063 exp(0.427 m_K) − 0.657, in preparation for the 500 hr JWST Rocky Worlds DDT survey.

## Key findings

| Planet | Visits | FN-PCA depth (ppm) | T_day (K) | Atmospheric conclusion |
|---|---|---|---|---|
| [[TRAPPIST-1b]] | 5 | 863 ± 90 | 499 ± 24 | Bare rock, low surface albedo |
| [[TRAPPIST-1c]] | 4 (visit 1 nondetection) | 312 ± 128 | 344 +43/−52 | Semireflective bare rock OR thin O₂/CO₂ atmosphere |
| [[LHS1478b]] | 2 (visit 2 nondetection) | 86 ± 66 | 583 +108/−115 (visit 1 only) | Rules out dark bare rock at ~2σ; CO₂-bearing atmosphere or A_B ≈ 0.66 bare rock |
| [[TOI-1468b]] | 3 | 286 ± 39 | 964 +78/−83 | Hotter than bare-rock prediction; deep-eclipse anomaly unexplained |
| [[LHS1140c]] | 3 | 242 ± 35 | 528 +32/−36 | Rules out atmosphere; consistent with low-albedo bare rock |

- **TRAPPIST-1 c cooling.** FN-PCA dayside is ~36 K cooler than Zieba et al. 2023 (not yet ingested), 1σ from their value but pushing the result further into the atmosphere / reflective-surface region of parameter space; potential tension flagged below.
- **Empirical detector-settling law.** Across 17 observations spanning K-mag 5–11, settling timescale follows T_settle [hr] = 0.063 exp(0.427 m_K) − 0.657 — a calibration deliverable for [[JWST-Rocky-Worlds-DDT]] survey planning.
- **Bias in eclipse-depth priors.** Negative-allowed priors are necessary for nondetection visits; positive-only priors mistakenly inflate depth from eclipse egress (TRAPPIST-1 c visits 3, 4).

## Methods

**FN-PCA detrending.** Each MIRI image frame is normalized by its total intensity before PCA, removing the astrophysical signal (eclipse + stellar variability) — which appears as uniform whole-detector flux changes — from the input cube. PCA is run on background-subtracted, frame-normalized image cubes via `sklearn`; the top 5 principal-component eigenvalue time series serve as non-parametric systematic regressors. Detrending model: F_sys = (1 + Σ c_i λ_i) · (a t + b), fit jointly with `batman` eclipse model and `emcee` MCMC.

**Pipeline.** New open-source pipeline [[Erebus]] (github.com/nicholasconnors/erebus) implements stages 1–3 around `jwst` calibration outputs. [[Eureka]] used for stage 2 of TRAPPIST-1 b visit 5 only. SPHINX stellar models recalibrated against measured F1500W flux (default models overestimate TRAPPIST-1 mid-IR flux). Bare-rock surface modeling via JESTER (Monaghan et al., in prep). Atmospheres modeled with [[SCARLET]].

**Reanalyzed datasets.**
- [[TRAPPIST-1b]] — GTO-1177 (PI Greene; original analysis Greene et al. 2023, not yet ingested) + GO-3077 phase curve.
- [[TRAPPIST-1c]] — GO-2304 (PI Zieba; original analysis Zieba et al. 2023, not yet ingested).
- [[LHS1478b]] — [[JWST-GO-3730]] Hot Rocks Survey (PI August; August et al. 2025, not yet ingested).
- [[TOI-1468b]] — [[JWST-GO-3730]] Hot Rocks Survey (Valdés et al. 2025, not yet ingested).
- [[LHS1140c]] — [[JWST-GO-3730]] Hot Rocks Survey (Fortune et al. 2025, not yet ingested).
- Systematics-only (used for detector-settling characterization, no atmospheric reanalysis): GJ 357 b, GJ 3473 b, LTT 3780 b, TOI 175 c, TOI 270 b, HD 260655 b, LP 791-18 d, LHS 1140 b.

## Caveats & limitations

- **Eclipse-depth bias on negative depths.** Pipeline can mistake eclipse egress for spurious depth (TRAPPIST-1 c visits 3, 4); negative-allowed priors required for unbiased nondetection handling.
- **TRAPPIST-1 c visit 4** required a 2nd-degree polynomial for residual stellar variation FN-PCA didn't capture.
- **Bare-rock model uncertainties** from chemical contaminants, mineralogical mixtures, and space weathering; lab reflectance only available below 20 μm.
- **SPHINX overestimates TRAPPIST-1 mid-IR flux**; recalibrated against measured F1500W.
- **LHS 1478 b conclusions limited** because visit 2 had to be discarded.

## Open questions / follow-ups

- Does the cooler TRAPPIST-1 c dayside hold up under additional visits? GO-7675 LHS 1478 b follow-up will test the visit-2 nondetection there; equivalent re-observation of TRAPPIST-1 c is the natural next step.
- TOI-1468 b's hot-anomaly origin — atmospheric, geological, or pipeline?
- Will FN-PCA generalize cleanly to other MIRI filters (F1280W, F2100W) and to MIRI/LRS spectroscopic time series?

## Tensions

- **TRAPPIST-1 c dayside temperature.** FN-PCA T_day = 344 +43/−52 K; Zieba et al. 2023 (not yet ingested) reported 380 ± 31 K. Difference is ~1σ but consistently in the atmosphere-favoring direction. Connors et al. attribute the shift to detrending choice; data themselves are unchanged. Status: not a contradiction, but reduces the bare-rock margin.

## Related

- [[2025_Xue_GJ3929b]] — independent MIRI F1500W eclipse on a comparable rocky planet (bare rock).
- [[2024_Xue_GJ1132b]], [[2024_WeinerMansfield_GJ486b]], [[2024_Wachiraphan_LTT1445Ab]] — MIRI/LRS eclipse spectroscopy bare-rock results.
- [[2026_Coy_HD3167b]] — MIRI/LRS eclipse on a USP super-Earth showing R = 0.57 (atmospheric / high-albedo evidence).
