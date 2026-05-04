---
type: code
aliases: [HELIOS-K opacity code]
tags: [opacity-calculation, atmospheric-modeling, gpu-accelerated]
---

# HELIOS-K

GPU-accelerated opacity calculation code (Grimm & Heng 2015; Grimm et al. 2021; not yet ingested) for computing molecular and atomic absorption cross-sections from line-list databases (HITRAN, ExoMol, HITEMP). Used as the opacity backend for the Bern atmospheric modeling stack — notably the [[BeAR]] retrieval framework — and accessible via the DACE platform (dace.unige.ch) for community use.

## Papers

- [[2025_Felix_TOI-270d]] — opacity backend for BeAR retrievals on TOI-270 d; line lists primarily from ExoMol (Tennyson et al. 2024) plus HITRAN CIA; cross-section grid for CH₄, CO₂, H₂O, CO, NH₃, CS₂, plus exotic species (CH₃Cl, CH₃F, H₂CS, OCS) from limited measured cross-sections.
