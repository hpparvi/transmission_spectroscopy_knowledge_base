---
type: method
aliases: [transit light source effect, TLSE modeling, starspot retrieval]
tags: [stellar-heterogeneity, m-dwarf, degeneracy, hub]
---

# Stellar contamination modeling

Forward or retrieval modeling of the transit light source effect ([[2018_Rackham_TLS]], [[2019_Rackham_TLS-FGK]]): unocculted photospheric heterogeneities (spots, faculae) imprint wavelength-dependent signatures on a [[transmission-spectrum]] that can mimic or mask atmospheric absorption. Typically parameterized by heterogeneity temperature(s), covering fraction(s), and a photosphere temperature; fit jointly with atmospheric parameters or compared via Bayesian model selection. The dominant computational mitigation strategy for [[stellar-contamination]] across M-dwarf planet papers in the wiki — complementary to empirical [[back-to-back-transit-correction]], GP marginalization (when stellar models fail), and [[flare-mitigation]] (for stochastic flare events).

## Variants

- **Joint atmosphere + TLSE retrieval (in-transit data).** Atmosphere-only and stellar-contamination-only models run as competing scenarios within a single Bayesian framework, or as additive components in a joint fit.
  - **Atmosphere vs starspot as alternatives:** [[2023_May_GJ1132b]], [[2023_Moran_GJ486b]] — both find equal Bayesian evidence; degeneracy unresolved without independent constraints.
  - **Combined stellar + atmosphere preferred:** [[2024_Banerjee_L98-59d]] — three-parameter contamination retrieval; "Stellar + Atmosphere" wins over "Stellar Only"; T_phot ≈ 3423 K, facula ~+324 K hotter.
  - **Combined preferred under TLS framework on a gas giant:** [[2026_Ashtari_HATS75b]] — first wiki application to a [[GEMS]]-class target; cool spots (T ≈ 3365 K, f ≈ 0.23) + warm faculae (T ≈ 3909 K, f ≈ 0.25) jointly retrieved with H_2/CH_4/CO/CO_2 atmosphere; TLS+atmosphere preferred over hazy clear-atmosphere given independent activity evidence.
  - **Stellar-only rejected, atmosphere preferred:** [[2024_Gressier_L98-59d]] — unocculted-spots/faculae model cannot reproduce the L 98-59 d spectrum; atmosphere required.
  - **Joint fit under TLSE-only (H₂ rejection):** [[2023_Lim_TRAPPIST1b]] — Visit 1 dominated by ~29% cool spots (~−197 K), Visit 2 by ~29% faculae (~+153 K); contamination amplitudes 750–1000 ppm peak-to-peak; joint stellar+atmosphere retrieval yields H₂ < 52% at 3σ.
- **Out-of-transit photospheric inversion (independent constraint).** Multi-component PHOENIX or [[SPHINX]] grid fits to the out-of-transit baseline yield independent photosphere parameters that constrain or contradict in-transit retrievals.
  - [[2023_Moran_GJ486b]] — 3-component (photosphere + spots + faculae) PHOENIX fit preferred by Δχ²ν ≈ 23, lending physical support to the in-transit starspot scenario.
  - [[2025_Bennett_GJ1132b]] — four-visit PHOENIX modeling; Visit 1 favors ~10% more cool-spot coverage than Visits 2–4; explains the Visit-1 transmission deviation reported in [[2023_May_GJ1132b]].
  - [[2025_Rathcke_TRAPPIST1bc]] — SPHINX 1- to 4-component fits via [[speclib]] to TRAPPIST-1 PRISM out-of-transit; 2-component prefers ~55.6% T₁ ≈ 2000 K + ~44.4% T₂ ≈ 2600 K; cool-component fraction varies ~0.1%/hr within a single visit.
- **GP marginalization over contamination.** Used when stellar models systematically fail. [[2025_Espinoza_TRAPPIST1e]] (PHOENIX models fail < 3 μm on TRAPPIST-1; GP enables atmospheric inference); [[2025_Glidden_TRAPPIST1e]] (GP correction from companion paper applied to all four visits).
- **Dedicated TLSE codes.** [[stctm]] ([[2025_PiauletGhorayeb_TRAPPIST1d]] — exotune sub-framework); [[fleck]] (forward-modeling on rotating stars; [[2026_Ashtari_HATS75b]]). [[POSEIDON]] embeds a Pinhas 2018 TLSE parameterization natively.
- **Activity-driven null tests.** [[2025_Taylor_GJ357b]] runs PHOENIX-grid 3- and 5-component setups on the GJ 357 b NIRISS/SOSS spectrum; all four TLS parameterizations yield Bayes factors below the flat-line model — consistent with GJ 357's exceptional inactivity (log R'HK = 5.53). A clean negative case.

## Trade-offs

- **Stellar-model fidelity floor.** PHOENIX and SPHINX hit grid-floor temperatures (~2000 K) and saturated-line wing limits below the ~1800 ppm/pixel residual seen in TRAPPIST-1; precision-bottlenecked retrievals are model-bottlenecked instead. [[2025_Glidden_TRAPPIST1e]] documents this explicitly: stellar-model uncertainty ~1800 ppm/pixel exceeds observational precision ~89 ppm.
- **TLSE-only vs atmosphere-only as exclusive alternatives.** Standard early-Cycle-1 framing ([[2023_Moran_GJ486b]], [[2023_May_GJ1132b]]); produces equal-evidence degeneracies.
- **Joint additive TLSE + atmosphere.** Standard for higher-information data ([[2024_Banerjee_L98-59d]], [[2026_Ashtari_HATS75b]], [[2023_Lim_TRAPPIST1b]]); resolves degeneracy when at least one component is well-constrained.
- **Out-of-transit constraint as Bayesian prior.** [[2023_Moran_GJ486b]], [[2025_Bennett_GJ1132b]], [[2025_Rathcke_TRAPPIST1bc]] use this approach. Cleaner than in-transit alone but assumes the out-of-transit photosphere matches the chord — an assumption [[2025_Rathcke_TRAPPIST1bc]] now challenges with its well-mixed-photosphere finding (see [[stellar-contamination]] § Tensions).
- **GP over physically motivated stellar models.** Pragmatic when models fail; sacrifices physical interpretability.

## Open issues

- **Stellar-model fidelity for ultracool-dwarf hosts.** [[2025_Espinoza_TRAPPIST1e]] / [[2025_Glidden_TRAPPIST1e]] both require GP workarounds because PHOENIX models fail on TRAPPIST-1; no clear path to atmospheric inference until either models improve or empirical [[back-to-back-transit-correction]] is applied.
- **Geometric assumption: well-mixed photosphere vs fully-unocculted spots.** [[2025_Rathcke_TRAPPIST1bc]] argues for the former with a 6× reduction in predicted >2.5 μm contamination amplitude on TRAPPIST-1; the wider M-dwarf sample has not been tested.
- **TLSE framework on M-dwarf gas giants.** [[2026_Ashtari_HATS75b]] is the first GEMS application; a population-level test of how strongly TLS+atmosphere combinations bias retrieved metallicities on these hosts is pending.
- **Coupling between TLSE and disequilibrium chemistry on hot Jupiters.** No wiki paper has explicitly tested whether stellar contamination on F/G/K hosts is marginal at the precision of current hot-Jupiter retrievals; assumed negligible by default.

## Papers

### Joint atmosphere + TLSE on rocky M-dwarf planets
- [[2025_Rathcke_TRAPPIST1bc]] — SPHINX 1–4-component fits + in-transit joint fit; well-mixed photosphere preferred.
- [[2025_Bennett_GJ1132b]] — four-visit out-of-transit PHOENIX; explains Visit-1 outlier from [[2023_May_GJ1132b]].
- [[2025_Glidden_TRAPPIST1e]] — GP correction from companion paper; stellar model uncertainty dominates.
- [[2025_Espinoza_TRAPPIST1e]] — novel GP marginalization over stellar contamination on TRAPPIST-1 e PRISM.
- [[2025_PiauletGhorayeb_TRAPPIST1d]] — [[stctm]] / exotune sub-framework on TRAPPIST-1 d PRISM.
- [[2024_Banerjee_L98-59d]] — three-parameter contamination retrieval; combined "Stellar + Atmosphere" preferred.
- [[2024_Gressier_L98-59d]] — unocculted-spots/faculae rejected as sole explanation; atmosphere required.
- [[2023_Moran_GJ486b]] — in-transit POSEIDON starspot retrieval + 3-component out-of-transit PHOENIX fit.
- [[2023_May_GJ1132b]] — atmosphere vs unocculted-starspot retrievals; indistinguishable evidence.

### TLS framework on a GEMS gas giant
- [[2026_Ashtari_HATS75b]] — first wiki application; spots+faculae jointly retrieved with atmosphere.

### TLS as null test on a K-dwarf host
- [[2025_Gressier_HATP26b]] — POSEIDON_TLS retrieval on Neptune-mass HAT-P-26 b around K-dwarf host; T_het and f_het free; **Bayes factor < 1** vs no-TLS retrieval — no statistical preference for stellar contamination; sets a useful negative reference for K-dwarf low-mass-planet targets.

### Semi-empirical occulted-spot correction
- [[2025_FernandezRodriguez_K2-18b]] — novel two-stage method for spot-crossing events: subtract spotted vs spotless transit-model light curves, treat the spot signal shape as wavelength-invariant with free amplitude per wavelength bin. Applied to a NIRISS ingress spot-crossing on K2-18 b; statistically preferred over no-correction (ΔAIC = 14.24); reduces wavelength-dependent biases at the bluest wavelengths.

### Activity-driven null
- [[2025_Taylor_GJ357b]] — all four TLS parameterizations yield Bayes factors below the flat-line model; consistent with GJ 357's exceptional inactivity.
- [[2023_Lustig-Yaeger_LHS475b]] — no contamination detected on LHS 475 b; clean null counter-example.

### Theory / framework papers
- [[2018_Rackham_TLS]] — foundational forward-model framework for M-dwarf TLS contamination spectra; A ∝ f_spot^0.5 calibration; PHOENIX + DRIFT-PHOENIX component spectra. The reference paper for the [[stctm]] / Pinhas 2018 retrieval parameterization.
- [[2019_Rackham_TLS-FGK]] — extends the framework to F5V–K9V; reference activity-level spot fractions per spectral type (Table 4); identifies K-dwarf TLS as a viable mechanism for the [[HD189733b]] panchromatic slope.

### Pre-JWST hot-Jupiter benchmarks (HD 189733 b)
- [[2014_McCullough_HD189733b]] — first hot-Jupiter TLS reinterpretation; clear-atmosphere + δ ≈ 5.6 % unocculted spots at T_spot ≈ 3 700 K reproduces the 0.3–24 μm panchromatic spectrum without Rayleigh-scattering dust.
- [[2013_Pont_HD189733b]] — establishes the AC (variability-driven) + DC (steady) unocculted-spot decomposition; APT photometry Gaussian-process interpolation; per-instrument scaling factors c_λ.
- [[2008_Pont_HD189733b]] — earliest TLS-aware hot-Jupiter analysis at ~50 km transit-radius precision; five-solution cross-check.

### M-dwarf gas giant + ultracool dwarf — joint atmosphere + TLSE
- [[2023_Lim_TRAPPIST1b]] — sequential and simultaneous TLSE+atmosphere fits; H₂ < 52% at 3σ on the joint solution.

### Occulted-spot crossings on limb-resolved spectra — K-dwarf
- [[2025_Murphy_WASP107b]] — first wiki treatment of **occulted-starspot bias on limb-resolved transmission**; NIRISS/SOSS and NIRSpec/G395H visits of WASP-107 b show 20–30 minute spot-crossing residuals in the broadband light curves at multiple longitudes; develops a [[Catwoman]] + `starry` injection-recovery model showing that a single spot near ingress vs. egress can **flip the polarity** of a retrieved limb-asymmetry signal. Wavelength-independent additive offsets (NIRISS +110 ppm evening / +20 ppm morning; NIRSpec −195 ppm evening / +240 ppm morning) bring the spot-affected NIRISS and NIRSpec spectra into agreement with the spot-free NIRCam baseline. Caveat: chromaticity, multi-spot crossings, and faculae crossings deferred to future work.
