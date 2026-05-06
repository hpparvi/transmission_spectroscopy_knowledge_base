---
type: code
aliases: [TauREX, TauREx, TauREx 3.1, Tau Retrieval for Exoplanet atmospheres]
tags: [retrieval-code, bayesian, transmission, emission, pre-jwst, hub]
---

# TauREX3

Open-source Bayesian atmospheric retrieval framework (Al-Refaie et al. 2019, 2021; not yet ingested), the third-generation TauREX code from UCL. Supports free-chemistry and equilibrium-chemistry retrievals for transmission and emission geometries, coupled by default to the [[MultiNest]] nested sampler via PyMultiNest. The standard retrieval engine for the ARES survey (HST WFC3 era; [[Iraclis]] reductions) and one of the most consistently re-used JWST-era retrieval codes in the wiki — appearing on every host-star spectral type from F to ultracool M.

## Variants

The wiki sees three recurring TauREX deployment patterns:

- **Primary single-code retrieval.** [[2021_Mugnai_GJ1132b]] (HST/WFC3 ARES reduction) and [[2025_Gressier_WASP17b]] (JWST/NIRISS/SOSS dayside emission) use TauREX 3.1 as the sole retrieval engine.
- **Two-code cross-check.** TauREX paired with another framework as a Bayes-factor cross-validation:
  - vs. [[POSEIDON]] — [[2025_Gressier_HATP26b]] (HAT-P-26 b NIRSpec G395H), [[2025_Gressier_WASP17b]] (cross-check with M&S09 and Piette-Madhusudhan BD T-P).
  - vs. [[NEMESISPY]] — [[2024_Gressier_L98-59d]] (L 98-59 d NIRSpec G395H).
  - vs. [[ARCiS]] — [[2025_Crouzet_HATP12b]] (HAT-P-12 b NIRSpec G395M; reproduces detection significances within ~0.4σ).
- **Population reanalysis driver.** [[2025_Gressier_HATP26b]] additionally uses TauREX as the workhorse for the SO₂-[M/H] population reanalysis of 11 JWST giant-planet transmission spectra (Fig. 7 trend) — establishing that TauREX scales to multi-target homogeneous reanalyses.
- **Plugin extension for novel chemistry / aerosols.** [[2025_Jaziri_K2-18b]] uses the **TauREx-PyMieScatt** module (Changeat et al. 2025; not ingested) for complex-refractive-index aerosol Mie-scattering retrievals — the first wiki application of complex-refractive-index aerosol modeling to a JWST sub-Neptune. [[2025_Gressier_HATP26b]] uses a custom MadhuSeager2009 plugin to expose a BD-type T-P parameterization.
- **Comprehensive vs. simplified retrievals.** [[2025_FernandezRodriguez_K2-18b]] runs the same TauREX 3.1 framework at four model complexities (1, 5, 9, 13 species) on the K2-18 b dataset; demonstrates that simplified retrievals systematically inflate detection significance — the comprehensive 13-species TauREX run reduces the original Madhusudhan 2023 4–5σ DMS claim to a 95% upper limit and CO₂ from ~3σ to ~2σ.

## History

- **HST/WFC3 era (2017–2021).** Standard ARES survey engine. [[2021_Mugnai_GJ1132b]] is the wiki representative — five WFC3 G141 GJ 1132 b transits homogeneously reduced via [[Iraclis]] then retrieved via TauREX.
- **JWST Cycle 1 emergence (2024).** [[2024_Gressier_L98-59d]] uses TauREX as one of two retrieval frameworks on the first L 98-59 d NIRSpec G395H transit; the H₂S/SO₂ tentative atmosphere holds up across both TauREX and NEMESISPY but at different significance.
- **JWST Cycle 2–3 (2025).** Adoption broadens to hot Jupiter dayside emission ([[2025_Gressier_WASP17b]]), Neptune-mass transmission ([[2025_Gressier_HATP26b]]), sub-Neptune transmission with novel aerosol chemistry ([[2025_Jaziri_K2-18b]]), and methodology cross-checks on K2-18 b ([[2025_FernandezRodriguez_K2-18b]]) and HAT-P-12 b ([[2025_Crouzet_HATP12b]]).

## Trade-offs

- **Strength: actively maintained plugin ecosystem.** TauREx-PyMieScatt for complex-RI aerosols ([[2025_Jaziri_K2-18b]]) and the custom MadhuSeager2009 T-P module ([[2025_Gressier_HATP26b]]) demonstrate the plugin model. Comparable JWST-era retrieval codes ([[POSEIDON]], [[CHIMERA]]) require core-code modifications for analogous extensions.
- **Strength: cross-code validation results consistent.** [[2025_Crouzet_HATP12b]] reports TauREX vs ARCiS detection significances agree within ~0.4σ; [[2025_Gressier_WASP17b]] reports TauREX vs POSEIDON agree on ln Z within ~3 across multiple T-P parameterizations. TauREX inferences are robust against retrieval-code choice.
- **Strength: comprehensive species library.** [[2025_FernandezRodriguez_K2-18b]] runs TauREX with up to 13 species for the K2-18 b retraction.
- **Limitation: free-chemistry-default.** Out-of-the-box TauREX runs use free chemistry; equilibrium chemistry requires upstream chemistry tables. Codes built around equilibrium chemistry as a primary mode (e.g., [[CHIMERA]], [[ATMO]]) integrate this more naturally.
- **Limitation: ARES-survey legacy reduction tooling.** [[Iraclis]] WFC3 reductions are the canonical input pipeline for TauREX; users on JWST data must supply their own pipeline output.
- **Limitation: 1D plane-parallel.** No native limb-asymmetry support; cannot directly retrieve evening-vs-morning chemistry differences ([[limb-asymmetry]]).

## Open issues

- **Detection-significance inflation in simplified retrievals.** [[2025_FernandezRodriguez_K2-18b]] documents this as a methodological concern: 1- and 5-species TauREX runs find DMS at 4–5σ, while 9- and 13-species runs reduce DMS to a 95% upper limit. Generalizable across retrieval codes but not yet a community standard.
- **Aerosol parameterization choice.** [[2025_Jaziri_K2-18b]] shows that complex-RI Mie-scattering tholins fit K2-18 b at lnB = 5.53 and reduce inferred metallicity from 20× to 0.3× solar — the haze parameterization is a major degeneracy axis not adequately explored across the TauREX user base.

## Papers

### JWST hot Jupiter / sub-Saturn / Neptune-mass — primary or cross-check retrieval
- [[2025_Gressier_HATP26b]] — TauREx 3.1 primary on HAT-P-26 b NIRSpec G395H + population reanalysis driver for SO₂-[M/H] trend across 11 JWST giant-planet spectra.
- [[2025_Crouzet_HATP12b]] — cross-check on HAT-P-12 b NIRSpec G395M (vs primary [[ARCiS]]); reproduces detections within ~0.4σ.
- [[2025_Gressier_WASP17b]] — primary on WASP-17 b NIRISS/SOSS dayside emission; H₂O at 6.4σ; supersolar metallicity at 3σ.

### JWST sub-Neptune
- [[2025_FernandezRodriguez_K2-18b]] — primary across 12 spectrum variants × 4–6 model complexities; comprehensive 13-species retrievals retract the DMS claim and reduce CO₂ to ~2σ.
- [[2025_Jaziri_K2-18b]] — TauREx-PyMieScatt aerosol plugin on K2-18 b NIRISS+NIRSpec+MIRI joint spectrum; tholin-haze model preferred at lnB = 5.53.

### JWST rocky-M-dwarf transmission
- [[2024_Gressier_L98-59d]] — one of two retrieval frameworks (alongside [[NEMESISPY]]); molecular-atmosphere preferred at 2.6σ–5.6σ.
- [[2024_Banerjee_L98-59d]] — TauREx 3.1 + exoretrievals on L 98-59 d NIRSpec G395H; "Stellar + Atmosphere" preferred over "Stellar Only"; complementary to Gressier 2024.

### HST/WFC3 ARES-survey
- [[2021_Mugnai_GJ1132b]] — TauREX 3.1 + MultiNest 1500 live points on five GJ 1132 b WFC3 G141 transits; cloud-only flat model preferred; all molecular species ruled out.
