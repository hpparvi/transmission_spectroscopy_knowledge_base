---
type: paper
bibkey: 2026_Heinke_HATP12b
authors: [Heinke, L., Min, M., Bouwman, J., Crouzet, N., Konings, T., Decin, L., Waters, L. B. F. M., Lagage, P.-O., et al.]
year: 2026
venue: A&A
arxiv: 2604.01219
targets: [HAT-P-12b]
instruments: [JWST-NIRISS, JWST-NIRSpec, JWST-MIRI, HST-STIS, HST-WFC3]
methods: [transmission-spectroscopy, atmospheric-retrievals, information-content-analysis]
species_detected: [H2O, CO2, CO, H2S]
codes: [exoTEDRF, CASCADe, TEATRO, ARCiS, MultiNest, juliet]
tags: [warm-sub-saturn, k-dwarf-host, panchromatic, information-content, exomiri]
ingested: 2026-04-29
---

# Information content of JWST transmission spectroscopy of the exoplanet HAT-P-12b from the optical to mid-infrared

**Authors:** Heinke, Min, Bouwman, Crouzet, Konings, Decin, Waters, Lagage, et al. (2026, A&A; arXiv:2604.01219)
**Target:** [[HAT-P-12b]] · **Host:** [[HAT-P-12]] (K4/K5V) · **Instruments:** [[JWST-NIRISS]] (SOSS), [[JWST-NIRSpec]] (G395M), [[JWST-MIRI]] (LRS); [[HST-STIS]] + [[HST-WFC3]] archival
**Program:** [[JWST-GTO-1281]] (ExoMIRI European Consortium)

## TL;DR

Panchromatic 0.36–12.4 μm transmission spectroscopy of the warm (~960 K) sub-Saturn [[HAT-P-12b]] combining a new JWST/NIRISS SOSS transit with companion JWST NIRSpec/G395M, JWST/MIRI LRS, HST/STIS, and HST/WFC3 data. **Robust detections of H₂O, CO₂, CO, and H₂S** in multi-instrument retrievals; metallicity 11–15× solar. **Information-content study** quantifies what each JWST mode contributes via Bayesian log-evidence (Δln Z): NIRISS dominates non-gray cloud evidence (>7.5σ only when included); NIRSpec dominates CO₂ and H₂S detections; CO requires NIRSpec + MIRI. C/O is sensitive to the NIRSpec reduction choice (CASCADe vs. TEATRO).

## Key findings

- **Detections (>3σ in multi-instrument retrievals):**
  - [[H2O]] — >12σ in any combination including NIRISS; ~3.1σ from NIRSpec alone.
  - [[CO2]] — >10σ via the 4.3 μm ν₃ band, requires NIRSpec.
  - [[CO]] — ~8σ from NIRSpec + MIRI; cannot be disentangled from H₂O/CO₂ by NIRSpec alone.
  - [[H2S]] — ~3.7σ via the 3.8 μm ν₁ band (TEATRO reduction); requires NIRSpec; degeneracy with gray cloud broken by adding NIRISS+MIRI.
- **Non-detections:** [[CH4]], SO₂, NH₃, HCN — only upper limits.
- **Metallicity:** 11–15× solar in multi-instrument retrievals; single-instrument retrievals systematically overestimate molecular abundances.
- **C/O:** sensitive to NIRSpec reduction choice (CASCADe vs. TEATRO); not robustly constrained.
- **Cloud:** non-gray cloud preferred at >7.5σ only when NIRISS is included; sub-Rayleigh slope (p < 4) consistently retrieved; cloud-top pressure < 10⁻³·⁶ bar.
- **T–P profile:** no preference for non-isothermal (contrast with WASP-39 b).

## Methods

- **Observations:** New JWST/NIRISS SOSS transit on 2023-06-20 (~6.2 h); companion NIRSpec G395M and MIRI LRS observations from the same GTO 1281 program. Archival HST/STIS G430L+G750L and HST/WFC3 G141.
- **Reductions:** [[exoTEDRF]] (NIRISS), [[CASCADe]] (NIRSpec/MIRI/STIS standard), [[TEATRO]] (alternate NIRSpec reduction).
- **Light curves:** [[juliet]], `dynesty`, `ExoTiC-LD` + Stagger grid limb-darkening, `spotrod` for spot-crossing.
- **Retrievals:** [[ARCiS]] (Min et al. 2020) with [[MultiNest]] over all combinations of instruments. Δln Z used to attribute detection significance to instrument combinations.
- **Forward model:** 5-point T–P, 100 layers, 10 bar reference, free chemistry (vertically-constant VMRs); ExoMol/HITRAN k-tables.

## Caveats & limitations

- **Δln Z significances** should be treated cautiously per Kipping & Benneke 2025 / Welbanks et al. 2025 (both not yet ingested).
- **Free chemistry, isobaric VMR** assumption — no equilibrium / disequilibrium chemistry constraints applied.
- **Possible spot-crossing event** in the NIRISS light curve at ~25 min post-mid-transit; limb asymmetry not modeled.
- **C/O sensitive to NIRSpec reduction choice** (CASCADe vs TEATRO).
- **MIRI MRS excluded;** MIRI LRS analysis deferred to a companion paper (Bouwman et al., in prep; not yet ingested).
- **HST reductions adopted from literature** (Sing 2016, Alexoudi 2018; not yet ingested) — no reanalysis.

## Open questions / follow-ups

- Resolve C/O via reduction-method consensus or higher-resolution observations.
- Test the H₂S detection with a dedicated PRISM or G395H follow-up.
- Why does HAT-P-12 b not require a non-isothermal T–P profile while WASP-39 b does?

## Related

- [[2025_Gressier_WASP17b]] — analogous panchromatic single-instrument JWST emission analysis (NIRISS SOSS) on a different hot Jupiter; contrasts retrieval approaches.
- [[2026_Radica_WASP96b]] — multi-instrument JWST + ground hot Jupiter retrieval; comparable sulfur-species (SO₂ tentative) story.
- WASP-39 b ERS papers (not yet ingested) — comparison benchmark for sub-Saturn vs. hot-Jupiter chemistry.
- [[2026_RoyPerez_WASP39b]] — methodologically related: pipeline-driven variation in retrieved abundances (here CASCADe vs. TEATRO; there four NIRSpec PRISM pipelines).
