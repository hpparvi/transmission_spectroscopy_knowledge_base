---
type: code
aliases: [Erebus pipeline, FN-PCA pipeline]
tags: [jwst-pipeline, miri, photometric-eclipse, data-reduction]
---

# Erebus

Open-source JWST MIRI eclipse-photometry pipeline introduced in [[2025_Connors_MIRI-15um]] (github.com/nicholasconnors/erebus). Implements **frame-normalized principal component analysis (FN-PCA)** as a data-driven, non-parametric detrending method: each MIRI image frame is normalized by its total intensity before PCA, removing the astrophysical signal (uniform whole-detector flux change) from the input cube; the top 5 principal-component eigenvalue time series serve as systematic regressors. Detrending model F_sys = (1 + Σ c_i λ_i) · (a t + b), fit jointly with `batman` eclipse + `emcee` MCMC. Designed in preparation for the 500 hr JWST Rocky Worlds DDT ([[JWST-DD-9235]]) survey.

## Papers

- [[2025_Connors_MIRI-15um]] — introduces Erebus and FN-PCA; uniformly reanalyzes 17 MIRI F1500W eclipses across five rocky-planet targets.
