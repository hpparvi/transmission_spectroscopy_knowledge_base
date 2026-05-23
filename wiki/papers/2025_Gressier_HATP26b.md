---
type: paper
bibkey: 2025_Gressier_HATP26b
authors: [Gressier, A., Batalha, N. E., Wogan, N., Alderson, L., Doud, D., Espinoza, N., MacDonald, R. J., Wakeford, H. R., Valenti, J. A., Lewis, N. K., Seager, S., Stevenson, K. B., Allen, N. H., Cañas, C. I., Challener, R. C., Glidden, A., Huang, J., Lin, Z., Louie, D. R., Maguire, C., Mullens, E., Sotzen, K., Valentine, D., Clampin, M., Pueyo, L., van der Marel, R. P., Mountain, C. M.]
year: 2025
venue: AJ
arxiv: 2510.21055
doi: 10.3847/1538-3881/ae0929
targets: [HAT-P-26b]
instruments: [JWST-NIRSpec]
methods: [transmission-spectroscopy, atmospheric-retrievals, stellar-contamination-modeling]
species_detected: [SO2, CO2, H2O]
species_tentative: [H2S]
species_ruled_out: [CO, NH3, C2H2, C2H4, HCN]
codes: [transitspectroscopy, ExoTiC-JEDI, TauREX3, POSEIDON, PICASO, Photochem, MultiNest, juliet]
tags: [hot-neptune, neptune-mass, sulfur-chemistry, jwst-tst-gto, photochemistry-detection]
ingested: 2026-05-03
---

# JWST-TST DREAMS: Sulfur Dioxide in the Atmosphere of the Neptune-mass Planet HAT-P-26 b from NIRSpec G395H Transmission Spectroscopy

**Authors:** Gressier, Batalha, Wogan, Alderson et al. (2025, AJ 170:292) · [arXiv:2510.21055]
**Targets:** [[HAT-P-26b]] · **Instrument:** [[JWST-NIRSpec]] G395H · **Program:** [[JWST-TST-GTO-1312]] (PI: N. Lewis)

## TL;DR

A single JWST NIRSpec G395H transit of the warm Neptune-mass planet HAT-P-26 b (M = 18.6 M⊕, R = 6.33 R⊕, T_eq ≈ 1000 K) yields a high-significance detection of [[SO2]] (lnB = 13.46), with strong [[CO2]] (lnB = 85.64) and moderate [[H2O]] (lnB = 4.06). The SO₂ detection is the first in a true Neptune-mass planet, **bridging the previous SO₂ detections in hot Jupiters and the sub-Neptune GJ 3470 b** and demonstrating that disequilibrium photochemistry is active across a much wider temperature range than previously expected (down to ~1000 K). The retrieved metallicity is ~10× solar with subsolar C/O ≈ 0.14. Population-level analysis of 11 JWST giant-planet transmission spectra confirms the Crossfield (2023) prediction that SO₂ abundance correlates with atmospheric metallicity — steep rise at low [M/H], gradual increase above ~30× solar.

## Key findings

- **SO₂ detection (lnB = 13.46, ≥5σ):** log X(SO₂) ≈ −4.40 from the [[POSEIDON]]_TLS free retrieval; absorption feature centered at 4.05 μm clearly visible in both [[transitspectroscopy]] and [[ExoTiC-JEDI]] reductions. First SO₂ in the Neptune-mass regime; previously detected only in hot Jupiters ([[WASP-39b]], WASP-107 b, HD 189733 b — not all yet ingested) and the sub-Neptune GJ 3470 b (Beatty et al. 2024; not yet ingested).
- **CO₂ detection (lnB = 85.64, ≫5σ):** log X(CO₂) ≈ −2.91; strong 4.3 μm feature spanning both NRS1 and NRS2.
- **H₂O detection (lnB = 4.06, ~3σ):** log X(H₂O) ≈ −2.07; lower-significance owing to degeneracy with stellar contamination at the short-wavelength end of NRS1.
- **H₂S tentative (~2σ):** log X(H₂S) posterior peaks near −3.5 with a 3σ upper limit of −2.67; sensitive to NRS1/NRS2 detector-offset modeling.
- **CO ruled out:** 3σ upper limit log X(CO) < −5.33.
- **Atmospheric metallicity:** [M/H] = 11.4⁺¹³.³₋₈.¹ × solar from O/H + C/H + S/H + N/H summed in solar units; consistent with Wakeford et al. 2017 HST estimate (4.8⁺²¹.⁵₋₄.₀ × solar) and the MacDonald & Madhusudhan 2019 reanalysis (18.1⁺²⁵.⁹₋₁₁.₃ × solar).
- **C/O ratio:** **subsolar at 0.14⁺⁰.²¹₋₀.₀₈**; compared with stellar C/O = 0.41 ± 0.1 (Polanski et al. 2022) or 0.89 ± 0.15 (Kolecki & Wang 2022), pointing to volatile-rich envelope accretion.
- **PICASO grid retrieval:** self-consistent radiative-convective + chemistry grid with clouds + SO₂ added prefers [M/H] = 10× solar, C/O = 0.4, heat redistribution = 0.4, T_int = 299 K. Adding SO₂ to the grid is **strongly preferred** (Δln Z = 18 vs. cloud-only).
- **Photochemistry validation:** [[Photochem]] (Wogan 2024) modeling on the PICASO best fit predicts peak SO₂ VMR ≈ 2 × 10⁻⁵ at 10⁻⁴ bar — within ~1σ of the retrieved value. Production via H₂S + 2 H₂O → SO₂ + 3 H₂, driven by H from water photolysis (S.-M. Tsai et al. 2023 mechanism extended to T ≈ 700 K).
- **Population-level SO₂–[M/H] correlation:** TauREx reanalysis of 11 JWST transmission spectra (HAT-P-26 b + GJ 1214 b, GJ 3470 b, HD 189733 b, HD 209458 b, HIP 67522 b, WASP-39 b, WASP-80 b, WASP-107 b, WASP-121 b, WASP-127 b) shows SO₂ VMR scales steeply with metallicity for [M/H] ≲ 30× solar and more gradually above. Most planets follow within 3σ; **WASP-107 b is a 7σ outlier** (lower SO₂ than predicted at 40× solar).
- **Stellar-contamination check:** POSEIDON_TLS retrieval (T_het, f_het free) yields ln Z = 459.41 vs. 459.13 without TLS — Bayes factor < 1; **no statistical preference for stellar contamination** despite K-dwarf host. f_het = 0.26 (unconstrained); detector-offset retrieval gives Δ_NRS2 = −114 ± 35 ppm (consistent with TLS-free retrieval).
- **Cool isothermal T–P:** retrieved T_atm = 667⁺⁶⁴₋₅₈ K — significantly **cooler than T_eq ≈ 1000 K**; possibly indicates asymmetric limb conditions or terminator-cloud condensation; [[2025_Madhusudhan_subneptunes]] (in prep, then) and forthcoming SOSS analysis (R. J. MacDonald et al. 2025, in prep) expected to refine.
- **Cloud constraints:** opaque cloud top at ~10⁻² bar required to mute spectral features and match the observed amplitude.

## Methods

Single 7 hr 56 min JWST NIRSpec G395H BOTS observation under [[JWST-TST-GTO-1312]] on 2023 June 15 (~2 hr 30 min in transit; SUB2048 subarray, 48-group NRSRAPID). Two independent reductions with [[transitspectroscopy]] (Espinoza 2022) and [[ExoTiC-JEDI]] (Alderson et al. 2022); both fitted with [[juliet]] (Espinoza 2019; batman + GP). Spectra agree at 1σ. Atmospheric inference combines:

- **Free-chemistry retrievals:** [[TauREX3]] (R = 100; molecular line lists from ExoMol + HITEMP + HITRAN), [[POSEIDON]] (with and without TLS module; isothermal and Madhusudhan & Seager 2009 T–P).
- **Self-consistent forward grid:** [[PICASO]] (576 models; T_int 200/300/400 K × heat redistribution × [M/H] 0–2 × C/O 0.25/0.5/1.5×) with optional SO₂ as a fifth grid parameter and a gray-cloud scaling factor.
- **Photochemistry:** [[Photochem]] v0.6.5 — full 1D continuity + diffusion model, ~600 reactions, ~100 species (H/He/C/O/N/S only — chlorine removed). UV input from MUSCLES HAT-P-26 spectrum.
- **Population-level analysis:** TauREx reanalysis of 10 archival JWST giant-planet transmission spectra (sample from Fu et al. 2025) plus this work, all under uniform retrieval setup.

Stellar-contamination handling: TLS retrieval (T_het, f_het) interpolating PHOENIX (Allard et al. 2012) via pysynphot; not preferred by the data (Bayes factor < 1).

## Caveats & limitations

- **Single visit.** The H₂O detection is statistically modest (lnB = 4.06); confirmation depends on the forthcoming NIRISS/SOSS analysis (R. J. MacDonald & DREAMS 2025, in prep) and the multi-instrument synthesis (L. Alderson & DREAMS 2025, in prep).
- **H₂S tentative only.** The 2.8–3.1 μm H₂S band overlaps the H₂O band and falls in the NRS1/NRS2 detector gap region; instrument-offset modeling materially affects the posterior.
- **Cool retrieved T–P (~700 K vs T_eq ~1000 K).** Authors flag this as possibly reflecting asymmetric limb conditions, condensation on the day side, or oversimplified isothermal assumption; not a fundamental tension but limits formal C/O precision.
- **Sub-solar C/O depends on full molecular inventory.** With CO ruled out at 3σ but no firm CH₄/CO detection, the C/O budget is dominated by CO₂ — an unusual configuration that makes the C/O determination model-sensitive (per Lodders 2010 formula).
- **SO₂–[M/H] population trend uses heterogeneous retrievals.** Even with TauREx-uniform reanalysis, planet-by-planet differences in cloud / T–P parameterizations and absent species could shift abundances by ≳ 1 dex (cf. [[2026_RoyPerez_WASP39b]] on WASP-39 b alone).
- **WASP-107 b 7σ outlier.** Authors note this constraint comes from a single G395H reanalysis (Sing et al. 2024); a combined retrieval including NIRCam (Welbanks et al. 2024) and MIRI (Dyrek et al. 2023) is needed to resolve.

## Open questions / follow-ups

- **Does the upcoming NIRISS/SOSS spectrum confirm H₂O at higher significance and tighten C/O?** R. J. MacDonald et al. 2025 (in prep) is expected to provide the tightest H₂O constraint and the first joint optical-NIR retrieval.
- **Will the full panchromatic MIRI/LRS + NIRSpec + SOSS analysis (L. Alderson et al. 2025, in prep) confirm the 700 K cool retrieval temperature?** A multi-wavelength T–P retrieval at MIRI's longer baseline will test the asymmetric-limb interpretation.
- **Is HAT-P-26 b's sub-solar C/O = 0.14 consistent with pebble accretion at 3–10 au?** Authors invoke this formation pathway via Turrini et al. 2021 framework but emphasize that current uncertainties are too large to discriminate from planetesimal accretion.
- **What populates the SO₂–[M/H] correlation between Neptune-mass and sub-Saturn?** With HAT-P-26 b filling the sparse Neptune regime, the next-most-needed targets are warm sub-Saturns (M ≈ 30–60 M⊕) at intermediate metallicity.
- **Why is WASP-107 b 7σ low?** Possibly cooler-than-expected upper atmosphere, cloud cover at altitudes where photochemistry is otherwise active, or MIRI/NIRCam-derived metallicity vs. SO₂ disconnect. A combined Bayesian retrieval is the required next step.

## Related

- [[2026_Radica_WASP96b]] — second JWST tentative SO₂ candidate (lnB = 2.69) on the [[SO2-photochemical-shoreline]]; HAT-P-26 b joins WASP-96 b as a confirmed (vs. tentative) shoreline-population member.
- [[2025_LustigYaeger_WASP17b]] — tentative SO₂ on a hot-Jupiter **nightside** via iESR-PIE; complementary day-night photochemistry.
- [[2026_RoyPerez_WASP39b]] — pipeline-systematics study on the WASP-39 b ERS PRISM dataset; key counter-example to the assumption that SO₂ abundances are pipeline-stable.
- [[2024_Gressier_L98-59d]], [[2024_Banerjee_L98-59d]] — tentative SO₂ on a rocky M-dwarf planet (volcanic, not photochemical, origin proposed).
- Beatty et al. 2024 (GJ 3470 b sub-Neptune SO₂; not yet ingested) — the sub-Neptune anchor of the SO₂ shoreline that Gressier 2025 explicitly bridges to the Neptune regime.
