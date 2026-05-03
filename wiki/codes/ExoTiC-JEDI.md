---
type: code
aliases: [ExoTiC-JEDI pipeline, Exoplanet Timeseries Characterisation — JWST Extraction and Diagnostic Investigator]
tags: [jwst-pipeline, data-reduction, time-series, nirspec]
---

# ExoTiC-JEDI

An end-to-end JWST time-series reduction pipeline (Alderson et al. 2022, 2023; not yet ingested. github.com/Exo-TiC/ExoTiC-JEDI), performing full extraction, reduction, and light-curve fitting from `uncal` files through to planetary spectra. Common choices: custom destriping for 1/f noise removal at the group level, custom bias subtraction, and column-by-column outlier rejection. Widely used as one of 2–3 parallel reductions in JWST NIRSpec transmission-spectroscopy papers; a standard in the COMPASS and CHAMPs workflows.

## Papers
- [[2025_Teske_TOI561b]] — cross-check reduction (alongside [[Eureka]]) for four TOI-561 b secondary eclipses.
- [[2025_Fisher_TOI1685b]] — cross-check reduction for five TOI-1685 b G395H transits.
- [[2025_Espinoza_TRAPPIST1e]] — one of three independent reductions for four TRAPPIST-1 e PRISM transits (primary: [[transitspectroscopy]]).
- [[2025_Bennett_GJ1132b]] — one of three independent reductions for the four-visit GJ 1132 b coadded spectrum.
- [[2025_Alderson_TOI-776b]] — primary reduction (alongside [[Eureka]]) for TOI-776 b.
- [[2024_Scarsdale_L98-59c]] — one of two independent reductions (alongside [[Eureka]]) for L 98-59 c COMPASS spectrum.
- [[2024_Alderson_TOI-836b]] — primary reduction (alongside [[Eureka]]) for TOI-836 b.
- [[2023_May_GJ1132b]] — one of three independent reductions for GJ 1132 b G395H data.
- [[2025_Gordon_COMPASS-G395H]] — sole pipeline for the uniform reanalysis of seven COMPASS targets; introduces the **RPF-PCA systematics model** (PCA of relative pixel fluxes, fit as a 6-vector basis) as a new default for low-groups-per-integration NIRSpec G395H observations.
