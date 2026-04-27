---
type: paper
bibkey: 2025_Fisher_TOI1685b
authors: [Fisher, C. E., Hooton, M. J., Gressier, A., Zgraggen, M., Tian, M., Heng, K., et al.]
year: 2025
venue: MNRAS
arxiv: 2512.15338
targets: [TOI-1685b]
instruments: [JWST-NIRSpec]
methods: [transmission-spectroscopy, atmospheric-retrievals, multi-visit-stacking, stellar-contamination-modeling]
species_ruled_out: [CO2, SO2, H2O]
codes: [Eureka, ExoTiC-JEDI, transitspectroscopy, juliet]
tags: [super-earth, m-dwarf-host, bare-rock, nirspec-g395h, multi-visit]
ingested: 2026-04-27
---

# JWST NIRSpec Finds No Clear Signs of an Atmosphere on TOI-1685 b

**Authors:** Fisher, C. E., Hooton, M. J., Gressier, A., et al. (2025, MNRAS, arXiv:2512.15338)
**Targets:** [[TOI-1685b]] · **Instrument:** [[JWST-NIRSpec]] (G395H, 2.67–5.17 μm) · **Program:** [[JWST-GO-4195]]

## TL;DR
Five JWST NIRSpec G395H transits of the hot super-Earth TOI-1685 b (Teq ≈ 1062 K, M2.5V host) — four new from GO 4195 plus one reanalyzed from the Luque et al. 2025 phase curve (GO 3263; not yet ingested) — yield a flat transmission spectrum with no atmospheric signatures. Bayesian evidence favors a flat-line model; H₂-dominated atmospheres are confidently ruled out; secondary atmospheres constrained to MMW ≳ 10 at ~5σ. Pure CO₂, SO₂, H₂O, and CH₄ secondary atmospheres cannot explain the data (though pure CH₄ may be physically unlikely). TOI-1685 b is likely a bare rock.

## Key findings
- Five total transits: four from GO 4195 (2024 Feb 25, Feb 29, Mar 2, Sep 1; PI: C. Fisher) plus one trimmed transit from the GO 3263 phase curve (2024 Feb 15; PI: Luque); observations in BOTS mode using F290LP + G395H, SUB2048, 16 groups/integration, 264 min visit duration.
- The fourth visit (Sep 1, 2024) was originally scheduled shortly after the other three but delayed a few months until TOI-1685 became JWST-observable again.
- **Flat transmission spectrum**: Bayesian evidence favors a simple flat-line model; no molecular feature detected.
- H₂-dominated atmospheres confidently ruled out.
- **MMW ≳ 10 at ~5σ**: secondary atmospheres with mean molecular weight below ~10 can be excluded.
- Pure [[CO2]], [[SO2]], and mixed secondary atmospheres (CO + CO₂ + SO₂) can explain the data (Δ ln Z < 3) but are physically disfavored or ruled out by individual molecular constraints.
- Pure [[H2O]] and CO₂ cases require a high-altitude cloud — physically unlikely.
- Pure CH₄ is physically unlikely as a secondary atmosphere.
- The single-transit phase-curve result (Luque et al. 2025; not yet ingested) also ruled out H₂-dominated atmospheres but lacked the SNR to constrain secondary atmospheres — the five-visit stacking here provides the needed sensitivity.
- Sep 1 visit shows quasi-sinusoidal variations (~200 ppm, 40 min period) in both detectors, modeled as a GP; attributed to instrumental or stellar granulation systematics, not a planetary signal.

## Methods
Three independent reduction methodologies: (1) [[Eureka]] (T. Bell et al. 2022; primary), (2) [[ExoTiC-JEDI]] (L. Alderson et al. 2022), (3) [[transitspectroscopy]] (N. Espinoza 2022). Light-curve fitting with [[juliet]] (N. Espinoza et al. 2019), incorporating Gaussian Processes (celerite, Matèrn 3/2 kernel + simple harmonic oscillator) for time-correlated noise. Limb-darkening priors from MPS-ATLAS-1 stellar models (Kostogryz et al. 2022; not yet ingested), implemented via ExoTiC-LD. Nested sampling via dynesty (Speagle 2020; not yet ingested). Atmospheric retrievals with BeAR code (ETH Zurich / Kitzmann group; not yet ingested). Planet and stellar parameters adopted from Burt et al. 2024 (not yet ingested).

## Caveats & limitations
- The Sep 1 visit's quasi-sinusoidal 200 ppm signal is modeled as noise but is the only strong periodicity across all five visits; if stellar, it could bias interpretation.
- BeAR retrieval code not yet in wiki (prose-only citation).
- Phase curve by Luque et al. 2025 (GO 3263; not yet ingested) is the companion context paper; its emission spectrum is consistent with a blackbody / bare-rock and no heat redistribution.

## Open questions / follow-ups
- Will additional visits further tighten the secondary-atmosphere MMW constraint below 10?
- What does the Luque et al. 2025 emission spectrum imply for the atmosphere-vs-no-atmosphere picture jointly with this transmission result?

## Related
- [[2025_Alderson_TOI-776b]] — similar flat-spectrum result with NIRSpec G395H multi-visit stacking for another M-dwarf super-Earth.
- [[2024_Scarsdale_L98-59c]] — COMPASS multi-visit approach; similar MMW limit context.
