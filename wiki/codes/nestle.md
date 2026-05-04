---
type: code
aliases: [nestle nested sampling]
tags: [nested-sampling, bayesian-inference, retrieval-sampler]
---

# nestle

Pure-Python nested sampling library (Skilling 2004, 2006; Barbary). Used as the Bayesian sampler in retrievals where MCMC samplers like emcee cannot natively handle non-trivial KDE-form priors.

## Papers
- [[2025_Coulombe_TOI-270b]] — chosen over emcee specifically to enable a 2-D KDE-form prior on (f_spot, ΔT_spot) derived from the simultaneous [[TOI-270d]] free-TLS retrieval, when applying it to the joint atmosphere+TLS retrieval of [[TOI-270b]]. This contrasts with Holmberg & Madhusudhan 2024's emcee-based approach, which had to use truncated Gaussians instead of the full KDE.
