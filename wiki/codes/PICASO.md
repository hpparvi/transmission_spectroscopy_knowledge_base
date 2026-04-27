---
type: code
aliases: [PICASO RT]
tags: [radiative-transfer, forward-modeling, transmission, emission]
---

# PICASO

An open-source radiative-transfer code (Batalha et al. 2019) for exoplanet transmission and emission spectroscopy, supporting both pre-tabulated abundance profiles and chemical-equilibrium atmospheres. Typically paired with [[CHIMERA]]-derived compositions or simple isothermal parameterizations; molecular opacities are sourced from the PICASO Zenodo v2 Resampled Opacities database (R ≈ 60,000; Batalha et al. 2022).

## Papers
- [[2025_Teske_TOI776c]] — 20-metallicity × 5-pressure forward-model grid for TOI-776 c, including two-component H₂O+H₂/He and CO₂+H₂/He mixture models; Bayesian retrieval via UltraNest.
- [[2025_Bennett_GJ1132b]] — forward models for the four-visit coadded GJ 1132 b analysis; grid extended to single/two-gas 1-bar isothermal atmospheres (pure [[CH4]], pure [[CO2]], [[H2O]] ± CH₄) to reject specific compositions.
- [[2025_Alam_L168-9b]] — transmission forward models on a [[CHIMERA]] equilibrium grid for L 168-9 b; 1–1000× solar metallicities tested.
- [[2025_Alderson_TOI-776b]] — thermochemical-equilibrium grid for TOI-776 b; rules out metallicities <100–350× solar at opaque pressure 10⁻³ bar.
- [[2024_Scarsdale_L98-59c]] — metallicity × opaque-pressure grid for L 98-59 c; rules out <300× solar.
- [[2024_Alderson_TOI-836b]] — 26-metallicity × 5-opaque-pressure grid for TOI-836 b; rules out <250× solar metallicities.
- [[2023_May_GJ1132b]] — transmission forward models on a [[CHIMERA]] equilibrium grid at 100–1000× solar metallicity for GJ 1132 b.
- [[2023_Moran_GJ486b]] — R=10,000 transmission forward models on a [[CHIMERA]] equilibrium grid + single-gas end-members (pure H₂O, CO₂, CH₄, Earth-like, 1000× solar) for GJ 486 b; pure H₂O provides the best fit.
