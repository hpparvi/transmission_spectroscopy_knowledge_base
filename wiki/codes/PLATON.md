---
type: code
aliases: [PLATON retrieval, PLanetary Atmospheric Tool for Observer Noobs]
tags: [retrieval, gpu-accelerated, free-chemistry, transmission-spectroscopy]
---

# PLATON

A GPU-accelerated atmospheric retrieval code (Zhang et al. 2019, 2020, 2025; not ingested) supporting both forward modeling and free-chemistry retrievals of exoplanet transmission spectra. Standard implementation includes isothermal P-T, opaque cloud deck, optional transit-light-source effect (TLSe) for starspot contamination, and instrumental offsets. Default opacity grid at R = 20,000 with 100 K temperature spacing; the latest version (6.3.1 as used in [[2025_Luque_K2-18b]]) supports custom high-resolution grids (R = 100,000 from DACE) with 50 K spacing for cool sub-Neptune targets. Nested sampling via pymultinest with Importance Nested Sampling (more accurate log-evidence than vanilla MultiNest at high dimension).

## Papers

- [[2025_Luque_K2-18b]] — primary retrieval framework on JExoRES native-resolution K2-18 b panchromatic spectrum (0.6–12 μm); 6.3.1 release with custom DACE R = 100,000 opacities and HITEMP 2020 CH₄ line list; TLSe-included retrievals confirm [[2025_Schmidt_K2-18b]] finding that TLSe inclusion does not alter molecular posteriors.
- [[2025_Canas_TOI5205b]] — PLATON v6.1 equilibrium-chemistry retrieval on TOI-5205 b NIRSpec PRISM with single-heterogeneity TLS framework + dynesty sampling. χ²_ν = 2.45; recovers sub-solar metallicity ([Fe/H] = −1.92⁺⁰·¹¹₋₀·₀₅) and super-solar C/O = 1.2 ± 0.4. Cross-validation against [[POSEIDON]] (which uses spots + faculae) — both codes recover similar metallicity but POSEIDON has lower χ²_ν.
- Davenport, Kempton, Nixon et al. 2025 (not ingested) — mini-Neptune transmission retrievals.
- [[2025_Fu_statistical-trends]] — PLATON forward-model grid for **population-level CO₂-L and CO-L index modeling**. Cloud-free + equilibrium chemistry + isothermal TP; 7 metallicities (1×–1000× solar) × 6 C/O ratios (0.1–1.1); BIC-grid evaluation across 8 hot-Jupiter / sub-Saturn JWST transmission spectra. Best fit: **mass-metallicity correlation + C/O = 0.3**.

Cross-checks against [[SCARLET]] in [[2025_Luque_K2-18b]] confirm consistency of retrieved abundances between independent frameworks operating on the same data.
