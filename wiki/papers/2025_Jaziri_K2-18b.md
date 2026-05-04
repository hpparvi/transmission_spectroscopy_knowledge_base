---
type: paper
bibkey: 2025_Jaziri_K2-18b
authors: [Jaziri, A. Y., Drant, T.]
year: 2025
venue: A&A Letter
arxiv: 2510.06905
doi: 10.1051/0004-6361/202556905
targets: [K2-18b]
instruments: [JWST-NIRISS, JWST-NIRSpec, JWST-MIRI]
methods: [transmission-spectroscopy, atmospheric-retrievals]
species_detected: [CH4]
species_tentative: [C2H4, H2CO]
species_ruled_out: []
codes: [TauREX3, MultiNest]
tags: [sub-neptune, photochemical-haze, tholins, aerosol-modeling, miri-niriss-tension, c-h-bending-7um]
ingested: 2026-05-04
---

# Investigating aerosols as a way to reconcile K2-18 b JWST MIRI and NIRISS/NIRSpec observations

**Authors:** Jaziri, Drant (2025, A&A 702:L20; DOI 10.1051/0004-6361/202556905)
**Type:** **A&A Letter to the Editor.** Combines reduced spectra from Madhusudhan et al. 2023 (NIRISS+NIRSpec; not ingested) with Luque et al. 2025 (MIRI/LRS Eureka! reduction; not ingested) on the temperate sub-Neptune [[K2-18b]].
**Targets:** [[K2-18b]] · **Instruments:** [[JWST-NIRISS]] SOSS + [[JWST-NIRSpec]] G395H + [[JWST-MIRI]] LRS · **Programs:** [[JWST-GO-2722]] (NIRISS+NIRSpec) + GO 2372 (MIRI; PI Madhusudhan; not yet ingested)

## TL;DR

The MIRI/LRS spectrum of K2-18 b shows features ~2× larger in amplitude than its NIRISS/NIRSpec G395H counterpart — a tension the [[2025_FernandezRodriguez_K2-18b]]-style high-metallicity nonequilibrium model cannot reconcile. Jaziri & Drant test whether **photochemical hazes (tholins)** can resolve the inconsistency. Using laboratory complex-refractive-index data for seven tholin analogs (CH₄-only "exo1" and "exo2" plus five N₂/CH₄ Titan-like variants), they show that tholins produced from CH₄-only mixtures **without N atoms (exo1, exo2)** generate a strong absorption feature near **7 μm** from C–H bending plus scattering attenuation at shorter wavelengths — the dual signature observed in the data. Adding an exo1-tholin haze with R_p, T-p, and chemistry retrieved jointly **improves the combined fit by Bayes factor 5.53**, reduces the inferred CH₄ abundance by ~2 orders of magnitude (log VMR 6.3×10⁻² → 3.0×10⁻⁴), and lowers the inferred metallicity from ~20× solar to ~0.3× solar. The retrieved haze properties (particle radius ~0.02 μm, density ~10¹¹ m⁻³, layer at ~10⁻⁴ bar) are physically reasonable for H₂-rich sub-Neptune atmospheres. **The result reinforces the metallicity-composition-aerosol degeneracy** identified by [[2025_FernandezRodriguez_K2-18b]], [[2025_Felix_TOI-270d]], and now also for the K2-18 b MIRI/LRS dataset: simplified retrievals systematically inflate detection significance and bias inferred parameters when aerosols are not modeled.

## Key findings

- **MIRI/LRS feature amplitudes ~2× the NIRISS/NIRSpec features.** This is what the high-metallicity nonequilibrium model from [[2025_FernandezRodriguez_K2-18b]] (and similar; Madhusudhan 2023 not ingested) cannot reconcile.
- **CH₄-derived tholins (exo1, exo2) reproduce the dual signature.** The 7 μm C–H bending feature appears in MIRI/LRS; the scattering tail flattens NIRISS/NIRSpec at shorter wavelengths. N₂/CH₄ Titan-like tholins (Titan1–Titan5) are less favored — their N-bearing C≡N and N-H absorption features don't match.
- **Bayes factor for tholin inclusion: ln(B) = 5.53.** Strong preference per Kass-Raftery scale; "moderate-to-strong" per Kipping-Benneke 2025.
- **Tholin best-fit parameters:** particle radius r_h ≈ 0.022 μm; haze density ~10¹¹ m⁻³; layer pressure ~10⁻⁴ bar; layer thickness 10² Pa. Consistent with theoretical predictions for sub-Neptune photochemistry (Lavvas et al. 2019; not ingested).
- **CH₄ abundance drops by ~2 dex.** From the no-tholin reference of log X(CH₄) ≈ −1.20 to log X(CH₄) ≈ −3.5 with tholins. Authors note this **goes against the original photochemical-haze motivation** (which assumed gaseous CH₄ as a haze precursor).
- **Metallicity drops by ~10×.** From Z ≈ 20× solar (no tholin) to Z ≈ 0.29× solar (with tholin).
- **C/O ratio elevated:** ≥ 2.1 in both retrieval setups, with or without tholins. Consistent with [[2025_FernandezRodriguez_K2-18b]]'s super-stellar C/O finding.
- **Methane clouds vs photochemical hazes.** Tholin haze formation requires gaseous CH₄ as a precursor; the retrievals find lower CH₄ when tholins are included. Authors note this is internally tense — but methane *clouds* (condensed CH₄) at the retrieved temperatures (~340–380 K) are inconsistent with K2-18 b's expected T-p profile (clouds would form at < 100 K). **Photochemical hazes are the more physically plausible aerosol scenario**.
- **Free retrieval on MIRI alone** prefers C₂H₂, C₂H₄, H₂CO (all hydrocarbons with C–H bending features overlapping the MIRI band) over CH₄, and infers low metallicity (4.42⁺¹⁴.³¹₋₄.₀₆ × solar). **None of the molecular models is statistically preferred over a flat line for MIRI alone** — apparent features are modest (Bayes factor 2.45 for the best, "weak preference" only).
- **Free retrieval on combined NIRISS+NIRSpec+MIRI without aerosols.** CH₄, C₂H₄, CO₂ are the most-favored molecules (Bayes factor 3.29 vs reference); recovers CH₄ amplitude consistent with [[2025_FernandezRodriguez_K2-18b]] but overstates the MIRI features.
- **Joint nonequilibrium retrieval (FRECKLL + TauREx 3) at K2-18 b conditions** still cannot reproduce the larger MIRI feature amplitudes — confirming that compositional model alone cannot resolve the tension.

## Methods

- **Data inputs (literature):**
  - NIRISS/SOSS + NIRSpec/G395H spectrum from Madhusudhan et al. 2023 (not ingested) — used as published.
  - MIRI/LRS spectrum from Luque et al. 2025 [[Eureka]] reduction (not ingested) — used as published, with NIRISS-relative offset of +160 ppm applied (best-fit χ² minimization shift).
- **Retrieval framework:**
  - **[[TauREX3]] 3.1** (Al-Refaie 2021; not ingested directly) — primary retrieval engine.
  - **[[MultiNest]] / PyMultiNest** sampler (800 live points).
  - **TauREx-PyMieScatt** module (Changeat et al. 2025; not ingested) — extension for aerosol Mie-scattering with **complex refractive index** (Re + Im parts), capturing absorption beyond simple scattering. Critical for tholin modeling because the imaginary part of the refractive index drives the C–H bending features.
  - **FRECKLL** + TauREx 3 — nonequilibrium chemistry retrieval (Al-Refaie 2024; not ingested). Used to assess MIRI consistency under nonequilibrium model.
- **Tholin laboratory data:** Seven analogs from Khare et al. 1984 (Titan, original PAMPRE/COSmIC setups) and Drant et al. 2025 (exo1 = 95% Ar / 5% CH₄, PAMPRE; exo2 = 95% Ar / 5% CH₄, COSmIC; Titan1–5 = various N₂/CH₄ ratios). Particles assumed spherical with lognormal size distribution.
- **Models tested:**
  - Flat-line (reference)
  - Free-chemistry with full 11-species set (CH₄, CO₂, CO, H₂O, NH₃, C₂H₂, C₂H₂, C₂H₄, H₂CO, H₂S, SO₂, HCN)
  - Reduced free-chemistry (CH₄ + C₂H₂ + C₂H₄ + H₂CO + H₂O + CO₂)
  - Nonequilibrium chemistry via FRECKLL (one model only, computationally expensive)
  - Each retrieval × {with tholin haze, without}

## Caveats & limitations

- **No new data reduction.** Uses Madhusudhan 2023 and Luque 2025 published spectra; inherits any systematics from those.
- **MIRI/LRS offset (+160 ppm) determined by χ² minimization** of NIRISS-NIRSpec model + MIRI fit; this offset is degenerate with continuum properties.
- **Tholin laboratory data are incomplete.** Tholin "exo1" cross-sections from Drant et al. 2025 (not ingested) cover the K2-18 b temperature/pressure range only approximately.
- **Spherical-particle assumption.** Photochemical hazes can be fractal aggregates (Adams et al. 2019); spherical-only models would underestimate scattering efficiency.
- **CH₄ reduction by 2 dex contradicts the haze-formation premise.** Photochemical hazes form from gas-phase CH₄ via UV photochemistry; if retrieved CH₄ is 100× lower, haze formation rate scales accordingly. The model predicts haze but reduces the gas-phase CH₄ — internally tense.
- **No companion N₂ presence test.** Tholin formation in N₂-rich atmospheres should produce N-bearing tholins (Titan1–Titan5); the favored exo1/exo2 (CH₄-only) signature implicitly assumes a low-N atmosphere — physically reasonable for K2-18 b but a model-dependent inference.
- **Limited statistical preference (Bayes factor 5.53).** Strong by Kass-Raftery but more conservative thresholds (Kipping-Benneke 2025) place it at "moderate" preference. Independent confirmation would be needed before establishing tholin presence.
- **Single MIRI/LRS visit.** Larger MIRI feature amplitudes could be partly visit-specific (instrumental); multi-visit MIRI confirmation would be valuable.
- **Free-chemistry MIRI retrievals do not statistically prefer any molecule over a flat line.** The Bayes factor for the best MIRI-alone model is 2.45 — well below the threshold for definitive detection.

## Open questions / follow-ups

- **Independent reanalysis of MIRI/LRS K2-18 b data.** Multiple reductions of the same MIRI dataset with different pipelines would test the +160 ppm offset and the larger feature amplitudes.
- **N-bearing tholin discriminators.** N₂/CH₄ Titan-like tholins predict NH₃ and HCN bands; observation of these would test the CH₄-only (exo1) preference.
- **Mass measurements of K2-18 b's haze layer.** Particle size and density predictions can be tested against transit-light-curve scattering slope measurements at higher precision.
- **Does the metallicity-aerosol-composition degeneracy generalize?** [[2025_Felix_TOI-270d]] and [[2025_Ahrer_KELT7b]] also document the same degeneracy on different targets; a population-level metallicity reanalysis with aerosol modeling would be highly informative.
- **Multi-visit MIRI on the canonical Hycean candidates.** GJ 1214 b multi-visit MIRI, [[K2-18b]] additional MIRI, and TOI-270 d MIRI (none ingested) would be the prescribed empirical follow-up.

## Related

- [[K2-18b]] — primary target; this paper is one of multiple independent reanalyses on the same JWST dataset.
- [[2025_FernandezRodriguez_K2-18b]] — most direct empirical companion: confirms the metallicity-composition-aerosol degeneracy story without using aerosols (instead via comprehensive 13-species retrieval); in tension with Jaziri's tholin scenario primarily because Jaziri's tholin retrieval pulls metallicity to sub-solar (vs Fernández-Rodríguez's super-solar).
- [[2025_Felix_TOI-270d]] — analogous independent reanalysis with degeneracy concern on a different sub-Neptune.
- [[2025_Ahrer_KELT7b]] — analogous degeneracy on a hot Jupiter (cloud deck or low metallicity).
- [[2025_Madhusudhan_subneptunes]] — review/perspective; framework into which Jaziri's haze finding fits.
- Madhusudhan 2023, Madhusudhan 2025, Schmidt 2025, Welbanks 2025, Hu 2025, Luque 2025, Wogan & Batalha 2024 — all not yet ingested; the K2-18 b literature has now produced 8+ independent analyses on roughly the same dataset.
