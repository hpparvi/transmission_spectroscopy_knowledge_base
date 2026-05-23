---
type: paper
bibkey: 2025_Ahrer_WASP94Ab
authors: [Ahrer, E.-M., Gandhi, S., Alderson, L., Kirk, J., Teske, J., Booth, R. A., McDonald, C. H., Christie, D. A., Claringbold, A. B., Nealon, R., Panwar, V., Veras, D., Wakeford, H. R., Wheatley, P. J., Zamyatina, M.]
year: 2025
venue: MNRAS
arxiv: 2505.11224
targets: [WASP-94Ab]
instruments: [JWST-NIRSpec]
methods: [transmission-spectroscopy, atmospheric-retrievals]
species_detected: [H2O, CO2, CO]
species_tentative: [H2S]
codes: [Eureka, Tiberius, ExoTiC-JEDI, petitRADTRANS, HyDRo, MultiNest]
tags: [hot-jupiter, misaligned, retrograde, f-dwarf-host, formation-tracer, c-o-ratio, kraft-break, jwst-go-3154]
ingested: 2026-05-06
---

# Tracing the Formation and Migration History: Molecular Signatures in the Atmosphere of Misaligned Hot Jupiter WASP-94 Ab Using JWST NIRSpec/G395H

**Authors:** Ahrer, Gandhi, Alderson, Kirk, Teske, Booth et al. (2025, MNRAS, accepted) · arXiv:2505.11224
**Target:** [[WASP-94Ab]] · **Host:** [[WASP-94A]] · **Instrument:** [[JWST-NIRSpec]] (G395H, 2.8–5.1 μm)
**Program:** [[JWST-GO-3154]]

## TL;DR

JWST NIRSpec/G395H transmission spectrum of the inflated retrograde-misaligned hot Jupiter [[WASP-94Ab]] (M = 0.45 MJ, R = 1.58 RJ, T_eq = 1508 K, λ = −123°). Cloud-free atmosphere; detects [[H2O]] at 4σ and [[CO2]] at 11σ, with tentative [[CO]] (~3σ) and [[H2S]] (~2.5σ). Equilibrium-chemistry [[atmospheric-retrievals]] yield C/O = 0.49⁺⁰·⁰⁸⁻⁰·¹³ — **substellar** vs. host C/O★ = 0.68 ± 0.10 — and metallicity Z = 2.17 ± 0.65 × solar, **stellar-like** (Z★ = 2.09 × solar). Combined with WASP-94 A sitting **above the Kraft break** (so the retrograde orbit is primordial), this composition pattern is best explained by **pebble accretion or planetesimal accretion combined with large-distance migration** — disfavoring local accretion of inner-disc gas. Methodologically reinforces the use of host-star reference values rather than solar normalizations for hot-Jupiter formation tracers.

## Key findings

- **CO₂ at 11σ** (Δ ln Z = 59 in HyDRo; lower bound after retrieval normalization). log VMR ≈ −4.25.
- **H₂O at 4σ** (4.0σ HyDRA, 4.1σ pRT); log VMR ≈ −1.60. Lower-bound conservative estimate; Δ ln Z dominated by retrieval setup.
- **Tentative CO at ~3σ** (2.8σ HyDRA, 3.3σ pRT); log VMR ≈ −2.85.
- **Tentative H₂S at ~2.5σ** (2.9σ HyDRA, 2.1σ pRT); log VMR ≈ −3.31 to −3.59 — adds WASP-94 Ab to the small set of hot Jupiters with hints of sulfur (cf. Fu et al. 2024 on WASP-39 b).
- **CH₄, NH₃, HCN, C₂H₂ all upper-limited** (log VMR < −5.0 to −6.5).
- **C/O = 0.49⁺⁰·⁰⁸⁻⁰·¹³** (equilibrium chemistry on Eureka R=400 fiducial); robustly **substellar** (planetary 0.72 ± 0.17 × stellar) — across all reductions and resolutions.
- **Metallicity Z ≈ 2× solar** (1.5–2.4 × solar across reductions/resolutions; fiducial 2.17 ± 0.65 × solar) — **stellar-like** (1.04 ± 0.33 × M/H_★).
- **Cloud-free** (cloud deck pushed to high pressures); cloudy retrievals not preferred.
- Equilibrium chemistry preferred over free chemistry (Δ ln Z = 1.6–4.4 across reductions/resolutions).

## Methods

- **Reductions**: [[Eureka]] (fiducial), [[Tiberius]], [[ExoTiC-JEDI]] — three independent pipelines.
- **Spectral resolutions**: R = 100 and R = 400 binning.
- **Free-chemistry retrievals**: [[HyDRo]] and [[petitRADTRANS]] (pRT) — independent codes; species H₂O, CO, CO₂, CH₄, HCN, NH₃, H₂S, C₂H₂.
- **Equilibrium-chemistry retrieval**: pRT with C/O and [Fe/H] as free parameters.
- **Detector offset**: NRS1–NRS2 offset retrieved as a free parameter (now common practice).
- **Stellar abundance reference**: re-uses Teske et al. (2016) WASP-94 A oxygen and carbon abundances (synthesis fitting + new equivalent-width fitting on O I, C I, CH lines) — yields C/O★ = 0.68 ± 0.10, Z★ = 2.09 × solar.

## Caveats & limitations

- **Spectral coverage limited to 2.8–5.1 μm** — H₂O detection significance is sensitive to the choice of retrieval setup; the conservative 4.1σ figure assumes joint-fit detector offset.
- **Free chemistry vs equilibrium tension**: free retrievals consistently return *lower* C/O and *higher* metallicity than equilibrium retrievals — attributable to CH₄/HCN/CO blending with H₂O bands at G395H resolution and cloud-deck differences (greyer cloud in equilibrium).
- **CO and H₂S detections are below the 3σ canonical threshold**; refining requires longer wavelength baselines (NIRISS or NIRCam) or additional visits.
- **Formation-history inference depends on disc-chemistry assumptions** (Penzlin et al. 2024) — the substellar-C/O signature is consistent with multiple migration scenarios; the host-star Kraft break placement is what discriminates.

## Open questions / follow-ups

- **Sample expansion above the Kraft break**: GO 3154 is part of a planned larger study to characterize misaligned vs aligned hot-Jupiter atmospheres above the Kraft break, testing the Penzlin et al. 2024 prediction that disc-driven (aligned) and high-eccentricity (misaligned) migration leave distinct C/O signatures — possibly reversed if silicate evaporation occurs.
- **NIRISS/SOSS or NIRCam follow-up** to nail down H₂O significance and access shorter-wavelength CO + H₂S diagnostics.
- **Confirm CO + H₂S** via panchromatic data — currently both at ~3σ.
- **Stellar abundance pipeline**: the substellar-C/O conclusion rests on accurate (C/O)★ = 0.68 ± 0.10; differential analysis vs WASP-94 B (Teske 2016) lends robustness, but other systems may not have such reference companions.

## Related

- [[2025_Fu_limb-asymmetry]] — same target; reports the **strongest morning–evening limb-asymmetry signal** in the JWST NIRISS sample using a separate NIRISS dataset; the present study uses NIRSpec/G395H so the asymmetry decomposition here is not attempted.
- [[2025_Ahrer_KELT7b]] — same lead author; aligned hot Jupiter as a comparison point for the misaligned/aligned C/O test.
- [[2025_Gressier_WASP17b]], [[2025_Murphy_WASP107b]] — comparable G395H+ sulfur-species work on hot Jupiters.
