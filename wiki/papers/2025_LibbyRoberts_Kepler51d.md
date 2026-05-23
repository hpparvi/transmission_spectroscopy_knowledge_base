---
type: paper
bibkey: 2025_LibbyRoberts_Kepler51d
authors: [Libby-Roberts, J. E., Bello-Arufe, A., Berta-Thompson, Z. K., Cañas, C. I., Chachan, Y., Hu, R., Kawashima, Y., Murray, C., Ohno, K., Tokadjian, A., Mahadevan, S., Masuda, K., Hebb, L., Morley, C., Fu, G., Gao, P., Stevenson, K. B.]
year: 2025
venue: arXiv (submitted)
arxiv: 2505.21358
targets: [Kepler-51d]
instruments: [JWST-NIRSpec]
methods: [transmission-spectroscopy, atmospheric-retrievals, stellar-contamination-modeling]
species_tentative: [CH4]
codes: [Eureka, ExoTiC-JEDI, spotrod, SCARLET, POSEIDON, CHIMERA, PICASO, VIRGA, fleck]
tags: [super-puff, low-density, young-system, g-dwarf-host, photochemical-haze, tilted-ring, jwst-go-2571]
ingested: 2026-05-06
---

# The James Webb Space Telescope NIRSpec/PRISM Transmission Spectrum of the Super-Puff, Kepler-51d

**Authors:** Libby-Roberts, Bello-Arufe, Berta-Thompson, Cañas, Chachan, Hu, Kawashima, Murray, Ohno, Tokadjian et al. (2025) · arXiv:2505.21358
**Target:** [[Kepler-51d]] · **Host:** [[Kepler-51]] · **Instrument:** [[JWST-NIRSpec]] (PRISM, 0.6–5.3 μm BOTS)
**Program:** [[JWST-GO-2571]]

## TL;DR

JWST NIRSpec/PRISM transmission spectrum of [[Kepler-51d]] — a 500 Myr [[super-puff]] (M = 5.6 ± 1.2 M⊕, R = 9.32 R⊕, ρ = 0.038 g/cm³) — across 0.6–5.3 μm. The spectrum is **near-featureless but strongly sloped** across the full wavelength range; tentative 2.2σ CH₄ at ppb level (interpretation: upwelling from interior, not bulk abundance). Forward models and retrievals interpret the slope as **a high-altitude photochemical haze layer at 1–100 μbar with sub-micron particles** (tholin/soot/sulfur compositions all viable) atop an extended H/He envelope. **A thin tilted ring of porous submicron particles can also reproduce the slope**, but a simple Pointing–Robertson lifetime argument gives ~0.1 Myr — implausibly short relative to the 500 Myr system age unless a recent collision is invoked. Stellar activity analysis (using a transit-time spot-crossing event) finds a hot-spot with ΔT ∼ 300 K hotter than the photosphere — > 1000 K hotter than typical sunspots — but the spot configuration alone cannot reproduce the observed 0.6–5.3 μm slope. Conclusion: the planet is **most likely an extended H/He atmosphere with substantial high-altitude haze**, with a transient ring as a low-probability alternative.

## Key findings

- **Sloped near-featureless spectrum** from 0.6 to 5.3 μm — a single sloped line is the best non-physical fit; any physical model must reproduce that slope.
- **CH₄ tentative at 2.2σ**, mixing ratio of order ppb (66⁺⁷²⁻⁴⁵ ppb in ExoTR best fit) — interpreted as upwelling from the deeper atmosphere; NOT a bulk abundance probe.
- **Photochemical haze layer at 1–100 μbar** (two orders of magnitude in pressure) reproduces the slope; both forward models and retrievals favor sub-micron monomer sizes; tholin / soot / sulfur compositions all fit equally — composition cannot be discriminated.
- **Tilted-ring alternative**: an optically thin ring of submicron porous particles also reproduces the slope; ruled out as steady-state by Pointing–Robertson lifetime ∼ 0.1 Myr ≪ 500 Myr system age — but cannot be ruled out as a transient post-collision event.
- **Massive opaque ring ruled out** by the slope morphology.
- **Stellar activity**: spot crossing during transit (white-light) yields a wavelength-dependent contrast inconsistent with cold sunspots — the spot is **300 K hotter than the photosphere**, > 1000 K hotter than solar sunspots; a hot spot penumbra or hot+cold spot complex are candidate physical interpretations.
- **Spot/photosphere parameters cannot reproduce the 0.6–5.3 μm slope** at any covering fraction tested → stellar contamination alone is not a viable explanation.
- **Inflated radius** is consistent with a substantial H/He envelope (>30% mass), with the haze layer providing the apparent enlargement.
- **Updates the prior HST/WFC3 result** (Libby-Roberts 2020; not yet ingested) which only saw a featureless spectrum — JWST's wider baseline reveals the slope characteristic.

## Methods

- **Reductions**: [[Eureka]], [[ExoTiC-JEDI]] — independent pipelines.
- **White light-curve + spot**: [[spotrod]] (Béky et al. 2014, transit-with-spot model) and `starry` spherical-harmonic spot model — degeneracy between spot configurations explored via nested sampling (`MultiNest`-class).
- **Spectroscopic light curves**: per-pixel-bin transit fits with second-order polynomial baseline.
- **Retrievals**: [[POSEIDON]], [[CHIMERA]], `ExoTR` — multi-code; haze parameterization included; haze monomer size and base/top pressures retrieved.
- **Forward models**: [[PICASO]] + [[VIRGA]] for cloud/haze condensation; tholin/sulfur/soot Mie opacities.
- **Out-of-transit stellar spectrum** modeled with [[fleck]]-style PHOENIX two-component fits — broadly consistent with in-transit spot constraints but unable to constrain coverage independently.

## Caveats & limitations

- **Sloped continuum cannot uniquely diagnose haze composition** — tholin, sulfur, and hydrocarbon-soot Mie scattering all fit the slope equally well.
- **CH₄ at 2.2σ** is below the canonical 3σ threshold; bulk CH₄ remains unconstrained.
- **The tilted-ring lifetime calculation** is order-of-magnitude (Pointing–Robertson + collisional cascade); a transient post-collision ring remains viable.
- **Spot temperature inversion** (hotter than photosphere) is a non-trivial astrophysical claim — potentially a faculae/penumbra/spot-complex — out-of-transit spectrum cannot independently constrain it.
- **No transmission spectrum constraints from the other Kepler-51 planets yet** — Kepler-51b/c/e need similar JWST observations to test whether the haze hypothesis is universal in this system.
- **HST/WFC3 + JWST-PRISM joint retrieval not performed** — could in principle tighten the slope vs cloud-deck pressure constraints but isn't shown.

## Open questions / follow-ups

- **System-wide [[super-puff]] characterization**: similar JWST observations of Kepler-51 b and c to test whether a high-altitude haze layer is the unifying feature of the system's super-puffs.
- **Haze composition discrimination** via MIRI/LRS or longer-wavelength data, where the sloped Mie continuum may show a transition.
- **Kepler-51d rotation period** of > 33 hr (Lammers & Winn 2024; Liu et al. 2024) implies an unusual angular-momentum history — confirmation via transit-shape ingress/egress timing in higher-S/N data.
- **Confirm the transient-ring scenario** (or rule it out) via repeated transits — a recent collisional event would predict variability.
- **Spot temperature calibration**: an out-of-transit spectrum at higher S/N or multi-epoch monitoring to confirm the hot-spot interpretation vs. a faculae complex.

## Related

- [[2025_Roy_LP791-18c]] — comparable strong photochemical haze on a temperate sub-Neptune.
- [[2025_Jaziri_K2-18b]] — tholin haze used to reconcile K2-18 b NIR/MIR transmission tension.
- HST/WFC3 Kepler-51b/d featureless spectra (Libby-Roberts 2020; not yet ingested) — superseded by this work for Kepler-51d (slope was hidden by the narrow WFC3 baseline).
- Akinsanmi 2020, Piro & Vissapragada 2020 (tilted-ring hypotheses; not ingested).
- Gao & Zhang 2020, Ohno & Tanaka 2021, Wang & Dai 2019, Kawashima 2019 (haze/dusty-outflow hypotheses; not ingested).
