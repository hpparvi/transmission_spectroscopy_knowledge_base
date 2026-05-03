---
type: paper
bibkey: 2000_Seager_TheoryTransmission
authors: [Seager, S., Sasselov, D. D.]
year: 2000
venue: ApJ 537:916
doi: 10.1086/309088
targets: [HD-209458b]
instruments: []
methods: [transmission-spectroscopy]
species_predicted: [Na, K, He]
tags: [hot-jupiter, theory, foundational, pre-detection, pre-jwst]
ingested: 2026-04-29
---

# Theoretical Transmission Spectra during Extrasolar Giant Planet Transits

**Authors:** Seager, S., Sasselov, D. D. (2000, ApJ 537:916) · DOI: 10.1086/309088
**Target:** [[HD-209458b]] (archetype) · **Instrument:** *theoretical (none)*

## TL;DR

The foundational theoretical paper introducing **[[transmission-spectroscopy]]** as an observational technique for close-in extrasolar giant planets (CEGPs). Predicts that high-resolution, high-S/N spectroscopy during a transit can detect absorption features at the ~10⁻⁴ to ~10⁻³ level relative to total stellar flux, with the **[[Na]] I D resonance doublet at 589.4 nm** as the strongest predicted feature. Establishes the geometric framework — stellar flux passing through an optically thin "transparent atmosphere" above the limb cloud-top — that every subsequent transmission paper inherits. Computes detailed spectra for [[HD-209458b]] specifically. The Na D prediction motivated the historic first detection of an exoplanet atmosphere by Charbonneau, Brown, Latham & Mayor 2002 (HST/STIS; not yet ingested).

## Key findings (predictions)

- Transparent-atmosphere/star area ratio ~3.6 × 10⁻⁴ for HD 209458 b; line-core depth ~10⁻³ relative to total stellar flux.
- **[[Na]] I D resonance doublet at 589.4 nm** — strongest predicted feature; line cores reach ~−1.65% to −1.70% transit depth (vs. ~−1.47% continuum).
- **[[K]] I resonance doublet at 767.0 nm** — narrower than Na I (lower abundance).
- **[[He]] I 2³S–2³P triplet at 1083.0 nm** — populated via stellar EUV photoionization and recombination cascade trapped in the metastable triplet state; potentially extreme amplitude if the exosphere is extended.
- **[[H2O]] and [[CH4]]** bands in the IR are obscured by the planet's own thermal emission redward of ~2000 nm.
- **Rayleigh scattering by H₂** important below 200 nm.
- **Cloud-top depth** identified as the key observable that distinguishes between atmospheric scenarios.

## Methods

- 1D self-consistent irradiated atmosphere code (Seager 1999; Seager, Whitney & Sasselov 2000; not yet ingested), with Gibbs free-energy minimization for chemical equilibrium and condensate opacities.
- Plane-parallel line-of-sight column geometry through the limb; sum over columns from cloud-top tangential down to skimming rays (densest column dominates).
- Opacities: H₂O, TiO, CH₄, H₂–H₂ and H₂–He CIA, Rayleigh from H/He/H₂, alkali resonance lines (Voigt with H₂/He pressure + Doppler broadening); oscillator strengths from Radzig & Smirnov 1985 and the Kurucz line list.
- Non-LTE He model atom (singlets + triplets to n=4) for the 1083 nm line.
- Refraction shown to be small (Δs/s < 2%).
- Cloud particles: 10 μm grains of MgSiO₃, Fe, Al₂O₃ (MgSiO₃ deck highest).
- Assumed planet parameters for [[HD-209458b]]: R_p = 1.54 R_J, M_p = 0.69 M_J, i = 85.2°, a = 0.0468 AU, T_eff ≈ 1350 K.

## Caveats & limitations

- Cloud particle type / size is the most uncertain free parameter; cloud-base location dominates predictions.
- Photochemistry not included.
- T–P assumed uniform around the planet (efficient wind redistribution).
- Exact line shape unpredictable due to unknown metallicity, non-equilibrium chemistry, cloud heights.
- *Note added in proof* explicitly downgrades the work to "conceptual description" given updated R_P, R_⋆ from Mazeh et al. 2000 (not yet ingested).
- Detection requires high-resolution, high-S/N spectroscopy and spectral-separation techniques at the ~10⁻⁴ level.

## Open questions / follow-ups (as of 2000)

- Will the Na D feature actually be detectable? *(Answered yes by Charbonneau et al. 2002.)*
- Will the He I 1083 nm metastable triplet be detectable? *(Answered yes much later by Spake et al. 2018, Nortmann et al. 2018; both not yet ingested.)*

## Related

- [[2001_Brown_TransmissionDiagnostics]] — companion foundational theory paper (Brown 2001) extending this work with a formal "spectrum ratio" framework, Doppler diagnostics from winds and rotation, photoionization of Na/K, and broader diagnostic mapping.
- Charbonneau, Brown, Latham & Mayor 2002 (HST/STIS Na I detection on HD 209458 b; not yet ingested) — the first ever exoplanet atmosphere detection, motivated directly by this paper's Na D prediction.
- [[2026_Radica_WASP96b]], [[2026_RoyPerez_WASP39b]] — JWST-era confirmations of [[Na]] absorption in hot-Jupiter atmospheres, vindicating the Na-D prediction across multiple targets.
- All wiki transmission-spectroscopy papers inherit the geometric framework introduced here.
