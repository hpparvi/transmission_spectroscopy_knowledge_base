---
type: code
aliases: [exoTEDRF pipeline]
tags: [jwst-pipeline, data-reduction, time-series, niriss-soss, nirspec, hub]
---

# exoTEDRF

JWST time-series reduction pipeline developed by the Montréal/Trottier group (Feinstein et al. 2023; Radica et al. 2023, 2024; not yet ingested), primarily designed for **NIRISS/SOSS** but also applicable to NIRSpec G395H, NIRSpec PRISM, and MIRI/LRS. Implements Stage 1 STScI standard corrections plus group-level 1/f noise removal (scale-achromatic method), Stage 2 flat-field and background subtraction, PCA-based detector detrending to capture sub-pixel trace drifts and thermal beating patterns, and optimal spectral extraction. The default pipeline for the [[JWST-GTO-1201]] NEAT program and increasingly the standard NIRISS/SOSS reduction across hot-Jupiter, sub-Neptune, and rocky-planet papers in the wiki.

## Variants

- **NIRISS/SOSS primary reduction.** The dominant role: 5 of 9 ingested papers.
  - [[2025_Taylor_GJ357b]] — first NIRISS/SOSS transmission of GJ 357 b; PCA reveals sub-pixel trace position drift and thermal beating, included in the systematics model.
  - [[2025_Murphy_WASP107b]] — primary on WASP-107 b limb-resolved NIRISS/SOSS transit; uses `refine_soss_timestamps` for accurate per-column time stamps; post-fit offsets +110 ppm evening / +20 ppm morning correct for occulted-spot bias.
  - [[2026_Heinke_HATP12b]] — primary NIRISS/SOSS for HAT-P-12 b panchromatic transmission.
  - [[2025_FernandezRodriguez_K2-18b]] — primary NIRISS/SOSS reduction (Stages 1–3) for K2-18 b transit under JWST GO 2722; box-extraction with 30-pixel aperture; jump threshold 7σ.
  - [[2025_Coulombe_TOI-270b]] — NIRSpec G395H reduction for the simultaneous TOI-270 b + d transit (companion paper context).
- **NIRSpec PRISM / G395H cross-check.**
  - [[2025_Roy_LP791-18c]] — cross-check reduction for LP 791-18 c NIRSpec PRISM (primary: custom Stage 1 + Eureka Stages 2/3).
  - [[2025_Howard_TRAPPIST1_flares]] — reduction for NIRISS/SOSS and NIRSpec PRISM flare-monitoring visits of TRAPPIST-1 b/c/f/g.
- **MIRI/LRS cross-check.**
  - [[2026_Coy_HD3167b]] — independent cross-check on HD 3167 b MIRI/LRS secondary eclipse (primary: [[SPARTA]], also cross-checked with [[Eureka]]).
- **Mixed two-detector hot-Jupiter primary.**
  - [[2026_Radica_WASP96b]] — nominal NIRISS+NIRSpec reduction for WASP-96 b panchromatic transmission; alternate NIRISS via [[NAMELESS]], alternate NIRSpec via [[Eureka]]; 1/f-correction methodology divergence with NAMELESS above 1.7 μm flagged as a caveat.

## History

- **2023** — exoTEDRF first published (Feinstein 2023, Radica 2023); designed for NIRISS/SOSS NEAT program.
- **2024** — adoption broadens beyond NEAT; NIRSpec extension matures.
- **2025** — saturating wiki adoption: 8 of 9 ingested exoTEDRF papers in 2025–2026; spans rocky-M-dwarf, sub-Neptune, K-dwarf super-Earth, hot-Jupiter, USP super-Earth, and limb-resolved hot-Saturn cases.

## Trade-offs

- **Strength: NIRISS/SOSS optimization.** Group-level 1/f handling, PCA detrending, and `refine_soss_timestamps` are NIRISS-specific innovations not found in vanilla [[Eureka]] reductions. Established as the NIRISS/SOSS reference pipeline.
- **Strength: PCA detector detrending.** Captures sub-pixel trace drifts and thermal-beating patterns that other pipelines treat as residual; particularly valuable for limb-resolved spectroscopy ([[2025_Murphy_WASP107b]]).
- **Strength: Cross-detector versatility.** Single pipeline handles NIRISS, NIRSpec G395H, NIRSpec PRISM, MIRI/LRS — useful for panchromatic targets ([[2026_Heinke_HATP12b]], [[2026_Radica_WASP96b]]).
- **Limitation: 1/f-correction divergence with NAMELESS above 1.7 μm.** [[2026_Radica_WASP96b]] explicitly flags this as a caveat for WASP-96 b; the wavelength-dependent 1/f model parameters differ between exoTEDRF and NAMELESS.
- **Limitation: ecosystem-specific to Montréal/Trottier group.** Espinoza-group papers ([[2025_Espinoza_TRAPPIST1e]] etc.) prefer [[transitspectroscopy]]; cross-validation against exoTEDRF on common datasets is limited.

## Open issues

- **NIRISS-NIRSpec calibration consistency above 1.7 μm.** The exoTEDRF-vs-NAMELESS 1/f divergence ([[2026_Radica_WASP96b]]) is the canonical example; broader population testing pending.
- **Limb-resolved-mode validation.** [[2025_Murphy_WASP107b]] is the first wiki application of `refine_soss_timestamps` for limb-asymmetry; cross-pipeline validation of timestamp-driven asymmetric-transit fits is open.

## Papers

### NIRISS/SOSS — primary reduction
- [[2025_Murphy_WASP107b]] — limb-resolved transit; `refine_soss_timestamps` for accurate per-column time stamps; spot-bias post-fit offsets.
- [[2025_Taylor_GJ357b]] — first NIRISS/SOSS transmission of GJ 357 b; PCA detrending used.
- [[2025_FernandezRodriguez_K2-18b]] — K2-18 b GO 2722 reanalysis; 30-pixel box extraction.
- [[2026_Heinke_HATP12b]] — HAT-P-12 b panchromatic NIRISS+NIRSpec G395M+MIRI.
- [[2026_Radica_WASP96b]] — WASP-96 b panchromatic transmission; NAMELESS divergence flagged.

### NIRSpec PRISM / G395H + flare-aware
- [[2025_Coulombe_TOI-270b]] — NIRSpec G395H simultaneous TOI-270 b + d transit.
- [[2025_Roy_LP791-18c]] — NIRSpec PRISM cross-check reduction.
- [[2025_Howard_TRAPPIST1_flares]] — NIRISS/SOSS + NIRSpec PRISM flare monitoring.

### MIRI/LRS cross-check
- [[2026_Coy_HD3167b]] — HD 3167 b LAVA LAMPS secondary-eclipse cross-check.
