---
type: species
aliases: [carbon dioxide]
tags: [carbon-bearing, metallicity-tracer, mid-infrared, hub]
---

# CO₂

Carbon dioxide — a metallicity-sensitive tracer with a strong 4.3 μm absorption feature accessible to [[JWST-NIRSpec]] G395H and a stronger 15 μm band accessible to [[JWST-MIRI]]. The first JWST detection of CO₂ in any exoplanet atmosphere was made on WASP-39 b from the ERS PRISM data ([[JWST-ERS-1366]]; original ERS papers not yet ingested), now also confirmed across four independent reductions in [[2026_RoyPerez_WASP39b]].

## Detection status

- **Confirmed detection (hot Jupiter):** [[WASP-39b]] — first JWST CO₂ detection in any exoplanet atmosphere; confirmed across all four reduction pipelines in [[2026_RoyPerez_WASP39b]].
- **Confirmed detection (mini-Neptune):** [[TOI-1130b]] — 3.3σ from the 4.3 μm band in combined NIRSpec G395H + NIRISS SOSS + TESS + CHEOPS transmission ([[2026_Barat_TOI1130b]]); log mass fraction ≈ −1.2. C/O < 0.75 (3σ); consistent with formation beyond the water ice line + disc migration.
- **Ruled out as bulk gas (rocky M-dwarf planets, MIRI/LRS emission):**
  - [[GJ486b]] — Venus-like thick CO₂ excluded; only <1 ppm CO₂ at ≤10 bar allowed ([[2024_WeinerMansfield_GJ486b]]).
  - [[LTT1445Ab]] — pure 1/10/100 bar CO₂ excluded at 4.2σ / 6.6σ / 6.8σ ([[2024_Wachiraphan_LTT1445Ab]]); refined to log P_CO₂ < −1.0 bar at 2σ via climate-constrained inversion ([[2026_Wogan_LTT1445Ab]]); X(CO₂)/(H₂+He) < 0.1 at P_opaque > 10⁻⁴ bar from G395H transmission ([[2026_Batalha_LTT1445Ab]]).
- **Ruled out as bulk gas (rocky M-dwarf planets, transmission):**
  - [[GJ1132b]] — pure-CO₂ rejected at >3σ; joint with MIRI emission, CO₂ <10 mbar ([[2025_Bennett_GJ1132b]]).
  - [[L98-59c]] — H₂/CO₂ mixtures with ≥10% CO₂ excluded at 3σ; high-MMW CO₂-rich atmospheres remain compatible ([[2024_Scarsdale_L98-59c]]).
  - [[GJ486b]] — pure-CO₂ rejected to 6.5σ in primary [[Eureka]] reduction ([[2023_Moran_GJ486b]]).
- **Compatible with featureless data (high MMW required):**
  - [[LHS475b]] — pure-CO₂ atmospheres remain consistent with featureless spectrum (χ² ≈ 1.0); 3σ feature upper limit 49 ppm at 4.3 μm ([[2023_Lustig-Yaeger_LHS475b]]).
  - [[L168-9b]] — pure-CO₂ tested; MIRI 15 μm eclipse proposed as the discriminator ([[2025_Alam_L168-9b]]).

## Open issues

- **Stellar CO₂ contamination.** [[2025_Bennett_GJ1132b]] speculates that spatially variable stellar molecular bands (CO, possibly CO₂) could mimic planetary features in the 4.3 μm region for M-dwarf transits.
- **MIRI follow-up of high-MMW CO₂ candidates.** Pure-CO₂ scenarios on rocky M-dwarf planets typically remain compatible with NIR-only featureless spectra (LHS 475 b, L 168-9 b); the 15 μm CO₂ band on MIRI is the next discriminator and is being deployed across the rocky-planet sample.

## Papers

- [[2025_Gressier_HATP26b]] — **strongest CO₂ detection to date** in a Neptune-mass planet (HAT-P-26 b NIRSpec G395H; lnB = 85.64, ≫5σ); log X(CO₂) ≈ −2.91; spans both NRS1 (4.3 μm region edge) and NRS2.
- [[2025_Ahrer_KELT7b]] — **tentative only** (Δ ln Z = 0.9–1.5) on hot Jupiter KELT-7 b NIRSpec G395H; log X(CO₂) ≈ −8.5⁺⁶ from POSEIDON free retrieval — much lower than expected for a hot Jupiter with photochemistry; consistent with high-altitude cloud masking the 4.3 μm feature.
- [[2025_Felix_TOI-270d]] — decisive detection on temperate sub-Neptune TOI-270 d (Bayes factor 3 × 10⁷; log VMR ≈ −1.3); independent reanalysis confirming Benneke 2024 detection. Sub-Neptune analog of the WASP-39 b CO₂ benchmark.
- [[2025_FernandezRodriguez_K2-18b]] — **marginal at ~2σ** on K2-18 b NIRISS+NIRSpec G395H (1.99σ in fiducial; non-detection in comprehensive 13-species retrieval); log VMR ≈ −3.94⁺¹·⁶⁸₋₄·²⁰; bimodal posterior. Configuration-dependent; Hu et al. 2025 NIRISS+NIRSpec+MIRI joint retrieval (not ingested) gets 3.7σ.
- [[2025_Luque_K2-18b]] — CO₂ reduction-dependent on K2-18 b panchromatic spectrum: two-sided posterior with log VMR ≈ −1.66 to −2.13 under SPARTA+JExoRES reductions in SCARLET; broader under exoTEDRF.
- [[2025_Schmidt_K2-18b]] — **no robust CO₂ detection** on K2-18 b across 60 NIRISS+NIRSpec data combinations × POSEIDON/BeAR retrievals. Maximum significance 2.3σ (Bayes factor < 5) in a single combination; most combinations show no evidence (Bayes factor < 3). 95% upper limit log CO₂ < −1.70 from ensemble posterior. Demonstrates in Appendix A that even the original Madhusudhan et al. 2023 (not ingested) data with their pipeline produces at most a 2.5σ CO₂ feature — i.e. the previous detection was reduction-specific.
- [[2025_Madhusudhan_K2-18b-MIRI]] — CO₂ not strongly constrained by MIRI/LRS alone; assumed at NIR-determined 1% abundance.
- [[2025_Mukherjee_GJ436b]] — **2σ tentative detection** in panchromatic 2.4–12 μm JWST emission spectrum of GJ 436 b; log VMR(CO₂) = −3.23⁺¹·⁶⁶₋₃·₃₀ (free-chemistry retrieval). The only molecule reaching ~2σ in the spectrum; self-consistent equilibrium models prefer ≥ 300× solar, disequilibrium ≥ 80× solar. JWST 3.6 μm flux fainter than Spitzer-era; overturns Spitzer-era extreme-metallicity / hot-interior inference.
- [[2025_Ohno_GJ1214b]] — **dominant spectral discriminant** for the [[GJ1214b]] panchromatic HST/WFC3 + NIRSpec/G395H + MIRI/LRS analysis. The 4.3 μm CO₂ feature in Schlawin 2024a NIRSpec data (2.4σ detection) is unmasked by the thick photochemical haze and drives the inference of **extreme metallicity [M/H] ≈ 3.5–3.8** (i.e. CO₂-dominated atmosphere where H₂ is no longer the main constituent). Per Hu & Seager 2014, abundant CO₂ only emerges under hydrogen-depleted conditions at GJ 1214 b's temperature.
- [[2025_Fu_statistical-trends]] — first wiki **population-level CO₂ study**. CO₂-L band index ([4.25–4.4 μm] − [2.9–3.7 μm]) shows temperature-dependent non-monotonic peak around 900 K for Z = 30× solar / C/O = 0.3 (PLATON forward grid). Population favors super-solar metallicity (>3× solar) + low C/O (<0.7). Joint mass-metallicity-correlation fit (BIC = 232) prefers freely fitted mass-metallicity over Solar System trend (BIC = 617) or uniform metallicity (BIC = 295).
- [[2025_Sikora_HD80606b]] — detected at 3.7–4.4σ on highly eccentric hot Jupiter HD 80606 b NIRSpec G395H emission spectrum post-periapse (NRS2 4.3 μm); chemical-equilibrium-retrieval preferred.
- [[2025_LustigYaeger_WASP17b]] — tentative 0.9σ detection on the WASP-17 b nightside; nightside abundance lower than dayside, an inverted day–night gradient that is unexplained.
- [[2026_Radica_WASP96b]] — detected in WASP-96 b transmission; log VMR ≈ −4.91 to −4.15.
- [[2026_Heinke_HATP12b]] — detected at >10σ in HAT-P-12 b via the 4.3 μm ν₃ band; requires NIRSpec.
- [[2026_Ashtari_HATS75b]] — detected at >3σ on HATS-75 b NIRSpec PRISM (TLS framework).
- [[2026_RoyPerez_WASP39b]] — confirmed detection in WASP-39 b across all four reduction pipelines.
- [[2025_Murphy_WASP107b]] — first **limb-resolved CO₂ asymmetry**; WASP-107 b morning limb log VMR ≈ −3.6 vs. evening −5.2 (~40×); larger amplitude than SO₂; quench-driven origin (CO₂ quenches at lower pressure than CH₄, retaining the photospheric T-gradient).
- [[2025_Verma_HD209458b]] — HD 209458 b CO₂ detected at 7.8σ in STIS+WFC3+NIRCam free-chemistry SANSAR retrieval (log VMR = −7.52⁺⁰·³⁰⁻⁰·²⁶); but NIRCam-only retrieval gives log VMR ≈ −5.31 — a 2-dex overestimate. Demonstrates that the 4.3 μm CO₂ feature alone, without optical baseline, cannot constrain CO₂ abundance robustly.
- [[2025_Barat_V1298Tau-b]] — CO₂ detected at **35σ** on the young sub-Neptune progenitor V1298 Tau b (~1000 ppm 4.3 μm feature); strongest CO₂ detection in the wiki for a sub-Neptune-mass planet; metallicity ~0.6× solar; SO₂ at 4σ + OCS at 3.5σ (tentative) accompany.
- [[2025_Deka_WASP39b]] — CO₂ retrieved across all four [[NEXOTRANS]] chemistry models on WASP-39 b NIRISS+PRISM+MIRI panchromatic data; log VMR ranging −4.65 (free) to −2.5 (equilibrium); offset in equilibrium-offset model accommodates the shape difference between equilibrium and observed feature.
- [[2025_Bennett_GJ1132b]] — pure-CO₂ rejected at >3σ on GJ 1132 b; joint with MIRI/LRS, CO₂ <10 mbar.
- [[2025_Alam_L168-9b]] — pure-CO₂ tested on L 168-9 b; 15 μm MIRI eclipse proposed as confirmation path.
- [[2024_WeinerMansfield_GJ486b]] — MIRI/LRS emission rules out Venus-like CO₂ on Gl 486 b.
- [[2024_Wachiraphan_LTT1445Ab]] — MIRI/LRS rules out pure 1/10/100 bar CO₂ on LTT 1445 A b.
- [[2024_Scarsdale_L98-59c]] — H₂/CO₂ mixtures with ≥10% CO₂ excluded on L 98-59 c at 3σ.
- [[2023_May_GJ1132b]] — pure-CO₂ tested on GJ 1132 b Visit 1; poorer fit than H₂O-dominated.
- [[2023_Moran_GJ486b]] — pure-CO₂ on GJ 486 b ruled out at 6.5σ (Eureka) / 2.3σ (others).
- [[2023_Lustig-Yaeger_LHS475b]] — pure-CO₂ remains consistent with featureless LHS 475 b spectrum.
- [[2025_Crouzet_HATP12b]] — detected at 12.2σ on HAT-P-12 b NIRSpec G395M (foundational JWST detection on this target).
- [[2025_AcunaAguirre_WASP80b]] — present on WASP-80 b in joint interior–atmosphere retrieval (per cited input retrievals).
- [[2025_Roy_LP791-18c]] — **ruled out** on LP 791-18 c (log X < −1.97 at 2σ; CH₄/CO₂ > 12 at 2σ); a sharp diversity contrast with K2-18 b and TOI-270 d at comparable T_eq.
- [[2025_Ahrer_WASP94Ab]] — **CO₂ at 11σ** on misaligned hot Jupiter WASP-94 Ab NIRSpec G395H (Δ ln Z = 59 in HyDRo); log VMR ≈ −4.25; used to compute the substellar C/O.
- [[2025_Ahrer_GJ3090b]] — tentative on warm sub-Neptune GJ 3090 b NIRSpec G395H; chemically consistent retrievals favor sub-solar C/O with CO₂ as part of the high-MMW absorbers; free retrievals cannot pin down individual species.
