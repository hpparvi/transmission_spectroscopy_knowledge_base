---
type: target
kind: star
class: M
aliases: [2MASS J23062928-0502285, TRAPPIST-1 host]
mass_msun: 0.0898
radius_rsun: 0.1192
teff_k: 2566
feh_dex: 0.05
tags: [m-dwarf, ultracool-dwarf, planet-host, active, heterogeneous-photosphere]
---
What pa
# TRAPPIST-1 (hub)

A nearby (12.5 pc) M8V ultracool dwarf hosting seven transiting terrestrial planets (Gillon et al. 2016, 2017; both not yet ingested). With Teff ≈ 2566 ± 26 K, R = 0.1192 R☉, M = 0.0898 M☉, and [Fe/H] = +0.05 (Agol et al. 2021; not yet ingested), it is the lowest-mass star in this wiki with confirmed atmospheric observations. The photosphere is highly heterogeneous, with JWST/NIRSpec PRISM spectra consistently yielding a 2-component model of ~55–56% coverage of a ≤2000 K cool component (at the SPHINX grid floor) and ~44% of a ~2600 K warm component ([[2025_Rathcke_TRAPPIST1bc]]). This heterogeneity is the dominant systematic — larger than photon noise — for all atmospheric searches in the system, and has been addressed via three distinct strategies across five published JWST papers: explicit photospheric model subtraction, GP marginalization, and empirical back-to-back transit correction.

## Basic properties

| Parameter | Value | Source |
|-----------|-------|--------|
| Spectral type | M8V | literature |
| Distance | 12.5 pc | literature |
| T_eff | 2566 ± 26 K | Agol et al. 2021 |
| R★ | 0.1192 R☉ | Agol et al. 2021 |
| M★ | 0.0898 M☉ | Agol et al. 2021 |
| [Fe/H] | +0.05 | Agol et al. 2021 |
| Photospheric model | ~55.6% ≤2000 K + ~44.4% ~2600 K | [[2025_Rathcke_TRAPPIST1bc]] |
| Cool-component variability | ~0.1%/hr covering fraction | [[2025_Rathcke_TRAPPIST1bc]] |

Known planets: b, c, d, e, f, g, h (Gillon et al. 2016, 2017; not yet ingested). JWST observations now cover **b, c, d, e, f, and g** — the wiki has analyses or methodology papers for each except h.

## Atmospheric composition

No atmospheric species have been detected in any TRAPPIST-1 planet observed with JWST to date. All published transmission spectra are consistent with flat lines at ≥100 ppm precision. The constraints to date are exclusions:

- **H₂-dominated atmospheres** ruled out at 16–29σ for b ([[2023_Lim_TRAPPIST1b]]), >3σ for d ([[2025_PiauletGhorayeb_TRAPPIST1d]]), and implied for e ([[2025_Glidden_TRAPPIST1e]]).
- **H₂-CO₂ mixtures** (μ ≤ 5.82) ruled out at 5σ for e ([[2025_Glidden_TRAPPIST1e]]).
- **Thick pure [[CO2]] atmospheres** ruled out at 6.9σ for e ([[2025_Glidden_TRAPPIST1e]]).
- **Cloud-free Venus/early Mars/modern Earth analogs** ruled out at >95% confidence for d ([[2025_PiauletGhorayeb_TRAPPIST1d]]).
- **Cloudy H₂-dominated (≥80% by volume) atmospheres** ruled out at >3σ for e ([[2025_Espinoza_TRAPPIST1e]]).
- **N₂-dominated secondary atmospheres** remain consistent with data for both d ([[2025_PiauletGhorayeb_TRAPPIST1d]]) and e ([[2025_Glidden_TRAPPIST1e]]).
- **Mean molecular weight** constrained to μ > 8.6 ± 0.4 u for e ([[2025_Glidden_TRAPPIST1e]]).

## Observations to date

**2022 July — TRAPPIST-1 b (NIRISS/SOSS):** Two NIRISS/SOSS transits on 2022 July 18 and 20 (program [[JWST-GO-2589]], PI: Lim). The spectra are dominated by stellar contamination — Visit 1 by cool spots (~29%, Δ−197 K) and Visit 2 by faculae (~29%, Δ+153 K) — illustrating the rapid evolution of TRAPPIST-1's photosphere over two days. After contamination modeling, the planetary spectrum is featureless. H₂-dominated atmospheres rejected at 16–29σ; secondary atmospheres unconstrained ([[2023_Lim_TRAPPIST1b]]).

**2022 November — TRAPPIST-1 d (NIRSpec PRISM):** Two NIRSpec PRISM transits on 2022 November 5 and 9 (program [[JWST-GTO-1201]], PI: Lafrenière, NEAT survey). Flat at ±100–150 ppm over 0.6–5.2 μm. H₂ excluded >3σ; cloud-free Venus/early Mars/modern Earth excluded >95%; N₂-rich consistent ([[2025_PiauletGhorayeb_TRAPPIST1d]]).

**2023 June–October — TRAPPIST-1 e (NIRSpec PRISM):** Four NIRSpec PRISM transits on 2023 June 22, June 28, July 23, and October 28 (program [[JWST-TST-GTO-1331]], DREAMS, PI: Mountain). Visits 3 (midtransit flare) and 4 show the strongest contamination; Visit 1 is 774+116/−120 ppm deeper in white light than Visit 2 (>5σ). Stellar model fidelity (~1800 ppm per pixel at R~15) exceeds observational precision (~89 ppm combined). Two companion papers: [[2025_Espinoza_TRAPPIST1e]] (data reduction + GP marginalization over contamination; cloudy H₂-dominated atmospheres ruled out >3σ) and [[2025_Glidden_TRAPPIST1e]] (atmospheric forward-modeling; H₂-CO₂ 5σ; thick CO₂ 6.9σ; μ > 8.6 u; N₂-rich consistent).

**2024 July — TRAPPIST-1 b + c back-to-back (NIRSpec PRISM):** Single visit on 2024 July 9 (program [[JWST-GO-2420]], PI: Rathcke), observing b and c back-to-back. Method validation: both planets show highly consistent contamination signals; dividing c by b yields 2.5× red-noise reduction at 0.8–2 μm. Well-mixed photosphere geometry inferred: cool-component coverage in the transit chord nearly equals disk average, reducing predicted CO₂-band contamination amplitude by ~6× vs. the fully-unocculted assumption ([[2025_Rathcke_TRAPPIST1bc]]).

## Open questions

- **N₂-dominated atmosphere on d and e**: neither planet's current data can rule out a nitrogen-dominated secondary atmosphere. Additional PRISM visits (scaling as 1/√N) are the prescribed path to probe this scenario.
- **Pattern across the system**: b, c, d, and e all show no thick atmosphere; f, g, h remain unobserved by JWST. Is there a systematic trend with orbital distance / irradiation?
- **Stellar model fidelity**: PHOENIX models (and the SPHINX grid, which floors at 2000 K) systematically fail to reproduce TRAPPIST-1's wavelength-dependent contamination features, particularly at λ < 3 μm ([[2025_Espinoza_TRAPPIST1e]]). The GP marginalization approach ([[2025_Espinoza_TRAPPIST1e]]) and the stctm model-fitting approach ([[2025_PiauletGhorayeb_TRAPPIST1d]]) are complementary responses; neither fully resolves the underlying stellar-model limitation.
- **Contamination geometry**: the well-mixed photosphere model from Rathcke 2025 (cool component ~equally distributed in and out of chord) reduces the predicted long-wave contamination budget ~6×, but has not yet been confirmed independently.
- **Tentative CH₄ hint on e**: Glidden et al. 2025 note a tentative forward-model preference for trace CH₄ in an N₂ background; explicitly stated as not a detection; unconstrained pending improved stellar models.

## Tensions

- **Contamination amplitude: NIRISS/SOSS vs NIRSpec/PRISM.** Lim 2023 ([[2023_Lim_TRAPPIST1b]]) measured ~750–1000 ppm peak-to-peak at 0.6–2.8 μm; Rathcke 2025 ([[2025_Rathcke_TRAPPIST1bc]]) finds ~280 ppm in the NIRSpec/PRISM 2–5 μm range under the well-mixed geometry. Consistent with wavelength-dependent spot/faculae contrast and the different geometric assumption, not a fundamental contradiction.
- **Well-mixed vs. fully-unocculted photosphere geometry.** Standard Rackham et al. 2018 formulation predicts ~1740 ppm peak-to-peak at >2.5 μm for the inferred 2-component model; the in-transit + out-of-transit joint fit in [[2025_Rathcke_TRAPPIST1bc]] prefers a well-mixed geometry giving ~280 ppm — a sixfold reduction materially reframing the long-wavelength contamination budget. See [[stellar-contamination]] for the full tension entry.
- **GP marginalization vs. explicit photospheric model.** [[2025_Espinoza_TRAPPIST1e]] demonstrates that current PHOENIX/SPHINX models cannot reproduce TRAPPIST-1's contamination features and uses a GP as a workaround; [[2025_PiauletGhorayeb_TRAPPIST1d]] applies the [[stctm]] explicit photospheric model. Both papers find flat spectra, but the residual uncertainties and the propagated atmospheric constraints differ. There is no fundamental contradiction — the approaches are complementary — but the preferred strategy for future multi-visit stacking campaigns remains open.

## Papers

### NIRSpec PRISM (2022–2024)
- [[2025_PiauletGhorayeb_TRAPPIST1d]] — NEAT GTO 1201; two Nov 2022 transits of TRAPPIST-1 d; flat; H₂ excl >3σ; cloud-free terrestrial analogs excl >95%; stctm contamination modeling
- [[2025_Glidden_TRAPPIST1e]] — DREAMS GTO 1331; four Jun–Oct 2023 transits of TRAPPIST-1 e; H₂-CO₂ excl 5σ; thick CO₂ excl 6.9σ; μ > 8.6 u; N₂-rich consistent
- [[2025_Espinoza_TRAPPIST1e]] — DREAMS GTO 1331; companion to Glidden; GP marginalization over stellar contamination; cloudy H₂ (≥80%) excl >3σ
- [[2025_Rathcke_TRAPPIST1bc]] — GO 2420; back-to-back Jul 2024 transits of b+c; 2.5× red-noise reduction; well-mixed photosphere geometry; methodology paper

### NIRISS/SOSS (2022)
- [[2023_Lim_TRAPPIST1b]] — GO 2589; two Jul 2022 transits of TRAPPIST-1 b; spots+faculae contamination; H₂ excl 16–29σ; secondary atm unconstrained

### MIRI F1500W secondary eclipses (reanalysis)
- [[2025_Connors_MIRI-15um]] — uniform FN-PCA reanalysis of TRAPPIST-1 b (5 visits, GTO 1177; original Greene et al. 2023 not yet ingested) and TRAPPIST-1 c (4 visits, GO 2304; original Zieba et al. 2023 not yet ingested). TRAPPIST-1 b T_day = 499 ± 24 K (low-albedo bare rock); TRAPPIST-1 c T_day = 344 +43/−52 K — ~36 K cooler than Zieba 2023 (potential tension), favoring a semireflective bare rock or thin O₂/CO₂ atmosphere.

### Methodology / flare characterization
- [[2025_Howard_TRAPPIST1_flares]] — characterizes six >10³⁰ erg flares on TRAPPIST-1 from JWST NIRISS/SOSS and NIRSpec PRISM transmission visits of [[TRAPPIST-1b]], [[TRAPPIST-1c]], [[TRAPPIST-1f]], [[TRAPPIST-1g]] (GO 2589 and GTO 1201). Introduces empirical and [[RADYN]]-based [[flare-mitigation]] pipelines that drop residual transit-spectrum noise to 54–65 ppm; first wiki characterization of TRAPPIST-1 f and g.
