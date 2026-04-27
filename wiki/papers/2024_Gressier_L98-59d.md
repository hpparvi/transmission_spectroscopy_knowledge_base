---
type: paper
bibkey: 2024_Gressier_L98-59d
authors: [Gressier, A., Espinoza, N., Allen, N. H., Sing, D. K., Banerjee, A., Barstow, J. K., Valenti, J. A., Lewis, N. K., Birkmann, S. M., Challener, R. C., Manjavacas, E., Crouzet, N., de Oliveira, C. A., Beck, T. L.]
year: 2024
venue: ApJL
doi: 10.3847/2041-8213/ad73d1
targets: [L98-59d]
instruments: [JWST-NIRSpec]
methods: [transmission-spectroscopy, atmospheric-retrievals, stellar-contamination-modeling]
species_detected: []
species_tentative: [H2S, SO2]
species_ruled_out: [primordial-H2]
codes: [transitspectroscopy, FIREFLy, juliet]
tags: [super-earth, m-dwarf-host, rocky-planet, jwst-gto-1224, secondary-atmosphere, sulfur-species, multi-planet-system]
ingested: 2026-04-23
---

# Hints of a Sulfur-rich Atmosphere around the 1.6 R⊕ Super-Earth L 98-59 d from JWST NIRSpec G395H Transmission Spectroscopy

**Authors:** Gressier, Espinoza, Allen, Sing, Banerjee, Barstow, et al. (2024, ApJL 975:L10) · [doi:10.3847/2041-8213/ad73d1]
**Target:** [[L98-59d]] · **Host:** [[L98-59]] · **Instrument:** [[JWST-NIRSpec]] (G395H, 2.87–5.17 μm)
**Program:** [[JWST-GTO-1224]]

## TL;DR
A single JWST NIRSpec/G395H transit of the super-Earth L 98-59 d reveals a **transmission spectrum that deviates from flat at 2.6σ–5.6σ** depending on reduction + retrieval choice. The feature at 3.3–4.8 μm is best fit by an atmosphere containing [[H2S]] (primary driver) and possibly [[SO2]] (bimodal posterior). A stellar-contamination-only retrieval cannot reproduce the feature, so the paper concludes the spectrum is best explained by a **sulfur-bearing atmosphere out of equilibrium**. Companion paper [[2024_Banerjee_L98-59d]] ("Paper II") independently reaches the same conclusion using different retrieval code.

## Key findings
- Feature between 3.3 and 4.8 μm; atmospheric model preferred over flat line at **5.6σ** (free chemistry, `transitspectroscopy` reduction, R~100).
- Equilibrium chemistry retrieval: 2.7σ vs flat line. Free chemistry is preferred over equilibrium by 3.8σ → the atmosphere is not in equilibrium.
- H₂S is the primary opacity source; log X(H₂S) constrained near the prior edge (~0.3). SO₂ mixing ratio is bimodal (either > −1.0 or upper limit < −1.5).
- [[FIREFLy]] reduction yields less significant but consistent atmospheric preference (3.0σ at R~100, 2.6σ at R~60).
- Pure H₂O, CH₄, CO₂, and pure-H₂S [[Exo-REM]] forward models all provide poorer fits than the free-chemistry retrieval; 300× solar equilibrium H₂-rich atmosphere rejected at 3σ+.
- Water mixing ratio upper limit < 10⁻⁵ — the atmosphere is water-poor, but still compatible with a water-rich bulk composition.
- Detected H₂S absorption is inconsistent with equilibrium in the absence of H₂O/CO₂; suggests intense volcanism (Io-analogue).

## Methods
- **Observations:** one transit on 2023-06-25 from [[JWST-GTO-1224]]; 2121 integrations × 6 groups over 5.34 hr.
- **Reduction:** [[transitspectroscopy]] (Espinoza 2022) primary + [[FIREFLy]] (Rustamkulov et al. 2022, 2023; not yet ingested) cross-check. Light curves fit with [[juliet]] + `dynesty`; Matérn-3/2 Gaussian-process detrending via `george`.
- **Forward modeling:** [[Exo-REM]] (Baudino et al. 2015, not yet ingested) at 300× solar equilibrium / non-equilibrium + pure-species grids.
- **Retrieval:** TauREx3 (Al-Refaie et al. 2021; not yet ingested) + exoretrievals (Espinoza et al. 2019; not yet ingested) with MultiNest sampling, 1500 live points.
- **Stellar contamination:** unocculted spots/faculae retrieval via exoretrievals; 1800–3250 K spot temperatures, 3550–5000 K faculae temperatures, 0–100% heterogeneity fraction.
- **Detector-offset test:** NRS1/NRS2 offsets of +37 ppm (`transitspectroscopy`) and −14 ppm ([[FIREFLy]]), both consistent with 0.

## Caveats & limitations
- Single transit; additional visits (second G395H + NIRISS SOSS accepted for Cycle 2) required for confirmation.
- Limb-darkening coefficients poorly constrained due to high impact parameter.
- H₂S posterior runs into the prior upper edge — the inferred abundance may be lower-limit only.
- Light-curve fitting choices (bin size, priors on limb darkening) change the atmospheric significance by ~1σ; no single "best" reduction.
- Between 2.9 and 3.3 μm the two reductions disagree noticeably, contributing to the significance spread.

## Open questions / follow-ups
- Will Cycle 2 JWST follow-up (second NIRSpec G395H + NIRISS SOSS) confirm the H₂S/SO₂ signature?
- What is the origin of sulfur: volcanic outgassing, magma-ocean equilibrium, or photochemistry?
- Can the larger SO₂ features at 7–10 μm be detected with MIRI/LRS?

## Tensions
- Agrees with [[2024_Banerjee_L98-59d]] (companion "Paper II") on the qualitative detection of H₂S/SO₂-driven absorption. Quantitative significance differs (Gressier: 2.6σ–5.6σ depending on reduction; Banerjee: 2.24σ vs stellar-only, 3.5σ vs flat). Different retrieval frameworks (TauREx3 + exoretrievals vs NEMESISPY) may explain the spread.

## Related
- [[2024_Banerjee_L98-59d]] — companion "Paper II" on the same data.
- [[2024_Scarsdale_L98-59c]] — JWST COMPASS on the sibling super-Earth [[L98-59c]]; featureless spectrum.
- Alderson et al. 2023 on WASP-39 b (not yet ingested) — paradigmatic JWST SO₂ detection cited as the hot-Jupiter context.
- Tsai et al. 2023 (not yet ingested) — SO₂ photochemistry predictions.
