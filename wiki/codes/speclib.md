---
type: code
aliases: [speclib]
tags: [stellar-models, interpolation, python]
---

# speclib

Python library (B. V. Rackham 2023; doi:10.5281/zenodo.7868050) providing a uniform interface to precomputed stellar-spectrum grids — notably [[SPHINX]] — with linear interpolation in T_eff, [Fe/H], and log g. Used to generate model stellar spectra for fits to JWST out-of-transit baselines in [[stellar-contamination-modeling]] workflows.

## Papers
- [[2025_Rathcke_TRAPPIST1bc]] — used to interpolate the SPHINX grid in T_eff for the 1- to 4-component photospheric fits to TRAPPIST-1's out-of-transit spectrum.
