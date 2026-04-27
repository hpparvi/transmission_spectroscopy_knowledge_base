---
type: paper
bibkey: 2025_Redai_GJ357b
authors: [Redai, J. A., Wogan, N., Wallack, N., Alam, M., Aguichine, A., Wolfgang, A., Wakeford, H. R., Teske, J., Scarsdale, N., Moran, S., López-Morales, M., Gao, P., Gagnebin, A., Batalha, N., Batalha, N. E., Alderson, L.]
year: 2025
venue: arXiv
arxiv: 2507.07165
targets: [GJ357b]
instruments: [JWST-NIRSpec]
methods: [transmission-spectroscopy, atmospheric-retrievals]
species_detected: []
species_tentative: []
species_ruled_out: []
codes: [Tiberius, Eureka]
tags: [super-earth, m-dwarf-host, rocky-planet, jwst-go-2512, compass, null-result, featureless]
ingested: 2026-04-24
---

# JWST COMPASS: A NIRSpec G395H Transmission Spectrum of the Super-Earth GJ 357 b

**Authors:** Redai, Wogan, Wallack, Alam, Aguichine, Wolfgang, Wakeford, Teske, Scarsdale, Moran, López-Morales, Gao, Gagnebin, Batalha, Batalha, Alderson (2025, arXiv:2507.07165) · [arXiv:2507.07165]
**Target:** [[GJ357b]] · **Host:** [[GJ357]] · **Instrument:** [[JWST-NIRSpec]] (G395H, 2.87–5.14 μm)
**Program:** [[JWST-GO-2512-COMPASS]]

## TL;DR
A single JWST NIRSpec/G395H transit of the super-Earth GJ 357 b yields a **featureless transmission spectrum** from 2.87–5.14 μm with median per-point precision of 18 ppm (NRS1) / 27 ppm (NRS2). Atmospheres with mean molecular weight (MMW) < 8 g/mol are excluded at 3σ; metallicities < 300–500× solar are ruled out. Combined with the earlier NIRISS/SOSS result ([[2025_Taylor_GJ357b]]), GJ 357 b now has featureless JWST transmission spectra over the full 0.85–5.14 μm range, making it one of the most strongly wavelength-constrained rocky-planet atmospheres observed to date.

## Key findings
- Single transit observed 2023-12-04; **featureless spectrum** across both NIRSpec detectors (NRS1 and NRS2).
- **MMW < 8 g/mol excluded at 3σ** — rules out all H/He-dominated primordial atmospheres.
- **Metallicity < 300–500× solar ruled out**, depending on assumed atmospheric scenario and compositional prior.
- Two independent reductions ([[Tiberius]] primary, [[Eureka]] cross-check) yield consistent results.
- Chemical equilibrium forward models computed with `equilibrate` (Wogan et al. 2024; not yet ingested), spanning a range of C/O ratios and metallicities, all predict detectable features for the excluded parameter space.
- GJ 357's exceptional inactivity makes [[stellar-contamination]] an unlikely driver of the featureless spectrum, consistent with the assessment in [[2025_Taylor_GJ357b]].

## Methods
- **Observations:** single NIRSpec G395H transit on 2023-12-04 under JWST Cycle 1 program [[JWST-GO-2512-COMPASS]].
- **Reduction:** [[Tiberius]] as primary pipeline; [[Eureka]] as independent cross-check.
- **Retrieval:** atmospheric constraints derived via forward-model comparison and retrieval over composition space; chemical equilibrium grids generated with `equilibrate` from the Photochem package (Wogan et al. 2024; not yet ingested); nested sampling via Ultranest (Buchner 2021; not yet ingested).

## Caveats & limitations
- Single transit; repeatability not yet verified.
- The 2.87–5.14 μm NIRSpec range does not cover the near-IR water bands (1.4, 1.9 μm) probed by [[2025_Taylor_GJ357b]]; the two datasets are complementary, not redundant.
- High-metallicity secondary atmospheres (CO₂-dominated) are not excluded by either transmission dataset; a 4.3 μm CO₂ feature would be the most accessible diagnostic for future deep observations.

## Open questions / follow-ups
- Do the combined Taylor (0.85–2.8 μm) + Redai (2.87–5.14 μm) spectra allow any remaining secondary atmosphere scenarios?
- Can MIRI/LRS thermal emission provide the discriminating constraint between a bare rock and a high-metallicity CO₂ secondary atmosphere, as recommended by [[2025_Taylor_GJ357b]]?

## Related
- [[2025_Taylor_GJ357b]] — first JWST transmission spectrum of GJ 357 b (NIRISS SOSS, 0.85–2.8 μm); also featureless; provides the near-IR complement to this paper.
- [[2024_Scarsdale_L98-59c]] — COMPASS NIRSpec G395H spectrum of the sibling super-Earth L 98-59 c; same program and instrument; also featureless.
- [[2025_Alderson_TOI-776b]] — another COMPASS NIRSpec G395H result on a super-Earth; consistent null-result pattern.
