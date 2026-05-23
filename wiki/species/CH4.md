---
type: species
aliases: [methane]
tags: [carbon-bearing, photochemistry-sensitive, near-infrared, hub]
---

# CH₄

Methane — expected in cool/reduced atmospheres in thermochemical equilibrium; its detection or non-detection constrains C/O ratio, metallicity, and disequilibrium processes (quenching, photochemistry). Strong 3.3 μm absorption feature accessible to [[JWST-NIRSpec]] G395H. CH₄ has been a recurring "ghost detection" in early JWST rocky-planet work, with multi-visit data subsequently retiring those inferences.

## Detection status

No firm CH₄ detection on any wiki target. Recurring pattern: tentative single-visit inference → ruled out by multi-visit follow-up.

- **Tentative — current (mini-Neptune):**
  - [[TOI-1130b]] — ~2σ tentative in combined NIRSpec G395H + NIRISS SOSS transmission ([[2026_Barat_TOI1130b]]); originally 2.6σ but lowered to 2.0σ after removing a single outlier at 3.8 μm; would discriminate between strictly equilibrium chemistry and aggressively photochemistry-suppressed atmospheres.
- **Tentative, then retired:**
  - [[GJ1132b]] — ~1% CH₄ tentatively inferred in Visit 1 (Bayes factor 27 / 3.1σ vs no CH₄, [[2023_May_GJ1132b]]); not reproduced in Visit 2; **retired** by the four-visit coadded spectrum at >10σ ([[2025_Bennett_GJ1132b]]).
- **Ruled out as bulk gas:**
  - [[GJ486b]] — pure CH₄ disfavored at χ²ν = 2.1 ([[2023_Moran_GJ486b]]).
  - [[LHS475b]] — pure CH₄ rejected at ≥5σ from absence of 3.3 μm band; 3σ feature upper limit 38 ppm ([[2023_Lustig-Yaeger_LHS475b]]).
  - [[L168-9b]] — pure CH₄ excluded by featureless NIR + MIR spectrum ([[2025_Alam_L168-9b]]).
  - [[GJ3090b]] — confident absence at ~3.4 μm in NIRSpec/G395H drives the high-metallicity (>100× solar at 3σ) inference for the warm sub-Neptune ([[2025_Ahrer_GJ3090b]]).
  - [[WASP-94Ab]] — log VMR < −5.83 (2σ upper limit; HyDRo) on the misaligned hot Jupiter ([[2025_Ahrer_WASP94Ab]]).
  - [[LTT1445Ab]] — X(CH₄)/(H₂+He) < 1.0 at P_opaque > 10⁻⁴ bar (G395H transmission, [[2026_Batalha_LTT1445Ab]]); strongest dominant-gas exclusion on this target due to the 3.3 μm CH₄ band's spectral prominence.
- **No detection on hot Jupiters:** WASP-39 b's PRISM data, including the [[2026_RoyPerez_WASP39b]] re-analysis, does not list CH₄ among detected species — consistent with thermochemical equilibrium at ~1100 K disfavoring CH₄.

## Open issues

- **Single-visit CH₄ inferences are unreliable.** The GJ 1132 b cycle ([[2023_May_GJ1132b]] → [[2025_Bennett_GJ1132b]]) is the cautionary example: multi-visit stacking retired a 3.1σ Bayes-factor "detection." [[multi-visit-stacking]] is now the de facto requirement for any CH₄ claim on a small planet.
- **Photochemical quenching expectations.** No wiki paper has yet probed a planet cool enough to test CH₄ as a thermochemical-equilibrium expectation; the quenching question remains open for cooler future targets.

## Papers

- [[2025_Felix_TOI-270d]] — **decisive detection** on temperate sub-Neptune TOI-270 d (T_eq = 360 K) NIRSpec G395H + NIRISS SOSS; Bayes factor 3 × 10²⁵; log VMR ≈ −1.7; reproduces prior detections by Benneke et al. 2024 (not ingested) and Holmberg & Madhusudhan 2024 (not ingested).
- [[2025_FernandezRodriguez_K2-18b]] — **robust detection at 4.16σ–4.62σ** across all 12 retrieval configurations on K2-18 b NIRISS+NIRSpec; log VMR ≈ −1.7 to −1.0; one of the cleanest sub-Neptune CH₄ detections; survives leave-one-out and comprehensive 13-species retrieval tests.
- [[2025_Luque_K2-18b]] — CH₄ robustly detected at high abundance across all four reductions of K2-18 b panchromatic spectrum (log VMR ≈ −1.6 to −0.9 in SCARLET; −0.85 to −0.94 in PLATON); median ~1 dex higher than the two-offsets case of Madhusudhan 2023.
- [[2025_Schmidt_K2-18b]] — CH₄ at **4.2⁺⁰·⁷₋₀·₉ σ** across 60 K2-18 b NIRISS+NIRSpec data combinations × [[POSEIDON]] retrievals, with [[BeAR]] cross-checks at 3.5–4.5σ; log VMR = **−1.15⁺⁰·⁴⁰₋₀·₅₂** (≈7%); consistent with deep Neptune (4 ± 1%) and supports a metal-enriched mini-Neptune scenario. The 7% CH₄ requires an active source if interpreted in a hycean framework, posing a challenge to the steady-state hycean scenario.
- [[2025_Madhusudhan_K2-18b-MIRI]] — CH₄ not constrained by MIRI/LRS alone — its NIR-determined ~1% abundance gives features dwarfed by the stronger DMS/DMDS spectral contributions over 6–12 μm.
- [[2025_Canas_TOI5205b]] — CH₄ detected at >3σ on the GEMS-class gas-giant TOI-5205 b via the 1.2 + 1.7 μm bands; log VMR ≈ −5.5 to −5.6 across 3 NIRSpec PRISM visits. Critical species for distinguishing equilibrium vs disequilibrium chemistry on warm GEMS.
- [[2025_Jaziri_K2-18b]] — **CH₄ abundance reduced by ~2 dex** when photochemical (tholin) hazes are included in the K2-18 b NIRISS+NIRSpec+MIRI joint retrieval; from log VMR ≈ −1.2 (no tholin) to ≈ −3.5 (with exo1 tholin haze). Highlights the metallicity-aerosol-composition degeneracy: simplified retrievals over-attribute the spectrum to gas-phase CH₄.
- [[2025_Sikora_HD80606b]] — **time-variable detection** on highly eccentric hot Jupiter HD 80606 b NIRSpec G395H emission spectrum; 4.1–10.7σ in NRS1 across post-periapse phases; CH₄ feature at 3.0–3.5 μm strongest in the immediate post-periapse spectrum; first wiki target with phase-resolved CH₄ tracking through a ~860× irradiation swing.
- [[2025_LustigYaeger_WASP17b]] — tentative 1.5σ detection on the WASP-17 b nightside via iESR-PIE; CH₄ day–night gradient traces zonal winds.
- [[2026_Ashtari_HATS75b]] — detected at >3σ on HATS-75 b NIRSpec PRISM (TLS framework); first CH₄ detection on a GEMS-class target in the wiki.
- [[2001_Brown_TransmissionDiagnostics]] — predicts CH₄ visible longward of 2.2 μm in hot-Jupiter transmission; strongly temperature-sensitive.
- [[2025_Bennett_GJ1132b]] — pure-CH₄ rejected at >10σ on GJ 1132 b; retires the [[2023_May_GJ1132b]] tentative CH₄ inference.
- [[2025_Alam_L168-9b]] — pure-CH₄ atmospheres ruled out on L 168-9 b by featureless NIR + MIR spectrum.
- [[2023_May_GJ1132b]] — ~1% CH₄ tentatively inferred in Visit 1 of GJ 1132 b; later retired.
- [[2023_Moran_GJ486b]] — pure-CH₄ atmospheres strongly disfavored on GJ 486 b.
- [[2023_Lustig-Yaeger_LHS475b]] — pure-CH₄ rejected at ≥5σ for LHS 475 b.
- [[2025_AcunaAguirre_WASP80b]] — CH₄ present on WASP-80 b in joint interior–atmosphere retrieval (per cited input retrievals; Bell et al. 2023 NIRCam first JWST CH₄ detection at 6σ, not yet ingested).
- [[2025_Roy_LP791-18c]] — detected at 4.5σ on the temperate sub-Neptune LP 791-18 c (NIRSpec PRISM); log X(CH₄) > −2.89 (2σ); CH₄ + haze combination contrasts sharply with K2-18 b's CH₄ + CO₂ spectrum at similar T_eq.
- [[2025_Murphy_WASP107b]] — CH₄ detected on WASP-107 b panchromatic limb spectrum (3.3 μm feature first reported by L. Welbanks 2024a; not ingested); single-limb amplitudes consistent across instruments after spot correction. WASP-107 b is the lowest-T_eq giant in the wiki with a JWST CH₄ inference.
- [[2025_Barat_V1298Tau-b]] — CH₄ detected at 6σ on the young sub-Neptune progenitor V1298 Tau b (log VMR ≈ −6.2⁺⁰·³⁻⁰·³); abundance is **7σ lower** than equilibrium prediction at T_eq ~ 670 K; serves as a "**methane thermometer**" requiring T_int ≈ 500 K + K_zz ~ 10⁷–10⁸ cm² s⁻¹ to dredge methane-poor gas from the deep atmosphere. CH₄ thus diagnostically traces the interior thermal state of low-mass planets.
- [[2025_LibbyRoberts_Kepler51d]] — tentative 2.2σ detection on the [[super-puff]] [[Kepler-51d]] NIRSpec/PRISM; ppb-level mixing ratio (66⁺⁷²⁻⁴⁵ ppb in ExoTR best fit); interpreted as **upwelling from the deeper atmosphere**, not a bulk-abundance probe.
- [[2025_Ahrer_GJ3090b]] — confident **non-detection** at ∼3.4 μm on warm sub-Neptune [[GJ3090b]]; the absence drives the high-metallicity inference (>100× solar at 3σ).
- [[2025_Ahrer_WASP94Ab]] — upper-limited (log VMR < −5.83 at 2σ) on misaligned hot Jupiter WASP-94 Ab; consistent with thermochemical equilibrium at T_eq = 1508 K.
