---
type: method
aliases: [multi-visit coadding, transit stacking, coadded transmission spectrum, leave-one-out transit analysis]
tags: [multi-visit, small-planet, rocky-planet, detection-discriminator]
---

# Multi-visit stacking

Weighted combination of multiple transit visits of the same target into a single higher-SNR [[transmission-spectrum]], typically paired with a **leave-one-out** diagnostic that drops each visit in turn to check that any apparent feature is not visit-specific. Essential for rocky M-dwarf planets where per-visit SNR barely reaches the expected atmospheric-feature amplitude and where visit-specific [[stellar-contamination]] can otherwise masquerade as atmospheric structure. Contrast with single-visit [[transmission-spectroscopy]], where the absence of a repeatability check leaves noise-draw and spot-evolution hypotheses unconstrained.

## Papers
- [[2025_Fisher_TOI1685b]] — five NIRSpec G395H transits of TOI-1685 b (four new + one from Luque et al. 2025 phase curve); stacked flat spectrum; MMW ≳ 10 at ~5σ; Sep 1 visit shows quasi-sinusoidal 200 ppm systematics modeled with GP.
- [[2025_Espinoza_TRAPPIST1e]] — four NIRSpec PRISM transits of TRAPPIST-1 e with GP marginalization over stellar contamination across all four visits; demonstrates per-visit stellar variability at >5σ amplitude differences in white-light depth.
- [[2025_PiauletGhorayeb_TRAPPIST1d]] — two NIRSpec PRISM transits of TRAPPIST-1 d; flat ±100–150 ppm; insufficient visits to constrain N₂-dominated secondary atmospheres.
- [[2025_Glidden_TRAPPIST1e]] — four-visit NIRSpec PRISM transmission spectroscopy of TRAPPIST-1 e; visits 3 and 4 stellar-activity-contaminated; GP-corrected four-visit combined spectrum used for μ > 8.6 u MMW constraint.
- [[2023_Lim_TRAPPIST1b]] — two NIRISS/SOSS transits of TRAPPIST-1 b; dominant stellar-contamination variation between visits (spots vs. faculae) illustrates the challenge of combining visits on active stars without contamination correction.
- [[2025_Teske_TOI776c]] — two-visit joint fit (Eureka!) and weighted average (Tiberius) of TOI-776 c; visit-to-visit NRS1 offset ambiguous (ΔlnZ = 12 for Tiberius visit 1, ΔlnZ = 1 for Eureka! visit 2); combined-spectrum atmospheric conclusions unchanged regardless of offset treatment.
- [[2025_Rathcke_TRAPPIST1bc]] — motivates stacking as the natural follow-up to [[back-to-back-transit-correction]]: once contamination is reduced to a white-noise floor (demonstrated at 0.8–2 μm on TRAPPIST-1 c), additional epochs scale as 1/√N and bring the 60–250 ppm secondary-atmosphere regime into reach.
- [[2025_Bennett_GJ1132b]] — coadded four-visit NIRSpec G395H + G395M spectrum of GJ 1132 b; leave-one-out analysis isolates Visit 1 (from [[2023_May_GJ1132b]]) as the outlier driving any residual steam-atmosphere preference, and reattributes it to evolving stellar heterogeneity rather than atmosphere.
- [[2025_Alam_L168-9b]] — weighted mean of three NIRSpec G395H visits of L 168-9 b plus a fourth MIRI/LRS visit; no offsets applied between NRS1/NRS2 given the cross-visit agreement.
- [[2025_Alderson_TOI-776b]] — two-visit joint analysis of TOI-776 b; modeling an NRS1/NRS2 offset is required to make Visit 2 consistent with Visit 1.
- [[2024_Scarsdale_L98-59c]] — two-visit joint fit of L 98-59 c; 22/36 ppm precision in NRS1/NRS2 at R~200; combined spectrum is featureless.
- [[2024_Alderson_TOI-836b]] — joint fit across both TOI-836 b visits reaches 25 ppm precision in R~200 bins; demonstrates ~1.3× worse than PandExo predictions.
- [[2023_Moran_GJ486b]] — weighted mean of two GJ 486 b transits across three reductions; identifies a superbias-driven NRS2 offset in Transit 1 and corrects it per reduction.
- [[2023_Lustig-Yaeger_LHS475b]] — weighted average of two LHS 475 b visits to produce a 56-point R~100 co-added spectrum.
