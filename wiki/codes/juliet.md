---
type: code
aliases: [juliet]
tags: [light-curve-fitting, transit-fitting, python, mcmc, nested-sampling, hub]
---

# juliet

Python light-curve and radial-velocity fitting package (Espinoza et al. 2019, MNRAS 490:2262; not yet ingested) providing a unified interface to BATMAN (transit models), radvel (RV models), nested sampling via dynesty or [[MultiNest]], and MCMC via emcee. Supports Gaussian-process detrending via george or celerite. The dominant downstream light-curve-fitting layer in the wiki — paired with most JWST reduction pipelines and especially tightly with [[transitspectroscopy]]; it appears in 9 wiki papers spanning rocky-M-dwarf transmission, hot-Jupiter dayside emission, sub-Neptune transmission, Neptune-mass transmission, and joint transit+RV system characterization.

## Variants

The wiki sees three juliet deployment patterns:

- **GP detrending with celerite Matérn 3/2 kernel.** The dominant pattern; used in [[2024_Gressier_L98-59d]], [[2025_Espinoza_TRAPPIST1e]] (per-visit GP amplitude + timescale), [[2025_Fisher_TOI1685b]] (Sep 1 visit quasi-sinusoidal systematics), [[2025_Gressier_HATP26b]], [[2025_Gressier_WASP17b]] (NIRISS/SOSS secondary eclipse). Standard for time-correlated noise on bright targets where wavelength-coherent systematics demand GP rather than parametric models.
- **Parametric / linear systematics with limb-darkening reparameterization.** [[2025_Taylor_GJ357b]] uses BATMAN with Kipping 2013 limb-darkening reparameterization + linear + PCA systematics for the GJ 357 b NIRISS/SOSS transit. [[2026_Heinke_HATP12b]] uses dynesty sampler for the HAT-P-12 b NIRISS/SOSS transit.
- **Joint transit + RV fitting.** [[2025_Xue_GJ3929b]] uses juliet for joint MIRI F1500W eclipse photometry + MAROON-X RV fitting (the only wiki use of juliet for combined photometric + RV fits — refines GJ 3929 b mass to 1.13 ± 0.09 M⊕).

## History

- **2019** — Espinoza et al. 2019 release; rapid uptake among Espinoza-group projects.
- **2024 onwards** — first JWST-era wiki appearance ([[2024_Gressier_L98-59d]]) as the L 98-59 d light-curve fitting layer.
- **2025–2026** — saturating wiki adoption: nine ingested papers, spanning every JWST instrument mode (NIRISS/SOSS, NIRSpec G395H, NIRSpec PRISM, MIRI F1500W). The transitspectroscopy + juliet chain is the canonical Espinoza-group reduction-to-fit workflow.

## Trade-offs

- **Strength: unified API across BATMAN + dynesty + celerite + emcee.** Switching between MCMC and nested sampling requires no code changes; pairing a BATMAN transit model with a celerite GP is one parameter dictionary.
- **Strength: GP detrending well-integrated.** Per-visit GP amplitudes and timescales as standard fit parameters; Matérn 3/2 kernel default. Cleaner than ad-hoc GP wrappers around BATMAN.
- **Strength: tight transitspectroscopy integration.** transitspectroscopy + juliet is the canonical Espinoza-group chain ([[2024_Gressier_L98-59d]], [[2025_Espinoza_TRAPPIST1e]], [[2025_Gressier_HATP26b]], [[2025_Gressier_WASP17b]]).
- **Limitation: not a reduction pipeline.** juliet starts from extracted light curves; upstream reduction must be handled by [[transitspectroscopy]], [[Eureka]], [[ExoTiC-JEDI]], etc.
- **Limitation: limited support for ECLIPSE or phase-curve fits.** Hot-Jupiter phase-curve papers ([[2025_Sikora_HD80606b]], [[2025_Murphy_WASP107b]]) tend to use specialized fitting infrastructure outside juliet.
- **Limitation: BATMAN's symmetric two-circle transit model.** No native support for the asymmetric two-semicircle transit model used in [[limb-asymmetry]] retrievals — [[Catwoman]] is the standard alternative.

## Open issues

- **Standardization of GP kernel choice.** Matérn 3/2 is the wiki default but other kernels (squared-exponential, simple-harmonic-oscillator) appear in some papers; no community standard for which kernel to choose for which systematics class.

## Papers

### Rocky M-dwarf transmission — primary light-curve fitting
- [[2024_Gressier_L98-59d]] — L 98-59 d NIRSpec G395H + dynesty + Matérn 3/2 GP via george.
- [[2025_Espinoza_TRAPPIST1e]] — four TRAPPIST-1 e PRISM transits; per-visit GP amplitude + timescale.
- [[2025_Fisher_TOI1685b]] — five TOI-1685 b G395H transits; Sep 1 visit GP for quasi-sinusoidal systematics.
- [[2025_Taylor_GJ357b]] — GJ 357 b NIRISS/SOSS; BATMAN + Kipping 2013 LD + linear + PCA systematics.

### Hot Jupiter / Neptune-mass / sub-Saturn — light-curve fitting
- [[2025_Gressier_HATP26b]] — HAT-P-26 b NIRSpec G395H + celerite Matérn 3/2 GP.
- [[2025_Gressier_WASP17b]] — WASP-17 b NIRISS/SOSS secondary eclipse + Matérn 3/2 GP.
- [[2026_Radica_WASP96b]] — WASP-96 b NIRSpec G395H transit (alongside exoUPRF).
- [[2026_Heinke_HATP12b]] — HAT-P-12 b NIRISS/SOSS + dynesty.

### Joint transit + RV
- [[2025_Xue_GJ3929b]] — GJ 3929 b MIRI F1500W eclipse + MAROON-X RVs jointly fit; refines mass to 1.13 ± 0.09 M⊕.
