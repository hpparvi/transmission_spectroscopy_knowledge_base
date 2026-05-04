---
type: code
aliases: [HELIOS radiative transfer]
tags: [radiative-transfer, thermal-emission, forward-model, exoplanet-atmosphere]
---

# HELIOS

A 1D radiative-transfer and thermal-structure code for exoplanet atmospheres (Malik et al. 2017, 2019; not yet ingested). Solves for the dayside temperature–pressure profile and computes emission spectra for a given composition, gravity, and stellar irradiation. Used for secondary-eclipse forward modeling: generating predicted emission spectra for bare-rock, atmospheric, and analogue scenarios to compare against MIRI/LRS observations.

## Papers
- [[2024_Xue_GJ1132b]] — forward models for bare-rock, CO₂, H₂O, and Earth/Venus-analogue scenarios for GJ 1132 b 5–12 μm secondary eclipse; all atmospheric models rejected in favor of a blackbody.
- [[2025_Xue_GJ3929b]] — HELIOS 3.0 emission forward models (bare-rock, CO₂-dominated, analogue scenarios) for GJ 3929 b 15 μm eclipse photometry.
- [[2026_Holmberg_GJ3473b]] — HELIOS + HELIOS-K atmospheric grids for thick-CO₂ and thin-atmosphere scenarios on GJ 3473 b; opacity baseline for the eclipse-depth interpretation.
- [[2025_Crossfield_SO2shoreline]] — primary T-p code for the 936-model SO₂ shoreline grid (T_eq = 250–2050 K × [M/H] = 0.3–1000× solar × C/O × T_int × XUV × K_zz); HELIOS feeds VULCAN and petitRADTRANS in a forward-modeling chain.
