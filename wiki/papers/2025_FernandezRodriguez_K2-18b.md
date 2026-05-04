---
type: paper
bibkey: 2025_FernandezRodriguez_K2-18b
authors: [Fernández-Rodríguez, G., Morello, G., Tan, J. C., Pallé, E., Swain, M. R., Poultourtzidis, E., Biagini, A., Changeat, Q., Jiang, C., Pozuelos, F. J., Amado, P. J.]
year: 2025
venue: A&A
arxiv: 2510.18098
targets: [K2-18b]
instruments: [JWST-NIRISS, JWST-NIRSpec]
methods: [transmission-spectroscopy, atmospheric-retrievals, stellar-contamination-modeling]
species_detected: [CH4]
species_tentative: [CO2]
species_ruled_out: [DMS, H2O, CO, NH3, HCN, H2S, OCS, CH3Cl, N2O, CS2]
codes: [exoTEDRF, Eureka, TauREX3, MultiNest, ExoTETHyS]
tags: [sub-neptune, hycean-debate, dms-retraction, c-o-supersolar, inside-out-planet-formation, semi-empirical-spot-correction]
ingested: 2026-05-04
---

# The Atmospheric Composition of Sub-Neptune K2-18 b and Implications for its Formation

**Authors:** Fernández-Rodríguez, Morello, Tan, Pallé, Swain et al. (2025, A&A submitted; arXiv:2510.18098)
**Targets:** [[K2-18b]] · **Instruments:** [[JWST-NIRISS]] SOSS + [[JWST-NIRSpec]] G395H · **Program:** [[JWST-GO-2722]] (PI: Madhusudhan)

## TL;DR

An independent reanalysis of the JWST NIRISS/SOSS + NIRSpec G395H transits of the temperate sub-Neptune K2-18 b under [[JWST-GO-2722]] — the original Madhusudhan et al. 2023 dataset (not ingested). Twelve transmission-spectrum variants are produced by varying spectral binning, limb-darkening treatment, instrumental offsets, error-bar inflation, and a **novel semi-empirical occulted-spot correction** in the NIRISS ingress (which Madhusudhan 2023 also flagged). Free-chemistry retrievals with [[TauREX3]] across a range of model complexities yield: **[[CH4]] robustly detected at > 4σ across all configurations**; **[[CO2]] is configuration-dependent at typically ~2σ**; **DMS vanishes** when comprehensive (full molecular suite) retrievals are run — confirming the Schmidt et al. 2025 retraction (not ingested). Atmospheric inferences span MMW ≈ 2.5–10 amu and T_10mbar ≈ 124–250 K; **C/O ≈ 10–13 (super-solar by ~10–20×)** with elevated absolute C and O abundances. The K2-18 b atmosphere is consistent with **Inside-Out Planet Formation** (Chatterjee & Tan 2014; not ingested) at a formation temperature ≈ 500 K, just interior to the carbon "soot" line — predicting a primordial H₂-He envelope inheriting an oxygen-and-carbon-rich gas-phase composition from the disc. Methodological message: simplified retrievals (with only 1–2 species) systematically inflate detection significance compared to comprehensive retrievals; ~3–4σ CH₄ and ~2σ CO₂ are the appropriate values, not the higher initial Madhusudhan 2023 numbers.

## Key findings

- **CH₄ detected at > 4σ** (4.6σ in the fiducial CO₂+CH₄ retrieval; 4.16σ in the comprehensive 13-species retrieval). log VMR ≈ −1.7 to −1.0 across reductions and retrieval setups; remains robust to all data-processing choices tested.
- **CO₂ marginal at ~2σ** (2.0σ in fiducial; non-detection in comprehensive 13-species retrieval). log VMR ≈ −3.94⁺¹·⁶⁸₋₄·²⁰; bimodal posterior with a long tail to lower values. Highly model-dependent — adding more species systematically lowers CO₂ significance.
- **DMS detection retracted.** With the same reduction quality and a comprehensive retrieval, DMS yields ln Z = 8.52 vs. 8.62 for CO₂+CH₄ alone — **no statistical preference for DMS** (Bayes factor < 1). Tentatively present at 2.13σ–2.31σ in some simplified retrievals; not statistically supported. **Confirms** Schmidt et al. 2025 (not ingested).
- **High MMW configuration found.** Across spectral extractions: MMW ranges 2.53 amu (CH₄-only retrieval) → 4.32 amu (all-molecule comprehensive); the all-molecule version pushes toward a high-MMW solution. The conventional "low-MMW H₂/He hycean atmosphere" is not strongly supported when the full molecular suite is included.
- **No water detected.** log X(H₂O) < −2.29 (95% upper limit). In all retrievals; consistent with sub-cloud condensation or a genuinely dry upper atmosphere.
- **Many species ruled out.** 95% upper limits: H₂O < −2.29, CO < −2.80, NH₃ < −4.41, HCN < −2.54, H₂S < −2.85, SO₂ < −3.20, DMS < −4.39, OCS < −4.61, CH₃Cl < −3.72, N₂O < −3.14, CS₂ < −5.32.
- **Novel semi-empirical spot correction.** New methodology: subtract spotted vs spotless light-curve models, treating the spot signal as wavelength-shape-invariant with free amplitude per wavelength bin. Particularly important for the NIRISS spot-crossing event during ingress reported by Madhusudhan 2023. Statistically preferred over no-spot-correction retrievals by ΔAIC = 14.24 (Blc-EQ-S vs Blc-PhQ).
- **C/O ≈ 10.3⁺¹³⁸·⁸₋₈·⁶ from comprehensive retrieval; 13.4⁺¹⁰⁴·³₋₁₁·¹ from full-suite retrieval** — both well above stellar (C/O ≈ 0.5) and solar.
- **C/H super-solar by 10–100×; O/H super-solar by ~10×** — consistent with formation interior to the C "soot" line (~500 K) but exterior to the H₂O ice line (170 K) on the disc, capturing the oxygen-enhanced gas + sublimated soot regime predicted by Cevallos Soto et al. 2022 (not ingested).
- **Inside-Out Planet Formation (IOPF) consistency.** With the K2-18 c innermost (non-transiting) planet's location at the dead-zone inner boundary (DZIB) at ~1200 K, K2-18 b at 0.159 au is predicted to have a formation temperature ~550 K — just interior to the soot line at ~500 K. This **uniquely** predicts the high-C/O primordial atmosphere actually observed.
- **Spectral binning effects.** Native-resolution retrievals are unstable in the low-S/N regime of NIRISS; binning to R ~ 100 before fitting light curves (Blc) gives more robust biases-out posteriors than binning post-fit (Bts). Adopts Blc as fiducial.
- **Madhusudhan 2023 spectrum (Orig-Mad23) reproducible only with their priors.** Even using the original Madhusudhan 2023 published spectrum, the comprehensive retrieval gives a non-detection of DMS and a CO₂ significance of 2.90σ — both lower than initially reported.

## Methods

Two transit observations under [[JWST-GO-2722]]:
- **NIRISS SOSS** on 2023 January 20–21 (~5.3 hr, NRSRAPID, 0.85–2.83 μm first-order). Reduced with [[exoTEDRF]] for stages 1–3.
- **NIRSpec G395H** on 2023 June 1 (~4.9 hr, F290LP, BOTS, 2.80–5.17 μm with detector gap). Reduced with [[Eureka]] for stages 1–3.

Custom MCMC light-curve fitting (Stage 4–6) with empirical or PHOENIX-derived limb-darkening (using [[ExoTETHyS]] for theoretical values), and a **novel two-stage spot correction** subtracting the difference between spotted and spotless transit-model light curves. Twelve spectrum variants produced by combinations of: binning timing (Blc vs Bts), limb-darkening treatment (EQ/PhQ/PhC4), and spot correction (S/S′/none).

Atmospheric retrievals with [[TauREX3]] 3.1 + PyMultiNest:
- **Fiducial:** Blc-EQ-S spectrum + 13-species + Mie-scattering cloud + Guillot T-p.
- **Variants:** isothermal vs Guillot T-p, with/without Mie/clouds, simplified (only-2σ-detected molecules) vs comprehensive (full 13-species) chemical setups.
- Species set: H₂O, CO, CO₂, CH₄, NH₃, HCN, H₂S, SO₂, plus biosignature/refractory candidates DMS, OCS, CH₃Cl, N₂O, CS₂.

Stellar contamination handling: novel semi-empirical spot correction (described above); the only NIRISS spot-crossing in the visit modeled with four parameters (φ_spot, λ_spot, f_spot/f_disk, r_spot/r_disk).

## Caveats & limitations

- **CO₂ at 2σ is fragile.** Configurations differ by ~3 dex in retrieved CO₂ abundance; statistically supported only in some setups. Hu et al. 2025 (not ingested) reanalyzing the same data with NIRSpec/MIRI also report CO₂ at 3.7σ. Convergence remains incomplete across the literature.
- **The DMS retraction depends on the comprehensive retrieval.** Simplified retrievals with only DMS (no CO₂, no NH₃) marginally favor it (Bayes factor 2). The retraction reflects a methodology argument (full chemistry should be tried) rather than a direct refutation.
- **Single transit per instrument.** All conclusions rest on one NIRISS + one NIRSpec G395H visit — small-numbers regime for atmospheric inference; multi-visit confirmation desirable.
- **Spot crossing signal is partially degenerate with limb-darkening.** Empirical vs PHOENIX-quadratic limb-darkening treatments differ; spot correction alleviates this but does not fully resolve it.
- **C/O = 10–13 has wide error bars** spanning 1σ from ~1 to ~150; broadly consistent with super-stellar but quantitatively imprecise.
- **IOPF is one of multiple formation theories** — disc migration with subsequent envelope evolution would yield different C/O predictions; the Fernández-Rodríguez paper does not formally rule out alternatives.

## Open questions / follow-ups

- **Multi-visit NIRISS + NIRSpec confirmation of CO₂.** With CO₂ at 2σ in fiducial and ~3.7σ in Hu et al. 2025 (not ingested), additional visits are critical to firm up.
- **Does MIRI/LRS provide independent CO₂ constraints?** Hu et al. 2025 includes MIRI; a uniform reanalysis at the higher complexity favored by Fernández-Rodríguez would help.
- **What's the C/O on the comparator sub-Neptunes [[TOI-270d]] and [[LP-791-18c]]?** [[2025_Felix_TOI-270d]] reports MMW ≈ 5.6 amu and ~160× solar metallicity for TOI-270 d — different chemical regime; [[2025_Roy_LP791-18c]] reports CH₄ + haze on LP 791-18 c. The diversity is real; mapping it to formation history is the next step.
- **Population test of IOPF.** Fernández-Rodríguez argue this is the first IOPF prediction to be empirically tested via atmosphere; a sample of 5–10 sub-Neptunes with measured C/O is the survey deliverable.

## Related

- [[2025_Felix_TOI-270d]] — methodologically aligned: independent reanalysis of a hycean candidate using a different retrieval framework. Felix et al. argue native-resolution + LSF; Fernández-Rodríguez argue R~100 binning + comprehensive retrieval. Both retract previously claimed sulfur species (SO₂ on TOI-270 d, DMS on K2-18 b).
- [[2025_Roy_LP791-18c]] — LP 791-18 c (CH₄ + haze, no CO₂); K2-18 b (CH₄ + tentative CO₂, no DMS); TOI-270 d (CH₄ + CO₂, tentative CS₂). The three temperate sub-Neptunes form a diversity benchmark.
- Madhusudhan et al. 2023 (K2-18 b CH₄ + CO₂ + DMS in NIRISS+NIRSpec; not ingested), Madhusudhan et al. 2025 (K2-18 b MIRI/LRS DMS confirmation; not ingested), Schmidt et al. 2025 (K2-18 b reanalysis, doubts on DMS; not ingested), Hu et al. 2025 (K2-18 b NIRISS+NIRSpec+MIRI, CO₂ at 3.7σ; not ingested).
