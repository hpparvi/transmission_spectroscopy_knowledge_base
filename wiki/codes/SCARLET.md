---
type: code
aliases: [SCARLET retrieval code, Self-Consistent Atmospheric Retrieval for Exoplanets with Layered Transmissions]
tags: [retrieval-code, frequentist, transmission, atmospheric-retrievals]
---

# SCARLET

A frequentist (χ²-based) exoplanet atmospheric retrieval and model-comparison code (Benneke & Seager 2012, 2013; Benneke et al. 2019; not yet ingested). Uses a self-consistent radiative-transfer forward model with parametric composition, temperature structure, clouds, and (optionally) stellar contamination. Provides model-comparison statistics suitable for frequentist null-hypothesis rejection (σ-significance against flat lines or alternative scenarios). Developed by the Benneke group (Montréal) as a complement to Bayesian approaches like [[POSEIDON]].

## Papers
- [[2025_PiauletGhorayeb_TRAPPIST1d]] — Bayesian retrieval for TRAPPIST-1 d PRISM transmission spectrum; tests H₂-dominated and terrestrial secondary atmosphere scenarios.
- [[2023_Lim_TRAPPIST1b]] — frequentist comparison of H₂-dominated atmosphere models against a flat-line baseline for TRAPPIST-1 b; H₂ at 1× solar rejected at 29σ and at 100× solar at 16σ.
