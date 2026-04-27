---
type: method
aliases: [transit light source effect, TLSE modeling, starspot retrieval]
tags: [stellar-heterogeneity, m-dwarf, degeneracy]
---

# Stellar contamination modeling

Forward or retrieval modeling of the transit light source effect (Rackham et al. 2018): unocculted photospheric heterogeneities (spots, faculae) imprint wavelength-dependent signatures on a transmission spectrum that can mimic or mask genuine atmospheric features. Typically parameterized by heterogeneity temperature, covering fraction, and photosphere temperature; fit jointly with atmospheric parameters or compared via Bayesian model selection. A central concern for M-dwarf transiting planets — see [[stellar-contamination]]. The empirical alternative, when a near-airless reference planet is available, is [[back-to-back-transit-correction]].

## Papers
- [[2025_Espinoza_TRAPPIST1e]] — novel GP marginalization over stellar contamination for TRAPPIST-1 e PRISM visits; demonstrates current PHOENIX models systematically fail to reproduce TRAPPIST-1 photospheric features at λ < 3 μm; GP workaround enables atmospheric inference without relying on stellar models.
- [[2025_PiauletGhorayeb_TRAPPIST1d]] — [[stctm]] code for stellar contamination correction of TRAPPIST-1 d PRISM transits; exotune sub-framework for photospheric heterogeneity fitting.
- [[2025_Glidden_TRAPPIST1e]] — visits 3 and 4 contaminated by stellar flares and activity; GP correction (from companion Espinoza et al. 2025, not yet ingested) applied to all four visits for the combined spectrum; stellar model uncertainty (~1800 ppm/pixel) dominates over observational precision (~89 ppm).
- [[2023_Lim_TRAPPIST1b]] — sequential and simultaneous stellar-contamination + atmosphere fits to TRAPPIST-1 b NIRISS/SOSS; Visit 1 dominated by cool spots (~29% covering fraction, ~−197 K), Visit 2 by faculae (~29%, ~+153 K); contamination amplitudes ~750–1000 ppm peak-to-peak.
- [[2025_Taylor_GJ357b]] — TLS models (PHOENIX grid, 3- and 5-component setups with/without log g free) tested against the GJ 357 b NIRISS/SOSS spectrum; all four TLS parameterizations yield Bayes factors below the flat-line model; GJ 357's exceptional inactivity (log R'HK = 5.53) makes a physical null result expected.
- [[2025_Rathcke_TRAPPIST1bc]] — SPHINX-grid 1- to 4-component fits (via [[speclib]]) to TRAPPIST-1 out-of-transit JWST/PRISM spectra; 2-component fit prefers ~55.6% T₁ ≈ 2000 K (grid-floor upper limit) + ~44.4% T₂ ≈ 2600 K, with the cool-component covering fraction varying ~0.1%/hr over a single visit. Joint in-transit fit prefers a well-mixed photosphere over a fully-unocculted-cool-component geometry.
- [[2025_Bennett_GJ1132b]] — four-visit PHOENIX modeling of GJ 1132's out-of-transit spectra; Visit 1 significantly favors ~10% more cool-spot coverage than Visits 2–4, interpreted as evolving stellar heterogeneity that drives the Visit-1 transmission-spectrum deviation reported in [[2023_May_GJ1132b]].
- [[2024_Gressier_L98-59d]] — unocculted-spots/faculae retrieval rejects stellar-contamination-only as an explanation for the L 98-59 d spectrum; atmospheric model preferred.
- [[2024_Banerjee_L98-59d]] — three-parameter stellar contamination retrieval on L 98-59 d; "Stellar + Atmosphere" favored over "Stellar Only"; retrieved T_phot ≈ 3423 K and facula temperature ~+324 K hotter.
- [[2023_May_GJ1132b]] — runs atmosphere and unocculted-starspot retrievals on GJ 1132 b and finds indistinguishable Bayesian evidence; uses out-of-transit PHOENIX modeling to argue against variability between visits.
- [[2023_Moran_GJ486b]] — in-transit [[POSEIDON]] starspot retrieval on GJ 486 b plus independent multi-component PHOENIX fits to the out-of-transit baseline; the 3-component (photosphere + spots + faculae) stellar model is preferred by Δχ²ν ≈ 23, lending physical support to the starspot scenario.
- [[2023_Lustig-Yaeger_LHS475b]] — tests for stellar contamination on LHS 475 b and finds none; no spot crossings during transit and low stellar activity in out-of-transit data.
