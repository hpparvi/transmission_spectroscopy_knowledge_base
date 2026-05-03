---
type: code
aliases: [TEATRO pipeline]
tags: [jwst-pipeline, data-reduction, nirspec]
---

# TEATRO

JWST NIRSpec time-series reduction pipeline used as an alternate reduction in the [[JWST-GTO-1281]] ExoMIRI program. The choice of TEATRO vs. [[CASCADe]] noticeably shifts retrieved C/O values on HAT-P-12 b — a documented case of pipeline-induced systematics in the small-amplitude-feature regime.

## Papers

- [[2026_Heinke_HATP12b]] — alternate NIRSpec G395M reduction (vs. primary [[CASCADe]]); recovers H₂S at ~3.7σ (vs CASCADe's H₂S only with NIRISS+MIRI added); shifts retrieved C/O.
- [[2025_Crouzet_HATP12b]] — primary NIRSpec G395M reduction for the HAT-P-12 b paper (jwst pipeline 1.10.2); paired with [[CASCADe]] for cross-check.
