---
type: code
aliases: [FIREFLy pipeline]
tags: [jwst-pipeline, data-reduction, time-series, nirspec]
---

# FIREFLy

A JWST time-series reduction pipeline (Rustamkulov et al. 2022, 2023; not yet ingested), wrapping stages 1–2 of the `jwst` pipeline with custom group-level 1/f correction and custom bias subtraction, then performing spectroscopic light-curve fitting. Frequently run alongside [[Eureka]] and [[ExoTiC-JEDI]] as one of three parallel reductions.

## Papers
- [[2025_Bennett_GJ1132b]] — one of three independent reductions for the four-visit GJ 1132 b coadded spectrum.
- [[2024_Gressier_L98-59d]] — secondary reduction (alongside [[transitspectroscopy]]) for L 98-59 d; yields less significant (3.0σ) but consistent atmospheric detection.
- [[2024_Banerjee_L98-59d]] — FIREFLy reduction used as a cross-check on the main [[transitspectroscopy]] spectrum; retrievals agree on sulfur-species preference.
- [[2023_May_GJ1132b]] — one of three independent reductions for GJ 1132 b G395H data.
- [[2023_Moran_GJ486b]] — one of three independent reductions for GJ 486 b (alongside [[Eureka]] and [[Tiberius]]); novel superbias-scaling detrending introduced here.
- [[2023_Lustig-Yaeger_LHS475b]] — primary reduction used for the final LHS 475 b transmission spectrum.
