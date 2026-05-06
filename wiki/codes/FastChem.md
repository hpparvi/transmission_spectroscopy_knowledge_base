---
type: code
aliases: [FastChem equilibrium chemistry, PyFastChem]
tags: [chemical-equilibrium, atmospheric-modeling, hub]
---

# FastChem

An open-source gas-phase chemical equilibrium code for planetary atmospheres (Stock et al. 2018, 2022; not yet ingested). Rapidly computes number densities for hundreds of species across temperature–pressure grids under the assumption of chemical equilibrium, using a Newton-Raphson solver coupled with thermochemical data from JANAF and additional astrophysical sources. The wiki's reference equilibrium-chemistry layer — used as the chemistry module within retrieval frameworks ([[POSEIDON]] via PyFastChem, [[SANSAR]], [[NEMESISPY]]) and as the benchmark against which **bespoke equilibrium-chemistry modules** ([[NEXOTRANS|NEXOCHEM]]) are validated.

## Variants

- **PyFastChem coupling within retrieval frameworks.** The dominant role:
  - [[2025_Verma_HD209458b]] — PyFastChem within [[SANSAR]] for HD 209458 b equilibrium-chemistry retrievals; varying C/H or O/H independently to control C/O. Demonstrates that NIRCam-only retrievals constrain supersolar metallicity (2.2–10.7×) while STIS+WFC3+NIRCam constrain solar/subsolar (0.8–2.1×).
  - [[2026_Radica_WASP96b]] — chemical equilibrium abundances within the [[NEMESISPY]] CE retrieval framework on WASP-96 b panchromatic transmission.
- **Forward-model equilibrium-chemistry coupled with [[GENESIS]] / radiative-transfer codes.**
  - [[2026_Coy_HD3167b]] — chemical equilibrium abundances for HD 3167 b atmospheric forward models (combined with [[GENESIS]] 1D radiative-convective grid for eclipse spectra).
- **Benchmark target for in-house equilibrium-chemistry modules.**
  - [[2025_Deka_WASP39b]] — FastChem benchmarks NEXOCHEM (the in-house [[NEXOTRANS]] equilibrium-chemistry module) on WASP-39 b; agreement well within typical observational uncertainties.
- **NEMESISPY+FastChem equilibrium-chemistry rejection scenario.**
  - [[2024_Banerjee_L98-59d]] — equilibrium-chemistry retrieval on L 98-59 d via NEMESISPY+FastChem is rejected at 3.8σ relative to free-chemistry → the atmosphere is *not* in equilibrium; high-MMW atmosphere (~10 g mol⁻¹) inferred. The wiki's clearest example of FastChem's diagnostic role: equilibrium-chemistry's *failure* is itself the constraint.

## History

- **2018, 2022** — FastChem v1 and v2 releases (Stock et al.); PyFastChem Python wrapper widely adopted.
- **2024** — first wiki appearance: [[2024_Banerjee_L98-59d]] uses NEMESISPY+FastChem to test (and reject) equilibrium chemistry on L 98-59 d.
- **2025–2026** — saturating wiki adoption across hot-Jupiter ([[2026_Radica_WASP96b]]), USP super-Earth ([[2026_Coy_HD3167b]]), HD 209458 b methodology ([[2025_Verma_HD209458b]]), and benchmarking new chemistry modules ([[2025_Deka_WASP39b]]).

## Trade-offs

- **Strength: Speed.** Newton-Raphson solver evaluates equilibrium chemistry at sub-millisecond per (T, P) point; cheap enough to embed in nested-sampling retrievals (PyMultiNest at thousands of model evaluations per dimension).
- **Strength: Comprehensive species library.** Hundreds of species with reliable thermochemistry; standard reference for gas-phase chemistry up to ~3000 K.
- **Strength: Established cross-validation.** [[2025_Deka_WASP39b]] benchmarks NEXOCHEM against FastChem and finds agreement well within observational uncertainties — FastChem is the recognized de facto reference.
- **Limitation: Equilibrium-only.** Disequilibrium chemistry (vertical mixing, photochemistry) requires coupling with [[VULCAN]] or [[Photochem]]. [[2024_Banerjee_L98-59d]]'s rejection of equilibrium chemistry on L 98-59 d is exactly the case where FastChem alone is inadequate and disequilibrium tools must take over.
- **Limitation: Gas-phase only.** Condensate equilibrium is a separate problem; cloud/aerosol modeling requires upstream microphysics codes ([[VIRGA]], MOPSMAP). [[2025_AcunaAguirre_WASP80b]] uses FastChem (via easyCHEM) for gas chemistry plus a separate cloud parameterization.

## Open issues

- **Disequilibrium-chemistry attribution.** [[2024_Banerjee_L98-59d]]'s 3.8σ rejection of FastChem-driven equilibrium chemistry on L 98-59 d does not specify *which* disequilibrium driver (photochemistry, vertical mixing, condensation) is responsible; mapping equilibrium-chemistry rejection events to specific disequilibrium mechanisms remains target-by-target.

## Papers

### Equilibrium chemistry within retrieval frameworks
- [[2025_Verma_HD209458b]] — PyFastChem within SANSAR; HD 209458 b metallicity 0.8–2.1× solar (full coverage) vs 2.2–10.7× (NIRCam-only).
- [[2026_Radica_WASP96b]] — within NEMESISPY CE retrieval on WASP-96 b panchromatic transmission.

### Forward modeling
- [[2026_Coy_HD3167b]] — combined with GENESIS for HD 3167 b eclipse forward models.

### Equilibrium-chemistry rejection / benchmark
- [[2024_Banerjee_L98-59d]] — NEMESISPY+FastChem equilibrium retrieval rejected at 3.8σ on L 98-59 d (favoring free chemistry).
- [[2025_Deka_WASP39b]] — benchmarks NEXOCHEM ([[NEXOTRANS]]'s in-house equilibrium module) on WASP-39 b; FastChem treated as reference truth.
