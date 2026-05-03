---
type: code
aliases: [CASCADe, Calibration of trAnsit Spectroscopy using CAusal Data]
tags: [jwst-pipeline, hst-pipeline, data-reduction, time-series, nirspec, miri]
---

# CASCADe

CASCADe (Calibration of trAnsit Spectroscopy using CAusal Data; Carone et al. 2021; Crouzet et al. 2025; Bouwman et al. in prep; all not yet ingested) — Python pipeline applying causal regression for time-series systematics removal across HST and JWST NIRSpec / MIRI / STIS observations. The standard reduction for the [[JWST-GTO-1281]] ExoMIRI program.

## Papers

- [[2026_Heinke_HATP12b]] — primary NIRSpec G395M, MIRI/LRS, and HST/STIS reductions for the panchromatic HAT-P-12 b information-content analysis; cross-checked against [[TEATRO]] for NIRSpec.
- [[2025_Crouzet_HATP12b]] — alternate NIRSpec G395M reduction for HAT-P-12 b (vs primary [[TEATRO]]); the CASCADe-only marginal 3.2σ H₂S detection is absent in TEATRO — pipeline-dependent.
