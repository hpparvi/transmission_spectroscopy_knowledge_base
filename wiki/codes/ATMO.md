---
type: code
aliases: [ATMO grid, ATMO atmosphere]
tags: [forward-model, radiative-convective, hot-jupiter, grid]
---

# ATMO

1D self-consistent radiative-convective atmosphere code and grid (Tremblin et al. 2015, 2016, 2017; Goyal et al. 2018, 2020; not yet ingested). Provides forward-model spectra spanning recirculation factor, metallicity, C/O ratio, and internal temperature for hot Jupiters. Used in [[2025_Gressier_WASP17b]] as the dayside emission grid for WASP-17 b — preferred fit at recirculation 0.5, 100× solar metallicity, C/O = 0.2.

## Papers

- [[2025_Gressier_WASP17b]] — ATMO grid (8 recirculation × 22 metallicities × 14 C/O × 4 T_int) for dayside emission interpretation.
- [[2025_Verma_HD209458b]] — used as one of four reference frameworks for SANSAR forward-model and retrieval benchmarking on WASP-96 b; absolute mean offset ~10 ppm in correlated-k mode at R ~ 1000.
- [[2025_Barat_V1298Tau-b]] — ATMO RCTE grid (5–30 M⊕ mass × 0.1–1× recirculation × 0.1–100× solar metallicity × 0.05–1.0 C/O × 200–600 K T_int) generated independently of [[PICASO]] for V1298 Tau b grid retrievals; agreement within 1σ on T_int, C/O and metallicity.
