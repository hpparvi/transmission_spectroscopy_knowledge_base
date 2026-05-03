---
type: code
aliases: [exoTEDRF pipeline]
tags: [jwst-pipeline, data-reduction, time-series, niriss-soss, nirspec]
---

# exoTEDRF

JWST time-series reduction pipeline (Feinstein et al. 2023; Radica et al. 2023, 2024) developed by the Montréal/Trottier group, primarily designed for NIRISS/SOSS observations but also applicable to NIRSpec. Implements Stage 1 standard STScI corrections plus 1/f noise removal at the group level (scale-achromatic method), Stage 2 flat-field and background subtraction, PCA-based detector detrending to capture sub-pixel trace drifts and thermal beating patterns, and optimal spectral extraction. Widely used across the NIRISS/SOSS literature and some NIRSpec reductions; the standard pipeline for the [[JWST-GTO-1201]] NEAT program.

## Papers
- [[2025_Taylor_GJ357b]] — primary reduction for the GJ 357 b NIRISS/SOSS transit; PCA reveals sub-pixel trace position drift and thermal beating, included in the systematics model.
- [[2026_Coy_HD3167b]] — independent cross-check reduction for HD 3167 b MIRI/LRS secondary eclipse (primary: [[SPARTA]]).
- [[2026_Radica_WASP96b]] — nominal NIRISS+NIRSpec reduction for WASP-96 b (alternate NIRISS via [[NAMELESS]], alternate NIRSpec via [[Eureka]]); 1/f-correction methodology divergence with NAMELESS above 1.7 μm flagged as a caveat.
- [[2026_Heinke_HATP12b]] — primary NIRISS/SOSS reduction for the HAT-P-12 b panchromatic transmission spectrum.
- [[2025_Howard_TRAPPIST1_flares]] — reduction for the NIRISS/SOSS and NIRSpec PRISM flare-monitoring visits of TRAPPIST-1 b/c/f/g.
- [[2025_Roy_LP791-18c]] — cross-check reduction for the LP 791-18 c NIRSpec PRISM transit (primary: custom Stage 1 + Eureka Stages 2/3).
