---
type: target
kind: planet
class: gas-giant
host_star: WASP-94A
aliases: [WASP-94 Ab]
mass_mjup: 0.45
radius_rjup: 1.58
period_days: 3.950
teq_k: 1508
discovery_year: 2014
tags: [hot-jupiter, inflated, f-dwarf-host, binary-system, misaligned, retrograde, limb-asymmetry-strongest, formation-tracer]
---

# WASP-94 Ab

Inflated retrograde-misaligned hot Jupiter (M ≈ 0.45 MJ, R ≈ 1.58 RJ → log g = 2.7 cgs, T_eq ≈ 1508 K, P = 3.95 d, λ = −123°) around the F8 primary of the WASP-94 visual binary [[WASP-94A]]. The host sits **above the Kraft break** so the retrograde orbit is primordial — making this target especially valuable for the formation-vs-migration test of the Penzlin 2024 disc-chemistry framework.

## Atmospheric composition

- [[CO2]] — detected at 11σ via JWST/NIRSpec G395H; log VMR ≈ −4.25 ([[2025_Ahrer_WASP94Ab]])
- [[H2O]] — detected at 4σ; log VMR ≈ −1.60 ([[2025_Ahrer_WASP94Ab]])
- [[CO]] — tentative at ~3σ; log VMR ≈ −2.85 ([[2025_Ahrer_WASP94Ab]])
- [[H2S]] — tentative at ~2.5σ; log VMR ≈ −3.31 to −3.59 ([[2025_Ahrer_WASP94Ab]])
- CH₄, NH₃, HCN, C₂H₂ — all upper-limited (log VMR < −5.0 to −6.5) ([[2025_Ahrer_WASP94Ab]])

## Observations to date

[[2025_Fu_limb-asymmetry]] reported the **strongest morning–evening limb-asymmetry signal** in the JWST NIRISS sample (δA_H = 2.83 ± 0.34 H) using a separate NIRISS/SOSS dataset — featureless morning, water-band evening — consistent with high-altitude evening aerosols cleared by morning downwelling, with WASP-94 Ab serving as the LSM normalization reference. [[2025_Ahrer_WASP94Ab]] then obtained a JWST/NIRSpec G395H transmission spectrum (GO 3154) and retrieves a **cloud-free atmosphere** with substellar C/O = 0.49⁺⁰·⁰⁸⁻⁰·¹³ (host C/O★ = 0.68 ± 0.10) and stellar-like metallicity Z = 2.17 ± 0.65 × solar (host Z★ = 2.09 × solar). The substellar-C/O + stellar-metallicity combination is best explained by **pebble accretion or planetesimal accretion combined with large-distance migration** within the Penzlin et al. 2024 disc-chemistry framework — disfavoring local gas accretion in the inner disc.

## Tensions

- **Cloud-free (G395H, [[2025_Ahrer_WASP94Ab]]) vs morning-aerosol (NIRISS, [[2025_Fu_limb-asymmetry]]):** the NIRISS analysis attributes the strongest limb asymmetry in the sample to terminator-asymmetric high-altitude aerosols; the G395H analysis finds no cloud-deck preference. Wavelength regimes differ — G395H is at λ > 2.8 μm where small-particle Rayleigh scattering is negligible — and the NIRISS-specific morning aerosol may simply be transparent to G395H. Listed as a tension to surface for follow-up rather than a contradiction; not adjudicated here.

## Open questions

- **Confirm CO and H₂S** (currently both at ~3σ) via panchromatic data (NIRISS or NIRCam baseline).
- **Reconcile cloud-free G395H result** with the NIRISS-resolved evening aerosol / morning-downwelling picture — joint NIRISS+G395H limb-resolved retrieval is the natural test.
- **Above-the-Kraft-break sample expansion**: GO 3154 + companion programs aim to test the Penzlin 2024 prediction that aligned vs misaligned hot Jupiters above the Kraft break leave distinct C/O signatures (possibly reversed if silicate evaporation occurs).

## See also

- Host: [[WASP-94A]]
- Concepts: [[limb-asymmetry]]
- Programs: [[JWST-GO-3154]]
- Papers: [[2025_Ahrer_WASP94Ab]], [[2025_Fu_limb-asymmetry]]
