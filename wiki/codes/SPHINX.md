---
type: code
aliases: [SPHINX grid, SPHINX models]
tags: [stellar-models, m-dwarf, ultracool-dwarf, spectral-grid]
---

# SPHINX

Self-consistent grid of cool-dwarf model atmospheres and emergent spectra (A. R. Iyer et al. 2023, ApJ 944:41; not yet ingested), spanning low-mass M dwarfs into the ultracool regime. Tabulated in T_eff, [Fe/H], and log g; commonly accessed via [[speclib]] for interpolation. Lower T_eff floor of the public grid is **2000 K**, which sets an upper limit on inferred cool-component temperatures for late-M and ultracool hosts. Widely used in [[stellar-contamination-modeling]] for late M-dwarf systems where PHOENIX-grid fidelity is limited.

## Papers
- [[2025_Rathcke_TRAPPIST1bc]] — used (via [[speclib]]) for 1- to 4-component photospheric fits to TRAPPIST-1's out-of-transit JWST spectrum; the cool component pegs at the 2000 K grid floor and is therefore quoted as an upper limit.
