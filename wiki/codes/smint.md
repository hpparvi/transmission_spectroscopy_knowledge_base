---
type: code
aliases: [Structure Model INTerpolator]
tags: [interior-structure, water-mass-fraction, core-mass-fraction, mass-radius]
---

# smint

Python interior-structure interpolator (Piaulet et al. 2021, 2022). Models a three-layer planet (iron core + silicate mantle + hydrosphere) using the Aguichine et al. 2021 grid for the steam-atmosphere-on-supercritical-water-layer prescription. Takes mass, irradiation temperature, water mass fraction, and core mass fraction as inputs and returns radius. Coupled with `emcee` for Bayesian inference on (WMF, CMF, T_irr, Mₚ).

## Papers
- [[2025_Coulombe_TOI-270b]] — used to derive WMF = 5.6⁺²·⁵⁻²·² % (log-uniform Fe/Mg prior) or 5.1 ± 1.0% (stellar Fe/Mg prior) for [[TOI-270b]]; reparameterized in Fe/Mg to avoid the biased uniform-CMF prior.
