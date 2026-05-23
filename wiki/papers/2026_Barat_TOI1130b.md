---
type: paper
bibkey: 2026_Barat_TOI1130b
authors: [Barat, S., Fairnington, T., Huang, C. X., Vanderburg, A., Morley, C. V., Korth, J., Parviainen, H., Brandeker, A., Zhou, G., Evans-Soma, T. M., Sha, L., Lin, D. N. C., Wright, D., Morrissey, A., Nabbie, E., Collins, K. A., Evans, P., Guillot, T., Horne, K., Radford, D. J., Schwarz, R. P., Shporer, A., Srdoc, G., Suarez, O.]
year: 2026
venue: ApJL (submitted)
arxiv: 2605.02036
doi: ""
targets: [TOI-1130b]
instruments: [JWST-NIRSpec, JWST-NIRISS, TESS, CHEOPS]
methods: [transmission-spectroscopy, atmospheric-retrievals]
species_detected: [H2O, CO2, SO2]
species_tentative: [CH4]
species_ruled_out: [He]
codes: [Eureka, exoTEDRF, petitRADTRANS, PLATON, PICASO, Photochem, MultiNest, easyCHEM, VIRGA, batman]
tags: [mini-neptune, multi-planet, mean-motion-resonance, 2-1-resonance, hot-jupiter-companion, ex-situ-formation, water-ice-line, pebble-filtering, sulfur-photochemistry, high-mmw, radius-cliff, k-dwarf-host]
ingested: 2026-05-22
---

# JWST unveils a high mean molecular weight atmosphere for mini-Neptune TOI-1130b: Evidence for formation beyond the water ice line

**Authors:** Barat, Fairnington, Huang, Vanderburg, Morley, Korth, Parviainen, Brandeker, Zhou, Evans-Soma, Sha, Lin, Wright, Morrissey, Nabbie, Collins, Evans, Guillot, Horne, Radford, Schwarz, Shporer, Srdoc, Suarez (2026, ApJL submitted) · arXiv:2605.02036
**Target:** [[TOI-1130b]] (host: [[TOI-1130]]; outer hot Jupiter [[TOI-1130c]]) · **Instruments:** [[JWST-NIRSpec]] G395H + [[JWST-NIRISS]] SOSS + [[TESS]] + [[CHEOPS]]
**Program:** [[JWST-GO-3385]] (PI: Barat); simultaneous CHEOPS via CH_PR149003 (PI: Brandeker)
**Observations:** Two consecutive transits of TOI-1130 b on 2024 Aug 20 (NIRSpec G395H) and 2024 Aug 24 (NIRISS SOSS)

## TL;DR

First JWST atmospheric characterization of the warm mini-Neptune [[TOI-1130b]] (3.66 R⊕, 19.8 M⊕, T_eq ≈ 825 K) — the inner planet of a unique multi-planet system in **2:1 mean-motion resonance** with an outer **hot Jupiter** [[TOI-1130c]] (13 R⊕, 336 M⊕). Combined NIRISS+NIRSpec G395H + TESS + CHEOPS transmission spectrum yields **H₂O at 7.5σ, CO₂ at 3.3σ, SO₂ at 3.6σ, and tentative CH₄ at ~2σ**, plus a strong optical scattering slope confirmed by TESS/CHEOPS optical depths. Free-chemistry retrievals ([[petitRADTRANS]], cross-checked with [[PLATON]]) give a **lower limit** on mean molecular weight **μ > 3.5 amu**; equilibrium-chemistry retrievals (also petitRADTRANS) give **log Z/Z_⊙ = 1.8⁺⁰·⁴₋₀·³, μ = 5.5⁺¹·³₋₀·⁸ amu, C/O < 0.75 (3σ)**. A self-consistent forward grid ([[PICASO]] + [[Photochem]]) confirms 100× solar / C/O = 0.3 / K_zz = 10¹⁰ as best-fit. Helium 1083 nm escape signature is **not detected** (upper limit 10¹¹ g s⁻¹). The high-MMW atmosphere + the outer hot-Jupiter "pebble filter" + the 2:1 MMR orbital architecture together strongly favor **ex-situ formation beyond the water ice line + disc migration** rather than in-situ formation. TOI-1130 b joins [[TOI-270d]] (μ ≈ 5.5) and [[GJ3470b]] (μ ≈ 5.7) as a third "**volatile-rich miscible-envelope mini-Neptune**" — class that may not have a homogeneous formation history.

## Key findings

- **Detected species** (combined NIRISS + NIRSpec + TESS + CHEOPS):
  - **H₂O at 7.5σ** (log mass fraction = −0.6⁺⁰·³₋⁰·⁵; petitRADTRANS free); confirmed across 1.4, 1.8 μm water bands.
  - **CO₂ at 3.3σ** (log mass fraction = −1.2⁺⁰·⁶₋⁰·⁸); 4.3 μm band.
  - **SO₂ at 3.6σ** (log mass fraction = −3.0⁺⁰·⁵₋⁰·⁷); 4 μm band; **independent of equilibrium chemistry** since equilibrium models do not produce SO₂ at this temperature → photochemistry required. Implies a high-metallicity atmosphere ([[2025_Crossfield_SO2shoreline]], Mukherjee 2024 not ingested).
  - **CH₄ tentative at ~2σ** (Bayes-factor revision lowers from 2.6σ to 2.0σ after removing outlier point at 3.8 μm).
- **Equilibrium-chemistry retrieval** ([[petitRADTRANS]] + [[easyCHEM]]):
  - log Z/Z_⊙ = **1.8⁺⁰·⁴₋⁰·³** (60× solar median, 60–300× solar 3σ range).
  - C/O **< 0.75 (3σ)**; asymptotic to lower values (0.2⁺⁰·⁴₋⁰·¹ median).
  - T_iso = 645⁺¹⁴⁶₋₅₀ K — lower than expected equilibrium 825 K; consistent with morning/evening averaging effect (MacDonald 2020 not ingested).
  - μ = **5.5⁺¹·³₋⁰·⁸ amu** post-processed from posterior (corresponds to ~72 % H₂/He + 20 % H₂O + ~8 % C-bearing species by mass).
- **Free-chemistry retrieval**: μ > 3.5 amu (lower limit; H₂O and CO₂ posterior pushes against upper bounds).
- **Self-consistent forward grid** ([[PICASO]] + [[Photochem]]; 27 models tested; metallicity 1/10/100× solar × C/O 0.3/1.0/2.0 × K_zz 10⁶/10¹⁰/10¹³ cm² s⁻¹):
  - Best fit: **100× solar, C/O = 0.3, K_zz = 10¹⁰ cm² s⁻¹**.
  - With factor-10 boost in S-bearing abundances (renormalized) reaches χ²_ν = 2.53 — comparable to free + equilibrium retrievals at fixed 825 K.
- **Helium 1083 nm escape signal**: **not detected**; **upper limit mass-loss rate < 10¹¹ g s⁻¹** (p-winds; Dos Santos 2022 not ingested) — corresponds to ≲ 0.5 M⊕ lost over 1 Gyr. Consistent with theoretical expectation that high-μ atmospheres suppress atmospheric escape (Yoshida & Gaidos 2025 not ingested).
- **Optical scattering slope** (NIRISS Order 1 + TESS + CHEOPS): strong blueward slope; modelled as Rayleigh + sulfur scattering boost (α = 4.5 power-law). **Soot, Tholin, and Phosphorus haze models excluded at >5σ**; ice-tholin haze excluded at 3σ.
- **Mean molecular weight context**: TOI-1130 b (μ = 5.5) joins [[TOI-270d]] (5.5⁺¹·²₋¹·¹) and [[GJ3470b]] (5.7⁺²·⁰₋¹·⁵) as the third "**miscible-envelope mini-Neptune**" — intermediate μ between low-MMW hot Saturns (HAT-P-26 b at 2.5, HAT-P-11 b at 2.4) and steam envelopes (μ > 10–18).
- **Formation interpretation**:
  - The outer hot Jupiter [[TOI-1130c]] in 2:1 MMR with the mini-Neptune indicates the system **migrated through the disc** rather than via high-eccentricity excitation (Beaugé 2006 not ingested).
  - Hot Jupiter beyond the mini-Neptune orbit **pebble-filters** the inner disc (Bitsch 2021 not ingested) — preventing inner-disc enrichment by inflowing volatiles. If TOI-1130 b accreted *inside* the water ice line, this pebble filter makes its observed high-μ atmosphere very hard to explain.
  - The H₂O + CO₂ detection + low C/O (0.2–0.75) is **consistent with formation beyond the water ice line and migration** (in-situ formation predicts very low C/O ≈ 0 from refractory accretion; Steinmeyer 2026 not ingested).
  - TOI-1130 b sits **at the edge of the radius cliff** (orbital period < 100 d × radius > 3 R⊕ is sparsely populated; Fulton 2017 not ingested, Dattilo 2023 not ingested); a high-μ atmosphere with low atmospheric escape would preserve a planet at the edge of the cliff (Rogers 2025 not ingested).

## Methods

- **JWST observations**:
  - NIRSpec G395H, 2024 Aug 20 — SUB2048, F290LP, NRSRAPID, 8 groups/integration, 2673 integrations, 6 hr.
  - NIRISS SOSS, 2024 Aug 24 — SUBSTRIP256, NISRAPID, 2 groups/integration, 1320 integrations, 6 hr.
- **Reductions**:
  - NIRSpec: [[Eureka]] (Bell 2022 not ingested) + cross-check [[exoTEDRF]] (Radica 2024 not ingested) → consistent within 1σ.
  - NIRISS: [[exoTEDRF]] only (no F277W image so contaminant flagging skipped); 17-pixel half-width box extraction.
- **Light-curve analysis**:
  - White light curves fit with [[batman]] (Kreidberg 2015 not ingested) + linear baseline; quadratic LD from [[ExoTiC-LD]] (Grant & Wakeford 2024 not ingested) fixed.
  - Spectroscopic curves: 50-pixel bins (NIRISS Order 1, NRS1, NRS2); 2 channels for NIRISS Order 2; two fitting methods (full-resolution + common-mode-divide-white-LC) cross-checked.
  - "Kink" in pre-transit NIRISS baseline (likely mirror tilt) handled with wavelength-dependent linear slope.
- **Transit-timing refinement** (essential due to ~2 hr TTV amplitude): 12 [[CHEOPS]] + 20 [[TESS]] sectors 13/27/67/94 + ground-based LCO + ASTEP + MINERVA transits jointly fitted via photodynamical model (Korth 2023 not ingested; Borsato 2024 not ingested).
- **Spectroscopic retrievals**:
  - Free chemistry: [[petitRADTRANS]] + emcee (50 walkers × 15 000 steps); 9 species (H₂O, CH₄, CO, CO₂, SO₂, NH₃, HCN, H₂S, CS₂) + jitter + offset.
  - Equilibrium chemistry: petitRADTRANS + [[easyCHEM]] (Mollière 2017 not ingested) at fixed isothermal T (free / fixed 825 K / fixed 625 K).
  - Cross-check: [[PLATON]] (Zhang 2020 not ingested) free retrieval — consistent within 1σ.
- **Self-consistent grid**: [[PICASO]] + [[Photochem]] (Wogan 2023 not ingested) on 27 models; UV irradiation from MUSCLES HD 85512 (France 2016 not ingested) rescaled to TOI-1130's T_eq = 825 K.
- **Haze modelling**: [[VIRGA]] (Batalha 2025 not ingested) with 26 nm median radius, 15–60 nm span; tested Titan-tholin, soot, ice-tholin, Saturn-phosphorus haze species (Khare 1984; Lavvas & Koskinen 2017; Khare 1993; Noy 1981 — all not ingested).
- **Helium 1083 nm**: 20-pixel half-width centered on He line; continuum-normalized; compared to [p-winds](https://github.com/ladsantos/p-winds) (Dos Santos 2022 not ingested) at 8000 K / 10000 K upper-atmosphere × 10⁹ / 10¹⁰ / 10¹¹ g s⁻¹.

## Caveats & limitations

- **Free retrieval pushes H₂O and CO₂ posteriors against the upper prior bounds** — interpreted as a μ lower-limit rather than a tight constraint. Equilibrium-chemistry posterior is better-determined.
- **Equilibrium chemistry does not produce SO₂** at 825 K — SO₂ detection is a robust independent indicator of disequilibrium photochemistry but the free-retrieval SO₂ abundance (~10⁻³ mass fraction) is ~5× higher than the [[Photochem]] grid prediction (~10⁻⁴ to 10⁻³ requires a 10× sulfur boost).
- **Optical slope strength** at the short-wavelength end is partially driven by NIRISS Order 1 outlier points between 2.3–2.7 μm; sensitivity test removing them does not change the bulk metallicity result.
- **Isothermal-T retrieval gives 600–650 K rather than 825 K** — likely an artifact of morning/evening averaging (MacDonald 2020 not ingested); fixing T = 825 K gives consistent abundance results with slightly worse χ²_ν.
- **C/O ratio is asymptotic, not Gaussian-distributed**: 3σ upper limit 0.75 is the robust statement; the median 0.2 should be treated as indicative.
- **Helium non-detection** could reflect either (a) genuinely low escape due to high μ, or (b) cold thermospheric temperatures (< 8000 K) suppressing the metastable line — degenerate without UV spectroscopy of the host.
- **CHEOPS faintness**: TOI-1130 is faint for CHEOPS; data were reprocessed with PIPE (PSF photometry) rather than the default DRP pipeline.

## Open questions / follow-ups

- **Confirm CH₄ detection** at higher S/N — currently 2σ tentative; would discriminate between fully-equilibrium chemistry (C/O = 0.3 produces some CH₄) and aggressively photochemistry-suppressed (Mukherjee 2024 not ingested) atmospheres.
- **NIRISS Order 2 + UV spectroscopy** to confirm the SO₂ photochemistry and constrain UV-driven mass-loss explicitly.
- **Constraints on TOI-1130c**: does the outer hot Jupiter show similarly enriched composition consistent with co-migration through the ice line, or is it H/He-dominated?
- **Quadratic A_H^H₂O scale-height-metric trend** (Brande 2024 not ingested) — TOI-1130 b lies just below the best-fit quadratic; including planets > 1000 K weakens the trend significantly. Whether the trend is fundamental or driven by silicate-condensate physics at 1000–1500 K is the key open question.
- **Mini-Neptune formation-history heterogeneity**: TOI-1130 b joins [[TOI-270d]] and [[GJ3470b]] as a third miscible-envelope mini-Neptune; the population may have multiple formation channels (ex-situ + in-situ + interior–atmosphere interactions).
- **Magma-atmosphere interactions** (Lichtenberg 2025, Dorn & Lichtenberg 2021 — not ingested): TOI-1130 b's ~25 % envelope mass fraction puts it at the transition where magma may solidify — current models predict it does, breaking the explanation by interior outgassing.

## Related

- [[2025_Barat_V1298Tau-b]] — same lead author; young sub-Neptune analog at much higher S/N (CO₂ at 35σ, H₂O at 30σ) but with substellar metallicity (~0.6× solar) — opposite end of the mini-Neptune metallicity spectrum.
- [[2025_Felix_TOI-270d]], [[2025_Coulombe_TOI-270b]] — same multi-planet sub-Neptune comparison class; TOI-270 d also has μ ≈ 5.5; **but no SO₂ detection** there. Compositional contrast worth tracking.
- [[2025_Gressier_HATP26b]] — comparable warm Neptune-mass exoplanet with SO₂ detection (lnB = 13.46); higher-mass analog of TOI-1130 b.
- [[2025_Crossfield_SO2shoreline]] — population framework for SO₂ in sub-Neptune to hot-Jupiter regime; TOI-1130 b extends the SO₂-positive sample to mini-Neptune class.
- [[2025_Madhusudhan_subneptunes]] — the sub-neptune-classification scheme. TOI-1130 b is comfortably in the "**miscible-envelope mini-Neptune**" category (T_eq > 350 K).
- [[2025_Roy_LP791-18c]], [[K2-18b]] — comparator temperate sub-Neptunes; TOI-1130 b is hotter (825 K vs 280–355 K) and joins these as a third compositional point.
- Concept: [[SO2-photochemical-shoreline]] — TOI-1130 b is a new positive-SO₂ data point at T_eq = 825 K / [M/H] ≈ 60× solar.
- Program: [[JWST-GO-3385]] (new — first wiki entry).
