---
type: method
aliases: [atmospheric retrieval, spectral retrieval, Bayesian retrieval]
tags: [bayesian, inverse-problem, core-method]
---

# Atmospheric retrievals

Bayesian inversion of an exoplanet [[transmission-spectrum]] (or emission spectrum) to recover posterior distributions over composition, temperature structure, cloud properties, and (optionally) [[stellar-contamination]] parameters. A forward model maps parameters → spectrum; a sampler (nested sampling or MCMC) explores the posterior. Model comparison via Bayes factors quantifies support for specific species or scenarios.

## Papers
- [[2025_Teske_TOI561b]] — [[HyDRo]] + [[GENESIS]] emission retrievals on TOI-561 b secondary eclipses; volatile-rich secondary atmospheres fit the depressed dayside temperature; bare-rock high-albedo scenario cannot be excluded.
- [[2025_Fisher_TOI1685b]] — BeAR nested-sampling retrievals; MMW ≳ 10 at ~5σ from the flat NIRSpec G395H transmission spectrum of TOI-1685 b.
- [[2025_PiauletGhorayeb_TRAPPIST1d]] — [[SCARLET]] retrievals on TRAPPIST-1 d PRISM spectrum; H₂-dominated and cloud-free terrestrial scenarios excluded.
- [[2025_Glidden_TRAPPIST1e]] — [[petitRADTRANS]] forward models for H₂-CO₂, pure CO₂, N₂-CO₂, N₂-only, and N₂+CH₄ scenarios; μ > 8.6 u; thick CO₂ ruled out at 6.9σ; N₂-rich atmospheres consistent.
- [[2023_Lim_TRAPPIST1b]] — [[SCARLET]] frequentist + [[POSEIDON]] joint stellar-contamination+atmosphere retrieval on TRAPPIST-1 b; H₂ < 52% at 3σ; secondary atmosphere composition unconstrained.
- [[2025_Teske_TOI776c]] — [[PICASO]] physical-model retrievals (metallicity × opaque pressure via UltraNest) on TOI-776 c; rules out metallicity < 180–240× solar; highlights that MMW inferences from featureless spectra are strongly model dependent (equilibrium vs. mixture models span 2.8–7.7 g mol⁻¹).
- [[2025_Redai_GJ357b]] — free-chemistry and equilibrium retrievals on GJ 357 b NIRSpec G395H; featureless spectrum constrains MMW > 8 g/mol and metallicity > 300–500× solar.
- [[2024_Gressier_L98-59d]] — TauREx3 + exoretrievals (free chemistry + equilibrium chemistry) on L 98-59 d; detects atmospheric absorption at 2.6σ–5.6σ with [[H2S]] as the dominant opacity source.
- [[2024_Banerjee_L98-59d]] — NEMESISPY CLR-prior retrievals on the same L 98-59 d transit; stellar + atmosphere scenario preferred, log X([[H2S]]) ≈ −0.62, log X([[SO2]]) ≈ −2.35.
- [[2023_May_GJ1132b]] — [[POSEIDON]] retrievals on GJ 1132 b transit spectra; direct comparison of atmosphere vs unocculted-starspot scenarios with equal Bayesian evidence.
- [[2023_Moran_GJ486b]] — [[POSEIDON]] 6-gas + rfast 1-gas retrievals on GJ 486 b transmission spectrum; H₂O-rich atmosphere and unocculted-starspot scenarios both fit at χ²ν ≈ 1.0.
- [[2023_Lustig-Yaeger_LHS475b]] — 5-component Bayesian retrievals (H₂O, CO₂, CH₄, CO + inactive bulk) on LHS 475 b; maps atmospheric MMW / scale-height / apparent-surface-pressure posteriors given the featureless spectrum.
