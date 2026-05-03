---
type: concept
aliases: [transit light source effect, TLSE, unocculted heterogeneities, starspot contamination]
tags: [stellar-heterogeneity, m-dwarf, systematics, hub]
---

# Stellar contamination

The imprint of unocculted photospheric heterogeneities — starspots and faculae outside the transit chord — on a planetary [[transmission-spectrum]] (Rackham et al. 2018; not yet ingested). Because the transit samples only the chord, any mismatch between the chord's and the disk's average spectrum produces wavelength-dependent features that can mimic or mask true atmospheric absorption. A dominant systematic for M-dwarf planets — almost every wiki paper on a late-M-dwarf host (TRAPPIST-1, L 98-59, GJ 1132, GJ 486, GJ 357, LHS 475, LTT 1445 A, L 168-9, GJ 3929, TOI-1685, TOI-776) addresses contamination as a primary error source — and the leading confounder in [[atmospheric-retrievals]].

## Mitigation strategies

Four complementary strategies appear across the wiki:

1. **Forward / retrieval modeling of the heterogeneous photosphere** (see [[stellar-contamination-modeling]]). 1- to N-component photospheric mixtures with covering fractions are fit jointly with — or as alternatives to — atmospheric models. Codes: [[stctm]] ([[2025_PiauletGhorayeb_TRAPPIST1d]]), [[POSEIDON]] ([[2023_Moran_GJ486b]], [[2023_Lim_TRAPPIST1b]]), [[SCARLET]] ([[2023_Lim_TRAPPIST1b]]), [[SPHINX]] grid ([[2025_Rathcke_TRAPPIST1bc]]).
2. **Empirical reference-planet correction** (see [[back-to-back-transit-correction]]). [[2025_Rathcke_TRAPPIST1bc]] introduces this for JWST: the simultaneous transit of an airless reference planet on the same chord cancels stellar contamination by division.
3. **GP marginalization over contamination structure.** [[2025_Espinoza_TRAPPIST1e]] adopts a Gaussian-process model for the wavelength-correlated contamination signal in TRAPPIST-1 e PRISM data when PHOENIX models fail.
4. **Flare mitigation** (see [[flare-mitigation]]). [[2025_Howard_TRAPPIST1_flares]] introduces both empirical and [[RADYN]] physics-based pipelines for the **stochastic, per-visit** flare component on M-dwarf hosts; complementary to (1)–(3), which target stable spot/facula contamination.

## History

- **Pre-JWST framing.** Rackham et al. 2018 (not yet ingested) defined the TLSE and showed the prediction for M-dwarf rocky-planet hosts.
- **Cycle 1 emergence (2023).** First JWST detections of TLSE-dominated rocky-planet spectra: [[2023_Lim_TRAPPIST1b]] (NIRISS/SOSS TRAPPIST-1 b dominated by spots/faculae across two visits), [[2023_May_GJ1132b]] (NIRSpec G395H GJ 1132 b — Visit 1 atmosphere/spots degenerate), [[2023_Moran_GJ486b]] (NIRSpec G395H GJ 486 b — H₂O atmosphere vs spots equally good fits).
- **Eclipse-side resolution (2024).** [[2024_WeinerMansfield_GJ486b]] uses MIRI/LRS emission to break the GJ 486 b transmission degeneracy — the first wiki case where emission distinguishes atmosphere from contamination scenarios. Set the template for emission-as-arbiter.
- **Cycle 2 stress test (2025).** TRAPPIST-1 system papers ([[2025_Espinoza_TRAPPIST1e]], [[2025_Glidden_TRAPPIST1e]], [[2025_PiauletGhorayeb_TRAPPIST1d]]) show that for ultracool dwarfs, stellar-model fidelity (~1800 ppm) dominates over observational precision (~89 ppm) — TLSE has become the bottleneck.
- **Empirical mitigation (2025).** [[2025_Rathcke_TRAPPIST1bc]] introduces [[back-to-back-transit-correction]]: 2.5× red-noise reduction at 0.8–2 μm.

## Open questions

- **Stellar-model fidelity floor.** PHOENIX, [[SPHINX]], and the like all hit grid-floor temperatures (~2000 K) and saturated-line wing limits below the 1800 ppm/pixel residual seen in TRAPPIST-1. No clear path to atmospheric inference until either models improve or empirical corrections like [[back-to-back-transit-correction]] are applied.
- **Photospheric well-mixedness.** [[2025_Rathcke_TRAPPIST1bc]] argues against the conventional fully-unocculted-spot assumption (see Tensions below); how widely does this generalize to other ultracool dwarfs?
- **Stellar CO bands as a new near-IR systematic.** [[2025_Bennett_GJ1132b]] speculates that spatially variable stellar CO absorption could mimic planetary CO/CO₂ features in NIRSpec G395H/G395M.

## Tensions

- **Fully-unocculted-spot vs. well-mixed-photosphere geometries.** The conventional Rackham et al. 2018 (not yet ingested) parameterization places the inferred cool component entirely outside the transit chord, predicting peak-to-peak contamination amplitudes at λ > 2.5 μm in TRAPPIST-1 of ~1740 ppm under a 2-component (~2000 K + ~2600 K) model. The in-transit + out-of-transit joint fit in [[2025_Rathcke_TRAPPIST1bc]] prefers a **well-mixed** geometry — cool-component coverage in the chord f₁,chord ≈ 0.495 vs disk-average 0.556, only a 6.1% deficit — reducing the predicted >2.5 μm amplitude to **~280 ppm (~6× lower)**. Not a contradiction in principle (different geometric assumptions), but materially reframes the long-wavelength contamination budget for late-M-dwarf rocky-planet searches.

## Papers

- [[2026_Ashtari_HATS75b]] — first wiki paper applying TLS modeling to a **gas-giant on an M-dwarf** ([[GEMS]]) rather than a rocky M-dwarf planet; spots+faculae jointly retrieved with atmospheric parameters; TLS+atmosphere preferred over hazy clear atmosphere.
- [[2025_Howard_TRAPPIST1_flares]] — quantifies that flares contaminate 50–70% of TRAPPIST-1 transits at the ~1000 ppm level (vs ~100 ppm atmospheric signals); introduces [[flare-mitigation]] as the fourth-strategy complement to spot/facula modeling, BBT correction, and GP marginalization.
- [[2025_Espinoza_TRAPPIST1e]] — four PRISM transits of TRAPPIST-1 e; Visit 1 white-light depth 774 ppm deeper than Visit 2 (>5σ); PHOENIX models fail; GP marginalization enables atmospheric inference.
- [[2025_PiauletGhorayeb_TRAPPIST1d]] — heterogeneous photosphere modeled with [[stctm]] for two TRAPPIST-1 d PRISM transits.
- [[2025_Fisher_TOI1685b]] — Sep 1 visit shows 200 ppm quasi-sinusoidal signal in both detectors; GP-modeled; instrumental or stellar granulation.
- [[2025_Glidden_TRAPPIST1e]] — stellar model uncertainties (~1800 ppm/pixel) exceed observational precision (~89 ppm); model fidelity is the dominant systematic.
- [[2025_Rathcke_TRAPPIST1bc]] — first empirical [[back-to-back-transit-correction]]; 2.5× red-noise reduction at 0.8–2 μm; well-mixed-photosphere preferred.
- [[2025_Bennett_GJ1132b]] — evolution of stellar heterogeneity between visits explains the Visit-1 outlier on GJ 1132 b; speculates on stellar CO as a new IR systematic.
- [[2024_WeinerMansfield_GJ486b]] — MIRI emission resolves the [[2023_Moran_GJ486b]] degeneracy in favor of starspot contamination.
- [[2024_Gressier_L98-59d]] — unocculted-spots/faculae model cannot reproduce L 98-59 d spectrum; sulfur-rich atmosphere preferred.
- [[2024_Banerjee_L98-59d]] — stellar-contamination-only retrievals rejected; combined stellar+atmosphere scenarios preferred.
- [[2023_Lim_TRAPPIST1b]] — TLS amplitude ~750–1000 ppm peak-to-peak between two visits; spots Visit 1, faculae Visit 2.
- [[2023_Moran_GJ486b]] — H₂O atmosphere or ~10% unocculted starspots at 2700 K fit equally well; out-of-transit PHOENIX fits favor spots.
- [[2023_May_GJ1132b]] — Visit 1 explainable as atmosphere or ~20% coverage of unocculted starspots ~400 K cooler than the photosphere.
- [[2023_Lustig-Yaeger_LHS475b]] — no contamination detected for LHS 475 b; clean null counter-example to the GJ 1132 b story.
