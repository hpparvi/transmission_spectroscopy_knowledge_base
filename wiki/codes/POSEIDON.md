---
type: code
aliases: [POSEIDON retrieval code]
tags: [retrieval-code, bayesian, transmission]
---

# POSEIDON

An open-source [[atmospheric-retrievals]] code (MacDonald & Madhusudhan 2017; MacDonald 2023) for exoplanet transmission and emission spectra, supporting free and chemical-equilibrium compositions, parametric T–P profiles, cloud/haze parameterizations, and joint atmosphere + [[stellar-contamination]] retrievals. Typically paired with PyMultiNest or MultiNest for sampling.

## Papers
- [[2023_May_GJ1132b]] — GJ 1132 b atmosphere and unocculted-starspot retrievals with a 15-parameter atmospheric model and 2000 PyMultiNest live points.
- [[2023_Moran_GJ486b]] — 6-gas free-chemistry atmospheric retrieval + alternative stellar-contamination retrieval (Pinhas 2018 parameterization) on GJ 486 b transmission spectrum; both scenarios fit at χ²ν ≈ 1.0.
- [[2023_Lim_TRAPPIST1b]] — simultaneous stellar-contamination + atmosphere joint retrieval on TRAPPIST-1 b NIRISS/SOSS spectra; H₂ abundance < 52% at 3σ.
- [[2025_LustigYaeger_WASP17b]] — POSEIDON v1.2 free-chemistry retrieval on the iESR-PIE WASP-17 b dayside and nightside spectra; tentative SO₂, CH₄, H₂O, CO₂ on the nightside.
- [[2025_Gressier_WASP17b]] — POSEIDON cross-check of WASP-17 b dayside NIRISS/SOSS retrieval (alongside primary [[TauREX3]]); two T–P parameterizations tested.
- [[2026_Radica_WASP96b]] — one of four free-chemistry retrieval frameworks cross-compared on WASP-96 b (alongside [[PyratBay]], [[NEMESISPY]], [[Aurora]]).
- [[2026_Ashtari_HATS75b]] — primary retrieval engine for HATS-75 b NIRSpec PRISM in both free-chemistry and chemical-equilibrium modes, within a TLS framework.
