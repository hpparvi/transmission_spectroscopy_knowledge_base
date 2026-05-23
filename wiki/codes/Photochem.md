---
type: code
aliases: [Photochem photochemistry, Photochem-Clima]
tags: [photochemistry, kinetics, atmospheric-modeling, climate-coupling, hub]
---

# Photochem

Open-source 1D photochemistry / chemical-kinetics code (Wogan et al. 2023, 2024, 2025a, 2026; all not ingested) supporting time-dependent gas-phase chemistry coupled to vertical transport, plus a 1.5-D climate sub-module (`Clima`) for radiative–convective equilibrium calculations. The combined Photochem + Clima package is the engine behind the wiki's first [[climate-constrained-inversion]] (introduced in [[2026_Wogan_LTT1445Ab]]) and is increasingly the standard alternative to [[VULCAN]] for sub-Neptune and rocky-planet disequilibrium modelling — also used within the [[ScCHIMERA]] self-consistent framework. Comprehensive reaction network spanning rocky-planet (CO₂ / H₂O / O₂ / SO₂ dominant) to giant-planet (H/He / hydrocarbon / sulfur) atmospheres.

## Family

- **Photochem (gas-phase kinetics)** — the photochemistry module proper.
- **Clima (1.5-D radiative-convective)** — climate sub-module producing self-consistent P–T profiles + heat-redistribution parameterization (Koll 2022 not ingested).
- **Resampled opacity database** — companion Zenodo product (Wogan 2025b; not ingested) for [[PICASO]] interoperability.

## Common usage patterns

- **Self-consistent disequilibrium chemistry**: Photochem post-processing of [[PICASO]] RCTE grids for sub-Neptune sulfur photochemistry (e.g. [[2025_Mukherjee_GJ436b]], [[2025_Barat_V1298Tau-b]], [[2025_Gressier_HATP26b]]).
- **Climate-constrained inversion**: Clima + PICASO + [[MultiNest]] for rocky-planet eclipse-spectrum surface-pressure constraints ([[2026_Wogan_LTT1445Ab]]; see [[climate-constrained-inversion]]).
- **Population-level SO₂ modelling**: Photochem coupled to PICASO RCTE grids across (T_eq, [M/H]) space for [[SO2-photochemical-shoreline]] empirical tests ([[2025_Fu_statistical-trends]]).
- **Chemically-consistent retrievals**: Photochem inside [[CHIMERA]] forward models for thick-aerosol sub-Neptunes ([[2025_Ohno_GJ1214b]]).

## Papers

- [[2025_Gressier_HATP26b]] — Photochem v0.6.5 1D continuity + diffusion model on HAT-P-26 b PICASO best-fit forward grid; ~600 reactions, ~100 species (H/He/C/O/N/S; chlorine network removed); MUSCLES UV input; predicts peak SO₂ VMR ≈ 2 × 10⁻⁵ at 10⁻⁴ bar — within 1σ of the retrieved value; validates Tsai 2023 H₂S → SO₂ pathway extending to T ≈ 700 K.
- [[2026_Radica_WASP96b]] — kinetics module within ScCHIMERA self-consistent grids for WASP-96 b SO₂ photochemistry interpretation.
- [[2025_Gordon_COMPASS-G395H]] — used with [[PICASO]] for cross-checking COMPASS atmospheric grids against the [[easyCHEM]]-based primary grid in the uniform reanalysis.
- [[2025_Barat_V1298Tau-b]] — coupled to [[PICASO]] self-consistent grid for V1298 Tau b photochemistry postprocessing; explores K_zz = 10⁵–10¹⁰ cm² s⁻¹ at metallicity 0.025–100× solar, C/O 0.1–1.0, T_int 100–600 K. The CH₄ thermometer reasoning is built on the Photochem-PICASO output.
- [[2025_Mukherjee_GJ436b]] — coupled to [[PICASO]] RCTE grid for GJ 436 b disequilibrium-chemistry post-processing; 2700 × 3 K_zz (10⁶, 10⁸, 10¹⁰ cm² s⁻¹) = 8100 disequilibrium models. The disequilibrium-chemistry inference allows lower atmospheric metallicity (≥80× solar at 2σ) than the equilibrium-chemistry models require (≥300× solar at 1σ).
- [[2025_Fu_statistical-trends]] — Photochem (Wogan et al. 2023) coupled to PICASO RCTE TP profiles for population-level SO₂ photochemistry modeling. Constant K_zz = 10¹⁰ cm² s⁻¹; provides the theoretical SO₂-VMR map that the SO₂-L empirical population indices are compared against.
- [[2025_Ohno_GJ1214b]] — Photochem (Wogan 2024) coupled to [[PICASO]] in the chemically-consistent retrieval cross-check on GJ 1214 b; yields [M/H] = 3.48⁺⁰·⁴²₋₀·³⁶ in agreement with the PM-haze grid result.
