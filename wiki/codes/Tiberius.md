---
type: code
aliases: [Tiberius pipeline, LRG-BEASTS-JWST]
tags: [jwst-pipeline, data-reduction, time-series, nirspec]
---

# Tiberius

A JWST time-series reduction pipeline (Kirk et al. 2018, 2019, 2021; not yet ingested), originally developed for ground-based low-resolution spectroscopy (LRG-BEASTS) and extended to JWST NIRSpec. Features custom bad-pixel handling and Gaussian trace fitting. Commonly run as a third parallel reduction alongside [[Eureka]] and [[FIREFLy]] (or [[ExoTiC-JEDI]]) for cross-reduction consistency checks.

## Papers
- [[2025_Teske_TOI776c]] — cross-check reduction for both TOI-776 c visits (v1.8.2); weighted average of visits; standard aperture photometry with 8-pixel aperture.
- [[2025_Redai_GJ357b]] — primary reduction for GJ 357 b NIRSpec G395H transit; cross-checked against [[Eureka]].
- [[2025_Alam_L168-9b]] — one of three independent NIRSpec reductions for L 168-9 b (alongside Aesop and [[Eureka]]).
- [[2023_Moran_GJ486b]] — one of three independent reductions for GJ 486 b (alongside [[Eureka]] and [[FIREFLy]]); highest flat-line rejection significance (3.29σ) but an unphysical H₂-dominated secondary retrieval mode is flagged.
- [[2023_Lustig-Yaeger_LHS475b]] — one of three independent reductions for LHS 475 b.
- [[2026_RoyPerez_WASP39b]] — one of four pipelines in the WASP-39 b ERS PRISM data-reduction systematics study.
