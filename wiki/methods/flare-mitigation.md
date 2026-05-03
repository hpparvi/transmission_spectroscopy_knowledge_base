---
type: method
aliases: [flare correction, stellar-flare subtraction, flare-template fitting]
tags: [stellar-activity, m-dwarf, methodology, transmission]
---

# Flare mitigation

Subtraction of stellar-flare contamination from JWST near-infrared transmission spectra of M-dwarf rocky planets, where flare signals can exceed expected secondary-atmosphere features by an order of magnitude. Two complementary approaches:

- **Empirical:** subtract a per-integration common-mode + Planck (T_eff(t)) flare-only spectrum extracted directly from the observed flare peak.
- **Physics-based:** fit fiducial [[RADYN]] flare templates (1D non-LTE radiative-hydrodynamics; T_eff-binned) to per-integration flare-only spectra and subtract.

The technique extends the wiki's M-dwarf [[stellar-contamination]] toolbox beyond stable spot/facula modeling and GP marginalization to the **stochastic, per-visit** flare component.

## Trade-offs

- **Strength:** Brings residual transmission noise to ~50–65 ppm on TRAPPIST-1 — sufficient for 3σ injection-recovery of CO₂ features at 150–250 ppm even in flare-contaminated transits.
- **Strength:** Unlike [[back-to-back-transit-correction]], does not require an airless reference planet on the same chord.
- **Limitation:** Validated only for **clearly discernible flare peaks** (~30% of flare time in the TRAPPIST-1 dataset); low-level flaring blended with spots/faculae remains unaddressed.
- **Limitation:** RADYN templates over-predict the Paschen jump at 0.82 μm — model deficiency in the chromospheric transition region.
- **Limitation:** 70% of flare peaks in the test dataset were out-of-transit; in-transit TLS effects from flares not directly tested.
- **Limitation:** Restricted to NIRISS wavelength range (≤2.8 μm) in the introducing paper; G395H / G395M applicability needs separate validation.

## Open issues

- Generalize to sub-detection / blended flares.
- Multi-wavelength simultaneous monitoring (X-ray, UV, mm) to test RADYN flare-counterpart predictions.

## Papers

- [[2025_Howard_TRAPPIST1_flares]] — introduces both empirical and RADYN-based mitigation pipelines on six TRAPPIST-1 flares observed across 11 JWST visits ([[JWST-GO-2589]] and [[JWST-GTO-1201]]); injection-recovery shows 3σ CO₂ feature detection at 150–250 ppm post-mitigation.
