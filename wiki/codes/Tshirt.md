---
type: code
aliases: [tshirt pipeline]
tags: [jwst-pipeline, data-reduction, time-series]
---

# Tshirt

A JWST time-series spectroscopy reduction pipeline (Schlawin & Glidic 2022; not yet ingested). Custom Stage-1 calibration with reference-pixel ROEBA correction, group-level 1/f noise subtraction (using bottom-row reference pixels), 6σ jump-step thresholds, and covariance-weighted optimal extraction (Schlawin et al. 2020; not ingested). Particularly suited to NIRCam time-series data, where group-level 1/f correction outperforms the [[Eureka]] reference-pixel method on the smaller subarray geometry; less proven on MIRI/LRS, where Eureka is preferred. Applied across the JWST NIR transmission and emission literature.

## Papers

- [[2025_Murphy_WASP107b]] — primary reduction for the NIRCam F322W2, NIRCam F444W, and NIRSpec G395H limb-resolved transits of WASP-107 b; chosen over Eureka for NIRCam to leverage Tshirt's group-level 1/f handling; cross-checked against [[Eureka]] for MIRI/LRS.
- [[2026_RoyPerez_WASP39b]] — one of six reductions applied to the WASP-39 b ERS PRISM dataset; cross-pipeline abundance variation of up to 2 dex documented.
