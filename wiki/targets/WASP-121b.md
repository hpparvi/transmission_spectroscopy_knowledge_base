---
type: target
kind: planet
class: gas-giant
host_star: WASP-121
aliases: [WASP-121 b]
mass_mjup: 1.16
radius_rjup: 1.75
period_days: 1.275
teq_k: 2350
discovery_year: 2016
tags: [ultra-hot-jupiter, inflated, thermal-dissociation, refractory-tracer, f-dwarf-host]
---

# WASP-121 b

Benchmark ultra-hot Jupiter (M = 1.16 ± 0.07 MJ, R = 1.75 ± 0.04 RJ, P = 1.275 d, T_eq ≈ 2350 K) around the F-type star [[WASP-121]]. Tidally locked with permanent dayside hot enough for [[thermal-dissociation]] of H₂O and H₂ and ionization of metals. Pre-JWST: HST (Evans 2018) showed a NUV rise pointing to high-altitude refractory absorbers; HST phase-curve (Mikal-Evans 2022/2023) showed dayside H₂O depletion; ground-based IGRINS Doppler tracking (Wardenier 2024) showed dayside H₂O depletion + globally uniform CO. JWST/NIRSpec G395H transmission analysis from the GO-1729 phase curve ([[2025_Gapp_WASP121b]]) detects [[SiO]] at 5.2σ — the first definitive identification of the long-suspected NUV absorber via direct spectral signature — and finds further evidence for thermal H₂O + H₂ dayside dissociation. A custom dayside/nightside atmosphere model demonstrates that 1D retrievals biased C/O high.

## Atmospheric composition

- [[SiO]] — detected (5.2σ; first definitive identification; chemical-equilibrium-compatible) ([[2025_Gapp_WASP121b]])
- [[H2O]] — detected; dayside-depleted via thermal dissociation, nightside-enriched ([[2025_Gapp_WASP121b]])
- H₂ — thermally dissociated on dayside, recombined on nightside ([[2025_Gapp_WASP121b]]); ~100× more thermodynamically potent than H₂O for redistributing heat to the nightside (Bell & Cowan 2018, not ingested)
- **Energy budget** (NIRISS/SOSS phase curve, [[2025_Splinter_WASP121b]]): Bond albedo **A_B = 0.277 ± 0.016**, heat-recirculation efficiency **ε = 0.246 ± 0.014** (exoTEDRF); T_day = 2717 ± 17 K, T_night = 1562⁺¹⁸₋₁₉ K. Geometric albedo (Order 2) A_g = 0.093⁺⁰·⁰²⁹₋₀·⁰²⁷ — **reinforces the hot-Jupiter A_B/A_g paradox** (factor-3 ratio in same observation). Bell_EBM prefers slow wind speed ~0.2 km s⁻¹ at deep ~1 bar mixed layer — consistent with strong magnetic drag.

## Open questions

- **Refractory-to-volatile ratios** (Si/O, Mg/O, Fe/O) require panchromatic NUV + NIR + MIR; SiO in NIRSpec is a foundation but Si abundance not yet quantified.
- **3D-aware retrievals** are needed — 1D spherical-symmetry retrievals bias C/O high due to the negative correlation between H₂ dissociation and CO abundance.
- **Mg I + Fe II contributions** to the NUV rise (Lothringer 2022 alternative) not ruled out by the G395H SiO detection alone.
- **A_B / A_g paradox** — factor-3 discrepancy ([[2025_Splinter_WASP121b]]) between thermal-emission-inferred Bond albedo (~0.28) and reflected-light-inferred geometric albedo (~0.09) in the same NIRISS/SOSS observation. Requires either UV/blue reflected-light contributions outside NIRISS coverage (A_short ≈ 0.34 needed for self-consistency) or systematic differences in the two albedo metrics. Joint NIRISS + NIRSpec phase curves needed.
- **Slow zonal winds (~0.2 km/s) at 1 bar mixed layer** ([[2025_Splinter_WASP121b]] Bell_EBM) vs ~5 km/s at low pressure (Seidel 2025 not ingested) — requires vertically resolved 3D circulation modelling with magnetic drag (Wardenier 2024 not ingested, Beltz 2022 not ingested) to reconcile.
- **Eastward phase-offset increase at short wavelengths** ([[2025_Splinter_WASP121b]] Figure 4) — first robust altitude-dependent hot-spot signature; reflected light from clouds on the eastern dayside or shifted hot-spot at higher altitudes are the candidate explanations.

## See also

- Host: [[WASP-121]]
- Concepts: [[thermal-dissociation]]
- Species: [[SiO]], [[H2O]]
- Programs: [[JWST-GO-1729]]
- Papers: [[2025_Gapp_WASP121b]] (transmission, SiO detection, dayside H₂O/H₂ dissociation); [[2025_Splinter_WASP121b]] (NIRISS/SOSS phase curve, energy budget); [[2025_Fu_statistical-trends]] (population anchor: ultra-hot end at T_eq = 2450 K; CO-L = 1.98 ± 0.16, highest in 8-planet sample, driving the population CO-L vs T_eq positive correlation)
