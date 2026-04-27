---
type: method
aliases: [quasi-simultaneous transit correction, anchor-planet correction, transit-pair contamination correction, model-independent contamination correction]
tags: [stellar-heterogeneity, m-dwarf, multi-planet-system, empirical, methodology]
---

# Back-to-back transit correction

A model-independent, epoch-specific correction for [[stellar-contamination]] applicable to multi-planet systems with at least one near-airless reference (anchor) planet. If two planets transit close in time and along similar chords, their transit spectra should differ only in their planetary atmospheric content; the ratio of their wavelength-dependent transit depths therefore captures the planetary signal of the target planet relative to the (assumed flat) reference, with the common stellar-contamination signal cancelling out. Originally proposed by the TRAPPIST-1 JWST Community Initiative (de Wit et al. 2024, Nat. Astron. 8, 810; not yet ingested) and demonstrated as a proof of concept by [[2025_Rathcke_TRAPPIST1bc]].

Distinct from [[stellar-contamination-modeling]], which forward-models or retrieves the heterogeneous-photosphere parameters; here the correction is empirical and does not depend on stellar-spectrum fidelity. The trade-off is added photon noise from the reference transit and the requirement of two suitable transits within the same epoch.

## Practical points
- Requires the reference planet to be airless or have an atmospheric signal much smaller than the contamination amplitude.
- Reference and target should have similar radii and impact parameters so that the chords sample comparable stellar surfaces.
- Performance is wavelength-dependent: at 0.8–2 μm the SNR per visit is high enough to verify the correction directly; at 2–5 μm a single visit is white-noise dominated and verification requires stacked epochs.
- Shifts the dominant noise source from structured red noise to white noise, making the residual challenge a [[multi-visit-stacking]] problem.

## Papers
- [[2025_Rathcke_TRAPPIST1bc]] — proof-of-concept demonstration on the back-to-back JWST/NIRSpec PRISM transits of TRAPPIST-1 b and c (2024 July 9). Achieves a 2.5× red-noise reduction at 0.8–2 μm; argues by analogy that the technique works across the full PRISM range. Establishes that TRAPPIST-1 b and c are interchangeable as anchor planets.
