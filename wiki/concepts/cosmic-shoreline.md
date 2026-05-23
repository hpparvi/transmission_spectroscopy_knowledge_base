---
type: concept
aliases: [atmospheric shoreline, Zahnle-Catling shoreline, atmospheric retention shoreline]
tags: [habitability, atmospheric-retention, rocky-planet, m-dwarf, hub]
---

# Cosmic shoreline

The hypothesized boundary in (planetary escape velocity) × (cumulative stellar XUV irradiation) space that separates rocky bodies that retain atmospheres from those that do not (Zahnle & Catling 2017; not yet ingested). For close-in M-dwarf rocky planets — where stellar XUV histories are intense and prolonged — the shoreline is expected to shift relative to the solar-system expression, making "does this planet host an atmosphere?" a first-order JWST-era question. The observational test is typically transit and/or eclipse spectroscopy of targets bracketing the shoreline; **the wiki currently catalogs both clear shoreline-confirmations (multiple bare-rock M-dwarf planets) and three independent shoreline-challengers (TOI-270 b, TOI-561 b, HD 3167 b)** that suggest the boundary may be more porous than originally proposed.

## Variants

The wiki catalogs three observational regimes for shoreline tests:

- **MIRI emission spectroscopy (LRS or F1500W).** Eclipse depth + bare-rock comparison via T_day / T_max ratio R. R ≈ 1 is consistent with airless body; R < 1 implies atmosphere or high albedo. The dominant approach for hot rocky M-dwarf planets:
  - **Bare-rock confirmations:** [[2024_WeinerMansfield_GJ486b]] (Gl 486 b: T_day = 865 K, R = 0.97), [[2024_Wachiraphan_LTT1445Ab]] (LTT 1445 A b: T_day = 525 K, R ≈ 1, thick CO₂ excluded >6σ), [[2024_Xue_GJ1132b]] (GJ 1132 b: T_day = 709 ± 31 K, R = 0.95 ± 0.04), [[2025_Xue_GJ3929b]] (GJ 3929 b: T_day = 782 ± 79 K, R ≈ 1.07).
  - **Inconclusive / atmosphere-permitting:** [[2026_Holmberg_GJ3473b]] (GJ 3473 b: R = 0.82 ± 0.12, both bare rock and atmosphere fit), [[2025_Connors_MIRI-15um]] (TRAPPIST-1 c reanalysis cooler than Zieba 2023, atmosphere/high-albedo case strengthened).
  - **Shoreline challengers:** [[2025_Teske_TOI561b]] (T_day = 1800–2150 K vs bare-rock ~2950 K, USP at P = 0.446 d, ancient ~10 Gyr K-dwarf — challenges shoreline), [[2026_Coy_HD3167b]] (T_day far below bare-rock at ~5σ on USP HD 3167 b — challenges shoreline).
- **Transmission spectroscopy (NIRSpec G395H / NIRISS / PRISM).** Transit-depth featurelessness rules out low-MMW atmospheres but cannot rule out high-MMW secondary atmospheres without strong absorbers:
  - **Featureless null results:** [[2023_Lustig-Yaeger_LHS475b]] (LHS 475 b H₂ ruled out >10σ), [[2025_Alam_L168-9b]] (L 168-9 b first 3–12 μm rocky-planet spectrum; <100× solar metallicity ruled out), [[2025_Redai_GJ357b]] (GJ 357 b: MMW < 8 g/mol ruled out), [[2025_Taylor_GJ357b]] (GJ 357 b: ≤100× solar metallicity ruled out at 3σ), [[2025_Fisher_TOI1685b]] (TOI-1685 b: MMW ≳ 10 at ~5σ).
  - **Transmission-only shoreline challenger:** [[2025_Coulombe_TOI-270b]] (TOI-270 b: tentative H₂O absorption at lnB = 0.3–3.2, plus underdense bulk requiring water mass fraction ~5–6%).
- **Joint transmission + emission ("paired" approach).** [[2024_WeinerMansfield_GJ486b]] eclipse rules out the water-rich transmission interpretation from [[2023_Moran_GJ486b]] — establishes emission as the arbiter of transmission-degenerate cases. The canonical pattern.

## History

- **Zahnle & Catling 2017 (not yet ingested)** — original shoreline proposal at v_esc² × XUV-cumulative space.
- **2023 Cycle-1 first wave.** [[2023_Lustig-Yaeger_LHS475b]] (CHAMPs first JWST Earth-size transmission), [[2023_Moran_GJ486b]] (transmission ambiguous), [[2023_May_GJ1132b]] (transmission ambiguous, Visit 1 vs 2 disagreement).
- **2024 Cycle-1 emission resolution.** [[2024_WeinerMansfield_GJ486b]] resolves Moran 2023 ambiguity in favor of bare rock — establishes emission-as-arbiter; same year, [[2024_Xue_GJ1132b]] (bare rock), [[2024_Wachiraphan_LTT1445Ab]] (bare rock).
- **2025 broader survey.** Hot Rocks Survey ([[JWST-GO-3730]]) and LAVA LAMPS ([[JWST-GO-4818]]) populate the shoreline; CHAMPs ([[JWST-GO-1981-CHAMPs]]) wraps up bare-rock confirmations; multi-instrument [[2025_Alam_L168-9b]] first broadband 3–12 μm rocky-planet spectrum; **first three shoreline challengers emerge** ([[2025_Teske_TOI561b]], [[2025_Coulombe_TOI-270b]]).
- **2025 system-by-system XUV histories.** [[2025_Taylor_GJ357b]] models the full XUV luminosity evolution of GJ 357 using MORS tracks; finds the star has been sub-threshold for transonic escape since ~10³ Myr — a system-specific shoreline analysis distinct from population-level placement.
- **2025–2026 USP shoreline anomaly.** [[2026_Coy_HD3167b]] adds USP super-Earth HD 3167 b to the challengers; extends the atmospheric-retention anomaly to true ultra-short-period super-Earths around K dwarfs. Three independent challengers (TOI-270 b, TOI-561 b, HD 3167 b) now warrant population-level revision.

## Trade-offs

- **MIRI emission as cleanest discriminator.** Eclipse depth + bare-rock comparison delivers the lowest-systematic test; T_day / T_max ratio R interpretable even at modest precision. The 4–6σ bare-rock confirmations on GJ 486 b / GJ 1132 b / LTT 1445 A b / GJ 3929 b set the precision benchmark.
- **Transmission spectroscopy ambiguity.** Featureless transmission rules out low-MMW H₂-rich atmospheres but cannot rule out high-MMW secondary atmospheres without strong absorbers — degenerate with starspot contamination on M-dwarf hosts ([[stellar-contamination]]); requires emission cross-check (canonical pattern: [[2024_WeinerMansfield_GJ486b]] resolves [[2023_Moran_GJ486b]]).
- **System XUV history matters as much as instantaneous insolation.** [[2025_Taylor_GJ357b]] argues GJ 357 b is favorable for secondary-atmosphere retention despite shoreline placement, because its host has been sub-threshold for transonic escape for ~Gyr; conversely, [[2025_Alam_L168-9b]] argues L 168-9 b could not have retained a primordial H/He atmosphere beyond ~200 Myr.
- **Bond-albedo confound.** R < 1 admits two physical interpretations: atmospheric heat redistribution OR high surface albedo. Disentangling requires either spectral-feature detection or albedo modeling.

## Open issues

- **What atmosphere class explains the shoreline-challengers?** TOI-270 b's underdense bulk requires water mass fraction ~5–6%; TOI-561 b's low T_day suggests thick volatile-rich atmosphere; HD 3167 b's R = 0.57 admits both high albedo (Aeff ≈ 0.72) and thick atmosphere. No unifying compositional inference yet.
- **Population-level shoreline reformulation.** *Four* challengers ([[2025_BelloArufe_L98-59b]] L 98-59 b, [[2025_Teske_TOI561b]] TOI-561 b, [[2026_Coy_HD3167b]] HD 3167 b, [[2025_Coulombe_TOI-270b]] TOI-270 b) + a growing inventory of "atmosphere-permitting but inconclusive" results ([[2026_Holmberg_GJ3473b]], TRAPPIST-1 c reanalysis) pressure the original Zahnle-Catling formulation; community has not yet repositioned the shoreline boundary in light of JWST data.
- **Disentangling atmospheric-retention from atmospheric-replenishment.** Long-term volcanic outgassing or impact-delivered volatiles could replenish atmospheres on ostensibly-airless-side targets — the shoreline test is implicitly a *steady-state* test, but the observed sample may be in flux. [[2025_BelloArufe_L98-59b]] is the wiki's first **active replenishment** case ([[volcanic-atmosphere]]).

## Papers

### Bare-rock confirmations (MIRI emission)
- [[2024_WeinerMansfield_GJ486b]] — Gl 486 b T_day = 865 K, R = 0.97; canonical emission-as-arbiter resolution of [[2023_Moran_GJ486b]] transmission ambiguity.
- [[2024_Xue_GJ1132b]] — GJ 1132 b T_day = 709 ± 31 K, R = 0.95 ± 0.04; bare-rock consistent.
- [[2024_Wachiraphan_LTT1445Ab]] — LTT 1445 A b T_day = 525 K; thick CO₂ excluded >6σ.
- [[2025_Xue_GJ3929b]] — GJ 3929 b T_day = 782 ± 79 K, R ≈ 1.07; CO₂ > 100 mbar excluded.
- [[2025_Bennett_GJ1132b]] — bare-rock conclusion via four-visit transmission coadd.

### Shoreline challengers (atmospheric retention possibly preferred)
- [[2025_BelloArufe_L98-59b]] — **L 98-59 b sub-Earth M-dwarf**; SO₂-rich [[volcanic-atmosphere]] preferred over flat line at 3.3–3.8σ (NIRSpec G395H 4-transit); first wiki **volcanically-replenished** shoreline challenger; ≥8× Io tidal heating per unit mass; subsurface magma ocean R_m ≈ 0.6–0.9 R_p.
- [[2025_Teske_TOI561b]] — TOI-561 b USP super-Earth, ancient K-dwarf; T_day far below bare-rock; thick atmosphere consistent.
- [[2026_Coy_HD3167b]] — HD 3167 b USP super-Earth K-dwarf; eclipse 38 ± 11 ppm vs 104 ± 3 ppm bare-rock (≈5σ deficit); atmosphere or high-albedo surface.
- [[2025_Coulombe_TOI-270b]] — TOI-270 b warm super-Earth M-dwarf; tentative H₂O absorption (lnB = 0.3–3.2) + underdense bulk requiring WMF ~5–6%.

### Inconclusive / atmosphere-permitting
- [[2026_Holmberg_GJ3473b]] — GJ 3473 b: R = 0.82 ± 0.12, bare-rock and atmosphere both fit; thick CO₂ excluded.
- [[2025_Connors_MIRI-15um]] — TRAPPIST-1 b/c uniform reanalysis; TRAPPIST-1 c moves toward atmospheric/high-albedo side.

### Featureless transmission (atmospheric upper limits)
- [[2025_Fisher_TOI1685b]] — MMW ≳ 10 at ~5σ on TOI-1685 b.
- [[2025_Redai_GJ357b]] — MMW < 8 g/mol ruled out on GJ 357 b.
- [[2025_Taylor_GJ357b]] — ≤100× solar metallicity ruled out on GJ 357 b at 3σ; system XUV-history analysis.
- [[2025_Alam_L168-9b]] — first broadband 3–12 μm rocky-planet spectrum; <100× solar metallicity excluded; photoevaporation modeling rules out primordial H/He retention.
- [[2023_Lustig-Yaeger_LHS475b]] — H₂ ruled out >10σ on LHS 475 b.

### Transmission ambiguity (later resolved)
- [[2023_Moran_GJ486b]] — water-rich transmission interpretation; resolved as starspot contamination by [[2024_WeinerMansfield_GJ486b]].
- [[2023_May_GJ1132b]] — Visit 1 vs 2 disagreement; resolved by [[2025_Bennett_GJ1132b]] four-visit coadd.

### Methodology / population reanalysis
- [[2025_Connors_MIRI-15um]] — FN-PCA uniform reanalysis across 17 MIRI F1500W eclipses on five rocky planets; introduces [[Erebus]] pipeline.

### Theory / synthesis
- [[2025_Madhusudhan_subneptunes]] — perspective on JWST sub-Neptune/rocky boundary; biosignature criteria implicitly cosmic-shoreline-aware.

### Analyses
- [[analyses/2026-05-03_terrestrial-planets-state-of-the-field]] — synthesis across 24 terrestrial planets; foregrounds the three shoreline challengers as the central population-level question.
- [[analyses/2026-04-29_rocky-planets-jwst-transit-and-eclipse]] — four rocky planets with both JWST transit and JWST eclipse coverage.
