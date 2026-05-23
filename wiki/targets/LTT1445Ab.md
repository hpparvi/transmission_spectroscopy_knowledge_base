---
type: target
kind: planet
class: terrestrial
host_star: LTT1445A
mass_mearth: 2.73
radius_rearth: 1.34
period_days: 5.3587635
teq_k: 431
discovery_year: 2019
tags: [rocky-planet, m-dwarf-host, triple-star-system, bare-rock, nearby-exoplanet]
---

# LTT 1445 A b

Rocky planet (R_p = 1.34 R⊕, M_p = 2.73 M⊕, T_eq = 431 K, P = 5.36 d) orbiting the primary of the nearby (6.86 pc) triple M-dwarf system [[LTT1445A]]. Bulk density 6.2 ± 1.3 g/cm³ is consistent with an Earth-like rocky composition; instellation (~5.77 S⊕) is Mercury-like. The **closest known transiting rocky exoplanet** at the time of the JWST observations. Discovery: Winters et al. 2019 (not ingested); parameters updated in Pass et al. 2023 (not ingested). One of the most thoroughly-characterised JWST rocky planets — 12 funded transits spanning NIRISS/SOSS + NIRSpec G395H + NIRCam DHS + NIRCam F322W2 + NIRCam F444W (programs 2512, 7073, 7251) plus two F1500W eclipses under the Rocky Worlds DDT program. Current working conclusion: **likely bare rock or tenuous (P_s ≤ 0.6 bar at 2σ) optically-thin O₂/N₂/CO atmosphere**; high-metallicity (≥ 500× solar) chemical-equilibrium atmospheres are ruled out at 3σ from joint JWST+HST transmission.

## Observations to date
- **MIRI/LRS thermal emission** ([[JWST-GO-2708]], [[2024_Wachiraphan_LTT1445Ab]]) — dayside temperature 525 ± 15 K; temperature ratio R = 0.95 ± 0.06 consistent with a dark rocky surface; thick CO₂ (100 bar) atmospheres ruled out at > 6σ.
- **Climate-constrained Bayesian inversion of the same MIRI/LRS data** ([[2026_Wogan_LTT1445Ab]]) — bare-rock model preferred at K_bare/atm = 11; **P_s ≤ 0.6 bar at 2σ**; if an atmosphere is present, it is dominated by an optically thin gas (O₂/N₂/CO ≤ 1 bar), with ≤ 0.1 bar CO₂, ≤ 10⁻³ bar H₂O, ≤ 10⁻⁴ bar SO₂. Forecasts that ≥ 4 F1500W visits at 20 ppm precision can detect the thickest still-allowed atmosphere.
- **NIRSpec G395H transmission** ([[JWST-GO-2512-COMPASS]], [[2026_Batalha_LTT1445Ab]]) — single transit, 2025 Sep 1; 22–36 ppm spectral precision; **no astrophysical features**, only an NRS1–NRS2 detector offset of −43 ± 5 ppm. Rules out atmospheric metallicities > 350 × Solar (3σ) clear-sky equilibrium chemistry; extends to > 500 × Solar combined with HST/WFC3 (Bennett et al. 2025a; not ingested). H₂/He + CO₂/H₂O/CH₄ dominant-gas mixtures > 10–100 % ruled out for opaque pressure > 0.01 bar.
- **Pre-JWST**: Magellan II/LDSS3C ground-based transmission (Diamond-Lowe et al. 2023; not ingested) ruled out clear H/He atmospheres.

## Atmospheric composition
No species detected. **Surface-pressure 2σ upper limit P_s ≤ 0.6 bar** (climate-constrained inversion of LRS data; [[2026_Wogan_LTT1445Ab]]). Dominant-gas restrictions on 10 %-level abundances (chemical-equilibrium retrieval of G395H + HST/WFC3 data; [[2026_Batalha_LTT1445Ab]]):
- [[H2O]] < 10⁻²·⁶ bar (LRS); X(H₂O)/(H₂+He) < 0.1 at P_opaque > 10⁻² bar (G395H)
- [[CO2]] < 10⁻¹·⁰ bar (LRS); X(CO₂)/(H₂+He) < 0.1 at P_opaque > 10⁻⁴ bar (G395H)
- [[CH4]] < 100 % at P_opaque > 10⁻⁴ bar (G395H) — strongest constraint
- [[SO2]] < 10⁻⁴·⁰ bar (LRS)
- Optically thin gas (O₂ proxy for O₂/N₂/CO) < 1 bar (LRS)

## Open questions
- **Is any atmosphere present at all, or is LTT 1445A b a bare rock?** Current LRS data marginally prefer bare rock (K = 7–11). The 12 funded transmission transits + 2 F1500W eclipses across NIRISS/SOSS + NIRSpec G395H + NIRCam DHS/F322W2/F444W will be needed to resolve this — combined dataset can rule out 1000× Solar atmospheres at 4.6 ± 1.1 σ ([[2026_Batalha_LTT1445Ab]] forecast).
- **Aerosol degeneracy** at P < 10⁻² bar: [[VIRGA]] microphysics rules out direct condensation (H₂O / KCl / S₈ / H₂SO₄ all undersaturated), but photochemical haze remains the primary unconstrained degeneracy with metallicity.
- **Rocky Worlds DDT F1500W follow-up**: scheduled to test whether the LRS-allowed ~1 bar O₂ + 0.01 bar CO₂ atmosphere is real. ≥ 4 visits at 20 ppm precision needed.

## See also
- Host: [[LTT1445A]]
- Method: [[climate-constrained-inversion]] (introduced for this target in [[2026_Wogan_LTT1445Ab]])
- Programs: [[JWST-GO-2708]], [[JWST-GO-2512-COMPASS]]
- Comparators: [[GJ1132b]], [[GJ486b]], [[TRAPPIST-1b]], [[LHS475b]] (other JWST rocky-planet featureless cases); [[2025_Coulombe_TOI-270b]] (tentative-atmosphere counter-example at slightly warmer T_eq)
- Concept: [[cosmic-shoreline]]
- Papers: [[2024_Wachiraphan_LTT1445Ab]], [[2026_Wogan_LTT1445Ab]], [[2026_Batalha_LTT1445Ab]]
