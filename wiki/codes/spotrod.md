---
type: code
aliases: [spotrod transit model]
tags: [stellar-contamination, spot-crossing, transit-fitting]
---

# spotrod

Open-source semi-analytic transit-and-spot light-curve model (Béky et al. 2014; not yet ingested), modeling occulted starspots crossed by the planet during transit. Typically paired with nested-sampling or MCMC backends.

## Papers

- [[2026_Heinke_HATP12b]] — fits a possible spot-crossing event ~25 min post-mid-transit in the HAT-P-12 b NIRISS light curve.
- [[2026_Ashtari_HATS75b]] — fits multiple in-transit spot-crossings on HATS-75 b NIRSpec PRISM data with `dynesty`; provides independent spot-temperature estimates that compare against retrieved-from-spectrum values at ~2σ.
- [[2025_Roy_LP791-18c]] — fits a spot-crossing event during the LP 791-18 c NIRSpec PRISM transit alongside a Gaussian-spot model.
