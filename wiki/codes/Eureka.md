---
type: code
aliases: [Eureka!, Eureka pipeline]
tags: [jwst-pipeline, data-reduction, time-series]
---

# Eureka!

An end-to-end JWST time-series reduction pipeline (Bell et al. 2022), wrapping the `jwst` pipeline for stages 1–2 and performing custom background subtraction, optimal spectral extraction, light-curve fitting, and spectroscopic binning for stages 3–5. Widely adopted for transmission-spectroscopy reductions.

## Papers
- [[2025_Teske_TOI561b]] — primary reduction (alongside [[ExoTiC-JEDI]]) for four TOI-561 b secondary eclipses; G395H emission spectrum.
- [[2025_PiauletGhorayeb_TRAPPIST1d]] — primary reduction for two TRAPPIST-1 d PRISM transits.
- [[2025_Fisher_TOI1685b]] — primary reduction for five TOI-1685 b G395H transits.
- [[2025_Espinoza_TRAPPIST1e]] — one of three independent reductions (primary: [[transitspectroscopy]]) for four TRAPPIST-1 e PRISM transits.
- [[2025_Teske_TOI776c]] — primary joint-fit reduction for both TOI-776 c visits; v1.11.4; custom group-level background subtraction.
- [[2025_Redai_GJ357b]] — cross-check reduction for GJ 357 b NIRSpec G395H transit (primary: [[Tiberius]]).
- [[2024_Xue_GJ1132b]] — cross-check reduction for GJ 1132 b MIRI/LRS secondary eclipse (primary: [[SPARTA]]).
- [[2025_Bennett_GJ1132b]] — reduces all four GJ 1132 b visits (G395H + G395M) with updated calibrations; one of three independent reductions feeding the coadded-spectrum analysis.
- [[2025_Alam_L168-9b]] — one of three independent NIRSpec reductions for L 168-9 b (alongside Aesop and [[Tiberius]]).
- [[2025_Alderson_TOI-776b]] — one of two independent reductions (alongside [[ExoTiC-JEDI]]) for TOI-776 b.
- [[2024_WeinerMansfield_GJ486b]] — cross-check reduction (alongside [[SPARTA]]) for Gl 486 b MIRI/LRS eclipses.
- [[2024_Wachiraphan_LTT1445Ab]] — parallel reduction (alongside [[SPARTA]]) for LTT 1445 A b MIRI/LRS eclipses.
- [[2024_Scarsdale_L98-59c]] — primary reduction (alongside [[ExoTiC-JEDI]]) for L 98-59 c COMPASS spectrum.
- [[2024_Alderson_TOI-836b]] — one of two independent reductions (alongside [[ExoTiC-JEDI]]) for TOI-836 b; used for the joint-fit final spectrum.
- [[2023_May_GJ1132b]] — one of three independent reductions (alongside [[FIREFLy]] and [[ExoTiC-JEDI]]) applied to two GJ 1132 b G395H transits; Eureka! reduction was used for the [[POSEIDON]] retrievals.
- [[2023_Moran_GJ486b]] — primary reduction used for the [[POSEIDON]] retrievals on GJ 486 b (alongside [[FIREFLy]] and [[Tiberius]] as independent cross-checks); most statistically significant flat-line rejection (3.20σ).
- [[2023_Lustig-Yaeger_LHS475b]] — one of three independent reductions (alongside [[FIREFLy]] and [[Tiberius]]) for the LHS 475 b transmission spectrum.
