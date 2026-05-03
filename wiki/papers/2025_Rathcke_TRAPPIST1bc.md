---
type: paper
bibkey: 2025_Rathcke_TRAPPIST1bc
authors: [Rathcke, A. D., Buchhave, L. A., de Wit, J., Rackham, B. V., August, P. C., Diamond-Lowe, H., Mendonça, J. M., Bello-Arufe, A., López-Morales, M., Kitzmann, D., Heng, K.]
year: 2025
venue: ApJL
doi: 10.3847/2041-8213/ada5c7
targets: [TRAPPIST-1b, TRAPPIST-1c]
instruments: [JWST-NIRSpec]
methods: [back-to-back-transit-correction, stellar-contamination-modeling, multi-visit-stacking, transmission-spectroscopy]
species_detected: []
species_tentative: []
species_ruled_out: []
codes: [Frida, speclib, spotter, SPHINX]
tags: [trappist-1, m-dwarf-host, terrestrial, stellar-contamination, methodology, jwst]
ingested: 2026-04-24
---

# Stellar Contamination Correction Using Back-to-back Transits of TRAPPIST-1 b and c

**Authors:** Rathcke, Buchhave, de Wit, Rackham, August, Diamond-Lowe, Mendonça, Bello-Arufe, López-Morales, Kitzmann, Heng (2025, ApJL 979:L19) · [doi:10.3847/2041-8213/ada5c7]
**Targets:** [[TRAPPIST-1b]], [[TRAPPIST-1c]] · **Host:** [[TRAPPIST-1]] · **Instrument:** [[JWST-NIRSpec]] (PRISM, 0.6–5.3 μm)
**Program:** [[JWST-GO-2420]]

## TL;DR
A proof of concept for a **model-independent**, **epoch-specific** stellar-contamination correction in transmission spectroscopy: divide the transit spectrum of an active-atmosphere candidate by that of a quasi-simultaneously transiting near-airless companion that traverses a near-identical chord. Applied to JWST/NIRSpec PRISM transits of TRAPPIST-1 b and c observed back-to-back on 2024 July 9, the spectra of b and c show **highly consistent contamination signals**, validating the approach. Using b to correct c yields a **2.5× reduction in red noise at 0.8–2 μm**, removing the 1.4 / 1.8 μm water features and most of the blue slope. At 2–5 μm the single-visit SNR is too low to verify the correction directly, but out-of-transit variations and a separate photospheric-model fit imply contamination persists and is mitigated to a similar extent. The method shifts the dominant noise from structured red noise (contamination) to white noise — addressable by stacking visits — and brings the **60–250 ppm secondary-atmosphere regime into reach** for TRAPPIST-1 system searches. A separate joint analysis of in- and out-of-transit data finds that TRAPPIST-1's ~2000 K and ~2600 K photospheric components are **well mixed across the disk**, reducing the expected long-wave contamination amplitude by ~6× relative to the conventional "spot fully unocculted" assumption.

## Key findings
- **Method validation:** transit spectra of TRAPPIST-1 b and c, observed back-to-back on the same visit, exhibit highly consistent contamination features — both the blue (0.8–1.5 μm) slope and the 1.4 / 1.8 μm water bands. Redward of 2 μm the two are mutually consistent within 110 ppm (1.2σ) per 0.1 μm bin.
- **Correction efficacy at 0.8–2 μm:** dividing c by b and renormalizing to b's 2–5 μm weighted-mean depth removes the water features and most of the blue slope; Allan variance shows the noise floor at bin size 10 drops from ~200 ppm to ~80 ppm — a **factor 2.5 red-noise reduction**.
- **Correction at 2–5 μm:** one-visit SNR insufficient to verify directly. The corrected spectrum is white-noise dominated down to ~40 ppm at the ~0.3 μm CO₂-feature bin width; the paper argues by analogy with the blue-side success that contamination is reduced by a similar factor (~200 → ~80 ppm).
- **Photospheric model:** SPHINX-grid 2-component fits to the out-of-transit spectrum yield **~55.6% T₁ ≈ 2000 K + ~44.4% T₂ ≈ 2600 K** disk coverage; T₁ is at the SPHINX grid floor and is therefore an upper limit. Effective temperature implied by the model + scale factor is ~2463 K, within 2σ of the Agol et al. 2021 literature value (2566 ± 26 K) given a 50 K systematic floor.
- **Time-resolved photospheric variability:** splitting the baseline into S1–S5 segments shows the cool-component covering fraction rises from 55.5% (S1) to 55.7% (S4, just after b's transit) before declining — i.e., **~0.1% / hr** — qualitatively tracking the white-light dimming over the visit.
- **Well-mixed photosphere:** the in-transit data prefer a mixed model with cool-component coverage f₁,chord ≈ 0.495 — only 6.1% below the disk-average 0.556 — rather than the conventional "cool component fully unocculted" assumption. This reduces the expected peak-to-peak contamination amplitude at λ > 2.5 μm from **1740 ppm → 280 ppm** (~6× reduction); important for CO₂-feature detectability.
- **Interchangeable reference planets:** with their nearly identical radii, similar impact parameters, and matching contamination signatures, both TRAPPIST-1 b and c can serve as reference (anchor) planets for atmospheric searches on TRAPPIST-1 d, e, f, g, h. Doubles the count of viable transit-pair windows (e.g., GO 6456 c+e is twice as frequent as b+e at <5 hr separation).
- **No atmospheric claims for b or c:** consistent with prior airless / thin-atmosphere expectations from Greene et al. 2023 and Zieba et al. 2023 (both not yet ingested), but the paper makes no new species detection or rejection.

## Methods
- **Observations:** quasi-simultaneous transits of TRAPPIST-1 b and TRAPPIST-1 c on 2024 July 9 with [[JWST-NIRSpec]] PRISM (S1600A1 slit, SUB512 subarray, NRSRAPID readout, 6 groups/integration). 10208 integrations covering ~5 hr.
- **Reduction:** custom pipeline [[Frida]] — uses only stage-1 of the STScI `jwst` pipeline; from stage 2 on it is independent. Custom bad-pixel masking, column-wise 1/f removal, preamp reset-noise removal, group-difference rate calculation (preferred over up-the-ramp fitting at low group counts), 5σ time-series cosmic-ray identification, optimal extraction with a smoothed-median PSF weight.
- **White-light fit:** joint two-planet `t0`, `P`, `Rp/R★`, `a/R★`, `i` with Gaussian priors from Agol et al. 2021. Shared quadratic limb-darkening (Kipping 2013 reparameterization), linear-trend systematics, squared-exponential GP, and a white-noise term — 17 free parameters, MCMC via `emcee` on 341 30-integration time bins. See Table 1 of the paper for priors and posteriors.
- **Spectroscopic fits:** per-bin fits with white-light wavelength-independent parameters and GP hyperparameters fixed; planet radii, linear-trend coefficients, and limb-darkening floated.
- **Out-of-transit photospheric modeling:** the Narrett et al. 2024 / Rackham & de Wit 2024 framework — see [[stellar-contamination-modeling]]. [[SPHINX]]-grid (A. R. Iyer et al. 2023) spectra interpolated via [[speclib]] in T_eff with `[Fe/H]` and `log g` fixed to Agol 2021 values. Stellar-surface chord visualization with [[spotter]]. 1- to 4-component photospheres tested on five sub-baseline spectra (S1–S5) and the full out-of-transit mean (S_all), with 2MASS fluxes as a constraint and a fitted JWST flux scale factor. Uncertainties **not** inflated for model-fidelity, deliberately, to expose temporal trends.
- **Stellar-contamination model for the in-transit data:** ε = (f₁,chord F₁ + f₂,chord F₂) / (f₁,disk F₁ + f₂,disk F₂); f_chord is varied independently of the disk-average covering fractions to test mixing. χ² scan over f₁,chord favors 0.495.
- **Stacking implication:** [[multi-visit-stacking]] is identified as the natural follow-up — once the correction reduces structured noise to a white-noise floor, additional visits scale as 1/√N and bring the 60–250 ppm secondary-atmosphere regime into reach.

## Caveats & limitations
- **Single visit only.** Long-wavelength assessment of contamination relies on extrapolating the demonstrated short-wavelength performance; a multi-visit campaign is needed to verify directly.
- **SPHINX grid floor at 2000 K.** The cool-component temperature is therefore an upper limit; true T₁ could be lower, with corresponding shifts in covering fractions.
- **Stellar-model fidelity.** The paper explicitly does not inflate uncertainties for stellar-model imprecision in the time-trend analysis. Inferred stellar parameters are not definitive — see also Wakeford et al. 2019 and Garcia et al. 2022 (both not yet ingested) for the wider model-fidelity discussion.
- **Residual blue-slope difference.** A small slope difference between the b and c uncorrected spectra remains after correction, attributed either to surface-coverage evolution between the two transits or to slightly different transit chords; the technique cannot distinguish.
- **Residual systematics.** Allan variance after correction still deviates from the 1/√N white-noise scaling, indicating some structured noise remains.
- **No atmosphere claim.** The paper does not detect or rule out atmospheric features on b or c; it builds the tooling for the search rather than executing it.

## Open questions / follow-ups
- Does the back-to-back technique generalize to other multi-planet systems with at least one airless reference? The discussion frames this as the next-step deployment.
- How does the contamination-correction performance scale with stacking? The paper sets up the case but does not coadd visits.
- Can the well-mixed-photosphere geometry inferred here be cross-validated with future spot-tracking observations or independent flares analyses?
- What range of low-pressure secondary atmospheres on TRAPPIST-1 b/c remains permitted given the corrected spectrum's noise floor?

## Tensions
- **Well-mixed photosphere vs. fully-unocculted-spot conventions.** The standard transit-light-source-effect formulation (Rackham et al. 2018; not yet ingested) places the inhomogeneity entirely outside the transit chord, predicting a peak-to-peak >2.5 μm contamination amplitude of ~1740 ppm for TRAPPIST-1 under the inferred 2-component model. The in-transit + out-of-transit joint analysis here prefers a mixed configuration that drops this to ~280 ppm — a sixfold reduction. Status: not contradictory in principle (different geometric assumption), but materially changes the expected contamination budget for TRAPPIST-1 atmosphere searches at long wavelengths. Recorded on [[stellar-contamination]].

## Related
- [[2023_Lustig-Yaeger_LHS475b]] — the canonical clean null on a low-activity M-dwarf; useful contrast for what TRAPPIST-1's contamination looks like when there is none.
- [[2023_Moran_GJ486b]] / [[2024_WeinerMansfield_GJ486b]] — the GJ 486 b transmission/emission resolution pair that motivated empirical contamination handling.
- TRAPPIST-1 JWST Community Initiative et al. 2024 (Nat. Astron. 8, 810; not yet ingested) — proposed the back-to-back technique that this paper executes.
- Greene et al. 2023, Zieba et al. 2023 (both not yet ingested) — set the airless / thin-atmosphere context for TRAPPIST-1 b and c.
