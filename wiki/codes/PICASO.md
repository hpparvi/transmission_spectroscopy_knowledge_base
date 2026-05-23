---
type: code
aliases: [PICASO RT, PICASO-v4]
tags: [radiative-transfer, forward-modeling, transmission, emission, hub]
---

# PICASO

Open-source radiative-transfer and atmospheric modelling code (Batalha et al. 2019; not ingested; v4 in Mang et al. 2026; not ingested) for exoplanet transmission, emission, and reflected-light spectroscopy. Supports pre-tabulated abundance profiles, chemical-equilibrium atmospheres via FastChem / easyCHEM, and self-consistent radiative-convective equilibrium grids. Standard pairing with [[CHIMERA]] or [[FastChem]] for composition + [[Photochem]] or [[VULCAN]] for disequilibrium kinetics + [[VIRGA]] for cloud microphysics; molecular opacities from the PICASO Zenodo v2 Resampled Opacities database (R ≈ 60 000; Batalha 2025 not ingested). The wiki's most-used radiative-transfer backbone — present in ~20 papers across rocky-planet emission, sub-Neptune transmission, and hot-Jupiter population studies.

## Common usage patterns

- **Self-consistent RCTE grids**: pre-computed atmospheres over (metallicity × C/O × T_int × heat-redistribution) for retrievals on giant planets and warm Neptunes (e.g. [[2025_Mukherjee_GJ436b]], [[2025_Barat_V1298Tau-b]], [[2026_Barat_TOI1130b]]).
- **Chemical-equilibrium retrievals**: PICASO + FastChem/easyCHEM as a fast forward model for rocky-planet transmission metallicity floors (e.g. [[2024_Alderson_TOI-836b]], [[2024_Scarsdale_L98-59c]], [[2025_Alam_L168-9b]], [[2026_Batalha_LTT1445Ab]]).
- **Rocky-planet emission climate-constrained inversion**: PICASO computes the eclipse depth from a 1.5-D climate model output ([[Photochem]] / Clima) — see [[climate-constrained-inversion]] in [[2026_Wogan_LTT1445Ab]].
- **Disequilibrium-chemistry coupling**: PICASO + Photochem or VULCAN post-processing for sub-Neptune and giant-planet sulfur photochemistry (e.g. [[2025_Mukherjee_GJ436b]], [[2025_Fu_statistical-trends]]).
- **Cloud-microphysics coupling**: PICASO + VIRGA for aerosol-inclusive forward models (e.g. [[2025_Fu_limb-asymmetry]] limb-asymmetry grid).

## Trade-offs vs alternatives

- vs [[petitRADTRANS]]: PICASO's strength is broad chemistry / cloud / RCTE coupling; petitRADTRANS is the wiki's other workhorse, often preferred for free-chemistry retrievals.
- vs [[POSEIDON]]: POSEIDON is the dedicated transmission/emission *retrieval* code; PICASO is more commonly used as the forward-model engine inside larger frameworks (UltraNest, PyMultiNest, custom MCMCs).
- vs [[ATMO]]: PICASO is more flexible for adding new chemistry / cloud parameterizations; ATMO has historically been the hot-Jupiter RCTE workhorse.

## Papers
- [[2025_Gressier_HATP26b]] — 576-model self-consistent radiative-convective + chemistry grid for HAT-P-26 b (T_int × heat redistribution × [M/H] × C/O); SO₂ added as fifth grid parameter; **adding SO₂ strongly preferred (Δ ln Z = 18 vs cloud-only)**; best fit at [M/H] = 10× solar, C/O = 0.4, heat redistribution = 0.4.
- [[2025_Teske_TOI776c]] — 20-metallicity × 5-pressure forward-model grid for TOI-776 c, including two-component H₂O+H₂/He and CO₂+H₂/He mixture models; Bayesian retrieval via UltraNest.
- [[2025_Bennett_GJ1132b]] — forward models for the four-visit coadded GJ 1132 b analysis; grid extended to single/two-gas 1-bar isothermal atmospheres (pure [[CH4]], pure [[CO2]], [[H2O]] ± CH₄) to reject specific compositions.
- [[2025_Alam_L168-9b]] — transmission forward models on a [[CHIMERA]] equilibrium grid for L 168-9 b; 1–1000× solar metallicities tested.
- [[2025_Alderson_TOI-776b]] — thermochemical-equilibrium grid for TOI-776 b; rules out metallicities <100–350× solar at opaque pressure 10⁻³ bar.
- [[2024_Scarsdale_L98-59c]] — metallicity × opaque-pressure grid for L 98-59 c; rules out <300× solar.
- [[2024_Alderson_TOI-836b]] — 26-metallicity × 5-opaque-pressure grid for TOI-836 b; rules out <250× solar metallicities.
- [[2023_May_GJ1132b]] — transmission forward models on a [[CHIMERA]] equilibrium grid at 100–1000× solar metallicity for GJ 1132 b.
- [[2023_Moran_GJ486b]] — R=10,000 transmission forward models on a [[CHIMERA]] equilibrium grid + single-gas end-members (pure H₂O, CO₂, CH₄, Earth-like, 1000× solar) for GJ 486 b; pure H₂O provides the best fit.
- [[2025_Gordon_COMPASS-G395H]] — atmospheric grids ([[PICASO]] + [[easyCHEM]] in this work; [[PICASO]] + [[Photochem]] cross-check vs prior COMPASS papers) used to constrain metallicity lower limits across all seven uniformly reanalyzed targets.
- [[2025_Fu_limb-asymmetry]] — PICASO + [[VIRGA]] 1.5D forward-model grid for nine hot Jupiters' morning vs. evening limb water-band amplitudes; Na₂S, MnS, MgSiO₃ clouds; fitted slope and f_sed reproduce the population-level δA_H(T_eq) trend.
- [[2025_Barat_V1298Tau-b]] — both **free-chemistry** and **self-consistent grid** retrieval modes on V1298 Tau b panchromatic transmission; ~4000 RCTE T-P profiles (5–30 M⊕ × 0.1–100× solar metallicity × 0.1–1.0 C/O × 100–600 K T_int × 10⁰⁵–10¹⁰ K_zz) postprocessed with [[Photochem]]. Mass measurement (12 ± 1 M⊕) via leaving mass free in the retrieval (atmospheric scale height implies gravity).
- [[2025_Canas_TOI5205b]] — RCTE grid for TOI-5205 b (1170 models: 13 [M/H] × 6 C/O × 5 T_int × 3 r_st) post-processed with [[VULCAN]] photochemistry to extend below the grid's lower [M/H] = −1.0 floor. With TLS post-processing (1170 → 11700 models adding spot fraction + temperature), gives χ²_ν improvement from 14.7 → 2.6.
- [[2025_Mukherjee_GJ436b]] — **primary forward-modeling engine** for the GJ 436 b panchromatic emission spectrum. Three model grids: (i) clear-RCTE 2700 models (5 T_int × 10 [M/H] × 6 C/O × 9 r_facv) with FastChem; (ii) clear-disequilibrium 8100 models (PICASO + [[Photochem]] post-processing at 3 K_zz values); (iii) cloudy-equilibrium with [[VIRGA]] KCl + Na₂S clouds (f_sed × K_zz grid). 17-parameter free-chemistry retrieval at R = 60,000 cross-checked against grid fits.
- [[2025_Fu_statistical-trends]] — PICASO RCTE forward grid coupled with [[Photochem]] kinetics to model SO₂ vertical VMR across (T_eq, [M/H]) for the SO₂-L population study. Constant K_zz = 10¹⁰ cm² s⁻¹, T_int = 200 K, M_p = 0.42 M_J; metallicity 1× to 100× solar; T_eq 500–2500 K. Predicts the **non-monotonic SO₂-L peak at ~1000 K and ~30× solar** that the 8-planet sample broadly tracks.
