---
type: instrument
aliases: [MIRI, JWST/MIRI, MIRI/LRS]
tags: [jwst, mid-infrared, spectrograph, hub]
---

# JWST-MIRI

The Mid-Infrared Instrument on JWST (Rieke et al. 2015; Kendrew et al. 2015; Bouwman et al. 2023; not yet ingested), covering 5–28 μm. Used for transiting exoplanets in two complementary configurations: the Low-Resolution Spectrometer (**LRS**, ~5–12 μm slitless, R ≈ 50–100) for transmission and emission spectroscopy, and broadband **photometric imaging** (notably **F1500W** at 15 μm) for single-band eclipse temperature measurements. Complementary to [[JWST-NIRSpec]] for small-planet atmospheres: MIRI accesses the strong 15 μm CO₂ band, the 9.6 μm O₃ band, the 7.7 μm CH₄ Q-branch, and the 5–8 μm H₂O continuum — diagnostics largely inaccessible to NIRSpec. The instrument of record for the **rocky-planet eclipse-temperature program** in the wiki: nearly every Cycle 1–3 small-planet bare-rock-vs-atmosphere test runs through MIRI F1500W or LRS.

## Modes

- **MIRI/LRS slitless.** ~5–12 μm spectroscopy; the workhorse for hot-Jupiter / sub-Saturn emission and transmission and for rocky-planet emission spectra.
  - Transmission: [[2025_Tusay_K2-22b]] (disintegrating planet — variable depths 0–1627 ppm), [[2025_Alam_L168-9b]] (combined with NIRSpec for 3–12 μm broadband).
  - Emission: [[2024_Xue_GJ1132b]], [[2024_WeinerMansfield_GJ486b]], [[2024_Wachiraphan_LTT1445Ab]], [[2026_Coy_HD3167b]], [[2026_Heinke_HATP12b]] (LRS analysis deferred to companion paper, Bouwman et al. in prep).
- **F1500W broadband imaging at 15 μm.** Single temperature point per visit via the strong CO₂ band; the standard "atmosphere vs bare rock" test for rocky M-dwarf planets.
  - [[2025_Connors_MIRI-15um]] — uniform FN-PCA reanalysis of 17 F1500W eclipses across 5 rocky planets ([[TRAPPIST-1b]], [[TRAPPIST-1c]], [[LHS1478b]], [[TOI-1468b]], [[LHS1140c]]); introduces [[Erebus]] pipeline.
  - [[2025_Xue_GJ3929b]] — two F1500W eclipses of GJ 3929 b; bare-rock; CO₂ > 100 mbar excluded.
  - [[2026_Holmberg_GJ3473b]] — Hot Rocks Survey V; four F1500W eclipses of GJ 3473 b; thick CO₂ excluded above 1.2–6.5 bar.
- **MRS (Medium-Resolution Spectrometer), F560W, F770W, F1000W, F1280W, F1800W, F2100W**: not yet appearing as primary modes in any wiki paper.

## History

- **Cycle 1 emission baseline (2024).** First MIRI/LRS eclipses of rocky M-dwarf planets establish the bare-rock template: [[2024_Xue_GJ1132b]] (T_day ≈ 709 K, R = 0.95), [[2024_WeinerMansfield_GJ486b]] (T_day ≈ 865 K, R = 0.97 — also retires the [[2023_Moran_GJ486b]] water-rich transmission interpretation), [[2024_Wachiraphan_LTT1445Ab]] (T_day ≈ 525 K, thick CO₂ excluded). MIRI emission becomes the canonical arbiter of transmission ambiguity.
- **Surveys consolidate (2025).** [[JWST-DD-9235]] (Rocky Worlds program; [[2025_Xue_GJ3929b]]), [[JWST-GO-3730]] (Hot Rocks Survey; [[2026_Holmberg_GJ3473b]]), [[JWST-GO-4818]] (LAVA LAMPS USP super-Earths; [[2026_Coy_HD3167b]]) start delivering F1500W eclipse photometry on a population of small planets.
- **Pipeline maturation (2025).** [[2025_Connors_MIRI-15um]] introduces the [[Erebus]] FN-PCA pipeline and a uniform reanalysis of 17 F1500W eclipses; characterizes the empirical detector-settling timescale T_settle [hr] = 0.063 exp(0.427 m_K) − 0.657 across K-mag 5–11 — a calibration deliverable for survey planning.
- **Multi-instrument panchromatic (2025–2026).** [[2025_Alam_L168-9b]] and [[2026_Heinke_HATP12b]] combine MIRI/LRS with NIR JWST + HST for the first 3–12 μm broadband rocky-planet transmission and full panchromatic sub-Saturn analysis.
- **First disintegrating-planet detection (2025).** [[2025_Tusay_K2-22b]] runs four MIRI/LRS visits on K2-22 b; one 9.7σ detection; iron-rich silicate dust + tentative NO gas at ~5.1 μm.
- **First USP atmosphere candidate (2026).** [[2026_Coy_HD3167b]] reports a single LRS eclipse on USP super-Earth HD 3167 b at 38 ± 11 ppm vs 104 ± 3 ppm bare-rock; ~5σ atmospheric evidence.

## Trade-offs

- **F1500W vs MIRI/LRS for atmospheric tests.** F1500W gives one band — degenerate between thick atmosphere and high-albedo bare rock. LRS resolves the spectral shape (CO₂ feature, H₂O continuum) but at lower SNR per visit. The community is converging on F1500W for survey reconnaissance + LRS for follow-up.
- **Detector settling.** First ~1 hour of MIRI exposures shows mag-dependent ramp behavior; [[2025_Connors_MIRI-15um]] provides the empirical calibration but no underlying physical model yet; settling cuts can be aggressive on bright targets.
- **FN-PCA vs simple ramp models.** Connors 2025 demonstrates FN-PCA recovers eclipses missed by ramp models and shifts inferred T_day on TRAPPIST-1 c cooler than the original Zieba 2023 (potential tension; not yet ingested).
- **Cross-pipeline consistency on LRS.** [[2024_Xue_GJ1132b]], [[2024_WeinerMansfield_GJ486b]], [[2024_Wachiraphan_LTT1445Ab]], [[2026_Coy_HD3167b]] each pair [[Eureka]] and [[SPARTA]] reductions for cross-checks; agreement is generally good but visit-specific outliers occur.

## Open issues

- **Detector-settling physical model.** Empirical law works but no first-principles understanding; calibration deliverables are still per-program.
- **Two-band eclipse tests for thick-atmosphere candidates.** Single F1500W cannot break the atmosphere/high-albedo degeneracy; F1280W or LRS follow-up is the natural next step (raised explicitly by [[2026_Coy_HD3167b]] for HD 3167 b and [[2026_Holmberg_GJ3473b]] for GJ 3473 b).
- **Connors 2025 vs prior eclipse depths.** The FN-PCA reanalysis of TRAPPIST-1 c gives a cooler dayside than Zieba 2023 (not yet ingested); reconciliation pending.

## Papers

### F1500W photometric eclipses (rocky M-dwarf planets)
- [[2026_Holmberg_GJ3473b]] — Hot Rocks Survey V; four F1500W eclipses of GJ 3473 b; R = 0.82 ± 0.12.
- [[2025_Xue_GJ3929b]] — two F1500W eclipses of GJ 3929 b; bare rock; CO₂ > 100 mbar excluded.
- [[2025_Connors_MIRI-15um]] — uniform FN-PCA reanalysis of 17 F1500W eclipses across 5 targets.

### MIRI/LRS emission (rocky M-dwarf and USP planets)
- [[2026_Coy_HD3167b]] — single LRS eclipse of USP super-Earth HD 3167 b; ~5σ atmospheric evidence.
- [[2024_Wachiraphan_LTT1445Ab]] — three LRS eclipses of LTT 1445 A b; thick CO₂ excluded > 6σ.
- [[2024_WeinerMansfield_GJ486b]] — two LRS eclipses of Gl 486 b; T_day = 865 K; resolves [[2023_Moran_GJ486b]] degeneracy.
- [[2024_Xue_GJ1132b]] — single LRS eclipse of GJ 1132 b; bare-rock consistent.

### MIRI/LRS emission (warm Neptune)
- [[2025_Mukherjee_GJ436b]] — **two LRS eclipses of warm-Neptune GJ 436 b** under [[JWST-GO-1185]] (MANATEE; PI Schlawin); combined with 6 NIRCam grism eclipses for first panchromatic 2.4–12 μm thermal emission spectrum of GJ 436 b; T_day = 662.8 ± 5.0 K; T_int ~ 60 K; revises Spitzer-era extreme metallicity downward.

### MIRI/LRS transmission
- [[2025_Madhusudhan_K2-18b-MIRI]] — first MIRI/LRS transmission of habitable-zone sub-Neptune K2-18 b under [[JWST-GO-2722]]; reports DMS+DMDS at 3σ in canonical CH₄+CO₂+X retrieval (contested).
- [[2025_Luque_K2-18b]] — independent multi-pipeline reduction of the same MIRI/LRS K2-18 b visit (exoTEDRF first-public MIRI support, SPARTA, Eureka); panchromatic NIR+MIR joint retrieval — DMS/DMDS not preferred. Notes MIRI features require T_p > energy-balance bound, implying systematic.
- [[2025_PicaCiamarra_K2-18b]] — 650-molecule agnostic search across the same MIRI/LRS data (JExoRES + JexoPipe); 11 species reach ≥2.5σ in MIRI but only 3 also in NIR — including diethyl sulfide and methacrylonitrile alongside DMS.
- [[2025_Taylor_K2-18b-MIRI]] — model-agnostic Gaussian-feature analysis of the [[2025_Madhusudhan_K2-18b-MIRI]] MIRI/LRS spectrum; 5 of 6 tests give "no evidence" over a flat line; argues M25 detection is inflated by curated 2-molecule canonical model.
- [[2025_Tusay_K2-22b]] — four LRS transit windows of K2-22 b; one 9.7σ detection; tentative NO at ~5.1 μm.
- [[2025_Alam_L168-9b]] — single LRS transit of L 168-9 b combined with NIRSpec G395H for first 3–12 μm broadband on a rocky planet.

### MIRI/LRS in panchromatic multi-instrument analyses
- [[2026_Heinke_HATP12b]] — MIRI/LRS as one component of NIRISS+NIRSpec G395M+MIRI+HST panchromatic information-content analysis (LRS detail in companion paper).
- [[2025_AcunaAguirre_WASP80b]] — MIRI/LRS emission folded into joint interior–atmosphere retrieval on WASP-80 b.
- [[2025_Jaziri_K2-18b]] — uses Luque et al. 2025 (not ingested) MIRI/LRS Eureka! reduction of K2-18 b transit (GO 2372; PI Madhusudhan; not ingested); MIRI feature amplitudes ~2× larger than NIRISS/NIRSpec — explained by photochemical (tholin) hazes contributing C–H bending absorption near 7 μm.
- [[2025_Murphy_WASP107b]] — MIRI/LRS limb-resolved transit covering 5–12 μm on WASP-107 b; co-fit with NIRCam at 1–5 μm; broad 6–11 μm cloud feature isolated to morning limb only; no spot-crossings during the visit.
- [[2025_Deka_WASP39b]] — MIRI/LRS WASP-39 b 5–12 μm spectrum (Powell et al. 2024; not ingested) co-fit with NIRISS + NIRSpec PRISM in the [[NEXOTRANS]] retrieval framework benchmark; three independent reductions (Eureka, Tiberius, SPARTA) cross-compared to validate the eight-code MIRI cross-comparison.
