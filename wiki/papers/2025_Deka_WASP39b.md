---
type: paper
bibkey: 2025_Deka_WASP39b
authors: [Deka, T., Khan, T. B., Dewan, S., Ghosh, P., Das, D., Majumdar, L.]
year: 2025
venue: ApJ
arxiv: 2507.05049
doi: 10.3847/1538-4357/add33d
targets: [WASP-39b]
instruments: [JWST-NIRISS, JWST-NIRSpec, JWST-MIRI]
methods: [atmospheric-retrievals]
species_detected: [H2O, CO2, CO, SO2, H2S, Na, K]
codes: [POSEIDON, FastChem, FIREFLy, Eureka, Tiberius, SPARTA, supreme-SPOON, MultiNest]
tags: [hot-jupiter, retrieval-framework, machine-learning, jwst-ers, mass-metallicity, methodology, benchmarking]
ingested: 2026-05-04
---

# A Next-generation Exoplanet Atmospheric Retrieval Framework for Transmission Spectroscopy (NEXOTRANS): Comparative Characterization for WASP-39 b Using JWST NIRISS, NIRSpec PRISM, and MIRI Observations

**Authors:** Deka, Khan, Dewan, Ghosh, Das, Majumdar 2025, ApJ 989:50 · [arXiv:2507.05049]
**Targets:** [[WASP-39b]] · **Instruments:** [[JWST-NIRISS]] (SOSS), [[JWST-NIRSpec]] (PRISM), [[JWST-MIRI]] (LRS)

## TL;DR
Introduces **NEXOTRANS**, a hybrid Bayesian + machine-learning atmospheric retrieval framework. Bayesian inference via PyMultiNest ([[MultiNest]]) and UltraNest; four ML algorithms (Random Forest, Gradient Boosting, k-Nearest Neighbor, Stacking Regressor) for accelerated retrieval. Includes **NEXOCHEM**, an in-house chemical-equilibrium module benchmarked against [[FastChem]]. Four chemistry options: free, equilibrium, **modified hybrid equilibrium**, and **modified equilibrium-offset** chemistry — the latter two extend the Constantinou & Madhusudhan 2024 (not ingested) frameworks. Applied to WASP-39 b with the full panchromatic JWST/NIRISS+PRISM+MIRI data (0.6–12.0 μm). For the best-fit hybrid model: O/H = 14.12⁺²·⁸⁶⁻¹·⁸² × solar, C/H = 21.37⁺⁴·⁹³⁻³·¹⁸ × solar, S/H = 5.37⁺⁰·⁷⁹⁻⁰·⁶⁵ × solar, and C/O = 1.35⁺⁰·⁰⁵⁻⁰·⁰¹² × solar. The ML retrieval (Stacking Regressor) is **highly competitive** with Bayesian retrieval (R² = 0.855 → 0.76 with the full-WASP-39 b data) but with much lower computational cost.

## Key findings
- **NEXOTRANS framework** introduced: Bayesian sampling via PyMultiNest (100 live points) or UltraNest; ML via supervised ensemble (Stacking Regressor with Random Forest + Gradient Boosting + kNN base models, Ridge Regressor metamodel). Four chemistry options:
  1. **Free chemistry** (10 species: Na, K, H₂O, CO₂, CO, SO₂, H₂S, CH₄, NH₃, HCN; constant VMR)
  2. **Equilibrium chemistry** (NEXOCHEM-driven; vary C/O and [M/H])
  3. **Modified hybrid equilibrium** (NEXOCHEM-driven; some species offset; SO₂ free)
  4. **Modified equilibrium-offset** (NEXOCHEM-driven; multiplicative offsets per species)
- **NEXOCHEM** equilibrium-chemistry module benchmarked against [[FastChem]] across T = 300–4000 K, P = 10⁻⁷–10² bar, C/O = 0.2–2, [M/H] = 10⁻¹–10³ × solar; agreement well within typical observational uncertainty.
- **Cloud + aerosol toolkit:** uniform/patchy gray, sigmoid clouds, Mie-scattering aerosols (MgSiO₃, ZnS), and Ackerman & Marley clouds — all with high-altitude haze + cloud-deck handling.
- **Validation against eight community retrieval codes** (ARCiS, Aurora, CHIMERA, Helios-r2/[[BeAR]], NEMESIS, [[PyratBay]], [[TauREX3]], POSEIDON) on the WASP-39 b MIRI/LRS-only retrievals; all retrievals agree within 1σ on log H₂O ≈ −1.5 to −2.0 and log SO₂ ≈ −5.5 to −5.8.
- **Best-fit hybrid retrieval (full panchromatic data):**
  - log H₂O = −2.60⁺⁰·⁰⁸⁻⁰·⁰⁸ (Bayesian) / −2.60⁺⁰·²⁷⁻⁰·³⁹ (ML)
  - log CO₂ = −4.59⁺⁰·⁰⁵⁻⁰·⁰⁵ (Bayesian) / −4.42⁺⁰·⁰⁵⁻⁰·⁵⁵ (ML)
  - log CO = −1.99⁺⁰·⁰⁴⁻⁰·⁰⁴ (Bayesian) / −2.25⁺⁰·²⁷⁻⁰·³² (ML)
  - log SO₂ = −5.73⁺⁰·¹¹⁻⁰·¹³ (Bayesian) / −6.24⁺¹·¹⁴⁻⁰·³² (ML)
  - log H₂S = −3.93⁺⁰·⁰⁵⁻⁰·⁰⁵ (Bayesian) / −3.81⁺⁰·⁰⁰⁻⁰·⁰⁰ (ML); broadly compatible across all four chemistry models
- **Elemental ratios:** O/H = 14× solar, C/H = 21× solar, S/H = 5× solar, C/O = 1.35× solar (≈ 0.80 absolute). Sits on the **mass-metallicity relation** for solar-system gas giants (Jupiter to Uranus/Neptune); slightly subsolar S/O.
- **Aerosol composition:** MgSiO₃ effective particle radius ~10⁻²·⁵ μm (Mie regime); ZnS effective radius ~10⁻¹·³ μm; aerosol coverage fraction f_c ≈ 0.55. Hybrid + offset models prefer larger MgSiO₃ particles and spatial heterogeneity.
- **Computational efficiency:** correlated-k forward model at R = 1000 with 5011 wavelength points completes in ~610 ms; opacity-sampling forward at R = 20,000 with 100,213 wavelength points in ~1 s after grid construction. Runs on standard 16-GB / 64-GB desktop hardware.

## Methods
NIRISS SOSS (Feinstein et al. 2023; not ingested) reduced via [[supreme-SPOON]]; NIRSpec PRISM (Rustamkulov et al. 2023; not ingested) via [[FIREFLy]] (Λ < 2 μm excluded due to detector saturation); MIRI LRS via three reductions ([[Eureka]], [[Tiberius]], [[SPARTA]]) following Powell et al. 2024 (not ingested). Bayesian retrieval at 100 live points + tolerance 0.5 with PyMultiNest; ML retrieval with 6 features per spectrum reduced from native resolution. Three-region Madhusudhan-Seager P-T parameterization. Mie aerosol scattering with explicit MgSiO₃ + ZnS condensates; aerosol vertical profile parameterized with `f_c` and `h_c` (slope).

## Caveats & limitations
- ML retrievals **do not provide reliable Bayesian-style posteriors** — uncertainty quantification relies on perturbation/resampling around best-fit predictions; not a fully principled approach.
- NEXOCHEM equilibrium-chemistry agreement with FastChem is shown only over a limited temperature range; extrapolation to higher/lower T/P may diverge.
- 1D plane-parallel atmosphere assumed; limb asymmetry not modeled despite WASP-39 b being among the strongest [[limb-asymmetry]] cases ([[2025_Fu_limb-asymmetry]]).
- The "modified hybrid equilibrium" and "modified equilibrium-offset" approaches use NEXOTRANS-specific implementations that differ from S. Constantinou & N. Madhusudhan 2024 (not ingested); cross-comparison with the Constantinou & Madhusudhan implementation would clarify the specifics.
- ML models trained on free-chemistry-derived data, then validated on observations; this introduces a model-form bias if the true atmosphere violates the equilibrium-/free-chemistry boundary conditions.
- WASP-39 b's PRISM data below 2 μm is excluded due to detector saturation; the optical wavelength range and Na/K constraints come solely from NIRISS.

## Open questions / follow-ups
- Does NEXOTRANS's ML retrieval generalize to other targets, or does it require retraining per target? Benchmarking on a broader sample (TOI-836b, WASP-80b, etc.) would clarify.
- How does the hybrid retrieval compare with a 2D limb-asymmetry retrieval on WASP-39 b? [[2025_Fu_limb-asymmetry]] argues this matters at the 2 dex level for limb-averaged abundances.
- Which Bayesian + ML combination is most efficient? The Stacking Regressor + PyMultiNest comparison shows MLs match Bayesian within 1σ at ~0.1× the wall-clock time.

## Related
- [[2026_RoyPerez_WASP39b]] — independent reduction-pipeline study on the same WASP-39 b data; documents up to 2 dex variation in retrieved abundances **between** pipelines (Tshirt vs. Eureka vs. supreme-SPOON vs. FIREFLy); orthogonal source of methodological variance to the framework variations explored in NEXOTRANS.
- [[2025_Verma_HD209458b]] — analogous methodology paper introducing the [[SANSAR]] framework on HD 209458 b panchromatic HST+JWST data; documents wavelength-coverage bias.
- [[2025_Fu_limb-asymmetry]] — WASP-39 b shows > 5σ limb asymmetry in NIRISS/SOSS; the limb-averaged retrieval bias documented there is up to 2 dex on metallicity, comparable to the framework-driven variation in NEXOTRANS.
