---
type: code
aliases: [juliet]
tags: [light-curve-fitting, transit-fitting, python, mcmc, nested-sampling]
---

# juliet

Python light-curve and radial-velocity fitting package (Espinoza et al. 2019, MNRAS 490:2262) providing a unified interface to BATMAN (transit models), radvel (RV models), nested sampling via dynesty or MultiNest, and MCMC via emcee. Supports Gaussian-process detrending via george or celerite. Widely used for JWST transit light-curve fitting in conjunction with various reduction pipelines.

## Papers
- [[2025_Espinoza_TRAPPIST1e]] — light-curve fitting for four TRAPPIST-1 e PRISM transits; GP detrending via celerite with per-visit amplitude and timescale parameters.
- [[2025_Fisher_TOI1685b]] — light-curve fitting for five TOI-1685 b G395H transits; GP detrending for the Sep 1 visit quasi-sinusoidal systematics.
- [[2025_Taylor_GJ357b]] — light-curve fitting for the GJ 357 b NIRISS/SOSS transit (BATMAN model, Kipping 2013 limb-darkening reparameterization, linear + PCA systematics).
- [[2024_Gressier_L98-59d]] — light-curve fitting for the L 98-59 d NIRSpec/G395H transit; paired with dynesty nested sampling and Matérn-3/2 GP detrending via george.
- [[2025_Xue_GJ3929b]] — joint transit + RV fitting for GJ 3929 b eclipse photometry and MAROON-X radial velocities.
- [[2025_Gressier_WASP17b]] — light-curve fitting for the WASP-17 b NIRISS/SOSS secondary eclipse with Matérn-3/2 GP detrending.
- [[2026_Radica_WASP96b]] — light-curve fitting for the WASP-96 b NIRSpec G395H transit (alongside exoUPRF).
- [[2026_Heinke_HATP12b]] — light-curve fitting for the HAT-P-12 b NIRISS/SOSS transit; dynesty sampler.
