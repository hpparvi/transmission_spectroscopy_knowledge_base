---
type: paper
bibkey: 2025_Barat_V1298Tau-b
authors: [Barat, S., Désert, J.-M., Mukherjee, S., Goyal, J. M., Xue, Q., Kawashima, Y., Vazan, A., Misener, W., Schlichting, H. E., Fortney, J. J., Taylor, J., Henry, G. W., Baeyens, R., Line, M. R., Livingston, J. H., David, T., Petigura, E. A., Sikora, J., Shivkumar, H., Feinstein, A. D., Oklopčić, A.]
year: 2025
venue: AJ
arxiv: 2509.04293
doi: 10.3847/1538-3881/adec89
targets: [V1298Tau-b]
instruments: [JWST-NIRSpec, HST-WFC3]
methods: [transmission-spectroscopy, atmospheric-retrievals, joint-interior-atmosphere-retrieval, flare-mitigation]
species_detected: [H2O, CO2, CO, CH4, SO2]
species_tentative: [OCS]
codes: [Eureka, SPARTA, PICASO, ATMO, VULCAN, Photochem, MultiNest]
tags: [young-planet, sub-neptune-progenitor, t-tauri-host, methane-thermometer, mass-loss, internal-temperature]
ingested: 2026-05-04
---

# A Metal-poor Atmosphere with a Hot Interior for a Young Sub-Neptune Progenitor: JWST/NIRSpec Transmission Spectrum of V1298 Tau b

**Authors:** Barat, Désert, Mukherjee, Goyal, Xue, Kawashima, Vazan, Misener, Schlichting, Fortney, Taylor, Henry, Baeyens, Line, Livingston, David, Petigura, Sikora, Shivkumar, Feinstein, Oklopčić 2025, AJ 170:165 · [arXiv:2509.04293]
**Targets:** [[V1298Tau-b]] · **Instruments:** [[JWST-NIRSpec]] (G395H/SUB2048), [[HST-WFC3]] (G141; archival)

## TL;DR
JWST/NIRSpec G395H transmission spectrum of the **young (10–30 Myr) sub-Neptune progenitor V1298 Tau b** (9.85 R⊕, T_eq ≈ 670 K) under [[JWST-GO-2149]] (PI Désert) on 2023 Feb 12. Combined with archival HST/WFC3 G141 (Barat et al. 2024b; not ingested) gives panchromatic 1.0–5.2 μm coverage. Reveals a **clear haze-free atmosphere** with a ~1500 km scale height. Detects [[CO2]] at 35σ, [[H2O]] at 30σ, [[CO]] at 10σ, [[CH4]] at 6σ, [[SO2]] at 4σ; tentative OCS at 3.5σ. **Mass measured from atmospheric scale height** (12 ± 1 M⊕, ~10% precision) — uniquely useful for young active stars where RV is jitter-limited; 40σ below the original Suárez Mascareño 2021 RV mass (0.64 M_J ≈ 200 M⊕). Atmospheric metallicity ~0.6× solar; sub-solar C/O ≈ 0.22; both ~10× lower than mature sub-Neptunes — places V1298 Tau b as a **gas-dwarf** sub-Neptune progenitor. CH₄ abundance is 7σ lower than equilibrium expectation, requiring high internal temperature (~500 K) and vertical mixing K_zz ~ 10⁷–10⁸ cm² s⁻¹. The high T_int is **inconsistent with formation/evolution models** predicting 100–200 K at 20 Myr; mass loss could enhance metallicity over Gyr to reconcile with mature sub-Neptunes.

## Key findings
- **Transmission spectrum: clear, haze-free, 1500 km scale height.** No 0.6–2.0 μm spectral slope; no broad continuum opacity from photochemical hazes. The ~1000 ppm CO₂ feature at 4.3 μm and ~600 ppm H₂O feature at 2.7 μm probe ~3–4 scale heights of the atmosphere.
- **Mass from scale height: 12 ± 1 M⊕** (free retrieval; PICASO grid: 15 ± 1.7 M⊕; ATMO grid: 15 M⊕). Uncertainty ~10% — comparable to ground-based RV for quiet stars; competitive on active T Tauri hosts where stellar jitter prevents RV mass measurement. The technique is validated against [[WASP-107b]] (Sing et al. 2024 NIRSpec G395H transmission yields 32 ± 3 M⊕ vs. RV-derived 30.5 ± 1.7 M⊕ — agreement within 1σ).
- **Atmospheric metallicity ~0.6× solar; C/O ≈ 0.22.** PICASO grid: log Z = 1.05 ± 0.2 dex (~10× solar) — slightly higher; ATMO grid: 1.0× solar; free retrieval: 0.6⁺⁰·⁴⁻⁰·⁶ × solar. C/O subsolar by all methods (PICASO: 0.23 ± 0.08; ATMO: 0.35; free: 0.22⁺⁰·⁰⁶⁻⁰·⁰⁵). Both ~10× lower than typical mature sub-Neptunes ([[2025_Madhusudhan_subneptunes]] reviews supersolar metallicities for K2-18 b, TOI-270 d, etc.).
- **CH₄ "thermometer": [CH₄] ~7σ lower than equilibrium prediction.** Self-consistent grids with photochemistry require high T_int ≳ 500 K + vertical mixing K_zz ~ 10⁷–10⁸ cm² s⁻¹ to deplete CH₄ via dredging from the deep atmosphere where the T-P profile crosses the CO/CH₄ equality line. CH₄ acts as a thermometer for the interior.
- **High T_int (500 K) is inconsistent with evolutionary models** predicting 100–200 K at 20 Myr (E. Lopez & Fortney 2014; Vazan et al. 2018, 2022; not ingested). Resolution requires either (i) post-formation heating (tidal, core-powered, Ohmic; not ingested), (ii) gradually-mixed primordial composition gradients (Vazan & Helled 2020; not ingested), or (iii) silicate-vapor envelope in equilibrium with rocky core (Misener & Schlichting 2022, 2023; not ingested) which slows contraction.
- **Mass-loss timescales:** core-powered evaporation gives mass-loss rate 5×10¹¹ g s⁻¹ → 7.5 Myr / 320 Myr / 1.2 Gyr depending on f_H/He = 0.002 / 0.08 / 0.3. Photoevaporation: silicate model maintains the planet over Gyr; pure H/He model strips entire envelope by 100 Myr. V1298 Tau b is in transient evaporation phase — could lose 50% of envelope by ~100 Myr.
- **OCS at 3.5σ** in the 4.85–5 μm window; broader 20-pixel binning reduces it to ~2σ — tentative. Predicted onset of OCS at ~500 K (S. Mukherjee et al. 2025; not ingested).

## Methods
[[Eureka]] reduction of NIRSpec G395H/SUB2048 raw data; [[SPARTA]] cross-check with consistent results in NRS1 but ~25% higher scatter in NRS2 (under development). White-light curve fitting via empirical model: quadratic stellar variability + double exponential flare + sinusoid post-flare oscillations + planet transit ([[batman]] not yet stubbed; treated like emcee/starry as standard tooling). **Data-driven detrending** of spectroscopic light curves: Gaussian-smoothed second-order polynomial coefficients from white-light curve provide stellar variability template; flare and oscillation profiles scaled per channel. Four channels (3.03, 3.29, 4.04, 4.65 μm) excluded as outliers. [[ExoTiC-LD]] (not yet stubbed) for limb-darkening from K1V models.

Three retrieval flavors:
1. **Free-chemistry [[PICASO]]** — 12 species (CO, CO₂, H₂O, CH₄, NH₃, H₂S, HCN, OCS, N₂O, C₂H₂, SO₂, OCS) + gray cloud + JWST/HST offset; isothermal P-T; PyMultiNest sampler.
2. **Self-consistent [[PICASO]] grid** — RCTE T-P profiles + [[Photochem]] photochemistry; metallicity (0.025–100× solar), C/O (0.1–1.0), T_int (100–600 K), K_zz (10⁰⁵–10¹⁰), recirculation factor; ~4000 grid models.
3. **Self-consistent [[ATMO]] grid** — RCTE T-P with [[VULCAN]] photochemistry; mass (5–30 M⊕), recirculation (0.25–1.0), [M/H] (0.1–100×), C/O (0.05–1.0), T_int (200–600 K); ~11,000 grid models.

For interior modeling, AIOLOS (Schulik & Booth 2023; not ingested) computes thermal evolution and mass loss for both pure H/He and silicate-vapor-envelope scenarios.

## Caveats & limitations
- High internal temperature inferred (500 K) is at the upper edge of grid coverage; stronger constraints would require denser grid sampling.
- T-P profile assumed adiabatic for the methane-quench-point reasoning; this assumption may be questioned for sub-Neptunes with metallicity gradients ("fuzzy" interiors).
- Stellar variability between HST (2020 Oct) and JWST (2023 Feb) epochs requires a 400 ± 10 ppm offset; treated as fitting parameter.
- In-transit stellar flare requires an empirical detrending approach; channels showing different flare profiles are removed (4 of 30 NRS1 channels excluded).
- Mass measurement assumes the well-mixed adiabatic deep atmosphere — relaxing this assumption could broaden the mass posterior.
- 1D plane-parallel atmosphere; gravity variation across atmospheric scale heights is included (~5% effect at 4.3 μm CO₂); other 3D effects neglected.

## Open questions / follow-ups
- What heats the deep interior to 500 K at 20 Myr? Plausible mechanisms (tidal heating, silicate-vapor envelope, "fuzzy" interior gradients) all require detailed modeling. Mass-loss-driven mass-metallicity scaling alone cannot reach 500 K from 100 K starting condition.
- TTV mass measurement (Livingston et al. 2025, in prep; not ingested) provides an independent test; current values 5–10 M⊕ from HST monitoring agree with the atmospheric scale-height mass within 2σ.
- Eclipse spectroscopy or NIRISS/SOSS coverage of the 0.6–2.7 μm range would tighten constraints on H₂O, alkali metals, and the 1.4 μm water feature seen in HST.
- Younger (~5 Myr) or older (~30+ Myr) targets in the same age sequence would test the proposed mass-loss-driven metallicity-evolution scenario.

## Related
- [[2025_Madhusudhan_subneptunes]] — review/perspective placing sub-Neptunes in the 6-class T_eq × H₂-content scheme; V1298 Tau b is a "gas dwarf" precursor with low metallicity that mass loss could evolve toward typical mini-Neptune endpoints.
- [[2025_Roy_LP791-18c]], [[2025_FernandezRodriguez_K2-18b]], [[2025_Felix_TOI-270d]] — atmospheric characterizations of mature sub-Neptunes with supersolar metallicities; V1298 Tau b is the youngest comparison anchor.
- [[2025_Murphy_WASP107b]] — WASP-107 b panchromatic JWST analysis. Sing et al. 2024 (not ingested) used the same NIRSpec G395H spectrum to derive a 32 ± 3 M⊕ mass from atmospheric scale height — within 1σ of the RV-derived 30.5 ± 1.7 M⊕. Cross-validates the mass-from-scale-height technique here.
