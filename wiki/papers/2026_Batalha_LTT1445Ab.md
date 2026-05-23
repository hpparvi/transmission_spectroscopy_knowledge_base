---
type: paper
bibkey: 2026_Batalha_LTT1445Ab
authors: [Batalha, N. E., Wallack, N. L., Gordon, T., Wogan, N. F., Bennett, K. A., Redai, J. A., López-Morales, M., Teske, J., Valenti, J., Alam, M. K., Alderson, L., Aguichine, A., Batalha, N. M., Gagnebin, A., Gao, P., Meech, A., Moran, S. E., Wakeford, H. R., Wolfgang, A.]
year: 2026
venue: arXiv preprint (May 2026)
arxiv: 2605.15003
doi: ""
targets: [LTT1445Ab]
instruments: [JWST-NIRSpec, HST-WFC3]
methods: [transmission-spectroscopy, atmospheric-retrievals]
species_detected: []
species_ruled_out: [H2O, CO2, CH4]
codes: [Eureka, ExoTiC-JEDI, PICASO, VIRGA, Photochem, MultiNest]
tags: [terrestrial, m-dwarf-host, featureless-spectrum, compass, jwst-go-2512, cosmic-shoreline]
ingested: 2026-05-22
---

# JWST COMPASS Program: The 3–5 μm transmission spectrum of LTT 1445 A b

**Authors:** Batalha, Wallack, Gordon, Wogan, Bennett, Redai, López-Morales, Teske, Valenti, Alam, Alderson, Aguichine, N. M. Batalha, Gagnebin, Gao, Meech, Moran, Wakeford, Wolfgang (2026, arXiv:2605.15003) · submitted May 2026
**Target:** [[LTT1445Ab]] · **Instrument:** [[JWST-NIRSpec]] G395H (2.87–5.14 μm)
**Program:** [[JWST-GO-2512-COMPASS]] (PI: N. E. Batalha & J. Teske)
**Related companion paper:** [[2026_Wogan_LTT1445Ab]] (same target, LRS emission analysis)

## TL;DR

**First JWST/NIRSpec G395H transmission spectrum of the closest known transiting rocky exoplanet** ([[LTT1445Ab]]; 6.86 pc) under the COMPASS program. A single transit on 2025 Sep 1 reduced through two independent pipelines ([[Eureka]] + [[ExoTiC-JEDI]]) yields **23 ppm (NRS1) and 36 ppm (NRS2) median spectral precision** across 30-pixel bins. No statistically significant astrophysical features are detected — only an instrument-level **−43 ± 5 ppm offset between NRS1 and NRS2** (Eureka!) / −15 ± 6 ppm (ExoTiC-JEDI), consistent with NIRSpec-COMPASS detector-offset systematics ([[2025_Gordon_COMPASS-G395H]]). Atmospheric metallicity ≥ 350 × Solar is ruled out at 3σ (clear-sky equilibrium chemistry grid) when opaque pressure > 0.01 bar; this extends to ≥ 500 × Solar when combined with the HST/WFC3 spectrum from Bennett et al. 2025a (not ingested). For dominant-gas mixtures with H₂/He background, **H₂O and CO₂ < 10 % abundance ruled out** (at P_opaque > 0.01 bar) and **CH₄ < 100 % ruled out** (at P_opaque > 10⁻⁴ bar). Establishes LTT 1445A b as one of the most thoroughly-characterised JWST rocky planets — 12 transits across NIRISS/SOSS, NIRSpec G395H, NIRCam DHS, F322W2, F444W are funded (programs 2512 + 7251 + 7073) plus two F1500W eclipses under the Rocky Worlds DDT program; binned to R < 100 the combined dataset can rule out 1000 × Solar atmospheres at 4.6 ± 1.1 σ.

## Key findings

- **Single transit, 4.5 hr exposure, 2025 Sep 1**: NIRSpec G395H BOTS mode, SUB2048, F290LP, NRSRAPID readout; 4468 integrations × 3 groups.
- **Two independent reductions**:
  - [[Eureka]] (v0.13 + jwst 1.18.0): R_p/R_★ = 0.044916 ± 0.000065 (NRS1), 0.044476 ± 0.000067 (NRS2); 22.3 ppm / 23.6 ppm median precision in 41 / 65 spectroscopic channels.
  - [[ExoTiC-JEDI]] (Alderson 2022 not ingested): R_p/R_★ = 0.044229 ± 0.000088 (NRS1), 0.044151 ± 0.000081 (NRS2); 36.5 / 36.7 ppm precision.
- **No astrophysical features**: 5 model tests (zero-slope, step-NRS1/NRS2 offset, sloped line, free Gaussian in NRS1, free Gaussian in NRS2) — the only model preferred is the **NRS1–NRS2 offset** (Eureka! ln Z = −72 vs −99 baseline, Δ ln Z = 27).
- **NRS1–NRS2 offset**: Eureka! = −43 ± 5 ppm (NRS2 below NRS1); ExoTiC-JEDI = −15 ± 6 ppm. Consistent with the [[2025_Gordon_COMPASS-G395H]] inter-detector-offset characterization for COMPASS targets.
- **Atmospheric metallicity (chemical equilibrium [M/H] vs opaque pressure level)** — clear-sky 3σ exclusions:
  - JWST G395H alone: **[M/H] > 350 × Solar** ruled out (P_opaque > 10⁻² bar); broader exclusion to 220 × Solar at P_opaque = 10⁻³ bar.
  - JWST + HST/WFC3 (Bennett 2025a): **[M/H] > 520 × Solar** ruled out (Eureka! method 2).
- **Dominant-gas mixture (H₂/He + single gas)** — clear-sky 3σ exclusions:
  - CO₂ < 10 % (P_opaque > 10⁻⁴ bar)
  - H₂O < 10 % (P_opaque > 10⁻² bar)
  - CH₄ < 100 % (P_opaque > 10⁻⁴ bar) — strongest constraint
  - Implied mean molecular weight: μ > 7 g mol⁻¹ (CO₂) / μ > 4 (H₂O) / μ > 16 (CH₄).
- **C/O ratio insensitive**: solar (0.458) vs 0.5× solar (0.229) results agree.
- **Aerosol assessment** ([[VIRGA]], Batalha 2026 not ingested): direct H₂O condensation undersaturated by ~3500× across high-likelihood posteriors; KCl saturation vapor mixing ratio ~10⁻⁷, far below threshold. H₂SO₄ requires oxidizing-condition photochemistry beyond current model scope; S₈ requires reducing H₂-rich atmosphere. Photochemical hydrocarbon hazes (Trainer 2006 not ingested) unlikely on warm, oxidizing rocky atmospheres. **Aerosols at P < 10⁻² bar remain a viable degeneracy with metallicity** above the 0.01-bar opaque-pressure threshold.
- **Forecast for all 12 funded transits** (2 NIRISS/SOSS + 2 NIRSpec G395H + 4 NIRCam F322W2 + 4 NIRCam F444W from programs 2512, 7073, 7251): a 1000× Solar metallicity atmosphere distinguishable from flat at **4.6 ± 1.1 σ** in 1000 random realizations; 100% H₂O at 6.8 ± 1.0 σ; 100% CO₂ at 3.8 ± 1.1 σ (most challenging due to CO₂ peak being just outside NIRSpec G395H).

## Methods

- **Reductions**: [[Eureka]] + [[ExoTiC-JEDI]], following established COMPASS workflow ([[2024_Alderson_TOI-836b]], [[2024_Scarsdale_L98-59c]], [[2025_Alderson_TOI-776b]], [[2025_Teske_TOI776c]], [[2025_Redai_GJ357b]], [[2025_Gordon_COMPASS-G395H]]).
- **Optimization**: Eureka! aperture half-width = 5 px (NRS1) / 8 px (NRS2); sigma-thresholds 10 (NRS1) / 60 (NRS2); 30-pixel spectroscopic bins.
- **Spectral-feature detection** ([[MultiNest]] via UltraNest, Buchner 2021 not ingested): 5 model types (zero-slope, step, sloped line, free Gaussian in NRS1 only, free Gaussian in NRS2 only) per reduction; Bayesian evidence comparison.
- **Atmospheric modeling** ([[PICASO]] v4 + UltraNest):
  - **Chemical-equilibrium grid**: 20 metallicities (1–1000× Solar, log-spaced) × 2 C/O ratios (solar 0.458, 0.5× 0.229); pressure–temperature from Guillot 2010 not ingested; opaque-cloud level as free parameter (grey τ = 10).
  - **Three-gas mixture model**: H₂/He background + single varying gas (H₂O, CO₂, or CH₄); UltraNest Bayesian fit with 5 free parameters (X_i/(H₂+He) abundance, opaque pressure, NRS1/NRS2 offset, error inflation).
  - **Offset handling**: Method 1 (offset corrected before fit) vs Method 2 (offset as free parameter); Method 2 is more conservative and adopted for final constraints.
- **HST/WFC3 combination**: Bennett et al. 2025a (not ingested) G141 0.6–1.65 μm transmission spectrum added with independent NRS1/NRS2 offset; offset method 2 yields the [M/H] > 520 × Solar combined constraint.
- **F322W2 / F444W / DHS forecast**: PandExo (Batalha 2017a/b not ingested) for simulated error bars; binned to R < 100; pure photon-noise stacking assumed (acknowledged optimistic).

## Caveats & limitations

- **NRS1 baseline offset between reductions** (Eureka 2016.8 ± 3.5 ppm vs ExoTiC-JEDI 1969 ± 4 ppm) — Method 2 (offset as free fit parameter) was adopted for atmospheric inference to ensure both pipelines agree at 3σ; this is the most conservative choice and a precedent for future COMPASS reductions.
- **Linear-slope offset between NRS1 and NRS2** (ExoTiC-JEDI) suggests possible LD parameter sensitivity; tested with fix-vs-fit on quadratic LD, found minor effect (14 ppm median spectrum shift).
- **CO₂-dominant atmospheres are the hardest case** to rule out at high metallicity (CO₂ feature peak at 4.2–4.5 μm is partially outside NRS1; only the wing reaches into the data). 100% CO₂ requires the most visits to discriminate from flat.
- **HST/WFC3 has lower SNR** than JWST G395H, but the broader wavelength coverage drives the 380 → 520× Solar improvement when combined.
- **Aerosols at low pressure** (P < 0.01 bar) remain the primary degeneracy; no observational constraint here on cloud microphysics, only on opaque-pressure level.
- **Single transit visit per detector** — multi-visit stacking will be needed to push below the current ~22 ppm NRS1 precision.

## Open questions / follow-ups

- **Joint transmission + emission inference**: this paper + [[2026_Wogan_LTT1445Ab]] LRS analysis + future F1500W program form a 1–17 μm panchromatic dataset to break the metallicity-pressure degeneracy.
- **Aerosol parameterization** at P < 10⁻² bar — the [[VIRGA]] cloud-microphysics calculations rule out direct condensation but cannot constrain photochemical haze; future analyses with [[Photochem]] in coupled climate-photochem mode (Wogan 2025a not ingested) would help.
- **Hot Rocks survey + COMPASS overlap**: LTT 1445A b is the **last of the eleven COMPASS planets**; the panchromatic + multi-transit population analysis is now in reach (Gordon et al. 2026 reanalysis already incorporates seven; eleven completes the program).
- **3-σ atmospheric rejection requires ≥4 F1500W visits** at 20 ppm precision per [[2026_Wogan_LTT1445Ab]] forecast.

## Related

- [[2024_Wachiraphan_LTT1445Ab]] — original MIRI/LRS emission spectrum; ruled out thick CO₂ at > 6σ but left thin atmospheres possible.
- [[2026_Wogan_LTT1445Ab]] — companion climate-constrained Bayesian inversion of the same MIRI/LRS data; refines Wachiraphan's qualitative conclusion to P_s ≤ 0.6 bar and forecasts F1500W detection prospects.
- [[2025_Gordon_COMPASS-G395H]] — uniform reanalysis of the first 7 COMPASS NIRSpec G395H spectra; defines the NRS1/NRS2 detector-offset characterization used in this paper.
- [[2024_Alderson_TOI-836b]], [[2024_Scarsdale_L98-59c]], [[2025_Alderson_TOI-776b]], [[2025_Teske_TOI776c]], [[2025_Redai_GJ357b]] — the COMPASS comparison set; all featureless to date.
- [[2023_Lim_TRAPPIST1b]], [[2023_Lustig-Yaeger_LHS475b]], [[2025_Bennett_GJ1132b]], [[2025_Fisher_TOI1685b]] — comparable featureless JWST rocky-planet transmission spectra.
- [[2025_Coulombe_TOI-270b]] — outlier in the rocky-planet sample with a *tentative* atmospheric detection on a slightly warmer (Teq ≈ 569 K) target.
- Program: [[JWST-GO-2512-COMPASS]] (this paper is the program's eleventh and last target).
- Concept: [[cosmic-shoreline]] — LTT 1445A b is consistently above the empirical shoreline.
