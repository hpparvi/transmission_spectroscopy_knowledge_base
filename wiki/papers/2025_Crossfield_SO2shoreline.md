---
type: paper
bibkey: 2025_Crossfield_SO2shoreline
authors: [Crossfield, I. J. M., Ahrer, E.-M., Brande, J., Kreidberg, L., Lothringer, J., Piaulet-Ghorayeb, C., Polman, J., Welbanks, L., Kirk, J., Powell, D., Khorshid, N.]
year: 2025
venue: AJ submitted
arxiv: 2509.14318
targets: []
instruments: []
methods: []
species_detected: []
species_tentative: []
species_ruled_out: []
codes: [HELIOS, VULCAN, petitRADTRANS]
tags: [theory, modeling-grid, sulfur-chemistry, photochemistry, metallicity-tracer, c-o-tracer, so2-shoreline]
ingested: 2026-05-04
---

# Mapping the SO₂ Shoreline in Gas Giant Exoplanets

**Authors:** Crossfield, Ahrer, Brande, Kreidberg, Lothringer, Piaulet-Ghorayeb, Polman, Welbanks, Kirk, Powell, Khorshid (2025, arXiv:2509.14318; AJ submitted)
**Type:** **Theoretical / forward-modeling grid paper.** No new observations.
**Targets discussed:** Comparison to JWST-observed sulfur-chemistry sample — [[WASP-39b]], [[HAT-P-26b]], WASP-107 b (not ingested), GJ 3470 b (not ingested), plus 8 non-detections (HD 209458 b, HD 189733 b, WASP-15 b, TrES-4 b, [[WASP-17b]], WASP-94 A b, HIP 67522 b, GJ 3090 b — all not ingested except WASP-17 b).

## TL;DR

A grid of 936 self-consistent atmospheric models — using [[HELIOS]] (T-p), [[VULCAN]] (photochemistry), and [[petitRADTRANS]] (synthetic spectra) — mapping the predicted [[SO2]] abundance across a wide parameter space (T_eq = 250–2050 K, [M/H] = 0.3–1000× solar, C/O = 0.30–0.80, K_zz = 10⁵–10⁹ cm² s⁻¹, T_int = 100–500 K, XUV = 0.03–30× nominal). Defines the **"SO₂ shoreline"** at the 1 ppm VMR contour: the boundary in (T_eq, [M/H]) space below which SO₂ is unlikely to be observable. **SO₂ depends strongly on metallicity and C/O ratio** (especially the latter); **surprisingly weakly on incident XUV flux** (only ~30× variation shifts the shoreline modestly for T_eq < 1400 K); **essentially independent of internal temperature**; weak K_zz dependence for T_eq ≳ 600 K. Of the four current SO₂ detections — [[WASP-39b]], WASP-107 b (not ingested), [[HAT-P-26b]] ([[2025_Gressier_HATP26b]]), GJ 3470 b (not ingested) — three sit comfortably within or near the nominal shoreline; **GJ 3470 b sits right at the edge** (potential mild tension). **SO₂ is never the dominant sulfur-bearing species** in the modeled atmospheres — H₂S, S₂, NS, SO, SH, S₈, and even atomic S frequently match or exceed it — but SO₂ remains the most easily detectable due to its 4.1 μm and 7.4/8.7 μm bands.

## Key findings

- **SO₂ shoreline maps a clean (T_eq, [M/H]) boundary.** Below ~600 K and at < 30× solar metallicity, SO₂ is too low to detect. Above ~600 K SO₂ becomes detectable at ≳ 10× solar metallicity. The shoreline is steeper (rising metallicity threshold) at cooler T_eq.
- **C/O is the strongest knob.** Increasing C/O from 0.30 → 0.80 substantially decreases SO₂ across all T_eq and [M/H]; the shoreline shifts ~equally in (T_eq, [M/H]) at each C/O step. **An SO₂ detection therefore strongly implies C/O ≲ stellar AND/OR high metallicity** — a uniquely diagnostic combination.
- **XUV dependence is weak.** Varying XUV flux 0.03×–30× shifts the shoreline only modestly for T_eq < 1400 K; consistent with Mukherjee et al. 2024 (not ingested) but contrary to Dyrek 2024, de Gruijter 2025 (not ingested) which had reported stronger XUV-driven shifts. Encouraging because XUV histories are largely unmeasured for most JWST targets — uncertainty in stellar XUV does **not** dominate the SO₂ inference.
- **K_zz weak above T_eq ≳ 600 K, strong below.** Vertical mixing has little effect at T_eq > 600 K; below 600 K, low K_zz dramatically suppresses SO₂.
- **T_int essentially irrelevant for SO₂.** SO₂ forms at upper-atmospheric pressures (1–100 μbar) where deep T_int has negligible thermal influence.
- **Sulfur budget at fixed (T_eq, [M/H]):** Pie charts (Fig. 7) show SO₂ rarely > 30% of total atmospheric sulfur. At 400 K, H₂S, NS, S, S₂ dominate; at 1150 K, H₂S still wins; at 2050 K, atomic S and SO take over. **SO₂'s observability is its only privilege** — not its abundance.
- **Population vs. shoreline.** Of 4 confirmed SO₂ detections, all sit at or above the nominal shoreline. Of 8 non-detections among targets at high enough metallicity to be in principle detectable, the result is **decent agreement** with the shoreline prediction.
- **Detectability of other sulfur species:** H₂S has its strongest band at 7–9 μm (MIRI/LRS); SO₂'s 4.1 μm band is more accessible to NIRSpec G395H. SO and SH could be detectable at 0.8–1.2 μm at high metallicity + high T_eq.
- **Future work caveats.** Models lack clouds/hazes (would attenuate features and sequester S into ZnS, MnS, Na₂S condensates at depth); use 1D not 3D; assume HAT-P-26 b system parameters as fiducial (the choice is reasonable for the SO₂-detected sub-Saturn / Neptune class but doesn't generalize trivially to ultra-hot Jupiters or super-Jupiter cores).

## Methods

- **HELIOS** (Malik et al. 2017; not ingested) — 1D radiative-convective T-p profiles at fixed bulk metallicity and semi-major axis (translates to T_eq).
- **VULCAN** (Tsai et al. 2017; not ingested directly, but used in [[2026_Radica_WASP96b]]) — chemical kinetics with the SNCHO network plus full UV photochemistry. MUSCLES UV input for HAT-P-26 system; scaled XUV for the parameter sweep.
- **[[petitRADTRANS]]** (Mollière et al. 2019) — synthetic transmission spectra at R = 30,000 with 21 species opacities (Table 2 of paper).
- **Grid:** 13 T_eq × 8 [M/H] = 104 nominal models, plus systematic single-parameter sweeps over T_int (3 values), XUV (3), K_zz (3), C/O (3) for a total of 936 models. All models use HAT-P-26 b system parameters as the fiducial.
- **Data products** publicly archived at Zenodo (10.5281/zenodo.17101615).

## Caveats & limitations

- **No clouds/hazes.** Likely sulfur-bearing condensates ZnS, MnS, Na₂S form for T_eq < 700 K and could deplete the gas-phase SO₂ inventory by ≲ 10% — not enough to change the broad shoreline geometry, but enough to affect specific-target predictions.
- **No water condensation in the coolest models.** For T_eq < 500 K, water ice could substantially restructure the thermal profile — invalidating the model assumptions for the lowest-T_eq grid points.
- **VULCAN's SNCHO network omits some C-S bonded reactions.** Could cause overestimate of SO₂ at cool T_eq where CS, CS₂ might sequester sulfur.
- **HAT-P-26 b system parameters as fiducial.** Doesn't extend cleanly to higher-gravity hot Jupiters; surface gravity affects atmospheric scale heights and SO₂ photodissociation budget (de Gruijter et al. 2025; not ingested).
- **1D models.** Don't capture morning-vs-evening terminator differences (Lee et al. 2023, Tsai et al. 2024; not ingested) or longitudinal gradients on tidally locked planets.
- **Opacity sources missing for some C-S species.** S₂O, H₂CS, CH₃SH cross-sections not in public databases — could be relevant if VULCAN allowed them.

## Open questions / follow-ups

- **GJ 3470 b is right at the shoreline edge** — its low non-solar C/O (or non-mass-metallicity-relation metallicity) could push it back into compatibility, or it could indicate a subtle photochemistry feature missing from the models.
- **The 4 lowest-mass non-detections (WASP-166 b, HIP 67522 b, TOI-421 b, GJ 3090 b)** all sit above the predicted shoreline yet show no SO₂ — possibly low-precision data, cloud cover, or a real gap in the model.
- **Massive hot-Jupiter SO₂ non-detections.** A consistent pattern at the high-mass end suggests low-metallicity primordial atmospheres dominate this regime.
- **Population-level test continues.** Fig. 1's prediction will need revision as detections accumulate; future Ariel observations will significantly extend the sample.
- **3D and time-dependent models** are the next theoretical frontier; current 1D treatments are a methodological baseline only.

## Related

- [[SO2-photochemical-shoreline]] — this paper is the **foundational mapping paper** for that concept; updated wiki concept page accordingly.
- [[2025_Gressier_HATP26b]] — the empirical companion to this theory: reanalysis of 11 JWST giant-planet transmission spectra against the Crossfield-2023 shoreline prediction, now formalized in this 2025 paper.
- [[2026_Radica_WASP96b]] — places WASP-96 b on the proposed shoreline at 10–20× solar; consistent with this Crossfield 2025 mapping.
- [[2026_RoyPerez_WASP39b]] — confirms WASP-39 b SO₂ across pipelines; one of the four anchor detections in this Crossfield paper.
- [[2025_LustigYaeger_WASP17b]] — tentative SO₂ on WASP-17 b nightside via iESR-PIE; WASP-17 b appears as one of the 8 non-detections at lower metallicity in Crossfield's Fig. 1 (the iESR-PIE tentative detection is below the firm-detection threshold).
