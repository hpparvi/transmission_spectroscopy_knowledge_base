---
type: code
aliases: [Tiberius pipeline, LRG-BEASTS-JWST]
tags: [jwst-pipeline, data-reduction, time-series, nirspec, hub]
---

# Tiberius

A JWST time-series reduction pipeline (Kirk et al. 2018, 2019, 2021; not yet ingested), originally developed for ground-based low-resolution spectroscopy (LRG-BEASTS) and extended to JWST NIRSpec G395H, NIRSpec PRISM, and MIRI/LRS. Features custom bad-pixel handling, Gaussian trace fitting, and aperture photometry suited to bright-target time-series. The Edinburgh-Kirk-group pipeline of choice; in the wiki it appears almost universally as a **third independent cross-check reduction** alongside [[Eureka]] + [[ExoTiC-JEDI]] (BOWIE-ALIGN), [[Eureka]] + [[FIREFLy]] (early Cycle-1 rocky-planet papers), or [[Eureka]] + [[SPARTA]] (MIRI reductions). Adopted across BOWIE-ALIGN, COMPASS, Hot Rocks, and the WASP-39 b ERS reductions — making Tiberius the most consistently-applied "third reduction" in the wiki.

## Variants

The wiki sees four Tiberius deployment patterns:

- **Three-pipeline cross-check on hot-Jupiter transmission.** Tiberius + Eureka + ExoTiC-JEDI is the canonical BOWIE-ALIGN (GO 3838) trio:
  - [[2025_Ahrer_KELT7b]] — KELT-7 b NIRSpec G395H BOWIE-ALIGN transit; identical reduction parameters across BOWIE-ALIGN sample to avoid reduction-dependent biases.
- **Three-pipeline cross-check on rocky-M-dwarf transmission.** Tiberius + Eureka + FIREFLy is the early Cycle-1 trio for null-result NIRSpec G395H rocky-planet transits:
  - [[2023_Lustig-Yaeger_LHS475b]] — LHS 475 b first JWST Earth-sized exoplanet spectrum.
  - [[2023_Moran_GJ486b]] — Gl 486 b NIRSpec G395H transits; Tiberius gives highest flat-line rejection (3.29σ) but an unphysical H₂-dominated secondary retrieval mode is flagged.
- **Cross-check + COMPASS uniform reanalysis.** [[2025_Teske_TOI776c]] uses Tiberius v1.8.2 with weighted average of two visits; standard aperture photometry with 8-pixel aperture.
- **MIRI three-pipeline cross-check.** [[2025_Deka_WASP39b]] uses Tiberius as one of three (Eureka, Tiberius, SPARTA) on WASP-39 b MIRI/LRS within the [[NEXOTRANS]] retrieval-framework benchmark.

Plus several primary-reduction roles:
- [[2025_Redai_GJ357b]] — primary on GJ 357 b NIRSpec G395H (with Eureka cross-check).
- [[2025_Alam_L168-9b]] — one of three independent NIRSpec reductions on L 168-9 b (Tiberius + Aesop + Eureka).
- [[2026_RoyPerez_WASP39b]] — one of four pipelines (Tiberius + FIREFLy + Eureka + Tshirt) in the canonical 4-pipeline systematics study on WASP-39 b PRISM ERS data.
- [[2025_Coulombe_TOI-270b]] — NIRSpec G395H reduction on the simultaneous TOI-270 b + d transit (companion paper context).

## History

- **2018–2021** — Tiberius developed for the LRG-BEASTS ground-based program (Kirk 2018, 2019, 2021); extended to JWST NIRSpec around 2022.
- **2023** — first JWST appearances in [[2023_Lustig-Yaeger_LHS475b]] and [[2023_Moran_GJ486b]] as third independent cross-check on rocky-planet G395H spectra.
- **2025** — adoption broadens: Cycle-2 hot-Jupiter (KELT-7 b in BOWIE-ALIGN), COMPASS rocky-planets (TOI-776 c), independent reductions on bright targets (L 168-9 b, GJ 357 b), data-reduction systematics studies (WASP-39 b in [[2026_RoyPerez_WASP39b]]).

## Trade-offs

- **Strength: independence of approach.** Originally ground-based, Tiberius brings a distinct philosophy to JWST reductions — aperture photometry rather than optimal extraction in some cases, simpler systematics models. Independence from the dominant Eureka tool chain is a methodological asset.
- **Strength: BOWIE-ALIGN cross-survey consistency.** Identical reduction parameters across BOWIE-ALIGN targets (KELT-7 b, WASP-15 b, TrES-4 b) eliminate reduction-dependent biases at the program level.
- **Limitation: Tiberius can over-fit when paired with Eureka discrepancies.** [[2023_Moran_GJ486b]] flags the Tiberius reduction's unphysical H₂-dominated secondary retrieval mode as a warning sign — flat-line rejection at 3.29σ does not guarantee physically sensible retrievals.
- **Limitation: Light on stellar-contamination handling.** Where pipelines like [[transitspectroscopy]] integrate GP marginalization over stellar contamination at the reduction layer, Tiberius leaves this to downstream codes.
- **Limitation: Less feature-rich for limb-resolved or 1/f-sensitive applications.** No `refine_soss_timestamps`-equivalent for NIRISS limb-asymmetry; no Eureka-like dynamic ECF reconfiguration.

## Open issues

- **Pipeline-induced abundance variation.** [[2026_RoyPerez_WASP39b]] documents up to 2 dex pipeline-induced retrieval abundance variation on WASP-39 b PRISM across Eureka / FIREFLy / Tiberius / Tshirt. Tiberius is part of the spread; whether different reduction philosophies cause systematic biases or just sample noise is open.
- **Unphysical retrieval modes.** [[2023_Moran_GJ486b]] flagged a Tiberius-specific unphysical H₂-dominated secondary mode; whether the issue is reproducible elsewhere is unclear.

## Papers

### Hot Jupiter — three-pipeline cross-check
- [[2025_Ahrer_KELT7b]] — Tiberius + Eureka + ExoTiC-JEDI on KELT-7 b NIRSpec G395H (BOWIE-ALIGN).

### Rocky M-dwarf transmission — three-pipeline cross-check
- [[2023_Moran_GJ486b]] — highest flat-line rejection (3.29σ) but unphysical H₂-dominated secondary mode flagged.
- [[2023_Lustig-Yaeger_LHS475b]] — LHS 475 b first JWST Earth-sized spectrum.

### COMPASS / Hot Rocks single-target
- [[2025_Teske_TOI776c]] — TOI-776 c two-visit cross-check (v1.8.2); 8-pixel aperture.
- [[2025_Redai_GJ357b]] — primary on GJ 357 b NIRSpec G395H (Eureka cross-check).
- [[2025_Alam_L168-9b]] — one of three independent reductions (with Aesop, Eureka).

### Methodology / systematics study
- [[2026_RoyPerez_WASP39b]] — one of four pipelines in the WASP-39 b PRISM ERS reduction systematics study.
- [[2025_Deka_WASP39b]] — one of three MIRI/LRS reductions (Eureka, Tiberius, SPARTA) for [[NEXOTRANS]] benchmark.

### Multi-planet / specialty
- [[2025_Coulombe_TOI-270b]] — simultaneous TOI-270 b + d NIRSpec G395H transit (companion paper context).
