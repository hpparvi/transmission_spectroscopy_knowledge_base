---
type: paper
bibkey: 2025_Splinter_WASP121b
authors: [Splinter, J., Coulombe, L.-P., Frazier, R. C., Cowan, N. B., Rauscher, E., Dang, L., Collins, S., Pelletier, S., Allart, R., MacDonald, R. J., Lafrenière, D., Albert, L., Benneke, B., Doyon, R., Jayawardhana, R., Johnstone, D., Krishnamurthy, V., Piaulet-Ghorayeb, C., Kaltenegger, L., Meyer, M. R., Taylor, J., Turner, J. D.]
year: 2025
venue: AJ 170:323
arxiv: ""
doi: 10.3847/1538-3881/ae0e52
targets: [WASP-121b]
instruments: [JWST-NIRISS]
methods: [secondary-eclipse-spectroscopy, atmospheric-retrievals]
species_detected: []
codes: [exoTEDRF, NAMELESS, Eureka, celerite]
tags: [ultra-hot-jupiter, phase-curve, bond-albedo, heat-redistribution, albedo-paradox, reflected-light, niriss-soss, neat-gto-1201]
ingested: 2026-05-22
---

# Precise Constraints on the Energy Budget of WASP-121 b from Its JWST NIRISS/SOSS Phase Curve

**Authors:** Splinter, Coulombe, Frazier, Cowan, Rauscher, Dang, Collins, Pelletier, Allart, MacDonald, Lafrenière, Albert, Benneke, Doyon, Jayawardhana, Johnstone, Krishnamurthy, Piaulet-Ghorayeb, Kaltenegger, Meyer, Taylor, Turner (2025, AJ 170:323, 20pp) · DOI: 10.3847/1538-3881/ae0e52
**Target:** [[WASP-121b]] · **Instrument:** [[JWST-NIRISS]] SOSS (0.6–2.85 μm; Orders 1 + 2)
**Program:** [[JWST-GTO-1201]] (NEAT GTO, PI: Lafrenière)
**Observation:** 36.9-hr full-orbit phase curve on 2023 Oct 26 (1 transit + 2 secondary eclipses)

## TL;DR

**First JWST/NIRISS/SOSS phase curve of an ultra-hot Jupiter**. The 0.6–2.85 μm bandpass captures 55–82 % of [[WASP-121b]]'s bolometric flux (vs ~20 % for the older [[HST-WFC3]] / [[JWST-NIRSpec]] phase curves), enabling the **most precise JWST energy-budget measurement to date** on this target. Two independent reductions ([[exoTEDRF]] fiducial, [[NAMELESS]] cross-check) yield consistent dayside / nightside effective temperatures **T_day = 2717 ± 17 K** and **T_night = 1562⁺¹⁸₋₁₉ K**, giving Bond albedo **A_B = 0.277 ± 0.016** and heat-recirculation efficiency **ε = 0.246 ± 0.014**. Bell EBM energy-balance modelling prefers similar A_B = 0.31 with a slow wind speed (~0.2 km s⁻¹) and ~1 bar mixed-layer depth — slow winds and deep layers consistent with magnetic drag / inefficient heat redistribution. Order 2 (0.6–0.85 μm) yields a **geometric albedo A_g = 0.093⁺⁰·⁰²⁹₋₀·⁰²⁷** (3σ upper limit 0.175) — **reinforcing the hot-Jupiter albedo paradox** (A_B 20–30 %, A_g ~10 %). At short wavelengths, **the phase offset shifts unexpectedly eastward** (5.1° ± 1.4° at 1.13 μm) with retained large phase-curve relative amplitudes — interpreted as reflected light from clouds on a slightly more reflective eastern dayside.

## Key findings

- **Phase-curve fitting** (Order 1 + Order 2 white light curves; 26 fitted parameters; 100 000 emcee steps × 4 walkers/param):
  - Eclipse depths: F_day (Order 1) = 1156⁺¹⁴.³⁰₋¹⁴.⁰⁴ ppm, F_day (Order 2) = 363⁺²⁰·⁷⁹₋²¹·⁶⁴ ppm.
  - Order 1 phase offset = **5.1° ± 1.4°** eastward; Order 2 phase offset = **10.5° ± 9.9°** (statistically insignificant).
- **Dayside / nightside effective temperatures**:
  - T_day = **2717 ± 17 K** (exoTEDRF) / 2717 ± 18 K (NAMELESS); identical between pipelines.
  - T_night = **1562⁺¹⁸₋₁₉ K** (exoTEDRF) / 1626⁺⁹·⁹₋₆·² K (NAMELESS).
  - Discrepancy in nightside driven entirely by treatment of negative planetary flux: exoTEDRF half-Gaussian penalty vs NAMELESS unconstrained.
- **Bond albedo + heat recirculation** (from T_day, T_night via Cowan & Agol 2011a):
  - **A_B = 0.277 ± 0.016**, **ε = 0.246 ± 0.014** (exoTEDRF).
  - NAMELESS gives A_B = 0.307 ± 0.018, ε = 0.186⁺⁰·⁰²¹₋⁰·⁰¹⁹ — 1.4σ tension on ε driven by warmer NAMELESS nightside.
- **Bell_EBM energy-balance fit** (Bell & Cowan 2018 not ingested):
  - A_B ≈ 0.31, V_wind ≈ 0.20 km s⁻¹, P_0 ≈ 1 bar — wind speeds **far slower** than GCM expectations (400–500 m s⁻¹, Davenport 2025 not ingested) and ~5× slower than ground-based high-resolution Doppler tracers (5.2 km s⁻¹, Mikal-Evans 2023 not ingested). Consistent with strong magnetic drag (Beltz 2022 not ingested) suppressing zonal winds.
  - Mixed-layer depth P_0 ~ 1 bar is **deeper than Spitzer phase curve inferences** (< 0.2 bar) — closer to expectations from Parmentier 2013 photon-deposition layer.
- **Geometric albedo (Order 2; 0.6–0.85 μm)**:
  - A_g = **0.093⁺⁰·⁰²⁹₋⁰·⁰²⁷** (3σ upper limit 0.175), consistent with TESS 0.6–0.95 μm (A_g = 0.07⁺⁰·⁰³⁷₋⁰·⁰⁴⁰; Daylan 2021 not ingested) and z′ band (A_g = 0.16 ± 0.01; Mallonn 2019 not ingested).
  - **Albedo paradox reinforced**: A_B = 0.20–0.30 (high) vs A_g ≈ 0.10 (low) — a factor-3 discrepancy in the same observation. Possible resolutions: wavelength-dependent reflected-light contributions outside the NIRISS bandpass (e.g. UV/blue Bond albedo > 0.34 needed for self-consistency).
- **Reflected light asymmetry**: longitudinal slice model (4 slices) consistently favors brighter eastern dayside reflection — eastward reflection always preferred even with A_i < 0 allowed (down to −1). Could indicate **clouds on the eastern dayside** (consistent with high-resolution Doppler clouds on the western limb evaporating eastward; Parmentier 2016 not ingested) or **higher baroclinic short-wavelength altitudes** (Changeat 2024 not ingested).
- **Phase-offset wavelength dependence** (spectroscopic Order 1, 5-pixel bins; Figure 4):
  - Phase offsets **increase to ~14° eastward at 1.13 μm** with negative minimum flux (i.e. unphysically high reflected light) — interpreted as the **first robust altitude-dependent hot-spot detection** (Roth et al. 2024 not ingested).
  - Consistent with NAMELESS cross-check.
- **Stellar granulation timescale**: 30.05⁺⁴·⁴⁴₋³·⁶¹ min (Order 1) / 35.5⁺⁶·²₋⁵·¹⁷ min (Order 2) — **slower than expected** ~6 min (Gilliland 2011 not ingested). Persistent finding across [[2025_Coulombe_TOI-270b]].
- **Tilt event** at integration 3149 (likely primary-mirror tilt) modelled with Heaviside function + PCA components 2–4.

## Methods

- **Two independent reductions**:
  - **Fiducial: [[exoTEDRF]]** v1.4.0 (Radica 2024 not ingested) — group-level 1/f via STScI SOSS background, 30-pixel box aperture, contaminant masking; ATOCA not applied (no significant cross-contamination).
  - **Cross-check: [[NAMELESS]]** (Coulombe 2023, 2025 not ingested) — independent reduction; agrees with exoTEDRF on dayside but warmer nightside (driven by negative-flux handling differences).
- **Light-curve model**: F_model = A(t) + S(t) + G(t):
  - **Astrophysical A(t)**: [[batman]] (Kreidberg 2015 not ingested) transit + sinusoidal phase + Cowan & Agol 2008 ellipsoidal variation correction; half-Gaussian prior on planetary flux to allow but penalize negative values; second-order sinusoidal phase model (4 parameters: C₁, C₂, D₁, D₂).
  - **Systematics S(t)**: linear trend + PCA components 2/3/4 + Heaviside tilt-event term.
  - **Gaussian process G(t)**: celerite (Foreman-Mackey 2017 not ingested) SHO kernel for stellar granulation/red noise (parameters S_0, ω_0, Q = 1/√2 fixed; reparameterized in amplitude A_GP / timescale τ_GP).
- **Energy-budget conversion**: brightness-temperature → effective-temperature (per orbital phase) via wavelength-weighted mean; uncertainty inflated by captured-flux fraction γ ≈ 0.55–0.82.
- **Bell_EBM grid**: 11 A_B × 50 V_wind × 100 P_0 (55 000 models) fitted to bolometric brightness-temperature phase curve.
- **Slice model** (Cowan & Agol 2008): 4 / 6 / 8 longitudinal slices for Order 2 reflected-light extraction; analytical kernels (Appendix B).
- **MCMC**: emcee (Foreman-Mackey 2013 not ingested), 12 500 burn-in + 50 000 production for white light curves; per-bin in spectroscopic fits.

## Caveats & limitations

- **NRS1–NRS2 / Order 1–Order 2 cross-instrument calibration**: requires assumption that the planetary radius is wavelength-independent (Order 2 R_p/R_★ slightly smaller than Order 1, consistent with low optical scale height).
- **Stellar variability model** (Order 2 only) — second-order sinusoid at stellar rotation period (1.13 d, Delrez 2016 not ingested); ΔBIC = 33 in Order 2 favors inclusion. Choice affects ε but not A_B significantly.
- **Negative planetary flux handling**: 1.4σ ε discrepancy between exoTEDRF (half-Gaussian penalty) and NAMELESS (unconstrained) demonstrates sensitivity. The exoTEDRF half-Gaussian is physically motivated but methodologically conservative.
- **Albedo paradox not resolved**, only better-quantified: A_B / A_g factor-3 ratio requires either reflected-light contributions at unobserved wavelengths (UV/blue) or systematic differences in interpretation between reflected and thermal emission.
- **Bell_EBM is a single-global-wind-speed model** — incompatible with the empirically inferred vertical wind structure (Seidel 2025 not ingested: 4–10 km/s at low pressure, much slower at depth). The 0.2 km/s "wind" is a deep-layer effective parameter, not directly comparable to upper-atmosphere Doppler tracers.
- **Phase offset wavelength dependence** (Figure 4) is striking but currently lacks a definitive interpretation (clouds vs altitude-dependent hot spot vs reflected-light-shifted hot spot).

## Open questions / follow-ups

- **Joint NIRISS/SOSS + NIRSpec/G395H phase-curve analysis** would extend the bolometric coverage from 55–82 % to >90 % and allow direct measurement of the A_B–A_g paradox across the full optical-NIR baseline.
- **3D GCM comparisons** including magnetic drag (Beltz 2022, Wardenier 2024 — not ingested) and condensate clouds (Roman 2021, Komacek 2022 — not ingested) are needed to reproduce the slow wind, deep mixed-layer, and eastward reflected-light asymmetry simultaneously.
- **High-resolution Doppler cross-check** of the inferred slow zonal wind: Seidel 2025 not ingested gives 4–10 km/s upper-atmosphere flows; Bell_EBM gives 0.2 km/s at ~1 bar. Reconciliation requires vertically resolved circulation modelling.
- **UV/blue albedo** would close the A_B–A_g gap if A_short ≈ 0.34 holds.
- **Phase-offset wavelength dependence** vs hot-spot altitude variation — needs detailed 3D treatment to discriminate from reflected-light dominance.

## Related

- [[2025_Gapp_WASP121b]] — companion NIRSpec/G395H *transmission-only* extraction from the GO-1729 phase curve; detects SiO at 5.2σ and reveals thermal H₂O + H₂ dayside dissociation. The two papers together give the first JWST panchromatic (0.6–5.2 μm) characterization of WASP-121 b.
- [[2025_Sikora_HD80606b]] — analogous partial phase curve methodology on a highly eccentric hot Jupiter; same NEAT GTO program family.
- [[2025_Fu_statistical-trends]] — WASP-121 b is the ultra-hot end of the 8-planet population sample; CO-L = 1.98 ± 0.16 (highest in the sample).
- [[2025_LustigYaeger_WASP17b]] — comparable JWST G395H phase curve methodology on a less-irradiated UHJ analog; PIE / iESR variant of the brightness-temperature analysis.
- [[2025_Gressier_WASP17b]] — JWST-TST DREAMS dayside emission of WASP-17 b; comparable atmospheric retrieval framework.
- Concept: [[thermal-dissociation]] — H₂ dissociation/recombination physics enters the Bell_EBM heat budget directly.
- Concept: [[transmission-spectrum]] (parent observable, here extended to full phase curves).
