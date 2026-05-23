---
type: code
aliases: [Planetary Spectrum Generator]
tags: [retrieval, radiative-transfer, spectral-modeling]
---

# PSG

The Planetary Spectrum Generator (Villanueva et al. 2018; NASA GSFC), a web-based and API-accessible radiative-transfer and spectral-modeling tool for planetary atmospheres. Supports a broad wavelength range (UV to radio) and a variety of atmospheric configurations (transmission, emission, reflection). Used in [[2026_RoyPerez_WASP39b]] as the atmospheric retrieval forward-model engine for WASP-39 b, coupled with [[MultiNest]] sampling and [[MOPSMAP]] aerosol opacities.

## Papers

- [[2025_RoyPerez_WASP39b]] — PSG/PUMAS forward-model engine for cloud-extinction-parameterization analysis on WASP-39 b NIRSpec PRISM (FIREFLy reduction). Demonstrates strong evidence for non-flat cloud opacity (Ångström ln B = 8.02; MOPSMAP ln B = 5.57 over flat); best-fit aerosol r_eff = 0.55 μm; molecular abundance shifts up to 4 dex (H₂S) depending on cloud parameterization.
- [[2026_RoyPerez_WASP39b]] — forward-model engine for six-pipeline retrieval comparison on WASP-39 b NIRSpec PRISM (data-reduction-systematics angle).
