---
type: concept
aliases: [transit light source effect, TLSE, unocculted heterogeneities, starspot contamination]
tags: [stellar-heterogeneity, m-dwarf, systematic]
---

# Stellar contamination

The imprint of unocculted photospheric heterogeneities — starspots and faculae outside the transit chord — on a planetary [[transmission-spectrum]] (Rackham et al. 2018). Because the transit samples only the chord, any mismatch between the chord's and the disk's average spectrum produces wavelength-dependent features that can mimic or mask true atmospheric absorption. A dominant systematic for M-dwarf planets and a common confounder in [[atmospheric-retrievals]]. Two complementary mitigation strategies are now in use: model-based retrieval / forward modeling of the heterogeneous photosphere (see [[stellar-contamination-modeling]]) and the empirical [[back-to-back-transit-correction]] using a near-airless reference planet.

## Tensions
- **Fully-unocculted-spot vs. well-mixed-photosphere geometries.** The conventional Rackham et al. 2018 (not yet ingested) parameterization places the inferred cool component entirely outside the transit chord, predicting peak-to-peak contamination amplitudes at λ > 2.5 μm in TRAPPIST-1 of ~1740 ppm under a 2-component (~2000 K + ~2600 K) model. The in-transit + out-of-transit joint fit in [[2025_Rathcke_TRAPPIST1bc]] prefers a **well-mixed** geometry — cool-component coverage in the chord f₁,chord ≈ 0.495 vs disk-average 0.556, only a 6.1% deficit — reducing the predicted >2.5 μm amplitude to **~280 ppm (~6× lower)**. Status: not a contradiction in principle (different geometric assumptions), but materially reframes the long-wavelength contamination budget for late-M-dwarf rocky-planet atmospheric searches.

## Papers
- [[2025_Espinoza_TRAPPIST1e]] — four PRISM transits of TRAPPIST-1 e; Visit 1 white-light depth 774+116/-120 ppm deeper than Visit 2 (>5σ); existing PHOENIX stellar models fail to reproduce wavelength-dependent contamination features (especially λ < 3 μm); GP marginalization over contamination structure enables atmospheric inference.
- [[2025_PiauletGhorayeb_TRAPPIST1d]] — stellar contamination modeled with [[stctm]] for two TRAPPIST-1 d PRISM transits; heterogeneous photosphere model incorporated into transmission spectrum.
- [[2025_Fisher_TOI1685b]] — Sep 1 visit shows 200 ppm quasi-sinusoidal signal in both detectors, modeled as a GP; attributed to instrumental or stellar granulation systematics.
- [[2023_Lim_TRAPPIST1b]] — NIRISS/SOSS TRAPPIST-1 b; contrasting stellar heterogeneities between two transits separated by two days: cool spots in Visit 1 (~−197 K, 29% coverage) and faculae in Visit 2 (~+153 K, 29% coverage); TLS amplitude ~750–1000 ppm peak-to-peak, illustrating the scale of contamination challenge for ultracool-dwarf-hosted planets at blue wavelengths.
- [[2025_Glidden_TRAPPIST1e]] — stellar model uncertainties (~1800 ppm/pixel) exceed observational precision (~89 ppm) for TRAPPIST-1 e NIRSpec PRISM; model fidelity is the dominant limitation for atmospheric characterization in the TRAPPIST-1 system.
- [[2025_Rathcke_TRAPPIST1bc]] — first empirical demonstration of [[back-to-back-transit-correction]]: a 2.5× red-noise reduction at 0.8–2 μm using TRAPPIST-1 b to correct TRAPPIST-1 c. Joint in/out-of-transit analysis prefers a well-mixed photosphere with ~2000 K + ~2600 K components and ~0.1%/hr coverage-fraction variability.
- [[2025_Bennett_GJ1132b]] — evolution of stellar heterogeneity between visits (a large cool spot that rotated off the GJ 1132 disk after Visit 1) is the preferred explanation for the Visit-1 outlier; also speculates on spatially variable stellar CO as a new near-infrared systematic for M-dwarf transit spectra.
- [[2024_WeinerMansfield_GJ486b]] — MIRI/LRS emission constraint on GJ 486 b shows R = 0.97 (airless); the [[2023_Moran_GJ486b]] transmission features must therefore be attributed to stellar contamination, not a water-rich atmosphere. First case where emission selects between scenarios a transmission paper had explicitly left open.
- [[2023_Moran_GJ486b]] — GJ 486 b transmission spectrum fit equally well by a water-rich atmosphere OR ~10% unocculted starspots at 2700 K; independent out-of-transit PHOENIX fits favor the spotted-star scenario.
- [[2024_Gressier_L98-59d]] — unocculted-spots/faculae model cannot reproduce the L 98-59 d spectrum; a sulfur-rich atmosphere is preferred.
- [[2024_Banerjee_L98-59d]] — stellar-contamination-only retrievals rejected in favor of combined stellar+atmosphere scenarios for L 98-59 d.
- [[2023_May_GJ1132b]] — GJ 1132 b Visit 1 is statistically equally well explained by an atmosphere or by ~20% coverage of unocculted starspots ~400 K cooler than the photosphere.
- [[2023_Lustig-Yaeger_LHS475b]] — no stellar contamination detected for LHS 475 b; no spot crossings during transit, low out-of-transit activity; a clean null counter-example to the GJ 1132 b story.
