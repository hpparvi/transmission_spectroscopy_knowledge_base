---
type: target
kind: planet
class: gas-giant
host_star: WASP-39
mass_mjup: 0.28
radius_rjup: 1.27
period_days: 4.0552
teq_k: 1166
discovery_year: 2011
tags: [hot-jupiter, inflated, jwst-ers, benchmark]
---

# WASP-39 b

Inflated hot Jupiter (0.28 MJ, 1.27 RJ, P ≈ 4.06 d) around the solar-type star [[WASP-39]]; the canonical JWST benchmark target observed as part of the Early Release Science program ([[JWST-ERS-1366]]). The first exoplanet for which CO₂ was detected via JWST (ERS papers; not yet ingested), along with SO₂ attributed to photochemistry, Na, K, H₂O, and CO. Roy-Perez et al. 2026 ([[2026_RoyPerez_WASP39b]]) use the same PRISM dataset to demonstrate that pipeline choices introduce up to 2 dex of variation in retrieved atmospheric parameters.

## Atmospheric composition

- [[Na]] — detected ([[2026_RoyPerez_WASP39b]]; confirmed across pipelines; first detection in original ERS papers, not yet ingested)
- [[K]] — detected ([[2026_RoyPerez_WASP39b]]; confirmed across pipelines)
- [[H2O]] — detected ([[2026_RoyPerez_WASP39b]]; confirmed across pipelines)
- [[CO2]] — detected ([[2026_RoyPerez_WASP39b]]; confirmed across pipelines; first JWST CO₂ detection in original ERS papers)
- [[CO]] — detected ([[2026_RoyPerez_WASP39b]]; confirmed across pipelines)
- [[SO2]] — detected ([[2026_RoyPerez_WASP39b]]; confirmed across pipelines; attributed to photochemistry in ERS)
- [[H2S]] — tentative ([[2026_RoyPerez_WASP39b]]; pipeline-dependent)

## Limb asymmetry

[[2025_Fu_limb-asymmetry]] reports δA_H = 2.20 ± 0.31 H — featureless morning, prominent water-band evening, > 5σ contrast — confirmed against the NIRSpec/PRISM dataset and three Espinoza et al. 2024 reductions of NIRISS/SOSS. WASP-39 b sits at 1166 K where MgSiO₃ alone cannot drive the morning–evening cloud divergence; Na₂S + MnS clouds are required. Implication: limb-averaged retrievals of the ERS data (e.g., Lueber et al. 2024 → log H₂O = −1.13; Espinoza et al. 2024 → log H₂O = −3.1) span ~2 dex partly because of unrecognized limb asymmetry.

## Methodology benchmarks

- [[2026_RoyPerez_WASP39b]] documents up to 2 dex variation in retrieved abundances across four data-reduction pipelines (Tshirt, Eureka, supreme-SPOON, FIREFLy) on the same PRISM ERS data — pipeline-driven systematics.
- [[2025_RoyPerez_WASP39b]] (companion / predecessor paper from same group) — instead examines **cloud-extinction-parameterization** systematics on the same FIREFLy reduction. Four cloud-extinction models tested ([[PSG]]/PUMAS + [[MultiNest]] + [[MOPSMAP]]): a flat cloud, free-slope linear, Ångström exponent, and MOPSMAP physical-aerosol. Ångström (ln B = 8.02) and MOPSMAP (ln B = 5.57) decisively preferred over flat clouds. Best-fit MOPSMAP r_eff = **0.55⁺⁰·⁰³₋₀·⁰³ μm** for spherical aerosols (n_r = 1.4). Different cloud parameterizations shift molecular abundances by up to 4 dex (H₂S: −2.23 vs −6.29), demonstrating that **cloud-extinction parameterization is a leading source of bias in retrieved abundances** — complementary to the pipeline-systematics angle.
- [[2025_Deka_WASP39b]] applies the **NEXOTRANS** retrieval framework to the panchromatic NIRISS+PRISM+MIRI (0.6–12.0 μm) WASP-39 b dataset; best-fit hybrid model yields O/H = 14× solar, C/H = 21× solar, S/H = 5× solar, C/O = 1.35× solar; cross-validated against eight community retrieval codes on the MIRI subset (all within 1σ).

## See also

- Host: [[WASP-39]]
- Concept: [[limb-asymmetry]], [[aerosols]]
- Programs: [[JWST-ERS-1366]]
- Papers: [[2025_Deka_WASP39b]], [[2025_RoyPerez_WASP39b]], [[2026_RoyPerez_WASP39b]], [[2025_Fu_limb-asymmetry]], [[2025_Fu_statistical-trends]] (population-level anchor; SO₂-L = −0.39 PRISM vs −0.08 G395H — instrumental discrepancy flagged)
