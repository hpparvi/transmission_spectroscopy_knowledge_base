---
type: concept
aliases: [morning-evening asymmetry, limb-to-limb asymmetry, terminator asymmetry, asymmetry horizon, Limb Spectroscopy Metric, LSM]
tags: [transmission-spectroscopy, hot-jupiter, aerosols, clouds, retrieval-bias]
---

# Limb asymmetry

The morning (leading) and evening (trailing) terminators of a tidally locked transiting planet are observed at different times during transit ingress vs. egress, and probe atmospheric parcels with different thermal histories — the morning limb has just emerged from the cool nightside, while the evening limb has just crossed the hot dayside. For hot Jupiters this introduces measurable differences in **temperature** (a few hundred K hotter on the evening limb) and **aerosol coverage** (cloud condensation/evaporation cycles can leave the morning cloudy and the evening clear, or vice versa). [[2025_Fu_limb-asymmetry]] uniformly reanalyzes nine archival JWST/NIRISS/SOSS hot-Jupiter spectra for limb-resolved transmission and shows that **3/9 planets ([[WASP-39b]], [[WASP-94Ab]], [[WASP-17b]]) display > 5σ morning–evening 1.4 μm water-band contrast** in the predicted muted-morning / clear-evening direction.

The signal is extracted via asymmetric two-semicircle transit-light-curve fitting ([[Catwoman]]), or via the model-independent in-vs-out-of-water-band light-curve residual differences during ingress vs. egress.

## Mechanisms

A persistent morning–evening difference in aerosol opacity requires aerosol removal on a timescale comparable to the limb-to-limb advection timescale (~day for hot Jupiters). The plausible drivers identified in [[2025_Fu_limb-asymmetry]]:

1. **Atmospheric vertical flow.** Day–night thermal contrast drives downwelling on the evening terminator and upwelling on the morning terminator (Showman et al. 2009; Steinrueck et al. 2021). Stronger temperature contrasts → stronger downwelling → faster aerosol removal from the evening limb. Predicts a monotonic δA_H vs. T_eq trend.
2. **Condensation–evaporation cycling.** Aerosol parcels cross condensation curves between dayside and nightside. Sets a non-monotonic, sawtooth-like δA_H(T_eq) shaped by the species in question (MgSiO₃ near 1300–1600 K; Na₂S/MnS at lower T).
3. **Gravitational settling + stellar radiation pressure.** Removes only large (>10 μm) particles within a year; insufficient for sub-μm hazes/grains. Disfavored as the dominant limb-clearing mechanism.

All three likely operate together; transmission alone cannot uniquely separate them — UV/optical for particle size and 8–10 μm silicate features for cloud chemistry are needed.

## Asymmetry horizon

An empirical 2-D sigmoid in (T_eq, log g) space fitted to the nine-planet δA_H sample ([[2025_Fu_limb-asymmetry]] Eq. 1, Figure 7):
$$\delta A_H = z / (1 + e^{-k(m\,T_{eq} - \log g + c)})$$

Best-fit parameters: m = 9.0 × 10⁻⁴ ± 3 × 10⁻⁴, c = 1.642⁺⁰·²⁴⁻⁰·³⁴, z = 2.034⁺⁰·²³⁻⁰·¹⁶, k = 579.2⁺²⁹⁰⁻³⁰⁷. Planets with strong δA_H cluster in the bottom-right (high T_eq, low log g). The contour where the sigmoid reaches ½ its maximum value is the **asymmetry horizon**: the predicted boundary above which limb-to-limb aerosol asymmetry should emerge in JWST observations.

## Limb Spectroscopy Metric (LSM)

A TSM-analog observability metric for limb-resolved transmission spectroscopy ([[2025_Fu_limb-asymmetry]] Eqs. 5–10). LSM scales with the per-scale-height feature size δ = 2HR_p/R_⋆², the J-band flux, and the ingress/egress duration τ:

$$\text{LSM} = (\delta/\delta_{\text{ref}}) \sqrt{10^{-0.4(J - J_{\text{ref}})}} \sqrt{\tau/\tau_{\text{ref}}}$$

normalized to [[WASP-94Ab]] (δ_ref = 234.6 ppm, J_ref = 9.159, τ_ref = 25.22 min). Empirically rescaled as LSM_empirical = (0.27 × LSM^1.46)⁻¹ to give δA_H error in scale heights — LSM_empirical = 1 → 1H precision on δA_H. The NASA Exoplanet Archive contains ~105 transiting planets with LSM_empirical > 1.

## Retrieval-bias implication

For terminator cloud-fraction f, the limb-averaged transmission spectrum has slope d ln σ / d ln λ reduced by a factor (1 − f) ([[2025_Fu_limb-asymmetry]] Eq. 3, after Line & Parmentier 2016). To recover the same scale height under the limb-averaged interpretation, a retrieval **inflates the mean molecular weight by 1/(1−f) and deflates the temperature by (1−f)**. For f = ½:

- **Metallicity bias:** up to **+2 dex** (true 10× solar can be retrieved as 1000× solar).
- **Temperature bias:** up to **−½×** of the true limb temperature.

Documented WASP-39 b, WASP-17 b, WASP-94 Ab cases show retrieved limb-averaged temperatures hundreds of K below their equilibrium temperatures, and inferred metallicities 1–2 dex apart between independent retrievals on the same data — a signature of unrecognized limb asymmetry. Recommendation: grid retrievals leveraging H₂O–CO₂ ratios are more robust to this bias than free retrievals.

## Chemical heterogeneity between limbs

Beyond temperature and aerosol asymmetries, **panchromatic limb-resolved JWST spectra resolve molecular abundance gradients**. [[2025_Murphy_WASP107b]] reanalyzes WASP-107 b's full JWST suite (NIRCam F322W2 + F444W, NIRISS/SOSS, NIRSpec G395H, MIRI LRS) and finds the morning limb has ~5× more [[SO2]] and ~40× more [[CO2]] than the evening — while [[H2O]] is uniform between limbs. The drivers separate cleanly: SO₂ is photochemical (production on dayside, transport to nightside), CO₂ is quench-driven (lower-pressure quench than CH₄ → still tracks T-gradient at the photosphere), H₂O is rapidly homogenized by circulation. In addition, the morning limb of WASP-107 b carries a strong broad 6–11 μm cloud feature absent from the evening limb. Murphy 2025 notes that occulted starspot crossings systematically biased the NIRISS/SOSS and NIRSpec/G395H limb spectra (NIRCam and MIRI clean); a [[Catwoman]] + `starry` injection-recovery correction is needed to bring all instruments into agreement — providing further context for the [[stellar-contamination]] complications in limb spectroscopy on active stars.

## Papers
- [[2025_Murphy_WASP107b]] — Murphy et al. 2025, AJ 170:61 — panchromatic 1–12 μm limb-resolved analysis of [[WASP-107b]]; first detection of SO₂, CO₂, and cloud heterogeneity between limbs; spot-correction methodology for limb-resolved spectra; reframes the WASP-107 b "no asymmetry" classification from [[2025_Fu_limb-asymmetry]].
- [[2025_Fu_limb-asymmetry]] — Fu et al. 2025, ApJL 989:L17 — population-level reanalysis of 9 NIRISS/SOSS hot-Jupiter spectra; introduces LSM and asymmetry horizon; quantifies up to +2 dex metallicity / ½× temperature retrieval bias.
