---
type: code
aliases: [exoTEDRF pipeline]
tags: [jwst-pipeline, data-reduction, time-series, niriss-soss, nirspec]
---

# exoTEDRF

JWST time-series reduction pipeline (Feinstein et al. 2023; Radica et al. 2023, 2024) developed by the Montréal/Trottier group, primarily designed for NIRISS/SOSS observations but also applicable to NIRSpec. Implements Stage 1 standard STScI corrections plus 1/f noise removal at the group level (scale-achromatic method), Stage 2 flat-field and background subtraction, PCA-based detector detrending to capture sub-pixel trace drifts and thermal beating patterns, and optimal spectral extraction. Widely used across the NIRISS/SOSS literature and some NIRSpec reductions; the standard pipeline for the [[JWST-GTO-1201]] NEAT program.

## Papers
- [[2025_Taylor_GJ357b]] — primary reduction for the GJ 357 b NIRISS/SOSS transit; PCA reveals sub-pixel trace position drift and thermal beating, included in the systematics model.
