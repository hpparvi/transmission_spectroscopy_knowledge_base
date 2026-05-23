---
type: method
aliases: [climate-constrained Bayesian inversion, climate-constrained Bayesian inference]
tags: [bayesian-inversion, rocky-planet-emission, radiative-convective-equilibrium, surface-pressure-constraints]
---

# Climate-Constrained Bayesian Inversion

Framework for interpreting JWST rocky-planet eclipse spectra introduced by [[2026_Wogan_LTT1445Ab]]. Distinct from free atmospheric retrievals (e.g. [[POSEIDON]] / [[petitRADTRANS]] free-chemistry) in that the forward grid is restricted to **physically self-consistent radiative–convective-equilibrium P–T profiles** rather than parameterized profiles. The inversion fits observed eclipse depths against a precomputed grid (~10⁵–10⁶ atmospheres) constructed via a 1.5-D climate model (e.g. [[Photochem]] / Clima) with [[PICASO]] radiative transfer; nested-sampling Bayesian evidence (e.g. [[MultiNest]] / PyMultiNest) over surface partial pressures, heat-redistribution efficiency, surface albedo, and equilibrium temperature delivers **quantitative upper limits on surface pressure** (e.g. P_s ≤ 0.6 bar at 2σ for [[LTT1445Ab]]) — directly testable against population-level hypotheses like the [[cosmic-shoreline]].

The methodology generalizes the parameterized-P–T atmospheric retrievals used for sub-Neptunes (e.g. [[2025_Felix_TOI-270d]] equilibrium-chemistry retrieval, [[2025_Coulombe_TOI-270b]] [[PACMAN-P]] coupling) to rocky-planet emission-spectrum work. It is the rocky-planet analog of equilibrium-chemistry transmission retrievals for sub-Neptunes. Forward-grid precomputation cost is high (~thousands of CPU-hours) but amortized over the population.

The method assumes (a) the climate model's heat-redistribution parameterization is adequate (Koll 2022 not ingested), (b) photochemistry is negligible at current JWST data S/N (defensible for current MIRI/LRS data per [[2026_Wogan_LTT1445Ab]] sensitivity tests), and (c) the atmospheric composition space is restricted to a small set of plausible secondary-atmosphere gases (CO₂ / H₂O / O₂ / SO₂ for [[LTT1445Ab]]; other choices required for different planets / formation histories). Joint transmission + emission analyses ([[2026_Batalha_LTT1445Ab]] companion paper + planned NIRISS/SOSS + NIRCam datasets) extend the framework to multi-wavelength inference.

## Papers
- [[2026_Wogan_LTT1445Ab]] — methodology introduction + case study on [[LTT1445Ab]]; bare-rock model favored at K = 7–11; P_s ≤ 0.6 bar at 2σ.
