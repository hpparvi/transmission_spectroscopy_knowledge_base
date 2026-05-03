---
type: code
aliases: [NEMESISPy, NEMESIS Python, NEMESISpy]
tags: [retrieval-code, bayesian, optimal-estimation, transmission]
---

# NEMESISPY

Python implementation of the NEMESIS optimal-estimation atmospheric retrieval framework (Yang et al. 2024; not yet ingested), originating from the radiative-transfer tradition for solar-system atmospheres (Irwin et al. 2008). Supports free-chemistry retrievals, chemical-equilibrium retrievals via [[FastChem]], and centred-log-ratio (CLR) priors that handle ratio constraints between major species.

## Papers

- [[2024_Banerjee_L98-59d]] — primary retrieval code for the L 98-59 d transmission spectrum; CLR priors over H₂O, H₂S, SO₂, CO₂, etc.; sulfur-rich atmosphere preferred.
- [[2026_Radica_WASP96b]] — one of four free-chemistry frameworks cross-compared on WASP-96 b; also used in chemical-equilibrium mode (with [[FastChem]]) for the metallicity / C/O determination.
