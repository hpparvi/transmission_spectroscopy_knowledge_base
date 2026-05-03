---
type: paper
bibkey: 2025_Gressier_WASP17b
authors: [Gressier, A., MacDonald, R. J., Espinoza, N., Wakeford, H. R., Lewis, N. K., Goyal, J., Louie, D. R., Radica, M., et al.]
year: 2025
venue: AJ 169:57
doi: 10.3847/1538-3881/ad97bf
targets: [WASP-17b]
instruments: [JWST-NIRISS]
methods: [secondary-eclipse-spectroscopy, atmospheric-retrievals]
species_detected: [H2O]
species_tentative: [FeH]
codes: [transitspectroscopy, supreme-SPOON, Ahsoka, Eureka, juliet, ATMO, TauREX3, POSEIDON, MultiNest]
tags: [hot-jupiter, dreams, dayside, supersolar-metallicity, niriss-soss, jwst-tst]
ingested: 2026-04-29
---

# JWST-TST DREAMS: A Supersolar Metallicity in WASP-17 b's Dayside Atmosphere from NIRISS SOSS Eclipse

**Authors:** Gressier, MacDonald, Espinoza, Wakeford, Lewis, Goyal, Louie, Radica, et al. (2025, AJ 169:57) · DOI: 10.3847/1538-3881/ad97bf
**Target:** [[WASP-17b]] · **Host:** [[WASP-17]] (F6 dwarf) · **Instrument:** [[JWST-NIRISS]] (SOSS, 0.6–2.8 μm)
**Program:** [[JWST-TST-GTO-1353]]

## TL;DR

First emission spectrum of [[WASP-17b]] from a single JWST/NIRISS SOSS secondary eclipse (UTC 2023-03-22, 9.89 hr). Detects [[H2O]] at 6.4σ on the dayside with a robustly **supersolar abundance** across all eight retrieval configurations (3σ lower limit O/H > 3× solar; peak likelihood ~100× solar). T–P profile is non-inverted, contradicting expectations for some hot Jupiters in this temperature range. Brightness temperature rises shortward of 1 μm — consistent with either a high internal temperature (T_int ≈ 600–700 K) or reflected light (toy A_g ≈ 0.2). [[FeH]] tentative at 3σ. Companion to [[2025_LustigYaeger_WASP17b]] on the nightside.

## Key findings

- **[[H2O]] detected at 6.4σ** dayside; log X(H₂O) ≈ −1.4 to −2.0 (supersolar across all 8 retrievals).
- **Supersolar metallicity:** 3σ lower limit O/H > 3× solar (≥ 6.6× solar with positive eclipse-depth priors only); peak likelihood ~100× solar.
- **[[FeH]] tentatively detected** at ~3σ (positive-depth priors); only an upper limit when negative depths allowed.
- **Non-inverted T–P profile** robustly preferred across reductions and parameterizations; ~800–1000 K gradient between 10⁻⁴–10⁻¹ bar.
- **Best forward grid fit:** ATMO grid prefers recirculation factor 0.5, 100× solar metallicity, C/O = 0.2 (subsolar).
- **Sub-1 μm brightness-temperature rise** to ~2400 K from ~1800 K longward of 1 μm; interpreted as either T_int ≈ 600–700 K or reflected light at A_g ≈ 0.2 (toy model). Tentative — only ~30% of bins support the rise under negative-depth priors.
- **Upper limits only** for CO, CO₂, NH₃, CH₄ — apparent detections in some configurations attributed to reduction-specific artifacts.

## Methods

- **Observations:** Single JWST NIRISS SOSS secondary eclipse, GR700XD/CLEAR + F277W out-of-eclipse, SUBSTRIP256, 720 integrations × 49.46 s, 9.89 hr total. Orders 1 (0.85–2.83 μm) and 2 (0.6–0.87 μm), R ≈ 100.
- **Three independent reductions:** [[transitspectroscopy]] (Espinoza 2022), [[supreme-SPOON]] (Feinstein/Radica/Coulombe), and the new [[Ahsoka]] pipeline (Louie et al. submitted; combines `jwst calibration`, supreme-SPOON, nirHiss, [[Eureka]]).
- **Light-curve fits** with [[juliet]] (`batman` + `dynesty`) using GP (Matern-3/2 via `george`) detrending; Bayesian model comparison. Eclipse depths fitted both with positive-only and negative-allowed priors to mitigate Lucy–Sweeney bias. Orbital parameters fixed to Alderson et al. 2022 (not yet ingested).
- **Forward modeling:** [[ATMO]] grid (8 recirculation factors × 22 metallicities × 14 C/O × 4 T_int).
- **Retrievals:** [[TauREX3]] v3.1 with [[MultiNest]], free chemistry over a wide species library; two T–P parameterizations (Madhusudhan & Seager 2009, and a new BD-type variant via the MadhuSeager2009 plugin). Cross-checked with [[POSEIDON]] (M&S09 and Piette & Madhusudhan 2020 BD T–P profiles).
- **Stellar models:** PHOENIX via `PyMSG`.

## Caveats & limitations

- **Lucy–Sweeney bias** on optical eclipse depths; results sensitive to positive-vs-negative eclipse-depth priors.
- **T–P parameterization sensitivity:** BD-type vs M&S09 differ in the deep atmosphere.
- **Order 2** noisy near zero; low-S/N sub-1 μm region.
- **Three reductions disagree most** above 2 μm and below 1 μm; combined-reduction interpretation needed.
- **Sub-1 μm excess** could be reflected light, high T_int, or systematics — current retrievals do not include reflected light.
- **CO / CO₂ / CH₄ weakly constrained** by the SOSS wavelength range; awaits MIRI LRS DREAMS coverage.

## Open questions / follow-ups

- Reflected light vs high T_int: panchromatic NIRISS + NIRSpec + MIRI dayside retrievals (Wakeford et al. 2025, not yet ingested) test this directly.
- How does the supersolar dayside H₂O reconcile with Grant et al. 2023 (not yet ingested) MIRI/LRS transmission, which inferred a low H₂O / high C/O at the terminator?
- Independent confirmation of FeH at higher resolution?

## Related

- [[2025_LustigYaeger_WASP17b]] — companion DREAMS paper on the **nightside** of WASP-17 b from NIRSpec G395H, using the supersolar dayside metallicity inferred here as the photochemistry boundary condition.
- Wakeford et al. 2025 panchromatic NIRISS+NIRSpec+MIRI dayside retrieval and Grant et al. 2023 MIRI/LRS SiO₂ transmission cloud feature (both not yet ingested) round out the DREAMS WASP-17 b suite.
- [[2024_Gressier_L98-59d]] — earlier paper by the same first author (A. Gressier) on the rocky planet L 98-59 d.
