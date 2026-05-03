---
type: paper
bibkey: 2025_Crouzet_HATP12b
authors: [Crouzet, N., Edwards, B., Konings, T., Bouwman, J., Min, M., Lagage, P.-O., Waters, L. B. F. M., Pye, J. P., et al.]
year: 2025
venue: A&A 703:A264
doi: 10.1051/0004-6361/202450690
targets: [HAT-P-12b]
instruments: [JWST-NIRSpec, HST-WFC3]
methods: [transmission-spectroscopy, atmospheric-retrievals]
species_detected: [CO2, H2O, CO]
species_tentative: [H2S]
species_ruled_out: [CH4, SO2, NH3, PH3]
codes: [TEATRO, CASCADe, ARCiS, TauREX3, VULCAN, petitRADTRANS, MultiNest]
tags: [warm-sub-saturn, k-dwarf-host, photochemistry, exomiri, jwst-gto-1281]
ingested: 2026-05-03
---

# Detection of CO₂, CO, and H₂O in the atmosphere of the warm sub-Saturn HAT-P-12 b

**Authors:** Crouzet, Edwards, Konings, Bouwman, Min, Lagage, Waters, Pye, et al. (2025, A&A 703:A264) · DOI: 10.1051/0004-6361/202450690
**Target:** [[HAT-P-12b]] · **Host:** [[HAT-P-12]] · **Instruments:** [[JWST-NIRSpec]] (G395M) + [[HST-WFC3]] (G141 archival)
**Program:** [[JWST-GTO-1281]] (ExoMIRI consortium)

## TL;DR

The foundational JWST/NIRSpec G395M (R≈1000, 2.87–5.10 μm) transmission paper for the warm sub-Saturn [[HAT-P-12b]], combined with two archival HST/WFC3 G141 transits. Detects [[CO2]] at 12.2σ, [[H2O]] at 6.0σ, and [[CO]] at 4.1σ. Inferred metallicity is **~10× solar (Saturn-like) when photochemical CO₂ pathways are included** in the forward model, but ~60× solar without photochemistry — the strongest illustration in the wiki to date that retrieved metallicity on a sub-Saturn depends critically on chemistry assumptions. CH₄ is conspicuously **not** detected. The companion panchromatic information-content study [[2026_Heinke_HATP12b]] builds directly on this paper's NIRSpec G395M data.

## Key findings

- **CO₂** detected at 12.2σ (ARCiS, HST + NIRSpec TEATRO reduction); 12.0σ via TauREX3.
- **H₂O** detected at 6.0σ; 5.9σ via TauREX3.
- **CO** detected at 4.1σ; 3.7σ via TauREX3.
- **H₂S** marginally detected at 3.2σ in the CASCADe reduction only; absent in TEATRO — pipeline-dependent (in line with the [[2026_Heinke_HATP12b]] companion paper's finding that CASCADe vs TEATRO shifts H₂S significance).
- **Non-detections:** [[CH4]], SO₂, NH₃, PH₃.
- **Metallicity 10× solar (Saturn-like)** when ARCiS photochemistry is included; **~60× solar** without photochemistry — a clean demonstration of the metallicity-vs-photochemistry degeneracy.
- **C/O < 1**, poorly constrained (TEATRO 0.5–0.75; CASCADe ~0.25). Atmosphere likely super-stellar in C and O.
- **Atmospheric T at the terminator** = 490 +75/−60 K in P ~ 4 × 10⁻⁸ to 4 × 10⁻³ bar — cold upper atmosphere.
- **Clouds preferred at 4.6σ** (TEATRO; CP 2–11 mbar); only 2.3σ (CASCADe; CP 5–269 mbar). Likely Na₂S / ZnS / NaCl per condensation curves.
- **CH₄ depletion is unexplained;** high T_int (800 K from optimization) with strong vertical mixing fits the data but exceeds tidal+delayed cooling predictions (~380–580 K).

## Methods

- **Observations:** Single JWST NIRSpec BOTS G395M + F290LP transit on 2023 Feb 11–12 (~6.34 h). NRS1 detector only (G395M is single-detector). 30 groups/integration, 816 integrations. Plus archival HST WFC3 G141 (1.1–1.7 μm) transits from HST GO 14260 (2015 Dec, 2016 Aug; not yet ingested).
- **Reductions:** [[TEATRO]] (Crouzet, jwst pipeline 1.10.2) and [[CASCADe]] (Bouwman, jwst pipeline 1.13.4) in parallel; binned into 117 channels (0.02 μm).
- **Light-curve fits:** the `exoplanet` PyMC3 package (TEATRO) and CASCADe's common-mode systematics model. Limb darkening from ExoTETHyS + STAGGER 2018.
- **Retrievals:** [[ARCiS]] (Min et al. 2020) primary with [[MultiNest]] (2500 live points), correlated-k tables from ExoMol; cross-checked with [[TauREX3]] v3.1 using ExoMol cross-sections. Both retrievals: isothermal P–T, gray cloud (single CP parameter), uniform VMRs over H₂O / CH₄ / CO / CO₂ / H₂S / SO₂.
- **Photochemistry:** ARCiS chemical relaxation + radiative-convective equilibrium for P–T; [[VULCAN]] (Tsai et al. 2017) photochemical kinetics with the SNCHO_PHOTO_NETWORK and a MUSCLES SED for HAT-P-12; synthetic spectra via [[petitRADTRANS]].
- **HST–NIRSpec offset** fit between datasets.

## Caveats & limitations

- **HST and NIRSpec band-averaged depths differ by ~4σ;** offset fitted but underlying cause not resolved.
- **CASCADe vs TEATRO disagreement on H₂S** (3.2σ vs absent) — pipeline-driven retrieval variation in the small-amplitude regime.
- **1D retrievals** known to underestimate terminator T vs. GCMs; might bias the SO₂ non-detection conclusion.
- **VULCAN forward-model parameters** not optimized per run; comparison illustrative.
- **Cloud rainout** may bias the inferred elemental abundances.
- **C/O has order-of-magnitude VMR uncertainties** → weak constraint.
- **T_int = 800 K** from optimization hits the upper bound; not a robust value.

## Open questions / follow-ups

- Why is CH₄ depleted? T_int + vertical mixing or photochemical loss?
- Resolve C/O via reduction-method consensus or higher-resolution observations.
- Pin down the bulk of the cloud composition (Na₂S / ZnS / NaCl candidates).

## Tensions

- **Metallicity 10× vs 60× solar** depending on whether photochemistry is included — a methodological tension the paper explicitly highlights.

## Related

- [[2026_Heinke_HATP12b]] — the panchromatic information-content companion paper that combines this NIRSpec G395M data with the same program's NIRISS/SOSS and MIRI/LRS observations plus HST archival data; same [[JWST-GTO-1281]] ExoMIRI program.
- [[2026_Radica_WASP96b]] — methodological cousin: tentative SO₂ on the photochemical shoreline; multi-pipeline retrieval cross-comparison.
- [[2026_RoyPerez_WASP39b]] — pipeline-driven retrieval variation theme; here the analogue is CASCADe vs TEATRO H₂S divergence.
