---
type: paper
bibkey: 2025_Canas_TOI5205b
authors: [Cañas, C. I., Lustig-Yaeger, J., Tsai, S.-M., Müller, S., Helled, R., Louie, D. R., Caloca, G. G., Gao, P., Libby-Roberts, J., Hardegree-Ullman, K. K., Colón, K. D., Czekala, I., Delamer, M., Han, T., Lin, A. J. S., Mahadevan, S., May, E. M., Ninan, J. P., Piette, A. A. A., Stefánsson, G., Stevenson, K. B., Teske, J., Wallack, N. L.]
year: 2025
venue: AJ
arxiv: 2502.06966
targets: [TOI-5205b]
instruments: [JWST-NIRSpec]
methods: [transmission-spectroscopy, atmospheric-retrievals, stellar-contamination-modeling]
species_detected: [CH4, H2S]
species_tentative: []
species_ruled_out: []
codes: [ExoTiC-JEDI, Eureka, juliet, spotrod, PICASO, VULCAN, FastChem, POSEIDON, PLATON, MultiNest]
tags: [gas-giant, m-dwarf-host, gems, stellar-contamination, sulfur-bearing, metal-poor, mass-metallicity-anomaly]
ingested: 2026-05-16
---

# GEMS JWST: Transmission spectroscopy of TOI-5205b reveals significant stellar contamination and a metal-poor atmosphere

**Authors:** Cañas, Lustig-Yaeger, Tsai, Müller, Helled, Louie, Caloca, Gao, Libby-Roberts, Hardegree-Ullman, Colón, Czekala, Delamer, Han, Lin, Mahadevan, May, Ninan, Piette, Stefánsson, Stevenson, Teske, Wallack (2025, AJ; arXiv:2502.06966)
**Target:** [[TOI-5205b]] · **Host:** [[TOI-5205]] · **Instrument:** [[JWST-NIRSpec]] PRISM · **Program:** [[JWST-GO-3171]] (PIs: Kanodia, Cañas, Libby-Roberts; "Red Dwarfs and the Seven Giants")

## TL;DR

Three [[JWST-NIRSpec]] PRISM transits (0.6–5.3 μm) of **TOI-5205 b** — a short-period (P = 1.63 d) Jupiter-like planet (M_p = 1.08 M_J, R_p = 0.94 R_J) orbiting an M4 dwarf, one of the **most extreme [[GEMS]]-class targets** in the wiki (planet-to-star mass ratio similar to Saturn around the Sun). All three transits exhibit **clear occulted spot-crossing events**, and the transmission spectra show a strong rise in transit depth toward the blue — the signature of unocculted-spot transit-light-source (TLS) contamination. **Stellar contamination is detected at >20σ** and the planetary atmosphere is detected at >12σ in nested Bayesian model comparison. Across multiple retrievals (PICASO + VULCAN + POSEIDON + PLATON) the data consistently favor a **sub-solar atmospheric metallicity (log [M/H] → −1 to −2)** combined with a **super-solar C/O ratio (≈ 1.2–1.3, ~3× solar)** — both clear/cloud-free. **[[CH4]] and [[H2S]]** drive the molecular features between 3–5 μm. The TLS dominance below 3 μm reduces sensitivity to H₂O. **Atmospheric metallicity is ~100× lower than the predicted bulk metallicity** from interior models (10–20% by mass) — suggesting the planet's interior and atmosphere are decoupled, with implications for [[GEMS]] formation and atmospheric mixing.

## Key findings

- **Significant stellar contamination ([[stellar-contamination]]) at >20σ.** Visit-to-visit variability in spot-crossing patterns (4 spots Visit 1+2; 3 spots Visit 3) detected directly in light curves; modeled with [[spotrod]]. After spot-crossing removal, residual unocculted-spot TLS contamination still drives a strong blueward slope in the transmission spectrum.
- **CH₄ and H₂S detected in the planetary atmosphere.** Free-chemistry retrievals constrain log VMR(CH₄) ≈ −5.5 to −5.6, log VMR(H₂S) ≈ −4.3 to −4.5 across visits. CH₄ at >3σ (1.2 + 1.7 μm bands); H₂S band at 3.9 μm. Both species are model-stable across pipelines (PLATON vs POSEIDON give consistent posteriors).
- **Sub-solar atmospheric metallicity.** PLATON equilibrium-chemistry retrieval: log [M/H] = −1.92⁺⁰·¹¹₋₀·₀₅ (≈ 0.01× solar). POSEIDON (with spots + faculae): log [M/H] = −0.76⁺⁰·¹⁷₋₀·₁₀ (~0.17× solar) — both at the lower edge of their model grids. PICASO RCTE grid: −2.0 ≤ log [M/H] ≤ 0.0 (preferred at grid edge); VULCAN photochemistry extended grid pushes to −2.0 dex consistently.
- **Super-solar C/O ≈ 1.2–1.3** (~3× the solar value of 0.458). POSEIDON: C/O = 1.3 ± 0.4. PLATON: 1.2 ± 0.4. VULCAN photochemistry: C/O = 0.25 to 1.0 across best-fit models.
- **Atmospheric vs bulk metallicity decoupling.** Müller & Helled (2021) bulk interior modeling predicts TOI-5205 b's bulk Z = 10–20% (>100× solar). The atmosphere sees ~0.01–0.17× solar — implying **~100× lower atmospheric than bulk metallicity**. Two scenarios: (i) atmospheric chemistry is decoupled from interior (poor mixing, settling of heavy elements into a deep envelope/core layer); (ii) primordial atmosphere captured from low-metallicity disk material that hasn't been mixed with interior heavy elements.
- **No firm H₂O detection.** Below ~3 μm the spectrum is TLS-dominated; the strongest H₂O features at 1.4 / 1.9 μm cannot be cleanly separated from spot contamination. Upper limit log VMR(H₂O) < −2.6 (no firm absorption).
- **Stellar parameters.** Best-fit photosphere T_phot = 3430 K; spot T_spot = 3156⁺⁴⁵₋₅₆ K (~270 K cooler than photosphere); faculae T_fac = 4263⁺¹³²₋₅₆ K (~830 K hotter). Spot covering fraction f_spot = 0.132⁺⁰·⁰¹⁵₋₀·₀¹³; faculae f_fac = 0.015⁺⁰·⁰⁰⁵₋₀·⁰⁰⁴.
- **Cloud/haze evidence is marginal** (~3σ in the most complex model M3.4 with cloud + haze; rejected in cleaner models). The atmosphere is essentially clear.
- **Planet radius refined.** R_p = 0.94 ± 0.04 R_J (smaller than ground-based estimates by ~6%, attributed to spot bias in ground-based light curves).
- **Inflated planet relative to mass-radius**: R_p / R_J = 0.94 at M_p = 1.08 M_J places TOI-5205 b on the inflated side of the gas-giant mass-radius distribution for its irradiation.

## Methods

**Observations.** Three [[JWST-NIRSpec]] PRISM transits under [[JWST-GO-3171]] on 2023-10-10, 2023-10-11, 2023-10-13 (visits 16, 17, 18 of the program). BOTS mode, NRSRAPID readout, SUB512 subarray (32×512 pixels), 15784 integrations of 4 groups each per visit; 1.5 hr pre-transit + 1 hr post-transit baseline. Visit 2 (observation 17) suffered a tilt event (telescope-segment perturbation) — first 2070 integrations excluded.

**Two reductions:** [[ExoTiC-JEDI]] (Alderson et al. 2022) and [[Eureka]] v0.10 — both produced spectra at native resolution from Stage 4 of Eureka! (columns 30–491, ~0.52–5.58 μm). Agreement at < 1σ across most wavelengths. Eureka used for downstream retrievals.

**Light-curve fitting.** White light curves jointly fit across three transits with [[juliet]] modified to include [[spotrod]] semi-analytical spot-crossing models. Configurations of 1–4 spots per visit tested; preferred: 4 spots (Visit 1, 2), 3 spots (Visit 3). Limb-darkening fixed to ExoTiC-LD/PHOENIX predictions for T_eff = 3430 K. Spot model parameters listed in Table 7.

**Forward modeling and grids.**
- **[[PICASO]]** RCTE (radiative-convective + thermochemical-equilibrium) atmospheric models on a grid: 13 [M/H] (−1.0 to +2.0), 6 C/O, 5 T_int (100–500 K), 3 r_st (heat-redistribution factors) = 1170 base models. Cross-sections from [[FastChem]] / Sonora Bobcat grid. Post-processed for stellar contamination with quiet + spot photosphere weighting at f_spot = 0.01–0.30, T_spot = 3230 / 3330 K.
- **[[VULCAN]]** disequilibrium photochemistry coupled to PICASO P-T grids; same parameter space + K_zz (10⁶ or 10⁹ cm² s⁻¹) + sulfur enhancement (f_S = 1, 10, 100). Used to extend the metallicity grid below [M/H] = −1.

**Bayesian retrievals.**
- **[[PLATON]]** v6.1: equilibrium-chemistry retrieval with [[FastChem]]. Spot-only TLS parameterization. R = 20,000. Dynesty sampler, 5000 live points.
- **[[POSEIDON]]** (MacDonald 2023): equilibrium-chemistry + free-chemistry retrievals; stellar contamination with **spots + faculae** (more flexible than PLATON). Free-chemistry retrievals fit H₂O, CH₄, CO₂, CO, SO₂, H₂S. 17-parameter baseline + nested models with/without clouds and hazes. 400 [[MultiNest]] live points.

**Model comparison.** Nested model comparison shows TLS effect is required (M1.4 vs no-TLS at >20σ); atmospheric absorption is required (M3.1 vs M1.4 at >12σ); clouds + hazes only marginal preference (~2–3σ). Preferred final model: TLS + atmosphere (M3.1).

## Caveats & limitations

- **Sub-grid metallicity preference.** Both POSEIDON and PLATON metallicity posteriors fall at the lower edge of their model grids ([M/H] → −0.9 in POSEIDON; → −2 in PLATON). Extending grids would refine — but the result is robust to the lower-bound choice.
- **C/O is super-solar but loosely constrained.** Posteriors span ~0.5–2.0 with peaks ≈ 1.2–1.3; the inferred C/O depends on which species are dominant — and CH₄ + H₂S dominate the inferences.
- **TLS-atmosphere covariance.** The free reference radius covaries with spot temperature; the cloud-top pressure correlates with CH₄ abundance. Multi-visit fits don't fully break these degeneracies. Future visits would help.
- **Visit-to-visit variability** in spectral feature amplitudes reflects spot configuration changes; the *atmospheric* parameters do agree within 1σ across visits (when clouds removed), but the joint posteriors are non-trivial.
- **No JWST emission counterpart.** Eclipses on TOI-5205 b under JWST would reach ~150–300 ppm — potentially achievable but not yet observed.
- **Equilibrium-chemistry assumption.** RCTE models systematically struggle to fit the < 3.5 μm region (χ² > 14 without TLS; χ² ≈ 2.6 with). VULCAN disequilibrium-chemistry improves the fit somewhat (χ² ≈ 2.6 → 2.56) but does not eliminate residuals.
- **Bulk-metallicity calibration is theory-driven.** Müller & Helled 2021 interior modeling for inflated GEMS is sensitive to equation-of-state choices and total H/He envelope mass — the 10–20% bulk metallicity prediction has ~factor-2 uncertainty.

## Open questions / follow-ups

- **Why is the atmospheric metallicity ~100× lower than bulk?** Possible scenarios: (i) primordial gas-accreted atmosphere from a low-metallicity disk that hasn't equilibrated with the heavy interior; (ii) settling of heavy elements onto an internal "core" layer; (iii) inefficient atmospheric mixing. Discriminator: more GEMS targets with both interior and atmospheric metallicity measurements.
- **Is the super-solar C/O a formation tracer?** A C/O ≈ 1.2 implies envelope accretion within the soot line (carbon-rich gas) with limited subsequent enrichment from oxygen-rich pebble accretion. Compare to [[WASP-94Ab]] (C/O = 0.49 substellar; pebble-accretion + migration) and [[K2-18b]] (C/O ~ 10).
- **Population trend for GEMS.** TOI-5205 b is the second GEMS target with a JWST atmospheric metallicity inference, after [[2026_Ashtari_HATS75b]] (sub-solar metallicity ~similar). Both being sub-solar atypically for hot Jupiters challenges the GEMS-formation core-accretion picture.
- **Companion-target sample.** The "Red Dwarfs and Seven Giants" sample (TOI-3984 A, TOI-3757, HATS-6, HATS-75 b, TOI-5293 A, TOI-3714, TOI-5205) — six more atmospheric inferences pending. Pattern emerging: GEMS show sub-solar atmospheric metallicities and significant TLS contamination.

## Related

- [[2026_Ashtari_HATS75b]] — second [[JWST-GO-3171]] GEMS-JWST result; **HATS-75 b**: also sub-solar atmospheric metallicity in TLS framework; same retrieval methodology. Both GEMS atmospheric metallicities are sub-solar despite being inflated gas giants.
- [[GEMS]] — concept page; this paper grows the GEMS-JWST sample to 2 targets.
- [[stellar-contamination]] — extreme case (>20σ TLS detection); M4-dwarf hosts dominate the wiki TLS sample.
- [[CH4]] — detected on TOI-5205 b at >3σ; latest in a growing CH₄-on-warm-giant sample.
- [[H2S]] — detected on TOI-5205 b; complements [[WASP-39b]] (NEXOTRANS retrieval) + [[2025_Gressier_HATP26b]] (HAT-P-26 b tentative).
- [[PLATON]] — used as the equilibrium-chemistry retrieval engine; demonstration of cross-code consistency with [[POSEIDON]].
- [[2025_Madhusudhan_subneptunes]] — review touching on M-dwarf giant atmospheric characterization.
