---
type: paper
bibkey: 2025_Fu_statistical-trends
authors: [Fu, G., Stevenson, K. B., Sing, D. K., Mukherjee, S., Welbanks, L., Thorngren, D., Tsai, S.-M., Gao, P., Lothringer, J., Beatty, T. M., Gapp, C., Evans-Soma, T. M., Allart, R., Pelletier, S., Thao, P. C., Mann, A. W.]
year: 2025
venue: arXiv preprint
arxiv: 2501.02081
targets: [GJ3470b, HIP67522b, WASP-107b, WASP-127b, WASP-39b, HD209458b, HD189733b, WASP-121b]
instruments: [JWST-NIRSpec, JWST-NIRCam]
methods: [transit-spectroscopy, population-study, band-index-analysis, atmospheric-retrievals]
codes: [PLATON, PICASO, Photochem]
species_detected: [SO2, CO2, CO, H2O]
tags: [population-study, hot-jupiter, sub-saturn, color-color-diagram, mass-metallicity, jwst-statistical, sulfur-photochemistry]
ingested: 2026-05-18
---

# Statistical Trends in JWST Transiting Exoplanet Atmospheres

**Authors:** Fu, Stevenson, Sing, Mukherjee, Welbanks, Thorngren, Tsai, Gao, Lothringer, Beatty, Gapp, Evans-Soma, Allart, Pelletier, Thao, Mann (2025, arXiv preprint) · [arXiv:2501.02081]
**Targets:** 8 hot-Jupiter / sub-Saturn / warm-Neptune class — [[GJ3470b]], [[HIP67522b]], [[WASP-107b]], [[WASP-127b]], [[WASP-39b]], [[HD209458b]], [[HD189733b]], [[WASP-121b]] · **Instruments:** [[JWST-NIRSpec]] (G395H, PRISM), [[JWST-NIRCam]] (F322W2 + F444W)

## TL;DR
First **population-level statistical study** of JWST transiting exoplanet atmospheres. Combines 8 high-precision 2.7–5 μm transmission spectra spanning T_eq = 615–2450 K and M_p = 0.03–1.16 M_J. Defines four photometric bands — **L (2.9–3.7 μm), SO₂ (3.95–4.1 μm), CO₂ (4.25–4.4 μm), CO (4.5–4.9 μm)** — and constructs scale-height-normalized band indices (SO₂-L, CO₂-L, CO-L) to enable population-level comparison. Reports three primary correlations: **(i) SO₂-L vs T_eq strong negative (r = −0.64 ± 0.08)** and **vs M_p moderate negative (r = −0.41 ± 0.09)** — SO₂ photochemistry preferentially operates on cooler (≲ 1200 K) low-mass (≲ 0.3 M_J) targets; **(ii) SO₂-L vs bulk Z fraction strong positive (r = 0.54 ± 0.10 for T_eq < 1400 K)** — SO₂ traces metallicity; **(iii) CO-L vs T_eq moderate positive (r = 0.46 ± 0.07)** driven by ultra-hot WASP-121 b. Population favors **super-solar metallicity (>3× solar), low C/O (<0.7), and a mass-metallicity correlation** (BIC 232 with freely fitted vs 295 uniform; Solar-system trend gives BIC 617). Introduces an SO₂-L vs CO₂-L "color-color diagram" framework for transiting exoplanets analogous to the HR diagram for stars. Also presents **new JWST/NIRSpec G395H transmission spectrum of WASP-127 b** (GO 2437, PI Pelletier).

## Key findings

- **SO₂-L vs equilibrium temperature: r = −0.64 ± 0.08** (strong negative). SO₂ photochemistry operates preferentially at T_eq ≲ 1200 K — consistent with VULCAN / Photochem predictions (Tsai 2023; Polman 2023 — not ingested).
- **SO₂-L vs planet mass: r = −0.41 ± 0.09** (moderate negative). SO₂ preferably exists in low-mass (≲ 0.3 M_J) targets. Driven by [[GJ3470b]] and [[WASP-107b]] (both with SO₂-L > 0).
- **SO₂-L vs host T_eff: r = −0.62 ± 0.08**. Likely a JWST-target-selection-induced degeneracy (cool low-mass planets orbit cool stars) but could partially reflect K-star SEDs driving higher SO₂ abundances via UV.
- **SO₂-L vs surface gravity: r = 0.00 ± 0.09** — no correlation. K_zz (vertical mixing) sensitivity to gravity not seen at this sample size.
- **SO₂-L vs bulk Z fraction: r = 0.25 ± 0.10 (full sample), r = 0.54 ± 0.10 for T_eq < 1400 K** — SO₂ traces metallicity, consistent with theory.
- **CO₂-L vs T_eq: temperature-dependent peak around ~900 K** for Z = 30× solar at C/O = 0.3 (PLATON forward models). No clear linear correlation.
- **CO-L vs T_eq: r = 0.46 ± 0.07** (moderate positive). CO becomes dominant carbon carrier at T_eq > 1000 K; **excluding WASP-121 b** the correlation drops to r = −0.21 ± 0.10. Useful index to study population-level C/O trends.
- **Population-level metallicity & C/O retrieval (PLATON forward grid).**
  - **Best fit: freely fitted mass-metallicity correlation + C/O = 0.3** (BIC = 232 over n = 8 planets at C/O grid 0.1, 0.3, 0.5, 0.7, 0.9, 1.1).
  - Solar System mass-metallicity trend less preferred: BIC = 617 vs uniform metallicity BIC = 295 at C/O = 0.3 → uniform metallicity is statistically *better* than the Solar-System trend with the present sample, but freely-fitted mass-metallicity is the genuine best fit.
  - **Low C/O (<0.7)** preferred; **super-solar metallicity (>3×)** preferred.
- **WASP-127 b new data.** First JWST/NIRSpec G395H transit (GO 2437, PI Pelletier; 2023 May 8). Observed at ~10% slit-loss flux deficit; JWST pointing stability (~0.01 pixel) minimized impact. Reduced per Rustamkulov 2023 (not ingested) + Sing 2024 (not ingested) procedures; orbital parameters fixed to Seidel 2020 (not ingested). Retrieved log g, T_eq from prior work (Seidel 2020).
- **WASP-39 b shows index disagreement between PRISM and G395H.** PRISM SO₂-L = −0.39 vs G395H SO₂-L = −0.08; CO₂-L 2.42 vs 2.89; CO-L 0.51 vs 0.32. Authors flag this as either instrumental calibration uncertainty or astrophysical; if future calibration programs demonstrate G395H is more accurate, the G395H index values should be used.
- **Color-color SO₂-L vs CO₂-L diagram.** Introduced as a framework for future population-level characterization. Upper-left region (high CO₂, low SO₂) is currently empty in the 8-planet sample — interpreted as either (i) clouds near 4 μm flattening continuum or (ii) a real bias in current targets; 56 additional planets in JWST Cycles 1, 2, 3 will fill the diagram.

## Methods

- **Sample selection.** Three criteria: (i) JWST 3–5 μm transmission coverage, (ii) precision sufficient for SO₂ and CO₂ band depths, (iii) M_p > 0.03 M_J (gas-giant H₂-dominated). 8 planets: [[GJ3470b]] (NIRCam F322W2+F444W; Beatty 2024 — not ingested), [[HIP67522b]] (NIRSpec G395H; Thao submitted), [[WASP-107b]] (G395H; Sing 2024 — not ingested), [[WASP-127b]] (G395H; this work), [[WASP-39b]] (NIRSpec PRISM; Carter & May), [[HD209458b]] (NIRCam F322W2+F444W; Xue 2023), [[HD189733b]] (NIRCam F322W2+F444W; Fu 2024), [[WASP-121b]] (G395H; [[2025_Gapp_WASP121b]]).
- **Band-index normalization.** Each transmission spectrum normalized by atmospheric scale height H = kT/μg using T_eq, μ = 2.3 amu, log g from literature; band indices = mean transit depth (scale heights) within band − L-band value.
- **Bulk Z fraction** via Thorngren 2016, 2019 (not ingested) approach. Chabrier 2019 EOS for H/He; ANEOS EOS for metals (50/50 water+rock mix); thermal evolution via Fortney 2007 atmosphere models. WASP-107 b uses Sing 2024 bulk metallicity (tidally heated; intrinsic-T-set adiabat).
- **Forward model grids.**
  - [[PICASO]] RCTE + [[Photochem]] (1D kinetics, Wogan et al. 2023) for SO₂ vertical-VMR predictions. Constant K_zz = 10¹⁰ cm² s⁻¹, T_int = 200 K, M_p = 0.42 M_J, R_p = 1 R_J, μ = 2.3 amu. Metallicity 1× to 100× solar; T_eq 500–2500 K.
  - [[PLATON]] (Zhang et al. 2020 — not ingested) for CO₂ and CO indices. Cloud-free equilibrium chemistry with isothermal TP profile; 7 metallicities (1×, 3×, 10×, 30×, 100×, 300×, 1000× solar); 6 C/O ratios (0.1, 0.3, 0.5, 0.7, 0.9, 1.1).
- **Statistical analysis.** Bootstrap correlation coefficient r with 1σ uncertainties; BIC = k·ln(n) + χ² grid evaluation for population-level metallicity + C/O fits.

## Caveats & limitations

- **8-planet sample.** Many correlations driven by 1–2 outliers (e.g. WASP-121 b drives CO-L vs T_eq; GJ 3470 b and WASP-107 b drive SO₂-L mass anti-correlation). Will grow in significance / fail with future JWST data.
- **Spectral-instrument mixing.** NIRSpec PRISM (R~100), NIRSpec G395H (R~2700), and NIRCam F322W2+F444W (R~1300) all included. Resolution effects on band-depth measurement are not explicitly corrected; could bias indices.
- **Cloud-free PLATON modeling.** Real atmospheres have aerosol continua that flatten band depths. The empty upper-left of the SO₂-L vs CO₂-L diagram could be cloud-driven rather than astrophysical.
- **Mass-radius assumption.** Bulk Z fractions assume 50/50 water+rock interior composition; ANEOS EOS. Different EOS choices change Z by ~0.1.
- **WASP-39 b PRISM-vs-G395H discrepancy** is unresolved — could affect the index values; the paper uses PRISM but flags G395H as the future-recommended dataset.
- **K_zz fixed at 10¹⁰ cm² s⁻¹ in Photochem models.** Real K_zz spans 10⁵–10¹⁰; high K_zz increases CH₄ depletion → could affect L-band reference.
- **WASP-107 b SO₂-L outlier on positive side (0.15 ± 0.14)** consistent with the tidally heated planet's enhanced internal energy and bulk Z (per Sing 2024); separate treatment needed for special-case planets.

## Open questions / follow-ups

- **Will SO₂-L vs T_eq correlation hold with the JWST Cycle 2 & 3 sample?** ~56 additional 3–5 μm transits available in next 1–2 years.
- **Color-color diagram fills.** The empty upper-left (high CO₂, low SO₂) region is the most diagnostic — does it remain empty as new spectra come in?
- **WASP-127 b atmospheric retrieval** as a standalone target — characterized for the first time in JWST in this paper but only treated at the index level.
- **HIP 67522 b atmosphere paper** (Thao et al. submitted) — the only sub-Neptune-mass target in the sample; first JWST atmospheric inference of a planet on a ~24 Myr T-Tauri-stage system.
- **Cross-validation against [[2025_Crossfield_SO2shoreline]].** That paper maps the SO₂ "1 ppm" shoreline at (T_eq, [M/H], C/O, K_zz, T_int, XUV); cross-population test should be possible once the SO₂-L band index can be computed on that paper's 936 grid.

## Related
- [[2025_Crossfield_SO2shoreline]] — theoretical population-grid paper mapping the SO₂ "shoreline" in (T_eq, [M/H]) space; this paper's empirical SO₂-L data should be directly comparable.
- [[2025_Gapp_WASP121b]] — WASP-121 b NIRSpec G395H transit paper providing the ultra-hot anchor; the only WASP-121 b spectrum used here.
- [[2025_RoyPerez_WASP39b]] — cloud-particle-properties analysis on WASP-39 b; demonstrates that cloud parameterization can shift abundances 4 dex — directly relevant to the cloud-driven flattening of band indices in this paper.
- [[2025_Fu_limb-asymmetry]] — separate Fu 2025 paper on NIRISS/SOSS limb asymmetry across 9 hot Jupiters; methodologically parallel but at a different wavelength range and focusing on limb-resolved (not band-integrated) information.
- [[SO2]] — concept hub for sulfur photochemistry in hot Jupiter / warm Neptune atmospheres.
- [[CO2]] — metallicity-tracer hub.
