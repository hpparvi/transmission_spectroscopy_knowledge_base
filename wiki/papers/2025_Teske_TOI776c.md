---
type: paper
bibkey: 2025_Teske_TOI776c
authors: [Teske, J., Batalha, N. E., Wallack, N. L., Kirk, J., Wogan, N. F., Gordon, T. A., Alam, M. K., Aguichine, A., Wolfgang, A., Wakeford, H. R., Scarsdale, N., Redai, J. A., Moran, S. E., López-Morales, M., Meech, A., Gao, P., Batalha, N. M., Alderson, L., Gagnebin, A.]
year: 2025
venue: AJ
doi: 10.3847/1538-3881/adb975
targets: [TOI-776c]
instruments: [JWST-NIRSpec]
methods: [transmission-spectroscopy, atmospheric-retrievals, multi-visit-stacking]
species_detected: []
species_tentative: []
species_ruled_out: []
codes: [Eureka, Tiberius, PICASO]
tags: [sub-neptune, m-dwarf-host, water-world-candidate, jwst-go-2512, compass, null-result, featureless, model-dependent]
ingested: 2026-04-25
---

# JWST COMPASS: NIRSpec/G395H Transmission Observations of TOI-776 c, a 2 R⊕ M Dwarf Planet

**Authors:** Teske, Batalha, Wallack, Kirk, Wogan, Gordon, Alam, Aguichine, Wolfgang, Wakeford, Scarsdale, Redai, Moran, López-Morales, Meech, Gao, Batalha, Alderson, Gagnebin (2025, AJ 169:249) · [doi:10.3847/1538-3881/adb975]
**Target:** [[TOI-776c]] · **Host:** [[TOI-776]] · **Instrument:** [[JWST-NIRSpec]] (G395H, 2.87–5.14 μm)
**Program:** [[JWST-GO-2512-COMPASS]]

## TL;DR
Two COMPASS NIRSpec G395H transits of the warm sub-Neptune TOI-776 c (2.02 R⊕, 5.3 M⊕, Teq ≈ 420 K, M1V host) yield a **featureless 3–5 μm transmission spectrum**. A zero-sloped flat line is preferred or equivalent to all more complex models by Bayesian evidence. Metallicities ≲ 180–240× solar are excluded at 3σ for cloud-top pressures > 10⁻³ bar; in equilibrium chemistry models this corresponds to MMW ≳ 7.7 g mol⁻¹. However, the paper explicitly warns that **MMW inferences are model dependent**: simple two-component H₂O+H₂/He or CO₂+H₂/He mixture models give much more pessimistic limits (MMW > 2.8 and 5.5 g mol⁻¹, respectively). TOI-776 c may simply sit just below JWST's current feature-detection threshold — its predicted spectral features are ~1.7× smaller than the similar TOI-270 d, which does show molecular features ([[CH4]], [[CO2]], [[H2O]]; Benneke et al. 2024, not yet ingested).

## Key findings
- **Featureless 3–5 μm spectrum** from two COMPASS NIRSpec G395H visits; zero-slope flat line is preferred or equal to all tested non-physical models (step function, slope, NRS1/NRS2 Gaussian features) by Bayesian evidence.
- **CH4 at 3.3 μm explicitly tested**: fixing the Gaussian center at 3.314 μm and comparing to the zero-slope model; no confident detection in any visit or reduction.
- **Metallicity < 180–240× solar ruled out at 3σ** (for cloud-top pressure > 10⁻³ bar), varying by reduction pipeline and modeling method.
- **MMW constraints are model dependent:** equilibrium chemistry (via [[PICASO]] + Cantera; Goodwin et al. 2022) → MMW ≳ 7.7 g mol⁻¹; H₂O+H₂/He mixture → >4% H₂O ruled out at 3σ (MMW ≳ 2.8 g mol⁻¹); CO₂+H₂/He mixture → >8% CO₂ ruled out at 3σ (MMW ≳ 5.5 g mol⁻¹).
- Two independent reductions ([[Eureka]] joint fit; [[Tiberius]] weighted average) yield consistent spectra. Visit-to-visit NRS1 offset ambiguous: strongly preferred by Tiberius visit 1 (ΔlnZ = 12 for step function), weakly preferred by Eureka! visit 2 (ΔlnZ = 1); combined-spectrum atmospheric conclusions unchanged.
- **Comparison to TOI-270 d**: TOI-776 c's system parameters (lower equilibrium temperature, slightly larger gravity, smaller planet-to-star radius ratio) predict spectral features ~1.7× smaller than TOI-270 d — the CO₂ amplitude is ~46 ppm vs. ~80 ppm for TOI-270 d — suggesting TOI-776 c sits just below the current JWST detectability threshold, not necessarily that it lacks an atmosphere.
- Median spectral precision: Eureka! joint — ~19 ppm (NRS1), ~33 ppm (NRS2); Tiberius weighted avg — ~17 ppm (NRS1), ~30 ppm (NRS2) in 30-pixel (~0.02 μm) bins.

## Methods
- **Observations:** two NIRSpec G395H transits on 2023-05-11 and 2023-05-27 under JWST Cycle 1 program [[JWST-GO-2512-COMPASS]]; 3636 integrations × 7 groups per visit; ~1.62/2.74 hr pre-/post-transit baseline.
- **Reduction:** [[Eureka]] v1.11.4 (primary; joint fit of both visits) and [[Tiberius]] v1.8.2 (cross-check; weighted average of visits). Light curves fit with `batman` (Kreidberg 2015); MCMC via `emcee` (Foreman-Mackey et al. 2013) for Eureka! white-light curves; Levenberg–Marquardt for Tiberius spectroscopic curves. Limb darkening: MPS-ATLAS grid (Kostogryz et al. 2022) for Eureka!; 3D Stagger grid via ExoTiC-LD (Grant & Wakeford 2024) for Tiberius.
- **Non-physical model comparison:** UltraNest (Buchner 2021; not yet ingested) nested sampling on four model types (zero-slope, step function, slope, NRS1/NRS2 Gaussian) plus a fixed-center CH4-band Gaussian; Bayesian evidence (lnZ) compared between models.
- **Physical model constraints:** [[PICASO]] (Batalha et al. 2019) transmission forward models on a 20-metallicity × 5-pressure grid; chemical equilibrium abundances via Cantera (Goodwin et al. 2022; not yet ingested); UltraNest for Bayesian retrieval on physical parameters (metallicity, opaque pressure level, radius factor, NRS1/NRS2 offset). Forward-model χ² grid as cross-check.
- **Two-component models:** H₂O+H₂/He and CO₂+H₂/He atmosphere grids to explore more pessimistic MMW constraints.

## Caveats & limitations
- MMW inferences strongly model dependent; the range 2.8–7.7 g mol⁻¹ spans the space of plausible physical assumptions. The paper cautions against reporting a single MMW limit without qualification.
- Visit-to-visit offsets not conclusively diagnosed as stellar heterogeneity vs. instrument systematics; both reductions proceed without empirical correction.
- 2 additional NIRSpec G395H visits would tighten the metallicity constraint to ~300× solar; MIRI thermal emission (~31 ppm signal, ~4 eclipses needed to detect) could distinguish between bare-rock and thick-atmosphere scenarios.
- The absence of features does not strongly favor a high-MMW atmosphere over a sub-threshold low-MMW one, given the scale height predictions.

## Open questions / follow-ups
- Is TOI-776 c a water world (H₂O-rich envelope on rocky core) or a rocky planet with a stripped H₂/He envelope? MIRI/LRS emission could help; Lyα atmospheric escape may be informative but complicated by the high stellar RV (~49 km s⁻¹) and expected high ionization fraction in high-metallicity atmospheres.
- Why does the nearly analogous planet TOI-270 d show molecular features while TOI-776 c does not? Is it purely a scale-height effect, or do atmospheric compositions or stellar environments differ fundamentally?
- Can a population-level analysis of COMPASS targets distinguish between multiple atmospheric populations (rocky, water-world, sub-Neptune) rather than just placing limits on individual planets?

## Related
- [[2025_Alderson_TOI-776b]] — COMPASS NIRSpec G395H result on the sibling inner planet TOI-776 b; also featureless.
- [[2024_Scarsdale_L98-59c]] — COMPASS NIRSpec G395H result on L 98-59 c; another 2-visit featureless sub-Neptune.
- [[2024_Alderson_TOI-836b]] — COMPASS NIRSpec G395H result on TOI-836 b; similar analysis strategy.
- TOI-270 d (Benneke et al. 2024; not yet ingested) — the directly analogous planet that shows CH4, CO2, H2O features at 0.6–5 μm; the principal comparison case for this paper.
