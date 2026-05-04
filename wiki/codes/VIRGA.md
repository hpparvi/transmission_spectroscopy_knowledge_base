---
type: code
aliases: [virga]
tags: [cloud-microphysics, aerosols, sedimentation, eddy-diffusion]
---

# VIRGA

Open-source eddy-diffusion-balanced cloud microphysics code (Rooney et al. 2022) implementing the Ackerman & Marley 2001 cloud-condensation framework. Inputs: a temperature–pressure profile and an eddy diffusion coefficient K_zz; output: vertical cloud particle distributions per condensate species. Sedimentation efficiency f_sed controls compactness — small f_sed → vertically lofted cloud decks, large f_sed → compact decks. Typically paired with [[PICASO]] for radiative-transfer post-processing.

## Papers
- [[2025_Fu_limb-asymmetry]] — used to generate the 1.5D forward-model grid of morning-vs-evening limb water-band amplitudes; three condensate species (Na₂S, MnS, MgSiO₃); fixed K_zz = 10¹⁰ cm² s⁻¹; fitted slope between morning and evening limb T(P) profiles plus log f_sed and the MgSiO₃ shutoff temperature.
