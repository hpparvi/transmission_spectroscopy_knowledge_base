---
type: paper
bibkey: 2026_Wogan_LTT1445Ab
authors: [Wogan, N. F., Batalha, N. E., Ih, J., Lustig-Yaeger, J., Stevenson, K. B.]
year: 2026
venue: arXiv preprint (May 2026)
arxiv: 2605.14997
doi: ""
targets: [LTT1445Ab]
instruments: [JWST-MIRI]
methods: [secondary-eclipse-spectroscopy, atmospheric-retrievals, climate-constrained-inversion]
species_detected: []
species_ruled_out: [CO2, H2O, SO2]
codes: [Photochem, PICASO, SPHINX, MultiNest, easyCHEM]
tags: [terrestrial, m-dwarf-host, climate-constrained, bayesian-inversion, cosmic-shoreline, rocky-worlds-ddt]
ingested: 2026-05-22
---

# A Climate-Constrained Bayesian Inverse Method for JWST Rocky Exoplanet Eclipse Spectra: A Case Study of LTT 1445A b

**Authors:** Wogan, Batalha, Ih, Lustig-Yaeger, Stevenson (2026, arXiv:2605.14997) · submitted May 2026
**Target:** [[LTT1445Ab]] · **Instrument:** [[JWST-MIRI]] LRS (5–12 μm; data from [[JWST-GO-2708]] / [[2024_Wachiraphan_LTT1445Ab]])
**Forecast for:** Future MIRI/F1500W eclipses via the Rocky Worlds DDT program

## TL;DR

Introduces a **climate-constrained Bayesian inversion** framework for interpreting JWST rocky-planet eclipse spectra: instead of using a free-retrieval code (e.g. [[POSEIDON]]) with parameterized P–T profiles, the inversion fits the observed eclipse depths against a precomputed grid of self-consistent **radiative–convective-equilibrium** atmospheres built with [[Photochem]]'s `Clima` 1.5-D climate model and [[PICASO]] radiative transfer. The forward grid spans 7 atmospheric parameters (4 partial pressures of CO₂/H₂O/O₂/SO₂, heat-engine efficiency χ, surface albedo, T_eq,0) for a total of 684 000 atmospheres precomputed on 512 CPU cores (~3.5 h). Applied to the [[2024_Wachiraphan_LTT1445Ab]] MIRI/LRS spectrum, the inversion **prefers the bare-rock model at K_bare/atm = 11 (16-bin) / 7 (8-bin)** — i.e. an atmosphere is not required. If an atmosphere is present, the 2σ upper limits are P_s ≤ 0.6 bar (total) ≤ 1 bar of optically thin gas (O₂/N₂/CO), ≤ 0.1 bar CO₂, ≤ 10⁻³ bar H₂O, ≤ 10⁻⁴ bar SO₂. **Forecasts** that scheduled MIRI/F1500W observations under the Rocky Worlds DDT program could *detect* one of the thicker atmospheres still allowed by the LRS (~1 bar O₂ + 0.01 bar CO₂, A_s = 0.2) at a Bayes factor of 35 *if* 20 ppm precision is achieved — estimated to need ≥ 4 visits. The methodology is positioned as the rocky-planet emission-spectrum analog of equilibrium-chemistry transmission retrievals: it turns JWST eclipse spectra into the quantitative pressure constraints needed for population-level tests of the [[cosmic-shoreline]].

## Key findings

- **K_bare/atm = 11 (16-bin) / 7 (8-bin)**: bare rock moderately favored over the climate-constrained atmospheric model. ΔAIC = −9.1 (16-bin) / −7.6 (8-bin) reinforces this with a frequentist check (Thorngren 2026 not ingested).
- **2σ surface-pressure upper limit P_s ≤ 0.6 bar** (16-bin); ≤ 1.8 bar (8-bin sensitivity test); ≤ 5 bar (no-heat-redistribution stress test).
- **Species upper limits (16-bin, 2σ)**: log P_H₂O < −2.6 bar; log P_CO₂ < −1.0 bar; log P_O₂ < −0.2 bar (1 bar); log P_SO₂ < −4.0 bar.
- **Thickest 2σ-permitted atmosphere**: ~1 bar O₂ with ~0.1 bar CO₂ — i.e., an optically thin O₂/N₂/CO-dominated atmosphere is the only thick scenario the LRS still allows.
- **Adopted O₂ as a proxy** for the sum of all low-opacity gases (O₂, CO, N₂) — the spectra are nearly identical between 1-bar O₂, N₂, and CO atmospheres in the MIRI/LRS bandpass; abundances of those gases individually are unconstrained.
- **Atmosphere prior built from XUV history**: H/He, H₂, CH₄, NH₃ are *not* permitted in the inversion. LTT 1445A b's pre-main-sequence XUV irradiation would have stripped H-bearing primary atmospheres ([[2024_Wachiraphan_LTT1445Ab]], Krissansen-Totton 2024 not ingested). Only CO₂/H₂O/O₂/SO₂ atmospheres are considered plausible secondary atmospheres.
- **F1500W forecast**: a 20-ppm-precision F1500W eclipse measurement of the thickest still-allowed atmosphere (1 bar O₂ + 0.01 bar CO₂, A_s = 0.2) yields **K_atm/bare = 35** — strong evidence for an atmosphere. ETC + Greene 2023 precision-scaling gives ≥4 visits to reach 20 ppm.
- **Aerosols**: photochemical sulfate/sulfur, KCl, and H₂O clouds all rejected (saturation factor ~10⁻⁷ for KCl, undersaturation ~3500× for H₂O at posterior P–T). Surface-lofted dust (Mars analogue) is the most plausible aerosol; including it *strengthens* (lowers) the upper limit on surface pressure rather than weakening it.
- **Photochemical O₃** (from O₂-rich atmospheres) is shown to produce at most a ~9 μm 16 ppm feature, smaller than the median 19.5 ppm error of the current LRS data — neglecting photochemistry in the main inversion is a defensible approximation at this S/N.
- **Climate-constrained vs free retrieval**: framework restricts inference to *physically self-consistent* radiative–convective-equilibrium P–T profiles; this is the rocky-planet emission analog of equilibrium-chemistry retrievals for sub-Neptunes (e.g. [[2025_Felix_TOI-270d]], [[2025_Coulombe_TOI-270b]]).

## Methods

- **Forward model** (Figure 1):
  - **Climate**: [[Photochem]] / Clima v0.8.2 (Wogan 2026 not ingested) — 1.5-D radiative–convective-equilibrium model with day-night heat redistribution parameterized by heat-engine efficiency χ (Koll 2022 not ingested).
  - **Stellar SED**: [[SPHINX]] grid (T_eff = 3340 K fixed; LTT 1445 A [Fe/H] = −0.34 from Winters 2019 not ingested).
  - **Spectral RT**: [[PICASO]] v4 (Batalha 2019 not ingested; Mang 2026 not ingested) — opacities for CO₂, H₂O, O₂, SO₂ + CIA H₂O-H₂O / O₂-O₂ / CO₂-CO₂ (Mlawer 2012 MT_CKD).
- **Atmosphere/surface 9-parameter grid**: log P_H₂O ∈ [−7, 2] step 1; log P_CO₂ ∈ [−7, 2] step 0.5; log P_O₂ ∈ [−5, 2] step 1; log P_SO₂ ∈ [−7, 2] step 1; χ ∈ {0.05, 0.2, 0.8}; A_s ∈ {0.0, 0.1, 0.2, 0.3, 0.4}; T_eq,0 ∈ {385, 431, 477} K. Total 684 000 atmospheres × 3.5 h on 512 CPU cores (4 nodes × 128 cores, NASA Aitken).
- **Bayesian inversion**: [[MultiNest]] (PyMultiNest; Buchner 2014 not ingested) over the 9-parameter grid; 1000 live points; evidence tolerance 0.5. Linear interpolation of the precomputed grid for each Multinest likelihood call (median grid error 0.6 ppm, max 6.9 ppm — both far below the ~20 ppm LRS 1σ).
- **Bare-rock comparison model**: 4-parameter (T_eq,0, A_s, T_eff, R_p/R_★), enforces no-atmosphere blackbody emission at dayside redistribution factor f = 2/3.
- **Aerosol sensitivity**: dust (Mars optical properties from Wolff 2009 not ingested) added a posteriori at fixed mass-mixing-ratio with optical depth τ_dust,9.3 ∈ {0.1, 1.0, 10}; r_p ∈ {0.5, 1.0, 5.0} μm.
- **Photochemistry sensitivity**: [[Photochem]] self-consistent coupling between climate and photochemistry, using GJ 176 UV (France 2016 not ingested) as M-dwarf XUV proxy; tested 1 bar O₂ + 10⁻⁴/10⁻² bar CO₂ cases.
- **F1500W forecast methodology**: same inversion run on synthetic LRS+F1500W joint data at a range of F1500W precisions (5–40 ppm in 5 ppm steps); JWST ETC (Pontoppidan 2016 not ingested) for visit-count scaling.

## Caveats & limitations

- **Heat-redistribution parameterization** (Koll 2022 not ingested) is known to overpredict heat redistribution for τ ≳ 1 bar atmospheres compared to GCMs. The authors fit χ as a free parameter but acknowledge this may not capture the full model error. The "no-redistribution" stress test relaxes the surface pressure upper limit to ~6 bar.
- **Atmosphere composition restricted to CO₂/H₂O/O₂/SO₂** — the inversion cannot constrain CO, N₂, NH₃, CH₄ directly. O₂ stands in as a proxy for all low-opacity gases, conflating them in the posterior.
- **Climate model is 1.5-D** (Wogan 2025a not ingested) and assumes a vertically isotropic atmosphere with dry adiabatic convection — appropriate for LTT 1445 A b's H₂O-undersaturated regime but not generalizable to wetter scenarios without modification.
- **Photochemistry omitted from the main inversion** — argued defensible at current LRS S/N but may bias future high-S/N analyses where O₃ features become measurable.
- **MIRI/F1500W forecast assumes 20 ppm precision is achievable**; current TRAPPIST-1 b precedent (Greene 2023; not ingested) is 29 % above ETC prediction, motivating the 36 ppm/√n_visit error budget and ≥4-visit requirement.
- **No transmission-spectrum joint analysis**: the LRS-only constraints are not propagated against the upcoming Bennett-led ([[JWST-GO-2512-COMPASS]]), Lustig-Yaeger/Stevenson (GO 7073), Batalha-Teske ([[JWST-GO-2512-COMPASS]]) transmission datasets that will independently probe similar metallicity / surface-pressure space.

## Open questions / follow-ups

- **Joint transmission + emission Bayesian inversion**: the LRS-only emission analysis here will be paired with the [[2026_Batalha_LTT1445Ab]] COMPASS transmission spectrum and the planned NIRISS/SOSS, NIRCam DHS, NIRCam F322W2, and NIRCam F444W transit datasets to give a panchromatic 1–17 μm joint constraint.
- **Population-level pressure ladders**: the climate-constrained inversion produces *quantitative* surface-pressure upper limits that can be aggregated across the M-dwarf rocky-planet sample to empirically constrain the [[cosmic-shoreline]] — currently only one rocky target ([[LTT1445Ab]]) has been processed this way; extending to TRAPPIST-1 b, GJ 1132 b, GJ 486 b, LHS 1140 c, LHS 1478 b, TOI-1468 b is the natural next step.
- **Photochemistry / 3D-coupling corrections**: when F1500W data reach 20 ppm precision the ~9 μm O₃ feature in O₂-rich atmospheres becomes measurable; a self-consistent climate + photochemistry inversion (using [[Photochem]] in fully coupled mode) is needed.
- **Aerosol breaking**: dust always lowers (tightens) the surface-pressure upper limit, but the exact magnitude depends on Mars-vs-Earth optical-property choices. Independent constraints on aerosol composition from transmission would help.

## Related

- [[2024_Wachiraphan_LTT1445Ab]] — original MIRI/LRS analysis using forward-model comparison rather than Bayesian inversion; this paper directly extends the same dataset with a more rigorous inference framework. Wachiraphan's claim of "≲ 100× solar metallicity" is recast as P_s ≤ 0.6 bar with O₂/CO/N₂ dominance.
- [[2026_Batalha_LTT1445Ab]] — companion paper on the same target: NIRSpec/G395H **transmission** spectrum from COMPASS, complementary to this LRS emission analysis. The two papers are explicit forecasts for the upcoming joint transmission + emission population analysis.
- [[2025_Coulombe_TOI-270b]] — analogous "thick-atmosphere consistent with cosmic-shoreline violation" result on a different rocky target, using a [[PACMAN-P]] climate model rather than [[Photochem]] / [[PICASO]].
- [[2025_BelloArufe_L98-59b]] — the wiki's first volcanic-atmosphere inference; uses [[ExoTR]] in a free-retrieval rather than climate-constrained framework; the Wogan methodology could resolve the ExoTR vs Aurora vs POSEIDON discrepancies on L 98-59 b.
- [[2025_Connors_MIRI-15um]] — MIRI/F1500W rocky-eclipse photometry program (TRAPPIST-1 b/c, LHS 1140 c, LHS 1478 b, TOI-1468 b) — natural application targets for the climate-constrained inversion.
- [[2025_Fisher_TOI1685b]], [[2025_Bennett_GJ1132b]] — featureless transmission spectra of rocky planets that could be combined with this methodology to give joint constraints.
- Concept: [[cosmic-shoreline]] — the framework's primary scientific motivation.
- Method: [[climate-constrained-inversion]] (this paper introduces the term).
