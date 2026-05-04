---
type: concept
aliases: [SO2 shoreline, SO2 photochemical shoreline, Crossfield shoreline]
tags: [photochemistry, hot-jupiter, neptune-mass, sub-neptune, sulfur, metallicity-tracer]
---

# SO₂ photochemical shoreline

A photochemical "shoreline" in the (atmospheric metallicity, equilibrium temperature) plane separating warm-giant atmospheres in which photochemical [[SO2]] production from H₂S / H₂O is observable from those in which it is suppressed. The original conceptual proposal is Crossfield 2023 (ApJL 952:L18; not yet ingested); the **formal grid-mapping paper is [[2025_Crossfield_SO2shoreline]]**, which uses 936 [[HELIOS]] + [[VULCAN]] + [[petitRADTRANS]] models to define the shoreline at the 1 ppm SO₂ contour and characterize its dependencies. Empirical population testing across 11 JWST giant-planet transmission spectra is in [[2025_Gressier_HATP26b]]: the SO₂ trend rises steeply with metallicity at low [M/H] and more gradually above ~30× solar, broadly consistent with the Crossfield 2025 shoreline.

## Theoretical mapping (Crossfield 2025)

[[2025_Crossfield_SO2shoreline]] establishes the formal shoreline using 936 self-consistent HELIOS + VULCAN + petitRADTRANS models at HAT-P-26 b system parameters. Key dependencies:

- **C/O ratio** is the strongest knob: increasing C/O 0.30 → 0.80 substantially decreases SO₂ across all (T_eq, [M/H]); SO₂ detection therefore implies either C/O ≲ stellar, high metallicity, or both.
- **Metallicity** drives the shoreline geometry: steep boundary at low T_eq, shallower at high T_eq.
- **XUV irradiation: surprisingly weak effect** (~30× variation shifts shoreline modestly for T_eq < 1400 K) — encouraging because most stellar XUV histories are unmeasured.
- **Internal temperature: essentially irrelevant** (SO₂ forms at 1–100 μbar, decoupled from deep T_int).
- **K_zz: weak above T_eq ≳ 600 K, strong below.**
- **SO₂ is never the dominant sulfur species** in the modeled atmospheres; H₂S, S₂, NS, SO, SH, S₈, atomic S frequently match or exceed it. SO₂'s privilege is observability, not abundance.

## Empirical population to date

[[2025_Gressier_HATP26b]] performs a uniform [[TauREX3]] reanalysis of 11 JWST transmission spectra (the ten in Fu et al. 2025 + HAT-P-26 b) spanning [M/H] ≈ 3 → 300× solar and T_eq ≈ 600 → 2500 K:

- **On the trend (within 3σ of Crossfield 2023):** GJ 3470 b (sub-Neptune, T_eq ≈ 600 K, [M/H] ~125× solar; [[H2S]]/SO₂ from Beatty et al. 2024 — not yet ingested), [[HAT-P-26b]] (Neptune-mass, T_eq ≈ 1000 K, ~11× solar — first Neptune-mass detection), [[WASP-39b]] (hot Saturn, T_eq ≈ 1166 K, ~6.5× solar), HD 189733 b (hot Jupiter, T_eq ≈ 1209 K, ~6.5× solar), [[WASP-80b]] (warm gas giant, T_eq ≈ 825 K, ~6× solar — upper limit only).
- **Upper-limit-only on the trend:** WASP-127 b (sub-Saturn, T_eq ≈ 1427 K), HIP 67522 b (young hot-Jupiter analog, T_eq ≈ 1175 K), HD 209458 b, GJ 1214 b (hot mini-Neptune; SO₂ < 10⁻³.⁶⁴ from Schlawin et al. 2024 / Ohno et al. 2025 — both not yet ingested).
- **Outlier:** **WASP-107 b at 7σ below the predicted trend** (40× solar metallicity; Sing et al. 2024 — not yet ingested). Tension flagged for combined NIRSpec + NIRCam + MIRI retrieval. [[2025_Murphy_WASP107b]] resolves limb-resolved SO₂ at log X = −4.7 (morning) / −5.4 (evening); the limb-averaged value (~10⁻⁵) sits below the trend, but the cooler morning limb has SO₂ closer to the shoreline expectation, consistent with photochemistry being suppressed at the hotter evening limb.
- **Excluded as outlier:** WASP-121 b (T_eq ≈ 2450 K, S = 5966 S⊕) — the ultra-hot Jupiter regime is outside Crossfield 2023's modeled (T_eq, [M/H]) grid; thermal dissociation likely dominates.

[[2026_Radica_WASP96b]] independently places WASP-96 b (T_eq ≈ 1300 K, ~10–20× solar) on the proposed shoreline at lnB = 2.69 (tentative).

## Open questions

- **How robust is the SO₂ inference to data-reduction choice?** [[2026_RoyPerez_WASP39b]] documents up to 2 dex variation in retrieved abundances on the same WASP-39 b ERS PRISM data — pipeline systematics could move multiple population points.
- **Why is WASP-107 b 7σ low?** Combined Bayesian retrieval with NIRSpec + NIRCam + MIRI ([[JWST-NIRCam]] + Welbanks et al. 2024 + Dyrek et al. 2023) is the required next step; possible cooler-than-expected upper atmosphere or aerosol shielding above the SO₂-active layer.
- **What is the upper T_eq limit before thermal dissociation suppresses SO₂?** WASP-121 b's exclusion from the test sample suggests it lies above this limit; somewhere between 1500 and 2500 K.
- **Can H₂S (the precursor) be co-detected to test the photochemistry directly?** [[2025_Gressier_HATP26b]] reports only a tentative ~2σ H₂S on HAT-P-26 b; [[2026_Heinke_HATP12b]] gets a firmer (but still marginal) detection.
- **Does the shoreline extend to even lower mass?** GJ 3470 b is the lowest-mass anchor at 14 M⊕ / 600 K; whether HAT-P-26 b's detection extends to true sub-Neptunes (M < 10 M⊕) is the natural follow-up.

## Tensions

- **WASP-107 b 7σ low.** Constraint comes from a single G395H reanalysis (Sing et al. 2024; not yet ingested); combined retrieval including NIRCam (Welbanks et al. 2024) and MIRI (Dyrek et al. 2023) — both not yet ingested — pending.

## Papers

- [[2025_Crossfield_SO2shoreline]] — **foundational shoreline-mapping paper**; 936 HELIOS + VULCAN + petitRADTRANS models; 1 ppm SO₂ contour as the formal shoreline; documents that C/O and [M/H] are the dominant controls and that XUV/K_zz/T_int matter weakly above T_eq ≳ 600 K. SO₂ never the dominant sulfur species — observability privileges it.
- [[2025_Gressier_HATP26b]] — establishes the empirical population test across 11 JWST giants; HAT-P-26 b = first Neptune-mass anchor (lnB = 13.46, log X(SO₂) ≈ −4.40); ~10× solar metallicity, C/O ≈ 0.14.
- [[2026_Radica_WASP96b]] — places WASP-96 b on the proposed shoreline; tentative SO₂ at lnB = 2.69; ~10–20× solar metallicity.
- [[2025_LustigYaeger_WASP17b]] — tentative 2.3σ SO₂ on the WASP-17 b nightside via iESR-PIE; complementary day-night photochemistry test.
- [[2026_RoyPerez_WASP39b]] — WASP-39 b SO₂ confirmed across four reductions but absolute abundance varies ≲ 2 dex.
- [[2025_Murphy_WASP107b]] — first **limb-resolved** SO₂ on a JWST giant; WASP-107 b morning limb has ~5× more SO₂ than the evening, consistent with photochemistry quench gradient across the terminator.
