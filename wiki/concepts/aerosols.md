---
type: concept
aliases: [haze, hazes, clouds, condensates, dust, aerosol]
tags: [transmission-spectroscopy, hot-jupiter, opacity, terminator]
---

# Aerosols

Suspended particulates — clouds, hazes, condensate grains, photochemical soots — that contribute continuum opacity to a [[transmission-spectrum]] without producing the discrete bands characteristic of gas-phase molecular absorption. The Pont 2008 footnote articulates the operational distinction: "*we make no fundamental distinction between clouds and haze, which differ only by their opacity*"; both are submicrometre-to-micrometre suspended particles and their transmission-spectrum signatures (transit-radius enhancement, slope, feature muting) are equivalent. The dominant continuum-opacity source for cool gas giants and many sub-Neptunes; the leading confounder of [[atmospheric-retrievals]] for low-significance feature detection.

## Signatures in transmission spectra

- **Featureless slope** — uniform absorbing/scattering particles produce a smooth continuum that flattens the relative amplitudes of expected molecular features. The flatness of the [[2008_Pont_HD189733b]] visible spectrum is the canonical example.
- **Rayleigh-like blueward slope** (σ ∝ λ⁻⁴) — submicrometre grains scatter blue more efficiently than red; the [[2013_Pont_HD189733b]] panchromatic slope spans 5+ scale heights at T ~ 1300 K with this dependence.
- **Visible/near-IR opacity gap** — large grains opaque in the visible can be transparent in the IR (Venus, Titan); the IR/visible offset of HD 189733 b first highlighted this in an exoplanet context.
- **Antigreenhouse temperature inversion** — visible-light absorption by dust above the IR photosphere produces an inverted T–P profile distinct from the TiO/VO mechanism; modeled for HD 189733 b in [[2013_Pont_HD189733b]] (γ ≈ 10, ξ ≈ 0.1 in the Heng et al. 2012 framework).
- **Limb-only signatures.** The [[limb-asymmetry]] population reveals chemical heterogeneity between morning and evening terminators — including aerosol heterogeneity. [[2025_Murphy_WASP107b]] resolves a broad 6–11 μm cloud feature as **morning-only** on WASP-107 b.

## Confounding with stellar contamination

[[2014_McCullough_HD189733b]] showed that the same Rayleigh-like slope attributed to dust on HD 189733 b can be quantitatively reproduced by **unocculted starspot contamination** — see [[stellar-contamination]] and the [[HD-189733b]] hub `## Tensions`. [[2019_Rackham_TLS-FGK]] generalized this: K-dwarf [[stellar-contamination]] (the transit-light-source-effect) generically produces visible blueward slopes at the magnitude observed for HD 189733 b. The dust-vs-TLS adjudication is target-specific and remains an open methodology question for any active-K-dwarf hot-Jupiter retrieval.

## Composition candidates (hot Jupiters, T ~ 1000–1500 K)

Silicates: enstatite (MgSiO₃), forsterite (Mg₂SiO₄). Other condensates: corundum (Al₂O₃), iron, MnS, Cr, Na₂S, KCl, Zn, C. Photochemical: tholins, hydrocarbon soots, polycyclic aromatics. Most observational constraints fail to discriminate between these — the data motivate continuum opacity rather than specific composition.

## Sub-Neptune connection

Cool sub-Neptunes routinely show muted features attributed to high-altitude photochemical hazes; [[2025_Roy_LP791-18c]] reports a 5.4σ haze + CH₄ detection on the temperate sub-Neptune LP 791-18 c, in contrast with the K2-18 b / TOI-270 d pair. [[2025_Jaziri_K2-18b]] models photochemical (tholin) hazes as a way to reconcile the K2-18 b NIRISS+G395H amplitude tension with MIRI/LRS — included at Bayes factor 5.53. The [[sub-neptune-classification]] scheme implicitly assumes haze-corrected transmission for type assignment.

## Papers

- [[2025_Murphy_WASP107b]] — first wiki paper resolving cloud heterogeneity between morning/evening limbs on a single target; broad 6–11 μm feature isolated to the morning limb.
- [[2025_Roy_LP791-18c]] — strong (5.4σ) photochemical haze on a temperate sub-Neptune.
- [[2025_Jaziri_K2-18b]] — tholin haze opacity reconciles K2-18 b NIR/MIR transmission tension at lnB = 5.53.
- [[2014_McCullough_HD189733b]] — proposes that the HD 189733 b "haze" slope may be unocculted starspot contamination instead.
- [[2013_Pont_HD189733b]] — panchromatic 0.3–24 μm dust scenario with first-order grain-physics modeling (Rayleigh slope + settling + cloud deck).
- [[2008_Pont_HD189733b]] — first conclusive aerosol claim in an exoplanet atmosphere.
