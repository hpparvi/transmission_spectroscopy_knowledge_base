---
type: code
aliases: [POSEIDON retrieval code]
tags: [retrieval-code, bayesian, transmission, hub]
---

# POSEIDON

An open-source [[atmospheric-retrievals]] code (MacDonald & Madhusudhan 2017; MacDonald 2023; not yet ingested) for exoplanet transmission and emission spectra. Supports free-chemistry and chemical-equilibrium compositions, parametric T–P profiles (isothermal, Madhusudhan & Seager 2009, gradient-based), cloud/haze parameterizations, and joint atmosphere + [[stellar-contamination]] retrievals (Pinhas et al. 2018 TLSE parameterization). Typically paired with PyMultiNest / [[MultiNest]] for sampling; v1.2 introduced extended emission and TLSE features used in 2025–2026 wiki papers. The single most-used retrieval framework in the wiki on small-planet G395H data, and increasingly the cross-check standard for hot-Jupiter / sub-Saturn free-chemistry retrievals.

## Variants

The wiki sees POSEIDON deployed in five recurring configurations:

- **Free-chemistry transmission, atmosphere-only.** [[2025_Gressier_WASP17b]] (cross-check alongside primary [[TauREX3]] on WASP-17 b NIRISS dayside, two T–P parameterizations); one of four free-chemistry frameworks in [[2026_Radica_WASP96b]] on WASP-96 b (alongside [[PyratBay]], [[NEMESISPY]], [[Aurora]]).
- **Free-chemistry, joint atmosphere + stellar-contamination.** [[2023_May_GJ1132b]] (15-parameter atmospheric model + 2000 PyMultiNest live points; atmosphere and unocculted-starspot retrievals run as alternatives with equal Bayesian evidence); [[2023_Moran_GJ486b]] (6-gas free-chemistry + alternative stellar-contamination retrieval; both scenarios fit at χ²ν ≈ 1.0).
- **Joint stellar + atmosphere simultaneous retrieval.** [[2023_Lim_TRAPPIST1b]] (NIRISS/SOSS spectra; H₂ abundance < 52% at 3σ from joint fit).
- **Free-chemistry transmission + emission via iESR-PIE.** [[2025_LustigYaeger_WASP17b]] uses POSEIDON v1.2 on WASP-17 b dayside + nightside iESR-PIE-extracted spectra simultaneously; tentative SO₂, CH₄, H₂O, CO₂ on the nightside.
- **Free-chemistry + chemical-equilibrium under TLS framework.** [[2026_Ashtari_HATS75b]] uses POSEIDON in both modes as the primary retrieval engine for HATS-75 b NIRSpec PRISM, jointly fit with photospheric heterogeneity (spots + faculae).

## Trade-offs

- **Strength: joint stellar+atmosphere natively.** The Pinhas 2018 TLSE parameterization is built in; competing codes typically need bolt-on extensions. This makes POSEIDON the path of least resistance on M-dwarf rocky planets where contamination retrievals are mandatory.
- **Strength: cross-code reproducibility.** The four-framework agreement on WASP-96 b ([[2026_Radica_WASP96b]]) and POSEIDON+TauREx convergence on WASP-17 b dayside ([[2025_Gressier_WASP17b]]) suggest the code's Bayesian evidence values are well-calibrated against peers for high-significance detections.
- **Limitation: degeneracy at low SNR.** On marginal small-planet spectra ([[2023_Moran_GJ486b]], [[2023_May_GJ1132b]]) atmosphere and starspot scenarios return statistically indistinguishable evidence — the code surfaces the degeneracy honestly but cannot resolve it without independent emission constraints (cf. [[2024_WeinerMansfield_GJ486b]]).
- **Limitation: forward-model assumptions on hot Jupiters.** The four-framework cross-check on WASP-96 b ([[2026_Radica_WASP96b]]) finds broad agreement on detected species but residual scatter on derived metallicity / C/O — POSEIDON shares the field's general "framework dependence" issue.

## Open issues

- **TLSE parameterization beyond two-component spots/faculae.** Recent ultracool-dwarf work ([[2025_Rathcke_TRAPPIST1bc]]) suggests well-mixed photosphere geometries dominate over fully-unocculted-spot configurations; POSEIDON's stellar-contamination module still bakes in the latter assumption.
- **Information-content extensions.** ARCiS-style per-instrument Δln Z analysis ([[2026_Heinke_HATP12b]]) is not yet a standard POSEIDON workflow; would generalize naturally to the panchromatic targets where the code already runs.

## Papers

### Hot Jupiter / sub-Saturn / Neptune / GEMS — primary or co-primary retrieval engine
- [[2025_Gressier_HATP26b]] — primary retrieval engine on HAT-P-26 b NIRSpec G395H; deployed in four configurations (POSEIDON, POSEIDON_TLS, POSEIDON_offset, POSEIDON_TP); SO₂ at lnB = 13.46; TLS retrieval finds Bayes factor < 1 — no preference for stellar contamination on this K-dwarf host.
- [[2025_Ahrer_KELT7b]] — POSEIDON free-chemistry + equilibrium-chemistry retrievals on KELT-7 b NIRSpec G395H; high-temperature species set (SiO, VO, TiO, AlO, SH) tested but ruled out as physically unrealistic; cloud-deck and low-metallicity scenarios both viable.
- [[2026_Ashtari_HATS75b]] — primary engine; free-chemistry + chemical-equilibrium under TLS framework.
- [[2025_LustigYaeger_WASP17b]] — POSEIDON v1.2 on iESR-PIE WASP-17 b dayside + nightside.
- [[2026_Radica_WASP96b]] — one of four free-chemistry frameworks cross-compared on WASP-96 b.
- [[2025_Gressier_WASP17b]] — cross-check alongside primary TauREX3 on WASP-17 b NIRISS dayside.

### Rocky M-dwarf planets — joint stellar+atmosphere retrievals
- [[2023_Lim_TRAPPIST1b]] — simultaneous stellar+atmosphere joint retrieval; H₂ < 52% at 3σ.
- [[2023_Moran_GJ486b]] — 6-gas free-chemistry + alternative starspot retrieval; equal evidence (later resolved by emission).
- [[2023_May_GJ1132b]] — atmosphere vs unocculted-starspot retrievals; equal Bayesian evidence on Visit 1.
- [[2025_Verma_HD209458b]] — benchmark reference for [[SANSAR]]; opacity-sampling forward-model agreement at ~6 ppm absolute mean offset; retrieval cross-comparison on WASP-96 b NIRISS data agrees within 1σ.
- [[2025_Deka_WASP39b]] — benchmark reference for [[NEXOTRANS]] on the WASP-39 b MIRI dataset; corner-plot overlay agreement within 1σ across log(H₂O), log(SO₂), and cloud parameters; same as in [[2026_Radica_WASP96b]].
