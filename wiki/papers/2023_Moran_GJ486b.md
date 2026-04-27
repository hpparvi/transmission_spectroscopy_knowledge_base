---
type: paper
bibkey: 2023_Moran_GJ486b
authors: [Moran, S. E., Stevenson, K. B., Sing, D. K., MacDonald, R. J., Kirk, J., Lustig-Yaeger, J., Peacock, S., Mayorga, L. C., Valenti, J. A., Bennett, K. A., López-Morales, M., May, E. M., Rustamkulov, Z., Adams Redai, J., Alam, M. K., Batalha, N. E., Fu, G., Gonzalez-Quiles, J., Highland, A. N., Kruse, E., Lothringer, J. D., Ortiz Ceballos, K. N., Sotzen, K., Wakeford, H. R.]
year: 2023
venue: ApJL
doi: 10.3847/2041-8213/accb9c
targets: [GJ486b]
instruments: [JWST-NIRSpec]
methods: [transmission-spectroscopy, atmospheric-retrievals, stellar-contamination-modeling, multi-visit-stacking]
species_detected: []
species_tentative: [H2O]
species_ruled_out: [H2, CH4]
codes: [Eureka, FIREFLy, Tiberius, POSEIDON, PICASO, CHIMERA]
tags: [super-earth, m-dwarf-host, rocky-planet, jwst-go-1981, champs, water-world-candidate, stellar-contamination, two-scenario, superseded]
ingested: 2026-04-24
---

# High Tide or Riptide on the Cosmic Shoreline? A Water-rich Atmosphere or Stellar Contamination for the Warm Super-Earth GJ 486 b from JWST Observations

**Authors:** Moran, Stevenson, Sing, MacDonald, Kirk, Lustig-Yaeger, et al. (2023, ApJL 948:L11) · [doi:10.3847/2041-8213/accb9c]
**Target:** [[GJ486b]] · **Host:** [[GJ486]] · **Instrument:** [[JWST-NIRSpec]] (G395H, 2.87–5.14 μm)
**Program:** [[JWST-GO-1981-CHAMPs]]

## TL;DR
Two JWST NIRSpec/G395H transits of the warm super-Earth GJ 486 b (Rp=1.3 R⊕, Mp=3.0 M⊕, Teq ≈ 700 K; M3.5 host) yield a transmission spectrum that deviates from a flat line at **2.24σ–3.29σ** across three independent reductions ([[Eureka]], [[FIREFLy]], [[Tiberius]]). The paper presents **two scenarios that fit the data equally well** (χ²ν ≈ 1.0): (a) an H₂O-rich atmosphere with log X(H₂O) > 10% at 2σ confidence, or (b) unocculted starspot contamination from ~10% coverage of 2700 K spots on a 3343 K photosphere. [[atmospheric-retrievals]] with [[POSEIDON]] cannot distinguish the two; independent multi-component PHOENIX fits to the out-of-transit stellar baseline moderately favor the spotted-star interpretation. The paper explicitly calls for shorter-wavelength follow-up to break the degeneracy and flags the already-scheduled MIRI/LRS emission observation (JWST GO 1743) as the tie-breaker — the follow-up that subsequently became [[2024_WeinerMansfield_GJ486b]], which **resolved the ambiguity in favor of stellar contamination**.

## Key findings
- Two NIRSpec/G395H transits (2022-12-25, 2022-12-29); three independent reductions agree on the blueward spectral slope (<~3.7 μm) morphology.
- Flat-line hypothesis rejected at **3.20σ ([[Eureka]]), 2.24σ ([[FIREFLy]]), 3.29σ ([[Tiberius]])** via Gaussian-feature Bayes-factor tests.
- Forward modeling ([[PICASO]] + [[CHIMERA]]) rejects H₂/He-dominated atmospheres up to 1000× solar metallicity at **>3σ**; a pure [[H2O]] atmosphere provides the best fit (χ²ν = 1.01), pure [[CO2]] marginally acceptable (χ²ν = 1.39), pure [[CH4]] strongly disfavored.
- [[POSEIDON]] and rfast (not yet ingested) retrievals converge on **H₂O as the most likely dominant gas**, with Bayes factors 133 and 8 (3.6σ and 2.6σ) for H₂O in [[Eureka]] and [[FIREFLy]] reductions. The [[Tiberius]] reduction does not uniquely require water (a secondary H₂-dominated mode exists; deemed unphysical).
- An alternative [[POSEIDON]] **unocculted-starspot retrieval fits equally well** (χ²ν ≈ 1.0) with f_het ≈ 0.11, T_spot ≈ 2700 K, T_phot ≈ 3343 K; preferred at 3.8σ / 2.9σ / 3.5σ over a flat spectrum across the three reductions.
- Independent PHOENIX multi-component fits to the **flux-calibrated out-of-transit baseline** prefer a 3-component (photosphere + spots + faculae) model over single-photosphere by Δχ²ν ≈ 23, lending physical support to the starspot scenario.
- Cannot distinguish water-rich atmosphere from stellar contamination with G395H data alone — **shorter-wavelength observations** are required.
- A systematic NRS2 offset in Transit 1 (traced to superbias) is identified and corrected in each reduction.

## Methods
- **Observations:** two NIRSpec/G395H BOTS transits of GJ 486 b on 2022-12-25 and 2022-12-29; 3507 integrations × 3 groups over 3.53 hr each.
- **Reduction:** three parallel pipelines — [[Eureka]] (primary interpretation), [[FIREFLy]], [[Tiberius]] — with consistent agreement after superbias correction of the NRS2 Transit-1 offset.
- **Light-curve fitting:** `batman` transit + polynomial systematics (quadratic/linear per detector); `ExoTiC-LD` limb darkening from MPS-ATLAS; `emcee` MCMC with photometric-uncertainty inflation to χ²ν = 1.
- **Multi-visit analysis:** weighted mean across the two transits; see [[multi-visit-stacking]].
- **Forward modeling:** [[PICASO]] transmission spectra at R=10,000 from [[CHIMERA]] thermochemical equilibrium + single-gas end-member atmospheres (pure H₂O, pure CO₂, pure CH₄, Earth-like, 1000× solar).
- **Retrievals:** [[POSEIDON]] (MacDonald & Madhusudhan 2017; not yet ingested) 6-gas free-chemistry + rfast (Robinson & Salvador 2023; not yet ingested) 1-gas + stellar-contamination (Pinhas et al. 2018 / Rathcke et al. 2021 parameterizations); PyMultiNest sampling with 2000 live points; joint priors over MMW, opaque surface pressure, planet mass.
- **Stellar baseline modeling:** 1-, 2-, and 3-component PHOENIX (Allard et al. 2012) fits to the out-of-transit flux-calibrated spectrum; see [[stellar-contamination-modeling]].

## Caveats & limitations
- The two scenarios are statistically indistinguishable within G395H — the paper's main result *is* the degeneracy, not a detection.
- Tiberius reduction's secondary H₂-dominated retrieval mode is unphysical (flagged by the authors) but numerically present.
- FIREFLy reduction has larger error bars than Eureka!/Tiberius, reducing its feature-detection significance to 2.24σ.
- Retrievals use Pinhas 2018 contamination parameterization (fixed-prior spot/facula temperatures); this constrains but does not uniquely determine the heterogeneity properties.
- No individual molecular-feature detections; inferences rest on spectral slope + full-range retrievals.
- Red noise present in white-light residuals (likely thermal cycling), inflating per-channel error bars by ~1.5×.

## Open questions / follow-ups
- Can shorter-wavelength observations (NIRISS SOSS, <2.8 μm) distinguish water-rich atmosphere from stellar contamination? Authors flag this as the key next step.
- The MIRI/LRS secondary-eclipse follow-up (JWST GO 1743) was already scheduled at time of writing — now published as [[2024_WeinerMansfield_GJ486b]], which **disambiguated in favor of the starspot scenario**.
- If the starspot interpretation is correct, what are the implications for transmission-spectroscopy systematics on all M-dwarf rocky planets? This paper functions as a cautionary tale.

## Tensions
- **vs. [[2024_WeinerMansfield_GJ486b]]:** Moran 2023 presents two equally-Bayesian scenarios (water-rich atmosphere OR unocculted starspots) and explicitly cannot choose between them. Weiner Mansfield 2024's MIRI/LRS emission campaign measured a dayside temperature ratio R = 0.97 ± 0.01, which is inconsistent with a water-rich atmosphere and consistent with a bare rock — **resolving the Moran 2023 ambiguity in favor of the stellar-contamination interpretation**. The Moran paper page is preserved as written; the resolution lives on [[GJ486b]]'s `## Observations to date` and `## Tensions` sections.

## Related
- [[2024_WeinerMansfield_GJ486b]] — the MIRI/LRS follow-up that broke the degeneracy Moran 2023 explicitly flagged.
- [[2023_Lustig-Yaeger_LHS475b]] — sibling JWST CHAMPs transmission paper on LHS 475 b (Earth-sized, featureless).
- [[2023_May_GJ1132b]] — the companion JWST CHAMPs paper on GJ 1132 b; discusses similar stellar-contamination-vs-atmosphere degeneracies.
- [[2024_Gressier_L98-59d]], [[2024_Banerjee_L98-59d]] — later JWST analyses using similar stellar-contamination retrieval frameworks on L 98-59 d.
- Ridden-Harper et al. 2022 (not yet ingested) — prior ground-based study of GJ 486 b ruling out solar-metallicity pure H₂O atmospheres.
- Caballero et al. 2022 (not yet ingested) — GJ 486 b discovery / characterization paper.
- Trifonov et al. 2021 (not yet ingested) — GJ 486 b transmission-spectroscopy metric.
