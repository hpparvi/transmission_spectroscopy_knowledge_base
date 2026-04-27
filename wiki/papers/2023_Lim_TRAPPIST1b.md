---
type: paper
bibkey: 2023_Lim_TRAPPIST1b
authors: [Lim, O., Benneke, B., Doyon, R., MacDonald, R. J., Piaulet, C., et al.]
year: 2023
venue: ApJL
doi: 10.3847/2041-8213/acf7c4
targets: [TRAPPIST-1b]
instruments: [JWST-NIRISS]
methods: [transmission-spectroscopy, stellar-contamination-modeling, atmospheric-retrievals, multi-visit-stacking]
species_ruled_out: [H2]
codes: [supreme-SPOON, NAMELESS, SOSSISSE, SCARLET, POSEIDON]
tags: [trappist-1, rocky-planet, stellar-contamination, m-dwarf-host, ultracool-dwarf-host, niriss-soss]
ingested: 2026-04-25
---

# Atmospheric Reconnaissance of TRAPPIST-1 b with JWST/NIRISS: Evidence for Strong Stellar Contamination

**Authors:** Lim, O., Benneke, B., Doyon, R., MacDonald, R. J., Piaulet, C., et al. (2023, ApJL 955:L22)
**Targets:** [[TRAPPIST-1b]] · **Instrument:** [[JWST-NIRISS]] (SOSS, 0.6–2.8 μm) · **Program:** [[JWST-GO-2589]]

## TL;DR
Two JWST NIRISS/SOSS transits of TRAPPIST-1 b in July 2022 reveal extraordinarily strong stellar contamination — the dominant spectral signal in both visits — from contrasting photospheric heterogeneities: cool spots in Visit 1 and warm faculae in Visit 2, each at ~29% covering fraction. After modeling the [[stellar-contamination]], no planetary atmospheric signatures are detected and H₂-dominated atmospheres are rejected at 16–29σ. Secondary atmospheres (N₂, H₂O, CO₂, CH₄-dominated) can be neither confirmed nor ruled out. NIRISS/SOSS contamination amplitudes (~750–1000 ppm peak-to-peak) are notably larger than those seen later in NIRSpec/PRISM observations of the same system ([[2025_Rathcke_TRAPPIST1bc]]).

## Key findings
- **Visit 1 (2022 Jul 18):** transmission spectrum dominated by unocculted cool spots; sequential stellar-contamination fit prefers ~29% covering fraction of spots ~197 K cooler than the photosphere; Bayes factor logBF = 5.3 over flat.
- **Visit 2 (2022 Jul 20):** dominated instead by unocculted faculae; ~29% covering fraction ~153 K warmer than photosphere; logBF = 2.9 over flat.
- The visit-to-visit contrast (spots → faculae over two days) illustrates how rapidly the active TRAPPIST-1 photosphere evolves.
- NIRISS/SOSS TLS amplitude ~750–1000 ppm peak-to-peak; significantly larger than the ~280 ppm NIRSpec/PRISM contamination signal reported in [[2025_Rathcke_TRAPPIST1bc]], due in part to NIRISS's bluer wavelength coverage where spot/faculae contrast peaks.
- After contamination correction: **no planetary atmosphere signatures**. Spectrum consistent with flat or high-MMW atmosphere.
- Cloud-free H₂-dominated atmospheres rejected at **29σ** (1× solar) and **16σ** (100× solar) via [[SCARLET]] frequentist comparison to a featureless baseline.
- Pure CH₄, H₂O, CO₂, and Titan-like atmospheres each yield ≤0.84σ deviation — none can be ruled out or confirmed.
- Simultaneous [[POSEIDON]] joint stellar-contamination + atmosphere retrieval: H₂ abundance < 52% at 3σ (Visit 1 constraint).
- Three independent reductions used: [[supreme-SPOON]], [[NAMELESS]] (most conservative; presented results), [[SOSSISSE]] (new pipeline, described in paper appendix).

## Methods
Two NIRISS/SOSS transits (0.6–2.8 μm, R~700) obtained 2022 July 18 and 20. Three reduction pipelines provide cross-check (supreme-SPOON, NAMELESS, SOSSISSE); NAMELESS results adopted as primary. Sequential stellar-contamination + atmosphere fitting using PHOENIX ACES stellar models. Joint simultaneous fitting via [[POSEIDON]] with the Pinhas et al. 2018 (not yet ingested) parameterization. Atmospheric comparison via [[SCARLET]] (Benneke & Seager 2012, 2013; Benneke et al. 2019; not yet ingested) frequentist model selection. MSG stellar models (Townsend & Lopez 2023; not yet ingested) used in some auxiliary comparisons.

## Caveats & limitations
- Only two visits, separated by two days; the spot vs. faculae contrast between visits could be explained by transit chord differences (occulted different photospheric regions) or by rapid surface evolution.
- Sequential stellar-contamination fitting (correcting contamination first, then fitting atmosphere) may not fully propagate stellar-model uncertainties into the atmospheric inference.
- Restricts to a frequentist non-detection of secondary atmospheres — does not provide strong Bayesian upper limits on individual species abundances.

## Tensions
- The NIRISS/SOSS contamination amplitude (~750–1000 ppm peak-to-peak) is ~3× larger than the NIRSpec/PRISM amplitude (~280 ppm) reported for the same star in [[2025_Rathcke_TRAPPIST1bc]]. This is partially wavelength-dependent (NIRISS covers bluer wavelengths with higher stellar contrast) and partially geometric (different TRAPPIST-1 epochs). The two papers use different instruments, wavelength ranges, epochs, and reduction approaches; the difference is consistent with wavelength-dependent TLS amplitudes and temporal photosphere variability rather than a fundamental contradiction.

## Open questions / follow-ups
- Can additional visits with NIRISS/SOSS resolve whether the Visit 1 / Visit 2 discrepancy is due to chord differences or temporal evolution?
- What secondary-atmosphere composition would survive the atmospheric retention constraints now in place for TRAPPIST-1 b?
- Do other TRAPPIST-1 planets observed with NIRISS/SOSS show similarly strong stellar contamination?

## Related
- [[2025_Rathcke_TRAPPIST1bc]] — NIRSpec/PRISM back-to-back transit correction for TRAPPIST-1 b+c; uses TRAPPIST-1 b as a near-airless reference.
- [[2025_Glidden_TRAPPIST1e]] — DREAMS NIRSpec/PRISM results for the habitable-zone planet TRAPPIST-1 e; same stellar contamination challenge.
