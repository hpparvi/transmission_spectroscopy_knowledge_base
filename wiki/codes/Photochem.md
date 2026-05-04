---
type: code
aliases: [Photochem photochemistry]
tags: [photochemistry, kinetics, atmospheric-modeling]
---

# Photochem

Open-source 1D photochemistry / chemical-kinetics code (Wogan et al. 2024; not yet ingested), an alternative to [[VULCAN]] for solving time-dependent photochemistry coupled to vertical transport. Used within the [[ScCHIMERA]] self-consistent framework. Supports a comprehensive reaction network for terrestrial-like and giant-planet atmospheres.

## Papers

- [[2025_Gressier_HATP26b]] — Photochem v0.6.5 1D continuity + diffusion model on HAT-P-26 b PICASO best-fit forward grid; ~600 reactions, ~100 species (H/He/C/O/N/S; chlorine network removed); MUSCLES UV input; predicts peak SO₂ VMR ≈ 2 × 10⁻⁵ at 10⁻⁴ bar — within 1σ of the retrieved value; validates Tsai 2023 H₂S → SO₂ pathway extending to T ≈ 700 K.
- [[2026_Radica_WASP96b]] — kinetics module within ScCHIMERA self-consistent grids for WASP-96 b SO₂ photochemistry interpretation.
- [[2025_Gordon_COMPASS-G395H]] — used with [[PICASO]] for cross-checking COMPASS atmospheric grids against the [[easyCHEM]]-based primary grid in the uniform reanalysis.
- [[2025_Barat_V1298Tau-b]] — coupled to [[PICASO]] self-consistent grid for V1298 Tau b photochemistry postprocessing; explores K_zz = 10⁵–10¹⁰ cm² s⁻¹ at metallicity 0.025–100× solar, C/O 0.1–1.0, T_int 100–600 K. The CH₄ thermometer reasoning is built on the Photochem-PICASO output.
