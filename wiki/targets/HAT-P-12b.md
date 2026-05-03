---
type: target
kind: planet
class: gas-giant
host_star: HAT-P-12
mass_mjup: 0.21
radius_rjup: 0.95
period_days: 3.21305751
teq_k: 960
discovery_year: 2009
tags: [warm-sub-saturn, inflated, k-dwarf-host, low-density]
---

# HAT-P-12 b

Warm low-density sub-Saturn (Mp ≈ 0.21 MJ, Rp ≈ 0.95 RJ, Teq ≈ 960 K, ρ ≈ 0.3 g cm⁻³) on a 3.21-day orbit around the K4/K5V star [[HAT-P-12]] (Hartman et al. 2009; not yet ingested). Targeted by the [[JWST-GTO-1281]] ExoMIRI program with a coordinated NIRISS/SOSS + NIRSpec G395M + MIRI/LRS sequence; the foundational JWST/NIRSpec G395M paper is [[2025_Crouzet_HATP12b]] and the panchromatic information-content companion is [[2026_Heinke_HATP12b]].

## Atmospheric composition

- **Detected** (cross-paper consensus): [[H2O]], [[CO2]], [[CO]], [[H2S]] at ≥3σ.
  - CO₂ at 12.2σ via NIRSpec G395M alone ([[2025_Crouzet_HATP12b]]); >10σ in panchromatic ([[2026_Heinke_HATP12b]]).
  - H₂O at 6.0σ via NIRSpec G395M; >12σ once NIRISS is added.
  - CO at 4.1σ via NIRSpec G395M; ~8σ when MIRI is added.
  - H₂S at 3.7σ in TEATRO reduction (panchromatic); 3.2σ in CASCADe NIRSpec-only; absent in TEATRO NIRSpec-only — pipeline-dependent.
- **Non-detections:** [[CH4]], SO₂, NH₃, PH₃, HCN — only upper limits across both papers.
- **Atmospheric T at terminator:** 490 +75/−60 K ([[2025_Crouzet_HATP12b]]) — cold upper atmosphere.
- **Metallicity:** **10× solar (Saturn-like)** when ARCiS photochemistry is included; ~60× solar without photochemistry ([[2025_Crouzet_HATP12b]]). Multi-instrument retrievals give 11–15× solar ([[2026_Heinke_HATP12b]]) — the two values are broadly compatible if photochemistry is treated.
- **C/O:** sub-stellar to stellar; sensitive to NIRSpec reduction choice (CASCADe vs TEATRO).
- **Cloud:** non-gray cloud preferred at >7.5σ when NIRISS is included ([[2026_Heinke_HATP12b]]); 4.6σ from NIRSpec G395M alone ([[2025_Crouzet_HATP12b]] TEATRO); cloud-top pressure < 10⁻³·⁶ bar.

## Tensions

- **Metallicity 10× vs 60× solar** depending on whether photochemistry is included in the [[ARCiS]] retrieval ([[2025_Crouzet_HATP12b]]) — methodological tension highlighted by the paper itself.
- **CASCADe vs TEATRO reduction** shifts retrieved C/O and the H₂S detection significance ([[2025_Crouzet_HATP12b]], [[2026_Heinke_HATP12b]]).

## See also

- Host: [[HAT-P-12]]
- Papers: [[2026_Heinke_HATP12b]], [[2025_Crouzet_HATP12b]]
