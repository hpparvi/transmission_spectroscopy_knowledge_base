---
type: concept
aliases: [transit light source effect, TLSE, unocculted heterogeneities, starspot contamination]
tags: [stellar-heterogeneity, m-dwarf, systematics, hub]
---

# Stellar contamination

The imprint of unocculted photospheric heterogeneities — starspots and faculae outside the transit chord — on a planetary [[transmission-spectrum]] ([[2018_Rackham_TLS]], [[2019_Rackham_TLS-FGK]]). Because the transit samples only the chord, any mismatch between the chord's and the disk's average spectrum produces wavelength-dependent features that can mimic or mask true atmospheric absorption. A dominant systematic for M-dwarf planets — almost every wiki paper on a late-M-dwarf host (TRAPPIST-1, L 98-59, GJ 1132, GJ 486, GJ 357, LHS 475, LTT 1445 A, L 168-9, GJ 3929, TOI-1685, TOI-776) addresses contamination as a primary error source — and the leading confounder in [[atmospheric-retrievals]]. Also a live methodological question for *active K-dwarf hot-Jupiter* hosts: the panchromatic Rayleigh slope on [[HD189733b]] attributed to a dust haze in [[2008_Pont_HD189733b]] / [[2013_Pont_HD189733b]] is reinterpreted as unocculted-starspot contamination by [[2014_McCullough_HD189733b]] and [[2019_Rackham_TLS-FGK]] (see HD 189733 b hub `## Tensions`).

## Mitigation strategies

Four complementary strategies appear across the wiki:

1. **Forward / retrieval modeling of the heterogeneous photosphere** (see [[stellar-contamination-modeling]]). 1- to N-component photospheric mixtures with covering fractions are fit jointly with — or as alternatives to — atmospheric models. Codes: [[stctm]] ([[2025_PiauletGhorayeb_TRAPPIST1d]]), [[POSEIDON]] ([[2023_Moran_GJ486b]], [[2023_Lim_TRAPPIST1b]]), [[SCARLET]] ([[2023_Lim_TRAPPIST1b]]), [[SPHINX]] grid ([[2025_Rathcke_TRAPPIST1bc]]).
2. **Empirical reference-planet correction** (see [[back-to-back-transit-correction]]). [[2025_Rathcke_TRAPPIST1bc]] introduces this for JWST: the simultaneous transit of an airless reference planet on the same chord cancels stellar contamination by division.
3. **GP marginalization over contamination structure.** [[2025_Espinoza_TRAPPIST1e]] adopts a Gaussian-process model for the wavelength-correlated contamination signal in TRAPPIST-1 e PRISM data when PHOENIX models fail.
4. **Flare mitigation** (see [[flare-mitigation]]). [[2025_Howard_TRAPPIST1_flares]] introduces both empirical and [[RADYN]] physics-based pipelines for the **stochastic, per-visit** flare component on M-dwarf hosts; complementary to (1)–(3), which target stable spot/facula contamination.

## History

- **HD 189733 b — first hot-Jupiter case (2008–2014).** [[2008_Pont_HD189733b]] introduced unocculted-spot corrections at the ~50 km transit-radius level for HD 189733 b ACS data; [[2013_Pont_HD189733b]] formalized the AC (variability-driven) component correction via 5-year APT photometry + Gaussian-process interpolation; [[2014_McCullough_HD189733b]] then argued for an additional **DC (steady minimum spot dimming)** component at δ ≈ 5.6 % that reinterprets the panchromatic blueward slope as TLS rather than haze.
- **Theoretical framework (2018–2019).** [[2018_Rackham_TLS]] (Paper I, M dwarfs) defined and quantified the TLSE; established that A ∝ f_spot^0.5 (square-root, not linear); showed M-dwarf TLSE is 1–15× the planetary atmospheric signal for rocky targets; biases TRAPPIST-1 densities by Δ(ρ) ≈ −8 %. [[2019_Rackham_TLS-FGK]] (Paper II, FGK dwarfs) extended to F5V–K9V — explicitly cites the McCullough HD 189733 b reinterpretation; demonstrates K-dwarf unocculted-spot contamination produces visible blueward slopes at the magnitude observed.
- **Cycle 1 emergence (2023).** First JWST detections of TLSE-dominated rocky-planet spectra: [[2023_Lim_TRAPPIST1b]] (NIRISS/SOSS TRAPPIST-1 b dominated by spots/faculae across two visits), [[2023_May_GJ1132b]] (NIRSpec G395H GJ 1132 b — Visit 1 atmosphere/spots degenerate), [[2023_Moran_GJ486b]] (NIRSpec G395H GJ 486 b — H₂O atmosphere vs spots equally good fits).
- **Eclipse-side resolution (2024).** [[2024_WeinerMansfield_GJ486b]] uses MIRI/LRS emission to break the GJ 486 b transmission degeneracy — the first wiki case where emission distinguishes atmosphere from contamination scenarios. Set the template for emission-as-arbiter.
- **Cycle 2 stress test (2025).** TRAPPIST-1 system papers ([[2025_Espinoza_TRAPPIST1e]], [[2025_Glidden_TRAPPIST1e]], [[2025_PiauletGhorayeb_TRAPPIST1d]]) show that for ultracool dwarfs, stellar-model fidelity (~1800 ppm) dominates over observational precision (~89 ppm) — TLSE has become the bottleneck.
- **Empirical mitigation (2025).** [[2025_Rathcke_TRAPPIST1bc]] introduces [[back-to-back-transit-correction]]: 2.5× red-noise reduction at 0.8–2 μm.

## Open questions

- **Stellar-model fidelity floor.** PHOENIX, [[SPHINX]], and the like all hit grid-floor temperatures (~2000 K) and saturated-line wing limits below the 1800 ppm/pixel residual seen in TRAPPIST-1. No clear path to atmospheric inference until either models improve or empirical corrections like [[back-to-back-transit-correction]] are applied.
- **Photospheric well-mixedness.** [[2025_Rathcke_TRAPPIST1bc]] argues against the conventional fully-unocculted-spot assumption (see Tensions below); how widely does this generalize to other ultracool dwarfs?
- **Stellar CO bands as a new near-IR systematic.** [[2025_Bennett_GJ1132b]] speculates that spatially variable stellar CO absorption could mimic planetary CO/CO₂ features in NIRSpec G395H/G395M.

## Tensions

- **HD 189733 b panchromatic slope — dust (Pont 2008/2013) vs. unocculted-starspot TLS (McCullough 2014).** Two physically distinct mechanisms reproduce the same 0.3–1 μm STIS+ACS+WFC3 spectrum to comparable Bayesian merit; recorded on the [[HD189733b]] hub. Driver: treatment of the unocculted-spot DC component. [[2019_Rackham_TLS-FGK]] vindicates the *quantitative viability* of the TLS mechanism for K-dwarf hosts at typical activity but does not adjudicate the disagreement on this target.
- **Fully-unocculted-spot vs. well-mixed-photosphere geometries.** The conventional Rackham et al. 2018 (not yet ingested) parameterization places the inferred cool component entirely outside the transit chord, predicting peak-to-peak contamination amplitudes at λ > 2.5 μm in TRAPPIST-1 of ~1740 ppm under a 2-component (~2000 K + ~2600 K) model. The in-transit + out-of-transit joint fit in [[2025_Rathcke_TRAPPIST1bc]] prefers a **well-mixed** geometry — cool-component coverage in the chord f₁,chord ≈ 0.495 vs disk-average 0.556, only a 6.1% deficit — reducing the predicted >2.5 μm amplitude to **~280 ppm (~6× lower)**. Not a contradiction in principle (different geometric assumptions), but materially reframes the long-wavelength contamination budget for late-M-dwarf rocky-planet searches.

## Papers

- [[2019_Rackham_TLS-FGK]] — TLS theory paper for FGK-dwarf hosts; references HD 189733 b explicitly; predicts band-averaged molecular-feature contamination is *not* detectable for typically active FGK dwarfs (with the exceptions of TiO/VO on active late-K, and atomic line wings).
- [[2018_Rackham_TLS]] — foundational TLS theory paper for M-dwarf hosts; A ∝ f_spot^0.5; TRAPPIST-1 case study (f_spot = 8⁺¹⁸⁻⁷ %, f_fac = 54⁺¹⁶⁻⁴⁶ %).
- [[2014_McCullough_HD189733b]] — first reinterpretation of a hot-Jupiter "Rayleigh haze slope" as unocculted-starspot TLS; 5.6 %-spot scenario.
- [[2013_Pont_HD189733b]] — formalizes AC + DC unocculted-spot corrections via APT photometry + Gaussian-process interpolation; sets the procedural benchmark for active K-dwarf contamination handling pre-JWST.
- [[2008_Pont_HD189733b]] — earliest wiki paper to address unocculted-spot contamination at ~50 km transit-radius precision; concludes contamination cannot dominate the slope, motivating the haze interpretation.
- [[2026_Ashtari_HATS75b]] — first wiki paper applying TLS modeling to a **gas-giant on an M-dwarf** ([[GEMS]]) rather than a rocky M-dwarf planet; spots+faculae jointly retrieved with atmospheric parameters; TLS+atmosphere preferred over hazy clear atmosphere.
- [[2025_Ahrer_GJ3090b]] — first wiki paper documenting **TLS-dominated NIRISS/SOSS spectra of a sub-Neptune** with **inter-visit variability** at active M-dwarf timescales: spot/faculae parameters change between two visits separated by 6 months (~10 stellar rotations); a 100 ppm offset between NIRSpec and NIRISS epochs (separated by ~2 months) prevents joint retrieval. Drives the methodological recommendation to schedule cross-instrument visits within one stellar rotation period.
- [[2025_LibbyRoberts_Kepler51d]] — first wiki paper applying TLS modeling to a **young G-dwarf host** rather than an M dwarf: hot-spot ΔT ∼ 300 K above photosphere (>1000 K hotter than typical sunspots); spot/photosphere combinations cannot reproduce the observed 0.6–5.3 μm slope at any covering fraction tested.
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
- [[2025_Canas_TOI5205b]] — **extreme TLS case (>20σ detection)** on the GEMS-class gas-giant TOI-5205 b around an M4 dwarf; clear spot-crossing events in all 3 visits + unocculted-spot TLS contamination driving a strong blueward slope. Spot T_spot = 3156⁺⁴⁵₋₅₆ K (~270 K cooler than 3430 K photosphere); f_spot = 0.132; faculae T_fac = 4263 K, f_fac = 0.015. Demonstrates that **TLS dominates < 3 μm even for gas giants** when the host is an active M dwarf, suppressing H₂O sensitivity.
- [[2025_BelloArufe_L98-59b]] — TLS cross-checks on the sub-Earth L 98-59 b around an M3 dwarf; POSEIDON 7-parameter TLS model jointly fit with atmosphere; TLS-only scenarios rejected at >12σ vs the SO₂-rich atmosphere model. Shows TLS doesn't *replace* an atmospheric inference here — supporting evidence for the [[volcanic-atmosphere]] interpretation.
