---
type: paper
bibkey: 2025_Fu_limb-asymmetry
authors: [Fu, G., Mukherjee, S., Stevenson, K. B., Sing, D. K., Ashtari, R., Mayne, N., Lothringer, J. D., Zamyatina, M., Schmidt, S. P., Gascón, C., Allen, N. H., Bennett, K. A., López-Morales, M.]
year: 2025
venue: ApJL
arxiv: ""
doi: 10.3847/2041-8213/adf20f
targets: [WASP-107b, WASP-80b, HAT-P-18b, WASP-39b, WASP-166b, WASP-96b, WASP-52b, WASP-94Ab, WASP-17b]
instruments: [JWST-NIRISS, JWST-NIRSpec]
methods: [transmission-spectroscopy, atmospheric-retrievals]
codes: [PICASO, VIRGA, Catwoman]
tags: [hot-jupiter, limb-asymmetry, aerosols, clouds, population-study, niriss-soss, asymmetry-horizon]
ingested: 2026-05-04
---

# Overcast Mornings and Clear Evenings in Hot Jupiter Exoplanet Atmospheres

**Authors:** Fu, Mukherjee, Stevenson, Sing, Ashtari, Mayne, Lothringer, Zamyatina, Schmidt, Gascón, Allen, Bennett, López-Morales (2025, ApJL 989:L17) · [DOI:10.3847/2041-8213/adf20f]
**Targets:** [[WASP-107b]], [[WASP-80b]], [[HAT-P-18b]], [[WASP-39b]], [[WASP-166b]], [[WASP-96b]], [[WASP-52b]], [[WASP-94Ab]], [[WASP-17b]] · **Instrument:** [[JWST-NIRISS]] (SOSS), with [[JWST-NIRSpec]] PRISM cross-check on WASP-39 b

## TL;DR
A uniform reanalysis of all nine archival JWST/NIRISS/SOSS hot-Jupiter transmission spectra (T_eq ≈ 770–1740 K, log g 2.45–3.2 cgs) extracts **morning** (leading) and **evening** (trailing) limb spectra separately for each planet, using ingress/egress asymmetry as the discriminator. Three planets — [[WASP-39b]], [[WASP-94Ab]], [[WASP-17b]] — show prominent (> 5σ) muted morning / clear evening 1.4 μm H₂O contrast, requiring high-altitude (0.1–0.01 mbar) aerosols on the morning limb that must be removed on ~day timescales (downwelling vertical flow or dayside cloud evaporation). The paper introduces (1) the **Limb Spectroscopy Metric (LSM)** to predict limb-asymmetry SNR for future targets and (2) the **"asymmetry horizon"** — an empirical 2-D sigmoid fit in (T_eq, log g) space marking where aerosol-driven asymmetry is expected to emerge. Critically, **unrecognized limb asymmetry biases retrieved metallicity by up to +2 dex and underestimates limb temperature by ~½×** under conventional limb-averaged retrievals — a cautionary finding for the interpretation of every hot-Jupiter transmission paper that does not account for this effect.

## Key findings

- **Three of nine planets show >5σ morning–evening H₂O contrast** in the 1.4 μm water band (limb water index δA_H, in scale heights):
  - [[WASP-94Ab]] — δA_H = 2.83 ± 0.34 (strongest signal in the sample); T_eq = 1543 K.
  - [[WASP-39b]] — δA_H = 2.20 ± 0.31; T_eq = 1166 K. Independently confirmed via cross-checks against the NIRSpec/PRISM (Carter et al. 2024; not yet ingested) and three Espinoza et al. 2024 reductions.
  - [[WASP-17b]] — δA_H = 1.50 ± 0.25; T_eq = 1740 K.
- **Morning limbs are uniformly muted** across all nine planets (A_H within 2σ of zero). This means the aerosol coverage on the morning terminator is a near-universal feature in this temperature range, while clear evenings are restricted to specific planets.
- **Aerosol altitude requirement.** The muted-morning amplitude requires aerosols at 0.1–0.01 mbar on the morning limb and removed (or absent) at ~10⁻³–10⁻² bar on the evening limb. The transition timescale must match the limb-to-limb advection timescale (~day) — implicates downwelling vertical flow, dayside evaporation, or both.
- **Mechanism candidates** (Section 3.3):
  1. **Gravitational settling** alone removes only large (≳10 μm) particles within a year; insufficient for typical sub-μm hazes/grains. Stellar radiation pressure shortens this for ≲0.1 μm grains by ~year — still too slow.
  2. **Atmospheric vertical flow** at downwelling speeds tied to day–night ΔT can advect aerosols downward on the evening limb on day-timescales. Empirical fit to the analytical T. D. Komacek 2017/2019 framework reproduces the broad δA_H vs T_eq trend.
  3. **Condensation/evaporation cycling** of MgSiO₃, Na₂S, MnS as parcels cross the condensation curves (cooler nightside → hotter dayside).
  - All three likely operate together; observations cannot yet uniquely separate them.
- **1D forward-model interpretation ([[PICASO]] + [[VIRGA]]).** A grid in (δT_eq slope, log f_sed, T_off for MgSiO₃ shutoff) shows:
  - **Single MgSiO₃ cloud** alone produces a single morning–evening divergence near 1600 K — fits [[WASP-94Ab]] and [[WASP-17b]] but not [[WASP-39b]].
  - **MgSiO₃ + Na₂S + MnS** is required to produce the second divergence at ~1300 K seen in WASP-39 b (analog of the brown-dwarf L/T transition silicate-cloud clearance).
  - Best-fit slope δT(T_eq) = 0.66 × (T_eq − 500 K), log_10(f_sed) = −2.6, T_off = 1200 K for MgSiO₃.
- **Asymmetry horizon (Equation 1).** A 2-D sigmoid in (log T_eq, log g) space marks the transition from homogeneous-aerosol to clear-evening regimes; targets with strong δA_H cluster near the bottom-right of (T_eq, log g) space, consistent with the prediction that hotter, lower-gravity planets are more prone to limb asymmetry. Fitted parameters with 1σ uncertainties for future-target prediction.
- **Limb Spectroscopy Metric (LSM, Equation 7).** A new TSM-analog observability metric incorporating ingress/egress duration τ and impact parameter b, normalized to WASP-94 Ab. The empirical rescaling LSM_empirical = (0.27 × LSM^1.46)^(−1) gives δA_H error in scale heights — a planet with LSM_empirical = 1 is expected to deliver δA_H precision of 1H. The NASA Exoplanet Archive contains ~105 transiting planets with LSM_empirical > 1.
- **Quantitative bias from unmodeled asymmetry** (Section 4, Eq. 3 and Figure 11). For terminator cloud fraction f = ½ (one limb featureless, other clear), the limb-averaged retrieval underestimates scale height by ~½, biasing **metallicity by up to +2 dex** and **temperature by up to ½×** — illustrated explicitly with WASP-94 Ab (Ahrer et al. 2025) and WASP-17 b (Louie et al. 2025) where reported limb-averaged temperatures are ≈ 1300 K vs. equilibrium temperatures of 1543–1740 K. WASP-39 b free-retrievals (Lueber et al. 2024 vs. Espinoza et al. 2024) span ~2 dex in inferred H₂O abundance — the same effect.
- **Cool planets (WASP-107 b, WASP-80 b, HAT-P-18 b — T_eq < 1000 K)** show muted features on **both** limbs (δA_H ≈ 0 with morning and evening both featureless); plausible mechanisms (photochemical haze formation at low T_eq; reduced vertical flow; condensate sedimentation at altitude) cannot yet be discriminated. Broad UV–MIR coverage of both limbs would resolve cloud vs. haze.

## Methods

- **Sample.** All nine published JWST/NIRISS/SOSS hot-Jupiter transmission datasets as of mid-2025 (Table 1): GTO 1201 (WASP-107 b, WASP-52 b), GO 5924 (WASP-80 b, WASP-94 Ab), COM 2734 (HAT-P-18 b, WASP-96 b), [[JWST-ERS-1366]] (WASP-39 b), GO 2062 (WASP-166 b), [[JWST-TST-GTO-1353]] (WASP-17 b).
- **Limb-spectrum extraction.** Light-curve fitting via [[Catwoman]] (asymmetric two-semicircle transit model; Jones & Espinoza 2020; Espinoza & Jones 2021) + emcee, with reparameterization Rp1 = Rp − ΔRp/2, Rp2 = Rp + ΔRp/2 to alleviate the strong intrinsic Rp1↔Rp2 degeneracy. Free parameters per spectroscopic channel: visit-long slope, constant, midtransit time, Rp, ΔRp, inclination, a/R⋆, two LDC. Stagger 3D LDC values fixed.
- **Asymmetry visualization.** In/out-of-water-band (1.35–1.5 μm vs. 0.9–1.3 μm) light-curve residual differences provide a model-independent visualization of asymmetry that bypasses Catwoman degeneracies (Figure 3).
- **Limb water index A_H.** A_H is the in–out water-band transit-depth difference normalized to the equilibrium-T scale height (assuming μ = 2.3 amu); δA_H = A_H,evening − A_H,morning. Robust to absolute T₀ uncertainty, which only translates a wavelength-independent offset.
- **Forward modeling.** [[PICASO]] (atmosphere) + [[VIRGA]] (eddy-diffusion-balanced cloud microphysics) at 3× solar metallicity, solar C/O. Three cloud species (Na₂S, MnS, MgSiO₃); fixed K_zz = 10¹⁰ cm² s⁻¹; fitted (slope, f_sed, T_off) to match observed δA_H(T_eq).
- **NIRSpec PRISM cross-check on WASP-39 b** (Carter et al. 2024 reduction): morning/evening limb spectra recovered with consistent water-band shapes — the asymmetry is not a NIRISS/SOSS systematic.
- **Limb Spectroscopy Metric.** LSM ∝ (δ_atm/δ_ref) × √(10^[−0.4(J − J_ref)]) × √(τ/τ_ref), normalized to WASP-94 Ab; LSM_empirical = (0.27·LSM^1.46)^(−1) calibrated against measured δA_H errors.

## Caveats & limitations

- **Sample size of nine; only three planets dominate the asymmetry signal.** The empirical asymmetry horizon comes from this small population; extrapolation to other (T_eq, log g) regions is speculative.
- **1D parameterized atmospheric model.** Same TP-profile shape, equilibrium chemistry, K_zz, and cloud-condensation lines for all planets; planet-to-planet variation in these quantities can bias the condensation/evaporation interpretation. No photochemical haze production. Longer-wavelength (1.8, 2.5 μm) water bands could be affected differently by the simplified cloud treatments — only the highest-SNR 1.4 μm band is fit.
- **Tidal-locking assumption.** Morning = leading = entering during ingress; evening = trailing = exiting during egress. Assumes synchronous rotation with eastward equatorial jet.
- **Limb-averaged retrieval bias quantified analytically; not yet validated against full-grid limb-resolved retrievals.** The paper recommends grid retrievals over H₂O–CO₂ for accurate metallicity inference.
- **Stellar contamination mitigation.** FGK hosts in the sample are too hot to host significant photospheric H₂O, so stellar heterogeneity is unlikely to introduce water-feature limb asymmetry. Assumption fails for cooler hosts.
- **Different reductions of WASP-39 b NIRSpec PRISM** (Espinoza et al. 2024 NE/MM/Tiberius) yield slightly different morning/evening shapes; the consistency is qualitative (limb-asymmetry pattern reproduced) but not point-by-point.

## Open questions / follow-ups

- **Do sub-Neptunes and rocky planets show similar asymmetry?** All transiting planets are tidally locked; the same mechanism could operate, but δ_atm is too small for SOSS. Methane condensation curves on K2-18 b–type planets create analogous evening-clear / morning-cloudy potential (cited: Barrier & Madhusudhan 2025).
- **Is WASP-52 b's negative δA_H (clearer morning, muted evening) significant?** δA_H = −0.62 ± 0.41 — opposite sign to the other planets; needs follow-up to confirm.
- **Cloud vs. haze on the cool planets (T_eq < 1000 K).** UV–optical (cloud particle size) + 8–10 μm silicate features (cloud chemistry) needed to discriminate.
- **Day-resolved transit-to-transit variability.** Aerosol cycling on day timescales should produce night-to-night variation; multi-visit limb spectra would test the condensation/evaporation hypothesis.
- **GCM + cloud microphysics simulations** (T. D. Komacek et al. 2022) would close the loop between observed δA_H and the dominant transport process.

## Tensions

- **Limb-averaged vs. limb-resolved retrievals.** Reported metallicities/temperatures from prior limb-averaged retrievals on [[WASP-39b]] (Lueber et al. 2024 vs. Espinoza et al. 2024 — span ~2 dex in H₂O), [[WASP-94Ab]] (Ahrer et al. 2025 — T = 700–1000 K vs. T_eq = 1543 K), and [[WASP-17b]] (Louie et al. 2025 — T = 1272 K vs. T_eq = 1755 K) are likely **biased low in temperature and high in metallicity** by ~½× and +2 dex respectively because of unrecognized limb asymmetry. Recorded as a tension on [[atmospheric-retrievals]].
- **Single MgSiO₃ cloud (~1600 K transition) vs. multi-species clouds at 1300 K.** WASP-39 b's evening clearance is incompatible with MgSiO₃-only models, requiring Na₂S/MnS dissipation between 1200–1400 K. The exact dissipation mechanism for MgSiO₃ below ~1300 K is unknown — sedimentation, patchy clouds, vertical mixing, thermochemical instability all proposed but unresolved.

## Related

- [[2026_Radica_WASP96b]] — analyzed the same WASP-96 b NIRISS/SOSS dataset; reports limb-averaged H₂O, CO₂, Na detections. δA_H ≈ +0.91 ± 1.48 here is consistent with limb-averaged interpretation within errors but the larger error bar means WASP-96 b is **inconclusive** in the asymmetry sample.
- [[2025_Gressier_WASP17b]], [[2025_LustigYaeger_WASP17b]] — DREAMS WASP-17 b NIRISS dayside + NIRSpec G395H transit + nightside; this paper analyzes the GTO 1353 transit visit.
- [[2026_RoyPerez_WASP39b]] — pipeline systematics study on WASP-39 b NIRSpec PRISM; the inter-pipeline 2 dex variation in retrieved abundances is conceptually related to (but distinct from) the limb-asymmetry bias documented here.
- Cross-reference: limb-asymmetry concept page → [[limb-asymmetry]].
