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
- [[2025_Deka_WASP39b]] — primary NIRSpec PRISM reduction (Rustamkulov et al. 2023; not ingested) for WASP-39 b in the panchromatic [[NEXOTRANS]] retrieval; data below 2 μm excluded due to detector saturation.
- [[2025_BelloArufe_L98-59b]] — cross-check reduction (alongside primary [[Eureka]]) for 4 NIRSpec G395H transits of L 98-59 b. Group-level 1/f subtracted + scaled background template removed; lacosmic cosmic-ray cleaning. Agreement < 1σ with Eureka.
- [[2025_Liu_HATP14b]] — **primary reduction** for HAT-P-14 b commissioning data (NIRSpec G395H + NIRISS SOSS); updated FIREFLy with custom group-level 1/f subtraction at threshold flux = 3.6 DN/s; manual saturation flagging for NIRISS NGROUP=3/4 columns. The updated reduction **overturns the previously reported NIRISS blueward slope** from Albert 2023 (not ingested) and reveals water features at 1.4 / 1.9 / 2.6 μm.
- [[2025_Schmidt_K2-18b]] — **first FIREFLy NIRISS+NIRSpec reduction of K2-18 b**, including the **first analysis of the NIRISS SOSS 2nd order**. Custom group-level 1/f via zodiacal-background subtraction with pickoff-mirror flux-jump correction; skip dark current and jump; pastasoss for wavelength/order tracing; integration-level 1/f via PSF-masked column-median subtraction; running 7-frame temporal median; 15σ temporal outliers; box extraction 30-pixel order 1, 23-pixel order 2; spot-crossing event trimmed (not modeled). NIRSpec processing: lacosmic cosmic-ray cleaning, 5.2-pixel (NRS1) and 2.41-pixel (NRS2) box extractions, 575/8/18 integration trimming. The FIREFLy + R≈25 NIRISS spectrum yields the lowest CH₄ detection significances (3.1–3.8σ); FIREFLy reductions are the principal alternative against which exoTEDRF reductions are compared.
