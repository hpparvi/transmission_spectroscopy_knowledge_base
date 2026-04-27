---
type: paper
bibkey: 2023_Lustig-Yaeger_LHS475b
authors: [Lustig-Yaeger, J., Fu, G., May, E. M., Ortiz Ceballos, K. N., Moran, S. E., Peacock, S., Stevenson, K. B., López-Morales, M., MacDonald, R. J., Mayorga, L. C., Sing, D. K., Sotzen, K., Valenti, J. A., Adams, J., Alam, M. K., Batalha, N. E., Bennett, K. A., Gonzalez-Quiles, J., Kirk, J., Kruse, E., Lothringer, J. D., Rustamkulov, Z., Wakeford, H. R.]
year: 2023
venue: Nature Astronomy
arxiv: 2301.04191
targets: [LHS475b]
instruments: [JWST-NIRSpec]
methods: [transmission-spectroscopy, atmospheric-retrievals, multi-visit-stacking, stellar-contamination-modeling]
species_detected: []
species_tentative: []
species_ruled_out: [H2, CH4]
codes: [Eureka, FIREFLy, Tiberius]
tags: [earth-sized, m-dwarf-host, rocky-planet, jwst-go-1981, champs, null-result, first-light]
ingested: 2026-04-22
---

# A JWST Transmission Spectrum of a Nearby Earth-Sized Exoplanet

**Authors:** Lustig-Yaeger, Fu, May, Ortiz Ceballos, Moran, et al. (2023, Nature Astronomy; arXiv:2301.04191)
**Target:** [[LHS475b]] · **Host:** [[LHS475]] · **Instrument:** [[JWST-NIRSpec]] (G395H, 2.87–5.27 μm)
**Program:** [[JWST-GO-1981-CHAMPs]]

## TL;DR
Two JWST NIRSpec/G395H transits of the nearby Earth-sized (Rp = 0.99 R⊕) rocky exoplanet LHS 475 b, validating the TESS candidate TOI 910.01 and delivering the first JWST transmission spectrum of an Earth-sized planet. The co-added spectrum is **featureless**, ruling out **primordial H₂-dominated atmospheres at > 10σ** for metallicities 1–100× solar and pure [[CH4]] atmospheres at ≥ 5σ. The data are consistent with an airless body, a pure [[CO2]] or [[H2O]] atmosphere, a Venus-like cloud deck, a Mars-like tenuous atmosphere, or an Earth-like high-MMW secondary atmosphere — all scenarios that produce transmission features < 50 ppm at NIRSpec G395H wavelengths. A 5 ppm noise floor demonstrates JWST can characterize terrestrial exoplanet atmospheres down to Earth-like feature amplitudes; the observed non-detection is a property of the **planet, not the instrument**.

## Key findings
- Two G395H transits (2022-08-31, 2022-09-04); three independent reductions ([[Eureka]], [[FIREFLy]], [[Tiberius]]) agree within ~1.1σ.
- Co-added spectrum is flat (χ²ν = 0.91 for a flat-line model).
- **Primordial H₂/He atmospheres at 1–100× solar metallicity rejected at > 10σ.**
- Pure CH₄ atmospheres rejected at ≥ 5σ (low molecular weight of CH₄ + strong 3.3 μm band drive the rejection).
- Consistent with: airless body / high-MMW secondary atmosphere / pure H₂O / pure CO₂ / Earth-like / Venus-like cloud deck / Mars-like tenuous atmosphere.
- **No stellar contamination** from starspots or faculae detected; [[LHS475]] is a low-activity M3.5V dwarf — see [[stellar-contamination]].
- 3σ absorption-feature upper limits: 61 ppm at 2.8 μm (H₂O), 38 ppm at 3.3 μm (CH₄), 49 ppm at 4.3 μm (CO₂), 62 ppm at 4.6 μm (CO).
- No evidence of a NIRSpec instrumental noise floor above 5 ppm.

## Methods
- **Observations:** two NIRSpec/G395H BOTS transits of LHS 475 b, 4 days apart; 2.9 hours each, 1158 integrations at 9 groups/integration.
- **Reduction:** three independent pipelines — [[Eureka]], [[FIREFLy]] (primary for final spectrum), [[Tiberius]]. Custom group-level background subtraction for 1/f noise.
- **Light curves:** simple linear trend + `batman` transit; Eureka! and FIREFLy agree within 1.1σ.
- **Multi-visit analysis:** weighted average of two-visit spectra binned to R~100 in 56 channels; see [[multi-visit-stacking]].
- **Forward modeling:** single-gas 1-bar isothermal atmospheres (pure H₂O, CH₄, CO₂, Earth-like) tested by χ² comparison; see [[transmission-spectroscopy]].
- **Retrievals:** 5-component (H₂O, CO₂, CH₄, CO + inactive bulk) Bayesian [[atmospheric-retrievals]] marginalizing over apparent surface pressure (10⁻⁶ to 10⁰ bar), MMW (2.5–50 g/mol), and planet mass consistent with a rocky interior.
- **Stellar contamination check:** no spot crossings during transits; residuals Gaussian; out-of-transit stellar activity low. See [[stellar-contamination-modeling]].

## Caveats & limitations
- Cannot distinguish between airless, tenuous, and high-cloud scenarios with G395H alone — degeneracies among high-MMW, small-scale-height, and high-cloud-top-pressure atmospheres span the allowed parameter space.
- LHS 475 b's mass is unmeasured (estimated 0.91 M⊕ from interior modeling); scale-height calculations assume rocky composition.
- A third transit was planned under GO 1981 (2023) to tighten constraints (not analyzed in this paper).

## Open questions / follow-ups
- Is LHS 475 b truly airless, or does it host a thin Mars/Venus-like secondary atmosphere? Best resolved by secondary-eclipse thermal-emission follow-up (MIRI).
- Does LHS 475 b share the "bare rock" picture emerging for [[GJ1132b]] and the TRAPPIST-1 rocky planets?
- What does the statistics of multiple CHAMPs targets say about the cosmic-shoreline boundary for close-in M-dwarf rocky planets? See [[cosmic-shoreline]].

## Tensions
- None directly with prior wiki content.

## Related
- [[2023_May_GJ1132b]], [[2025_Bennett_GJ1132b]] — companion JWST CHAMPs papers on super-Earth GJ 1132 b; similar null-detection + bare-rock-favored picture.
- [[2025_Alam_L168-9b]], [[2024_Alderson_TOI-836b]], [[2025_Alderson_TOI-776b]] — JWST COMPASS companion results on other rocky M/K-dwarf super-Earths.
- Ment et al. in prep (not yet ingested) — ground-based follow-up validation of LHS 475 b.
