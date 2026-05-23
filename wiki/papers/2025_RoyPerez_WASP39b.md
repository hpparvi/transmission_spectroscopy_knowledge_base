---
type: paper
bibkey: 2025_RoyPerez_WASP39b
authors: [Roy-Perez, J., Pérez-Hoyos, S., Barrado-Izagirre, N., Chen-Chen, H.]
year: 2025
venue: A&A
arxiv: 2505.02081
doi: 10.1051/0004-6361/202450142
targets: [WASP-39b]
instruments: [JWST-NIRSpec]
methods: [atmospheric-retrievals, transit-spectroscopy, cloud-extinction-modeling]
codes: [PSG, PUMAS, MOPSMAP, MultiNest, FIREFLy]
species_detected: [H2O, CO2, CO, SO2, Na, H2S]
species_tentative: [CH4]
tags: [hot-jupiter, jwst-ers, wasp-39b, aerosols, clouds, cloud-particle-properties, mopsmap]
ingested: 2026-05-18
---

# The Role of Cloud Particle Properties in the WASP-39 b Transmission Spectrum Based on JWST/NIRSpec Observations

**Authors:** Roy-Perez, Pérez-Hoyos, Barrado-Izagirre, Chen-Chen (2025, A&A 694:A249) · [arXiv:2505.02081]
**Targets:** [[WASP-39b]] · **Instrument:** [[JWST-NIRSpec]] (PRISM)

## TL;DR
Re-analyzes the JWST/NIRSpec PRISM transit spectrum of [[WASP-39b]] (the canonical [[JWST-ERS-1366]] benchmark) — focusing **specifically on cloud particle properties** rather than gas detection. Uses the [[FIREFLy]] reduction (Rustamkulov et al. 2023; not ingested) as input data and runs >5 cloud-vertical-profile retrievals + 4 cloud-extinction-spectral-behavior retrievals via [[PSG]]/PUMAS forward modeling + [[MultiNest]] nested sampling, with the [[MOPSMAP]] database providing aerosol optical cross-sections. **Two cloud extinction models with non-flat wavelength dependence are decisively preferred** over a flat-cloud baseline: the Ångström-exponent parametrization (ln B = 8.02, strong) and the MOPSMAP physical-aerosol model (ln B = 5.57, strong). The best-fit MOPSMAP model gives effective particle radius **r_eff = 0.55⁺⁰·⁰³₋₀.⁰³ μm** with spherical aerosols and refractive index n_r = 1.4. Different cloud extinction models lead to **molecular abundance shifts of up to ~4 dex** (notably H₂S: −2.23 in model III vs −6.29 in model IV), and CH₄ shifts in and out of statistical significance with the cloud parameterization. The paper's central message: **cloud extinction parameterization is a leading source of bias in retrieved molecular abundances**, and JWST/NIRSpec PRISM's 0.5–5.5 μm range is the first instrument capable of breaking the wavelength-flat-cloud assumption commonly made in HST-era retrievals.

## Key findings

- **Cloud vertical profile: Uniform (model A) preferred by Occam's razor.** Five cloud vertical models (A=Uniform, B=Opaque step, C=Step, D=Step+Uniform, E=Slab) all reach similar evidence (ln B ranges from −3.87 for B to ≈ 0 for others); the simplest (A) is selected.
- **Cloud extinction wavelength dependence: Ångström strongly favored** over flat.
  - Model I (Flat): reference (ln B = 0)
  - Model II (Free linear slope): ln B = −1.40 (worse than flat)
  - Model III (Ångström exponent α with Q_ext ∝ λ⁻ᵅ): **ln B = +8.02** (strong evidence over flat)
  - Model IV (MOPSMAP physical aerosols): **ln B = +5.57** (strong evidence)
- **Two physically distinct best-fit aerosol scenarios.**
  - **Model III Ångström α = 2.89⁺⁰·⁵⁷₋₀.₅₁** — opacity **strongly decreases** with wavelength (small-particle behavior, Rayleigh-like). However, this requires unphysical mean molecular weight μ_atm = 3.50 g mol⁻¹ to fit the data.
  - **Model IV MOPSMAP r_eff = 0.55⁺⁰·⁰³₋₀·⁰³ μm** with refractive index n_r = 1.4 — opacity **slightly increases** with wavelength (large-particle behavior). Mean molecular weight μ_atm ≈ 2.60 g mol⁻¹ (consistent with H₂-He expectation).
  - The paper recommends Model IV (large-particle increasing-opacity) as the most physically realistic.
- **Molecular abundance bias from cloud parameterization.** Retrieved abundances differ between cloud models in ways that affect even the qualitative claim of detection:
  - log CO₂: −3.70 (Model III) vs −3.97 (Model IV)
  - log H₂O: −2.50 vs −2.73
  - log CO: −1.41 vs −1.99
  - log SO₂: −4.70 vs −5.05
  - log Na: −5.19 vs −5.14
  - **log H₂S: −2.23 (Model III) vs −6.29 (Model IV) — 4 dex spread**. H₂S is statistically supported in Model III (ln B for removal = −14.0) but **not** in Model IV (ln B for removal = −0.86, below threshold).
  - log CH₄: not statistically supported (ln B ≈ 0.37) in baseline Model III, but reaches ln B = 8.66 (strong) when included alongside Model III; reaches log CH₄ = −5.85⁺⁰·¹⁴₋₀·¹⁴, an upper limit consistent with Rustamkulov 2023.
- **Confirms H₂O, CO₂, SO₂, Na, CO, H₂S** at log VMR consistent with prior ERS analyses (Ahrer 2023, Alderson 2023, Powell 2024, Fisher 2024 — none ingested) within ~0.5–1 dex.
- **MOPSMAP enables direct physical-particle inference.** The MOPSMAP database (Gasteiger & Wiegner 2018; not ingested) provides aerosol optical properties (Q_ext, single-scattering albedo, asymmetry parameter) for parametrizable particle sizes, shapes, and refractive indices — allowing retrieval to back out physical particle properties (r_eff, n_r, n_i) rather than fitting empirical opacity shapes.
- **Imaginary refractive index not robustly constrained.** Posteriors show n_i smaller than 10⁻² fits equally well; particle absorption (composition) is not well-constrained in transit geometry alone — reflected-light phase-curve geometry needed to discriminate.

## Methods

- **Input data.** WASP-39 b NIRSpec/PRISM spectrum from Rustamkulov et al. 2023 (Nature 614:659; not yet ingested) (Nature 614:659), using their **FIREFLy reduction** (selected for cross-comparison against ERS-paper reductions).
- **Forward model.** [[PSG]] (Planetary Spectrum Generator; Villanueva et al. 2018; not ingested), invoking PUMAS (Planetary and Universal Model of Atmospheric Scattering; Villanueva 2015, Smith 2013) for correlated-k line-by-line radiative transfer. Line lists: H₂O (Polyansky 2018), CO₂ (Yurchenko 2020), CO (Li 2015), SO₂ (Gordon 2022), Na (Allard 2019), H₂S (Gordon 2022), CH₄ (Yurchenko 2024), K (Allard 2016). Includes Rayleigh (Sneep & Ubachs 2005), refraction, UV broad absorption, CIA from H₂-H₂ (Abel 2011) and H₂-He (Abel 2012), multiple scattering.
- **Atmosphere parametrization.** 40 levels uniformly log-spaced from 10⁻⁶ to 10¹ bar. P-T profile: isothermal (selected by model comparison; ln B for two-parameter = 2.66 and three-parameter = 4.38 over isothermal — but the simplest model preferred by Occam's). T_iso ∈ [500, 2000] K uniform prior. Molecular abundances log-uniform [10⁻¹², 10⁻¹] independent. D_pl Gaussian prior 179000 ± 7000 km (Faedi 2011), R_⋆ Gaussian 0.895 ± 0.023 R_⊙, log g Gaussian 0.63 ± 0.05 m s⁻² (Faedi 2011).
- **Cloud parametrization.** Cloud vertical profile (model A: uniform), with three free parameters [Cloud mass mixing ratio (log-uniform), P_Top, P_Bot]. Cloud extinction with 1–3 additional free parameters depending on model (m_Cl slope for II, α Ångström for III, r_eff for IV).
- **Aerosol optical properties.** [[MOPSMAP]] database (Gasteiger & Wiegner 2018; not ingested) computes Q_ext(λ) for spherical aerosols with assumed n_r = 1.4 + n_i = 10⁻⁴ → 10⁻²; size distributions log-normal with v_eff = 0.1 fixed.
- **Bayesian inference.** [[MultiNest]] via custom in-house wrapper (PSG does not natively integrate MultiNest); 88 degrees of freedom; Bayes factor model selection on Jeffrey's scale (ln B > 5 strong, > 2.5 moderate).

## Caveats & limitations

- **Cloud single-scattering albedo and asymmetry parameter were not varied** — transit geometry has limited sensitivity to these (per Barstow 2016). Reflected-light phase-curve geometry would constrain them better.
- **Spherical aerosols assumed.** Real atmospheric particles often have fractal/irregular morphology (Adams 2019; Lavvas 2024 not ingested). Ohno-Kawashima fractal-aggregate corrections not applied.
- **n_r fixed at 1.4** (typical of water-rich aerosols in Solar System work). Different aerosol compositions (Mn-rich silicate, ZnS, KCl, photochemical hazes) have substantially different n_r — could bias the inferred r_eff.
- **Ångström-model μ_atm = 3.50 g mol⁻¹** is "probably unphysical" — paper flags this as a clear warning that Model III (small-particle Rayleigh) is geometrically possible but physically suspect.
- **Imaginary refractive index n_i** poorly constrained: any value smaller than 10⁻² is compatible with the data; composition cannot be inferred in transit geometry alone.
- **Only single visit / single reduction.** The companion [[2026_RoyPerez_WASP39b]] paper looks at pipeline-systematic spread; this paper does not vary reductions.
- **Independent constraints on aerosol identity not used.** Could combine with NIRSpec dayside emission (Powell 2024 not ingested) or MIRI/LRS (Powell 2024 not ingested) to discriminate composition more directly.

## Open questions / follow-ups

- **Confirm large-aerosol-particle interpretation via independent geometry.** Dayside emission or reflected-light measurements could break the small-vs-large-particle degeneracy seen between Model III and Model IV.
- **Test fractal/non-spherical particle models.** Solar System experience (Pluto, Titan) and laboratory experiments (He 2018, 2024 not ingested) consistently produce fractal aggregates; the inference of spherical r_eff = 0.55 μm may translate to a different fractal-equivalent size.
- **Imaginary refractive index from phase-curve data.** Detection of strong forward/backscattering peaks would discriminate the aerosol composition (water-rich tholin vs Mn-silicate vs KCl).
- **Cross-validation against pipeline systematics ([[2026_RoyPerez_WASP39b]]).** That paper's 2-dex spread in retrieved parameters across pipelines is consistent with this paper's claim that cloud parameterization is the dominant inference systematic — but cross-checks between the two angles are not yet integrated.
- **Generalize to other JWST-NIRSpec targets.** The Ångström + MOPSMAP analysis pattern is portable to other cloudy hot Jupiters (WASP-17 b, WASP-43 b, HD 189733 b); the paper invites this generalization without performing it.

## Related
- Rustamkulov et al. 2023 (Nature 614:659; not yet ingested) — primary NIRSpec PRISM observation; provides the FIREFLy reduction used as input data.
- [[2026_RoyPerez_WASP39b]] — companion paper from same group examining **data-reduction-pipeline systematics** rather than cloud parameterization. Together they document up-to-2-dex spread in retrieved parameters from both data-level and model-level choices.
- [[2025_Ohno_GJ1214b]] — analogous photochemical-microphysical haze grid analysis on GJ 1214 b; explicit two-moment microphysics rather than this paper's empirical Ångström / MOPSMAP fits.
- [[WASP-39b]] — target hub.
- [[aerosols]] — concept page; this paper provides the first-decisive-rejection-of-flat-cloud demonstration on a NIRSpec PRISM benchmark target.
- [[2026_RoyPerez_WASP39b]] is by the same lead author (a 2026 paper); the present paper precedes it methodologically — pipeline systematics build on the cloud-parameterization framework introduced here.
