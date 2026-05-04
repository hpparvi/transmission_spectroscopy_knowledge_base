---
type: species
aliases: [methane]
tags: [carbon-bearing, photochemistry-sensitive, near-infrared, hub]
---

# CH₄

Methane — expected in cool/reduced atmospheres in thermochemical equilibrium; its detection or non-detection constrains C/O ratio, metallicity, and disequilibrium processes (quenching, photochemistry). Strong 3.3 μm absorption feature accessible to [[JWST-NIRSpec]] G395H. CH₄ has been a recurring "ghost detection" in early JWST rocky-planet work, with multi-visit data subsequently retiring those inferences.

## Detection status

No firm CH₄ detection on any wiki target. Recurring pattern: tentative single-visit inference → ruled out by multi-visit follow-up.

- **Tentative, then retired:**
  - [[GJ1132b]] — ~1% CH₄ tentatively inferred in Visit 1 (Bayes factor 27 / 3.1σ vs no CH₄, [[2023_May_GJ1132b]]); not reproduced in Visit 2; **retired** by the four-visit coadded spectrum at >10σ ([[2025_Bennett_GJ1132b]]).
- **Ruled out as bulk gas:**
  - [[GJ486b]] — pure CH₄ disfavored at χ²ν = 2.1 ([[2023_Moran_GJ486b]]).
  - [[LHS475b]] — pure CH₄ rejected at ≥5σ from absence of 3.3 μm band; 3σ feature upper limit 38 ppm ([[2023_Lustig-Yaeger_LHS475b]]).
  - [[L168-9b]] — pure CH₄ excluded by featureless NIR + MIR spectrum ([[2025_Alam_L168-9b]]).
- **No detection on hot Jupiters:** WASP-39 b's PRISM data, including the [[2026_RoyPerez_WASP39b]] re-analysis, does not list CH₄ among detected species — consistent with thermochemical equilibrium at ~1100 K disfavoring CH₄.

## Open issues

- **Single-visit CH₄ inferences are unreliable.** The GJ 1132 b cycle ([[2023_May_GJ1132b]] → [[2025_Bennett_GJ1132b]]) is the cautionary example: multi-visit stacking retired a 3.1σ Bayes-factor "detection." [[multi-visit-stacking]] is now the de facto requirement for any CH₄ claim on a small planet.
- **Photochemical quenching expectations.** No wiki paper has yet probed a planet cool enough to test CH₄ as a thermochemical-equilibrium expectation; the quenching question remains open for cooler future targets.

## Papers

- [[2025_Felix_TOI-270d]] — **decisive detection** on temperate sub-Neptune TOI-270 d (T_eq = 360 K) NIRSpec G395H + NIRISS SOSS; Bayes factor 3 × 10²⁵; log VMR ≈ −1.7; reproduces prior detections by Benneke et al. 2024 (not ingested) and Holmberg & Madhusudhan 2024 (not ingested).
- [[2025_FernandezRodriguez_K2-18b]] — **robust detection at 4.16σ–4.62σ** across all 12 retrieval configurations on K2-18 b NIRISS+NIRSpec; log VMR ≈ −1.7 to −1.0; one of the cleanest sub-Neptune CH₄ detections; survives leave-one-out and comprehensive 13-species retrieval tests.
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
