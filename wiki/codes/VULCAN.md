---
type: code
aliases: [VULCAN photochemistry, VULCAN-2D]
tags: [photochemistry, kinetics, atmospheric-modeling, hub]
---

# VULCAN

A 1D / 2D chemical-kinetics and photochemistry code for exoplanet atmospheres (Tsai et al. 2017, 2021, 2024; not yet ingested). Solves time-dependent Eulerian transport-coupled chemical kinetics with comprehensive reaction networks (SNCHO and SNCHO_PHOTO_NETWORK most commonly), capturing both vertical mixing (eddy diffusion K_zz) and UV photochemistry. The dominant photochemistry code in the wiki for interpreting [[SO2]] and other photochemically-driven species — every wiki paper that detects or theoretically maps SO₂ on a hot-Jupiter or sub-Saturn target uses VULCAN. The 2D variant ([[2025_LustigYaeger_WASP17b]] adaptation of Tsai 2024) couples a dayside and a nightside column with horizontal advection.

## Variants

- **1D + SNCHO_PHOTO_NETWORK.** The standard mode. Used for HAT-P-12 b ([[2025_Crouzet_HATP12b]]), V1298 Tau b ([[2025_Barat_V1298Tau-b]]), HAT-P-26 b fiducial ([[2025_Crossfield_SO2shoreline]] core network), LP 791-18 c ([[2025_Roy_LP791-18c]]). Inputs include MUSCLES or observed stellar SEDs for UV.
- **1D as forward-grid back-end.** [[2025_Crossfield_SO2shoreline]] runs VULCAN on each of 936 (T_eq, [M/H], C/O, K_zz, T_int, XUV) parameter combinations, downstream of [[HELIOS]] T-P calculation and upstream of [[petitRADTRANS]] synthetic-spectrum generation. The grid maps the SO₂ "shoreline" at the 1 ppm contour.
- **2D dayside / nightside columns.** [[2025_LustigYaeger_WASP17b]] adapts Tsai 2024 to two columns linked by zonal-wind advection; provides the photochemistry boundary condition for the SO₂-transport interpretation of WASP-17 b nightside emission. First wiki use of 2D photochemistry on a JWST target.
- **Cross-check vs. [[Photochem]].** [[2026_Radica_WASP96b]] uses Photochem within the ScCHIMERA framework as an alternative to VULCAN — flags Photochem as an emerging competitor for sub-Neptune disequilibrium chemistry.

## History

- **2017 onwards** — original VULCAN release (Tsai 2017); rapid uptake among hot-Jupiter photochemistry communities.
- **2024** — Tsai 2024 2D extension (not yet ingested) demonstrated on hot-Jupiter day/night chemistry.
- **2025** — saturating wiki adoption: 6 ingested papers in 2025–2026 alone span hot-Jupiter dayside/nightside emission, sub-Saturn transmission, sub-Neptune temperate atmospheres, and the SO₂-shoreline grid.

## Trade-offs

- **Strength: comprehensive photochemistry network.** SNCHO_PHOTO_NETWORK handles S, N, C, H, O species with explicit UV photolysis; the standard for SO₂ formation modeling.
- **Strength: GPU-acceleration plus modest cost.** Cheap enough to run thousands of grid points ([[2025_Crossfield_SO2shoreline]] 936 models).
- **Strength: 2D capability.** Dayside-nightside coupling supported via Tsai 2024 ([[2025_LustigYaeger_WASP17b]]); useful for terminator-asymmetry and nightside chemistry.
- **Limitation: network completeness.** [[2025_Crossfield_SO2shoreline]] explicitly flags that VULCAN's network omits some C-S bonded-species reactions (CS, CS₂); abundances of those species at cool T_eq may be underestimated — relevant for sub-Saturn / Neptune-mass atmospheres where carbon-sulfur cross-coupling is non-negligible.
- **Limitation: 1D plane-parallel assumption inherent to the standard mode.** Limb-resolved photochemistry (morning vs evening) requires either the 2D mode or downstream column-by-column post-processing.
- **Limitation: no native interface to retrieval frameworks.** VULCAN is a forward-modeling code; coupling to Bayesian retrievals requires user-built tabulation or grid emulation.

## Open issues

- **Carbon-sulfur network gaps.** [[2025_Crossfield_SO2shoreline]] explicitly flags this as the principal known limitation of the SNCHO_PHOTO_NETWORK at low T_eq.
- **2D-vs-1D differences for hot-Jupiter day/night chemistry.** [[2025_LustigYaeger_WASP17b]] is the only wiki 2D-VULCAN paper; population-level testing of the 1D-vs-2D inferential difference is pending.
- **Cross-validation against [[Photochem]].** Both codes claim independent network compilation; head-to-head validation on a common test atmosphere would inform error budgets but is not yet published.

## Papers

### Hot Jupiter / sub-Saturn — primary photochemistry
- [[2025_LustigYaeger_WASP17b]] — 2D VULCAN (Tsai 2024 adaptation) provides photochemistry boundary condition for SO₂-transport interpretation on WASP-17 b nightside emission.
- [[2025_Crouzet_HATP12b]] — VULCAN with SNCHO_PHOTO_NETWORK + MUSCLES SED for HAT-P-12 b photochemistry; informs ~10× solar metallicity result.
- [[2026_Radica_WASP96b]] — uses [[Photochem]] (alternative to VULCAN) for ScCHIMERA framework on WASP-96 b.

### Sub-Neptune / temperate
- [[2025_Roy_LP791-18c]] — VULCAN at K_zz = 10⁴ cm² s⁻¹ for LP 791-18 c; data consistent with chemical equilibrium.
- [[2025_Barat_V1298Tau-b]] — VULCAN + SNCHO_PHOTO_NETWORK within ATMO grid for V1298 Tau b; photochemistry preferred at Δχ² = 359 over vertical-mixing-only for the CO₂ feature.

### Theoretical population grid
- [[2025_Crossfield_SO2shoreline]] — VULCAN on each of 936 parameter combinations to map the SO₂ shoreline; flags carbon-sulfur network gaps.
- [[2025_Ohno_GJ1214b]] — VULCAN with SNCHO + photochemistry network (571 reactions + 1142 reversed + 69 photolysis) for the photochemical-microphysical haze grid on [[GJ1214b]]. 200 vertical molecular-abundance profiles spanning [M/H] ∈ [2.0, 4.0], C/O ∈ [0.057, 1.457], and K_zz ∈ [10⁵, 10⁹] cm² s⁻¹; MUSCLES UV input. Provides chemistry input for the downstream Ohno & Okuzumi two-moment microphysical haze code.

### GEMS / metal-poor giant
- [[2025_Canas_TOI5205b]] — VULCAN photochemistry post-processed onto [[PICASO]] RCTE grids for TOI-5205 b; used to **extend the metallicity grid below the PICASO lower bound** [M/H] = −1.0; K_zz = 10⁶ or 10⁹ cm² s⁻¹; sulfur enhancements f_S = 1, 10, 100. Disequilibrium models reach χ²_ν = 2.56 (vs RCTE χ²_ν = 2.635).
