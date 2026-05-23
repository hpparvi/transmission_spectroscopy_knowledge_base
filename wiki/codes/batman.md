---
type: code
aliases: [BATMAN, batman-package]
tags: [transit-model, light-curve-fitting, utility]
---

# batman

Open-source Python implementation of the Mandel & Agol (2002) analytic transit-light-curve model (Kreidberg 2015; not ingested). The de facto standard for forward-modelling the deterministic astrophysical component of JWST and HST exoplanet transit time-series — used in the vast majority of wiki papers as the inner `transit_model` of larger reduction frameworks like [[Eureka]], [[exoTEDRF]], [[ExoTiC-JEDI]], [[FIREFLy]], and [[NAMELESS]]. Supports quadratic, four-parameter, and arbitrary-order limb-darkening; circular and Keplerian orbits; primary, secondary, and full-phase models.

## Papers
- [[2025_Splinter_WASP121b]] — Order 1 + Order 2 white-light + spectroscopic transit + eclipse + phase fitting.
- [[2026_Barat_TOI1130b]] — TESS + CHEOPS + JWST joint white-light fitting; limb-darkening from [[ExoTiC-LD]].
- [[2025_Barat_V1298Tau-b]] — single-instrument transit modelling.
- Used (often implicitly via parent pipelines) in essentially all other JWST transit papers in the wiki.
