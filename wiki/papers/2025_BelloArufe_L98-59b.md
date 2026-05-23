---
type: paper
bibkey: 2025_BelloArufe_L98-59b
authors: [Bello-Arufe, A., Damiano, M., Bennett, K. A., Hu, R., Welbanks, L., MacDonald, R. J., Seligman, D. Z., Sing, D. K., Tokadjian, A., Oza, A. V., Yang, J.]
year: 2025
venue: ApJL
doi: 10.3847/2041-8213/adaf22
targets: [L98-59b]
instruments: [JWST-NIRSpec]
methods: [transmission-spectroscopy, atmospheric-retrievals, stellar-contamination-modeling]
species_detected: [SO2]
species_tentative: []
species_ruled_out: []
codes: [Eureka, FIREFLy, ExoTR, Aurora, POSEIDON, MultiNest]
tags: [sub-earth, m-dwarf-host, rocky-planet, volcanic-atmosphere, sulfur-bearing, tidally-heated, cosmic-shoreline-challenger, magma-ocean]
ingested: 2026-05-16
---

# Evidence for a Volcanic Atmosphere on the Sub-Earth L 98-59 b

**Authors:** Bello-Arufe, Damiano, Bennett, Hu, Welbanks, MacDonald, Seligman, Sing, Tokadjian, Oza, Yang (2025, ApJL 980:L26; doi:10.3847/2041-8213/adaf22)
**Target:** [[L98-59b]] · **Host:** [[L98-59]] · **Instrument:** [[JWST-NIRSpec]] G395H · **Program:** JWST-GO-3942 (PI: Damiano)

## TL;DR

Four NIRSpec G395H transits (2.87–5.15 μm) of the **sub-Earth L 98-59 b** (R_p = 0.85 R⊕; T_eq ≈ 600–1000 K including tidal heating; on a 2.25-day orbit around the M-dwarf [[L98-59]]). The smallest exoplanet with a JWST transmission spectrum. Bayesian retrievals favor an **SO₂-dominated volcanic atmosphere** over a featureless flat line at **3.6σ** (Aurora simple model) / 3.37σ (ExoTR 14-parameter) / 3.6σ (POSEIDON nested without SO₂). Forward models from Seligman et al. 2024 (not ingested) and a self-consistent EPACRIS-Climate model of an SO₂-rich photochemical atmosphere both fit the data. The atmosphere has **>90% SO₂ at 68% confidence**, with H₂ < 24% (2σ), CO₂ < 84% (2σ), and no detection of H₂O, CH₄, H₂S, CO, NH₃. The signal — primarily two SO₂ absorption bands at 3.9–4.5 μm and 2.8–3.1 μm — would require **≥8× Io's tidal heating per unit mass**, implying a subsurface magma ocean spanning **60–90% of the planetary radius**, and an oxidized mantle with f_O₂ > IW + 2.7. The detection places L 98-59 b on the *atmosphere-bearing* side of the [[cosmic-shoreline]] despite its insolation/escape-velocity position predicting an airless world — a third independent shoreline challenger after [[TOI-270b]], [[2025_Teske_TOI561b]], and [[HD3167b]].

## Key findings

- **SO₂ at 3.6σ over flat line** (Aurora simple 2-parameter atmospheric model: planet radius + offset; pure 100% SO₂ assumed). Same data, more complex 14-parameter atmospheric retrieval (gas species + clouds + isothermal T + offsets): 3.3σ; LOO-CV cross-validation predictive-density improvement at 2.2σ. **Frequentist p-value of the flat-line model is 0.81** — cannot be rejected on its own.
- **ExoTR 14-parameter retrieval**: SO₂-bearing atmosphere preferred at 3.37σ over bare rock. The atmospheric T_iso = 596⁺¹²⁵₋₁₄₃ K — broadly consistent with T_eq ≈ 600 K. SO₂ inferred at >90% VMR (within 68% confidence) when allowed to be the bulk gas. Other species unconstrained or rejected (H₂O, CH₄, CO, NH₃, H₂S all consistent with non-detection).
- **POSEIDON 11-parameter retrieval**: SO₂-rich atmosphere preferred at ln(Z_atm) − ln(Z_flat) = 2.3 (Bayes factor 10, ~2.2σ for SO₂ in nested comparison without SO₂); 3.8σ when interdetector offset is excluded. H₂ mixing ratio < 24% at 2σ (rules out thick low-MMW envelopes); CO₂ < 84% at 2σ.
- **Spectrum amplitude ~50–80 ppm** with mean transit depth ~620 ppm. The 2.8–3.1 μm and 3.9–4.5 μm wavelength ranges show absorption consistent with the predicted SO₂ ν₁/ν₃ stretching bands.
- **Self-consistent volcanic-atmosphere model from Seligman et al. 2024 (not ingested)**: 98% SO₂ synthetic spectrum reaches χ² = 189.6 / 216 DOF — comparable fit quality to the flat-line. Coupled with the EPACRIS-Climate radiative-convective-photochemistry model run at 1× / 10× insolation: predicts steady-state SO₃ + S_x (elemental sulfur) atop the SO₂; ~400 K middle atmosphere temperature; mild thermal inversion in upper atmosphere from S₈ visible-band absorption.
- **Tidal-heating constraint**: Equating the inferred volcanic outgassing flux to the energy-limited XUV-driven atmospheric escape rate (≈ 2 × 10⁵ kg/s assuming 1% efficiency, balanced with Io-like outgassing scaling ≈ 1–2 × 10⁹ kg/s on Earth-like Mantle, requires *at least 8× Io's tidal heating per unit mass*. Tidal-Q upper limit Q_L98-59b ≲ 1400 Q_Io.
- **Subsurface magma ocean**: Combining tidal heating with the runaway-melting framework (Peale & Cassen 1978, applied to Io 1979), and assuming Love number k₂ ∈ 0.1–0.5, predicts a melted-mantle radius R_m ≈ 0.6–0.9 R_p — a substantial liquid interior.
- **Oxidized mantle**: An SO₂-rich (vs. e.g., H₂S- or H₂O-rich) outgassed atmosphere requires oxygen fugacity > IW + 2.7 (≥2.7 log units above iron-wüstite buffer), consistent with terrestrial mantle but not consistent with H₂O-dominated outgassing or strongly reduced primordial atmospheres.
- **Stellar contamination ruled out as primary signal**: Bayesian retrievals with explicit unocculted spot/faculae (POSEIDON M2 series) show only an SO₂-rich atmosphere model is consistently preferred over both flat line AND TLS-only scenarios at >3σ; TLS-only models are rejected at >12σ.

## Methods

**Observations.** [[JWST-NIRSpec]] G395H, BOTS mode, NRSRAPID + SUB2048 subarray, S1600A1 aperture; 3 groups × 2822 integrations per visit × 4 visits = 11,288 in-transit/out-of-transit integrations spanning 0.97 hr transit + ~3.7 hr baseline. Observed 2024 January 30 / February 3, 6, 19. Spectral coverage 2.87–3.71 μm (NRS1) + 3.83–5.15 μm (NRS2) with a Δλ = 0.1 μm detector gap. Program: JWST-GO-3942 (PI: Damiano).

**Two reductions:** [[Eureka]] v0.10 (default Stage 1–4 with 4σ→7σ jump threshold, mean group-level background subtraction, 13-pixel boxcar optimal extraction, 10σ outlier rejection in spatial profile) and [[FIREFLy]] (group-level 1/f corrected, lacosmic cosmic-ray cleaning, fourth-order polynomial trace fit, 4.8/5.3-pixel aperture). Both reductions agree within 1σ.

**Light-curve fitting:** batman transit model + emcee MCMC; orbital period fixed to literature; broad uniform prior on transit midtime; Gaussian priors on i and a/R_⋆ from Demangeon et al. 2021 (not ingested); broad uniform prior on R_p/R_⋆; quadratic limb-darkening fixed to ExoTiC-LD predictions (Magic et al. 2015 stellar models; T_eff = 3415 K, log g = 4.86, [Fe/H] = −0.46). White-noise multiplier accommodates correlated noise.

**Atmospheric retrieval frameworks:**
- **[[ExoTR]]** (Damiano et al. 2024; first wiki ingest of the code; cloud-as-water-VMR-profile, stellar heterogeneity, [[FastChem]]-equilibrium or free-chemistry abundances in centered-log-ratio space). 14 parameters: T_iso, cloud, R_p, NIRISS/NRS1/NRS2 offsets, 5 species CLR-prior abundances, heterogeneity fraction + temperature, stellar T_eff. MultiNest sampler, 800 live points. Used for both JWST-only and HST+JWST joint retrievals (HST/WFC3 spectrum from Damiano et al. 2022; not ingested).
- **[[Aurora]]** (Welbanks & Madhusudhan 2021; Bell et al. 2023). 14-parameter retrieval (8 species + isothermal T + cloud-top P + cloud fraction + reference P + R_p + NIRS1-NRS2 offset); also a 2-parameter simple "pure SO₂" retrieval. Resolution R = 20,000.
- **[[POSEIDON]]** (MacDonald & Madhusudhan 2017; MacDonald 2023). 11-parameter atmosphere model with patchy clouds + Rayleigh hazes; cross-checked with TLS-only and flat-line models. 2000 MultiNest live points.

Three retrieval frameworks agree to within 1σ on SO₂ abundance and qualitatively agree on the conclusion of an SO₂-rich atmosphere.

**Forward model cross-check.** **EPACRIS-Climate** (ExoPlanet Atmospheric Chemistry & Radiative Interaction Simulator; Scheucher et al. 2025, in preparation): radiative-convective-photochemistry climate model. SO₂-only initial atmosphere at Bond albedo 0; tidal heat fluxes of 1× and 10× insolation tested. Photochemistry network from R. Hu 2021; SO₂ photoexcitation drives SO₃ + S_x production. Stellar UV from MUSCLES survey GJ 176 spectrum (proxy for L 98-59).

## Caveats & limitations

- **Frequentist p-test cannot reject flat line** (p = 0.81). The result is a Bayesian-evidence detection: a model with SO₂ has higher log-evidence than a flat line, but the χ² of the flat-line model is itself acceptable. Different observational standards apply.
- **Wide range of SO₂ abundance consistent**: 70–98% (1× to 10× insolation models); 90% lower limit from 14-parameter retrieval. The data prefer "lots of SO₂" but cannot pin down the specific fraction.
- **No high-altitude tracer**: Stratospheric SO₂ photolysis products (SO₃, S₈, S_x) predicted at trace abundances; not detectable at present S/N.
- **Other gases unconstrained.** H₂S, CO₂, NH₃, CO, H₂O posteriors mostly fill the prior — formal 2σ upper limits only. The "SO₂ is the only firm gas" conclusion is partly a data-quality statement, not a chemistry one.
- **Stellar contamination cross-checks not exhaustive.** The 4-spot configuration adopted in spot-modeling assumes 1-component spot temperature; multi-component or faculae could mimic some of the signal. The Aurora 14-parameter and POSEIDON 7-parameter TLS models alleviate but do not eliminate this.
- **Tidal-heating inference is model-dependent.** The 8× Io estimate assumes a constant 1% atmospheric-escape efficiency and Io-like tidal-Q–volume scaling; uncertain factors of 2–3.
- **Magma-ocean radius (60–90% R_p) depends on k₂ assumption** (0.1–0.5 range tested); the runaway-melting equilibrium is sensitive to Love-number and viscosity.

## Open questions / follow-ups

- **Multi-visit / multi-instrument confirmation.** Bello-Arufe estimates ~6 more transits would push the SO₂ detection past 5σ — relatively achievable on this bright (J = 7.9), short-period system.
- **MIRI/LRS follow-up for SO₂ ν₂ band at 7.5 μm.** The two NIRSpec G395H-detected bands lie at 3.9–4.5 μm + 2.8–3.1 μm; an independent test at 7.5 μm would discriminate against systematics.
- **Is there an [[SO2-photochemical-shoreline]] analog for volcanic SO₂?** The Crossfield et al. 2025 SO₂-shoreline framework targets photochemical SO₂ in H₂-rich atmospheres; volcanic SO₂ on rocky planets is a distinct production channel but the same spectroscopic feature.
- **Companion-planet diversity.** [[L98-59c]] (sub-Earth, [[2024_Scarsdale_L98-59c]] featureless) and [[L98-59d]] (sulfur-bearing tentative, [[2024_Gressier_L98-59d]] / [[2024_Banerjee_L98-59d]]) are also in this system. Three rocky planets, three different inferred atmospheric states — a system-scale test of M-dwarf rocky atmosphere theory.
- **What's the volcanic outgassing rate on Io-analog tidally-heated rocky exoplanets?** Bello-Arufe argues for ≥8× Io mass-normalized; future characterization of TRAPPIST-1 e, GJ 1132 b, and other tidally-heated rocky planets is the population test.
- **[[cosmic-shoreline]] population reformulation.** L 98-59 b is a fourth wiki target whose JWST atmospheric inference *contradicts* the Zahnle & Catling 2017 (not ingested) shoreline placement; the empirical shoreline may be different for tidally-heated planets.

## Related

- [[L98-59c]] — companion super-Earth in the same system; featureless [[JWST-GO-2512-COMPASS]] PRISM spectrum ([[2024_Scarsdale_L98-59c]]).
- [[L98-59d]] — companion sub-Neptune in the same system; tentative S-bearing atmosphere ([[2024_Gressier_L98-59d]], [[2024_Banerjee_L98-59d]]); cited here as supporting evidence for system-wide widespread mantle melting (Gressier 2024 + Banerjee 2024).
- [[SO2]] — first wiki SO₂ detection on a rocky planet; previously only seen on hot Jupiters / warm Neptunes (WASP-39 b, WASP-107 b, HAT-P-26 b, V1298 Tau b).
- [[cosmic-shoreline]] — fourth wiki shoreline challenger; airless-side placement contradicted by atmospheric inference.
- [[GJ486b]] — previous most-promising "volcanic atmosphere" candidate; emission spectrum retrieved no atmosphere ([[2024_WeinerMansfield_GJ486b]]) and transmission analyzed as airless/spotted star ([[2023_Moran_GJ486b]]). L 98-59 b is a different candidate class because of greater tidal heating.
- [[2025_Madhusudhan_subneptunes]] — review paper; cites L 98-59 b as an atmospheric-detection candidate.
- Damiano et al. 2022 + Zhou et al. 2022 (HST/WFC3 transmission of L 98-59 b; both not ingested) — pre-JWST cloud-free H₂-rich rejection; consistent with high-MMW atmosphere allowed here.
- Seligman et al. 2024 (not ingested) — theoretical volcanic-atmosphere predictions on L 98-59 b; the synthetic spectra at 5/50/98% SO₂ used directly in this paper.
