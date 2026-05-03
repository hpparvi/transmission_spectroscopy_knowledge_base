---
type: paper
bibkey: 2025_Gordon_COMPASS-G395H
authors: [Gordon, T. A., Batalha, N. M., Batalha, N. E., Aguichine, A., Gagnebin, A., Kirk, J., Lopez-Morales, M., Meech, A., Scarsdale, N., Teske, J., Wallack, N. L., Wogan, N.]
year: 2025
venue: arXiv:2511.18196
arxiv: 2511.18196
targets: [GJ357b, TOI-836b, TOI-836c, TOI-776b, TOI-776c, L98-59c, L168-9b]
instruments: [JWST-NIRSpec]
methods: [transmission-spectroscopy, multi-visit-stacking]
codes: [ExoTiC-JEDI, PICASO, easyCHEM, Photochem, petitRADTRANS, ultranest]
tags: [compass, methodology, systematics, reanalysis, reduction-systematics, nrs-detector-offsets]
ingested: 2026-05-03
---

# JWST COMPASS: Insights into the Systematic Noise Properties of NIRSpec/G395H From a Uniform Reanalysis of Seven Transmission Spectra

**Authors:** Gordon, Batalha (N. M.), Batalha (N. E.), Aguichine, Gagnebin, Kirk, Lopez-Morales, Meech, Scarsdale, Teske, Wallack, Wogan (full author list — only 12 authors total) · 2025, arXiv:2511.18196
**Targets:** [[GJ357b]], [[TOI-836b]], [[TOI-836c]], [[TOI-776b]], [[TOI-776c]], [[L98-59c]], [[L168-9b]] · **Instrument:** [[JWST-NIRSpec]] (G395H BOTS, NRS1+NRS2)
**Program:** [[JWST-GO-2512-COMPASS]] (PI: N. E. Batalha)

## TL;DR

A **uniform [[ExoTiC-JEDI]] re-reduction and re-fit** of the first seven [[JWST-GO-2512-COMPASS]] NIRSpec/G395H transmission spectra. Introduces a **PCA-of-relative-pixel-fluxes (RPF) systematics model** that captures trace-shape variations (shifting, de-focusing, rotation, alternating-column noise, residual 1/f) and is strongly preferred for low-groups-per-integration observations. Finds NIRSpec G395H systematics are strongest in **NRS1 between 2.8–3.5 μm**, that PandExo under-predicts real error bars by **~5% (NRS1) / ~12% (NRS2)** on average (rising to 13% / 18% with the 6-vector model), and that all seven flat spectra remain flat with metallicity lower limits of several hundred × solar. Co-adding super-Earth or sub-Neptune subsets yields no compelling shared features.

## Key findings

- **Five sources of detector systematics identified:** (1) trace shifting, (2) de-focusing, (3) rotation, (4) alternating column noise (ACN), (5) residual 1/f noise.
- **6-vector RPF model strongly preferred** for 3-group observations ([[GJ357b]], [[TOI-836b]], [[TOI-836c]]); marginally preferred or unnecessary for 4- and 7-group observations.
- **PandExo under-prediction** of achieved precision: 5% (NRS1) / 12% (NRS2) on average; rising to 13% / 18% with the 6-vector model.
- **Systematics dominantly in NRS1 between 2.8–3.5 μm.**
- **Oscillations at 3.4 and 3.63 minutes** attributed to ISIM Electronics Compartment heater thermal cycling (Rigby 2024; not yet ingested).
- **Flat spectra for all seven targets;** metallicity lower limits of several hundred × solar (clear-atmosphere); composite super-Earth and sub-Neptune coadded spectra are also flat.
- **NRS1/NRS2 transit-depth offsets statistically significant** for [[TOI-836c]], [[GJ357b]], [[TOI-776b]], [[TOI-776c]] — quantifies the offset that previous wiki COMPASS papers have flagged per-target.

## Methods

- **Reduction:** Uniform [[ExoTiC-JEDI]] reduction with custom group-level destriping (Alderson et al. 2024).
- **RPF-PCA systematics model:** PCA of relative pixel fluxes (per-pixel flux normalized by frame total) yields basis vectors tracking trace shape/position; fit as a linear combination of the first 6 components plus a linear-in-time trend ("6-vector model"), compared to a 0-vector (linear only) and a shifts-only baseline (x/y trace positions, à la Rustamkulov 2022; not yet ingested).
- **Light curves:** Custom MCMC; ExoTiC-LD limb darkening with MPS-ATLAS-1.
- **Atmospheric grids:** [[PICASO]] + [[easyCHEM]] (this work) and [[PICASO]] + [[Photochem]] (cross-check vs prior COMPASS papers); MCMC sampling via `ultranest`; [[petitRADTRANS]] for cross-target model spectra.
- **Noise prediction reference:** PandExo + Pandeia.

## Caveats & limitations

- **Flat spectra preclude composition determination** — only lower limits.
- **Higher-order trace-morphology changes** beyond positional shifts may inject spurious features in the 2.8–3.5 μm range, especially for low-group observations.
- **RPF method assumes correlated noise lives in the pixel-flux PCA basis** — validated against ICA, found equivalent.

## Open questions / follow-ups

- Will the RPF-PCA framework recover any feature significance on the four COMPASS targets not yet uniformly reanalyzed?
- Is the per-target NRS1/NRS2 offset modeled satisfactorily by the 6-vector basis, or does it represent a separate calibration product the JWST team should deliver?
- How does the noise floor compare on PRISM and G395M observations?

## Tensions

- **None new with prior COMPASS papers** — the uniform reanalysis broadly reproduces the per-target conclusions of [[2024_Alderson_TOI-836b]], [[2024_Scarsdale_L98-59c]], [[2025_Alderson_TOI-776b]], [[2025_Teske_TOI776c]], [[2025_Redai_GJ357b]], plus the L 168-9 b spectrum re-derived here. PandExo under-prediction quantifies an existing systematics theme.

## Related

- [[2025_Connors_MIRI-15um]] — analogous uniform reanalysis methodology applied to MIRI F1500W eclipses (FN-PCA via the [[Erebus]] pipeline); both papers prepare the community for survey-scale work.
- [[2026_RoyPerez_WASP39b]] — pipeline-driven retrieval-parameter variation up to 2 dex on the same WASP-39 b ERS PRISM data; the systematics theme generalizes from per-pipeline to per-target scope here.
- [[2024_Alderson_TOI-836b]], [[2024_Scarsdale_L98-59c]], [[2025_Alderson_TOI-776b]], [[2025_Teske_TOI776c]], [[2025_Redai_GJ357b]] — the original per-target COMPASS papers reanalyzed here; conclusions broadly preserved.
