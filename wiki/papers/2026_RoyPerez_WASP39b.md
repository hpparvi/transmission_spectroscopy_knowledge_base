---
type: paper
bibkey: 2026_RoyPerez_WASP39b
authors: [Roy-Perez, A., et al.]
year: 2026
venue: A&A 707:A297
doi: 10.1051/0004-6361/202558193
targets: [WASP-39b]
instruments: [JWST-NIRSpec]
methods: [atmospheric-retrievals]
species_detected: [Na, K, H2O, CO2, CO, SO2]
species_tentative: [H2S]
codes: [FIREFLy, Tshirt, Tiberius, Eureka, PSG, MultiNest, MOPSMAP]
tags: [hot-jupiter, systematics, data-reduction, retrieval-uncertainty, jwst-ers]
ingested: 2026-04-27
---

# The effect of JWST/NIRSpec data reduction on the retrieval of WASP-39b atmospheric properties

**Authors:** Roy-Perez, A., et al. (2026, A&A 707:A297) · DOI: 10.1051/0004-6361/202558193
**Targets:** [[WASP-39b]] · **Instrument:** [[JWST-NIRSpec]] (PRISM)

## TL;DR

A methodological systematics study applying four independent reduction pipelines ([[FIREFLy]], [[Tshirt]], [[Tiberius]], [[Eureka]]) to the same JWST NIRSpec PRISM observation of WASP-39b from the ERS program ([[JWST-ERS-1366]]; 2022 July 10). Retrieved atmospheric parameters — including molecular abundances, temperature, and gravity — vary by up to 2 dex (two orders of magnitude) depending purely on which data reduction choices are made. All species detected from the ERS analysis are recovered (Na, K, H₂O, CO₂, CO, SO₂), and H₂S is tentative. The paper is a cautionary demonstration that data reduction is not a neutral step: pipeline choices propagate into the science.

## Key findings

- Retrieved abundances, T–P profiles, and surface gravity posterior widths differ by up to 2 dex across six independent reductions of the same PRISM dataset.
- Na, K, H₂O, CO₂, CO, and SO₂ are detected across all or most pipelines, confirming the canonical ERS detections.
- H₂S is tentatively detected in some reductions but not all — a species whose reality depends on reduction.
- Retrieval performed with [[PSG]] + [[MultiNest]]; aerosol opacity via [[MOPSMAP]].
- Highlights that the 1/f noise treatment, background subtraction, and spectral extraction choices are the dominant sources of pipeline-to-pipeline variation.
- Makes the case for standardized data reduction reporting (e.g., spectral covariance matrices, full pipeline descriptions) to enable cross-study comparisons.

## Methods

The ERS PRISM transit observation (Program [[JWST-ERS-1366]]; PI: Batalha) from 2022 July 10 is reduced through six independent reductions spanning four pipelines: [[FIREFLy]], [[Tshirt]] (new pipeline introduced in this work), [[Tiberius]], and [[Eureka]] + ExoTEP (plus a Carter reduction). The resulting transmission spectra feed into [[PSG]] (Planetary Spectrum Generator) atmospheric retrievals using [[MultiNest]] as the sampler. Aerosol optical properties computed with [[MOPSMAP]] (Mie scattering). The study isolates which reduction stages produce the greatest inter-pipeline divergence.

## Caveats & limitations

- Restricted to the PRISM mode and one observing epoch; G395H and G235H ERS spectra are not analyzed here.
- Focus is on reduction-induced variation; instrumental systematics common to all pipelines (e.g., detector nonlinearity) are not independently quantified.
- Retrieval framework (PSG + MultiNest) is held fixed; retrieval-model variation is not studied.

## Open questions / follow-ups

- How much of the 2 dex retrieval variance reduces when pipelines align on 1/f noise treatment?
- Do similar-magnitude pipeline effects appear for smaller, cooler targets where S/N is lower?
- What community standards for data reporting would be sufficient to enable reproducibility?

## Related

- [[2023_May_GJ1132b]] — a cautionary tale from NIRSpec G395H: two visits with three reductions yielded discrepant spectra on a fainter target; reduction systematics flagged as a primary concern.
- [[2023_Moran_GJ486b]] — three-reduction NIRSpec G395H comparison; feature significance varied 2.2σ–3.3σ across reductions.
- [[2025_Teske_TOI776c]] — explicitly shows that MMW inferences from featureless spectra vary by 2.8–7.7 g mol⁻¹ depending on whether equilibrium or mixture models are used; retrieval-model analogue of the pipeline-variation result here.
