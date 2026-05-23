---
type: code
aliases: [SPARTA pipeline, Simple Planetary Atmosphere Reduction Tool for Anyone]
tags: [jwst-pipeline, data-reduction, time-series, miri-lrs, nirspec, hub]
---

# SPARTA

An independent JWST time-series reduction pipeline (Kempton et al. 2023; not yet ingested), designed from scratch **without dependency on the STScI `jwst` pipeline**. Provides nonlinearity correction, dark subtraction, gain multiplication, up-the-ramp fitting with outlier rejection, background subtraction, and optimal extraction directly from raw `_uncal` files. The wiki's canonical role for SPARTA is **MIRI/LRS secondary-eclipse + photometric-eclipse cross-check**, where independence from the STScI pipeline serves as a guard against shared systematics; secondary roles include MIRI F1500W imaging mode and NIRSpec G395H cross-check.

## Variants

The wiki sees three SPARTA modes:

- **MIRI/LRS slitless eclipse spectroscopy.** The dominant role: 4 of 7 ingested papers. SPARTA primary, Eureka! cross-check is the standard pairing for secondary-eclipse depths on rocky M-dwarf planets ([[2024_Xue_GJ1132b]], [[2024_WeinerMansfield_GJ486b]], [[2024_Wachiraphan_LTT1445Ab]], [[2026_Coy_HD3167b]]) — agreement within 1σ on broadband eclipse depths is the standard validation criterion (e.g. 133.3 ± 5.0 ppm SPARTA / 133.7 ± 6.6 ppm Eureka! on Gl 486 b).
- **MIRI F1500W photometric imaging eclipses.** [[2025_Xue_GJ3929b]] uses an updated SPARTA for the MIRI imaging-mode time series on GJ 3929 b — first wiki use of SPARTA outside slitless spectroscopy. F1500W eclipse photometry is a Hot Rocks Survey staple ([[JWST-GO-3730]]) and the [[Erebus]] / [[Pegasus]] / SPARTA triumvirate now serves as the F1500W cross-check ecosystem.
- **NIRSpec G395H transmission cross-check.** [[2025_Barat_V1298Tau-b]] uses SPARTA on the V1298 Tau b NIRSpec G395H/SUB2048 transit; agrees with Eureka! within 1σ on retrieved abundances but shows ~25% higher scatter on NRS2 — under development for NIRSpec. [[2025_Deka_WASP39b]] uses SPARTA as one of three reductions (Eureka, Tiberius, SPARTA) on WASP-39 b MIRI data within the [[NEXOTRANS]] benchmark.

## History

- **2023** — SPARTA introduced (Kempton et al. 2023); rapid uptake on MIRI/LRS rocky-planet eclipses where independence from STScI pipeline is critical.
- **2024** — three back-to-back rocky-planet MIRI/LRS papers ([[2024_Xue_GJ1132b]], [[2024_WeinerMansfield_GJ486b]], [[2024_Wachiraphan_LTT1445Ab]]) standardize SPARTA-as-primary-with-Eureka-cross-check on rocky-planet eclipses.
- **2025** — extension to MIRI F1500W imaging mode ([[2025_Xue_GJ3929b]]) and NIRSpec G395H ([[2025_Barat_V1298Tau-b]]). NIRSpec mode under development with documented ~25% NRS2 scatter penalty.
- **2026** — [[2026_Coy_HD3167b]] uses SPARTA primary + Eureka! + exoTEDRF as a three-way cross-check on the LAVA LAMPS ([[JWST-GO-4818]]) HD 3167 b eclipse — first wiki LAVA LAMPS paper validating the SPARTA framework against two competing pipelines.

## Trade-offs

- **Strength: STScI-pipeline independence.** SPARTA reads `_uncal` files directly; Eureka! and most other pipelines wrap STScI stages 1–2. Shared systematics in those upstream stages cannot affect SPARTA — the value proposition for cross-validation.
- **Strength: MIRI/LRS specialization.** Optimized for the MIRI detector noise regime; consistent agreement with Eureka! on broadband depths supports the pipeline's correctness.
- **Limitation: NIRSpec mode immature.** [[2025_Barat_V1298Tau-b]] flags ~25% higher NRS2 scatter than Eureka!; treated as "under development." Not yet recommended as primary on NIRSpec G395H.
- **Limitation: limited light-curve fitting / spectroscopic infrastructure.** SPARTA stops at extracted spectra; downstream binning and light-curve fitting typically use external tools ([[juliet]], custom MCMC). [[Eureka]] integrates these stages internally.
- **Limitation: less battle-tested across cycles.** Eureka! has 28 wiki papers; SPARTA has 7. New target classes (NIRSpec PRISM rocky-planet hosts, MIRI/LRS phase curves) may surface untested edge cases.

## Open issues

- **NIRSpec mode reliability.** The Barat 2025 ~25% scatter issue on NRS2 is unresolved; until SPARTA NIRSpec matches Eureka! detector-by-detector, NIRSpec-primary use is gated.
- **Comparison against Erebus / Pegasus on MIRI F1500W.** [[2025_Connors_MIRI-15um]] uses Erebus across a 17-eclipse MIRI F1500W reanalysis; direct head-to-head with SPARTA F1500W has not been published.

## Papers

### MIRI/LRS rocky-planet secondary eclipses (primary reduction)
- [[2026_Coy_HD3167b]] — primary on HD 3167 b LAVA LAMPS eclipse; three-way cross-check vs Eureka! and [[exoTEDRF]]; eclipse 38 ± 11 ppm vs 104 ± 3 ppm bare-rock (≈5σ deficit).
- [[2024_Xue_GJ1132b]] — primary on GJ 1132 b GTO 1274 eclipse; Eureka cross-check; T_day = 709 ± 31 K, R = 0.95 ± 0.04, bare-rock consistent.
- [[2024_WeinerMansfield_GJ486b]] — primary on Gl 486 b two MIRI/LRS eclipses; Eureka cross-check; broadband 133.3 ± 5.0 ppm; rules out water-rich atmosphere from [[2023_Moran_GJ486b]] transmission.
- [[2024_Wachiraphan_LTT1445Ab]] — parallel reduction alongside Eureka on LTT 1445 A b three eclipses; T_day = 525 K; thick CO₂ excluded at >6σ.

### MIRI F1500W imaging mode
- [[2025_Xue_GJ3929b]] — primary reduction (updated for MIRI imaging mode) on GJ 3929 b two F1500W eclipses; T_day = 782 ± 79 K; bare-rock; CO₂ > 100 mbar excluded.

### NIRSpec G395H cross-check
- [[2025_Barat_V1298Tau-b]] — independent G395H pipeline cross-check on V1298 Tau b; agrees with Eureka! on abundances within 1σ; ~25% higher NRS2 scatter (under development).
- [[2025_Deka_WASP39b]] — one of three reductions (Eureka, Tiberius, SPARTA) cross-compared on WASP-39 b MIRI data within the [[NEXOTRANS]] retrieval-framework benchmark.

### NIRSpec G395H + MIRI/LRS panchromatic (sub-Neptune)
- [[2025_Luque_K2-18b]] — SPARTA used as one of four reductions on K2-18 b panchromatic spectrum (alongside JExoRES, exoTEDRF, Eureka!). NIRSpec G395H R = 200 spectroscopic light curves with detector positional + linear-in-time systematics. MIRI/LRS reduction with exponential ramp + linear trend systematics; first wiki use of SPARTA for sub-Neptune-temperature MIRI transit.
