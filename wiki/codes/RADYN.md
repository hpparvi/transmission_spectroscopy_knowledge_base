---
type: code
aliases: [RADYN flare model]
tags: [stellar-atmosphere, flare-modeling, radiative-hydrodynamics, m-dwarf]
---

# RADYN

1D non-LTE radiative-hydrodynamics stellar-atmosphere code (Carlsson & Stein 1995, 1997; not yet ingested) modeling chromospheric heating by non-thermal electron beams. Solves coupled radiative transfer + hydrodynamics for a stellar atmosphere parameterized by the beam flux F_e, low-energy cutoff, and power-law index δ. The grid extension by Kowalski et al. 2024 (not yet ingested) provides flare-spectrum templates suitable for matched-filter mitigation in JWST near-infrared transmission observations of M-dwarf rocky planets.

## Papers

- [[2025_Howard_TRAPPIST1_flares]] — applied to six TRAPPIST-1 flares (T_eff peaks 3000–5000 K) with a 43-model grid spanning ~10⁴ in beam parameter space; best-fit flare model has filling factor ≈ 0.46% of the stellar disk.
