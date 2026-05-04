---
type: code
aliases: [SPARTA pipeline, Simple Planetary Atmosphere Reduction Tool for Anyone]
tags: [jwst-pipeline, data-reduction, time-series, miri-lrs, nirspec]
---

# SPARTA

An independent JWST time-series reduction pipeline (Kempton et al. 2023; not yet ingested), designed from scratch without dependency on the STScI `jwst` pipeline. Provides nonlinearity correction, dark subtraction, gain multiplication, up-the-ramp fitting with outlier rejection, background subtraction, and optimal extraction. Commonly run in parallel with [[Eureka]] as a cross-check on MIRI/LRS secondary-eclipse and NIRSpec transmission observations.

## Papers
- [[2024_Xue_GJ1132b]] — primary reduction for GJ 1132 b MIRI/LRS secondary eclipse; cross-checked against [[Eureka]].
- [[2024_WeinerMansfield_GJ486b]] — primary reduction for Gl 486 b MIRI/LRS eclipses; cross-checked against [[Eureka]].
- [[2024_Wachiraphan_LTT1445Ab]] — parallel reduction alongside [[Eureka]] for LTT 1445 A b MIRI/LRS eclipses.
- [[2025_Xue_GJ3929b]] — primary reduction for GJ 3929 b MIRI F1500W photometric eclipse time series (updated SPARTA for MIRI imaging mode).
- [[2026_Coy_HD3167b]] — primary reduction for HD 3167 b MIRI/LRS secondary eclipse; cross-checked against [[Eureka]] and [[exoTEDRF]].
- [[2025_Barat_V1298Tau-b]] — independent NIRSpec G395H pipeline cross-check vs. primary [[Eureka]] reduction on V1298 Tau b; agreement within 1σ on retrieved abundances; SPARTA shows ~25% higher scatter in NRS2 (under development for NIRSpec).
- [[2025_Deka_WASP39b]] — one of three reductions (Eureka, Tiberius, SPARTA) cross-compared on WASP-39 b MIRI data within the [[NEXOTRANS]] retrieval framework benchmark.
