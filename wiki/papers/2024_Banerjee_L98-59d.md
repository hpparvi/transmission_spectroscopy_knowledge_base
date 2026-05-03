---
type: paper
bibkey: 2024_Banerjee_L98-59d
authors: [Banerjee, A., Barstow, J. K., Gressier, A., Espinoza, N., Sing, D. K., Allen, N. H., Birkmann, S. M., Challener, R. C., Crouzet, N., Haswell, C. A., Lewis, N. K., Lewis, S. R., Yang, J.]
year: 2024
venue: ApJL
doi: 10.3847/2041-8213/ad73d0
targets: [L98-59d]
instruments: [JWST-NIRSpec]
methods: [transmission-spectroscopy, atmospheric-retrievals, stellar-contamination-modeling]
species_detected: []
species_tentative: [H2S, SO2]
species_ruled_out: []
codes: [transitspectroscopy, FIREFLy]
tags: [super-earth, m-dwarf-host, rocky-planet, jwst-gto-1224, secondary-atmosphere, sulfur-species, multi-planet-system]
ingested: 2026-04-23
---

# Atmospheric Retrievals Suggest the Presence of a Secondary Atmosphere and Possible Sulfur Species on L 98-59 d from JWST NIRSpec G395H Transmission Spectroscopy

**Authors:** Banerjee, Barstow, Gressier, Espinoza, Sing, et al. (2024, ApJL 975:L11) · [doi:10.3847/2041-8213/ad73d0]
**Target:** [[L98-59d]] · **Host:** [[L98-59]] · **Instrument:** [[JWST-NIRSpec]] (G395H, 2.9–5.2 μm)
**Program:** [[JWST-GTO-1224]]

## TL;DR
[[atmospheric-retrievals]] on a single JWST NIRSpec/G395H transit of the super-Earth L 98-59 d (Teq=416 K, Rp=1.58 R⊕) favor a **high-MMW secondary atmosphere containing [[H2S]] and [[SO2]]** over either a flat line or a pure [[stellar-contamination]] model. Log volume mixing ratios are log X(H₂S) ≈ −0.62 and log X(SO₂) ≈ −2.35; the combined sulfur detection significance is ~2σ, with the atmosphere+stellar model preferred at 2.24σ over stellar-only and 3.50σ over a flat-line-with-offset. If confirmed, the sulfur species hint at **active volcanism** on this tidally heated planet. A companion paper ([[2024_Gressier_L98-59d]] — "Paper I") independently analyzes the same transit with different pipelines and retrieval codes.

## Key findings
- Preferred retrieval is "Stellar + Atmosphere": unocculted faculae (ΔT_het ≈ +324 K) *plus* [[H2S]] + [[SO2]] absorption.
- **High-MMW atmosphere** (~10 g mol⁻¹) inferred; an equilibrium-chemistry retrieval is rejected at 3.8σ relative to free chemistry → the atmosphere is not in equilibrium.
- Stellar-only scenarios (no atmosphere) cannot reproduce the ~3.3 μm and ~4.4 μm features in the spectrum.
- Retrievals without H₂S or SO₂ as active gases produce much worse fits, confirming these species drive the observed features.
- Individual detection significances of H₂S and SO₂ ~2σ each — weak but consistent.
- Equilibrium-chemistry retrieval also favors sulfur enrichment (retrieved Z/Z☉ ≈ 467, C/O ≈ 0.58, S/O ≈ 1.16).
- Consistent results across `transitspectroscopy` (primary) and [[FIREFLy]] (cross-check) reductions.

## Methods
- **Observations:** single NIRSpec/G395H transit of L 98-59 d on 2023-06-25 from [[JWST-GTO-1224]] (PI Birkmann).
- **Reduction:** [[transitspectroscopy]] (Espinoza 2022; not yet ingested) primary + [[FIREFLy]] cross-check.
- **Retrieval:** [[NEMESISPY]] with CLR (centered-log-ratio) priors for 8 gases (H₂O, CO₂, CO, NH₃, PH₃, CH₄, H₂S, SO₂) + N₂ continuum; PyMultiNest sampler with 2000 live points.
- **Stellar contamination:** three-parameter model (f_het, ΔT_het, T_phot) using PHOENIX stellar grids; see [[stellar-contamination-modeling]].
- **Scenarios tested:** Stellar+Atmosphere (preferred), Atmosphere Only, Stellar Only (rejected), Offset Stellar Only, Equilibrium chemistry ([[NEMESISPY]]+[[FastChem]]), No-H₂S/SO₂, Nitrogen-background, NRS2 offset.

## Caveats & limitations
- Single transit only; reproducibility untested within this paper (Cycle 2 GO 4098 + NIRISS SOSS GTO 1201 follow-ups were accepted at time of writing).
- L 98-59 d has a high impact parameter → transit chord close to the limb; limb-darkening coefficients are hard to pin down.
- Individual H₂S / SO₂ significance ~2σ; the overall atmospheric preference rests on joint opacity patterns, not either species alone.
- Retrieval assumes isothermal T–P; the spectrum probes too narrow a pressure range for a gradient to be statistically preferred.

## Open questions / follow-ups
- Do the sulfur species survive additional JWST transits (GO 4098 G395H, GTO 1201 NIRISS SOSS)?
- Can the 7–10 μm SO₂ band (inaccessible here) be observed with MIRI/LRS? The paper highlights MIRI as particularly decisive for SO₂ confirmation.
- Is the sulfur from active volcanism (L 98-59 d is potentially tidally heated, Io-like), outgassing from a magma ocean, or photochemistry from H₂O?

## Tensions
- Broadly consistent with [[2024_Gressier_L98-59d]] (companion "Paper I"); both favor H₂S/SO₂-driven atmospheric models, but differ in quantitative significance (Gressier: 2.6σ–5.6σ depending on reduction + retrieval; [[TauREX3]] and exoretrievals rather than [[NEMESISPY]]). Treat as a methodology cross-check, not a disagreement.

## Related
- [[2024_Gressier_L98-59d]] — companion "Paper I" on the same transit; independent retrieval agrees on the sulfur-species interpretation.
- [[2024_Scarsdale_L98-59c]] — JWST COMPASS on sibling [[L98-59c]]; featureless, in contrast to L 98-59 d's sulfur hints.
- Seligman et al. 2024 (not yet ingested) — predicted L 98-59 d as a sulfur-detection target.
- Demangeon et al. 2021 (not yet ingested) — source of L 98-59 system parameters.
- Zhou et al. 2023 (not yet ingested) — prior HST/WFC3 featureless spectrum of L 98-59 d.
