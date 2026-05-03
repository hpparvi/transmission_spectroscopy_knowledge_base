---
type: method
aliases: [multi-visit coadding, transit stacking, coadded transmission spectrum, leave-one-out transit analysis]
tags: [multi-visit, small-planet, rocky-planet, detection-discriminator, hub]
---

# Multi-visit stacking

Weighted combination of multiple transit visits of the same target into a single higher-SNR [[transmission-spectrum]], typically paired with a **leave-one-out** diagnostic that drops each visit in turn to check that any apparent feature is not visit-specific. Essential for rocky M-dwarf planets where per-visit SNR barely reaches the expected atmospheric-feature amplitude and where visit-specific [[stellar-contamination]] can otherwise masquerade as atmospheric structure. The de facto standard for any small-planet atmospheric claim in the JWST era — over half the wiki's small-planet papers stack multiple visits, and the pattern of "single-visit hint → multi-visit retraction" recurs across [[GJ1132b]], [[GJ486b]], and [[TRAPPIST-1e]].

## Variants

- **Joint fit across visits** (preferred when visits are nearly contemporaneous and per-visit systematics are similar). Used in [[2025_Teske_TOI776c]] (Eureka! joint fit of two visits), [[2025_Alderson_TOI-776b]], [[2024_Scarsdale_L98-59c]], [[2024_Alderson_TOI-836b]].
- **Weighted mean of independently fit per-visit spectra** (preferred when visits are far apart in time or have visit-specific systematics requiring different parameters). Used in [[2025_Bennett_GJ1132b]], [[2025_Alam_L168-9b]], [[2025_Teske_TOI776c]] (Tiberius weighted average), [[2023_Moran_GJ486b]], [[2023_Lustig-Yaeger_LHS475b]].
- **GP marginalization across visits.** [[2025_Espinoza_TRAPPIST1e]] and [[2025_Glidden_TRAPPIST1e]] introduce Gaussian-process modeling of contamination structure during the stacking step itself rather than after; necessary for ultracool-dwarf hosts where individual visits are contamination-dominated.
- **Empirical contamination correction + stacking.** [[2025_Rathcke_TRAPPIST1bc]] motivates stacking as the natural complement to [[back-to-back-transit-correction]]: once the empirical correction reduces structured red noise to a white-noise floor, additional visits scale as 1/√N.

## Trade-offs

- **NRS1/NRS2 detector-offset modeling.** Several G395H papers ([[2025_Alderson_TOI-776b]], [[2025_Teske_TOI776c]], [[2024_Alderson_TOI-836b]], [[2023_May_GJ1132b]], [[2023_Moran_GJ486b]]) document visit-specific offsets between NRS1 and NRS2 that must be modeled before coadding. Treatments vary; [[2025_Alam_L168-9b]] applies no offset, [[2025_Alderson_TOI-776b]] requires it for Visit 2 consistency.
- **Leave-one-out as a feature reality check.** [[2025_Bennett_GJ1132b]] is the canonical example: a Bayes-factor 27 (3.1σ) Visit-1 CH₄ inference vanishes when that visit is dropped, and reappears when other visits are dropped — diagnosing the visit as the outlier rather than the atmosphere.
- **Stacking on active stars.** [[2023_Lim_TRAPPIST1b]] cautions that simple coaddition on active hosts produces a misleading "average" of evolving spot/facula configurations; per-visit contamination correction is required first.

## Open issues

- **Treatment of detector offsets.** No community standard; per-paper choices.
- **Visit-correlated stellar contamination.** Whether GP marginalization or empirical reference-planet correction is preferable on a given host depends on the rotational timescale, photospheric structure, and number of visits; not yet systematized.
- **How many visits are enough?** Bennett 2025 (4 visits on GJ 1132 b), Espinoza/Glidden 2025 (4 on TRAPPIST-1 e), Fisher 2025 (5 on TOI-1685 b) suggest 4–5 visits is the floor for retiring single-visit inferences on M-dwarf planets at NIRSpec G395H precision.

## Papers

- [[2026_Holmberg_GJ3473b]] — joint fit of four MIRI F1500W eclipses on GJ 3473 b; tentative visit-to-visit depth variability flagged.
- [[2026_Ashtari_HATS75b]] — three-visit weighted stacking of HATS-75 b NIRSpec PRISM transits with two parallel reduction variants (fleck + emcee, spotrod + dynesty).
- [[2025_Connors_MIRI-15um]] — joint FN-PCA fits across 2–5 MIRI F1500W eclipses per target on 5 rocky planets; first uniform multi-visit reanalysis of MIRI F1500W eclipse photometry.
- [[2025_Fisher_TOI1685b]] — five G395H transits of TOI-1685 b; stacked flat; MMW ≳ 10 at ~5σ.
- [[2025_Espinoza_TRAPPIST1e]] — four PRISM transits with GP marginalization across visits.
- [[2025_PiauletGhorayeb_TRAPPIST1d]] — two PRISM transits; flat ±100–150 ppm.
- [[2025_Glidden_TRAPPIST1e]] — four PRISM transits; GP-corrected four-visit combined spectrum.
- [[2025_Bennett_GJ1132b]] — four-visit coadded G395H + G395M spectrum; leave-one-out analysis retires the [[2023_May_GJ1132b]] Visit-1 inference.
- [[2025_Teske_TOI776c]] — two-visit joint fit + weighted-average comparison; conclusions unchanged across offset treatments.
- [[2025_Rathcke_TRAPPIST1bc]] — motivates stacking as the natural follow-up to [[back-to-back-transit-correction]].
- [[2025_Alam_L168-9b]] — three G395H + one MIRI/LRS visit; weighted mean.
- [[2025_Alderson_TOI-776b]] — two G395H visits; NRS1/NRS2 offset required for Visit-2 consistency.
- [[2024_Scarsdale_L98-59c]] — two-visit joint fit; 22/36 ppm precision NRS1/NRS2.
- [[2024_Alderson_TOI-836b]] — two-visit joint fit; 25 ppm precision; ~1.3× worse than PandExo predictions.
- [[2023_Lim_TRAPPIST1b]] — cautionary case for active-star stacking without contamination correction.
- [[2023_Moran_GJ486b]] — two-visit weighted mean; superbias-driven NRS2 offset corrected per reduction.
- [[2023_Lustig-Yaeger_LHS475b]] — two-visit weighted average; 56-point R~100 coadded spectrum.
