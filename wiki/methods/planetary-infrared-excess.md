---
type: method
aliases: [PIE, Planetary Infrared Excess, in-eclipse spectrum removal, iESR]
tags: [emission, hot-jupiter, methodology]
---

# Planetary infrared excess

A family of techniques for extracting an exoplanet's thermal emission spectrum from time-series photometry / spectroscopy without relying on imprecise stellar atmosphere models. The dominant variant in the wiki is **in-eclipse spectrum removal (iESR)**, introduced in [[2025_LustigYaeger_WASP17b]]: a back-to-back transit + secondary-eclipse pair separated by less than the host's stellar rotation period is reduced uniformly, and the in-eclipse spectrum is used as an empirical template for the stellar flux. F_day / F_⋆ and F_night / F_⋆ are then formed as simple ratios, sidestepping the ~1.3% PHOENIX-model imprecision floor that otherwise dominates the nightside signal.

iESR-PIE is contrasted with — and complementary to — standard [[secondary-eclipse-spectroscopy]], which subtracts a model stellar spectrum.

## Variants

- **iESR (in-eclipse spectrum removal)** — uses the in-eclipse spectrum from the same epoch as the empirical stellar template. Requires temporal stability between the transit and eclipse observations (i.e., stellar rotation period ≫ separation).

## Trade-offs

- **Strength:** Bypasses the ~1.3% stellar-model imprecision floor that limits standard emission retrievals.
- **Strength:** Yields nightside spectra not otherwise accessible from a single-epoch dataset.
- **Limitation:** Only works when transit and eclipse are observed within a stellar rotation period and instrumental systematics are stable. iESR has failed on NIRISS/SOSS (zeroth-order contamination, position-angle changes between transit and eclipse) and MIRI/LRS (long temporal ramps) in [[2025_LustigYaeger_WASP17b]] tests.
- **Limitation:** Active stars degrade the method (cf. HAT-P-26 b null result, Sotzen 2025; not yet ingested).

## Papers

- [[2025_LustigYaeger_WASP17b]] — introduces iESR-PIE on JWST NIRSpec G395H; first JWST nightside emission spectrum of WASP-17 b; tentative SO₂, CH₄, H₂O, CO₂.
