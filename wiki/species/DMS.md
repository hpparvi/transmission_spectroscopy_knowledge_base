---
type: species
aliases: [dimethyl sulfide, methylthiomethane, (CH3)2S]
tags: [sulfur-bearing, biosignature-candidate, sub-neptune, hycean]
---

# DMS — dimethyl sulfide ((CH₃)₂S)

A volatile sulfur-organic molecule (Seager et al. 2013; not ingested) proposed as a potential biosignature for habitable sub-Neptune ("Hycean") atmospheres — its production on Earth is dominated by marine plankton, with no known abiotic terrestrial source at significant scale. JWST searches at the 4.5 μm absorption edge are sensitive to its presence at ~10⁻⁵ to 10⁻⁴ VMR. Its detection on [[K2-18b]] in Madhusudhan et al. 2023 (not ingested) sparked the most-watched biosignature debate in the JWST era; the MIRI follow-up ([[2025_Madhusudhan_K2-18b-MIRI]]) reasserts DMS+DMDS at 3σ over 6–12 μm. Subsequent independent reanalyses — [[2025_FernandezRodriguez_K2-18b]] (comprehensive NIR retrieval, Bayes factor < 1), [[2025_Luque_K2-18b]] (joint NIR+MIR retrieval, Δln Z never reaches 5), [[2025_PicaCiamarra_K2-18b]] (650-molecule agnostic search; 10 alternative hydrocarbons fit comparably), [[2025_Schmidt_K2-18b]] (60-data-combination ensemble across two NIRISS and four NIRSpec reductions; max DMS significance 2.2σ; 95% upper limit log C₂H₆S < −3.70), and Welbanks-Nixon 2025 (not ingested) — concur that **DMS is not robustly preferred** under comprehensive retrievals. Status as of mid-2025: **disputed**, with methodological consensus tilting strongly against detection.

The wiki has no firm DMS detection on any target. The opacity database (Sharpe et al. 2004; HITRAN cross-sections at 1 bar, 278 K only) is sparse — limiting reliable retrievals at sub-Neptune temperatures (~1 mbar photosphere).

## Papers

- [[2025_Madhusudhan_K2-18b-MIRI]] — **DMS+DMDS preferred at 3.4σ over a flat spectrum / 3.2σ over CH₄+CO₂-only baseline** in MIRI/LRS canonical retrieval (CH₄+CO₂+X). Individual DMS-only 2.9σ; DMDS-only 3.2σ; the two are spectrally degenerate. Retrieved log X(DMS) = −3.42⁺¹·¹⁶₋₁·⁴⁴ ≈ 10⁻³.5 — ~10× the abundance for biogenic flux ~20× Earth (Tsai et al. 2024; not ingested). Claim contested by [[2025_Luque_K2-18b]] and [[2025_PicaCiamarra_K2-18b]].
- [[2025_Luque_K2-18b]] — **DMS/DMDS not preferred** in panchromatic NIR+MIR retrieval. Joint Δln Z = −0.3 to +2.8 across reductions; never reaches Δln Z ≥ 5. Ethane (C₂H₆) provides an equally good fit due to shared methyl C–H stretching (3.4 μm) and H–C–H bending (6.9 μm) bands. ~26 MIRI transits needed for 3σ rejection of a flat line.
- [[2025_PicaCiamarra_K2-18b]] — DMS reaches ≥2.5σ in both MIRI pipelines and all three retrieval codes, AND in the NIR data (no offsets). **However, diethyl sulfide and methacrylonitrile reach the same threshold simultaneously** — DMS is no longer spectroscopically unique. 8 additional hydrocarbons fit MIRI comparably.
- [[2025_Taylor_K2-18b-MIRI]] — **model-agnostic Gaussian-feature analysis** of the [[2025_Madhusudhan_K2-18b-MIRI]] MIRI/LRS spectrum: 5 of 6 Gaussian tests yield "no evidence" (Δln Z < 1); only fixed-Gaussian at 7 + 8.8 μm gives weak evidence (Δln Z = 1.21, ~2σ). Demonstrates the M25 detection is inflated by curated 2-molecule canonical model + non-nested model comparison.
- [[2025_FernandezRodriguez_K2-18b]] — **DMS not statistically preferred** on K2-18 b under comprehensive retrievals (Bayes factor < 1; ln Z = 8.52 vs 8.62 for CO₂+CH₄ alone); 95% upper limit log X(DMS) < −4.39. Tentative 2.13σ–2.31σ in some simplified retrieval setups but not in comprehensive ones.
- [[2025_Schmidt_K2-18b]] — **DMS not robustly evidenced** under a 60-data-combination ensemble retrieval of NIRISS+NIRSpec. Max significance 2.2σ for a single data combination (exoTEDRF R≈100); marginal hints vanish at higher resolution or with FIREFLy reductions. 95% upper limit log C₂H₆S < −3.70 from the combined ensemble posterior. The paper formalizes the "ensemble posterior" method (marginalizing over data-level choices) as guarding against statistical artifacts from any single reduction.
- [[2025_Felix_TOI-270d]] — tested for on TOI-270 d; not detected; not preferred over CO₂+CH₄ alone.
- [[2025_Madhusudhan_subneptunes]] — review/perspective on sub-Neptune frontier; reaffirms K2-18 b DMS detection as a "very tentative inference" pending independent confirmation; lists DMS as one of five most-promising sub-Neptune biosignature candidates (DMS, CS₂, OCS, CH₃Cl, N₂O).

(Madhusudhan et al. 2023 K2-18 b initial NIR DMS claim not yet ingested; reanalyses by Welbanks-Nixon et al. 2025 and Stevenson et al. 2025 also not yet ingested.)
