---
type: code
aliases: [Exotic-LD, ExoTiC LD, exotic-ld]
tags: [limb-darkening, stellar-models, utility]
---

# ExoTiC-LD

Stellar limb-darkening parameter calculator (Grant & Wakeford 2024; not ingested). Interpolates pre-computed limb-darkening tables from multiple stellar-atmosphere grids (e.g. MPS-ATLAS, Stagger, 3D-CO5BOLD) to a given JWST or HST instrument response, returning quadratic or four-parameter LD coefficients ready for use in [[batman]] or other transit-modelling backends. The de facto LD calculator across the JWST pipelines and used as a prior in essentially all wiki papers that fit limb-darkening parameters; alternative is `ExoTETHyS`.

## Papers
- [[2026_Batalha_LTT1445Ab]] — MPS-ATLAS quadratic LD priors for the COMPASS LTT 1445A b NIRSpec G395H spectroscopic fits.
- [[2026_Barat_TOI1130b]] — quadratic LD coefficients fixed from ExoTiC-LD for NIRSpec G395H + NIRISS SOSS + TESS + CHEOPS transit fitting.
- [[2025_Barat_V1298Tau-b]] — same use case.
- Often invoked via parent reduction pipelines (e.g. [[Eureka]], [[ExoTiC-JEDI]]) in many other wiki papers.
