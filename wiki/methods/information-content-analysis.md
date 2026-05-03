---
type: method
aliases: [information content, IC analysis, instrument-attribution analysis]
tags: [bayesian, model-comparison, methodology]
---

# Information-content analysis

Quantifies what each instrument or wavelength band contributes to retrieved atmospheric parameters by performing systematic leave-one-out [[atmospheric-retrievals]] across all combinations of instruments and computing the change in Bayesian log-evidence (Δln Z) per combination. Calibrated to nσ via Benneke & Seager 2013 (not yet ingested). Results are typically visualized as Venn diagrams over the instrument set, attributing detection significances to specific data subsets and identifying which mode is essential vs. redundant for each retrieved parameter.

## Trade-offs

- **Strength:** Identifies necessary observations for a given science target — directly informs follow-up planning.
- **Strength:** Reveals retrieval-prior sensitivities (e.g., single-instrument retrievals overestimate molecular abundances if dominant carriers fall outside the band).
- **Limitation:** Δln Z significances should be interpreted cautiously per Kipping & Benneke 2025 / Welbanks et al. 2025 (not yet ingested).
- **Limitation:** Computational cost grows combinatorially with number of instruments.

## Papers

- [[2026_Heinke_HATP12b]] — applies the framework across JWST NIRISS+NIRSpec+MIRI plus HST/STIS+WFC3 on HAT-P-12 b; identifies NIRISS as essential for non-gray cloud evidence and NIRSpec as essential for CO₂ / H₂S detections.
