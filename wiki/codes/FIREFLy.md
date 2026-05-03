---
type: code
aliases: [FIREFLy pipeline]
tags: [jwst-pipeline, data-reduction, time-series, nirspec, hub]
---

# FIREFLy

A JWST NIRSpec time-series reduction pipeline (Rustamkulov et al. 2022, 2023; not yet ingested) developed alongside the WASP-39 b ERS analysis. Wraps stages 1–2 of the STScI `jwst` pipeline with **custom group-level 1/f correction** and **custom bias subtraction**, then performs spectroscopic light-curve fitting. Distinguished from [[Eureka]] by its bias/1/f handling and from [[Tiberius]] by its NIRSpec-native focus. Frequently the third leg of three-pipeline cross-checks for high-stakes results.

## Variants

- **NIRSpec PRISM and G395H BOTS** are the modes where FIREFLy appears; no NIRISS/SOSS or MIRI deployment in the wiki.
- **Superbias-scaling detrending.** Introduced in [[2023_Moran_GJ486b]] to address the NRS2 Transit-1 superbias offset on GJ 486 b.

## Trade-offs

- **Strength:** STScI-pipeline-independent 1/f and bias treatment; the natural cross-check against [[Eureka]] (which inherits stage 1–2 behavior from the STScI `jwst` pipeline).
- **Strength:** Tends toward conservative feature significances. [[2024_Gressier_L98-59d]] reports a 3.0σ feature versus the [[transitspectroscopy]] primary's 5.6σ on the same L 98-59 d data — consistent with more aggressive systematics suppression.
- **Limitation:** Like all reductions, FIREFLy contributes to the up-to-2-dex retrieval-parameter spread documented in [[2026_RoyPerez_WASP39b]].

## Open issues

- **Cross-pipeline reproducibility.** FIREFLy and [[Eureka]] occasionally produce significantly different feature significances on the same data ([[2023_Moran_GJ486b]] CO₂: 6.5σ Eureka vs 2.3σ FIREFLy; [[2024_Gressier_L98-59d]] sulfur feature: 5.6σ transitspectroscopy vs 3.0σ FIREFLy). The community has no standardized comparison protocol.

## Papers

- [[2026_RoyPerez_WASP39b]] — one of four pipelines in the WASP-39 b ERS PRISM data-reduction systematics study.
- [[2025_Bennett_GJ1132b]] — one of three independent reductions for the four-visit GJ 1132 b coadded spectrum.
- [[2024_Gressier_L98-59d]] — secondary reduction (alongside [[transitspectroscopy]]) for L 98-59 d; less significant (3.0σ) but consistent atmospheric detection.
- [[2024_Banerjee_L98-59d]] — cross-check on the main [[transitspectroscopy]] spectrum; retrievals agree on sulfur-species preference.
- [[2023_May_GJ1132b]] — one of three independent reductions for GJ 1132 b G395H data.
- [[2023_Moran_GJ486b]] — one of three independent reductions for GJ 486 b; introduces superbias-scaling detrending.
- [[2023_Lustig-Yaeger_LHS475b]] — primary reduction used for the final LHS 475 b transmission spectrum.
