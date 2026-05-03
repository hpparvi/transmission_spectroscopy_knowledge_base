---
type: code
aliases: [ARCiS, Atmospheric Retrieval Code in Snellius]
tags: [retrieval-code, bayesian, transmission, forward-model]
---

# ARCiS

ARCiS (Atmospheric Retrieval Code; Min et al. 2020; Ormel & Min 2019; not yet ingested) — a forward-model + Bayesian retrieval code supporting transmission and emission, with cloud condensation, line-by-line opacities (ExoMol/HITRAN k-tables), and parametric or N-point T–P profiles. Coupled to [[MultiNest]] for sampling. The primary retrieval engine of the [[JWST-GTO-1281]] ExoMIRI program.

## Papers

- [[2026_Heinke_HATP12b]] — primary retrieval code for the panchromatic information-content study of HAT-P-12 b; runs across all combinations of NIRISS+NIRSpec+MIRI+HST instruments.
- [[2025_Crouzet_HATP12b]] — primary retrieval framework for the HAT-P-12 b NIRSpec G395M paper; chemical relaxation + radiative-convective equilibrium for the P–T profile, with [[VULCAN]] photochemistry coupled in for the metallicity assessment.
