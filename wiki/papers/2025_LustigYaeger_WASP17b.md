---
type: paper
bibkey: 2025_LustigYaeger_WASP17b
authors: [Lustig-Yaeger, J., Sotzen, K. S., Stevenson, K. B., Tsai, S.-M., Challener, R. C., Goyal, J., Lewis, N. K., Louie, D. R., et al.]
year: 2025
venue: arXiv:2510.06169
arxiv: 2510.06169
targets: [WASP-17b]
instruments: [JWST-NIRSpec]
methods: [secondary-eclipse-spectroscopy, atmospheric-retrievals, planetary-infrared-excess]
species_detected: []
species_tentative: [SO2, CH4, CO2, H2O]
codes: [Eureka, POSEIDON, MultiNest, VULCAN]
tags: [hot-jupiter, dreams, nightside, phase-asymmetry, photochemistry, jwst-tst]
ingested: 2026-04-29
---

# JWST-TST DREAMS: The Nightside Emission and Chemistry of WASP-17 b

**Authors:** Lustig-Yaeger, Sotzen, Stevenson, Tsai, Challener, Goyal, Lewis, Louie, et al. (2025, arXiv:2510.06169) · CHAMPs / DREAMS consortium
**Target:** [[WASP-17b]] · **Host:** [[WASP-17]] (F6 dwarf, Teff = 6550 K) · **Instrument:** [[JWST-NIRSpec]] (G395H, 2.9–5.2 μm)
**Program:** [[JWST-TST-GTO-1353]]

## TL;DR

Applies the **Planetary Infrared Excess (PIE)** technique — specifically the **in-Eclipse Spectrum Removal (iESR)** variant introduced here — to a back-to-back JWST/NIRSpec G395H **transit + secondary eclipse** of [[WASP-17b]] taken 1.8 days (0.5 phase) apart, extracting the first JWST nightside emission spectrum of WASP-17 b. Uses the in-eclipse stellar spectrum as an empirical stellar template, sidestepping the ~1.3% PHOENIX-model imprecision floor that otherwise dominates the nightside signal. Retrieves a nightside Teq = 1005 ± 256 K and Bond albedo A_B = 0.42 +0.06/−0.10 (non-zero, inefficient redistribution). Tentative SO₂ at 2.3σ on the nightside requires day-to-night transport from a ~10× solar metallicity dayside atmosphere. Validates iESR for transiting planets observed within a stellar rotation period.

## Key findings

- **First JWST nightside emission spectrum of WASP-17 b.** Broadband nightside Tb ≈ 1050 K (NIRSpec NRS1 + NRS2 weighted means); retrieved nightside Teq = 1005 ± 256 K.
- **Inefficient heat redistribution.** Energy-balance fit gives recirculation factor f = 0.54 (close to dayside-only redistribution); Bond albedo A_B = 0.42 +0.06/−0.10.
- **Tentative nightside species detections** (with required noise-floor inflation of 224 ± 18 ppm):
  - [[SO2]] at 2.3σ (lnB = 1.45)
  - [[CH4]] at 1.5σ
  - [[CO2]] at 0.9σ
  - [[H2O]] at 1.5σ
  - Combined feature significance 3.0σ.
  - Without error inflation: SO₂ rises to 7.6σ and CH₄ to 8.8σ — but the inflated values are the conservative reported result.
- **Nightside SO₂ implies horizontal transport.** SO₂ lifetime > 10 days, so the nightside abundance is set by photochemistry on the dayside being advected by zonal winds; consistent with a 2D VULCAN photochemistry model adapted from Tsai 2024 at ~10× solar metallicity. Inconsistent with zero-wind chemistry.
- **CH₄ day–night gradient** traces zonal winds under weak vertical mixing.
- **CO₂ puzzle.** Nightside CO₂ retrieved at lower abundance than dayside — opposite to most transport-induced expectations; not understood.
- **iESR validation.** iESR-PIE recovers reasonable retrievals for WASP-17 b even though parallel attempts on NIRISS/SOSS (zeroth-order contamination) and MIRI/LRS (long temporal ramps) failed, defining a method-applicability boundary.

## Methods

- **Observations:** JWST NIRSpec G395H NRS1+NRS2, SUB2048, NRSRAPID, 66 groups; transit + eclipse 1.8 d apart (0.5 orbital phase).
- **Reduction:** [[Eureka]] (Stages 1–6, pmap-locked, identical settings for transit and eclipse).
- **iESR construction:** average pre/post-eclipse and pre/post-transit out-of-event spectra, then form F_day/F_⋆ and F_night/F_⋆ via simple ratios using the in-eclipse spectrum as the stellar template (Eqs. 1–4 of the paper). Two dayside (pre/post-eclipse) and two nightside (pre/post-transit) spectra extracted.
- **Outlier rejection:** low-resolution σ-clipping in 0.02 μm bins (3% rejected dayside, 4.5% nightside).
- **Retrievals:** [[POSEIDON]] v1.2 with [[MultiNest]] sampler; Mullens 2024 pressure contribution functions (not yet ingested). Free chemistry over H₂O, CH₄, CO, CO₂, SO₂; M&S09 T–P parameterization. Adopted Wakeford 2025 (not yet ingested) panchromatic high-γ constraint to resolve a dayside two-mode posterior.
- **Photochemistry:** [[VULCAN]] 2D framework (Tsai 2024 adaptation; not yet ingested), simplified to two columns (dayside / nightside) with zonal-wind-driven horizontal advection.
- **Stellar models:** PHOENIX adopted only for cross-comparison (not as the iESR baseline).

## Caveats & limitations

- **Tentative detections.** SO₂, CH₄, H₂O, CO₂ all at 1.5–2.3σ with required 224 ppm noise-floor inflation. Without inflation the significances rise dramatically (8.8σ CH₄, 7.6σ SO₂) but the inflated treatment is the reported result.
- **iESR fails on NIRISS/SOSS** (zeroth-order contamination, position-angle changes between transit and eclipse) and on **MIRI/LRS** (long temporal ramps); the method requires temporal stability between the two observations.
- **Method limited by stellar rotation.** Transit and eclipse must be separated by less than the stellar rotation period (here 1.8 d ≪ 8 d). Active stars degrade iESR — flagged via a null-result HAT-P-26 b companion paper (Sotzen 2025; not yet ingested).
- **CO₂ nightside underabundance** unexplained.
- **No species firmly detected** — all reported detections are tentative.

## Open questions / follow-ups

- Does the nightside SO₂ signature persist with more transit + eclipse pairs, or with longer-baseline phase curves?
- What sets the inverse CO₂ day–night gradient? Cloud condensation, photochemistry, or systematics?
- Is the iESR PIE method generalizable to JWST/NIRCam and to lower-host-star activity targets?

## Related

- [[2025_Gressier_WASP17b]] — companion DREAMS paper on the **dayside** of WASP-17 b from NIRISS/SOSS eclipse; provides the supersolar metallicity context this paper uses for photochemistry boundary conditions.
- Wakeford et al. 2025 (panchromatic NIRISS+NIRSpec+MIRI dayside retrieval; not yet ingested) and Lewis et al. 2025 (transit/eclipse light-curve analyses; not yet ingested) round out the DREAMS WASP-17 b suite.
- Earlier WASP-17 b: Grant et al. 2023 MIRI/LRS SiO₂ cloud feature (not yet ingested), Valentine et al. 2024 eclipse map with hotspot offset 18.7° E (not yet ingested), Louie et al. 2024 NIRISS transmission (not yet ingested).
