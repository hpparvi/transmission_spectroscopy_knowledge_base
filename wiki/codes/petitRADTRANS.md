---
type: code
aliases: [pRT, petitRADTRANS retrieval code]
tags: [radiative-transfer, retrieval-code, forward-model, transmission, emission, hub]
---

# petitRADTRANS

An open-source radiative-transfer and atmospheric retrieval code for exoplanet atmospheres (Mollière et al. 2019; not yet ingested). Computes transmission and emission spectra for user-defined pressure–temperature profiles and chemical compositions using line-by-line (R ~ 10⁶) or correlated-k (R ~ 1000) opacity tables. By the JWST era it has emerged as the most flexible "Lego-style" radiative-transfer toolkit in the wiki — used as a forward-model engine for self-consistent grids ([[2025_Crossfield_SO2shoreline]]), as an emission-spectrum retrieval engine ([[2025_Sikora_HD80606b]]), as the atmosphere half of joint interior–atmosphere retrievals ([[2025_AcunaAguirre_WASP80b]]), and as a reference cross-check against [[POSEIDON]] / [[CHIMERA]] / [[ATMO]] / [[Aurora]] for transmission retrievals.

## Variants

The wiki sees four recurring petitRADTRANS deployment patterns:

- **Stand-alone retrieval engine.** [[2025_Ahrer_KELT7b]] runs pRT v3.1 with both free chemistry (4-parameter T-P + PyMultiNest 500 live points) and equilibrium chemistry from [[easyCHEM]] tabulated grids on KELT-7 b NIRSpec G395H — cross-checked against POSEIDON, equilibrium chemistry preferred at Δ ln Z = 1.6–3.1.
- **Forward-model engine within a self-consistent grid.** [[2025_Crossfield_SO2shoreline]] couples [[HELIOS]] (T-P), [[VULCAN]] (photochemistry), and pRT (synthetic spectra at R = 30,000 with 21 species) for the 936-model SO₂-shoreline grid — pRT is the radiative-transfer back-end, not the retrieval driver.
- **Forward models for ruling-out atmospheric scenarios.** [[2025_Glidden_TRAPPIST1e]] computes pRT forward models for five candidate atmospheres (H₂-CO₂, pure CO₂, N₂-CO₂, N₂-only, N₂+CH₄) on TRAPPIST-1 e featureless PRISM spectra; used to derive μ > 8.6 u and 5–6.9σ thick-CO₂ rejections.
- **Emission-spectrum retrieval coupled with [[easyCHEM]].** [[2025_Sikora_HD80606b]] runs pRT + easyCHEM at 10 phases of the HD 80606 b NIRSpec G395H partial phase curve (Guillot 2010 4-parameter T-P, gray cloud deck, emcee 16 walkers × 10⁵ steps); chemical-equilibrium retrievals preferred over [[PyratBay]] free chemistry post-periapse. Same pattern in [[2025_Crouzet_HATP12b]] (pRT + [[VULCAN]] photochemistry on HAT-P-12 b).
- **Atmosphere half of joint interior–atmosphere retrieval.** [[2025_AcunaAguirre_WASP80b]] couples [[GASTLI]] (interior, 2-layer core + envelope) with pRT v3.0 (atmosphere; Guillot 2010 P-T, easyCHEM equilibrium chemistry, 5-parameter cloud) under a single Bayesian likelihood — the wiki's first [[joint-interior-atmosphere-retrieval]].
- **Cross-target model spectra for population studies.** [[2025_Gordon_COMPASS-G395H]] uses pRT for cross-target model spectra in the COMPASS uniform reanalysis of seven NIRSpec G395H spectra.

## History

- **2019** — pRT introduced (Mollière et al. 2019); rapid uptake on hot-Jupiter retrievals.
- **2024** — emerges in the wiki via [[2025_AcunaAguirre_WASP80b]] (submitted late 2025) and [[2025_Sikora_HD80606b]] for hot-Jupiter emission/transmission retrievals.
- **2025** — application broadens to (i) population-level theoretical grids ([[2025_Crossfield_SO2shoreline]]), (ii) rocky-planet null-test forward models ([[2025_Glidden_TRAPPIST1e]]), (iii) joint interior-atmosphere retrievals ([[2025_AcunaAguirre_WASP80b]]), (iv) hot-Jupiter cross-checks against POSEIDON/CHIMERA ([[2025_Ahrer_KELT7b]]).

## Trade-offs

- **Strength: modular and easy to couple.** The "Lego-style" architecture allows pRT to slot into self-consistent grids ([[2025_Crossfield_SO2shoreline]]) and joint interior-atmosphere likelihoods ([[2025_AcunaAguirre_WASP80b]]) without code modifications upstream.
- **Strength: dual-precision opacity (correlated-k + line-by-line).** Correlated-k for retrievals where speed matters (~1000–10000 model evaluations per dim per nested-sampling step); line-by-line for forward-model grids and high-resolution validation.
- **Strength: easyCHEM coupling.** Equilibrium-chemistry retrievals straightforward; the [[easyCHEM]] tabulation is the standard upstream chemistry.
- **Limitation: no native limb-asymmetry support.** 1D plane-parallel; cannot directly retrieve evening-vs-morning chemistry differences ([[limb-asymmetry]]). Comparable to [[CHIMERA]] / [[POSEIDON]] in this respect; [[Catwoman]] + pRT is the workaround for transit-light-curve-driven limb-resolved spectra.
- **Limitation: stellar-contamination handling external.** pRT on its own does not parameterize unocculted starspots/faculae; downstream codes ([[POSEIDON]] with TLS module, [[stctm]]) handle this.
- **Limitation: emission retrieval framework not fully exposed in the standalone API.** Emission retrievals as in [[2025_Sikora_HD80606b]] required custom wrapper code coupling pRT to emcee.

## Open issues

- **Free-chemistry vs. equilibrium-chemistry preference is target-dependent.** [[2025_Ahrer_KELT7b]] prefers equilibrium chemistry on KELT-7 b at Δ ln Z = 1.6–3.1; [[2025_Sikora_HD80606b]] reports the chemical-equilibrium retrieval gives higher Bayesian evidence than [[PyratBay]] free chemistry on HD 80606 b post-periapse. No general rule; per-target Bayesian model comparison required.
- **Cloud-parameter degeneracies.** Gray cloud decks in [[2025_Sikora_HD80606b]] / [[2025_Ahrer_KELT7b]] are functionally identical; more elaborate cloud parameterizations (5-parameter Pinhas, Mie-scattering tholins) increase posterior dimensionality faster than data constrains.

## Papers

### Hot Jupiter / Neptune-mass — primary or cross-check
- [[2025_Ahrer_KELT7b]] — pRT v3.1 free + equilibrium chemistry on KELT-7 b NIRSpec G395H; cross-check vs POSEIDON; equilibrium preferred at Δ ln Z = 1.6–3.1.
- [[2025_Sikora_HD80606b]] — pRT + [[easyCHEM]] emission retrievals at 10 phases of the HD 80606 b NIRSpec G395H partial phase curve; equilibrium chemistry preferred over PyratBay free chemistry.
- [[2025_AcunaAguirre_WASP80b]] — pRT v3.0 atmosphere half of [[joint-interior-atmosphere-retrieval]] coupled with [[GASTLI]] interior on WASP-80 b transmission + emission.
- [[2025_Crouzet_HATP12b]] — synthetic spectra coupled with VULCAN photochemistry for HAT-P-12 b NIRSpec G395M analysis.

### Population-level / population-scale forward modeling
- [[2025_Crossfield_SO2shoreline]] — pRT R=30,000 synthetic spectra in the 936-model SO₂-shoreline grid; couples downstream of HELIOS + VULCAN.
- [[2025_Gordon_COMPASS-G395H]] — pRT for cross-target model spectra in the COMPASS uniform reanalysis of seven NIRSpec G395H spectra.

### Rocky-planet null-test forward models
- [[2025_Glidden_TRAPPIST1e]] — pRT forward models for five candidate atmospheres on TRAPPIST-1 e PRISM; H₂-rich (5σ) and thick CO₂ (6.9σ) rejected; μ > 8.6 u; N₂-rich consistent.
