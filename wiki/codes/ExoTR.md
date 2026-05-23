---
type: code
aliases: [ExoTR retrieval, Exoplanetary Transmission Retrieval]
tags: [retrieval-code, bayesian, transmission, stellar-contamination, sub-neptune, rocky-planet]
---

# ExoTR

**Exoplanetary Transmission Retrieval** — a fully-Bayesian transmission-spectrum retrieval code developed by M. Damiano (Damiano et al. 2024; not ingested). Distinctive features:
- **Cloud as water VMR profile** — clouds modeled as an optically thick surface or via non-uniform water-mixing-ratio profile, similar to ExoReL^R (Hu 2019; Damiano & Hu 2020, 2022; not ingested).
- **Stellar heterogeneity jointly fit** — TLS effect parameterization following Rackham et al. 2018 (= [[2018_Rackham_TLS]]; via fractional spot/faculae coverage + temperature).
- **Centered-log-ratio (CLR) abundance space** — allows any trace gas to become the background gas; agnostic to bulk atmospheric composition (Benneke & Seager 2012; not ingested).
- **Photochemical haze with prescribed optical constants** + free particle size (to be described in Tokadjian et al. 2025, in preparation; not ingested).

Sampling via [[MultiNest]] / pymultinest. Typically 800 live points; convergence tolerance 0.5.

## Papers

- [[2025_BelloArufe_L98-59b]] — primary retrieval engine for the [[L98-59b]] [[volcanic-atmosphere]] inference. 14-parameter model spanning T_iso, cloud-top P, R_p, 3 detector offsets, 5 CLR-prior gas abundances, heterogeneity fraction + temperature, stellar T_eff. Cross-validated against [[Aurora]] and [[POSEIDON]]; all three agree on the SO₂-rich atmosphere preference at 3.3–3.8σ.
- [[2025_LibbyRoberts_Kepler51d]] — used as one of two retrieval codes for the [[Kepler-51d]] [[super-puff]] sloped-spectrum analysis.
