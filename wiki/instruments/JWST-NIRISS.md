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
