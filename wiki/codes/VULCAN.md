---
type: code
aliases: [VULCAN photochemistry]
tags: [photochemistry, kinetics, atmospheric-modeling]
---

# VULCAN

A 1D / 2D chemical-kinetics and photochemistry code for exoplanet atmospheres (Tsai et al. 2017, 2021; not yet ingested). Solves time-dependent Eulerian transport-coupled chemical kinetics with a comprehensive reaction network, used to interpret species like [[SO2]] that arise from photochemistry rather than thermochemical equilibrium. The 2D variant (Tsai 2024; not yet ingested) couples a dayside and a nightside column with horizontal advection — the framework used to interpret nightside SO₂ on WASP-17 b in [[2025_LustigYaeger_WASP17b]].

## Papers

- [[2025_LustigYaeger_WASP17b]] — 2D VULCAN simulations adapted from Tsai 2024 (two-column dayside/nightside) provide the photochemistry boundary condition for the SO₂ transport interpretation on WASP-17 b.
- [[2025_Crouzet_HATP12b]] — VULCAN photochemical kinetics with the SNCHO_PHOTO_NETWORK and a MUSCLES SED for HAT-P-12; informs the photochemistry-corrected ~10× solar metallicity for HAT-P-12 b.
- [[2025_Roy_LP791-18c]] — disequilibrium-chemistry exploration for LP 791-18 c at K_zz = 10⁴ cm² s⁻¹; the data are consistent with chemical equilibrium and require no disequilibrium signatures.
- [[2025_Crossfield_SO2shoreline]] — SNCHO chemical network with full UV photochemistry on a HAT-P-26 b fiducial atmosphere; central code for the sulfur-budget calculations driving the SO₂ shoreline. Authors flag that VULCAN's network omits some C-S bonded-species reactions (CS, CS₂ may be underestimated at cool T_eq).
- [[2025_Barat_V1298Tau-b]] — VULCAN with the SNCHO_PHOTO_NETWORK provides photochemistry within the [[ATMO]] self-consistent grid for V1298 Tau b; observed stellar spectrum from G. M. Duvvuri 2023 (not ingested). Generates two grid sub-families: (i) vertical mixing only, (ii) vertical mixing + photochemistry. Photochemistry preferred at Δχ² = 359 over vertical-mixing-only for the CO₂ feature.
