---
type: target
kind: planet
class: gas-giant
host_star: HAT-P-14
mass_mjup: 3.44
radius_rjup: 1.42
period_days: 4.62767
teq_k: 1624
discovery_year: 2010
tags: [super-jupiter, f-star-host, eccentric-orbit, grazing-transit, commissioning, m-dwarf-companion]
---

# HAT-P-14 b

Super-Jupiter (M_p = 3.44 M_J, R_p = 1.42 R_J, ρ ≈ 1.5 g/cm³) on a moderately eccentric (e = 0.11) 4.63-day **grazing transit** orbit (b = 1.014) around the F-type star [[HAT-P-14]] (T_eff = 6600 K; J = 9.09; with a known faint M-dwarf companion at 0.844"). Discovered by Torres et al. 2010 (not ingested). Among the **first JWST commissioning targets**: NIRSpec G395H (PID 1118, PI Proffitt) on 2022-05-30 and NIRISS SOSS (PID 1541, PI Espinoza) on 2022-06-08. Originally analyzed by Albert et al. 2023 (A23) + Espinoza et al. 2023 (E23) — both not ingested — with conflicting conclusions: NIRSpec featureless vs NIRISS blueward-slope + 1.4 μm break. **[[2025_Liu_HATP14b]] reanalyzes both datasets** with the latest STScI jwst pipeline + [[FIREFLy]] and detects [[H2O]] at 3.09σ, weak gray cloud (1.90σ), and roughly solar metallicity ([Fe/H] = −0.08⁺⁰·⁸⁹₋₀·⁹⁸). The blueward slope disappears in the updated reduction — corroborating the [[2025_Carter_NIRISS-jump-ramp]] message that **early NIRISS/SOSS commissioning data need uniform reanalysis**.

## Atmospheric composition

- **Detected:** [[H2O]] at 3.09σ (Δln Z = +3.4); log VMR ≈ −2.32⁺¹·¹³₋₁·₄₀ ([[2025_Liu_HATP14b]]). Equilibrium-chemistry retrieval: [Fe/H] = −0.08⁺⁰·⁸⁹₋₀·⁹⁸; C/O = 0.41⁺⁰·²⁴₋₀·²⁰ (~ solar).
- **Ruled out / upper limits (95%):** log VMR(CO₂) < −3.23; log VMR(CO) < −1.69; log VMR(CH₄) < −4.36. Non-detection of CO₂/CH₄ consistent with mass-metallicity scaling at this mass.
- **Cloud deck** weakly preferred at 1.90σ; log P_cloud = −2.02⁺¹·⁷⁸₋₁·₁₃ bars.

## Observations to date

**JWST commissioning:**
- NIRSpec G395H — JWST-PID-1118 (PI Proffitt); 2022-05-30; 6.5-hr transit.
- NIRISS SOSS — JWST-PID-1541 (PI Espinoza); 2022-06-08; 6.1-hr transit; SUBSTRIP256 + GR700XD.

## Open questions

- **Multi-visit confirmation.** Single transits per instrument; CO detection plausible with another visit.
- **Pipeline-version sensitivity** of NIRISS/SOSS commissioning data — Liu et al. argue this is a generic concern; cross-validation with [[exoTEDRF]], [[Eureka]] would test.
- **Methodology message:** HAT-P-14 b ranks 805th in the Transmission Spectroscopy Metric (Kempton et al. 2018; not ingested) — a 3σ detection on a "non-priority" target demonstrates JWST can deliver atmospheric inferences on ~1000 exoplanets.

## See also

- Host: [[HAT-P-14]]
- Comparator: [[2025_Carter_NIRISS-jump-ramp]] (methodology paper independently flagging the same pipeline-version issue)
- Papers: [[2025_Liu_HATP14b]]
