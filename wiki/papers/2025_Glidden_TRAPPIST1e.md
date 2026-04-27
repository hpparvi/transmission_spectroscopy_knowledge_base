---
type: paper
bibkey: 2025_Glidden_TRAPPIST1e
authors: [Glidden, A., Ranjan, S., Seager, S., Espinoza, N., MacDonald, R. J., et al.]
year: 2025
venue: ApJL
doi: 10.3847/2041-8213/adf62e
targets: [TRAPPIST-1e]
instruments: [JWST-NIRSpec]
methods: [transmission-spectroscopy, atmospheric-retrievals, stellar-contamination-modeling, multi-visit-stacking]
species_ruled_out: [CO2]
codes: [petitRADTRANS]
tags: [trappist-1, habitable-zone, rocky-planet, m-dwarf-host, ultracool-dwarf-host, nirspec-prism, dreams-gto]
ingested: 2026-04-25
---

# JWST-TST DREAMS: Secondary Atmosphere Constraints for the Habitable Zone Planet TRAPPIST-1 e

**Authors:** Glidden, A., Ranjan, S., Seager, S., Espinoza, N., MacDonald, R. J., et al. (2025, ApJL 990:L53)
**Targets:** [[TRAPPIST-1e]] · **Instrument:** [[JWST-NIRSpec]] (PRISM, 1–5 μm) · **Program:** [[JWST-TST-GTO-1331]]

## TL;DR
Four JWST NIRSpec PRISM transits of the habitable-zone planet TRAPPIST-1 e yield a featureless combined transmission spectrum and rule out H₂-rich and thick pure-CO₂ atmospheres, but cannot confirm or rule out an N₂-rich (secondary) atmosphere. The dominant limitation is not photon noise — it is stellar model fidelity: TRAPPIST-1's M8V photosphere generates model uncertainties ~1800 ppm/pixel that dwarf the ~89 ppm observational precision of the combined spectrum. The paper explicitly concludes "cannot obtain strong evidence for or against an atmosphere."

## Key findings
- Visits 3 and 4 heavily contaminated by stellar activity; Visit 3 contains a midtransit flare. The science analysis therefore distinguishes between (i) visits 1+2 uncorrected and (ii) all four visits combined with a GP-based stellar contamination correction from the companion Espinoza et al. 2025 (not yet ingested).
- Visits 1+2 alone are consistent with a flat line. The GP-corrected four-visit combined spectrum (from [[2025_Espinoza_TRAPPIST1e]]) is also consistent with flat, though with correlated residuals.
- Mean molecular weight constraint (GP-corrected, above 1 μm, requiring 4–5 observable scale heights): **μ > 8.6 ± 0.4 u**.
- H₂-dominated atmospheres ruled out broadly; the specific H₂-CO₂ scenario (μ ≤ 5.82) ruled out at **5σ** using the GP-corrected spectrum ([[JWST-NIRSpec]] sensitivity to the 4.3 μm CO₂ feature).
- Thick pure [[CO2]] atmosphere ruled out at **6.9σ**.
- CO₂-rich (N₂-background) atmospheres weakly disfavored at ~2σ at surface pressures corresponding to Venus cloud-top levels.
- N₂-rich atmospheres broadly consistent with data: **cannot rule out a secondary atmosphere**.
- Tentative forward-model hint: trace [[CH4]] in an N₂-background model fits apparent features at ~1, ~3.3, and ~4.3 μm. Explicitly stated as NOT a detection.
- TRAPPIST-1 stellar model uncertainties (~1800 ppm/pixel, R~15 binning) dominate over observational precision (~89 ppm combined visits 1+2); model fidelity at M8V temperatures is the primary bottleneck for atmospheric characterization in this system.

## Methods
Four transits observed on 2023 June 22, 28, July 23, and October 28. Atmospheric forward models computed with [[petitRADTRANS]] (Mollière et al. 2019; not yet ingested) for H₂-CO₂, pure CO₂, N₂-CO₂, N₂-only, and N₂+CH₄ scenarios. Photochemical modeling with MEAC (Rajan et al. 2022; not yet ingested; prose-only). The GP-corrected spectrum and the joint stellar-contamination retrieval framework are presented in the companion [[2025_Espinoza_TRAPPIST1e]], which uses [[transitspectroscopy]]; the Glidden paper uses those reduced/corrected spectra as input to its atmospheric forward-modeling analysis.

## Caveats & limitations
- The ~1800 ppm/pixel stellar model systematic overwhelms the ~89 ppm observational noise; this is the dominant limitation, not visit count or instrument sensitivity.
- Visits 3 and 4 are stellar-activity-dominated; the four-visit combined GP-corrected result retains correlated residuals.
- The "tentative CH₄ hint" is not statistically significant and the paper explicitly cautions against treating it as a detection.
- The companion [[2025_Espinoza_TRAPPIST1e]] presents the stellar contamination modeling and GP correction pipeline underlying the GP-corrected spectra used here.

## Open questions / follow-ups
- Can next-generation stellar atmosphere models (beyond the current TRAPPIST-1 SPHINX grid floor at ~2000 K) reduce the ~1800 ppm model systematic to a level where secondary atmospheres become testable?
- Does the tentative CH₄ feature persist with improved stellar models or additional visits?
- The DREAMS program covers additional TRAPPIST-1 planets; do other members of the system show consistent results?

## Related
- [[2025_Espinoza_TRAPPIST1e]] — companion paper; data reduction, GP stellar contamination marginalization, and atmospheric inference underpinning the GP-corrected spectra used here.
- [[2025_Rathcke_TRAPPIST1bc]] — empirical stellar contamination correction approach in the same system; back-to-back NIRSpec PRISM transits of TRAPPIST-1 b+c.
- [[TRAPPIST-1]] — host star page; photospheric heterogeneity context.
