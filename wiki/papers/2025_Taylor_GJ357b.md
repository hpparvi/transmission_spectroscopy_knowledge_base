---
type: paper
bibkey: 2025_Taylor_GJ357b
authors: [Taylor, J., Radica, M., Chatterjee, R. D., Hammond, M., Meier, T., Aigrain, S., MacDonald, R. J., Albert, L., Benneke, B., Coulombe, L.-P., Cowan, N. B., Dang, L., Doyon, R., Flagg, L., Johnstone, D., Kaltenegger, L., Lafrenière, D., Pelletier, S., Piaulet-Ghorayeb, C., Rowe, J. F., Roy, P.-A.]
year: 2025
venue: MNRAS
arxiv: 2505.24462
targets: [GJ357b]
instruments: [JWST-NIRISS]
methods: [transmission-spectroscopy, stellar-contamination-modeling]
species_detected: []
species_tentative: []
species_ruled_out: []
codes: [exoTEDRF, CHIMERA, juliet]
tags: [super-earth, m-dwarf-host, rocky-planet, jwst-gto-1201, null-result, atmospheric-retention, inactive-star]
ingested: 2026-04-24
---

# JWST NIRISS Transmission Spectroscopy of the Super-Earth GJ 357 b, a Favourable Target for Atmospheric Retention

**Authors:** Taylor, Radica, Chatterjee, Hammond, Meier, Aigrain, MacDonald, Albert, Benneke, Coulombe et al. (2025, MNRAS, accepted 2025-05-30) · [arXiv:2505.24462]
**Target:** [[GJ357b]] · **Host:** [[GJ357]] · **Instrument:** [[JWST-NIRISS]] (SOSS, 0.85–2.8 μm)
**Program:** [[JWST-GTO-1201]]

## TL;DR
A single JWST/NIRISS SOSS transit of the super-Earth GJ 357 b on 2023-11-22 — the **first atmospheric observation of this planet** — yields a featureless transmission spectrum across 0.85–2.8 μm, with no statistically significant spectral features or stellar contamination signal. Atmospheres with metallicity ≤100× solar and cloud top pressure > 0.01 bar are rejected at 3σ. Notably, the paper's larger contribution is a **detailed case for atmospheric retention**: GJ 357's XUV luminosity falls below the transonic-escape threshold at ~10³ Myr, making volcanic revival of a CO₂-dominated secondary atmosphere plausible. The featureless spectrum is therefore consistent with either a bare rock or a high-mean-molecular-weight (≥100× solar) secondary atmosphere — distinguishable with 3–4 future NIRSpec/G395H transits.

## Key findings
- **Partial transit recovered**: only ~60% of the transit was captured — ingress missed because the observation was built on the outdated Jenkins et al. 2019 ephemeris, which predicted mid-transit ~1.5 hr later than the more accurate Oddo et al. 2023 ephemeris. A Gaussian prior on mid-transit time from Oddo et al. 2023 recovers consistent orbital parameters (b = 0.213 ± 0.118, a/R★ = 22.62 ± 0.678); the resulting transmission spectrum is ~25% less precise than a full transit would have been.
- **Featureless spectrum (0.85–2.8 μm)**: Gaussian-feature searches at the positions of H₂O (0.95, 1.15, 1.4, 1.85 μm), CH₄ (1.7, 2.3 μm), and CO₂ (2.8 μm) all yield Bayes factors below the flat-line model (flat line slightly favored). ln(Z) = −28.20 ± 0.04 for the Gaussian model vs −27.95 ± 0.04 for flat line. No feature is detected.
- **No stellar contamination**: PHOENIX-grid TLS models (3- and 5-component setups including spot and faculae temperatures, covering fractions) all produce Bayes factors below the flat line. GJ 357's exceptional inactivity (log R'HK = 5.53; rotation period ~78 days; one of the least active M2.5V stars in a sample of >4000) is physically consistent with this null.
- **Atmospheric constraint at 3σ**: [[CHIMERA]] + FastChem2 grid (1–1000× solar metallicity, cloud-top pressure 10⁻⁴–10 bar, isothermal at Teq = 525 K, solar C/O); atmospheres with **metallicity ≤100× solar and cloud-top pressure > 0.01 bar are rejected at 3σ**. Above 100× solar, all models are degenerate with the flat line (over-fitting at 60 DOF). No full Bayesian retrieval is performed due to the partial transit and limited SNR. C/O ratio is unconstrained (Appendix A).
- **Interior model**: MAGRATHEA three-layer hydrostatic equilibrium model (iron core, silicate mantle, water layer); mass–radius position is consistent with **Earth-like bulk composition** (32.5% Fe, 67.5% silicates). Equally consistent with a pure-iron core + water layer or an Earth-silicate + H/He envelope — mass–radius alone is degenerate without element-ratio constraints.
- **Atmospheric retention analysis (§4):**
  - GJ 357 is the least active M2.5V star in Boro Saikia et al. 2018 (4000+ stars) by calcium activity proxy; log R'HK = 5.53.
  - MORS photoevaporation model: cycle-averaged XUV luminosity drops below the Chatterjee & Pierrehumbert 2024 transonic-escape threshold at **~10³ Myr**. GJ 357 has been sub-threshold for ~2–9 Gyr (minimum age ~4 Gyr from MORS rotation-period match ~78 days).
  - Stellar-wind mass-loss rate estimated ≪0.1 bar/Myr by scaling from GJ 414 (comparable mass, higher activity; Wood et al. 2021).
  - Outgassing supply: for 1.84 M⊕ at the Dorn et al. 2018 Earth-like bulk rate, ~10 bar/Gyr; revival of a CO₂-dominated secondary atmosphere of several bars is **plausible but uncertain** (key uncertainties: early flaring duration; mantle volatile depletion before the main sequence).
- **Predictions for future characterisation (§5):**
  - 2 MIRI/LRS eclipses to distinguish bare-rock surface types (tholeitic basalt vs. lunar anorthosite); strong degeneracy between reflective surface and thin atmosphere in individual photometric points.
  - **3–4 NIRSpec/G395H transits** to detect a 1 bar N₂ + 1000 ppm CO₂ atmosphere at 3σ via the 4.3 μm CO₂ feature.
  - 9 NIRSpec/G395H transits for 1 bar N₂ + 1 ppm CO₂ at 3σ.
  - NIRISS/SOSS (this paper's mode) cannot distinguish these scenarios to 3σ even after 10 transits.
  - Also flagged: the Rocky Worlds DDT program (Redfield et al. 2024; not yet ingested) has already accepted GJ 357 b as a target.

## Methods
- **Observations:** single NIRISS/SOSS transit of GJ 357 b on 2023-11-22 (UT 11:40–17:10); SUBSTRIP96 subarray, 2201 integrations, 2 groups/integration; 0.85–2.8 μm SOSS first diffraction order. Part of [[JWST-GTO-1201]] (NEAT GTO, PI: Lafrenière).
- **Reduction:** [[exoTEDRF]] pipeline (Feinstein et al. 2023; Radica et al. 2023, 2024). Stage 1: standard STScI corrections + 1/f noise removal at group level (scale-achromatic method, Radica et al. 2023, 2024); Stage 2: flat-field, background subtraction using STScI SUBSTRIP96 model; principal-component analysis (PCA) on 2D detector images for detector-level detrending. Spectral extraction via simple box aperture (32 pixel width).
- **Light-curve fits:** [[juliet]] wrapper around BATMAN transit model (Kreidberg 2015); quadratic limb-darkening via Kipping 2013 reparameterization with Gaussian priors from ExoTiC-LD (Grant & Wakeford 2024) on the 3D Stagger grid (Magic et al. 2015); systematics model = linear trend in time + first two PCA eigenvalue time series + error inflation term. No GP included (periodogram of baseline integrations shows no significant period; GP models with SHO kernel via celerite all produce unphysical light curves unconstrained by the pre-transit baseline).
- **Spectroscopic fits:** binned to R = 50; 8 free parameters per bin (transit depth, limb-darkening × 2, systematics × 5); Gaussian priors on limb-darkening coefficients.
- **Feature detection:** nested sampling via pymultinest (2000 live points, ln(Z) tolerance 0.5); Bayes factor = ln(Z₁) − ln(Z₂) with Z₂ = flat line; atmospheric models unfavored if Bayes factor < 0.
- **TLS modeling (§3.2):** PHOENIX grid via pysynphot; four setups (3-component with and without log g free; 5-component with and without log g free); same Bayesian evidence comparison. GJ 357 treated as inactive by assumption; all TLS models disfavored.
- **Atmospheric forward models (§3.3):** [[CHIMERA]] + FastChem2 on a 26 × 5 (metallicity × cloud-top pressure) grid; χ² fitting with rejection sigma statistic; C/O appendix with full retrieval.
- **Interior models (§3.4):** MAGRATHEA (Huang et al. 2022; not yet ingested); three-layer planet (iron core, silicate mantle, water layer); Earth-like composition assumed (32.5% Fe, 67.5% silicates + forsterite/wadsleyite/bridgmanite post-perovskite).
- **MIRI emission predictions (§5):** AGNI 1D atmosphere model (Hammond et al. 2024; not yet ingested) for emission spectra; PandExo (Batalha et al. 2017) for noise simulation.

## Caveats & limitations
- **Partial transit (~40% ingress missed)**: precision is ~25% worse than a full transit would achieve, and the residual correlated noise in the post-transit baseline is not fully captured by the systematics model. No GP was found to help reliably.
- **No full Bayesian retrieval**: partial transit + limited SNR justify χ² analysis on a forward model grid only; abundance constraints are grid-point-dependent.
- **Degenerate interior models**: mass–radius alone cannot distinguish Earth-like from pure-iron + water layer or silicate + H/He configurations.
- **Atmospheric retention caveats**: MORS over-estimates the measured XUV luminosity by over an order of magnitude (suggesting GJ 357 is unusually inactive even for its rotation period), so the sub-threshold timing is uncertain; early flaring-state duration and mantle depletion remain the key unknowns.
- **Model unconstrained at high metallicity**: above 100× solar, χ²ν < 1 for all models — the data are over-fit; no upper metallicity limit can be placed.

## Open questions / follow-ups
- Does a high-MMW secondary (CO₂-dominated) atmosphere exist? 3–4 NIRSpec/G395H transits required for a 3σ test via the 4.3 μm feature.
- Can MIRI emission distinguish bare-rock surface composition from a thin CO₂ atmosphere? 2 eclipses required, but surface-vs-atmosphere degeneracy remains without multiple MIRI filters.
- How long was GJ 357 in its pre-main-sequence flaring phase — the critical constraint on mantle volatile depletion?
- Will Rocky Worlds DDT (Redfield et al. 2024; not yet ingested) confirm or update the null result?

## Related
- [[2023_Lustig-Yaeger_LHS475b]], [[2025_Bennett_GJ1132b]], [[2025_Alam_L168-9b]], [[2024_Alderson_TOI-836b]], [[2024_Scarsdale_L98-59c]], [[2025_Alderson_TOI-776b]] — the family of featureless-spectrum super-Earth / rocky-planet results this paper joins; all NIRSpec G395H, vs. this paper's NIRISS SOSS.
