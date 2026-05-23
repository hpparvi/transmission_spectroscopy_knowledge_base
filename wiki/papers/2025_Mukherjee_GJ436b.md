---
type: paper
bibkey: 2025_Mukherjee_GJ436b
authors: [Mukherjee, S., Schlawin, E., Bell, T. J., Fortney, J. J., Beatty, T. G., Greene, T. P., Ohno, K., Murphy, M. M., Parmentier, V., Line, M. R., Welbanks, L., Wiser, L. S., Rieke, M. J.]
year: 2025
venue: arXiv
arxiv: 2502.17418
targets: [GJ436b]
instruments: [JWST-NIRCam, JWST-MIRI]
methods: [secondary-eclipse-spectroscopy, atmospheric-retrievals]
species_detected: []
species_tentative: [CO2]
species_ruled_out: []
codes: [Tshirt, Eureka, PICASO, Photochem, MultiNest, VIRGA]
tags: [warm-neptune, m-dwarf-host, emission-spectroscopy, panchromatic, manatee, spitzer-disagreement, low-tint, metallicity-revision, cloudy]
ingested: 2026-05-16
---

# A JWST Panchromatic Thermal Emission Spectrum of the Warm Neptune Archetype GJ 436b

**Authors:** Mukherjee, Schlawin, Bell, Fortney, Beatty, Greene, Ohno, Murphy, Parmentier, Line, Welbanks, Wiser, Rieke (2025, arXiv:2502.17418)
**Target:** [[GJ436b]] · **Host:** [[GJ436]] · **Instruments:** [[JWST-NIRCam]] (F322W2 + F444W) + [[JWST-MIRI]] LRS · **Program:** JWST-GO-1177 + JWST-GO-1185 (MANATEE; PI: Schlawin)

## TL;DR

**First panchromatic 2.4–12 μm JWST thermal emission spectrum of GJ 436 b** — the archetype warm Neptune (M_p = 25.43 M⊕, R_p = 4.03 R⊕, P = 2.64 d, e = 0.16 around an M-dwarf). Eight eclipses (3× NIRCam F322W2 + 3× NIRCam F444W + 2× MIRI/LRS) under the **MANATEE survey** ([[JWST-GO-1177]] + [[JWST-GO-1185]], PI: Schlawin). **The JWST 3.6 μm flux is significantly fainter than Spitzer photometry** — overturning the longstanding Spitzer-era inference of extreme metallicity (≥hundreds × solar) and hot interior (T_int ≥ 300 K) driven by tidal dissipation. **Day-side T_day = 662.8 ± 5.0 K** ≈ zero-albedo equilibrium temperature (675 K); Bond albedo upper limit A_B ≤ 0.66 (3σ). Free-chemistry retrieval finds **weak CO₂ evidence at 2σ** (log VMR ≈ −3.23⁺¹·⁶⁶₋₃·₃₀); no other molecule above 3σ. Self-consistent forward modeling:
- **Cloudy [[FastChem]]-equilibrium with [M/H] ≥ 300× solar (1σ); ≥ 500× solar best-fit** OR
- **Clear disequilibrium with [M/H] ≥ 80× solar (2σ); ≥ 130× solar (1σ), T_int ~ 60 K**
These metallicities are an order of magnitude lower than Spitzer-era inferences (Stevenson 2010, Morley 2017 not ingested). The T_int ~ 60 K result contradicts the Spitzer-era T_int ≥ 300 K consequence of tidal heating; instead the planet's interior may be much cooler than long assumed.

## Key findings

- **8-eclipse panchromatic emission spectrum** spanning 2.4–12 μm. Two independent reductions ([[Tshirt]] and [[Eureka]]) agree at < 1σ for NIRCam (3 each), within 1σ for MIRI (2 each).
- **JWST is significantly fainter than Spitzer at 3.6 μm.** Stevenson et al. 2010 (Spitzer IRAC) and Morley et al. 2017 (Spitzer reanalysis) both reported high 3.6 μm flux (~120–200 ppm). JWST NIRCam F322W2 measures ~50 ppm in this band. Mukherjee et al. (Section 8.7) refit two unpublished 2018 Spitzer phase-curve eclipses (PI Parmentier) and find 46 ± 43 ppm — consistent with JWST at 2.8σ lower than Morley 2017.
- **Day-side T_day = 662.8 ± 5.0 K.** Isothermal-atmosphere retrieval; consistent with T_eq = 675 K (zero-albedo, full-redistribution). Bond albedo + heat-recirculation efficiency (ε) corner plot: A_B = 0.43⁺⁰·²³₋₀·₄₀; ε = 0.62⁺⁰·³⁸₋₀·⁴². 3σ upper limit A_B ≤ 0.66.
- **GJ 436 b and GJ 1214 b are unique** among non-terrestrial planets observed by JWST in having T_day / T_eq ≤ 1 (i.e., day-side colder or equal to equilibrium temperature). All other gas-giant JWST targets are *hotter* than T_eq. This may reflect either high albedo or extreme metallicity (e.g., the GJ 1214 b conclusion from Kempton et al. 2023, not ingested).
- **CO₂ tentatively detected at 2σ.** Free-chemistry retrieval gives log VMR(CO₂) = −3.23⁺¹·⁶⁶₋₃·₃₀; CO and SO₂ upper limits log VMR < −4.5 and −5.0 at 2σ. No firm detection of CH₄, H₂O, NH₃, HCN, C₂H₂, H₂S, OCS.
- **Self-consistent equilibrium models prefer high metallicity ([M/H] ≥ 300× solar at 1σ).** [[PICASO]] RCTE grid over 13 [M/H] (−1 to +2.9), 6 C/O, 5 T_int (60–400 K), 9 heat-redistribution factors. Best fit: [M/H] = +2.7, C/O = 0.1× solar, T_int = 100 K, r_facv = 0.6.
- **Disequilibrium chemistry models prefer lower metallicity.** PICASO + [[Photochem]] grid with K_zz = 10⁶ / 10⁸ / 10¹⁰: best-fit [M/H] = +2.7, C/O = 0.1× solar, T_int = 100 K. **But the 1σ lower limit drops to [M/H] ≥ +1.9; 2σ to ≥ +1.5** (i.e., 80–130× solar). Disequilibrium chemistry allows much lower metallicities than equilibrium chemistry.
- **Cloudy equilibrium models** (with [[VIRGA]] KCl + Na₂S clouds; f_sed = 0.5, log K_zz = 9): best-fit [M/H] = +2.9, C/O = 1.0× solar, r_facv = 0.7. Lower bound [M/H] ≥ +2.5 (1σ) / ≥ +2.1 (2σ).
- **T_int ≈ 60 K, not ≥ 300 K.** The Spitzer-era tidal-heating-driven hot-interior hypothesis (Morley 2017 not ingested; required T_int ≈ 300–400 K to suppress CH₄ via vertical mixing) is **not supported** by the fainter JWST 3.6 μm flux. JWST flux *allows* a cold interior (T_int ≈ 60 K) which is more consistent with stellar-age evolutionary models.
- **HST/WFC3 transmission consistent.** The Knutson et al. 2014a (not ingested) flat HST/WFC3 transmission spectrum is consistent with the cloudy-equilibrium model from this work (cloud deck obscures features). Cloud-free metal-poor models are ruled out by HST/WFC3 + JWST.
- **Comparison to high-resolution CRIRES+.** Grasser et al. 2024 (CRIRES+ transmission; not ingested) ruled out cloud-free metal-poor atmospheres at high spectral resolution. The new JWST emission-spectrum inference is consistent: metal-rich + cloudy.
- **No phase-curve constraint.** A future phase curve of GJ 436 b would distinguish whether the low day-side temperature reflects high albedo (A_B → 1, ε → 1) or extreme metallicity (high MMW, low scale height). This is currently degenerate.

## Methods

**Observations.** [[JWST-GO-1177]] + [[JWST-GO-1185]] (MANATEE survey; PI: E. Schlawin). 8 eclipses:
- 3× [[JWST-NIRCam]] F322W2 grism (2.4–4.0 μm) at 85 nm/87 px binning
- 3× [[JWST-NIRCam]] F444W grism (3.9–5.0 μm) at 63 nm/65 px
- 2× [[JWST-MIRI]] LRS (5–12 μm) at 250 nm binning

All collected 2022-12-07 → 2023-12-21. Eclipse duration T_14 = 1.02 hr; baseline 2.65–2.74 hr.

**Two reductions.**
- **[[Tshirt]]** (Schlawin et al. 2020): custom jwst-pipeline replacement with ROEBA 1/f correction; 6σ jump rejection; covariance-weighted optimal extraction. NIRCam: 10-pixel full aperture; MIRI: 8-pixel.
- **[[Eureka]]** v0.11 dev (Bell et al. 2022): standard Stage 1–6. NIRCam: 6σ jump rejection; lastframe trimming; mean column background. MIRI: 8σ jump; row-by-row 90° rotated background. GP detrending with celerite2 + Matérn-3/2 kernel for MIRI; FPAH temperature + reference-pixel correlation vectors for NIRCam.

Two reductions agree at ≲ 1σ; tshirt used for the science spectra.

**Atmospheric retrieval.**
- [[PICASO]] free-chemistry 17-parameter retrieval: T(P) Madhusudhan-Seager 2009 6-parameter profile; 11 free volume mixing ratios (H₂O, CH₄, CO₂, CO, NH₃, N₂, HCN, C₂H₂, OCS, H₂S, SO₂); R = 60,000 native opacities binned to data resolution. PyMultiNest 2000 live points.
- Isothermal blackbody retrieval (1 parameter T_iso) used to derive T_day, A_B, ε via Cowan & Agol 2011 (not ingested) methodology.

**Self-consistent forward models.**
- **[[PICASO]] RCTE** (radiative-convective-thermochemical-equilibrium) grid: 2700 models. χ² minimization + grid Bayesian-weight corner plot.
- **PICASO + [[Photochem]] disequilibrium** grid: 2700 × 3 K_zz values = 8100 models.
- **PICASO + [[VIRGA]] cloud** grid: cloudy variant with KCl + Na₂S condensates; f_sed and K_zz varied. Post-processed (not radiatively self-consistent).

**Stellar spectrum.** GJ 436 stellar parameters from JWST: T_eff = 3648 K, R = 0.41 R_⊙, log g = 4.47, [M/H] = +0.5, [C/M] = −0.5 fit against BOSZ stellar atmosphere models. Planet radius R_p = 0.329 R_J derived using the JWST stellar radius + Bourrier et al. 2018 (not ingested) R_p/R_⋆ ratio.

## Caveats & limitations

- **Equilibrium vs disequilibrium metallicities differ by factor of ~3** in 1σ lower bounds (300× vs 100×). Both fit the data nearly equally well; the discriminator requires either better S/N or independent abundance measurements (CO or H₂O detection at 5σ would help).
- **Self-consistent cloudy models are not radiatively coupled.** VIRGA clouds are post-processed onto cloud-free RCTE P-T profiles; full self-consistency (cloud opacity feedback on T(P)) not implemented.
- **Phase curve / day-night gradient unknown.** Single-side eclipses can't distinguish high albedo + efficient redistribution from clear extreme-metallicity + inefficient redistribution.
- **Spitzer 3.6 μm flux outlier vs JWST is unexplained at high confidence.** The reanalysis of two 2018 unpublished phase-curve eclipses (PI Parmentier) confirms a 46 ± 43 ppm depth — closer to JWST than to Morley 2017. The Stevenson 2010 + Lanotte 2014 depth must be a sub-pixel pointing/sweet-spot artifact (consistent with Murphy 2023 not ingested on Spitzer pointing reliability).
- **No CO detection** despite predicting CO as a major C-bearing species in disequilibrium models. Disequilibrium may not be vigorous enough at the inferred 100× solar metallicity to produce detectable CO.
- **Stellar spectrum mismatch at optical.** Fitting both UV-optical + JWST simultaneously is inconsistent; JWST alone gives well-behaved stellar parameters.

## Open questions / follow-ups

- **Phase curve of GJ 436 b** would discriminate the high-albedo vs high-metallicity degeneracy. With JWST, a partial phase curve at NIRCam F444W is feasible.
- **Transmission spectrum at JWST resolution.** Knutson et al. 2014a HST/WFC3 transmission was featureless; JWST transmission would test cloud-deck pressure (~10 bar in current best-fit) directly. NIRSpec G395H or PRISM transmission would be informative.
- **Comparison to GJ 1214 b and HD 149026 b.** Both are warm/cool Neptunes with JWST data; GJ 436 b is now the third in this class.
- **Tidal heating revisited.** With T_int ≈ 60 K, tidal heating doesn't need to be invoked at the 300 K level — but the eccentricity (e = 0.16) still demands a dissipation mechanism. Where does the heat go?
- **CO at 5σ?** A 4–5σ CO detection in further visits would unambiguously settle the disequilibrium-vs-equilibrium debate.

## Related

- [[GJ486b]] — different M-dwarf rocky planet; emission spectroscopy retired the [[2023_Moran_GJ486b]] water-rich transmission interpretation. Methodology parallel: emission resolves transmission ambiguity.
- [[2024_WeinerMansfield_GJ486b]] — MIRI/LRS eclipse spectroscopy; the type of work that this paper does at panchromatic NIRCam + MIRI for a warm Neptune.
- Morley et al. 2017 (Spitzer reanalysis; not ingested) — the canonical pre-JWST analysis of GJ 436 b; metallicity inferences (~hundreds × solar) now revised downward.
- Stevenson et al. 2010 (Spitzer; not ingested) — original GJ 436 b multi-band photometry showing high 3.6 μm flux.
- Grasser et al. 2024 (CRIRES+ transmission; not ingested) — high-resolution complement; rules out cloud-free metal-poor.
- Bell et al. 2024 (Nature MANATEE; not ingested) — methodology paper for the MANATEE survey reduction pipeline.
