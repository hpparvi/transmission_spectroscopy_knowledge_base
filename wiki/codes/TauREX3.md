---
type: code
aliases: [TauREX, Tau Retrieval for Exoplanet atmospheres]
tags: [retrieval-code, bayesian, transmission, emission, pre-jwst]
---

# TauREX3

Open-source exoplanet atmospheric retrieval framework (Al-Refaie et al. 2019, 2021; not yet ingested), the third major version of the TauREX code developed at UCL. Supports free-chemistry and equilibrium-chemistry retrievals for both transmission and emission geometries, coupled to the MultiNest nested sampler. Standard retrieval engine for the ARES survey (HST WFC3 era) and used in several JWST-era analyses.

## Papers
- [[2025_Gressier_HATP26b]] — TauREx 3.1 retrieval (R = 100; ExoMol/HITEMP/HITRAN line lists) on HAT-P-26 b NIRSpec G395H; reproduces POSEIDON evidence within ~3 ln Z; **also primary code for the population-level SO₂–[M/H] reanalysis of 11 JWST giant-planet transmission spectra** (Fig. 7 trend).
- [[2025_FernandezRodriguez_K2-18b]] — TauREx 3.1 + PyMultiNest free-chemistry retrievals on K2-18 b NIRISS+NIRSpec G395H spectrum across 12 reduction variants × 4–6 model setups; demonstrates retrieval-complexity dependence (CO₂ at ~2σ in comprehensive 13-species retrieval; vanishes in simpler runs); DMS 95% upper limit < −4.39 in comprehensive retrievals.
- [[2025_Jaziri_K2-18b]] — TauREx 3.1 + PyMultiNest with the **TauREx-PyMieScatt** module (Changeat et al. 2025; not ingested) on K2-18 b NIRISS+NIRSpec+MIRI joint spectrum; aerosol Mie-scattering with complex refractive indices for 7 tholin analogs; CH₄-only PAMPRE "exo1" tholin preferred at Bayes factor 5.53; first wiki paper to apply complex-refractive-index aerosol modeling to a JWST sub-Neptune.
- [[2021_Mugnai_GJ1132b]] — Bayesian retrieval on five HST WFC3 G141 transits of GJ 1132 b; cloud-only flat model favored; all molecular species ruled out.
- [[2024_Gressier_L98-59d]] — one of two retrieval frameworks used on the L 98-59 d NIRSpec/G395H transit (alongside NEMESISPY); molecular feature preferred at 2.6σ–5.6σ.
- [[2025_Gressier_WASP17b]] — TauREx 3.1 primary retrieval on WASP-17 b NIRISS/SOSS dayside emission spectrum; supersolar metallicity at 3σ; H₂O at 6.4σ.
- [[2025_Crouzet_HATP12b]] — TauREx 3.1 cross-check on HAT-P-12 b NIRSpec G395M (vs primary [[ARCiS]]); reproduces detection significances within ~0.4σ.
