---
type: paper
bibkey: 2025_Murphy_WASP107b
authors: [Murphy, M. M., Beatty, T. G., Schlawin, E., Bell, T. J., Radica, M., Kennedy, T. D., Mehta, N., Welbanks, L., Line, M. R., Parmentier, V., Greene, T. P., Mukherjee, S., Fortney, J. J., Ohno, K., Wiser, L., Arnold, K., Rauscher, E., Edelman, I. R., Rieke, M. J.]
year: 2025
venue: AJ
arxiv: 2506.03002
doi: 10.3847/1538-3881/addf38
targets: [WASP-107b]
instruments: [JWST-NIRCam, JWST-MIRI, JWST-NIRISS, JWST-NIRSpec]
methods: [transmission-spectroscopy, limb-asymmetry, stellar-contamination-modeling, atmospheric-retrievals]
species_detected: [SO2, CO2, H2O, CH4]
codes: [Eureka, Tshirt, exoTEDRF, Catwoman]
tags: [warm-jupiter, super-puff, jwst, limb-asymmetry, stellar-contamination, panchromatic]
ingested: 2026-05-04
---

# A Panchromatic Characterization of the Evening and Morning Atmosphere of WASP-107 b: Composition and Cloud Variations, and Insight into the Effect of Stellar Contamination

**Authors:** Murphy, Beatty, Schlawin, Bell, Radica, Kennedy, Mehta, Welbanks, Line, Parmentier, Greene, Mukherjee, Fortney, Ohno, Wiser, Arnold, Rauscher, Edelman, Rieke 2025, AJ 170:61 · [arXiv:2506.03002]
**Targets:** [[WASP-107b]] · **Instruments:** [[JWST-NIRCam]], [[JWST-MIRI]], [[JWST-NIRISS]], [[JWST-NIRSpec]]

## TL;DR
Reanalyzes five archival JWST transit observations of WASP-107 b ([[JWST-NIRCam]] F322W2 + F444W, [[JWST-MIRI]] LRS, [[JWST-NIRISS]]/SOSS, [[JWST-NIRSpec]] G395H) and extracts limb-resolved transmission spectra spanning 1–12 μm using the [[Catwoman]] two-semicircle transit model. Confirms the ~180 K evening–morning temperature gradient inferred previously from F322W2 alone (Murphy et al. 2024b; not ingested) and identifies, for the first time, **chemical and cloud heterogeneity between the limbs**: morning limb has ~5× more [[SO2]] (log VMR ≈ −4.7 vs −5.4 evening), ~40× more [[CO2]] (log VMR ≈ −3.6 vs −5.2 evening), and a strong broad 6–11 μm cloud feature absent on the evening limb; [[H2O]] is uniform between limbs. Develops an injection-recovery correction model for occulted-starspot bias on limb-resolved spectra (NIRISS and NIRSpec affected, NIRCam and MIRI clean) using [[Catwoman]] + [[Eureka]] + the `starry` stellar-surface model.

## Key findings
- **Evening–morning T gradient** of ~180 K (cloudy SPARC/MITgcm GCM matches; clear-atmosphere RM-GCM underpredicts) is corroborated across the panchromatic dataset, consistent with the original NIRCam/F322W2-only inference.
- **[[SO2]] heterogeneity:** χ²-grid analysis of the 4 μm + 7.5 μm + 8 μm + 10 μm features yields log(SO₂) = −5.4 (evening) and −4.7 (morning); 5× more [[SO2]] on the cooler morning limb. Consistent with photochemical models (S.-M. Tsai 2023b; not ingested) where SO₂ photodissociation on the dayside transports product to the nightside and is dredged through the morning limb.
- **[[CO2]] heterogeneity:** ~40× more [[CO2]] on the morning limb (log CO₂ = −3.6 vs −5.2). Higher significance than the SO₂ asymmetry; supports a quench-driven origin (M. Zamyatina 2024; not ingested) since CO₂ quenches at lower pressures than CH₄.
- **Cloud heterogeneity:** the broad 6–11 μm absorption feature reported by A. Dyrek 2024 (silicates) and L. Welbanks 2024a (parametric Gaussian; not ingested) is present **only** on the morning limb; absent on the evening limb. SPARC/MITgcm cloudy run with Na₂S (not silicates, KCl, MnS, or ZnS) reproduces this distribution; silicate clouds in RM-GCM are too homogeneous.
- **[[H2O]] uniformity:** χ²-grid analysis of the 2.7 μm feature yields log H₂O ≈ −2.5 (evening) and −2.3 (morning); within 68% confidence on both limbs. Consistent with theoretical expectations (Fortney et al. 2020; M. Zamyatina 2024; both not ingested) that H₂O homogenizes via circulation.
- **Occulted starspot bias on limb-resolved spectra:** broadband residuals of NIRISS/SOSS and NIRSpec/G395H show 20–30 minute spot-crossing bumps near transit ingress, midtransit, and egress. Authors apply [[Catwoman]] + `starry` injection-recovery and derive simple offset corrections (NIRISS evening +110 ppm, morning +20 ppm; NIRSpec evening −195 ppm, morning +240 ppm); after correction, NIRISS and NIRSpec evening- and morning-limb spectra align with NIRCam (which has no spot-crossings during its visit). Establishes that **a single occulting starspot can flip the polarity of a retrieved limb-asymmetry signal** if it occurs near ingress vs near egress.
- **WASP-39 b comparison:** WASP-107 b's evening-limb 4.4 μm CO₂ feature has ~⅓ the relative amplitude of WASP-39 b's evening; the morning limbs are ~equal. WASP-39 b's anomalously oversized evening CO₂ feature (N. Espinoza 2024; not ingested) is attributed to a relatively cloudy morning limb on WASP-39 b — the opposite cloud asymmetry to WASP-107 b.

## Methods
Five reductions: [[Tshirt]] for NIRCam F322W2 + F444W, [[Eureka]] for MIRI LRS, [[exoTEDRF]] for NIRISS/SOSS, [[Tshirt]] for NIRSpec/G395H. Each visit refit with [[Catwoman]] for evening- and morning-limb radii independently with quadratic limb darkening priors from ATLAS9 + ExoCTK + ExoTiC-LD. χ² grid sweeps over molecular VMR for SO₂, CO₂, H₂O on each limb (using [[Aurora]]-derived models) compared to forward GCMs (RM-GCM and SPARC/MITgcm cloudy/clear). Stellar contamination modeled via the `starry` stellar-surface code; injection-recovery tests measure spot bias on limb-resolved transit depths as a function of crossing longitude.

## Caveats & limitations
- Spot-crossing correction is wavelength-independent and assumes a single spot; achromaticity is a known simplification; magnetic facular crossings are not modeled.
- Cloud-opacity degeneracy with CO₂ and SO₂ feature amplitudes only partially explored; CO₂ asymmetry treated as upper limit when cloud opacity allowed to vary.
- Achromatic correction may not capture wavelength-dependent contrast of starspots; full chromatic spot-crossing model deferred to future work.
- Ground-truth temperature for limb T-gradient depends on the cloudy-GCM choice between two codes which differ by ~50 K despite both producing ~180 K morning–evening contrast.
- Limb asymmetry assumes the planetary chord aligns with stellar equator; WASP-107 b's near-polar orbit (Dai & Winn 2017; Rubenzahl 2021; not ingested) violates this — flagged as a future modeling concern.

## Open questions / follow-ups
- Eclipse spectroscopy (MIRI LRS or G395H) of WASP-107 b would directly test the morning-limb cloud and resolve the silicate vs Na₂S choice on the dayside.
- Why is the evening limb CO₂ feature smaller than the morning by ~40× when 3D circulation models (Tsai 2023a; Zamyatina 2024) predict only ~10× heterogeneity? Photochemistry-disequilibrium overlap may mask the underlying pattern.
- Does an occulted facular crossing on the morning limb (rather than the spot crossing on the evening limb in Visit 3) explain the sign-flipping in the polarity of NIRISS/NIRSpec limb-resolved spectra? Authors flag chromatic spot modeling as a community-level need.
- Companion JWST observations during the same transit window (e.g., from JWST-GTO-1201 NIRSpec; in execution) may resolve cloud properties further.

## Related
- [[2025_Fu_limb-asymmetry]] — uniform NIRISS/SOSS reanalysis sample including WASP-107 b; flagged as having both limbs uniformly muted (lowest-gravity sample member); now superseded by the panchromatic limb-resolved analysis here for the SO₂/CO₂/cloud heterogeneity result.
- [[2025_Crossfield_SO2shoreline]] — theoretical SO₂ shoreline grid; WASP-107 b sits comfortably above the photochemical threshold; the limb-resolved SO₂ asymmetry is consistent with the shoreline framework.
- [[2025_Gressier_HATP26b]] — first SO₂ in a Neptune-mass planet; complements the WASP-107 b SO₂ heterogeneity case for sub-Saturn-mass photochemistry.
- [[2025_LustigYaeger_WASP17b]], [[2025_Gressier_WASP17b]] — DREAMS panchromatic + limb-resolved analyses on WASP-17 b for cross-comparison.
