---
type: code
aliases: [transitspectroscopy pipeline, transitspectroscopy package]
tags: [jwst-pipeline, data-reduction, time-series, nirspec, hub]
---

# transitspectroscopy

A JWST NIRSpec time-series reduction package (Espinoza 2022; github.com/nespinoza/transitspectroscopy; not yet ingested), wrapping the STScI `jwst` pipeline and adding customized jump detection, spectral tracing with Gaussian fits, and column-by-column 1/f background removal. The Espinoza-group pipeline of choice for **NIRSpec PRISM and G395H** time-series spectroscopy across rocky-planet, sub-Neptune, hot-Jupiter, and ultracool-dwarf-host targets — appears as primary reduction or first-among-three cross-check in 7 wiki papers, almost always paired with [[juliet]] for light-curve fitting.

## Variants

The wiki sees three transitspectroscopy deployment patterns:

- **Primary reduction + cross-checks via Eureka / ExoTiC-JEDI / FIREFLy.** The dominant pattern on COMPASS-style and GTO single-target transmission programs:
  - [[2025_Espinoza_TRAPPIST1e]] — primary on four TRAPPIST-1 e PRISM transits with three-pipeline cross-check ([[Eureka]], [[ExoTiC-JEDI]]).
  - [[2025_Gressier_HATP26b]] — primary on HAT-P-26 b NIRSpec G395H BOTS, cross-checked against [[ExoTiC-JEDI]]; both agree at 1σ.
  - [[2024_Gressier_L98-59d]] — primary on L 98-59 d G395H transit, [[FIREFLy]] cross-check.
  - [[2024_Banerjee_L98-59d]] — adopts the Gressier 2024 transitspectroscopy primary reduction for the companion retrieval analysis.
  - [[2025_Fisher_TOI1685b]] — one of three independent reductions ([[Eureka]] primary, [[ExoTiC-JEDI]], transitspectroscopy) for five TOI-1685 b G395H transits.
- **Primary reduction + GP stellar-contamination framework.** [[2025_Espinoza_TRAPPIST1e]] runs transitspectroscopy with a novel GP marginalization over wavelength-correlated stellar contamination (celerite Matèrn 3/2 kernel) — produces the GP-corrected spectrum used by [[2025_Glidden_TRAPPIST1e]] for atmospheric forward modeling.
- **NIRISS/SOSS cross-check.** [[2025_Gressier_WASP17b]] uses transitspectroscopy as one of three independent NIRISS/SOSS reductions (alongside [[supreme-SPOON]] and the new [[Ahsoka]] pipeline) on the WASP-17 b dayside emission spectrum — confirms transitspectroscopy is not strictly NIRSpec-locked.

## History

- **2022** — Espinoza 2022 release (github); rapid uptake within the GTO 1224 (L 98-59) and DREAMS GTO programs.
- **2024** — first wiki appearance on a rocky-planet transmission spectrum ([[2024_Gressier_L98-59d]]); paired with [[juliet]] + Matérn-3/2 GP detrending.
- **2025** — broad adoption: TRAPPIST-1 e PRISM with GP marginalization ([[2025_Espinoza_TRAPPIST1e]]), DREAMS Neptune-mass G395H ([[2025_Gressier_HATP26b]]), TOI-1685 b G395H ([[2025_Fisher_TOI1685b]]), WASP-17 b NIRISS/SOSS dayside emission ([[2025_Gressier_WASP17b]]).

## Trade-offs

- **Strength: first-class GP marginalization on stellar contamination.** [[2025_Espinoza_TRAPPIST1e]] introduces a celerite Matèrn 3/2 kernel that runs *during* light-curve fitting; the GP-corrected spectrum then feeds atmospheric retrievals downstream. No other wiki pipeline integrates GP stellar-contamination handling at the reduction layer this cleanly.
- **Strength: customized jump detection + 1/f.** Custom modules over and above the STScI `jwst` pipeline; addresses NIRSpec PRISM cosmic-ray jump artifacts that vanilla STScI pipeline does not catch.
- **Strength: tight juliet integration.** transitspectroscopy + juliet is the canonical Espinoza-group reduction-to-fit chain; consistent across all wiki papers using the pipeline.
- **Limitation: Espinoza-group ecosystem.** Less independent-of-STScI than [[SPARTA]] (which builds from `_uncal`); transitspectroscopy still wraps STScI stages. Cross-validation against SPARTA on the same dataset is the methodological gold standard but rarely published.
- **Limitation: NIRISS/SOSS support newer.** Used in [[2025_Gressier_WASP17b]] but the Espinoza-group standard for SOSS is supreme-SPOON / Ahsoka.

## Open issues

- **Cross-pipeline reproducibility on PRISM.** [[2025_Espinoza_TRAPPIST1e]] reports good 1σ agreement with Eureka and ExoTiC-JEDI on TRAPPIST-1 e PRISM, but [[2026_RoyPerez_WASP39b]] (a different methodology paper using a different pipeline set) documents up to 2 dex pipeline-induced abundance variation on WASP-39 b PRISM ERS data — the question of whether transitspectroscopy converges as cleanly on bright hot-Jupiter PRISM data is open.

## Papers

### NIRSpec PRISM rocky / temperate M-dwarf hosts
- [[2025_Espinoza_TRAPPIST1e]] — primary on four TRAPPIST-1 e PRISM transits; introduces GP marginalization over stellar contamination via celerite Matèrn 3/2 kernel.
- [[2025_Glidden_TRAPPIST1e]] — uses the [[2025_Espinoza_TRAPPIST1e]] GP-corrected spectrum as input to the atmospheric forward-modeling analysis; transitspectroscopy reduction is the upstream of the joint two-paper workflow.

### NIRSpec G395H — Neptune-mass and rocky
- [[2025_Gressier_HATP26b]] — primary on HAT-P-26 b BOTS; ExoTiC-JEDI cross-check.
- [[2025_Fisher_TOI1685b]] — one of three independent reductions (Eureka primary) on five TOI-1685 b G395H transits.
- [[2024_Gressier_L98-59d]] — primary on L 98-59 d G395H transit; FIREFLy cross-check.
- [[2024_Banerjee_L98-59d]] — adopts the Gressier 2024 reduction for retrieval analysis.

### NIRISS/SOSS — emission cross-check
- [[2025_Gressier_WASP17b]] — one of three independent NIRISS/SOSS reductions (alongside supreme-SPOON and Ahsoka) on WASP-17 b dayside emission.
