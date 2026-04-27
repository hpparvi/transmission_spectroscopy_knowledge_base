---
type: paper
bibkey: 2025_Bennett_GJ1132b
authors: [Bennett, K. A., MacDonald, R. J., Peacock, S., Perez, J., May, E. M., Moran, S. E., Alderson, L., Lustig-Yaeger, J., Wakeford, H. R., Sing, D. K., et al.]
year: 2025
venue: AJ
doi: 10.3847/1538-3881/adf198
targets: [GJ1132b]
instruments: [JWST-NIRSpec]
methods: [transmission-spectroscopy, stellar-contamination-modeling, multi-visit-stacking]
species_detected: []
species_tentative: []
species_ruled_out: [CH4, CO2]
codes: [Eureka, PICASO, CHIMERA]
tags: [super-earth, m-dwarf-host, rocky-planet, jwst-go-1981, champs, bare-rock, multi-visit, null-result]
ingested: 2026-04-22
---

# Additional JWST/NIRSpec Transits of the Rocky M Dwarf Exoplanet GJ 1132 b Reveal a Featureless Spectrum

**Authors:** Bennett, MacDonald, Peacock, Perez, May, Moran, Alderson, Lustig-Yaeger, Wakeford, Sing, et al. (2025, AJ 170:205) · [doi:10.3847/1538-3881/adf198]
**Target:** [[GJ1132b]] · **Host:** [[GJ1132]] · **Instrument:** [[JWST-NIRSpec]] (G395H + G395M modes, 2.8–5.2 μm)
**Program:** [[JWST-GO-1981-CHAMPs]]

## TL;DR
A four-visit JWST NIRSpec campaign on the rocky M-dwarf super-Earth GJ 1132 b — combining the two G395H transits from [[2023_May_GJ1132b]] with **two new G395M transits** (2024-02-08, 2024-06-05) — yields a **coadded transmission spectrum best fit by a flat line** across all three independent reductions. Null-hypothesis tests give χ²ν ≈ 0.9–1.1 and Gaussian-feature detections ≤ 1.7σ. Combined with MIRI/LRS emission results from [[2024_Xue_GJ1132b]], transmission + emission are consistent with only the thinnest of atmospheres; given GJ 1132 b's age and irradiation a thin atmosphere would be unstable, so the simplest explanation is that **GJ 1132 b is a bare rock**.

This result **retires the Visit-1-only H₂O + [[CH4]] + N₂O inference** from [[2023_May_GJ1132b]]. A leave-one-out analysis shows that the prior "thin steam atmosphere" fit is driven almost entirely by Visit 1, and flux-calibrated out-of-transit stellar spectra show Visit 1 had ~10% more cool starspots and ~5% fewer faculae than the other three visits. The Visit-1 deviation is reattributed to evolving stellar heterogeneity (a large spot rotating off the visible disk before Visit 2, eight days later), not to planetary atmospheric features.

## Key findings
- Four-visit coadded spectrum ([[Eureka]], FIREFLy, ExoTiC-JEDI reductions) is statistically consistent with a flat line (deviation from null ≤ 1.2σ; Gaussian-feature Bayes-factor tests all favor the null).
- **1000× solar metallicity H₂/He atmosphere rejected at > 4σ** — a substantial tightening over the marginal rejection from two visits in [[2023_May_GJ1132b]].
- Pure **[[CH4]]** atmosphere rejected at > 10σ; pure **[[CO2]]** atmosphere rejected at > 3σ; H₂O + 1–10% CH₄ mixtures also rejected.
- Thin H₂O (steam) atmospheres remain formally consistent with the coadded spectrum (χ²ν 0.9–1.3), but leave-one-out analysis isolates Visit 1 as the driver of that fit; dropping Visit 1 removes the preference.
- **Stellar heterogeneity evolved between visits:** Visit 1 favors ~10% more 2900 K cool-spot coverage than Visits 2–4, consistent with a large spot that rotated off the visible disk (122-day rotation period) before Visit 2.
- **First combination of NIRSpec G395H + G395M** on a single target. G395M fills the NRS1/NRS2 detector gap and shows no evidence of a G395H-specific detector offset at the data's precision. The paper argues G395M should be preferred over G395H for faint M-dwarf rocky-planet targets.
- A ~200 ppm discrepancy at 4.5 μm in Visit 3 is too large for planetary variability; the paper speculates it could arise from **spatially variable CO on the stellar surface** (citing Smitha et al. 2025 MHD models) — a potentially new systematic for M-dwarf transit spectra.
- Together with MIRI/LRS emission ([[2024_Xue_GJ1132b]]): CO₂ constrained to < 10 mbar, and any thin atmosphere would be unstable over GJ 1132's ≥ 5 Gyr age. Conclusion: **bare rock**.
- Ground-based CRIRES+ cross-correlation follow-up (Palle et al. 2025; not yet ingested) independently rules out the HCN/CH₄/H₂O features proposed by Swain et al. 2021.

## Methods
- **Observations:** four JWST-NIRSpec transits of GJ 1132 b — two G395H visits (2023-02-25, 2023-03-05; 14 groups/integration) and two new G395M visits (2024-02-08, 2024-06-05; 6 groups/integration). Program [[JWST-GO-1981-CHAMPs]].
- **Reduction:** three independent pipelines — [[Eureka]], FIREFLy, ExoTiC-JEDI — each run across all four visits with consistent calibrations. Light curves fit with `batman` (Kreidberg 2015); limb-darkening with `ExoTiC-LD` on the MPS2 grid; MCMC with `emcee`; correlated-noise inflation via the Pont et al. 2006 red-noise diagnostic.
- **Coadding:** weighted mean of all four visits produces a single R ≈ 100 coadded transmission spectrum per reduction — see [[multi-visit-stacking]]. A leave-one-out analysis drops each visit in turn to isolate its contribution.
- **Null-hypothesis tests:** χ²ν distributions from simulated flat-spectrum realizations; Gaussian-feature Bayes-factor comparison via `dynesty` nested sampling.
- **Forward modeling:** [[PICASO]]-generated transmission models on a [[CHIMERA]] thermochemical-equilibrium grid (100–1000× solar) plus single/two-gas 1-bar isothermal atmospheres (pure CH₄, pure CO₂, H₂O ± CH₄ at 1% or 10%).
- **Stellar forward modeling:** three-component PHOENIX (F. Allard et al. 2012) fits to flux-calibrated out-of-transit spectra — see [[stellar-contamination-modeling]]. Visit 1 significantly favors higher cool-spot coverage than the other three visits.

## Caveats & limitations
- A thin H₂O steam atmosphere (< 10 mbar) cannot be formally rejected by the coadded transmission spectrum alone; the paper relies on MIRI/LRS emission + thermodynamic-stability arguments to close that gap.
- The leave-one-out analysis assumes stellar heterogeneity is the only plausible Visit-1-specific systematic; if a different visit-level systematic is at play, the flat-line interpretation survives but the stellar-spot narrative weakens.
- The stellar-CO hypothesis for the Visit-3 4.5 μm residual is motivated by theory (Smitha et al. 2025) but not directly tested against data here.
- Retrievals are not presented in this paper; interpretation is via χ²ν and Bayes-factor comparison on a grid of forward models.

## Open questions / follow-ups
- How common is Visit-1-style spot-coverage evolution in CHAMPs-cadence observations? A systematic survey across the program would calibrate it as a general systematic.
- Can stellar CO spatial variability be detected and corrected in out-of-transit spectra? Smitha et al. 2025 MHD work is the theoretical anchor.
- What is the minimum atmospheric mass detectable on GJ 1132 b with further NIRSpec visits? The paper's working answer is "not much beyond thin steam"; a quantitative limit would help prioritize similar campaigns on other rocky targets.

## Tensions
- **vs [[2023_May_GJ1132b]] Visit-1 interpretation:** May et al. 2023 offered both "unlucky noise draw" (preferred) and "H₂O-dominated atmosphere with ~1% CH₄" (alternative) framings for Visit 1's nonflat spectrum. This paper's leave-one-out analysis + flux-calibrated stellar modeling favor a **third explanation** — Visit 1 reflects real but *stellar* heterogeneity, i.e., a large cool spot that has since rotated out of view. The atmospheric interpretation is retired; the noise-draw interpretation is partially retained but refined toward "noise modulated by spot evolution." Tension status recorded on [[GJ1132b]].
- **HCN / H₂-dominated atmosphere claim (Swain et al. 2021; not yet ingested):** reinforced rejection. Both JWST (this paper) and ground-based CRIRES+ (Palle et al. 2025; not yet ingested) independently rule out the HCN signature; Mugnai et al. 2021 and Libby-Roberts et al. 2022 re-analyses of the same HST data remain the simplest resolution.

## Related
- [[2023_May_GJ1132b]] — the paper this work builds on and updates; same program, same target, first two visits.
- [[2024_Xue_GJ1132b]] ([[JWST-GTO-1274]]) — MIRI/LRS emission; the second leg of the transmission + emission joint constraint on GJ 1132 b.
- CRIRES+ cross-correlation search (Palle et al. 2025; not yet ingested) — ground-based independent ruling-out of Swain 2021.
