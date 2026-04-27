---
type: paper
bibkey: 2025_Teske_TOI561b
authors: [Teske, J. K., Lustig-Yaeger, J., Ih, J., Kempton, E. M.-R., et al.]
year: 2025
venue: ApJL
doi: 10.3847/2041-8213/ae0a4c
targets: [TOI-561b]
instruments: [JWST-NIRSpec]
methods: [secondary-eclipse-spectroscopy, atmospheric-retrievals]
codes: [Eureka, ExoTiC-JEDI, HyDRo, GENESIS]
tags: [super-earth, k-dwarf-host, thick-atmosphere-detection, emission-spectroscopy, usp-planet, cosmic-shoreline, nirspec-g395h, thick-disk-star]
ingested: 2026-04-27
---

# Hints of an Atmosphere on a Rocky Exoplanet: JWST Observations of the Secondary Eclipses of TOI-561 b

**Authors:** Teske, J. K., Lustig-Yaeger, J., Ih, J., Kempton, E. M.-R., et al. (2025, ApJL 995:L39)
**Targets:** [[TOI-561b]] · **Instrument:** [[JWST-NIRSpec]] (G395H, 2.8–5.2 μm) · **Program:** [[JWST-GO-3860]]

## TL;DR
Four secondary eclipses of TOI-561 b — a dense (~4.3 g/cm³) ultra-short-period super-Earth orbiting an ancient (~10 Gyr) thick-disk K dwarf — observed with JWST NIRSpec G395H (May 1–3, 2024; GO 3860). The measured dayside brightness temperature (1800–2150 K) is significantly cooler than predicted for a bare rock (~2950 K), indicating either a high surface albedo or, more compellingly, significant heat redistribution by a substantial atmosphere. This is one of the first confident detections consistent with a thick atmosphere on a rocky exoplanet, and it challenges the cosmic shoreline hypothesis — TOI-561 b lies well above the expected atmosphere-retention boundary but apparently retains volatiles.

## Key findings
- Four secondary eclipses observed consecutively on May 1–3, 2024 (GO 3860, PI: J. Teske); NIRSpec G395H (2.8–5.2 μm), SUB2048, BOTS mode.
- **Dayside brightness temperature: 1800–2150 K** (1σ range); bare-rock prediction ~2950 K assuming zero albedo and no heat redistribution. The ~800–1150 K temperature deficit is inconsistent with a bare rock at >3σ.
- **Two interpretations**: (1) high surface albedo (e.g., a highly reflective silicate surface); or (2) significant atmospheric heat redistribution from dayside to nightside by a thick volatile-rich atmosphere. The authors favor the atmospheric explanation.
- Volatile-rich compositions — including water-dominated, carbon-dominated, and nitrogen-dominated secondary atmospheres — are consistent with the data.
- **Challenges the cosmic shoreline**: TOI-561 b lies well above the predicted atmosphere-retention boundary (extreme XUV flux, short orbital period, low planetary gravity), yet the data suggest atmosphere retention over the ~10 Gyr system lifetime.
- **Thick-disk host**: TOI-561 is a ~10 Gyr, metal-poor ([Fe/H] ≈ −0.4) K dwarf in the Galactic thick disk — among the oldest planet-hosting stars with JWST observations. The ancient host age constrains atmospheric evolution timescales.
- TOI-561 b: Teq ≈ 2300 K, R ≈ 1.45 R⊕, M ≈ 2.24 M⊕, ρ ≈ 4.3 ± 0.4 g/cm³ (Earth-like bulk density); P = 0.446 d (ultra-short-period).
- Individual eclipse depths are consistent across the four visits; the stacked eclipse spectrum shows no strong molecular emission or absorption features, but the overall thermal emission level is low compared to a bare rock.

## Methods
Two independent reductions: [[Eureka]] (T. Bell et al. 2022; primary) and [[ExoTiC-JEDI]] (L. Alderson et al. 2022; cross-check). Atmospheric forward models and retrievals with [[HyDRo]] (S. Gandhi & N. Madhusudhan 2018; A. Piette et al. 2022), specialized for hot rocky planet emission spectra. Self-consistent 1D radiative-convective thermal structure models from [[GENESIS]] (S. Gandhi & N. Madhusudhan 2017, 2020). Surface albedo and atmosphere parameter space explored via grid-based thermal emission modeling.

## Caveats & limitations
- A high surface albedo (e.g., from fresh silicate regolith or surface mineralogy) could in principle explain the low dayside temperature without invoking an atmosphere; the data alone cannot distinguish between these two scenarios.
- Four eclipses provide a stacked spectrum but still limited SNR for compositional constraints — no individual molecular feature is detected.
- Phase-curve observations (not obtained) would directly probe heat redistribution and provide stronger atmospheric evidence.
- The thick-disk stellar age (~10 Gyr) introduces some stellar parameter uncertainties compared to younger solar-type hosts.

## Open questions / follow-ups
- Can a JWST phase curve of TOI-561 b confirm heat redistribution and definitively rule out the high-albedo bare-rock scenario?
- What does the ~10 Gyr age imply for atmosphere replenishment mechanisms — outgassing vs. early delivery — if the atmosphere has survived?
- Does this result revise the placement or interpretation of the cosmic shoreline for dense USP super-Earths?

## Related
- [[2025_Xue_GJ3929b]] — MIRI photometric eclipse of GJ 3929 b; bare rock by comparison; illustrates the contrast with the TOI-561 b detection.
- [[2025_Fisher_TOI1685b]] — NIRSpec G395H multi-visit transmission of TOI-1685 b; flat spectrum + bare rock; USP M-dwarf host; complementary null result for context.
- [[2025_Alam_L168-9b]] — NIRSpec G395H + MIRI/LRS transmission of L 168-9 b; featureless; rocky super-Earth comparison case.
