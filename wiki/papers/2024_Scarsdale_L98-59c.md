---
type: paper
bibkey: 2024_Scarsdale_L98-59c
authors: [Scarsdale, N., Wogan, N., Wakeford, H. R., Wallack, N. L., Batalha, N. E., Alderson, L., Wolfgang, A., Teske, J., Moran, S. E., López-Morales, M., Kirk, J., Gordon, T., Batalha, N. M., Gao, P., Adams Redai, J.]
year: 2024
venue: AJ
doi: 10.3847/1538-3881/ad73cf
targets: [L98-59c]
instruments: [JWST-NIRSpec]
methods: [transmission-spectroscopy, multi-visit-stacking]
species_detected: []
species_tentative: []
species_ruled_out: [H2, CH4]
codes: [Eureka, ExoTiC-JEDI, PICASO]
tags: [super-earth, m-dwarf-host, rocky-planet, jwst-go-2512, compass, multi-planet-system, flat-spectrum]
ingested: 2026-04-23
---

# JWST COMPASS: The 3–5 μm Transmission Spectrum of the Super-Earth L 98-59 c

**Authors:** Scarsdale, Wogan, Wakeford, Wallack, N. E. Batalha, et al. (2024, AJ 168:276) · [doi:10.3847/1538-3881/ad73cf]
**Target:** [[L98-59c]] · **Host:** [[L98-59]] · **Instrument:** [[JWST-NIRSpec]] (G395H, 2.87–5.05 μm)
**Program:** [[JWST-GO-2512-COMPASS]]

## TL;DR
Two JWST NIRSpec/G395H transits of the warm super-Earth L 98-59 c (1.385 R⊕, 2.22 M⊕, Teq=553 K) reduced with [[Eureka]] and [[ExoTiC-JEDI]] yield a **featureless transmission spectrum** at 22 ppm (NRS1) and 36 ppm (NRS2) per 30-pixel bin (R~200). [[PICASO]] forward modeling **rules out primordial H₂–He atmospheres** to cloud pressures of ≥0.1 mbar and atmospheric metallicities **<300× solar at 3σ** (MMW ≤10 g/mol). Pure CH₄ atmospheres are also excluded. Compatible scenarios: no atmosphere at all, or high-MMW CO₂- or H₂O-rich atmospheres. L 98-59 c adds to the growing evidence that planets ≲1.5 R⊕ around M dwarfs lack clear extended atmospheres.

## Key findings
- Two transits 2023-07-09 and 2023-07-13 (separated by one orbital period; deliberate short cadence to minimize stellar variability).
- Combined precision 22 ppm (NRS1) / 36 ppm (NRS2) in R~200 bins — ~1.3× worse than PandExo predictions.
- Feature-detection Bayes factors for Gaussian models against a flat line are all <1.2 → no statistically preferred features.
- Eureka! and ExoTiC-JEDI reductions agree within ~1σ; some residual red noise present in the white-light curves.
- **H₂/He atmospheres rejected** for cloud-top pressures up to 0.1 mbar.
- **Metallicities <300× solar ruled out at 3σ**; MMW ≤10 g/mol excluded; for H₂–CO₂ mixtures, ≲10% CO₂ (MMW ≤8 g/mol) ruled out at 3σ; for H₂–H₂O, ≤0.5 H₂O mole fraction (MMW ≤10 g/mol) ruled out.
- Remaining compatible scenarios: airless, or high-MMW atmospheres (CO₂- or H₂O-rich) with high clouds / low surface pressure.
- Significantly tighter than the prior HST spectrum of L 98-59 c (Barclay et al. 2023; not yet ingested), which ruled out <80× solar.

## Methods
- **Observations:** two NIRSpec/G395H transits under [[JWST-GO-2512-COMPASS]] (PIs N. E. Batalha + Teske).
- **Reduction:** [[Eureka]] (primary) and [[ExoTiC-JEDI]] pipelines run in parallel.
- **Light-curve fitting:** `batman` transit + linear + trace-position systematics `S(λ) = s₀ + s₁·t + s₂·xₛ|yₛ|`; `emcee` MCMC, 50,000 steps after burn-in; joint visit fit for final transmission spectrum.
- **Feature detection:** Gaussian-feature nested-sampling Bayes-factor tests at 4.4 μm (CO₂) and 3.3 μm (CH₄) specifically; also unconstrained-center Gaussian.
- **Forward modeling:** [[PICASO]] grid at chemical equilibrium via Cantera across H₂/H₂O/CO₂/CH₄ mixtures and metallicities from 1× to 1000× solar; opaque-pressure levels from 10⁻⁴ to 1 bar; Guillot T–P profile.
- **Coadding:** joint fit for Eureka!, weighted mean for ExoTiC-JEDI — see [[multi-visit-stacking]].

## Caveats & limitations
- Red noise is present in white-light curves → best-fit parameters disagree between detectors and visits at ~2σ before fixing inclination to literature value.
- L 98-59 c's mass (2.22 M⊕) is the key uncertainty propagating to MMW conversions; revised RV measurements could tighten the scale-height inference.
- No retrievals run — interpretation via forward-model χ² only.
- Precision ~1.3× worse than PandExo predictions, matching the trend flagged in [[2024_Alderson_TOI-836b]] and [[2025_Alderson_TOI-776b]].

## Open questions / follow-ups
- Is L 98-59 c truly airless, or hiding a high-MMW atmosphere with high clouds? MIRI/LRS emission could distinguish.
- How does L 98-59 c compare directly to the sibling L 98-59 d ([[2024_Banerjee_L98-59d]] + [[2024_Gressier_L98-59d]])? The system offers a rare pair of super-Earths around the same bright M-dwarf — L 98-59 c flat, L 98-59 d sulfur-rich. A joint interpretation would test shared-host assumptions.
- Does L 98-59 b (smaller, inner planet, studied under GTO 1201, Damiano et al. 2024; not yet ingested) show the same pattern?

## Tensions
- None directly with prior wiki content.
- System-level contrast with [[2024_Banerjee_L98-59d]] and [[2024_Gressier_L98-59d]] — L 98-59 c featureless vs L 98-59 d sulfur-hints. Not a methodological tension but a genuine astrophysical difference between two planets around the same host: the larger/warmer/tidally-heated d shows sulfur; the smaller/cooler c does not.

## Related
- [[2024_Banerjee_L98-59d]], [[2024_Gressier_L98-59d]] — sibling planet L 98-59 d with sulfur-species hints.
- [[2025_Alam_L168-9b]], [[2024_Alderson_TOI-836b]], [[2025_Alderson_TOI-776b]] — companion JWST COMPASS super-Earth results.
- [[2023_Lustig-Yaeger_LHS475b]], [[2025_Bennett_GJ1132b]] — similar null-detection results on rocky M-dwarf planets.
- Damiano et al. 2024 (not yet ingested) — L 98-59 b NIRISS/SOSS spectrum from GTO 1201.
- Barclay et al. 2023 (not yet ingested) — prior HST/WFC3 L 98-59 c spectrum.
