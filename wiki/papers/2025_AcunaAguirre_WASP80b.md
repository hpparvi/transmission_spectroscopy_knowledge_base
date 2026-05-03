---
type: paper
bibkey: 2025_AcunaAguirre_WASP80b
authors: [Acuña-Aguirre, L., Kreidberg, L., Mollière, P., Bachmann, N.]
year: 2025
venue: A&A
arxiv: 2511.13483
targets: [WASP-80b]
instruments: [JWST-NIRCam, JWST-MIRI, HST-STIS, HST-WFC3]
methods: [transmission-spectroscopy, secondary-eclipse-spectroscopy, atmospheric-retrievals, joint-interior-atmosphere-retrieval]
species_detected: [H2O, CH4, CO, CO2]
codes: [GASTLI, petitRADTRANS, easyCHEM, MultiNest]
tags: [warm-jupiter, k-dwarf-host, joint-retrieval, bulk-metallicity, methodology]
ingested: 2026-05-03
---

# The bulk metal content of WASP-80 b from joint interior–atmosphere retrievals: Breaking degeneracies

**Authors:** Acuña-Aguirre, Kreidberg, Mollière, Bachmann (2025, A&A; arXiv:2511.13483)
**Target:** [[WASP-80b]] · **Host:** [[WASP-80]] (K/early-M dwarf, T_eff = 4145 K) · **Instruments:** [[JWST-NIRCam]] + [[JWST-MIRI]] (LRS) + [[HST-STIS]] + [[HST-WFC3]]

## TL;DR

A re-analysis paper introducing **joint interior + atmosphere Bayesian retrievals** on WASP-80 b (warm Jupiter, T_eq ≈ 825 K) by coupling [[GASTLI]] (interior structure) with [[petitRADTRANS]] (atmosphere) and fitting transmission (HST/STIS+WFC3+JWST/NIRCam, 0.5–4 μm) plus emission (HST/WFC3+JWST/NIRCam+JWST/MIRI/LRS, 1–12 μm) jointly with mass and age constraints. Two fiducial scenarios emerge: a **secular-cooling** case (Z_planet = 0.12 ± 0.02; atmospheric M/H = 2.75× solar) or an **additionally-heated** case (Z_planet = 0.28 ± 0.11; M/H = 10× solar). Both prefer **sub-solar C/O (0.10–0.30)** and super-solar metallicity. Joint retrievals expose previously hidden degeneracies between envelope composition, chemistry, and thermal state — a methodological framework directly applicable to the [[2026_Ashtari_HATS75b]] bulk-vs-atmospheric metallicity tension.

## Key findings

- **Detected species** (from cited input retrievals): [[H2O]], [[CH4]], [[CO]], [[CO2]] (Wiser et al. 2025 panchromatic emission; not yet ingested).
- **Scenario JR6** (secular cooling, equilibrium chemistry):
  - M/H = 2.75 +0.88/−0.56 × solar
  - C/O = 0.12 +0.03/−0.02
  - CMF (core mass fraction) = 0.02
  - Z_planet = 0.12 ± 0.02
  - M_core = 3.49 +3.49/−1.59 M_⊕
  - T_int = 134 +12/−9 K
- **Scenario JR5*** (additional heating, free chemistry):
  - M/H = 10.00 +8.20/−4.75 × solar
  - C/O = 0.24 ± 0.09
  - Z_planet = 0.28 ± 0.11
  - M_core = 31.8 +21.3/−17.5 M_⊕
  - T_int = 257 +68/−44 K
- **Both scenarios prefer sub-solar C/O (0.10–0.30) and super-solar metallicity** — suggests late pebble or planetesimal accretion; very low C/O favors H₂O-ice accretion outside the snowline or evaporated inward-drifting pebbles.
- **Z_planet / Z_star ratios** (12.1 vs 30.3) bracket the Thorngren et al. 2016 (not yet ingested) mass–metallicity trend.
- **Emission constrains** T = 700–1000 K at P = 10⁻³–1 bar.
- **Cloud base** P_base ~ 0.1–100 bar from transmission; emission-only retrieval suggests high-altitude clouds at P ~ 10⁻⁴ bar.

## Methods

- **No new observations** — re-analysis of HST/STIS (0.4–1.0 μm transmission), HST/WFC3 (1.1–1.7 μm transmission + emission), JWST/NIRCam transmission (2.5–4.0 μm) and emission (F322W2 + F444W), JWST/MIRI/LRS emission (5.0–12 μm). Source datasets: Bell et al. 2023 (NIRCam, CH₄ at 6σ; not yet ingested), Wiser et al. 2025 (panchromatic emission; not yet ingested), Jacobs et al. 2023 (WFC3 emission; not yet ingested), Wong et al. 2022 (HST; not yet ingested).
- **[[joint-interior-atmosphere-retrieval]] framework:** [[GASTLI]] (interior, 2-layer core + H/He+metals envelope, hot-start adiabat to P = 1000 bar) coupled with [[petitRADTRANS]] v3.0 forward atmospheres (Guillot 2010 P–T, [[easyCHEM]] equilibrium chemistry or free abundances, 5-parameter cloud model). Single Bayesian likelihood combining spectra plus bulk observables (M_pl, R_pl, age) without down-weighting (in contrast to Wilkinson et al. 2024 on WASP-39 b; not yet ingested). Interior–atmosphere interface fixed at P_surf = 1000 bar; CMF and Z_env sampled.
- Sampling via PyMultiNest (Nasedkin et al. 2024; not yet ingested) and `emcee` for interior-only retrievals.

## Caveats & limitations

- **Adiabatic interior assumed** — no compositional gradients, double diffusion, or He rain (impacts at >250× solar M/H only).
- **No conduction in core.**
- **Tidal heating ruled out** as inflation source (Q' > 2.7 × 10⁵); **Ohmic dissipation** plausible but unmodeled.
- **Equilibrium chemistry** may break with strong vertical mixing (K_zz–T_int–C/O degeneracy).
- **P_surf fixed at 1000 bar.**
- **No reflected-light data** included (Morel et al. 2025 NIRISS/SOSS dataset discussed but not retrieved on; not yet ingested).
- **Cloud parameterization strongly affects retrieved M/H and C/O** — clear-atmosphere assumptions cause bias.
- **Critique of Wilkinson et al. 2024:** weighting bulk observables in the likelihood would underestimate uncertainties.
- **CMF grid spacing ΔCMF = 0.10** may artificially reduce posterior CMF spread.

## Open questions / follow-ups

- Independent confirmation of which of the two fiducial scenarios (secular-cooling vs additionally-heated) is correct — would benefit from a phase curve or improved age constraints.
- Apply the joint framework to other targets with bulk-vs-atmospheric metallicity tensions (notably [[HATS-75b]] from [[2026_Ashtari_HATS75b]]: bulk Z_p ≈ 0.20 vs atmospheric [M/H] = −1.74).
- Robustness of low C/O to non-equilibrium chemistry — needs disequilibrium tests with K_zz mixing.

## Related

- [[2026_Ashtari_HATS75b]] — separate (sequential, not joint) inference of bulk Z_p ≈ 0.20 vs atmospheric [M/H] = −1.74 on a GEMS gas giant; the joint framework introduced here is the natural next-step methodology for that and similar systems.
- [[2026_Heinke_HATP12b]] / [[2025_Crouzet_HATP12b]] — comparable warm-gas-giant atmospheric retrieval but without the interior coupling; provides the panchromatic transmission-only methodology.
- Wilkinson et al. 2024 (WASP-39 b joint retrieval; not yet ingested) — methodological predecessor that this work extends and critiques.
