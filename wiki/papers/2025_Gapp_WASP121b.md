---
type: paper
bibkey: 2025_Gapp_WASP121b
authors: [Gapp, C., Evans-Soma, T. M., Barstow, J. K., Lothringer, J. D., Sing, D. K., Ruseva, D., Ahrer, E.-M., Goyal, J. M., Christie, D., Kreidberg, L., Mayne, N. J.]
year: 2025
venue: arXiv (submitted)
arxiv: 2506.02199
targets: [WASP-121b]
instruments: [JWST-NIRSpec]
methods: [transmission-spectroscopy, atmospheric-retrievals]
species_detected: [SiO, H2O]
tags: [ultra-hot-jupiter, thermal-dissociation, refractory-tracer, hemispheric-heterogeneity, formation-tracer, jwst-go-1729]
codes: [FIREFLy, NEMESISPY, ATMO, MultiNest, Catwoman]
ingested: 2026-05-06
---

# WASP-121 b's Transmission Spectrum Observed with JWST/NIRSpec G395H Reveals Thermal Dissociation and SiO in the Atmosphere

**Authors:** Gapp, Evans-Soma, Barstow, Lothringer, Sing, Ruseva et al. (2025) · arXiv:2506.02199
**Target:** [[WASP-121b]] · **Host:** [[WASP-121]] · **Instrument:** [[JWST-NIRSpec]] (G395H, 2.54–5.15 μm)
**Program:** [[JWST-GO-1729]]

## TL;DR

JWST NIRSpec/G395H transmission spectrum of the benchmark ultra-hot Jupiter [[WASP-121b]] (T_eq ≈ 2350 K) extracted from the full phase-curve observation (analyzing only the transit window). Finds evidence for **[[thermal-dissociation]] of H₂O and H₂ on the dayside** and detects [[SiO]] at **5.2σ** — the first identification of the long-suspected NUV absorber via direct spectral signature. Implements a custom dayside/nightside split atmospheric model in the [[NEMESISPY]] framework to handle hemispheric chemistry differences; the split-model retrieval favors **higher H₂O on the nightside than dayside**, demonstrating that 1D retrievals of ultra-hot Jupiters bias the C/O ratio. Constraining SiO and refractory-to-volatile abundance ratios opens a path to inferring rocky-material accretion history during the planet's migration.

## Key findings

- **SiO detected at 5.2σ** in NRS1 (2.54–3.72 μm), compatible with chemical equilibrium on the dayside; **first definitive identification** of the NUV absorber inferred since Evans et al. 2018 (HST/STIS) — supports the Lothringer et al. 2022 silicate-cloud-condensation hypothesis distinguishing T_eq > 2100 K from cooler hot Jupiters.
- **H₂O detected** but with depleted dayside abundance — the spectrum shows evidence for **[[thermal-dissociation]] of H₂O** on the permanent dayside and recombination on the nightside (consistent with Mikal-Evans 2022 phase-curve and Wardenier 2024 IGRINS Doppler-shift findings).
- **H₂ thermal dissociation** on the dayside contributes to dayside scale-height inflation and biased absorption-feature amplitudes (CO enhanced; H₂O depleted) when ignored.
- **Custom dayside/nightside [[NEMESISPY]] retrieval** prefers higher H₂O on the nightside than the dayside — agrees with phase-curve and high-resolution Doppler evidence.
- **One-dimensional spherical-symmetry retrievals biased high in C/O**: the negative correlation between H₂ dissociation and CO abundance produces degeneracies that prevent robust 1D constraints.
- **Refractory-to-volatile ratio (Si/O) observability**: simultaneous SiO + H₂O + CO constraints would in principle yield rocky-material accretion fraction during planet migration; this paper sets the methodological foundation but cannot yet quantify the ratio due to the 3D bias.
- The G395H spectrum is extracted from the **transit window of a phase-curve observation** (37.8 hr long); this reduces nightside-emission contamination of the inferred transmission spectrum vs. a transit-only program.

## Methods

- **Phase-curve transit extraction**: 7 hr around mid-transit (3.5 hr pre/post baseline) from JWST GO-1729 phase-curve observation (Mikal-Evans 2023; Evans-Soma 2025 phase-curve analysis not ingested).
- **Reduction**: [[FIREFLy]] (Rustamkulov 2022, 2023) — group-level systematics handling.
- **Light-curve fits**: `batman` transit + quadratic polynomial baseline + per-detector white light curve joint fit; `emcee` posterior; `ExoTIC-LD` Stagger 3D limb darkening priors. Sigma clipping at 5σ; spectroscopic binning at R ∼ 600 and R ∼ 3000.
- **Retrievals**:
  - [[NEMESISPY]] **custom dayside/nightside split atmospheric model** (new in this paper) — separate P–T profile, abundances, and contributions for each hemisphere; weighted sum produces the observed transmission spectrum.
  - [[NEMESISPY]] standard 1D retrieval as comparison.
  - [[ATMO]] cross-check.
  - PETRA cross-check (Lothringer & Barman 2020; not yet a wiki code page).
- **Sampling**: [[MultiNest]] / `dynesty`.
- **Limb-resolved transit** test using [[Catwoman]] mentioned for completeness.

## Caveats & limitations

- **3D geometry not fully captured**: even the dayside/nightside split is a coarse approximation of the actual 3D temperature and chemistry structure (Caldas et al. 2019; Pluriel et al. 2020 simulations). True abundance constraints require GCM-coupled retrievals.
- **Bulk H₂O and C/O cannot be uniquely constrained** from this spectrum alone — the negative correlation between H₂ dissociation and CO biases 1D retrievals.
- **NUV identification still indirect** — the SiO detection is via the 4.0–4.5 μm features in NRS1; longer-wavelength MIRI or NUV STIS data would tighten the identification but are not in this work.
- **Mg I and Fe II contributions** to the NUV rise (Lothringer 2022 alternative) are not ruled out by this G395H detection alone.

## Open questions / follow-ups

- **Refractory-to-volatile constraints**: combining NIRSpec (SiO, CO, H₂O) with NUV (Mg, Fe) and MIRI mid-IR data — would discriminate between possible migration histories.
- **3D-aware retrievals**: GCM-emulator or hierarchical 3D retrievals are needed to break the dayside-dissociation–CO-abundance degeneracy.
- **Confirm SiO via additional bands** (e.g., 8 μm SiO band on MIRI/LRS) and via [[Catwoman]] limb-asymmetry analysis.
- **Other refractories**: are TiO, VO, Mg, Fe also identifiable in NIRSpec G395H once the dayside-dissociation framework is applied?

## Related

- Evans-Soma et al. 2025 (full phase-curve analysis of the same dataset; not yet ingested) — emission-spectrum complement.
- Mikal-Evans et al. 2022, 2023 (HST + JWST/NIRSpec phase curves; not yet ingested) — established H₂O dayside depletion.
- Wardenier et al. 2023, 2024 (Gemini-S/IGRINS high-resolution Doppler; not yet ingested) — independent confirmation of dayside H₂O depletion.
- [[2025_LustigYaeger_WASP17b]] — limb/nightside emission methodology comparison case for hemispheric heterogeneity.
- [[2025_Ahrer_WASP94Ab]] — refractory-volatile formation-history motivation extended to lower-T_eq hot Jupiter without thermal dissociation.
