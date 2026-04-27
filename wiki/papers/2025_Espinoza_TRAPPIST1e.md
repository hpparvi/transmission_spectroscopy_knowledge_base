---
type: paper
bibkey: 2025_Espinoza_TRAPPIST1e
authors: [Espinoza, N., Allen, N. H., Glidden, A., Lewis, N. K., Seager, S., et al.]
year: 2025
venue: ApJL
doi: 10.3847/2041-8213/adf42e
targets: [TRAPPIST-1e]
instruments: [JWST-NIRSpec]
methods: [transmission-spectroscopy, stellar-contamination-modeling, multi-visit-stacking]
codes: [transitspectroscopy, Eureka, ExoTiC-JEDI, juliet]
tags: [trappist-1, habitable-zone, rocky-planet, m-dwarf-host, ultracool-dwarf-host, nirspec-prism, dreams-gto, stellar-contamination, gp-method]
ingested: 2026-04-27
---

# JWST-TST DREAMS: NIRSpec/PRISM Transmission Spectroscopy of the Habitable Zone Planet TRAPPIST-1 e

**Authors:** Espinoza, N., Allen, N. H., Glidden, A., Lewis, N. K., Seager, S., et al. (2025, ApJL 990:L52)
**Targets:** [[TRAPPIST-1e]] · **Instrument:** [[JWST-NIRSpec]] (PRISM, 0.6–5 μm) · **Program:** [[JWST-TST-GTO-1331]]

## TL;DR
The data reduction and stellar contamination analysis companion to [[2025_Glidden_TRAPPIST1e]]. Four JWST NIRSpec PRISM transit observations of TRAPPIST-1 e exhibit similar levels of stellar contamination as seen in other TRAPPIST-1 planets, but the key methodological advance is a Gaussian Process (GP) framework that marginalizes over stellar contamination features rather than requiring an explicit stellar model. This GP approach enables novel atmospheric inferences. The paper demonstrates that current stellar modeling frameworks cannot adequately explain the observed contamination features, but a GP-based marginalization yields a clean atmospheric constraint: cloudy, primary H₂-dominated atmospheres (≥80% by volume) are ruled out at better than 3σ.

## Key findings
- Four PRISM transits obtained: June 22, June 28, July 23, October 28, 2023 (same four visits as [[2025_Glidden_TRAPPIST1e]]).
- All four visits exhibit stellar contamination signatures of varying character: Visit 1 shows the largest white-light transit depth (774+116/-120 ppm deeper than Visit 2, >5σ); this variability is attributed to TRAPPIST-1's evolving heterogeneous photosphere, not instrumental effects — confirmed across all three independent reduction pipelines.
- Visit 3 (July 23) contains a midtransit flare, evidenced by the Hα light curve bump; this also raises the white-light transit depth. Visit 4 (October 28) shows the lowest correlated-noise residual amplitude (σ_GP = 134 ppm).
- **Current stellar atmosphere models cannot explain the contamination features**: PHOENIX models of TRAPPIST-1's M8V photosphere systematically fail to reproduce the wavelength-dependent transit depth variations, particularly at λ < 3 μm.
- **Novel GP marginalization**: applying a GP (celerite, Matèrn 3/2 kernel) to the wavelength-dependent transit depths marginalizes over whatever stellar contamination structure is present without assuming a specific photospheric model.
- **Atmospheric constraint**: cloudy, primary H₂-dominated atmospheres (≥80% by volume) are ruled out at better than **3σ** using the GP-marginalized combined spectrum.
- Companion paper [[2025_Glidden_TRAPPIST1e]] builds on these GP-corrected spectra to provide full secondary-atmosphere constraints (including ruling out H₂-CO₂ at 5σ and thick CO₂ at 6.9σ).

## Methods
Three independent reductions cross-check the robustness of all results: [[transitspectroscopy]] (N. Espinoza 2022; primary), [[Eureka]] (T. Bell et al. 2022; cross-check), and [[ExoTiC-JEDI]] (L. Alderson et al. 2022; cross-check). Light-curve fitting with [[juliet]] (N. Espinoza et al. 2019) using a quadratic limb-darkening law, with limb-darkening coefficients fixed to PHOENIX-predicted values. GP modeled using celerite (D. Foreman-Mackey et al. 2017; not yet ingested) with a Matèrn 3/2 kernel. The GP parameters (amplitude σ_GP and timescale ρ_GP) are fit per visit, with timescales constrained to 5–10 min for visits 1 and 3 and loosely constrained for visits 2 and 4.

## Caveats & limitations
- GP marginalization over stellar contamination adds uncertainty to the final transmission spectrum: the GP inflates error bars relative to a no-GP analysis. The paper explicitly prefers this more conservative approach.
- Visit 3 contains a midtransit flare; its contribution is partly absorbed by the GP but imposes residual correlated structure.
- Stellar model fidelity for TRAPPIST-1 (M8V) remains the bottleneck — the paper demonstrates the *failure* of existing models rather than providing a solution. The GP is a workaround, not a fix.

## Open questions / follow-ups
- Can improved TRAPPIST-1 stellar atmosphere models (below the SPHINX floor at ~2000 K) make the GP marginalization unnecessary?
- Would additional PRISM visits further tighten the H₂-dominated constraint below the 3σ threshold established here?

## Related
- [[2025_Glidden_TRAPPIST1e]] — companion paper; full secondary-atmosphere constraints built on the GP-corrected spectra from this paper.
- [[2025_Rathcke_TRAPPIST1bc]] — alternative stellar-contamination approach for TRAPPIST-1 system using back-to-back empirical correction.
- [[2023_Lim_TRAPPIST1b]] — same system, different instrument (NIRISS/SOSS); comparison context for NIRISS vs NIRSpec contamination amplitudes.
