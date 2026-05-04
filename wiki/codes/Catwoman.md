---
type: code
aliases: [catwoman, asymmetric transit model]
tags: [light-curve-fitting, limb-asymmetry, transit-model]
---

# Catwoman

Asymmetric transit-light-curve model (Jones & Espinoza 2020; Espinoza & Jones 2021) that approximates the planet as **two semicircles** with potentially different radii (Rp1 = leading/morning, Rp2 = trailing/evening). Recovering ΔRp = Rp2 − Rp1 from the in-transit light curve is the standard way to extract limb-resolved transmission spectra without resorting to ingress/egress-only analysis. The intrinsic Rp1 ↔ Rp2 degeneracy is alleviated by reparameterizing in (mean Rp, ΔRp) and using emcee for MCMC sampling.

## Papers
- [[2025_Fu_limb-asymmetry]] — used to extract morning and evening limb spectra for all nine hot Jupiters in the JWST/NIRISS/SOSS sample; standard ([[Catwoman]] + emcee + Stagger 3D LDC) workflow. Cross-checked against in-vs-out-of-water-band light-curve residual differences during ingress vs. egress for model-independent visualization.
- [[2025_Murphy_WASP107b]] — Catwoman fits all five JWST visits of WASP-107 b (NIRCam F322W2/F444W, NIRISS/SOSS, NIRSpec G395H, MIRI/LRS) for evening- and morning-limb radii independently; combined with `starry` for an injection-recovery test showing that occulted starspot crossings near ingress vs. egress can flip the polarity of a retrieved limb-asymmetry signal.
