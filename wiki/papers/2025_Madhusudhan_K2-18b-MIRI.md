---
type: paper
bibkey: 2025_Madhusudhan_K2-18b-MIRI
authors: [Madhusudhan, N., Constantinou, S., Holmberg, M., Sarkar, S., Piette, A. A. A., Moses, J. I.]
year: 2025
venue: ApJL
doi: 10.3847/2041-8213/adc1c8
targets: [K2-18b]
instruments: [JWST-MIRI]
methods: [transmission-spectroscopy, atmospheric-retrievals]
species_detected: []
species_tentative: [DMS, DMDS]
species_ruled_out: [H2O, NH3, CO, H2S, SO2, C2H2, C2H4, C2H6, CH3SH, PH3, CH3OH]
codes: [JExoRES, AURA, Aurora, MultiNest, UltraNest]
tags: [sub-neptune, hycean-debate, dms-claim, dmds-claim, mid-infrared, single-instrument, contested]
ingested: 2026-05-16
---

# New Constraints on DMS and DMDS in the Atmosphere of K2-18 b from JWST MIRI

**Authors:** Madhusudhan, Constantinou, Holmberg, Sarkar, Piette, Moses (2025, ApJL 983, L40; doi:10.3847/2041-8213/adc1c8)
**Targets:** [[K2-18b]] · **Instrument:** [[JWST-MIRI]] LRS · **Program:** [[JWST-GO-2722]] (PI: Madhusudhan)

## TL;DR

First MIRI/LRS (~5–12 μm) transmission spectrum of K2-18 b under [[JWST-GO-2722]] (5.85 hr visit, 2024 April 25–26, 5095 integrations). Reduced via two independent pipelines ([[JExoRES]] + JexoPipe) that agree within 1σ. From an 11-molecule canonical retrieval (CH₄, CO₂, plus a variable X), the **canonical model including [[DMS]] and [[DMDS]] is preferred at 3.4σ over a featureless flat spectrum** and at 3.2σ over a CH₄+CO₂-only baseline. Individual canonical models with DMS-only or DMDS-only each reach 2.9–3.2σ — the two molecules are spectrally degenerate at the present S/N. Both molecules have prominent C–H stretching (~6.8–8 μm) and methyl bending bands (~9.8 μm for DMS, ~10.5 μm for DMDS) that the data favor. Retrieved abundances are **log X(DMDS) = −3.48⁺¹·²⁴₋₂·²⁷ ≈ 10⁻³** and log X(DMS) = −3.42⁺¹·¹⁶₋₁·⁴⁴ — i.e. ~10× the abundance scale predicted for biological sulfur fluxes ~20× Earth (Tsai et al. 2024; not ingested). 18 of 20 prominent molecules tested have no spectral support; CH₄ and CO₂ from prior NIR observations are not constrained by MIRI alone. Authors frame this as **"new independent evidence" for the previously-tentative DMS biosignature** — claim contested by [[2025_Luque_K2-18b]], [[2025_PicaCiamarra_K2-18b]], and Welbanks, Nixon et al. 2025 (not ingested).

## Key findings

- **DMS+DMDS at 3.4σ over a flat spectrum.** Canonical model: 16 free parameters (CH₄, CO₂, DMS, DMDS + 6 P-T profile + 4 cloud + P_ref + MIRI offset). ln(Z) = 216.40 (JExoRES); flat-spectrum reference assumes uniform ±N ppm prior with N ∈ [600, 2000] (3.4σ–3.8σ); 3.4σ adopted as conservative.
- **Individual molecules also significant.** DMS-only reaches 2.9σ (JExoRES) / 3.0σ (JexoPipe); DMDS-only reaches 3.2σ (JExoRES) / 3.0σ (JexoPipe). The two are spectrally degenerate — broad C-H stretching peak between 6.8–8 μm shared between them; DMS uniquely features ~9.8 μm; DMDS uniquely features ~10.5 μm. Combined posterior of DMS+DMDS = 3.2σ.
- **Robust to data-reduction choices.** Stable across JExoRES and JexoPipe pipelines (1σ agreement throughout). Stable under varying trend models (exp+linear, exp+quad, quadratic only). Stable under masking the "shadow region" past 10.6 μm. Stable under Gaussian Process modeling of time-correlated noise (3.3σ). Stable under varying spectral binning (0.2/0.4/0.8 μm).
- **High retrieved abundances ~10⁻³.** Log X(DMDS) = −3.48⁺¹·²⁴₋₂·²⁷; log X(DMS) = −3.42⁺¹·¹⁶₋₁·⁴⁴. Both are ~1–2 orders of magnitude above the ~10⁻⁴ predicted for "high biogenic flux ~20× Earth" (Tsai et al. 2024; not ingested). When both molecules are in the model, DMDS dominates the spectral fit; when DMDS alone is retrieved, DMS is recovered as a substitute due to spectral degeneracy.
- **18 of 20 candidate molecules show no evidence.** Tested: H₂O, CH₄, NH₃, CO, CO₂, HCN, (CH₃)₂S = DMS, CH₃Cl, CS₂, OCS, N₂O, H₂S, SO₂, C₂H₂, C₂H₄, C₂H₆, (CH₃)₂S₂ = DMDS, PH₃, CH₃SH, CH₃OH. Of these, only DMS and DMDS show non-zero posterior peaks. **C₂H₆ (ethane) is rejected** in this analysis — a result later contested by [[2025_Luque_K2-18b]] who find ethane provides an equally good fit when included in PLATON/SCARLET retrievals across different reductions.
- **CH₄ and CO₂ not constrained by MIRI alone.** Their prior-detected amplitudes (1% VMR) are dwarfed by the much stronger DMS/DMDS spectral contributions in 6–12 μm range. Inclusion of CH₄ and CO₂ at their NIR-determined values yields a comparable fit; their MIRI-only constraints are weak.
- **Retrieved T_p ≈ 422⁺¹⁴¹₋₁₃₃ K at 1 mbar** — somewhat higher than the equilibrium temperature (~255 K) but ~1σ-consistent with NIR-derived temperatures. *Note: [[2025_Luque_K2-18b]] flag this T_p as physically inconsistent with the energy-balance bound of 380 K and argue the MIRI feature amplitudes require an implausibly large scale height.*
- **Leave-one-out cross-validation.** Two data points near 7 μm and just under 9 μm drive the DMS+DMDS detection (large positive Δelpd); the point below 6 μm is better fit by the no-DMS/DMDS model (negative Δelpd). The detection is **driven by multiple data points** but not uniformly distributed.

## Methods

**Observations.** [[JWST-MIRI]]/LRS slitless prism + F560W + FASTR1 readout; 5.85 hr visit on 2024 April 25–26; 2.68 hr in-transit; 5095 integrations of 25 groups each. ~5–12 μm at R ~ 100. Spectrum below 5.6 μm discarded due to instability.

**Data reduction.** Two independent pipelines:
- [[JExoRES]] (Holmberg & Madhusudhan 2023; Madhusudhan 2023b not ingested) — adapted for MIRI. Stages 1–2 use the JWST Science Calibration Pipeline (Bushouse 2020). Custom bad-pixel flagging (Sarkar et al. 2024; not ingested). Row-wise background subtraction. Optimal extraction with 9-pixel aperture. Gaussian-process modeling of correlated noise. First 250 integrations masked.
- **JexoPipe** (Sarkar et al. 2024; not ingested) — fully independent framework previously applied to NIRSpec PRISM and G395H. Used as primary cross-check.

The two pipelines agree within 1σ across all spectral bins (Fig. 3).

**Atmospheric retrieval.** AURA framework (Pinhas et al. 2018) as implemented in recent works (Constantinou et al. 2023, [[2025_Madhusudhan_subneptunes]]); cross-checked with [[Aurora]] (Welbanks & Madhusudhan 2021; Nixon et al. 2024). Plane-parallel hydrostatic atmosphere; parametric six-parameter T-p profile (Madhusudhan & Seager 2009); free volume-mixing ratios for all included molecules. Patchy cloud + Rayleigh-haze parameterization (MacDonald & Madhusudhan 2017; Pinhas et al. 2019). 12 free atmospheric parameters + N_mol mixing ratios. Nested sampling with MultiNest (2000 live points) + cross-check with UltraNest.

Hierarchical Bayesian model selection: a "maximal" 20-molecule model establishes the parameter space; molecules with non-trivial posterior peaks (DMDS first, then DMS upon DMDS removal) are promoted to a "canonical" 16-parameter model. The simpler canonical is preferred over maximal at 2.2σ — Occam-favored.

## Caveats & limitations

- **Single MIRI visit.** All conclusions rest on one 5.85-hr observation. Authors' own follow-up simulations in [[2025_Luque_K2-18b]] estimate **~26 transits** are needed for a 3σ rejection of a flat-line model — current data are at the edge of statistical adequacy.
- **MIRI-only.** Does not include the NIRISS+NIRSpec spectrum from Madhusudhan 2023 (not ingested) in a joint retrieval. [[2025_Luque_K2-18b]] perform that joint retrieval and find DMS/DMDS evidence drops to Δln Z ≤ 2.8 across all reductions — never reaching the Δln Z ≥ 5 strong-evidence threshold.
- **Retrieved T_p physically inconsistent with energy balance.** Per [[2025_Luque_K2-18b]], the 422 K T_p exceeds the maximum zero-albedo no-atmosphere substellar temperature of 380 K. The MIRI features may therefore reflect uncorrected systematics rather than planetary signal — or imply implausibly large scale heights.
- **DMS/DMDS line lists are pressure-limited.** Sharpe et al. 2004 cross-sections are measured at 1 bar / 278 K. K2-18 b's photosphere is at ~1 mbar — orders of magnitude lower pressure than the laboratory data. Real cross-sections may differ substantially; retrieved abundances are biased by an unknown amount.
- **The 20-molecule maximal retrieval is not exhaustive.** [[2025_PicaCiamarra_K2-18b]] subsequently search 650 molecules in the same MIRI data and find 11 that reach ≥2.5σ — including diethyl sulfide and methacrylonitrile that fit the data comparably to DMS. The "two-molecule canonical" framing of the present paper inflates significance relative to a broader candidate space.
- **The shadow region beyond 10.6 μm** (a known MIRI/LRS detector discontinuity; T. J. Bell et al. 2024, not ingested) is not flagged as present; masking it does not change the result. Robustness check, but the systematic is real.
- **No transit-light-source-effect (TLSe) modeling.** The MIRI wavelengths are presumed insensitive to stellar contamination — true at first order but worth checking with multi-visit baselines.

## Open questions / follow-ups

- **Are the MIRI features astrophysical?** The amplitude inconsistency (per [[2025_Luque_K2-18b]]) suggests systematics. A multi-visit MIRI stack (4 transits/year max) is the only direct test — would take 6+ years for a 3σ feature confirmation under current estimates.
- **What's the *true* DMS/DMDS opacity at sub-Neptune photospheric conditions?** New experimental and theoretical cross-section work at ~1 mbar pressures is required to firm up retrieved abundance estimates.
- **Joint NIR+MIR retrieval converges on what?** [[2025_Luque_K2-18b]] panchromatic retrievals retract; [[2025_PicaCiamarra_K2-18b]] broaden the candidate space to 650 molecules; future work must integrate these constraints with abiotic photochemistry predictions (Tsai et al. 2024; Wogan et al. 2024; not ingested).
- **Is DMS even a robust biosignature?** Recent laboratory work (Reed et al. 2024; not ingested) demonstrates abiotic DMS synthesis; cometary DMS detected (Hänni et al. 2024a; not ingested). Seager et al. 2025 (not ingested) argues DMS is no longer a robust biosignature — though neither lab nor cometary abundance scales to the K2-18 b inferred values.

## Related

- [[2025_Luque_K2-18b]] — directly refutes the DMS/DMDS detection via panchromatic (NIRISS+NIRSpec+MIRI) retrieval. Same MIRI data; opposite conclusion driven by broader molecular set and joint NIR constraint.
- [[2025_PicaCiamarra_K2-18b]] — from the Madhusudhan group; partial endorsement (reproduces the 3σ DMS/DMDS canonical-model result) but identifies diethyl sulfide, methacrylonitrile, propyne, and 8 other molecules as comparably good explanations. Recasts the DMS claim as **one of a family of equally-good fits** rather than a unique identification.
- [[2025_Madhusudhan_subneptunes]] — review by the same author group; reaffirms K2-18 b as the cornerstone hycean candidate.
- [[2025_FernandezRodriguez_K2-18b]] — independent NIR-only reanalysis; also retracts DMS at Bayes factor < 1 under comprehensive retrievals.
- [[2025_Schmidt_K2-18b]] — comprehensive NIRISS+NIRSpec reanalysis with 60 data combinations × 4+ retrievals; DMS max significance 2.2σ; 95% upper limit log C₂H₆S < −3.70.
- [[2025_Taylor_K2-18b-MIRI]] — model-agnostic Gaussian critique of this paper's MIRI/LRS data; 5 of 6 Gaussian tests give no evidence over a flat line.
- Welbanks, Nixon et al. 2025 (not ingested) — additional independent reanalysis arguing against DMS.
