---
type: code
aliases: [Mie Optical Properties of aerosol Particle Sizes and Morphologies And Properties]
tags: [aerosol, mie-scattering, retrieval]
---

# MOPSMAP

A Mie-scattering aerosol optical-property database and computation package (Gasteiger & Wiegner 2018). Computes single-scattering properties (extinction, scattering, absorption cross sections; phase functions) for a range of aerosol compositions, size distributions, and morphologies. Used in [[2026_RoyPerez_WASP39b]] to supply cloud/haze opacity inputs for the [[PSG]]-based atmospheric retrieval of WASP-39 b.

## Papers

- [[2025_RoyPerez_WASP39b]] — MOPSMAP database provides physical-aerosol Q_ext(λ) for the "Model IV" retrieval of WASP-39 b NIRSpec PRISM. Spherical aerosols, n_r = 1.4, n_i = 10⁻⁴ to 10⁻², log-normal size distribution with v_eff = 0.1; retrieves r_eff = 0.55⁺⁰·⁰³₋₀·⁰³ μm. Decisively favored over a flat cloud (ln B = 5.57); slightly less preferred than the empirical Ångström model (ln B = 8.02) but **gives the more physically reasonable mean molecular weight** μ_atm = 2.60 g mol⁻¹ vs the Ångström model's "probably unphysical" 3.50 g mol⁻¹.
- [[2026_RoyPerez_WASP39b]] — aerosol opacities for PSG retrieval of WASP-39 b NIRSpec PRISM.
