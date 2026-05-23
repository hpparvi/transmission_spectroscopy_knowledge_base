---
type: paper
bibkey: 2025_Taylor_K2-18b-MIRI
authors: [Taylor, J.]
year: 2025
venue: arXiv (research note)
arxiv: 2504.15916
targets: [K2-18b]
instruments: [JWST-MIRI]
methods: [transmission-spectroscopy]
species_detected: []
species_tentative: []
species_ruled_out: []
codes: [MultiNest]
tags: [sub-neptune, hycean-debate, dms-claim, agnostic-features, gaussian-feature-analysis, methodology, contested]
ingested: 2026-05-16
---

# Are there Spectral Features in the MIRI/LRS Transmission Spectrum of K2-18b?

**Author:** Taylor (2025, arXiv:2504.15916; research note, Apr 22 2025)
**Target:** [[K2-18b]] · **Instrument:** [[JWST-MIRI]] LRS · **Program:** [[JWST-GO-2722]] (PI: Madhusudhan)

## TL;DR

A short, model-independent research note testing whether the [[2025_Madhusudhan_K2-18b-MIRI]] MIRI/LRS spectrum of [[K2-18b]] actually contains any spectral features over a flat line — *agnostic* to which molecule might produce them. The author fits the JExoRES MIRI spectrum with six Gaussian-feature models of increasing complexity: a free positive Gaussian, a free negative Gaussian, both combined, and fixed-position variants at 7 μm and 8.8 μm (the wavelengths Madhusudhan-MIRI identifies as feature-driving). **5 of 6 models fall into "no evidence" on the Jeffreys scale (Δln Z < 1)**; only the two-Gaussian model with positions fixed at 7 μm and 8.8 μm shows weak evidence (Δln Z = 1.21, χ²_ν = 0.99, ~2σ "equivalent sigma"). A flat-line fit yields χ²_ν = 1.06 — also acceptable. Conclusion: **no strong statistical evidence for any spectral features in the K2-18 b MIRI/LRS transmission spectrum**. The 3.4σ flat-line rejection in Madhusudhan-MIRI is argued to be inflated by (1) non-nested model comparison between a 16-parameter "canonical" model and 1-parameter flat line, (2) prior-range sensitivity, and (3) restriction to two molecules at fixed wavelengths — the same critique developed independently in [[2025_Luque_K2-18b]] and [[2025_PicaCiamarra_K2-18b]].

## Key findings

- **5 of 6 Gaussian feature tests reach "no evidence" (Δln Z < 1)** over the flat line:
  - Free single positive Gaussian: Δln Z = 0.05 (χ²_ν = 1.18)
  - Free single negative Gaussian: Δln Z = 0.07 (χ²_ν = 1.18)
  - Fixed positive Gaussian at 7 μm: Δln Z = 0.54 (χ²_ν = 1.04)
  - Fixed negative Gaussian at 8.8 μm: Δln Z = 0.76 (χ²_ν = 0.98)
  - Free combined positive + negative Gaussians: Δln Z = 0.14 (χ²_ν = 1.34)
- **Only fixed-position dual-Gaussian (7 + 8.8 μm) reaches weak evidence**: Δln Z = 1.21 (χ²_ν = 0.99). Bayes factor ≈ 3.35. Even in this case, the "equivalent sigma" maps to ~2σ — well below the 5σ standard for a detection claim.
- **Flat-line fit is acceptable**: χ²_ν = 1.06, ln-Evidence = −17.69 ± 0.05 on the 29 spectral bins.
- **Agnostic Gaussian fits collapse to flat lines** when the position is allowed to float — the data don't independently localize where features should be. Only by *imposing* the DMS/DMDS feature positions from prior work does a residual signal emerge.
- **Methodological critiques of [[2025_Madhusudhan_K2-18b-MIRI]]**:
  1. The "canonical vs flat-line" comparison in M25 is not a nested-model comparison (the 1-parameter flat line is not a subset of the 16-parameter canonical model), so the Bayesian evidence interpretation requires careful prior treatment.
  2. M25 themselves note that under the wider 32-parameter "maximal" model, the flat-line rejection drops from 3.4σ → ~3σ — direct evidence of prior sensitivity.
  3. Fitting 29 data points with 16–32 free parameters risks overfitting.
  4. The M25 "canonical" model excludes opacity from species the "maximal" model considered — inflating Bayesian preference by narrowing the model space.
  5. M25 cites Tsai et al. 2024 (not ingested) abundance predictions for DMS, but Tsai et al. 2024 themselves show that **ethane (C₂H₆) would be more readily detectable than DMS** at the same biogenic flux — and ethane is not detected. This logical inconsistency, independently echoed in [[2025_Luque_K2-18b]] and [[2025_PicaCiamarra_K2-18b]], is a serious chemistry-consistency problem with the DMS/DMDS interpretation.

## Methods

**Data.** JExoRES-pipeline reduction of the MIRI/LRS K2-18 b transit from [[2025_Madhusudhan_K2-18b-MIRI]] (Madhusudhan-team release on Zenodo); 29 spectral bins between 5.6 and 11.8 μm. Author also tested the JexoPipe-pipeline reduction; conclusions unchanged.

**Models.** Six Gaussian feature models (1) standard Gaussian δ_λ = A·exp(−(λ−μ)²/2σ_m²) + c, with 4 free parameters (A, μ, σ_m, c); (2) negative Gaussian (same form, A < 0); (3) combined positive + negative Gaussian (7 free parameters). For each, an additional analysis with μ fixed at 7 μm and/or 8.8 μm (motivated by Fig. 6 of Madhusudhan-MIRI showing those wavelengths drive the canonical claim).

**Reference (null) model.** Flat line δ_λ = c, 1 free parameter.

**Inference.** Bayesian evidence (Z) calculated with [[MultiNest]] (Feroz et al. 2009; Buchner et al. 2014). Model preference assessed via Jeffreys' scale (Trotta 2008): Δln Z < 1 "no evidence", 1–2.5 "weak", 2.5–5 "moderate", ≥5 "strong".

## Caveats & limitations

- **Gaussian features are an approximation.** Real molecular absorption bands have intrinsic shapes (Voigt-like cores, asymmetric wings) that depend on temperature, pressure, and broadening physics. A Gaussian model captures rough amplitude + central wavelength + width but not the precise spectral structure. However, for low-resolution MIRI/LRS, DMS and DMDS bands shown in Fig. 3 of Madhusudhan-MIRI are approximately Gaussian, so the approximation is reasonable.
- **No molecular identification.** The analysis is intentionally agnostic to the molecule producing the feature; it cannot distinguish DMS from DMDS or any other species.
- **Single-pipeline result.** Only JExoRES is shown explicitly, though author states JexoPipe gives consistent results. Cross-checks with other reductions (exoTEDRF, SPARTA, Eureka — as in [[2025_Luque_K2-18b]]) not performed.
- **Equivalent-sigma conversion.** Mapping Δln Z = 1.21 → ~2σ depends on the Bayesian-to-frequentist conversion convention (Trotta 2008); not a unique mapping.
- **Research note** (4 pages) rather than full paper. Designed as a targeted methodological critique, not a comprehensive reanalysis.

## Open questions / follow-ups

- **Does Madhusudhan-MIRI's "canonical model" reach DMS+DMDS detection because of model curation rather than data signal?** The result here suggests yes: the data alone do not strongly prefer Gaussian features at any wavelength; the M25 detection requires both fixed feature positions AND a restricted molecular set.
- **Should ethane be considered?** Per Tsai et al. 2024 (not ingested), abiotic photochemistry predicts ethane as a methyl-byproduct equally detectable to DMS — yet not detected, as also flagged in [[2025_Luque_K2-18b]].
- **What constitutes "evidence" for an exoplanet biosignature?** The author argues that Madhusudhan-MIRI's "3.4σ rejection of a flat line" framing fails standard model-comparison hygiene; the wider methodological community is converging on more conservative thresholds for biosignature claims.

## Related

- [[2025_Madhusudhan_K2-18b-MIRI]] — the paper directly critiqued; M25 reports DMS+DMDS at 3.4σ over flat spectrum.
- [[2025_Luque_K2-18b]] — independent panchromatic NIR+MIR retrieval reaching same "no robust evidence" conclusion via a fundamentally different approach (joint retrieval vs Gaussian-feature analysis).
- [[2025_PicaCiamarra_K2-18b]] — 650-molecule agnostic search; concurs that DMS is not statistically preferred over a wide alternative-molecule space.
- [[2025_FernandezRodriguez_K2-18b]] — independent NIR-only reanalysis; also retracts DMS under comprehensive retrievals.
- [[2025_Schmidt_K2-18b]] — comprehensive NIRISS+NIRSpec ensemble reanalysis; arrives at the same conclusion (DMS not robustly preferred) through data-level marginalization across 60 reduction combinations.
- Welbanks, Nixon et al. 2025 (not ingested) — additional contemporaneous critique.
- Tsai, Innes, Wogan, Schwieterman 2024 (ApJL 966 L24; not ingested) — the photochemistry paper whose ethane prediction is invoked here against the DMS interpretation.
