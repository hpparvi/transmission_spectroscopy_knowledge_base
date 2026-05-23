---
type: instrument
aliases: [NIRISS, JWST/NIRISS, NIRISS/SOSS]
tags: [jwst, near-infrared, spectrograph, slitless]
---

# JWST-NIRISS

The Near Infrared Imager and Slitless Spectrograph on JWST (Doyon et al. 2023; Albert et al. 2023). For transiting exoplanet time-series, the primary mode is **SOSS** (Single Object Slitless Spectroscopy), covering 0.85–2.8 μm with resolving power R ~ 700 using the GR700XD grism and the SUBSTRIP96 (bright targets) or SUBSTRIP256 (fainter targets) subarray. SOSS records two diffraction orders simultaneously; the first order (0.85–2.8 μm) is used for transmission spectroscopy.

Key distinctions from [[JWST-NIRSpec]]: NIRISS/SOSS is slitless (no slit losses), has no detector gap, and extends the blue wavelength coverage to ~0.85 μm — providing sensitivity to stellar-contamination signatures (spots, faculae) and H₂O bands at 0.95–1.4 μm inaccessible to NIRSpec/G395H. Trade-off: the SUBSTRIP96 subarray excludes the second SOSS diffraction order when used in bright-target mode, restricting analysis to the first order only; the shorter upper wavelength limit (2.8 μm vs. ~5 μm for G395H) means CO₂ at 4.3 μm is not accessible without NIRSpec follow-up.

Reduced with the [[exoTEDRF]] pipeline (Feinstein et al. 2023; Radica et al. 2023, 2024).

## Papers
- [[2023_Lim_TRAPPIST1b]] — two SOSS transits of TRAPPIST-1 b (0.6–2.8 μm); dominant stellar contamination from spots (Visit 1) and faculae (Visit 2); H₂-dominated atmospheres rejected at 16–29σ; secondary atmospheres unconstrained; TLS amplitude ~750–1000 ppm peak-to-peak.
- [[2025_Taylor_GJ357b]] — single SOSS transit of the super-Earth GJ 357 b (SUBSTRIP96, 2 groups/integration, 0.85–2.8 μm); first NIRISS/SOSS paper in this wiki; featureless spectrum rules out ≤100× solar metallicity atmospheres with cloud-top pressure > 0.01 bar at 3σ.
- [[2025_Gressier_WASP17b]] — single SOSS **secondary-eclipse** observation of WASP-17 b (SUBSTRIP256, 0.6–2.8 μm); H₂O at 6.4σ on dayside; supersolar metallicity; first NIRISS/SOSS *eclipse* paper in this wiki, demonstrating the mode for hot-Jupiter dayside emission.
- [[2026_Heinke_HATP12b]] — new SOSS transit of the warm sub-Saturn HAT-P-12 b combined with NIRSpec G395M + MIRI/LRS + HST/STIS+WFC3; NIRISS dominates non-gray cloud evidence (>7.5σ only when included).
- [[2026_Radica_WASP96b]] — archival NIRISS/SOSS WASP-96 b spectrum (ERS reanalysis) combined with new NIRSpec G395H + VLT/FORS2; reduction divergence between exoTEDRF and NAMELESS above 1.7 μm flagged.
- [[2025_Felix_TOI-270d]] — single SOSS transit of temperate sub-Neptune TOI-270 d combined with NIRSpec G395H (GO 4098); first-order only (second-order excluded due to stellar contamination at < 0.85 μm); reduced with custom Eureka! + PASTASOSS trace.
- [[2025_FernandezRodriguez_K2-18b]] — single SOSS transit of habitable-zone sub-Neptune K2-18 b combined with NIRSpec G395H (GO 2722); spot-crossing event during ingress modeled with novel semi-empirical correction; first-order 0.85–2.83 μm + second-order 0.6–1.1 μm both extracted.
- [[2025_Fu_limb-asymmetry]] — uniform reanalysis of all nine archival JWST/NIRISS/SOSS hot-Jupiter transmission spectra (T_eq = 770–1740 K, log g 2.45–3.2 cgs); first JWST population-level study of morning–evening limb asymmetry; introduces the [[limb-asymmetry|Limb Spectroscopy Metric]] for predicting future-target SOSS observability.
- [[2025_Murphy_WASP107b]] — NIRISS/SOSS limb-resolved transit of WASP-107 b is biased by **two occulted starspot crossings** (at longitudes ~−60° and +60°); injection-recovery with [[Catwoman]] + `starry` derives offset corrections (+110 ppm evening, +20 ppm morning) bringing the SOSS spectrum into agreement with NIRCam.
- [[2025_Deka_WASP39b]] — NIRISS/SOSS Eureka!-reduced transit of WASP-39 b included in the panchromatic NIRISS+PRISM+MIRI [[NEXOTRANS]] retrieval framework demonstration; NIRISS provides the optical-NIR baseline.
- [[2025_Ahrer_GJ3090b]] — two NIRISS/SOSS transits of warm sub-Neptune GJ 3090 b separated by 6 months under GO 4098; **TLS-dominated** with visit-to-visit variation in retrieved spot/faculae parameters precluding atmospheric inference at NIRISS wavelengths; companion paper to NIRSpec G395H. First detection of metastable He I in a sub-Neptune via NIRISS/SOSS pixel-level spectroscopy at 5.5σ.
- [[2025_Luque_K2-18b]] — NIRISS/SOSS K2-18 b transit in panchromatic NIR+MIR joint retrieval; uses [[exoTEDRF]] reduction from [[2025_Schmidt_K2-18b]] (R = 100); first MIRI+NIRISS+NIRSpec joint analysis under one framework.
- [[2025_Schmidt_K2-18b]] — comprehensive NIRISS+NIRSpec reanalysis with two reduction pipelines ([[FIREFLy]] + [[exoTEDRF]]) and the **first analysis of the NIRISS SOSS 2nd order** (0.6–0.85 μm); 2nd-order data tightens CH₄ significance (~3.3σ → ~4.5σ) and enables detection of unocculted starspots at 5% coverage. Spot-crossing during ingress trimmed in FIREFLy, modeled as a Gaussian in exoTEDRF.
- [[2025_PicaCiamarra_K2-18b]] — same NIRISS/SOSS K2-18 b transit; 650-molecule trace-gas search across NIR and MIR with three retrieval codes; **3 species reach ≥2.5σ in NIR** (DMS, diethyl sulfide, methacrylonitrile).
- [[2025_Carter_NIRISS-jump-ramp]] — **methodology paper.** JWST Technical Report comparing default JWST pipeline vs LIKELY method (Brandt 2024) for jump detection and ramp fitting; on-sky WASP-39 b ERS visit + 23-realization simulated noise. Differences at ~50 ppm on-sky and 12–18% improvement on simulated data with LIKELY in 1/f and All-noise cases. Flags **group-level 1/f correction** as the dominant unaddressed systematic.
- [[2025_Liu_HATP14b]] — JWST commissioning NIRISS/SOSS visit of HAT-P-14 b ([[JWST-PID-1541]]); reanalyzed with updated [[FIREFLy]] + STScI jwst pipeline. **Blueward slope reported in Albert 2023 (commissioning analysis) disappears** in the updated reduction — corroborates the [[2025_Carter_NIRISS-jump-ramp]] thesis that early NIRISS/SOSS commissioning data need uniform reanalysis.
