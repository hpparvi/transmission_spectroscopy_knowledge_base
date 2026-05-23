---
type: paper
bibkey: 2025_Ahrer_KELT7b
authors: [Ahrer, E.-M., Fairman, C., Kirk, J., Wakeford, H. R., Barstow, J. K., Penzlin, A. B. T., Alderson, L., Booth, R. A., Christie, D. A., Claringbold, A. B., Esparza-Borges, E., Gascón, C., López-Morales, M., Meech, A., McCormack, M., Mollière, P., Owen, J. E., Sergeev, D. E., Valentine, D., Panwar, V., Wheatley, P. J., Zamyatina, M.]
year: 2025
venue: MNRAS
arxiv: 2509.10000
doi: 10.1093/mnras/staf1535
targets: [KELT-7b]
instruments: [JWST-NIRSpec]
methods: [transmission-spectroscopy, atmospheric-retrievals]
species_detected: []
species_tentative: [H2O, CO2]
species_ruled_out: [CO, H2S, HCN, CH4, NH3, SiO, VO, TiO, AlO, SH]
codes: [Eureka, ExoTiC-JEDI, Tiberius, petitRADTRANS, POSEIDON, NEMESISPY, MultiNest, easyCHEM]
tags: [hot-jupiter, aligned-orbit, f-star-host, bowie-align, weak-features, cloud-deck, low-metallicity-candidate]
ingested: 2026-05-03
---

# BOWIE-ALIGN: weak spectral features in KELT-7 b's JWST NIRSpec/G395H transmission spectrum imply a high cloud deck or a low-metallicity atmosphere

**Authors:** Ahrer, Fairman, Kirk, Wakeford, Barstow et al. (2025, MNRAS 543:2442–2462)
**Targets:** [[KELT-7b]] · **Instrument:** [[JWST-NIRSpec]] G395H · **Program:** [[JWST-GO-3838]] (BOWIE-ALIGN; PIs: Kirk & Ahrer)

## TL;DR

A single JWST NIRSpec G395H transit of the aligned hot Jupiter KELT-7 b (M = 1.39 M_J, R = 1.60 R_J, T_eq = 2048 K, F2-star host) shows only **weak, tentative features**: H₂O at log VMR ≈ −7 with ln Z = 1.0–1.9 (POSEIDON) and CO₂ similarly tentative; CO not detected. Three independent reductions ([[Eureka]], [[ExoTiC-JEDI]], [[Tiberius]]) and two retrieval frameworks ([[POSEIDON]], [[petitRADTRANS]]) leave two viable scenarios: (1) **high-altitude cloud deck** at log P ≈ 0.5 bar masking features under near-equilibrium chemistry with C/O ≈ 0.43–0.74 and metallicity 1–16× solar; or (2) an **extremely low-metallicity** free-chemistry atmosphere where the lack of features reflects intrinsically low absorber abundance. Equilibrium chemistry is statistically slightly preferred (Δ ln Z = 1.6–3.1). The wide constraints prevent definitive formation-history conclusions for this aligned hot Jupiter, but solar-to-supersolar metallicity would imply solid-material accretion. Third planet in the BOWIE-ALIGN survey ([[2025_Ahrer_KELT7b]]) following WASP-15 b (misaligned; Kirk et al. 2025, not yet ingested) and TrES-4 b (aligned; Meech et al. 2025, not yet ingested).

## Key findings

- **Tentative H₂O.** Free-retrieval log X(H₂O) ≈ −7.05⁺⁰·⁶⁷₋₁·⁹⁶ ([[POSEIDON]] / Eureka! R = 400) with Δ ln Z = 1.9; weak by Sellke 2001 mapping (~2–2.5σ). Detection significance varies modestly across reductions and retrieval codes.
- **Tentative CO₂.** log X(CO₂) ≈ −8.46⁺⁶·⁰²₋₀·²⁸ in [[POSEIDON]] free retrieval; Δ ln Z = 1.5 (≲ 2σ).
- **CO not detected.** [[POSEIDON]] free retrieval Δ ln Z = −0.7 — model including CO is *not* preferred.
- **No high-temperature absorbers.** Including SiO, VO, TiO, AlO, SH, H₂S yields physically unrealistic high abundances (e.g., log X(VO) ≈ −2.79); ruled out as physical despite Δ ln Z = 2.0–2.4 statistical preference (POSEIDON), since 2025_Gascon_KELT7b (Gascón et al. 2025; not yet ingested) HST/G280 optical observations show no opacity at these wavelengths where high-T species would dominate.
- **Two competing scenarios from equilibrium-chemistry retrievals:**
  - **Cloud-deck scenario (preferred, Δ ln Z = 1.6–3.1):** high-altitude opaque cloud deck at log P_cloud ≈ 0.62⁺⁰·⁹¹₋⁰·⁹⁴ bar masking features; near-equilibrium abundances at C/O ≈ 0.43–0.74 and metallicity 1–16× solar.
  - **Low-metallicity scenario (free-chemistry):** atmosphere genuinely low-metallicity (well below solar) with low-altitude clouds; features absent because absorber abundances are low.
- **Retrieved C/O = 0.43–0.74** across all reductions and resolutions; large 1σ uncertainties up to 0.32; consistent with stellar C/O = 0.54 (Asplund 2009 solar reference) and with stellar [Fe/H] = +0.139 ± 0.075. **All posteriors disfavor C/O > 0.9–1 at ~2σ.**
- **Retrieved metallicity = solar to ~15× solar** (1.4–16× solar across reductions). Equilibrium pRT and POSEIDON values agree within 1–2σ; cannot distinguish stellar from super-stellar.
- **NRS1/NRS2 detector offset documented** at 28 ± 12 ppm (Tiberius), 51⁺¹⁰₋₁₃ ppm (Eureka!), and -55⁺¹¹₋₁₀ ppm (ExoTiC-JEDI) — variable across pipelines and inconsistent for Tiberius's broadband fit. Does not change the inferred atmospheric parameters.
- **Mirror tilt event during observation.** A tilt event ~one-third into the transit caused a step in the light curves; modeled as a step function in all three reductions. Smaller in magnitude than the WASP-39 b tilt event ([[2026_RoyPerez_WASP39b]]) — not visible in spectral trace position or FWHM, only in flux. JWST FGS data via spelunker (Deal & Espinoza 2024; not ingested) confirm the event occurred ~5 min before light-curve detection.
- **HST + JWST joint retrieval inconclusive.** Combining the 2025_Gascon_KELT7b HST/UVIS+G280 optical (Gascón 2025; not ingested) and the Pluriel et al. 2020 HST/WFC3 IR (not ingested) data with the JWST/NIRSpec spectrum **does not improve constraints**: the H⁻ continuum opacity is unconstrained without overlapping wavelengths between G280 and NIRSpec, and the offset between detectors cannot be resolved. C/O ≈ 0.25–0.9 from joint retrievals; consistent with multiple formation scenarios.
- **BOWIE-ALIGN context.** KELT-7 b is the third target in JWST GO 3838. Comparison: WASP-15 b (misaligned; Kirk et al. 2025, not ingested) shows super-solar metallicity with solar C/O — consistent with planetesimal accretion. TrES-4 b (aligned; Meech et al. 2025, not ingested) shows sub-solar metallicity and sub-solar C/O — consistent with oxygen-rich gas accretion or carbon-poor planetesimals plus low-metallicity gas. The KELT-7 b range (solar to super-solar metallicity, broadly solar C/O) does not yet discriminate at the per-target level, but the population trend (4–6 planets total in BOWIE-ALIGN) is the survey's deliverable.

## Methods

Single 7.51 hr JWST NIRSpec G395H BOTS observation under [[JWST-GO-3838]] on 2024 February 3 (NRSRAPID, 5 groups/integration, 4976 integrations, SUB2048). Three parallel reductions:

- **[[Eureka]]** — `jwst` v1.12.2 stages 1–2 with custom 1/f and bias correction; box extraction; BATMAN + linear systematic + step-function for mirror tilt; emcee MCMC.
- **[[ExoTiC-JEDI]]** — `jwst` v1.13.4 with custom group-level bias and 1/f; least-squares + step function; ExoTiC-LD limb darkening (Grant & Wakeford 2024).
- **[[Tiberius]]** — `jwst` v1.8.2 wrapper with custom 1/f at group level; BATMAN with step function and linear baseline; emcee.

All three reductions agree to within ~50 ppm. R = 100 and R = 400 spectra produced.

Atmospheric inference:

- **[[POSEIDON]]** — free chemistry (R = 30,000 forward at 1–5.2 μm; PyMultiNest 1000 live points) with H/He bulk; equilibrium chemistry (C/O, [M/H] free); high-temperature species set (SiO, VO, TiO, AlO, SH) tested separately.
- **[[petitRADTRANS]]** v3.1 — equilibrium chemistry from [[easyCHEM]] (Lei et al. 2025) tabulated grid; free chemistry (4-parameter T–P; PyMultiNest 500 live points).
- **[[NEMESISPY]]** — for HST/UVIS+G280 + JWST joint retrievals; H⁻ + e⁻ as free parameters per Gascón et al. 2025 framework (not ingested).

Stellar contamination not formally retrieved — KELT-7 is an F2 dwarf above the Kraft break (T_eff > 6100 K), beyond the regime where TLSE typically dominates.

## Caveats & limitations

- **Single visit.** Individual feature significances are below 3σ; all conclusions rest on Bayesian model preferences rather than feature detection. A second G395H transit would be needed to firm up either the cloud-deck or low-metallicity interpretation.
- **NRS1/NRS2 detector offset varies across reductions** (range −55 to +51 ppm). Eureka! posterior favors low-metallicity solution; Tiberius posterior favors moderate metallicity — possibly driven by the offset rather than by intrinsic atmospheric properties.
- **High-altitude cloud at log P_cloud ≈ 0.5 bar requires SiO₂ or Al₂O₃ condensates** (Wakeford & Sing 2015); not unprecedented at T_eq ≈ 2050 K but the wider patchy-cloud parameter space is not explored.
- **H⁻ from HST observations + lack of UV-NIR overlap with JWST** prevents firm continuum / cloud-level constraint when combining datasets.
- **Free vs equilibrium chemistry yield different metallicity.** Free retrievals favor metallicity ~1–4× solar (Eureka! R = 400 POSEIDON: log [M/H] = 0.62⁺⁰·⁵³₋₀·⁴⁸ — i.e., ~4× solar); equilibrium retrievals span 1–16× solar. The discrepancy is data-driven, not arbitrary, but cautions that the inferred formation scenario depends on the retrieval framework.
- **C/O range 0.25–0.9 from JWST + HST joint** is too wide to distinguish formation scenarios (pebble vs planetesimal accretion at different disc locations).

## Open questions / follow-ups

- **Does a second transit confirm the cloud-deck or low-metallicity scenario?** A repeat G395H visit would beat down the NRS1/NRS2 offset uncertainty and improve feature significance.
- **Can MIRI/LRS resolve the cloud-vs-metallicity degeneracy?** SiO₂ / Al₂O₃ cloud absorption features at 7–10 μm would be diagnostic; not in the GO 3838 program.
- **What does the population-level analysis of BOWIE-ALIGN (4–6 planets) reveal?** With WASP-15 b (misaligned, super-solar Z, solar C/O), TrES-4 b (aligned, sub-solar Z and C/O), and KELT-7 b (aligned, ambiguous), the alignment-vs-formation hypothesis is approachable in 2026.
- **Is the H⁻ inferred from HST a real ultra-hot-Jupiter dissociation feature on a planet at T_eq = 2048 K?** Or stellar / instrumental? A combined NIRISS + NIRSpec + MIRI study would resolve.

## Related

- [[2026_RoyPerez_WASP39b]] — also documents a NIRSpec mirror tilt event during WASP-39 b ERS observations; the Ahrer 2025 KELT-7 b event is smaller in magnitude but shares the methodology.
- [[2025_Gressier_HATP26b]] — same JWST-TST DREAMS retrieval framework family; Neptune-mass counterpoint to KELT-7 b's hot-Jupiter ambiguity.
- WASP-15 b (Kirk et al. 2025) and TrES-4 b (Meech et al. 2025) — first two BOWIE-ALIGN targets; both not yet ingested. KELT-7 b is the third.
- [[2026_Heinke_HATP12b]] — uses the same POSEIDON information-content philosophy applied here at the joint-data level; HAT-P-12 b had the multi-instrument coverage to disambiguate that KELT-7 b currently lacks.
