---
type: target
kind: planet
class: gas-giant
host_star: WASP-107
mass_mjup: 0.10
radius_rjup: 0.94
period_days: 5.721
teq_k: 770
discovery_year: 2017
tags: [warm-jupiter, super-puff, low-density, k-dwarf-host, limb-asymmetry]
---

# WASP-107 b

Warm super-puff (Mp ≈ 0.10 MJ, Rp ≈ 0.94 RJ → log g = 2.45 cgs, T_eq ≈ 770 K) on a 5.72-day orbit around the K6V dwarf [[WASP-107]]. Lowest gravity in the [[2025_Fu_limb-asymmetry]] hot-Jupiter sample; near-polar orbit (Dai & Winn 2017; Rubenzahl 2021; not yet ingested). Major helium exosphere (~7× the optical radius) flagged as evidence of active mass loss.

## Atmospheric composition

- [[H2O]] — detected, **uniform between limbs** (log VMR ≈ −2.4) ([[2025_Murphy_WASP107b]])
- [[CO2]] — detected, **~40× more on morning than evening** (log VMR = −3.6 morning, −5.2 evening) ([[2025_Murphy_WASP107b]])
- [[SO2]] — detected, **~5× more on morning than evening** (log VMR = −4.7 morning, −5.4 evening) ([[2025_Murphy_WASP107b]]); first system with confirmed photochemical-product heterogeneity between limbs
- [[CH4]] — detected ([[2025_Murphy_WASP107b]])

## Observations to date

[[2025_Fu_limb-asymmetry]] reported both limbs uniformly muted in the NIRISS/SOSS-only reanalysis (δA_H = 0.02 ± 0.13 H), placing WASP-107 b in the cool-and-symmetric corner of the proposed [[limb-asymmetry]] horizon. [[2025_Murphy_WASP107b]] then reanalyzed all five archival JWST visits (NIRCam F322W2 + F444W, NIRISS/SOSS, NIRSpec G395H, MIRI LRS) panchromatically (1–12 μm) using [[Catwoman]] limb-resolved fits, and resolved a much richer story: the panchromatic limb-resolved spectra confirm the ~180 K evening–morning T gradient previously inferred from F322W2 alone, reveal evening–morning **chemical heterogeneity** in [[SO2]] (~5×) and [[CO2]] (~40×) — uniform [[H2O]] — and cloud heterogeneity (a broad 6–11 μm absorption present only on the morning limb). NIRISS and NIRSpec spectra were biased by occulted starspot crossings; an injection-recovery correction model was developed to bring them into agreement with NIRCam.

## Open questions

- Which condensate produces the morning-limb broad 6–11 μm cloud? A. Dyrek 2024 (silicates; not ingested) and L. Welbanks 2024a (parametric Gaussian; not ingested) disagreed; SPARC/MITgcm prefers Na₂S over silicates/KCl/MnS/ZnS in [[2025_Murphy_WASP107b]].
- Why does limb-asymmetry analysis from NIRISS-only [[2025_Fu_limb-asymmetry]] disagree with the panchromatic Murphy 2025 finding? Stellar-contamination contamination on the NIRISS visit (one occulted spot near ingress, another near egress) substantially biased the inferred limb spectra.
- Does an eclipse spectrum confirm the morning-limb cloud composition?

## Tensions

- **Limb asymmetry classification:** [[2025_Fu_limb-asymmetry]] places WASP-107 b in the symmetric (no detected asymmetry) bin via NIRISS/SOSS; [[2025_Murphy_WASP107b]] finds significant asymmetry in SO₂ + CO₂ + cloud distribution via panchromatic limb-resolved analysis. Driver: stellar contamination correction in the NIRISS visit; Murphy's correction restores agreement between instruments.

## See also
- Host: [[WASP-107]]
- Concepts: [[limb-asymmetry]], [[SO2-photochemical-shoreline]], [[stellar-contamination]]
- Programs: [[JWST-GTO-1201]], [[JWST-GTO-1224]]
- Papers: [[2025_Murphy_WASP107b]], [[2025_Fu_limb-asymmetry]], [[2025_Fu_statistical-trends]] (population-level: SO₂-L = 0.15 ± 0.14, one of two positive-SO₂-L outliers; CO₂-L = 4.70 ± 0.16 — highest CO₂-L in 8-planet sample)
