---
type: paper
bibkey: 2025_Schmidt_K2-18b
authors: [Schmidt, S. P., MacDonald, R. J., Tsai, S.-M., Radica, M., Wang, L.-C., Ahrer, E.-M., Bell, T. J., Fisher, C., Thorngren, D. P., Wogan, N., May, E. M., Ferrari, P., Bennett, K. A., Rustamkulov, Z., López-Morales, M., Sing, D. K.]
year: 2025
venue: Submitted to AAS Journals
arxiv: 2501.18477
targets: [K2-18b]
instruments: [JWST-NIRISS, JWST-NIRSpec]
methods: [atmospheric-retrievals, transit-spectroscopy, transit-light-source-effect]
codes: [POSEIDON, BeAR, FIREFLy, exoTEDRF, Eureka, batman, emcee, PyMultiNest, Photochem, PICASO, VULCAN, HELIOS, lacosmic, pastasoss, exoUPRF, lmfit, Fastchem, exotic-ld]
species_detected: [CH4]
species_ruled_out: [DMS, CO2, H2O, NH3, HCN, CO, CS2, OCS, N2O, CH3Cl]
tags: [sub-neptune, k2-18b, jwst-ers, biosignature-debate, hycean, dms, transit-light-source-effect, mini-neptune, reanalysis]
ingested: 2026-05-18
---

# A Comprehensive Reanalysis of K2-18 b's JWST NIRISS+NIRSpec Transmission Spectrum

**Authors:** Schmidt, MacDonald, Tsai, Radica, et al. (2025, submitted AAS) · [arXiv:2501.18477]
**Targets:** [[K2-18b]] · **Instruments:** [[JWST-NIRISS]] (SOSS), [[JWST-NIRSpec]] (G395H)

## TL;DR
First independent comprehensive reanalysis of K2-18 b's JWST NIRISS SOSS + NIRSpec G395H transmission spectra ([[JWST-GO-2722]]). Two reduction pipelines for NIRISS ([[FIREFLy]], [[exoTEDRF]]), four for NIRSpec ([[FIREFLy]], [[exoTEDRF]], two [[Eureka]] variants), the first-ever analysis of the NIRISS SOSS 2nd order, multiple spectral resolutions, two independent retrieval codes ([[POSEIDON]] and the newly introduced [[BeAR]]), and >250 retrievals across 60 data combinations. CH₄ is robustly detected at 4.2⁺⁰·⁷₋₀·₉ σ (log CH₄ = −1.15⁺⁰·⁴⁰₋₀·₅₂; ≈7%). **No statistically significant or reliable evidence is found for CO₂ (max 2.3σ; log CO₂ < −1.70 at 95%) or DMS (max 2.2σ; log C₂H₆S < −3.70 at 95%)**. The revised composition is compatible with an oxygen-poor mini-Neptune (C/O ≳ 3) without requiring a liquid water surface or life.

## Key findings

- **CH₄ robustly detected.** Across all 60 data combinations the CH₄ detection significance exceeds 2.7σ; the ensemble averaged significance is **4.2⁺⁰·⁷₋₀·₉ σ** ([[POSEIDON]]), confirmed by [[BeAR]] at 3.5–4.5σ across four checked combinations. Retrieved abundance log CH₄ = **−1.15⁺⁰·⁴⁰₋₀·₅₂** (≈7%); consistent with Madhusudhan et al. 2023 (not ingested)'s −1.74⁺⁰·⁵⁹₋₀·₆⁹ at ~1σ. The high CH₄ value is similar to deep Neptune (4 ± 1%) and is compatible with a metal-enriched mini-Neptune.
- **CO₂ — no reliable detection.** The maximum significance across all 60 NIRISS×NIRSpec data combinations is **2.3σ** (Bayes factor < 5; "weak evidence at best" on Jeffreys' scale). Most combinations show **no evidence at all** (Bayes factor < 3, denoted "−" in Figure 5). 95% upper limit log CO₂ < −1.70 from the ensemble. The CO₂ detection in Madhusudhan et al. 2023 (not ingested) is shown in Appendix A to reach at most 2.5σ when applied to their JExoRES data — i.e. **the apparent CO₂ feature is a reduction-specific artifact**, not a robust atmospheric signal.
- **DMS — no reliable detection.** Maximum significance 2.2σ for a single data combination ([[exoTEDRF]] R≈100); marginal hints disappear at higher resolution or with FIREFLy reductions. 95% upper limit log C₂H₆S < −3.70. The paper's central conclusion: **the DMS inference of [[2025_Madhusudhan_K2-18b-MIRI]] is reduction-and-resolution-dependent and not statistically robust** when explored across the full space of reasonable data-level choices.
- **All other proposed biosignatures: non-detections.** 95% upper limits: log CS₂ < −3.29, log CH₃Cl < −2.11, log OCS < −3.09, log N₂O < −2.98.
- **H₂O and NH₃ depleted from the gas phase.** log H₂O < −3.05, log NH₃ < −5.25 at 95%. The paper argues these depletions need not require a liquid water ocean: a deep magma layer can sequester NH₃ (Shorttle et al. 2024 (not ingested) — not yet ingested), and high C/O ratios (≳3) plus condensation can deplete H₂O in a mini-Neptune.
- **Hycean scenario challenged on a new front.** Photochemical-climate models ([[Photochem]] + [[PICASO]], [[VULCAN]] + [[HELIOS]]) show CH₄ in a thin H₂ hycean atmosphere is photochemically converted to CO₂ on ~10–100 Myr. Given the robust CH₄ detection but non-detection of CO₂, the hycean steady state is hard to reconcile without an active CH₄ source replenishing what photochemistry destroys. An oxygen-poor mini-Neptune (C/O = 3.25 in the self-consistent model) naturally explains the CH₄ abundance and the H₂O/CO₂ non-detections **without invoking life or a surface ocean**.
- **First analysis of NIRISS SOSS 2nd order.** Both [[FIREFLy]] and [[exoTEDRF]] extract the 2nd-order spectrum (0.6–0.85 μm), tightening CH₄ detection significance from ~3.3σ (R≈25) to ~4.5σ (R≈100). The 2nd-order data also drives the inference of cool unocculted starspots.
- **Unocculted starspot detection (5⁺³₋₂% coverage).** The two-heterogeneity stellar contamination model retrieves f_spot = 0.05⁺⁰·⁰³₋₀·₀₂ at ΔT ≈ 500 ± 350 K cooler than the photosphere. Including stellar contamination does *not* alter the inferred atmospheric composition meaningfully — but the 2nd-order NIRISS data is what enables this detection. Madhusudhan et al. 2023 (not ingested) reported no stellar contamination but did not include the 2nd-order data.
- **Updated planet mass from transmission spectrum.** Ensemble retrieval gives M_p = 8.46⁺¹·¹³₋₁·¹⁵ M_⊕, modestly tighter than radial-velocity (8.63 ± 1.35 M_⊕; Cloutier 2019).
- **Pipeline-and-resolution sensitivity is the dominant systematic.** Marginal CO₂ or DMS hints depend on (i) coupling FIREFLy NIRSpec data with exoTEDRF R≈100 or 2-pixel NIRISS, OR (ii) using exoTEDRF R≈100/R≈200 NIRSpec data; they disappear at pixel-level resolution. The paper formalizes this as the "ensemble posterior" — marginalizing over 60 data variants — which is a methodological contribution beyond K2-18 b.

## Methods

- **NIRISS SOSS reductions.** Two pipelines:
  - [[FIREFLy]] (recently updated for NIRISS SOSS; Liu & Wang, Wang et al. in prep): start from uncal; custom group-level 1/f via zodiacal-background subtraction with pickoff-mirror flux-jump correction; skip dark current and jump steps; pastasoss for wavelength + order tracing; 15σ temporal outliers; box extraction 30-pixel order 1, 23-pixel order 2.
  - [[exoTEDRF]]: scale-achromatic 1/f at group level; piece-wise SOSS background scaling (Lim 2023, Fournier-Tondreau 2024a); exoTEDRF-custom 10σ jump; edgetrigger order tracing; 30-pixel box aperture.
- **NIRSpec G395H reductions.** Four reductions: [[FIREFLy]], [[exoTEDRF]], and two [[Eureka]] variants ("A" using default flow + custom bias and `lacosmic` outlier cleaning; "B" following Schlawin et al. 2024 — used in [[2025_Madhusudhan_K2-18b-MIRI]] flow).
- **Spot-crossing event in NIRISS light curves.** Trimmed in FIREFLy; modeled as a Gaussian in exoTEDRF (informed by Roy et al. in prep). The choice between Gaussian modeling and trimming has negligible impact on resulting spectra.
- **Retrieval — [[POSEIDON]] reference.** 28 free parameters; H₂-He background; ExoMol updated CH₄ MM line list (2024_Yurchenko_CH4 not yet ingested); one-heterogeneity TLS model with PHOENIX grid; opacity sampling at R = 100,000; PyMultiNest with 1,000 live points; ~50 CPU-years total. 240 retrievals across 60 data combinations × 4 (reference + 3 nested for CH₄, CO₂, DMS Bayes factors).
- **Retrieval — [[BeAR]] cross-check.** Bern Atmospheric Retrieval (formerly Helios-r2; Kitzmann 2020, Fisher 2024 — not yet ingested); isothermal T; opaque cloud deck; two-heterogeneity stellar model (blackbody photosphere + spot + facula); R = 60,000 opacity sampling; PyMultiNest. Applied to 4 (FIREFLy + exoTEDRF) × (R≈100 + pixel-level) combinations. Gives results in "excellent agreement" with POSEIDON.
- **Atmosphere & interior modeling.** Self-consistent photochemical-climate iteration with two independent code pairs: [[Photochem]] + [[PICASO]] and [[VULCAN]] + [[HELIOS]]. Equilibrium chemistry exploration via Fastchem. Four scenarios tested: mini-Neptune with water clouds, oxygen-poor (high C/O) mini-Neptune, hycean planet, supercritical ocean. Interior structure: Chabrier & Debras 2021 H/He EoS, Mazevet 2019 H₂O EoS, with thermal evolution from Fortney 2007.

## Caveats & limitations

- **Pipeline-version sensitivity is real but framed as a strength**: the ensemble-posterior method explicitly marginalizes over data-level choices, but does not eliminate the possibility that *all* pipelines share a common bias against weak features.
- **Stellar contamination signal is shallow.** f_spot ≈ 5% is small enough that "the stochastic nature of the transit light source effect" (paper's wording) means further repeat observations are recommended. Continued NIRISS SOSS coverage (especially at <1 μm) is advocated as prudent.
- **CH₄ source mechanism on a putative hycean K2-18 b is open.** Even with their robust CH₄ detection, sustaining 7% CH₄ in a thin hycean H₂ atmosphere requires an active source equivalent to ≥20× Earth's marine flux (Tsai et al. 2024 not ingested; Wogan et al. 2024 also notes this).
- **Inability to distinguish supercritical-ocean scenarios.** Without an effective climate model that can track transitions from supercritical to subcritical states, the CH₄/CO₂ retrievals cannot uniquely test the Benneke et al. 2024 (TOI-270 d analog) supercritical-water-mixed-into-H₂ scenario.
- **No haze ruled out**, but the loose cloud-pressure constraint (log P_cloud > −6.41 only) means an upper-altitude haze remains compatible if shallow.

## Open questions / follow-ups

- Direct test of the high-C/O oxygen-poor mini-Neptune scenario via CO₂ and CO upper limits at higher precision (the paper notes future programs such as **GO-2372 (PI: R. Hu)** would help). Implies cycle-3+ JWST follow-up.
- Whether continued NIRISS SOSS observations will confirm or contradict the 5% spot-coverage inference. The TLS signal here is shallow enough that stochastic spot evolution between epochs could change the picture.
- Whether the [[2025_Madhusudhan_K2-18b-MIRI]] DMS+DMDS MIRI detection (3.4σ) survives this kind of ensemble analysis. Schmidt et al.'s methodology is built for NIRISS+NIRSpec; the MIRI evidence remains untested by this paper.
- Schmidt et al. explicitly highlight the framework as portable: "to our knowledge, this conceptually simple — but computationally expensive — technique is novel for atmospheric inferences from JWST data." It is the strongest statement to date that the K2-18 b NIRISS+NIRSpec data alone do not warrant biosignature claims.

## Related
- Madhusudhan et al. 2023 (not ingested) — the paper whose statistical claims this work re-examines and largely overturns for CO₂ and DMS, while confirming CH₄.
- [[2025_Madhusudhan_K2-18b-MIRI]] — the MIRI follow-up that this paper does *not* reanalyze; DMS/DMDS MIRI claim untouched here.
- [[2025_Luque_K2-18b]] — concurrent panchromatic NIRISS+NIRSpec+MIRI joint retrieval that also fails to detect DMS/DMDS; complementary approach.
- [[2025_PicaCiamarra_K2-18b]] — 650-molecule agnostic search that independently rules out DMS at high significance.
- [[2025_Taylor_K2-18b-MIRI]] — model-agnostic Gaussian critique of the MIRI-specific DMS claim.
- [[K2-18b]] — target hub with the full controversy chronology.
