---
type: paper
bibkey: 2018_Rackham_TLS
authors: [Rackham, B. V., Apai, D., Giampapa, M. S.]
year: 2018
venue: ApJ
arxiv: 1711.05691
doi: 10.3847/1538-4357/aaa08c
targets: [TRAPPIST-1]
instruments: []
methods: [stellar-contamination-modeling]
codes: []
tags: [tls, foundational, m-dwarf-host, methodology, theory, stellar-heterogeneity, transit-light-source-effect]
ingested: 2026-05-04
---

# The Transit Light Source Effect: False Spectral Features and Incorrect Densities for M-dwarf Transiting Planets

**Authors:** Rackham, Apai, Giampapa 2018, ApJ 853:122 · [arXiv:1711.05691]
**Targets:** [[TRAPPIST-1]] (case study) · **Methods:** [[stellar-contamination-modeling]]

## TL;DR
The foundational paper defining and quantifying the transit-light-source-effect (TLSE; see [[stellar-contamination]]) for M-dwarf planet hosts. Builds rotating-photosphere forward models with PHOENIX (M0V–M5V) and DRIFT-PHOENIX (M5V–M9V) component spectra, four heterogeneity cases (giant spots, solar-like spots, each ± faculae), and Monte Carlo over spot placements (100 trials per spectral type per case). Calibrates the relation between observed I-band rotational variability amplitude A and spot covering fraction f_spot to A ∝ f_spot^0.5 — **emphatically not** the linear relation often assumed in the literature. For a typical 1 % I-band variability, mean spot covering fractions for M dwarfs are 8–14 % (solar-like spots) or ~1 % (giant spots) in the spots-only case; faculae double the typical solar-like-spot coverage to ~14 %. The associated stellar contamination spectra (0.3–5.5 μm) for typically active M dwarfs are **1–15× larger than the transit-depth changes expected for atmospheric features in rocky planets** — meaning that, for most M-dwarf rocky-planet observations, TLSE *dominates* the planetary signal at the molecular bands of CH₄, CO, CO₂, H₂O, N₂O, O₂, O₃. For [[TRAPPIST-1]] specifically: f_spot = 8⁺¹⁸⁻⁷ %, f_fac = 54⁺¹⁶⁻⁴⁶ %; TLSE alters JWST transit depths at the wavelengths of interest by **1–15×** the planetary atmospheric feature; biases bulk densities by Δ(ρ) = −8⁺⁷⁻²⁰ % (overestimating volatile content).

## Key findings
- **A ∝ f_spot^0.5 not A ∝ f_spot.** Variability amplitude grows as the square root of spot coverage — a square-root rather than linear scaling — because spots distributed randomly in longitude partly cancel rather than add coherently. Typical previous M-dwarf spot-coverage estimates from photometric monitoring (e.g., Berta et al. 2011; Sing et al. 2011) **underestimate the true spot covering fraction**.
- **Spectral-type independence of contamination scale.** Across M0V–M9V, the *scale* of contamination (measured as average transit-depth change across 0.3–5.5 μm) is largely uniform within each heterogeneity case at fixed variability amplitude — **what differs across spectral types is which features are present**, not how strong the contamination is.
- **Spot-size dependence dominates contamination shape.** Smaller, more numerous "solar-like" spots produce contamination spectra ~10× larger than fewer "giant" spots at the same variability amplitude, because giant spots can produce 1 % variability with f_spot ~1 % whereas solar-like spots require ~10 %.
- **TRAPPIST-1 specific predictions.** Density of TRAPPIST-1 b–h underestimated by 8⁺⁷⁻²⁰ % through stellar contamination; volatile contents inferred from those densities are correspondingly overestimated. JWST transit depths at the 1.0 μm H₂O, 2.5 μm CH₄, 3.3 μm CH₄, 4.3 μm CO₂ bands are biased by 1–15× the planetary atmospheric signature.
- **Faculae can mask atmospheric features.** Pure faculae produce *negative* contamination at near-IR wavelengths (decrease transit depth at facula-emission peaks); when a feature falls at a wavelength where facular emission spectrally exceeds the photosphere, faculae can hide a real atmospheric absorption.
- **Unocculted spots produce broad, mostly positive contamination** that increases transit depth, mimicking absorption features — exactly the slope/false-feature concern raised by [[2014_McCullough_HD189733b]] for HD 189733 b.

## Methods
Iterative spot-placement: starting with an immaculate photosphere, spots (and faculae at 10:1 facula-to-spot area for the spots+faculae cases) are added at random coordinates until reaching specified spot coverage. 180×360-pixel hemispheric grid; double-cosine weighting kernel for limb-darkening. Phase curve over 360° rotation; variability amplitude A = max − min normalized flux. Monte Carlo over 100 model photospheres per (spectral type, heterogeneity case, target spot fraction) configuration to map out the distribution of A vs. f_spot.

Spot temperature relation: T_spot = 0.86 × T_phot (Afram & Berdyugina 2015). Faculae temperature: T_fac = T_phot + 100 K (Gondoin 2008). Contamination spectrum: ε_λ = 1 / (1 − f_het(1 − F_λ,het/F_λ,phot)) for a single-component heterogeneity, generalized to two-component for spots+faculae.

## Caveats & limitations
- **Stellar-axis aligned with sky-plane** assumed (consistent with edge-on transits). Polar spots (common in Doppler imaging of rapidly rotating M dwarfs) would contribute nothing to rotational variability but full TLSE — *underestimating* contamination is possible.
- **Sun-like latitudinal spot distribution** assumed. M-dwarf spots may distribute differently; unocculted spots at high latitudes are not directly probed.
- **PHOENIX/DRIFT-PHOENIX grid limitations** — saturated atomic-line wings, limited accuracy at λ < 1 μm for ultracool dwarfs.
- **Only rotational variability** considered as input — chromospheric activity (Hα, Ca II) provides additional but uncalibrated constraints.
- **No occulted-spot crossings** modeled; this paper handles unocculted contamination only. Joint modeling with occulted-spot signatures (e.g., Pont et al. 2008's chromatic spot crossings) is left to follow-up.

## Open questions / follow-ups
- **Spectral-type dependence of facular emission.** Faculae adopted as T_phot + 100 K everywhere; little observational constraint on M-dwarf facular temperature contrast.
- **TLSE spectral signature library.** This paper reports contamination spectra for M-dwarf rotational variability; analogous library for FGK dwarfs needed (delivered by [[2019_Rackham_TLS-FGK]]).
- **Empirical validation vs. JWST.** Direct test on observed M-dwarf transmission spectra will discriminate between TLSE-dominant and atmospheric interpretations (e.g., [[2023_Lim_TRAPPIST1b]], [[2023_Moran_GJ486b]], [[2023_May_GJ1132b]]).
- **Time variability of TLSE.** If spot patterns evolve over weeks–months, transit-to-transit comparison is itself a TLSE diagnostic — taken up by [[2025_Bennett_GJ1132b]] / [[2025_Rathcke_TRAPPIST1bc]].

## Related
- [[2014_McCullough_HD189733b]] — earliest application of the TLSE concept to a hot-Jupiter K-dwarf system; this paper makes the prediction systematic for the M-dwarf small-planet science case.
- [[2019_Rackham_TLS-FGK]] — companion paper extending the framework to FGK dwarfs; directly applicable to HD 189733 b.
- [[2023_Lim_TRAPPIST1b]] — first JWST detection of strongly TLSE-dominated transmission spectrum on TRAPPIST-1 b; spots in Visit 1, faculae in Visit 2; ~750–1 000 ppm peak-to-peak between visits.
- [[2025_PiauletGhorayeb_TRAPPIST1d]] — applies the Rackham 2018 framework via [[stctm]] to TRAPPIST-1 d.
- [[stctm]] — open-source code (Piaulet 2024) implementing the Rackham 2018 TLSE retrieval as part of the **exotune** framework.
