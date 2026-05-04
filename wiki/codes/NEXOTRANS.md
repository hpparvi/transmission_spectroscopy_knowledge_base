---
type: code
aliases: [NEXOTRANS, NEXOCHEM, Next-generation Exoplanet Atmospheric Retrieval Framework]
tags: [retrieval-framework, machine-learning, bayesian, equilibrium-chemistry, hot-jupiter, hub-candidate]
---

# NEXOTRANS

Hybrid Bayesian + machine-learning atmospheric retrieval framework for exoplanet transmission spectroscopy, introduced in [[2025_Deka_WASP39b]] (Deka, Khan, Dewan, Ghosh, Das, Majumdar 2025, ApJ 989:50). Bayesian sampling via PyMultiNest ([[MultiNest]]) and **UltraNest** (Buchner 2021); ML inference via supervised ensemble (Stacking Regressor with Random Forest + Gradient Boosting + k-Nearest Neighbor base models, Ridge Regressor metamodel). Includes **NEXOCHEM**, an in-house chemical-equilibrium module benchmarked against [[FastChem]] across T = 300–4000 K, P = 10⁻⁷–10² bar, C/O = 0.2–2, [M/H] = 10⁻¹–10³ × solar.

Four chemistry options:
1. **Free chemistry** (constant VMR for each species)
2. **Equilibrium chemistry** (NEXOCHEM; vary C/O and [M/H])
3. **Modified hybrid equilibrium** (NEXOCHEM + free SO₂; offsets per species)
4. **Modified equilibrium-offset** (NEXOCHEM + multiplicative offsets per species)

Cloud + aerosol toolkit: uniform/patchy gray cloud, sigmoid cloud, Mie-scattering aerosols (MgSiO₃, ZnS), and Ackerman & Marley clouds; high-altitude haze and cloud-deck handling via [[POSEIDON]]-style parameterization.

Validated on WASP-39 b MIRI/LRS data against eight community retrieval codes ([[ARCiS]], [[Aurora]], [[CHIMERA]], Helios-r2/[[BeAR]], NEMESIS, [[PyratBay]], [[TauREX3]], [[POSEIDON]]); all retrievals agree within 1σ on log H₂O ≈ −1.5 to −2.0 and log SO₂ ≈ −5.5 to −5.8.

ML retrievals are **highly competitive** with Bayesian (R² = 0.855 → 0.76 on full WASP-39 b data) at ~0.1× the wall-clock time, but do not provide principled Bayesian posteriors — uncertainty quantification relies on perturbation around best-fit predictions.

## Papers

- [[2025_Deka_WASP39b]] — introduces NEXOTRANS and NEXOCHEM; benchmarked on WASP-39 b panchromatic JWST NIRISS+PRISM+MIRI data; best-fit hybrid retrieval gives O/H = 14× solar, C/H = 21× solar, S/H = 5× solar, C/O = 1.35× solar; 8-code MIRI cross-comparison validation.
