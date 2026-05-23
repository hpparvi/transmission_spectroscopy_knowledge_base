---
type: paper
bibkey: 2025_Liu_HATP14b
authors: [Liu, R., Wang, L.-C., Rustamkulov, Z., Sing, D. K.]
year: 2025
venue: arXiv
arxiv: 2504.08903
targets: [HAT-P-14b]
instruments: [JWST-NIRISS, JWST-NIRSpec]
methods: [transmission-spectroscopy, atmospheric-retrievals]
species_detected: [H2O]
species_tentative: []
species_ruled_out: [CO, CO2, CH4]
codes: [FIREFLy, petitRADTRANS, MultiNest]
tags: [super-jupiter, f-star-host, eccentric-orbit, grazing-transit, commissioning, pipeline-reanalysis, low-tsm, solar-metallicity]
ingested: 2026-05-16
---

# Unveiling the atmosphere of the super-Jupiter HAT-P-14 b with JWST NIRISS and NIRSpec

**Authors:** Liu, Wang, Rustamkulov, Sing (2025, arXiv:2504.08903)
**Target:** [[HAT-P-14b]] · **Host:** [[HAT-P-14]] · **Instruments:** [[JWST-NIRISS]] SOSS + [[JWST-NIRSpec]] G395H · **Programs:** JWST-PID-1118 + JWST-PID-1541 (commissioning)

## TL;DR

Combined [[JWST-NIRISS]] SOSS (0.6–2.8 μm) + [[JWST-NIRSpec]] G395H (2.87–5.14 μm) transmission spectrum of the **super-Jupiter HAT-P-14 b** (M_p = 3.44 M_J, R_p = 1.42 R_J, P = 4.6 d, e = 0.11, around an F-type star T_eff = 6600 K). Both observations were taken during **JWST commissioning** (NIRSpec G395H: 2022-05-30, PID 1118 PI Proffitt; NIRISS/SOSS: 2022-06-08, PID 1541 PI Espinoza); initial analyses by Albert et al. 2023 (A23) and Espinoza et al. 2023 (E23) — both not ingested — reported (i) a featureless NIRSpec G395H spectrum and (ii) an unexplained NIRISS/SOSS blueward slope and 1.4 μm "break." Liu et al. reanalyze both datasets with the latest [[FIREFLy]] pipeline + improved STScI jwst-pipeline calibrations. The **blueward slope disappears** in the updated reduction; the previously "featureless" NIRSpec spectrum reveals small but consistent water bumps at 1.4, 1.9, and 2.6 μm. **[[H2O]] is detected at 3.09σ** (Δln Z = +3.4 over baseline); a gray cloud deck is weakly preferred at 1.90σ. Equilibrium-chemistry retrievals constrain **[Fe/H] = −0.08⁺⁰·⁸⁹₋₀·⁹⁸ and C/O = 0.41⁺⁰·²⁴₋₀·²⁰** (consistent with solar and stellar). HAT-P-14 b ranks 805th in the Transmission Spectroscopy Metric (TSM = 23.64) — far from a "favorable" target — yet a meaningful atmospheric inference is achievable: a methodology demonstration that **JWST can characterize ~1000 exoplanet atmospheres** through transmission spectroscopy. The result also highlights the **need to reanalyze early commissioning data** with the latest pipeline.

## Key findings

- **H₂O detected at 3.09σ** in the combined NIRISS + NIRSpec G395H spectrum. Δln Z = +3.4 over baseline (no-water), moderate Jeffreys preference. Free-chemistry retrieval: log VMR(H₂O) = −2.32⁺¹·¹³₋₁·₄₀. Equilibrium retrieval: [Fe/H] = −0.08⁺⁰·⁸⁹₋₀·⁹⁸ and C/O = 0.41⁺⁰·²⁴₋₀·²⁰.
- **No detection of CO, CO₂, CH₄.** Free-chemistry retrieval 95% upper limits: log VMR(CO₂) < −3.23, log VMR(CO) < −1.69, log VMR(CH₄) < −4.36. CO₂ and CH₄ non-detection consistent with the mass-metallicity relationship at this planet mass.
- **Weak gray cloud deck** at 1.90σ; log P_cloud = −2.02⁺¹·⁷⁸₋₁·₁₃ bars. Marginal preference; not a strong cloud signature.
- **Blueward slope in NIRISS reported by A23 disappears** in the updated reduction. The previous slope (>1.4σ from a flat line, ≥100 ppm amplitude at 0.85 μm) is attributed to the older STScI jwst calibration pipeline + older superbias-subtraction step. With improved calibrations (CRDS_CTX = jwst_12.41.pmap / jwst_13.03.pmap; superbias step updated since A23), the slope is not reproduced.
- **NIRSpec G395H spectrum not featureless.** A23 / E23 (not ingested) reported the G395H spectrum was consistent with a flat line. Liu et al. detect small bumps at 1.4 / 1.9 / 2.6 μm aligned with H₂O features that boost the combined-spectrum H₂O detection beyond what either instrument alone would deliver.
- **Spectrum-fit quality**: best-fit atmosphere χ²_ν = 0.98 (DOF = 194) vs. flat-line χ²_ν = 1.10 (DOF = 199). Atmosphere is a better fit but flat line cannot be entirely rejected.
- **M-dwarf companion is not the H₂O source.** HAT-P-14 has a known faint (ΔJ = 5 mag) M-dwarf companion ~0.844" away that contaminates the NIRISS subarray. Liu et al. compute a worst-case dilution factor as a function of wavelength (using PHOENIX models at T_eff = 6600 / 3300 K); dilution-correction does not remove the water features. The 1.4 / 1.9 μm bumps are intrinsic to HAT-P-14 b.
- **[[stellar-contamination]] (TLSe) ruled out.** HAT-P-14 is an inactive F-star (no Ca H/K emission per Torres et al. 2010, not ingested) with low expected spot-coverage; F-star spots cannot reach the cool temperatures needed for H₂O spectral features. TESS light curve shows no rotational modulation.
- **Methodology demonstration.** HAT-P-14 b's TSM = 23.64 (Kempton et al. 2018, not ingested) places it 805th in transmission-spectroscopy target priority. The 3σ H₂O detection on such a low-TSM target demonstrates that **JWST can deliver atmospheric inferences on ~1000 exoplanets** — far beyond the canonical "top-100" sample.

## Methods

**Observations.**
- **[[JWST-NIRSpec]] G395H** (PID 1118, PI Proffitt, commissioning) — 2022-05-30; 6.5-hr transit; BOTS mode, NRSRAPID, 20 groups × 1139 integrations; S1600A1 + SUB2048. NRS1 + NRS2 detectors used.
- **[[JWST-NIRISS]] SOSS** (PID 1541, PI Espinoza, commissioning) — 2022-06-08; 6.1-hr transit; GR700XD/CLEAR + SUBSTRIP256; 6 groups × 572 integrations. Order 1 and Order 2 spectra.

**Reductions.** Both datasets reduced with [[FIREFLy]] (Rustamkulov et al. 2022, 2023; not ingested), modified from the official STScI jwst pipeline. Key choices:
- Custom group-level 1/f noise subtraction (after superbias, before dark current, with PSF mask threshold flux = 3.6 DN/s).
- Dark-current and jump steps in the jwst pipeline are skipped (handled separately).
- NIRISS: manual saturation correction — flag whole columns at NGROUP=3 (saturated), NGROUP=4 (progressively flagged), to mitigate first-group-effect biases per Carter et al. 2024 (= [[2025_Carter_NIRISS-jump-ramp]]).
- Background subtraction: SOSS commissioning template scaled to the observation.

**Light-curve fitting.** White light curve fit with [[batman]] + emcee, fixed period and eccentricity, fit a/R_⋆ and b. Two-stage approach: white-light fit gives a/R_⋆ and b; spectroscopic fits then fix these and fit only R_p/R_⋆ + linear systematic + limb-darkening (free for NIRSpec; fixed to 3D PHOENIX values for grazing NIRISS).

**Atmospheric retrieval.** [[petitRADTRANS]] free-chemistry retrieval (Mollière et al. 2019); isothermal T = 1624 K (Southworth 2012, fixed); seven free parameters: planet radius, log P_cloud, log VMR(H₂O), log VMR(CO₂), log VMR(CO), log VMR(CH₄), offset between NIRISS and NIRSpec (~+237 ppm).

**Equilibrium-chemistry retrieval** also run with 4 parameters: log P_cloud, [Fe/H], C/O, log P_quench. Nested sampling with [[MultiNest]] / pymultinest, 2000 live points.

## Caveats & limitations

- **Grazing transit (b = 1.014).** The transit is extremely grazing — both NIRSpec NRS1 and NRS2 white-light fits agree to within 1 R_p/R_⋆. Limb-darkening is poorly constrained; LD fixed to theoretical 3D Magic et al. 2015 (not ingested) values. F-star LD modeling is well-validated.
- **Single transit per instrument.** Both visits are commissioning observations; no follow-up to break degeneracies or check repeatability.
- **Equilibrium-chemistry C/O is uncertain.** The 0.41⁺⁰·²⁴₋₀·²⁰ value spans 0.21–0.65 at 1σ — broad. Substellar C/O within errors.
- **No carbon-species detection.** This is a 3.44 M_J giant where mass-metallicity scaling predicts low [Fe/H] and hence low [C/H] (and CO₂/CH₄/CO). Non-detection is consistent, but CO upper limit log VMR < −1.69 is loose enough that more visits could detect it.
- **NIRISS Order 1 systematic noise persists.** A 30-min-correlation residual structure flagged in white light curve fits; common-mode detrending applied but increases white-noise residuals.
- **Pre-binning vs post-binning** affects RMS at small bin sizes. Pre-binning preferred for these data.
- **Different conclusion from A23/E23 (not ingested)** — pipeline-version-driven. Liu et al. argue (and Wang et al. in prep argues for WASP-96 b) that the early NIRISS/SOSS spectra need reanalysis with the latest jwst pipeline.

## Open questions / follow-ups

- **Multi-visit confirmation.** A second NIRISS or NIRSpec G395H visit would firm up the H₂O detection beyond 3σ and potentially detect CO.
- **HAT-P-14 b's equilibrium temperature** is ~1574 K — bracketed by the limit where CO ↔ CH₄ thermochemistry transitions; equilibrium and disequilibrium models differ in CO/CH₄ predictions. Better S/N would test this.
- **Generalization to faint commissioning targets.** WASP-96 b NIRISS commissioning (Radica et al. 2023, not ingested) also showed a blueward slope that disappeared in later reanalysis (Wang et al. in prep). Pattern: **early NIRISS/SOSS commissioning data may need uniform reanalysis**.
- **[[JWST-ERS-1366]] and other early NIRISS/SOSS observations** of WASP-39 b, WASP-96 b, and HAT-P-14 b form a "first-three-NIRISS-targets" reanalysis cohort that this work + Carter et al. 2025 ([[2025_Carter_NIRISS-jump-ramp]]) urgently flag.

## Related

- [[2025_Carter_NIRISS-jump-ramp]] — same conclusion about the importance of updated pipeline; uses WASP-39 b ERS as test bed. The HAT-P-14 b case is independent direct corroboration.
- A23 = Albert et al. 2023 (PASP 135 075001; not ingested) — original NIRISS/SOSS HAT-P-14 b commissioning paper.
- E23 = Espinoza et al. 2023 (PASP 135 018003; not ingested) — original NIRSpec G395H commissioning paper.
- Carter & May et al. 2024 (Nature Astronomy; not ingested) — joint NIRISS/SOSS + NIRSpec + NIRCam analysis of WASP-39 b ERS; provides orbital parameter constraints used here.
- Wang et al. in prep — WASP-96 b NIRISS/SOSS reanalysis showing same disappearing blueward slope.
- Schmidt & Tsai et al. in prep — referenced as supporting the "pipeline matters" thesis.
- Liu, Wang, Rustamkulov & Sing 2025 frames itself as a "1000-exoplanet feasibility study" — TSM = 23.64 with a 3σ H₂O detection.
