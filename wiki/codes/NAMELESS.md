---
type: code
aliases: [NAMELESS pipeline]
tags: [jwst-pipeline, data-reduction, niriss-soss, time-series]
---

# NAMELESS

A JWST NIRISS/SOSS time-series reduction pipeline (Feinstein et al. 2022; Coulombe et al. 2023; not yet ingested). Provides an independent reduction pathway for NIRISS/SOSS observations. Described as the "most conservative" of the three reductions used in [[2023_Lim_TRAPPIST1b]]; its results are adopted as the primary presented analysis in that paper. Commonly run alongside [[supreme-SPOON]] and [[SOSSISSE]] for cross-check consistency.

## Papers
- [[2023_Lim_TRAPPIST1b]] — primary reduction presented for TRAPPIST-1 b NIRISS/SOSS transits; cross-checked against [[supreme-SPOON]] and [[SOSSISSE]]; adopted for most conservative contamination and atmospheric inferences.
- [[2026_Radica_WASP96b]] — alternate NIRISS/SOSS reduction (vs. primary [[exoTEDRF]]); 1/f-correction methodology divergence flagged for spectra >1.7 μm.
