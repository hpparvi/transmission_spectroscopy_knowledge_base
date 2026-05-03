---
type: paper
bibkey: 2001_Brown_TransmissionDiagnostics
authors: [Brown, T. M.]
year: 2001
venue: ApJ 553:1006
doi: 10.1086/320950
targets: [HD-209458b]
instruments: []
methods: [transmission-spectroscopy]
species_predicted: [Na, K, H2O, CO, CH4]
tags: [hot-jupiter, theory, foundational, pre-detection, pre-jwst, spectrum-ratio]
ingested: 2026-04-29
---

# Transmission Spectra as Diagnostics of Extrasolar Giant Planet Atmospheres

**Authors:** Brown, T. M. (single author; 2001, ApJ 553:1006) · DOI: 10.1086/320950
**Target:** [[HD-209458b]] (archetype) · **Instrument:** *theoretical (none)*

## TL;DR

The second foundational [[transmission-spectroscopy]] theory paper, building substantially on [[2000_Seager_TheoryTransmission]]. Introduces the formal **"spectrum ratio"** R(λ) = F_transit/F_out as the natural observable, and adds new physics: cloud-top-pressure parameter studies, Doppler diagnostics from height-dependent winds and planetary rotation, [[Na]] / [[K]] photoionization by stellar UV, refraction, and a Sudarsky-style parameterized cloud deck. Maps how cloud height, metallicity, T(P) profile, thermal inversions, winds, and rotation each imprint themselves on R(λ), defining the diagnostic catalog the field still uses. Predictions computed for [[HD-209458b]] with feature depths at the ~10⁻³ level relative to stellar continuum.

## Key findings (predictions)

For the fiducial model (T₀ = 1400 K at 1 bar, R_p = 1.55 R_J, MgSiO₃ cloud deck at 0.03 bar):

- **Continuum transit depth** ≈ 1.53%.
- **[[Na]] D and [[K]] resonance lines:** line cores ~0.2% absorption; apparent radius ~6% larger than continuum; line depths ~10⁻³ relative to stellar continuum.
- **[[H2O]] bands** (0.7–2.5 μm): 0.08–0.17% below continuum at the 1.4 μm band (R = 3000 to 150,000).
- **[[CO]] first overtone at 2.3 μm:** prominent; "most promising" molecular diagnostic with modest H₂O contamination.
- **[[CH4]]:** visible longward of 2.2 μm in the fiducial model; strongly temperature-sensitive.
- **H₂ CIA** dominates the continuum redward of 1.6 μm when clouds lie deep.
- **Cloud-top pressure** is *the* dominant determinant of feature depth (cloud deck mutes everything below it).
- **Diagnostic feature depths at the 10⁻³ level** are achievable with sufficient S/N.

## Methods

- **Opacity:** HITRAN 1996 line-by-line for H₂O (~19,400 lines), CO (~400), CH₄ (~6,200) over 0.25–2.5 μm; Karkoschka 1994 low-res for CH₄ < 1 μm; Kurucz & Bell 1995 for Na/K with Lorentzian profiles and Burrows et al. Weisskopf collisional broadening; Rayleigh on H₂; H₂ CIA via Linsky 1969; cloud particle scattering (Mie-smoothed monotonic).
- **Chemistry:** thermodynamic equilibrium via Burrows & Sharp 1999 for H, C, N, O system (H₂, H₂O, CO, CH₄, N₂, NH₃); solar abundances (Anders & Grevesse 1989).
- **T–P profile:** prescribed (not self-consistent); adapted from Sudarsky et al. 2000 irradiated Type IV "roaster" model raised by 200 K to give T₀ = 1400 K at 1 bar.
- **Clouds:** single MgSiO₃ (enstatite) deck, Sudarsky-style size distribution peaked at 3 μm, top at 0.03 bar (fiducial); cloud-top pressure varied across 1, 0.1, 0.01, 0.001 bar.
- **Geometry:** spherical hydrostatic, tangential rays, refraction included (Seager & Sasselov 2000 formalism); annular bimodal rotational broadening profile at v_eq = 2 km/s; height-dependent wind shear.
- **Photoionization:** plane-parallel UV transfer for Na/K in two bands (<241.2 nm; 241.2–285.6 nm).

## Innovations vs. Seager & Sasselov 2000

1. The formal "spectrum ratio" R(λ) framework as the natural observable.
2. Explicit cloud-top pressure parameter studies showing clouds are *the* dominant determinant of feature depth.
3. Doppler diagnostics from height-dependent winds and planetary rotation (annular bimodal profile).
4. Na/K photoionization by stellar UV affecting line-core depth.
5. Thermal-inversion ("stratosphere") sensitivity via scale-height changes.
6. High-resolution cross-correlation as a detection technique.
7. Feasibility budgets for HIRES / NIRSPEC / NGST (the latter became JWST).

## Caveats & limitations

- T(P) prescribed, not self-consistent.
- Equilibrium chemistry only (no photochemistry; Brown's Na/K photoionization is a separate add-on).
- Ionization treatment crude (radiative recombination only, no charge exchange).
- Clouds parameterized.
- Helium opacity excluded.
- Lorentzian wings inaccurate.
- Latitudinal/zonal variation not modeled.
- Required S/N (10³–10⁵) and R (10³–10⁶) beyond reach in 2001.

## Related

- [[2000_Seager_TheoryTransmission]] — earlier foundational theory paper (Seager & Sasselov 2000); predicted Na D as the strongest feature; this paper extends with cloud-physics, dynamics, and photoionization.
- Charbonneau, Brown, Latham & Mayor 2002 (HST/STIS Na I detection on HD 209458 b; not yet ingested) — first ever exoplanet atmosphere detection, vindicating both papers; T. M. Brown is co-author.
- [[2026_Radica_WASP96b]], [[2026_RoyPerez_WASP39b]] — modern hot-Jupiter retrievals confirming the predicted [[Na]] / [[K]] / [[H2O]] / [[CO]] features.
- The "spectrum ratio" R(λ) terminology and the cloud / metallicity / T(P) / wind diagnostic catalog defined here are still the standard language of the field.
