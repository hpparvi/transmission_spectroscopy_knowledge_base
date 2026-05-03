---
type: code
aliases: [transitspectroscopy pipeline]
tags: [jwst-pipeline, data-reduction, time-series, nirspec]
---

# transitspectroscopy

A JWST NIRSpec time-series reduction pipeline (Espinoza 2022; not yet ingested. github.com/nespinoza/transitspectroscopy), wrapping the STScI `jwst` pipeline and adding customized jump detection, spectral tracing with Gaussian fits, and 1/f background removal. Used as the primary reduction in the L 98-59 d analyses, cross-checked against [[FIREFLy]].

## Papers
- [[2025_Espinoza_TRAPPIST1e]] — primary reduction for four TRAPPIST-1 e PRISM transits; GP stellar contamination marginalization using celerite Matèrn 3/2 kernel.
- [[2025_Fisher_TOI1685b]] — cross-check reduction for five TOI-1685 b G395H transits.
- [[2024_Gressier_L98-59d]] — primary reduction for the L 98-59 d G395H transit; primary spectrum in the atmospheric retrievals.
- [[2024_Banerjee_L98-59d]] — primary reduction adopted for the companion retrieval analysis on the same transit.
- [[2025_Gressier_WASP17b]] — one of three independent reductions (alongside [[supreme-SPOON]] and [[Ahsoka]]) for the WASP-17 b NIRISS/SOSS secondary eclipse.
