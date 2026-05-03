---
type: method
aliases: [joint interior+atmosphere retrieval, coupled interior-atmosphere retrieval]
tags: [bayesian, retrieval, interior-modeling, gas-giant, methodology]
---

# Joint interior–atmosphere retrieval

A Bayesian retrieval framework that couples a planetary interior model (e.g., [[GASTLI]]) with an atmospheric forward model (e.g., [[petitRADTRANS]]) into a single likelihood, fitting transmission and/or emission spectra **plus** bulk observables (mass, radius, age) **plus** stellar parameters jointly. The interior model takes core mass fraction and envelope metallicity as parameters and outputs the planet radius at a chosen interior–atmosphere boundary (typically P_surf = 1000 bar); the atmosphere extends outward from there. Joint sampling exposes degeneracies — between envelope composition, atmospheric chemistry, and thermal state — that separate (sequential) atmospheric and interior retrievals miss.

## Variants

- **Unweighted joint likelihood** (combining spectra and bulk observables on equal footing) — the [[2025_AcunaAguirre_WASP80b]] approach.
- **Weighted joint likelihood** (down-weighting bulk observables relative to spectra) — Wilkinson et al. 2024 on WASP-39 b (not yet ingested); critiqued by Acuña-Aguirre as underestimating posterior uncertainties.

## Trade-offs

- **Strength:** Breaks degeneracies between bulk metallicity (Z_planet) and atmospheric metallicity (M/H) that single-domain retrievals leave unconstrained.
- **Strength:** Self-consistent envelope-temperature treatment couples T_int directly into atmospheric P–T predictions.
- **Limitation:** Sensitive to interior assumptions — adiabatic interior, no compositional gradients, no He rain (impacts at >250× solar M/H only); P_surf fixed at the chosen boundary.
- **Limitation:** Cloud parameterization in the atmospheric module strongly affects retrieved M/H and C/O.
- **Limitation:** Computationally expensive; CMF grid spacing can artificially reduce posterior CMF spread.

## Open issues

- **Likelihood weighting** of bulk vs spectra remains contentious (Wilkinson 2024 vs Acuña-Aguirre 2025).
- **Equilibrium chemistry assumption** may break with strong vertical mixing, introducing K_zz–T_int–C/O degeneracy.
- **Application beyond hot/warm Jupiters** to GEMS or sub-Neptune targets where bulk-vs-atmospheric metallicity tensions also appear.

## Papers

- [[2025_AcunaAguirre_WASP80b]] — applies [[GASTLI]] + [[petitRADTRANS]] to WASP-80 b panchromatic HST + JWST data; identifies two fiducial scenarios (secular-cooling vs additionally-heated) bracketing Z_p = 0.12–0.28 and M/H = 2.75–10× solar.
