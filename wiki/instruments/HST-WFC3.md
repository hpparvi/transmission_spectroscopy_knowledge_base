---
type: instrument
aliases: [WFC3, HST/WFC3, WFC3 G141, WFC3 G102]
tags: [hst-wfc3, near-infrared, spectrograph, pre-jwst, hub]
---

# HST-WFC3

The Wide Field Camera 3 on the Hubble Space Telescope, providing near-infrared transmission and emission spectroscopy via two slitless grisms in **spatial-scanning mode** for time-series observations of bright transiting systems. The pre-JWST workhorse for 1.1–1.7 μm transit spectroscopy and the principal instrument that established H₂O at 1.4 μm as the canonical exoplanet-atmosphere diagnostic. Its archival data now anchor the optical-to-near-IR baseline of every JWST hot-Jupiter / sub-Saturn / sub-Neptune retrieval in the wiki, with the 1.4 μm band breaking the radius–abundance–cloud degeneracy that purely longer-wavelength NIRCam/NIRSpec coverage cannot ([[2025_Verma_HD209458b]]).

## Variants

- **G141 grism (1.075–1.70 μm, R ≈ 130).** The dominant configuration; covers the 1.4 μm H₂O band and the J/H continuum. Used as the primary instrument in [[2014_McCullough_HD189733b]] and [[2021_Mugnai_GJ1132b]]; archival in [[2025_Verma_HD209458b]] (Deming et al. 2013), [[2025_Crouzet_HATP12b]], [[2025_Barat_V1298Tau-b]] (Barat et al. 2024b), [[2025_AcunaAguirre_WASP80b]] (Wong et al. 2022 and Skaf et al. 2020 reductions), [[2026_Heinke_HATP12b]], and [[2013_Pont_HD189733b]] (two transits as part of the panchromatic 0.3–24 μm dataset).
- **G102 grism (0.8–1.15 μm, R ≈ 210).** A bluer companion grism extending toward the optical; less commonly used in the wiki sample.
- **Spatial-scanning mode.** Standard for bright targets — scans the spectrum across detector rows during exposure to avoid saturation while maintaining high-photon S/N. McCullough & MacKenty 2012's original demonstration is cited across all wiki G141 papers.

The standard G141 reduction in the wiki is [[Iraclis]] (Tsiaras et al. 2016) — used by [[2021_Mugnai_GJ1132b]] (ARES survey) and adopted as the default for the panchromatic combinations in [[2025_AcunaAguirre_WASP80b]] / [[2025_Crouzet_HATP12b]] / [[2026_Heinke_HATP12b]]. Earlier wiki papers (Pont 2013, McCullough 2014) used custom pipelines pre-dating Iraclis.

## History

- **2008–2010** — pre-WFC3 era at HST: Pont et al. visible/UV transmission via [[HST-ACS]] G800L on HD 189733 b ([[2008_Pont_HD189733b]]).
- **2010 onwards** — WFC3 commissioning + spatial-scanning mode validated.
- **2013** — first wiki appearance: WFC3 G141 photometric points anchor the panchromatic [[2013_Pont_HD189733b]] HD 189733 b spectrum.
- **2014** — first single-target detection: [[2014_McCullough_HD189733b]] reports H₂O at 1.4 μm (200 ± 47 ppm) on HD 189733 b; the same data motivate the unocculted-starspot reinterpretation of the visible Rayleigh slope.
- **2017–2021** — WFC3 G141 becomes the workhorse for HST hot-Jupiter and sub-Neptune transit spectra. The ARES survey ([[Iraclis]] + [[TauREX3]]) re-reduces a population of WFC3 transits homogeneously; [[2021_Mugnai_GJ1132b]] is the wiki representative — five GJ 1132 b transits flat at 1.1–1.7 μm, decisively rebutting Swain et al. 2021's tentative HCN/H₂ claim.
- **2022 onwards** — JWST takes over for new high-precision time-series, but **WFC3 archival data become the optical/near-IR anchor** for JWST panchromatic retrievals on hot Jupiters and sub-Saturns. The pattern is ubiquitous in the wiki's 2025–2026 papers.

## Trade-offs

- **Strength: 1.4 μm coverage anchors retrievals.** [[2025_Verma_HD209458b]] demonstrates that JWST/NIRCam-only retrievals overestimate H₂O and CO₂ abundances by ~3 dex relative to STIS+WFC3+NIRCam — the WFC3 1.4 μm H₂O feature breaks the radius–abundance–cloud degeneracy. Generalizes to all warm-to-hot gas giants where alkali-only optical or NIR-only data leave clouds and metallicity unconstrained.
- **Strength: bright-target capability.** Spatial-scanning mode delivers ~30 ppm photon-limited precision per 19-nm bin on V ≈ 7–8 hosts (HD 189733, HD 209458) — a precision JWST routinely matches but rarely exceeds for bright hosts.
- **Limitation: stellar variability between epochs.** [[2025_Barat_V1298Tau-b]] requires a 400 ppm offset between archival WFC3 and new JWST/NIRSpec G395H data on the young host V1298 Tau b — stellar activity changes between visits introduce a non-trivial broad-band offset that has to be fit. [[2026_Heinke_HATP12b]]'s HST/STIS+WFC3 + JWST joint fit similarly carries instrument-pair offsets as nuisance parameters.
- **Limitation: narrow band.** 1.075–1.70 μm covers only the 1.4 μm H₂O band; without optical coverage (Na/K/Rayleigh) and without 3–5 μm coverage (CO₂, CO, SO₂, CH₄), inferences are degenerate. WFC3 alone produced the canonical mid-2010s "tentative H₂O" hot-Jupiter detections that JWST has since confirmed or revised.
- **Limitation: superseded by JWST for new data.** WFC3 G141 transit precision is now matched in single visits by JWST/NIRISS SOSS; JWST/NIRSpec PRISM extends to broader wavelength range. New WFC3 GO programs are increasingly archival-only.

## Open issues

- **Stellar-variability offsets between WFC3 and JWST epochs.** Active hosts (V1298 Tau, HD 189733, HAT-P-12) show ≥100 ppm broad-band shifts between WFC3 and JWST observations; whether these are genuine atmospheric variability or photospheric/instrument calibration is target-dependent. [[2025_Barat_V1298Tau-b]] handles this by fitting a single offset; not yet a community-standard approach.
- **Cross-instrument calibration.** [[2025_Verma_HD209458b]] fits a HST↔JWST offset of ~205 ppm (free retrieval) vs ~39 ppm (equilibrium retrieval); the physical origin is unclear and treated as a fitting parameter.

## Papers

### Pre-JWST hot-Jupiter detections (HD 189733 b)
- [[2014_McCullough_HD189733b]] — single G141 spatial-scan transit; first H₂O detection on HD 189733 b (200 ± 47 ppm at 1.4 μm + 83 ± 53 ppm at 1.15 μm); reinterprets the [[2013_Pont_HD189733b]] panchromatic Rayleigh slope as unocculted-starspot contamination.
- [[2013_Pont_HD189733b]] — two G141 transits combined with STIS + ACS + NICMOS + Spitzer for 0.3–24 μm panchromatic transmission; flat 1.10–1.69 μm consistent with muted (≤ 1 scale height) molecular features.

### HST G141 single-instrument transmission
- [[2021_Mugnai_GJ1132b]] — five G141 transits of GJ 1132 b (2017 Apr–Nov, ARES survey via Iraclis); featureless; rules out H₂-dominated atmospheres; rebuts the Swain et al. 2021 HCN/H₂ claim.

### Archival WFC3 + JWST panchromatic retrievals
- [[2025_Verma_HD209458b]] — archival G141 transit (Deming et al. 2013) + STIS + JWST/NIRCam; the 1.4 μm coverage anchors temperature in the SANSAR retrievals; without it, NIRCam-only retrieval overestimates H₂O by 3 dex.
- [[2025_Crouzet_HATP12b]] — archival G141 transit on HAT-P-12 b combined with new NIRSpec G395M; H₂O at 6.0σ; metallicity 10× solar with photochemistry, ~60× without.
- [[2026_Heinke_HATP12b]] — archival G141 + HST/STIS + JWST NIRISS+NIRSpec G395M+MIRI/LRS for panchromatic 0.36–12.4 μm information-content study of HAT-P-12 b; H₂O at >12σ, NIRISS-driven; 11–15× solar metallicity.
- [[2025_AcunaAguirre_WASP80b]] — archival G141 (Wong 2022 and Skaf 2020 reductions) + STIS + JWST/NIRCam in a joint interior-atmosphere retrieval on warm gas giant WASP-80 b; brackets atmospheric M/H = 2.75–10× solar.
- [[2025_Barat_V1298Tau-b]] — archival G141 transit of the young (10–30 Myr) sub-Neptune progenitor V1298 Tau b (Barat 2024b); offset by 400 ppm to match JWST visit due to stellar variability; combined with JWST/NIRSpec G395H for panchromatic 1.0–5.2 μm transmission; H₂O at 30σ.
