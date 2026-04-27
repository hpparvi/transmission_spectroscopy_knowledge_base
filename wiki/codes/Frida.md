---
type: code
aliases: [Frida pipeline]
tags: [jwst-pipeline, data-reduction, time-series, nirspec-prism]
---

# Frida

A custom JWST time-series reduction pipeline (Rathcke et al. 2025) developed independently of `Eureka!` and the STScI `jwst` pipeline. Frida uses only stage-1 of `jwst` for ramp-level processing; from stage 2 onward it is fully independent. Distinguishing features: column-wise saturation masking, group-level preamplifier reset-noise removal, column-wise 1/f noise correction, group-difference rate calculation (preferred over up-the-ramp fitting at low group counts), 5σ time-series cosmic-ray identification at the pixel level, and optimal extraction with a smoothed-median PSF weight.

## Papers
- [[2025_Rathcke_TRAPPIST1bc]] — primary reduction for the back-to-back JWST/NIRSpec PRISM transits of TRAPPIST-1 b and c. Authors note Frida's group-difference rate is more robust than `jwst` ramp-fitting when integrations contain only a few groups.
