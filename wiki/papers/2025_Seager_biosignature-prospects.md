---
type: paper
bibkey: 2025_Seager_biosignature-prospects
authors: [Seager, S., Welbanks, L., Ellerbroek, L., Bains, W., Petkowski, J. J.]
year: 2025
venue: PNAS
arxiv: ""
doi: 10.1073/pnas.2416188122
targets: [K2-18b, WASP-39b, WASP-107b, TOI-270d]
instruments: [JWST-NIRSpec, JWST-NIRISS, JWST-MIRI, JWST-NIRCam]
methods: [transmission-spectroscopy, atmospheric-retrievals]
species_detected: []
tags: [perspective, biosignatures, habitable-zone, sub-neptune, m-dwarf-host, jwst-noise-floor]
ingested: 2026-05-22
---

# Prospects for detecting signs of life on exoplanets in the JWST era

**Authors:** Seager, Welbanks, Ellerbroek, Bains, Petkowski (2025, PNAS 122:39, e2416188122) · DOI: 10.1073/pnas.2416188122 · **Perspective**

## TL;DR

A perspective on JWST's potential to detect exoplanet biosignature gases. Sets the **enabling photometric precision** (~30 ppm assumed noise floor, derived from the WASP-39 b ERS demonstration of ~50 ppm per single transit) and uses the 3-scale-height transmission-signal estimator TS ≈ 6HR_p/R_★² to bound the accessible target population: an Earth-twin around a Sun-like star is unreachable (TS ~ 1 ppm), only a handful of Earth-sized planets in habitable zones (some [[TRAPPIST-1]] planets, LP 791-18 d) survive the cut, and as many as ~6 sub-Neptunes (1.5–3 R⊕, T_eq < 373 K) qualify. The paper then formalises a **3 Key Criteria framework — Detection, Attribution, Interpretation** — and applies it to the [[K2-18b]] DMS tentative claim of Madhusudhan 2023, concluding the DMS claim **fails all three criteria**. Surveys [[WASP-107b]] (Welbanks 2024 CH₄) as a "Key-Criteria-satisfying" but biosignature-irrelevant counter-example, and [[TOI-270d]] (Holmberg 2024 vs Benneke 2024) as a cautionary tale where independent reductions of the same JWST pixels yield conflicting planet archetypes. Concludes that **JWST may never definitively claim a biosignature gas**; future progress requires solving M-dwarf stellar contamination, refining retrievals, building a "Deep Planet Simulator" for false-positive ruling, and ultimately next-generation telescopes (Habitable Worlds Observatory, LIFE, Starshade).

## Key findings

- **Adopted JWST noise floor: 30 ppm** (empirical estimate, derived from WASP-39 b ERS single-transit ~50 ppm performance under [[JWST-ERS-1366]]; to be refined as multi-transit stacked data accumulate).
- **TS ≈ 6HR_p/R_★² feasibility metric** (3 scale heights × planet annulus / stellar area) cleanly explains why M-dwarf hosts gain 4–100× signal vs Sun-sized hosts.
- **Habitable-zone target inventory under TS feasibility** (Cycles 1–3 TrExoLiSTS): only ~few Earth-size planets ([[TRAPPIST-1]] members, LP 791-18 d); ≤6 sub-Neptunes (1.5–3 R⊕, T_eq < 373 K). Most temperate sub-Neptunes are *too hot* for surface liquid water due to H₂-greenhouse + collision-induced absorption.
- **Three Key Criteria for biosignature claims**:
  1. **Detection** — Is the signal robust above noise?
  2. **Attribution** — Are spectral features correctly assigned to the right gas?
  3. **Interpretation** — Are derived planetary properties (abundance, false positives, plausible production rate) sound?
- **K2-18 b DMS claim assessed against the 3 Key Criteria — fails all three**:
  - Detection: ~2.4σ tentative (model comparison between 11-species vs 10-species reference); statistically insignificant against a flat-line baseline; sensitive to instrumental offset between NIRISS+NIRSpec.
  - Attribution: other sulfur gases share spectral features ([[2025_PicaCiamarra_K2-18b]]); echoes earlier H₂O→CH₄ confusion ([[2025_FernandezRodriguez_K2-18b]]).
  - Interpretation: requires ~20× modern-Earth DMS biological flux to overcome photochemical destruction ([[Photochem]] simulations); false-positive abiotic pathways remain unaddressed.
- **WASP-107 b is presented as the criteria-satisfying counter-example**: high SNR ([[JWST-NIRCam]] + [[JWST-NIRSpec]] CH₄), independent pipelines agreeing on detection + attribution, and a robust interpretation (chemical disequilibrium driven by tidal heating + photochemistry). Not itself a biosignature target (too hot, H₂-He envelope), but the template for what a robust JWST candidate would look like.
- **TOI-270 d cautionary tale**: same JWST pixels processed by Benneke 2024 vs Holmberg 2024 give CH₄+H₂O at consistent identifications but **inconsistent planetary archetype** (water-world hot-ocean vs metal-rich H₂/H₂O/CH₄ mixed atmosphere) — challenges in Step 4 (interpretation) cascade from Step 2 (data reduction) and Step 3 (retrieval).
- **Biosignature gas list (Table 1)**: O₂, CH₄, N₂O, CH₃Cl, CH₃Br, CH₃OH, CH₃SH, [[DMS]], PH₃, [[NH3]], isoprene, carbonyls, HCN, NO₂, SF₆, NF₃, CFCs, PFCs; **none satisfy all criteria simultaneously** (distinct spectral features + plausible production rate + no significant false positives).
- **CH₄ is championed for rocky-planet biosignatures on planets without H₂-dominated envelopes** — pre-Cambrian Earth analog; difficult to produce abiotically for oxidized mantles ([[Photochem]] / Wogan et al. 2024 not ingested; Thompson 2022 not ingested).
- **Recommended path forward**: (i) solve M-dwarf [[stellar-contamination]]; (ii) discover longer-period, colder sub-Neptunes; (iii) refine atmospheric retrievals; (iv) expand the biosignature gas list with context-gas requirements; (v) build a "Deep Planet Simulator" coupling interior + atmosphere + photochemistry over Gyr timescales; (vi) move to next-generation observatories (Habitable Worlds Observatory, LIFE, Starshade, Solar Gravitational Lens, Starshot).

## Methods

- **Pure perspective paper** — no new observations or retrievals. Synthesises the WASP-39 b ERS noise-floor measurements, the K2-18 b biosignature debate, the WASP-107 b chemical-disequilibrium analysis, and the TOI-270 d interpretation discrepancy into a unifying framework.
- **TS ≈ 6HR_p/R_★² feasibility heuristic** — three-scale-height transmission signal estimator, applied against the TrExoLiSTS catalog (Cycles 1–3) to count habitable-zone targets.
- **Three Key Criteria** — formal taxonomy of biosignature-claim sources of error: Detection, Attribution, Interpretation. Conceptually positions atmospheric inference as a 4-step pipeline (Observations → Spectrum → Models → Interpretation) with subjective choices at each step.

## Caveats & limitations

- **Pessimistic framing**: the paper explicitly leaves open the possibility that JWST *will* identify "biosignature gas candidates" but argues it may not be able to *definitively claim* one. The cosmic-shoreline-challenger cases ([[TOI-561b]], [[L98-59b]]) and the volcanic-atmosphere inference are not discussed.
- **Noise-floor estimate is not empirically demonstrated** for multi-transit M-dwarf hosts where stellar variability stacks unfavorably — 30 ppm may be optimistic in the TRAPPIST-1 regime.
- **Table 1 biosignature gas evaluation is qualitative** (✓ / (✓) / X marks) and acknowledged as subjective; many entries depend on the assumed planetary context.
- **The "Deep Planet Simulator" call** acknowledges that even with detailed coupled models, the parameter space is poorly constrained by remote sensing of spatially averaged exoplanet spectra — the analogue with Illustris-style galaxy simulations breaks at the validation step.

## Open questions / follow-ups

- **Can the 3 Key Criteria framework be made quantitative**, e.g., a Bayes-factor threshold for each criterion that propagates uniformly across published biosignature claims?
- **Does the cosmic-shoreline-challenger pattern** (atmospheres on planets that "shouldn't" have them: [[TOI-270b]], [[TOI-561b]], [[HD3167b]], [[L98-59b]]) recalibrate the perspective's pessimism about habitable-zone target availability?
- **For M-dwarf rocky planets**, can [[stellar-contamination]] be reduced enough that the 30 ppm noise floor is actually reached on temperate worlds — or is the [[2018_Rackham_TLS]] M-dwarf TLS contamination an irreducible barrier for the very targets most accessible to JWST?
- **Beyond JWST**: would a fluorine-based technosignature gas detection (SF₆, NF₃, CFCs, PFCs) bypass false-positive concerns, given the lack of natural high-temperature fluorine chemistry?

## Related

- [[2025_Madhusudhan_K2-18b-MIRI]] — the DMS biosignature claim assessed against the 3 Key Criteria framework; explicitly named in §3.3 as failing all three criteria. Cited via Madhusudhan et al. 2023 (not ingested) for the original tentative NIR detection.
- [[2025_FernandezRodriguez_K2-18b]], [[2025_Luque_K2-18b]], [[2025_PicaCiamarra_K2-18b]], [[2025_Schmidt_K2-18b]], [[2025_Taylor_K2-18b-MIRI]] — five independent retractions or critiques of the K2-18 b DMS claim that converge with this perspective's pessimistic assessment.
- [[2025_Murphy_WASP107b]] — Welbanks 2024 / Sing 2024 (not ingested) WASP-107 b panchromatic analysis cited as the criteria-satisfying case study. Murphy 2025 (limb-resolved) reinforces the same conclusion (chemical disequilibrium real).
- [[2025_Coulombe_TOI-270b]], [[2025_Felix_TOI-270d]] — TOI-270 system characterizations; Felix 2025 explicitly addresses the Holmberg-vs-Benneke interpretation discrepancy that Seager 2025 cites as a cautionary tale.
- [[2025_Madhusudhan_subneptunes]] — the [[sub-neptune-classification]] perspective from the Madhusudhan group; Seager 2025 is the parallel pessimistic perspective from the MIT / ASU groups.
- [[2025_Crossfield_SO2shoreline]] — the theoretical SO₂-shoreline framework; conceptually parallel to the criteria framework but for non-biosignature inference.
