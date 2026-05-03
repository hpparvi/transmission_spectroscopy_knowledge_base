---
type: paper
bibkey: 2026_Holmberg_GJ3473b
authors: [Holmberg, M., Diamond-Lowe, H., Mendonça, J. M., Kitzmann, D., Espinoza, N., Allen, N. H., August, P. C., Fortune, M., et al.]
year: 2026
venue: arXiv:2604.02332
arxiv: 2604.02332
targets: [GJ3473b]
instruments: [JWST-MIRI]
methods: [secondary-eclipse-spectroscopy, multi-visit-stacking]
codes: [JExoRES, MultiNest, HELIOS, SPHINX]
tags: [super-earth, rocky-planet, m-dwarf-host, miri-f1500w, hot-rocks-survey]
ingested: 2026-04-29
---

# Hot Rocks Survey V: Secondary Eclipse Photometry of GJ 3473 b with JWST/MIRI

**Authors:** Holmberg, Diamond-Lowe, Mendonça, Kitzmann, Espinoza, Allen, August, Fortune, et al. (2026, arXiv:2604.02332)
**Target:** [[GJ3473b]] · **Host:** [[GJ3473]] (mid-M, T_eff = 3347 ± 54 K) · **Instrument:** [[JWST-MIRI]] (F1500W photometry)
**Program:** [[JWST-GO-3730]] (Hot Rocks Survey, paper V)

## TL;DR

Four JWST MIRI F1500W secondary eclipses of the highly-irradiated rocky exoplanet [[GJ3473b]] (Teq ≈ 773 K, R = 1.264 R⊕, M = 1.86 M⊕) yield a joint eclipse depth of **186 ± 45 ppm** (lnB = 5.1) — somewhat shallower than a zero-albedo blackbody, giving R = T_day/T_max = 0.82 ± 0.12 and T_day = 820 ± 120 K. **Both bare-rock and atmospheric scenarios remain consistent**; thick CO₂ atmospheres with surface pressure > 1.2–6.5 bar are excluded (95% upper limit, depending on Bond albedo). Tentative visit-to-visit eclipse-depth variability (33–371 ppm) is reported. Fifth published Hot Rocks Survey result.

## Key findings

- **Joint eclipse depth** = 186 ± 45 ppm; lnB = 5.1 vs no-eclipse model.
- **T_day** = 820 ± 120 K; **R = 0.82 ± 0.12** — between the bare-rock prediction (R ≈ 1) and a thick-atmosphere expectation (R ≪ 1).
- **Per-visit depths** (with GP detrending): 33⁺⁸⁰₋₈₃, 103⁺⁹³₋₉₅, 371⁺⁸³₋₈₁, 224⁺⁸⁶₋₈₄ ppm — tentative ~3σ variability, possibly planetary or systematic.
- **Atmospheric scenarios:** thick 100% CO₂ atmospheres ruled out at P_surf > 1.2–6.5 bar (depending on A_B = 0–0.3); thin CO₂, H₂O, and other atmospheres remain possible.
- **CO₂ atmospheric collapse threshold** P_surf ≈ 0.6–1 mbar derived.
- **Highly reflective surfaces** (e.g. granite/felsic) match the low eclipse depth; geologically realistic lower-reflectance bare rocks also fit.
- Posterior P(atmosphere) ≈ 47–52% (prior-dependent) — single-band photometry cannot break the degeneracy.

## Methods

- **Observations:** 4 visits (2024 Mar 12, Mar 13, Mar 30, Oct 20); MIRI F1500W SUB256 subarray, FASTR1, 39 groups/integration; 1017 integrations/visit (~3.4 h each).
- **Primary reduction:** [[JExoRES]] (Holmberg & Madhusudhan 2023; not yet ingested). No alternate reduction pipeline cross-check.
- **Light-curve fits:** `batman` + [[MultiNest]] + `celerite` GP for time-correlated noise.
- **Atmospheric / surface modeling:** [[HELIOS]] + HELIOS-K (Malik 2017, 2019; Grimm & Heng 2015) for atmospheric grids; Hapke 2001 / Paragas et al. 2025 (not yet ingested) for surface emission. [[SPHINX]] and BT-Settl for stellar models.

## Caveats & limitations

- **Single-band F1500W photometry** cannot break the atmosphere/bare-rock degeneracy — even >10 visits would leave a degeneracy with high-albedo surfaces.
- **Visit-4 settling anomalous** (PSF broadens then narrows) due to the preceding F560W observation.
- **Flare-like ~700 ppm feature** in visit 2.
- **Granite-like surface fit** may be geologically unrealistic for an irradiated rocky planet.
- **Tidal locking assumed** but not directly verified.
- **No alternate reduction** — JExoRES is the sole pipeline.

## Open questions / follow-ups

- Is the visit-to-visit variability planetary (e.g., variable cloud cover) or systematic?
- Does the LRS spectroscopic mode (e.g., GO 7675 LHS 1478 b follow-up) better break the atmosphere/bare-rock degeneracy?
- What is the inventory of remaining atmospheric scenarios consistent with R = 0.82?

## Related

- [[2025_Connors_MIRI-15um]] — uniformly reanalyzes 17 MIRI F1500W eclipses on 5 rocky planets but treats GJ 3473 b only as a systematics-characterization target (no atmospheric analysis); this paper is the first / only atmospheric analysis of GJ 3473 b in the wiki.
- Hot Rocks Survey series companion papers (all not yet ingested): August et al. 2025 (paper I, LHS 1478 b), Meier Valdés et al. 2025 (TOI-1468 b), Fortune et al. 2025 (LHS 1140 c), Allen et al. 2025 (LTT 3780 b).
- [[2026_Coy_HD3167b]] — different MIRI/LRS R = 0.57 result on a USP super-Earth (atmospheric / high-albedo evidence).
