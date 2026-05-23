---
type: paper
bibkey: 2025_PicaCiamarra_K2-18b
authors: [Pica-Ciamarra, L., Madhusudhan, N., Cooke, G. J., Constantinou, S., Binet, M.]
year: 2025
venue: arXiv
arxiv: 2505.10539
targets: [K2-18b]
instruments: [JWST-NIRISS, JWST-NIRSpec, JWST-MIRI]
methods: [transmission-spectroscopy, atmospheric-retrievals]
species_detected: []
species_tentative: [DMS, DMDS]
species_ruled_out: []
codes: [POSEIDON, petitRADTRANS, Aurora, MultiNest, JExoRES]
tags: [sub-neptune, hycean-debate, dms-claim, agnostic-search, methodology, panchromatic, multi-pipeline-cross-check]
ingested: 2026-05-16
---

# A Systematic Search for Trace Molecules in Exoplanet K2-18 b

**Authors:** Pica-Ciamarra, Madhusudhan, Cooke, Constantinou, Binet (2025, arXiv:2505.10539)
**Targets:** [[K2-18b]] · **Instruments:** [[JWST-NIRISS]] SOSS + [[JWST-NIRSpec]] G395H + [[JWST-MIRI]] LRS · **Program:** [[JWST-GO-2722]] (PI: Madhusudhan)

## TL;DR

The first **agnostic, 650-molecule search** for trace gases in K2-18 b's atmosphere, using all available JWST observations (NIRISS+NIRSpec from Madhusudhan 2023 not ingested; MIRI from [[2025_Madhusudhan_K2-18b-MIRI]] both JExoRES and JexoPipe reductions). Atmospheric retrievals are run individually for each of 650 candidate species (HITRAN-database hydrocarbons, halocarbons, nitriles, sulfur-bearing molecules, organics) in CH₄ + CO₂ + X canonical models with three independent retrieval codes ([[POSEIDON]], **VIRA** — latest in the [[Aurora]] family, and [[petitRADTRANS]]). Only species reaching ≥2.5σ in both MIRI pipelines and all three codes are kept. **11 molecules survive in MIRI; only 3 reach ≥2.5σ in the NIR data simultaneously.** Beyond DMS, the most promising candidates are **diethyl sulfide (CH₃CH₂)₂S** and **methacrylonitrile (C₄H₅N)** — both biogenic on Earth but with no known significant astrophysical sources at the inferred ~10⁻³–10⁻⁴ abundances. Six additional hydrocarbons (propyne, cyclohexane, 2-butene, trans-2-pentene, butane, cyclopentane) are equally consistent with the MIRI JExoRES data but have known abiotic chemical pathways. **DMS is no longer spectroscopically unique** at the present S/N; the data permit a family of solutions whose discriminator is physical/chemical plausibility rather than statistical significance.

## Key findings

- **Three molecules pass all data cuts simultaneously:** [[DMS]], diethyl sulfide ((CH₃CH₂)₂S), and methacrylonitrile (C₄H₅N). Each reaches ≥2.5σ in both MIRI pipelines (JExoRES and JexoPipe), all three retrieval codes (VIRA, petitRADTRANS, POSEIDON), AND the NIR data (with no detector offsets). Retrieved abundances ~10⁻³–10⁻⁴.
- **11 molecules pass MIRI but not NIR.** [[DMDS]], chloroethane, propyne, bromoethane, 2-butene, dichloromethane, cyclohexane, butane, allyl chloride, cyclopentane, trans-2-pentene. All reach ≥2.5σ in both MIRI pipelines across all three codes but ≤2σ (or upper-limit only) in NIR. Either NIR S/N is insufficient or the molecule contributes only at MIRI wavelengths.
- **DMS detection is reproducible but not unique.** This work confirms the 2.8σ DMS / 2.7σ DMDS preference reported in [[2025_Madhusudhan_K2-18b-MIRI]] across all three independent retrieval codes — within ±0.2σ. **It does not validate uniqueness** — DMS is one of a family of ~11 spectroscopically equivalent fits at MIRI wavelengths.
- **No molecule reaches 2σ with NIRISS/NIRSpec offset included.** When inter-detector offsets are allowed in the NIR retrievals, no candidate molecule (including DMS) reaches 2σ. The detection significance is fundamentally limited by the M-dwarf systematics budget.
- **Diethyl sulfide and methacrylonitrile have no known significant astrophysical sources.** Diethyl sulfide is biogenic (plants); chemical-warfare-simulant industrial production. Methacrylonitrile is anthropogenic (polymer industry). Their inferred ~10⁻³–10⁻⁴ abundances are not explainable by known abiotic chemistry — making them "interesting but unmotivated" candidates rather than biosignatures.
- **Methodology message.** The Madhusudhan 2025 (MIRI) canonical-model approach inflates significance when X is restricted to one molecule at a time. A **maximal Bayesian model comparison** including all 20 molecules from M25 yields the same canonical preference (~2σ over featureless), but it does NOT extend to identifying X uniquely. **The retrieval-significance number is data-quality-limited, not chemistry-limited.**
- **Of the 6 hydrocarbons** flagged by Welbanks, Nixon et al. 2025 (not ingested) at ≥2.7σ in MIRI JExoRES (propyne, cyclohexane, 2-butene, trans-2-pentene, butane, cyclopentane), **all are confirmed** in this work to reach ≥2.7σ across multiple retrieval codes — but only propyne has known abiotic chemistry (atmospheric photochemistry, ISM detection) that scales to the inferred ~10⁻⁵ abundance.
- **Mass abundance scaling agreement.** Retrieved volume mixing ratios from MIRI are consistent between JExoRES and JexoPipe within 1σ. NIR upper limits at ~10⁻⁴ are consistent with MIRI-retrieved medians at ~10⁻³ at 1σ — non-detections in NIR don't rule out the MIRI inferences.

## Methods

**Data.** All public JWST observations of K2-18 b: NIRISS SOSS + NIRSpec G395H from Madhusudhan et al. 2023 (~0.8–5.2 μm; not ingested), MIRI/LRS from [[2025_Madhusudhan_K2-18b-MIRI]] — both JExoRES and JexoPipe reductions.

**Candidate molecules.** 650 species selected from the HITRAN cross-section database (Gordon et al. 2022) and the [[POSEIDON]] native library:
- Hydrocarbons (90 species; W25 list as starting point)
- Halocarbons + hydrohalocarbons + CFCs + HCFCs + HFCs (350+ species)
- Sulfur molecules (29 species incl. DMS, DMDS, diethyl sulfide, CS₂, OCS, H₂S, SO₂, CH₃SH, etc.)
- Nitriles + nitrogenated hydrocarbons (57 species)
- Fully-fluorinated + halogenated alcohols/ethers (96 species)
- Alcohols, ethers, oxygenated hydrocarbons (144 species)
- Other (29 species)

Cross-sections preferentially adopted at T ~ 300 K, P ~ 1 bar; nearest-available otherwise. 16 species excluded due to missing cross-section data in the mid-IR or unverifiable molecular weight.

**Retrieval framework.** Bayesian model comparison against a CH₄ + CO₂ baseline (the M25 canonical setup) for each of the 650 species; X added as a single free volume-mixing-ratio parameter. Three independent codes:
- **VIRA** (Constantinou & Madhusudhan 2024) — latest in the [[Aurora]] family; same architecture as AURA (M25).
- [[petitRADTRANS]] (Mollière et al. 2019; Nasedkin et al. 2024) — mass-mixing-ratio prior U(−11, −0.1).
- [[POSEIDON]] (MacDonald & Madhusudhan 2017; MacDonald 2023) — primary; volume-mixing-ratio prior U(−12, −0.3); 11 free parameters + 3 mixing ratios.

P-T profile from Madhusudhan & Seager 2009 (6 parameters); patchy clouds + Rayleigh hazes (4 parameters, MacDonald & Madhusudhan 2017 / Pinhas et al. 2019). Nested sampling with [[MultiNest]].

**Filtering pipeline (Fig. 1).** Each species must (1) reach ≥2.5σ in MIRI JExoRES with POSEIDON, then (2) be confirmed at ≥2.5σ in MIRI JexoPipe, then (3) re-verified with VIRA and petitRADTRANS, then (4) tested for ≥2.5σ in the NIRISS+NIRSpec data (no offsets). Only species passing all four stages are "promising."

## Caveats & limitations

- **Detection significances are not corrected for the 650-trial look-elsewhere effect.** Across 650 species, the expected number of ≥2σ false positives by chance is ~30 — comparable to the number actually detected. The authors note this and explicitly frame their results as "candidate species" rather than detections.
- **The 2.5σ threshold is generous.** Moderate evidence per Jeffreys' scale starts at 2.7σ (ln B ≥ 2.5); 5σ is the standard for a discovery claim. None of the 11 MIRI-only candidates pass 3.5σ.
- **Single-molecule X-replacement.** Each X is tested independently — does not search for *combinations* (e.g., 1% propyne + 0.5% diethyl sulfide). The true atmospheric inventory may be a multi-species mixture not represented in any single-molecule retrieval.
- **Cross-section pressure mismatch.** Many of the 650 species have lab cross-sections at 1 bar, 298 K — not the ~1 mbar photospheric pressure of K2-18 b. Real cross-sections may differ; retrieved abundances biased by an unknown amount.
- **Identical baseline to [[2025_Madhusudhan_K2-18b-MIRI]] (CH₄+CO₂+X).** Inherits its weakness — the choice of CH₄+CO₂ as a fixed baseline excludes alternative scenarios with no CH₄+CO₂ background (which [[2025_Luque_K2-18b]] note is consistent with the data).
- **Most candidate molecules have no astrophysical motivation.** Cyclohexane, methacrylonitrile, allyl chloride, etc. are predominantly industrial/biogenic on Earth with no known synthesis routes at the inferred 10⁻³–10⁻⁴ abundances in temperate H₂-rich atmospheres. The "promise" of these species is statistical, not chemical.

## Open questions / follow-ups

- **What's the photochemical inventory of K2-18 b's atmosphere?** Self-consistent photochemical models (Tsai et al. 2024; Welbanks-Nixon 2025; Cooke & Madhusudhan 2024; not ingested) predict different inventories than these agnostic retrievals find. Coupling agnostic retrieval results to chemistry predictions is the next step.
- **Can multi-species combinations explain the MIRI features better than any single molecule?** This is one of the explicit "future work" lines in the paper.
- **Does cross-section data exist for these candidate molecules at low pressure?** Most do not — experimental laboratory work is required to firm up retrieved abundances.
- **At what S/N does DMS become spectroscopically unique?** [[2025_Luque_K2-18b]] estimate ~26 MIRI transits for 3σ feature detection; the uniqueness threshold (DMS vs diethyl sulfide vs methacrylonitrile) likely requires substantially more — beyond JWST in this M-dwarf habitable zone.

## Related

- [[2025_Madhusudhan_K2-18b-MIRI]] — the canonical 2-molecule retrieval that this work expands to 650 species. Same group; reproduces the 3σ DMS+DMDS preference but **does not validate uniqueness**.
- [[2025_Luque_K2-18b]] — uses C₂H₆ as the explicit alternative; both papers converge on the conclusion that DMS is one of many spectroscopically equivalent fits.
- [[2025_FernandezRodriguez_K2-18b]] — independent NIR-only reanalysis; retracts DMS in comprehensive retrievals (Bayes factor < 1). Methodologically aligned with Pica-Ciamarra in advocating broader molecular space.
- [[2025_Madhusudhan_subneptunes]] — review/perspective placing the broader hycean and sub-Neptune biosignature framework into context.
- [[2025_Schmidt_K2-18b]] — comprehensive NIRISS+NIRSpec reanalysis with ensemble posterior across 60 data combinations; converges on the same conclusion through a different lens (data-level marginalization rather than molecular-space broadening).
- [[2025_Taylor_K2-18b-MIRI]] — model-agnostic Gaussian-feature critique of the MIRI/LRS spectrum.
- Welbanks, Nixon et al. 2025 (not ingested) — additional independent critique.
- [[2025_Felix_TOI-270d]] — comparator: independent reanalysis of a sub-Neptune sulfur claim using a different retrieval framework; SO₂ on TOI-270 d retracted.
