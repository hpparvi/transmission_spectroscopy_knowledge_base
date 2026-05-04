---
type: code
aliases: [CHIMERA thermochemistry, CHIMERA retrieval]
tags: [thermochemistry, equilibrium-chemistry, forward-modeling]
---

# CHIMERA

A thermochemical-equilibrium forward-modeling code (Line & Yung 2013; Line et al. 2014) producing abundance profiles for H, H₂, He, H₂O, CH₄, CO, CO₂, NH₃, N₂, HCN, H₂S at specified metallicity and C/O with a Guillot (2010) T–P profile. Typically paired with [[PICASO]] for radiative transfer in transmission-spectrum forward modeling.

## Variants
- **[[ScCHIMERA]]** — self-consistent radiative-convective + photochemistry extension; coupled with [[Photochem]] for kinetics. Used in [[2026_Radica_WASP96b]].

## Papers
- [[2025_Bennett_GJ1132b]] — extended grid for the four-visit GJ 1132 b coadded analysis; 1000× solar H₂/He atmosphere rejected at > 4σ.
- [[2025_Alam_L168-9b]] — 1–1000× solar metallicity grid for L 168-9 b; rules out <100× solar cloudless atmospheres at >3σ.
- [[2024_Alderson_TOI-836b]] — precomputed chemical-equilibrium grid (interpolated via [[PICASO]]) for TOI-836 b forward models; rules out <250× solar.
- [[2023_May_GJ1132b]] — 100–1000× solar metallicity grids used to rule out H₂-dominated atmospheres on GJ 1132 b at ≥ 2.5σ.
- [[2023_Moran_GJ486b]] — thermochemical-equilibrium grid for GJ 486 b; 1000× solar H₂/He atmosphere rejected at >3σ.
- [[2025_Verma_HD209458b]] — used as one of four reference frameworks (POSEIDON, ATMO, CHIMERA, Aurora) to benchmark SANSAR's correlated-k retrieval mode on WASP-96 b; agreement within 1σ across all major parameters.
