---
type: paper
bibkey: 2024_Alderson_TOI-836b
authors: [Alderson, L., Batalha, N. E., Wakeford, H. R., Wallack, N. L., Aguichine, A., Teske, J., Adams Redai, J., Alam, M. K., Batalha, N. M., Gao, P., Kirk, J., López-Morales, M., Moran, S. E., Scarsdale, N., Wogan, N. F., Wolfgang, A.]
year: 2024
venue: AJ
doi: 10.3847/1538-3881/ad32c9
targets: [TOI-836b]
instruments: [JWST-NIRSpec]
methods: [transmission-spectroscopy, multi-visit-stacking]
species_detected: []
species_tentative: []
species_ruled_out: [H2]
codes: [Eureka, ExoTiC-JEDI, PICASO, CHIMERA]
tags: [super-earth, k-dwarf-host, rocky-planet, jwst-go-2512, compass, multi-planet-system, flat-spectrum]
ingested: 2026-04-22
---

# JWST COMPASS: NIRSpec/G395H Transmission Observations of the Super-Earth TOI-836 b

**Authors:** Alderson, N. E. Batalha, Wakeford, Wallack, et al. (2024, AJ 167:216) · [doi:10.3847/1538-3881/ad32c9]
**Target:** [[TOI-836b]] · **Host:** [[TOI-836]] · **Instrument:** [[JWST-NIRSpec]] (G395H, 2.87–5.14 μm)
**Program:** [[JWST-GO-2512-COMPASS]]

## TL;DR
Two JWST NIRSpec/G395H transits of the bright-K-dwarf super-Earth TOI-836 b (Rp=1.70 R⊕, Teq=871 K), reduced independently with [[Eureka]] and [[ExoTiC-JEDI]]. The combined spectrum is **well fit by a flat line** (median precision 25 ppm per R~200 spectroscopic channel). A [[PICASO]] thermochemical-equilibrium grid rules out atmospheric metallicities **< 250× solar** at an opaque pressure of 0.1 bar, corresponding to mean molecular weights ≤ 6 g mol⁻¹. TOI-836 b therefore **does not host an H₂-dominated atmosphere**, in striking contrast to its larger sub-Neptune sibling TOI-836 c (Wallack et al. 2024; not yet ingested).

The paper also flags that JWST's per-transit precision for small planets is ~1.3× worse than PandExo predictions — a caution for future COMPASS-style proposals that budget transits on optimistic noise-floor estimates.

## Key findings
- Median transit-depth precision 34 ppm (Visit 1) and 36 ppm (Visit 2) in ~0.02 μm spectroscopic channels; combined 25 ppm.
- Spectrum is flat: zero-slope model preferred across both reductions and both visits individually and combined; step-function / slope alternatives disfavored by Bayes factors.
- **Rules out metallicities < 250× solar** at opaque pressure 0.1 bar for a solar C/O atmosphere ([[PICASO]] + [[CHIMERA]] thermochemical equilibrium grid, 1–1000× solar).
- Constraint corresponds to MMW ≤ 6 g mol⁻¹; rules out H₂-dominated atmospheres to high confidence.
- Sibling TOI-836 c (sub-Neptune; separate COMPASS paper, not yet ingested) hosts a different atmosphere — the multi-planet system offers a natural pair comparing rocky vs gaseous atmospheres around the same host star.
- PandExo predicts ~1.3× better precision than achieved; future small-planet proposals should account for the gap when budgeting transits.

## Methods
- **Observations:** two NIRSpec G395H transits (2023-03-04, 2023-03-08; separated by one orbital period). BOTS mode, SUB2048 subarray, NRSRAPID readout.
- **Reduction:** independent [[ExoTiC-JEDI]] and [[Eureka]] pipelines; consistent within ~1σ on the combined spectrum.
- **Light-curve fitting:** `batman` transit model with systematics `S(λ) = s₀ + s₁·t + s₂·xₛ|yₛ|`, `emcee` MCMC, 50,000 steps after 50,000 burn-in, red-noise inflation via Pont et al. 2006.
- **Forward modeling:** 26-metallicity × 5-opaque-pressure [[PICASO]] grid with Guillot T–P profile and interpolated thermochemical-equilibrium chemistry.
- **Statistical tests:** `UltraNest` / `MLFriends` nested sampling for zero-slope vs step-function vs slope model comparison.
- **Multi-visit analysis:** joint fit across both visits to obtain the final transmission spectrum; see [[multi-visit-stacking]].

## Caveats & limitations
- The metallicity constraint depends on the assumed opaque pressure level; a high-altitude cloud deck could mask deeper molecular features.
- Limited to 2 visits; visit-to-visit systematics could be underestimated.
- Interpretation via forward-model χ² and Bayes factors; no full atmospheric retrieval.

## Open questions / follow-ups
- Is TOI-836 b genuinely atmosphere-less, or hiding a thin high-MMW atmosphere? MIRI follow-up would help.
- How does TOI-836 b compare directly to TOI-836 c? A joint interpretation paper would test shared-host assumptions.
- Does PandExo's optimism generalize? Worth cross-checking across the COMPASS sample.

## Tensions
- None directly with prior wiki content.

## Related
- [[2025_Alam_L168-9b]], [[2025_Alderson_TOI-776b]] — companion JWST COMPASS super-Earth results.
- [[2023_Lustig-Yaeger_LHS475b]] — Earth-sized comparison from JWST CHAMPs.
- [[2023_May_GJ1132b]], [[2025_Bennett_GJ1132b]] — rocky M-dwarf planet results with similar null-detection conclusions.
- Wallack et al. 2024 (not yet ingested) — TOI-836 c (sub-Neptune sibling) JWST transmission observations.
- Hawthorn et al. 2023 (not yet ingested) — TOI-836 system discovery paper; source of the system parameters adopted here.
