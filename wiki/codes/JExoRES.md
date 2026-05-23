---
type: code
aliases: [JExoRES pipeline]
tags: [jwst-pipeline, miri, photometric-eclipse, data-reduction]
---

# JExoRES

JWST exoplanet reduction pipeline introduced by Holmberg & Madhusudhan 2023 (not yet ingested) for time-series photometric and spectroscopic observations. Used as the primary reduction in the Hot Rocks Survey ([[JWST-GO-3730]]) MIRI F1500W eclipse photometry analyses and across the Madhusudhan-group K2-18 b series ([[JWST-GO-2722]]) covering NIRISS+NIRSpec+MIRI.

## Papers

- [[2026_Holmberg_GJ3473b]] — primary (and sole) reduction for the four MIRI F1500W secondary eclipses of GJ 3473 b.
- [[2025_Madhusudhan_K2-18b-MIRI]] — JExoRES adapted for MIRI/LRS K2-18 b transit; cross-checked with JexoPipe; agreement within 1σ throughout.
- [[2025_Luque_K2-18b]] — uses JExoRES native-resolution NIRISS+NIRSpec spectrum (from Madhusudhan 2023, not ingested) + MIRI spectrum (from [[2025_Madhusudhan_K2-18b-MIRI]]) as one of three independent reductions in panchromatic retrievals; comparator against [[exoTEDRF]], [[Eureka]], and [[SPARTA]].
- [[2025_PicaCiamarra_K2-18b]] — uses both JExoRES and JexoPipe K2-18 b MIRI spectra; agreement across pipelines determines the 11-molecule "promising" set.
