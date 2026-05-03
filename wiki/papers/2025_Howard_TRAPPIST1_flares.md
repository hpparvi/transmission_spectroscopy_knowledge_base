---
type: paper
bibkey: 2025_Howard_TRAPPIST1_flares
authors: [Howard, W. S., Kowalski, A. F., Radica, M., Flagg, L., Vasilyev, V., Rackham, B. V., Tovar Mendoza, G., MacGregor, M. A., et al.]
year: 2025
venue: arXiv:2512.04265
arxiv: 2512.04265
targets: [TRAPPIST-1b, TRAPPIST-1c, TRAPPIST-1f, TRAPPIST-1g]
instruments: [JWST-NIRISS, JWST-NIRSpec]
methods: [stellar-contamination-modeling, flare-mitigation]
codes: [exoTEDRF, RADYN, batman, llamaradas-estelares]
tags: [trappist-1, m-dwarf-host, methodology, flares, stellar-activity, ucd-host]
ingested: 2026-05-03
---

# Separating flare and secondary atmospheric signals with RADYN modeling of near-infrared JWST transmission spectroscopy

**Authors:** Howard, Kowalski, Radica, Flagg, Vasilyev, Rackham, Tovar Mendoza, MacGregor, et al. (2025, arXiv:2512.04265)
**Targets:** [[TRAPPIST-1b]], [[TRAPPIST-1c]], [[TRAPPIST-1f]], [[TRAPPIST-1g]] (flare-monitoring + transit visits) · **Host:** [[TRAPPIST-1]] · **Instruments:** [[JWST-NIRISS]] (SOSS, 104 s cadence) + [[JWST-NIRSpec]] (PRISM, 1.6 s cadence)
**Programs:** [[JWST-GO-2589]] (Lim) and [[JWST-GTO-1201]] (Lafrenière)

## TL;DR

Methodology paper introducing **[[RADYN]] flare-mitigation pipelines** (both empirical and physics-based) for JWST NIR transmission spectroscopy of M-dwarf rocky planets. Six >10³⁰ erg flares (F1–F6, T_eff peaks 3000–5000 K) on [[TRAPPIST-1]] are characterized via 1D radiative-hydrodynamics electron-beam models and used to construct fiducial flare-spectrum templates at six effective temperatures (2130–4010 K). After mitigation, residual transit-spectrum noise drops to **54 ± 14 ppm (empirical) or 65 ± 17 ppm (RADYN)**, enabling injection-recovery 3σ detection of CO₂ transmission features at 150–250 ppm even in flare-contaminated transits. Directly relevant to the flare-contamination concerns flagged for [[TRAPPIST-1e]] in [[2025_Glidden_TRAPPIST1e]] / [[2025_Espinoza_TRAPPIST1e]].

## Key findings

- **Flares contaminate 50–70% of TRAPPIST-1 transits at the ~1000 ppm level** vs. typical ~100 ppm atmospheric signals — a quantification of the worst-case contamination rate.
- Best-fit RADYN flare model: mF12-37-5 (electron-beam flux 10¹² erg s⁻¹ cm⁻², cutoff 37 keV, power-law index δ = 5), filling factor ≈ 0.46% of the stellar disk.
- All RADYN models **over-predict the Paschen jump** at 0.82 μm — a model deficiency.
- **Predicted flare XUV / FUV / NUV counterparts:** 8.9–28.9 × 10²⁷ / 4.3–13.9 × 10²⁶ / 3.4–11.4 × 10²⁷ erg s⁻¹.
- Flaring contributes **1.35 +2.0/−0.15 × quiescence** to TRAPPIST-1's annual XUV emission.
- **Residual noise after mitigation:** 100–140 ppm worst case, 54–65 ppm typical.
- **Injection recovery:** 3σ CO₂ feature detection at 150–250 ppm.
- **No new atmospheric detections claimed** — the paper builds the mitigation infrastructure rather than executing the search.

## Methods

- **Observations:** 11 visits across [[JWST-GO-2589]] (Lim, TRAPPIST-1 b/c/g) and [[JWST-GTO-1201]] (Lafrenière, TRAPPIST-1 f), spanning 2022-07-17 to 2023-10-31. NIRISS-SOSS at 104 s cadence (SUBSTRIP256) and NIRSpec PRISM at 1.6 s cadence.
- **RADYN flare modeling:** 1D non-LTE radiative-transfer + hydrodynamics solver (Carlsson & Stein 1995, 1997; grid from Kowalski et al. 2024; not yet ingested) with non-thermal electron-beam heating. 43 model sets across ~10⁴ in (F_e, cutoff, δ) parameter space grid-searched against six flare-peak spectra.
- **Pipeline:** (a) extract per-integration flare-only spectrum + T_eff via Planck fit; (b) build fiducial T_eff-binned flare spectra; (c) compute common-mode spectrum; (d) subtract common-mode + Planck (empirical) or RADYN model (physics-based) per integration; (e) average and inject CO₂ templates from Lustig-Yaeger et al. 2019 (not yet ingested) for sensitivity tests.
- **Reduction:** [[exoTEDRF]] for NIRISS/SOSS and NIRSpec PRISM.
- **Light-curve modeling:** `batman`; flare templates `llamaradas-estelares` (Tovar Mendoza et al. 2022; not yet ingested).
- **Stellar baseline:** PHOENIX models (Wilson 2021; not yet ingested) for the quiescent contaminant spectrum.

## Caveats & limitations

- **RADYN over-predicts the Paschen jump at 0.82 μm** — model deficiency in the chromospheric transition region.
- **Quiescent residual features** (notably a 1.4 μm NIRSpec dip) are of ambiguous origin — TLS imprint, magnetic-feature disappearance, or instrumental.
- **Pipeline validated only for clearly-discernible flare peaks** (~30% of flare time); low-level flaring blended with spots/faculae remains unaddressed.
- **70% of flare peaks are out-of-transit** — in-transit TLS effects from flares are not directly tested.
- **Wavelength range restricted to ≤2.8 μm** (NIRISS); applicability to G395H / G395M needs separate validation.
- **No simultaneous multi-wavelength monitoring** (X-ray, UV, mm) — would test RADYN flare predictions directly.

## Open questions / follow-ups

- Does the pipeline work as well on smaller, sub-detection flares blended into spot/facula contamination?
- Will the mitigation recover atmospheric signals on subsequent transits with currently-marginal claims (e.g., on [[TRAPPIST-1e]])?
- Forthcoming JWST GO 7068 (PI: Doshi; not yet ingested) on five young M0–M4 flare stars will extend the calibration.

## Related

- [[2023_Lim_TRAPPIST1b]] — original NIRISS/SOSS paper providing several visits reanalyzed here for flares (spots/faculae alternation between visits is the contamination signature; flares are the second component).
- [[2025_Espinoza_TRAPPIST1e]] / [[2025_Glidden_TRAPPIST1e]] — TRAPPIST-1 e PRISM transits where Visits 3–4 were flagged as flare/activity-contaminated; this paper provides the mitigation tool that future TRAPPIST-1 e analyses can apply.
- [[2025_Rathcke_TRAPPIST1bc]] — back-to-back-transit-correction is the alternative empirical contamination strategy; complementary to flare mitigation since BBT cancels stable contamination but flares are stochastic per visit.
- [[stellar-contamination]] (hub) — flare mitigation extends the wiki's M-dwarf contamination toolbox beyond spot/facula modeling and GP marginalization.
