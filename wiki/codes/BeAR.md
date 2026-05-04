---
type: code
aliases: [Bern Atmospheric Retrieval, HELIOS-R2]
tags: [retrieval-code, bayesian, transmission, emission, line-spread-function-aware]
---

# BeAR

The Bern Atmospheric Retrieval code (Kitzmann et al. 2020; not yet ingested) — the renamed and updated form of the **HELIOS-R2** retrieval framework. Open-source Bayesian retrieval with [[MultiNest]] nested-sampling backend; supports free-chemistry and chemical-equilibrium compositions; can produce forward models at native instrument resolution (R = 10⁰⁰⁰⁰) and convolve with **a wavelength-dependent line-spread function (LSF)** for direct comparison to JWST data without binning. Distinct from peer retrieval codes ([[POSEIDON]], [[petitRADTRANS]], [[TauREX3]], [[ARCiS]]) primarily in its emphasis on native-resolution analysis. Opacity computation is via the companion [[HELIOS-K]] code.

## Variants

- **Native-resolution + LSF convolution** (Felix et al. 2025 deployment): forward model at R = 10⁰⁰⁰⁰ → Gaussian LSF (FWHM ≈ 2 px wavelength-dependent) → unbinned data.
- **Binned data, no LSF** (legacy approach): forward model and data both binned to common resolution; Felix 2025 documents this as a source of Bayes-factor instability for sub-Neptune retrievals.

## Trade-offs

- **Strength:** Native-resolution retrieval prevents Bayes-factor variability with binning. Felix 2025 documents 3 dex variation in retrieved abundances (and Bayes factors flipping between 1 and 78) when binning a TOI-270 d spectrum — issues that disappear at native resolution.
- **Strength:** Used as the sub-Neptune analog of [[POSEIDON]] / [[petitRADTRANS]] for cross-code comparisons.
- **Limitation:** Computational cost — native-resolution forward models at R = 10,000 are 10–100× slower than R ≈ 100 binned models.
- **Limitation:** Not yet widely deployed beyond the Bern group; cross-validation against ARCiS / POSEIDON / TauREx is currently single-paper-per-target.

## Papers

- [[2025_Felix_TOI-270d]] — primary retrieval engine for TOI-270 d NIRSpec G395H + NIRISS SOSS reanalysis; Bern fiducial isothermal cloud-free model; supports six-parameter Madhusudhan-Seager T–p profile and gray/non-gray cloud variants. Demonstrates native-resolution + LSF as the methodologically robust regime for sub-Neptune atmospheric inference.
