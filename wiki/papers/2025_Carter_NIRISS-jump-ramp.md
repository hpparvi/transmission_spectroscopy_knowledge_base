---
type: paper
bibkey: 2025_Carter_NIRISS-jump-ramp
authors: [Carter, A. L., Espinoza, N., Albert, L., Brandt, T., Baines, T., Filippazzo, J., Volk, K.]
year: 2025
venue: JWST Technical Report
doi: JWST-STScI-008975
targets: [WASP-39b]
instruments: [JWST-NIRISS]
methods: [transmission-spectroscopy]
species_detected: []
species_tentative: []
species_ruled_out: []
codes: [Eureka]
tags: [methodology, calibration, pipeline, niriss-soss, ramp-fitting, jump-detection, technical-report, jwst-pipeline]
ingested: 2026-05-16
---

# Effects of Jump Detection and Ramp Fitting Algorithms on NIRISS/SOSS Exoplanet Time-Series Observations

**Authors:** Carter, Espinoza, Albert (Université de Montréal), Brandt, Baines, Filippazzo, Volk (2025, JWST Technical Report STScI-008975; release 6 May 2025)
**Target:** [[WASP-39b]] (ERS test case) · **Instrument:** [[JWST-NIRISS]] SOSS

## TL;DR

JWST Technical Report assessing the **differential impact of jump detection and ramp-fitting algorithms** on NIRISS/SOSS exoplanet time-series observations (TSOs). Compares the **default JWST pipeline** (Anderson & Gordon 2018 two-point-difference jump detection + Fixsen et al. 2000 generalized-least-squares ramp fitting) against the **LIKELY method** (Brandt 2024a, 2024b: covariance-aware maximum-likelihood ramp fitting + χ²-based jump detection). Test bed: WASP-39 b NIRISS/SOSS from the [[JWST-ERS-1366]] visit + a suite of 23-realization simulated noise scenarios (Pristine / Poisson / White / 1/f / All). **Result:** the two methods produce transmission spectra that differ at the ~50 ppm level on-sky (WASP-39 b), and the LIKELY method offers a 12–18% improvement in residual scatter and maximum deviation from ground truth in the 1/f and All cases on simulated data. **Group-level 1/f noise correction** emerges as the dominant systematic; current default implementations are integration-level and biased. The on-sky differences exceed the ~10s-of-ppm precision needed for sub-Neptune atmospheric inference — implying that current and future NIRISS-based atmospheric claims may be method-dependent.

## Key findings

- **On-sky differences are ~50 ppm.** Comparing default-pipeline and LIKELY transmission spectra of WASP-39 b (ERS [[JWST-ERS-1366]] visit, 8.2 hr, 537 integrations, NIRISS/SOSS GR700XD, SUBSTRIP256 subarray) shows residual scatter between the two methods at ~50 ppm (σ; max ~150–200 ppm). The spectrum shape is consistent but wavelength-dependent biases emerge particularly at longer wavelengths (>2 μm), where the Order 1 trace has lower flux.
- **LIKELY method offers 12–18% improvement on simulated data.** Across the 1/f and All noise cases in 23 multi-simulation realizations:
  - All-noise case: LIKELY max deviation ~820 ppm vs default ~990 ppm (~17% better); standard deviation 86 ppm vs 99 ppm (~13% better).
  - 1/f-only: LIKELY max ~740 ppm vs default ~840 ppm (~12% better); σ 72 vs 82 ppm.
  - The improvement comes from LIKELY's covariance-aware treatment of differenced reads — correlated 1/f noise is better modeled than under default weighting schemes.
- **1/f noise dominates the systematic budget.** Even with optimal ramp fitting + jump detection, residual differences of ~6 ppm scatter / ~50 ppm max remain in spectra. Most of this is unmitigated 1/f striping that propagates from integration-level 1/f correction (current default) being inferior to **group-level 1/f correction** (not yet a default but commonly applied in the community: [[exoTEDRF]], [[SPARTA]], [[Eureka]]).
- **White-noise bias toward deeper transits.** A subtle but important finding: the White-noise case alone preferentially biases the fitted transit depth deeper for both methods, particularly at lower pixel illuminations. The flux-correlated inverse-dilution effect has max amplitude ~150 ppm and **can mimic broad atmospheric absorption features**. This is a "by-eye" wavelength-dependent structure that should not be over-interpreted.
- **Poisson-only case overestimates uncertainties slightly.** The Poisson-only simulation yields fitted transit depth uncertainties that are too tight by ~5–10% relative to the Gaussian-expected distribution — useful diagnostic for light-curve uncertainty calibration.
- **Snowballs and cosmic rays favor default method.** A caveat: the simulations do not include cosmic rays or spatially structured noise (snowballs, showers); preliminary on-sky analyses (Willott, priv. comm. as cited) suggest the default jump detection handles these better than LIKELY. The optimal pipeline may combine both methods.
- **LIKELY method requires ≥4 groups/integration.** With only 3 groups, only 2 differenced frames exist and individual jumps cannot be robustly identified — restricting LIKELY applicability for high-saturation observations. New multistripe subarray readouts (e.g., NIRCam MULTISTRIPE) could broaden applicability.
- **Architecture generalizes beyond SOSS.** NIRISS shares detector architecture with NIRCam and NIRSpec — Carter et al. predict similar benefits for [[JWST-NIRSpec]] BOTS and [[JWST-NIRCam]] Grism TSO modes. MIRI has different detector architecture and lower 1/f noise; less impact expected there.

## Methods

**On-sky test.** [[JWST-ERS-1366]] (PI: Batalha) NIRISS/SOSS observation of [[WASP-39b]]: 8.2 hr, 537 integrations, SUBSTRIP256 + GR700XD grism. Order 3 excluded (low flux; planned future calibration in GO-3279 PI: Hoeijmakers). Already analyzed in Feinstein et al. 2023 (not ingested) and Carter & May et al. 2024 (not ingested); used here as a well-characterized test bed.

**Simulated data.** IDT-SOSS simulator (Albert et al. 2023; not ingested) using WebbPSF trace profiles, PHOENIX stellar models at T_eff = 5400 K, log g = 4.5, J = 10.663; planet with uniform 1% transit at all wavelengths; orbital parameters from Carter & May 2024 (P = 4.0552842 d, b = 0.4498). 9 groups/integration × 537 integrations × 23 independent realizations.

Five noise prescriptions added to simulated *uncal.fits files:
- **Pristine** — no added noise (test ramp-fit floor).
- **Poisson** — pixel-level random Poisson noise.
- **White** — σ_w = 6.58.
- **1/f** — colored noise (β = 1.0217, σ_f = 6.11) calibrated to on-sky SUBSTRIP96 darks via Approximate Bayesian Computation (`abeec` package).
- **All** — all three combined.

**Reduction pipelines.** Two parallel reductions from *uncal.fits to *rateints.fits:
- **Default pipeline** — JWST Calibration Pipeline (CRDS_CTX = jwst_12.41.pmap for on-sky / jwst_13.03.pmap for simulated) with default jump detection (Anderson & Gordon 2018, two-point difference at ~7σ + snowball/shower modifications JWST-STScI-008545) and default ramp fitting (Fixsen et al. 2000, generalized least-squares).
- **LIKELY** — substituting jump detection and ramp fitting with Brandt 2024a/2024b implementation (algorithm = 'LIKELY' in the ramp-fitting step). Tridiagonal-covariance maximum-likelihood ramp + χ² jump rejection within the ramp-fit step. Now available as non-default option in the JWST pipeline.

Stage 2 (spectroscopic processing) and Stage 3 (light-curve fitting) identical between methods. Light curves extracted with custom box aperture (15-pixel half-height) + [[Eureka]] for fitting. White-light-curve parameters fixed to Carter & May 2024 best-fits.

## Caveats & limitations

- **Restricted on-sky validation.** WASP-39 b at T_eq ≈ 1200 K, ~2% transit depth, J = 10.6 — a bright, large-transit target. The ~50 ppm differences observed may be larger for fainter, lower-S/N habitable-zone targets where atmospheric signals are themselves ~10s of ppm. The on-sky impact on existing K2-18 b, GJ 1214 b, etc. NIRISS observations is **not** assessed here.
- **Ground-truth comparison limited to simulations.** Real-data absolute accuracy of either method cannot be assessed without an external truth — only *relative* differences are reported on-sky.
- **No cosmic rays in simulations.** Real JWST data exhibit cosmic-ray events; LIKELY may underperform default in this regime (preliminary indication only).
- **Single subarray.** SUBSTRIP256 only; SUBSTRIP96 (used for bright targets to avoid saturation) not tested. Authors expect similar behavior given the calibration was derived from SUBSTRIP96 darks but do not verify.
- **Group-level 1/f correction is the recommended next step.** Not implemented in this study; the residual differences remain a lower bound on the achievable accuracy.
- **MIRI not directly tested.** Detector architecture is different; benefits may not transfer.

## Open questions / follow-ups

- **Group-level 1/f correction as JWST pipeline default.** Authors explicitly call for testing and integrating this — currently a community practice ([[exoTEDRF]], [[SPARTA]]) but not the JWST Stage 1 default.
- **How does the choice of method propagate to atmospheric inferences?** Authors note ~50 ppm spectrum differences are "significant enough to bias the interpretation" for faint targets but do not perform the retrieval-level test. The K2-18 b debate ([[2025_Luque_K2-18b]], [[2025_FernandezRodriguez_K2-18b]], [[2025_Madhusudhan_K2-18b-MIRI]]) is one obvious downstream domain.
- **Hybrid jump-detection algorithms** combining the strengths of default (snowball/shower handling) and LIKELY (covariance treatment) are flagged as future work (D. Law, priv. comm.).
- **NIRCam Grism TSO and NIRSpec BOTS** would benefit from the same analysis; predicted similar but unverified.

## Related

- [[2025_FernandezRodriguez_K2-18b]] — uses [[exoTEDRF]] (which already includes group-level 1/f correction) for K2-18 b NIRISS; demonstrates the kind of cross-pipeline reduction-dependent variability Carter et al. anticipate.
- [[2025_Luque_K2-18b]] — also uses exoTEDRF for NIRISS+NIRSpec+MIRI; the ~50 ppm spectrum-shape differences across reductions Carter et al. quantify are a directly relevant lower bound on the cross-pipeline systematic budget.
- [[JWST-ERS-1366]] — WASP-39 b NIRISS visit used as the on-sky test bed.
- Feinstein et al. 2023, Carter & May et al. 2024 (not ingested) — published reductions of the same WASP-39 b data using the default pipeline.
- Brandt 2024a, 2024b (not ingested) — the LIKELY methodology references.
