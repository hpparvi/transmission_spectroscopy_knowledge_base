---
type: paper
bibkey: 2021_Mugnai_GJ1132b
authors: [Mugnai, L. V., Modirrousta-Galian, D., Edwards, B., Changeat, Q., Bouwman, J., et al.]
year: 2021
venue: AJ
doi: 10.3847/1538-3881/abfc3
targets: [GJ1132b]
instruments: [HST-WFC3]
methods: [transmission-spectroscopy, atmospheric-retrievals]
species_ruled_out: [H2O, CH4, CO2]
codes: [Iraclis, TauREX3]
tags: [super-earth, m-dwarf-host, bare-rock, hst-wfc3, ares-survey, null-result]
ingested: 2026-04-28
---

# ARES. V. No Evidence For Molecular Absorption in the HST WFC3 Spectrum of GJ 1132 b

**Authors:** Mugnai, L. V., Modirrousta-Galian, D., Edwards, B., Changeat, Q., et al. (2021, AJ 161:284)
**Targets:** [[GJ1132b]] · **Instrument:** [[HST-WFC3]] (G141, 1.125–1.650 μm) · **Program:** HST Proposal 14758 (PI: Berthiaume)

## TL;DR
The ARES consortium reanalyzed five HST WFC3 G141 transits of GJ 1132 b (observed April–November 2017) and found a **flat transmission spectrum** with no evidence for molecular absorption. Bayesian model comparison strongly favors a cloud-only (flat) model over any scenario with H₂O, CH₄, CO, CO₂, NH₃, or HCN. This directly contradicts Swain et al. 2021 (not yet ingested), which claimed an H₂-dominated atmosphere with HCN and CH₄ features from the same HST dataset. The ARES featureless result is consistent with the later JWST findings of [[2023_May_GJ1132b]] and [[2025_Bennett_GJ1132b]], which close the GJ 1132 b atmospheric question in favor of a bare rock.

## Key findings
- Five transits observed with HST WFC3 G141 (1.125–1.650 μm, spatial scanning, R ≈ 130) under program 14758; reduced with the [[Iraclis]] pipeline.
- Weighted-mean transmission spectrum: (Rp/R★)² = 0.002352 ± 0.0000283; χ²ν = 1.04 for 25 degrees of freedom — consistent with a flat line.
- Bayesian model comparison (TauREX3, MultiNest 1500 live points): the **cloud-only flat model** (log E = 218.52) is the best-fitting scenario. All atmospheric models with molecular species yield lower evidence.
- Molecular species tested and ruled out: H₂O, [[CH4]], CO, [[CO2]], NH₃, HCN. None produce a detectable spectral signature at the precision of this dataset.
- H₂-dominated and H₂-He primordial atmospheres are ruled out.
- The spectrum directly contradicts Swain et al. 2021 (not yet ingested), which reported ±200 ppm features at the same wavelengths; Mugnai et al. find ±50 ppm residuals consistent with noise.
- Jack-knife and autocorrelation tests confirm the residuals are Gaussian white noise.

## Methods
Data reduction with [[Iraclis]] (Tsiaras et al. 2016; not yet ingested), the standard HST WFC3 spatial-scanning pipeline. Atmospheric retrieval with [[TauREX3]] (Al-Refaie et al. 2019; not yet ingested) and the MultiNest nested sampler (Buchner et al. 2014; not yet ingested) with 1500 live points. Limb-darkening computed with ExoTETHyS (Morello et al. 2020; not yet ingested) using PHOENIX 2018 stellar models. An independent reduction with the CASCADe pipeline (Schölkopf et al. 2016; not yet ingested) produces spectra consistent within 1σ.

## Caveats & limitations
- HST WFC3 G141 covers only 1.125–1.650 μm — a narrow window that cannot distinguish between diverse atmospheric scenarios (cloudy primordial, secondary, or bare-rock) at the current precision; multiple scenarios are consistent at 1σ.
- The dataset is identical to that analyzed by Swain et al. 2021 (not yet ingested); the discrepancy originates in reduction and systematics-handling choices, not in the underlying photons.
- No observations at λ < 1.1 μm (where spot/faculae contamination would be detectable) or at λ > 1.65 μm (where CO₂ and other species have stronger bands).

## Tensions
- **Swain et al. 2021 H₂/HCN claim.** Swain et al. (HST/WFC3; not yet ingested) analyzed the same five transits and claimed a 1.53 μm HCN feature and H₂-dominated atmosphere. This paper finds ±50 ppm featureless residuals from the same data; the discrepancy reaches ~200 ppm at the feature wavelengths. The tension is fully resolved by JWST: both JWST visits in [[2023_May_GJ1132b]] rule out the Swain atmosphere at >4.2σ, and the four-visit coadded spectrum in [[2025_Bennett_GJ1132b]] retires it definitively.

## Open questions / follow-ups
- What systematic choice in Swain et al. 2021 produced the discrepant features? A detailed comparison is beyond the scope of this paper but remains an instructive case study in HST-era reduction reproducibility.

## Related
- [[2023_May_GJ1132b]] — two JWST NIRSpec G395H transits; rules out Swain atmosphere at >4.2σ; the Mugnai result is cited as supporting context.
- [[2025_Bennett_GJ1132b]] — four-visit JWST coadd; definitively flat; closes the GJ 1132 b atmospheric question.
- [[2024_Xue_GJ1132b]] — JWST MIRI/LRS emission; T_day consistent with bare rock.
