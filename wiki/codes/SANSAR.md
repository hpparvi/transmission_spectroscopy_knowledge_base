---
type: code
aliases: [SANSAR, Suite of Adaptable plaNetary atmoSphere model And Retrieval]
tags: [retrieval-framework, forward-model, hot-jupiter, hub-candidate]
---

# SANSAR

Python-based atmospheric forward and retrieval framework introduced in [[2025_Verma_HD209458b]] (Verma, Goyal, Avarsekar, Shukla 2025, AJ 170:69). Supports both opacity-sampling and correlated-k radiative transfer (LBL precomputed at 0.001 cm⁻¹; Exo_k for k-tables); free, equilibrium, and self-consistent grid retrievals; PyFastChem (or [[FastChem]] direct) for equilibrium chemistry; PyMultiNest (which wraps [[MultiNest]]) for Bayesian sampling. Hosts a 12-species opacity database (H₂O, CO, CO₂, Na, K, CH₄, NH₃, C₂H₂, H₂S, HCN, FeH, plus CIA H₂–H₂ and H₂–He); 100-layer hydrostatic atmosphere; 2D MacDonald & Madhusudhan 2017 cloud + Rayleigh-haze parameterization. P-T parameterizations: Madhusudhan-Seager 3-region, Guillot, isothermal.

Benchmarked against [[POSEIDON]] (~6 ppm offset), [[ATMO]] (~10 ppm), [[CHIMERA]] (~4 ppm), and [[Aurora]] (~10 ppm) on WASP-96 b in both forward-model and inverse-model modes; agreement well below typical observational uncertainties (~50–100 ppm for JWST). Retrieval results consistent within 1σ across all four reference codes on the same dataset.

## Papers
- [[2025_Verma_HD209458b]] — introduces SANSAR; benchmarks against POSEIDON/ATMO/CHIMERA/Aurora on WASP-96 b; applies to HD 209458 b for three instrument combinations (NIRCam-only, WFC3+NIRCam, STIS+WFC3+NIRCam) demonstrating that wavelength coverage matters more than retrieval choice; H₂O/CO₂ overestimated by ~3 dex without optical baseline.
