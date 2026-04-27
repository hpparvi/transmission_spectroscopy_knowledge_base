---
type: paper
bibkey: 2025_PiauletGhorayeb_TRAPPIST1d
authors: [Piaulet-Ghorayeb, C., Benneke, B., Radica, M., Lafrenière, D., et al.]
year: 2025
venue: ApJ
doi: 10.3847/1538-4357/adf207
targets: [TRAPPIST-1d]
instruments: [JWST-NIRSpec]
methods: [transmission-spectroscopy, stellar-contamination-modeling, atmospheric-retrievals, multi-visit-stacking]
species_ruled_out: [H2O]
codes: [Eureka, stctm, SCARLET]
tags: [trappist-1, habitable-zone, rocky-planet, m-dwarf-host, ultracool-dwarf-host, nirspec-prism, neat-gto, stellar-contamination]
ingested: 2026-04-27
---

# TRAPPIST-1 d with JWST NIRSpec/PRISM: No Evidence for a Thick Atmosphere

**Authors:** Piaulet-Ghorayeb, C., Benneke, B., Radica, M., Lafrenière, D., et al. (2025, ApJ 989:181)
**Targets:** [[TRAPPIST-1d]] · **Instrument:** [[JWST-NIRSpec]] (PRISM, 0.6–5.2 μm) · **Program:** [[JWST-GTO-1201]]

## TL;DR
Two JWST NIRSpec PRISM transits of TRAPPIST-1 d (November 5 and 9, 2022; GTO 1201 NEAT, PI: Lafrenière) yield a flat transmission spectrum over 0.6–5.2 μm at ±100–150 ppm precision. H₂-dominated atmospheres are excluded at >3σ. Cloud-free terrestrial secondary atmospheres resembling Venus, early Mars, and modern Earth are ruled out at >95% confidence. An N₂-dominated atmosphere with low CO₂ abundance remains consistent with the data but unconstrained. Stellar contamination from TRAPPIST-1's heterogeneous photosphere is modeled with the new [[stctm]] code.

## Key findings
- Two PRISM transits: November 5 and November 9, 2022; SUB2048 subarray; program GTO 1201 (PI: D. Lafrenière, NEAT survey).
- **Flat transmission spectrum** at ±100–150 ppm over 0.6–5.2 μm; no molecular feature detected above noise.
- **H₂-dominated atmospheres excluded at >3σ**: a cloud-free, solar-composition H₂-rich atmosphere is inconsistent with the flat spectrum.
- **Cloud-free terrestrial analogs excluded at >95%**: Venus-like (96% CO₂), early-Mars-like, and modern-Earth-like cloud-free atmospheric scenarios are each ruled out. High-altitude cloud or haze decks could, in principle, suppress features from such atmospheres below detection, but are physically disfavored.
- **N₂-dominated atmosphere consistent with data**: a nitrogen-rich atmosphere with low CO₂ mixing ratio is not constrained by the current data — additional transits would be needed to probe or rule out this scenario.
- Stellar contamination is modeled using the [[stctm]] framework (Piaulet-Ghorayeb et al. 2024); contamination corrections are incorporated into the final transmission spectrum.
- The combined spectrum is consistent with a bare-rock interpretation but does not firmly rule out a thin or N₂-dominated secondary atmosphere.

## Methods
Primary reduction with [[Eureka]] (T. Bell et al. 2022). Stellar contamination modeling with [[stctm]] (C. Piaulet-Ghorayeb et al. 2024; github.com/cpiaulet/stctm), which incorporates the exotune sub-framework for fitting TRAPPIST-1 heterogeneous photosphere models. Atmospheric retrievals with [[SCARLET]] (B. Benneke & S. Seager 2012, 2013; B. Benneke 2019), a transmission-spectroscopy Bayesian retrieval framework. Limb-darkening from PHOENIX stellar models.

## Caveats & limitations
- With only two transits, the photon-limited precision (±100–150 ppm) is insufficient to probe N₂-dominated secondary atmospheres — a definitive null result on all secondary atmosphere scenarios requires more visits.
- Stellar contamination modeling for M8V TRAPPIST-1 remains model-dependent; stctm mitigates this but does not eliminate the photospheric uncertainty.
- The two visits are separated by only four days — insufficient temporal baseline to sample TRAPPIST-1's spot/faculae variability over longer rotation periods.

## Open questions / follow-ups
- Can additional PRISM visits constrain or rule out an N₂-rich secondary atmosphere on TRAPPIST-1 d?
- How do the TRAPPIST-1 d results compare with the emerging picture from d, e, and f together: is there a pattern of atmosphere loss across the habitable-zone planets?

## Related
- [[2025_Glidden_TRAPPIST1e]] — same system (TRAPPIST-1 e), same instrument mode (NIRSpec PRISM), DREAMS GTO 1331; companion atmospheric constraint for the habitable-zone planet.
- [[2025_Espinoza_TRAPPIST1e]] — data reduction + stellar contamination companion to Glidden for TRAPPIST-1 e; GP marginalization approach contrasts with the stctm approach used here.
- [[2023_Lim_TRAPPIST1b]] — NIRISS/SOSS observations of TRAPPIST-1 b; stellar contamination discussion context.
- [[2025_Rathcke_TRAPPIST1bc]] — back-to-back NIRSpec PRISM transits of TRAPPIST-1 b and c; empirical contamination correction contrasts with stctm.
