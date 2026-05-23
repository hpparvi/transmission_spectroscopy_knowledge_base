---
type: instrument
aliases: [NIRSpec, JWST/NIRSpec]
tags: [jwst, near-infrared, spectrograph, hub]
---

# JWST-NIRSpec

The Near-Infrared Spectrograph on JWST (Birkmann et al. 2022, Jakobsen et al. 2022; not yet ingested), providing 0.6–5.3 μm spectroscopy. The dominant JWST instrument for exoplanet transmission spectroscopy in this wiki — present in 19 of the 28 papers — and the workhorse for both small-planet rocky-world programs and the WASP-39 b ERS benchmark.

## Modes

- **G395H** (2.8–5.2 μm, R ≈ 2700): Two detectors **NRS1** (≲3.7 μm) and **NRS2** (≳3.8 μm) separated by a physical gap. The default BOTS configuration for K- and M-dwarf super-Earth and sub-Neptune programs (especially [[JWST-GO-2512-COMPASS]]). Probes CO₂ at 4.3 μm, CO at 4.7 μm, SO₂ at 4.05 μm, H₂O across both detectors.
- **G395M** (2.9–5.2 μm, R ≈ 1000): Lower resolution; **single detector with no NRS1/NRS2 gap**. [[2025_Bennett_GJ1132b]] is the first wiki demonstration of combining G395H + G395M to fill the gap.
- **PRISM** (0.6–5.3 μm, R ≈ 100): Single dispersion, single detector. The standard for ultracool-dwarf hosts (TRAPPIST-1, L 98-59 from GTO 1224) where photon SNR is the limit and broad wavelength coverage is needed in one shot. The ERS WASP-39 b benchmark mode.
- **G235H, G235M, G140H, G140M, NIRSpec/IFU**: not yet appearing as primary modes in any wiki paper.

## History

- **Cycle 1 baseline (2023).** [[2023_Lustig-Yaeger_LHS475b]] establishes that NIRSpec G395H has no noise floor above 5 ppm on an Earth-sized rocky planet. [[2023_May_GJ1132b]] and [[2023_Moran_GJ486b]] document the NRS1/NRS2 superbias / detector-offset systematic that has shaped subsequent small-planet work. ERS WASP-39 b PRISM data (original ERS papers; not yet ingested) define the benchmark for hot Jupiters.
- **COMPASS small-planet survey ([[JWST-GO-2512-COMPASS]]).** Standardizes G395H two-visit reductions on rocky super-Earths and sub-Neptunes: [[2024_Alderson_TOI-836b]], [[2024_Scarsdale_L98-59c]], [[2025_Alderson_TOI-776b]], [[2025_Teske_TOI776c]], [[2025_Redai_GJ357b]].
- **TRAPPIST-1 PRISM era (2025).** A cluster of TRAPPIST-1 papers stress-tests PRISM on the most challenging stellar-contamination targets: [[2025_Espinoza_TRAPPIST1e]], [[2025_Glidden_TRAPPIST1e]], [[2025_PiauletGhorayeb_TRAPPIST1d]], [[2025_Rathcke_TRAPPIST1bc]]. Stellar-model fidelity is identified as the dominant systematic (~1800 ppm) over photon precision (~89 ppm) on these hosts.
- **Multi-mode and multi-instrument coadds (2025).** [[2025_Bennett_GJ1132b]] combines G395H + G395M; [[2025_Alam_L168-9b]] combines G395H + MIRI/LRS for the first broadband 3–12 μm rocky-planet transmission spectrum.
- **Methodology critique (2026).** [[2026_RoyPerez_WASP39b]] documents up to 2 dex pipeline-induced variation in retrieved abundances on the same NIRSpec PRISM ERS WASP-39 b dataset.

## Trade-offs

- **G395H vs G395M.** G395H has higher resolution (R ≈ 2700 vs 1000) but the NRS1/NRS2 gap excises ~3.7–3.85 μm, missing the CH₄ Q-branch. G395M fills that gap at lower R; combining the two modes is the [[2025_Bennett_GJ1132b]] solution. For faint M-dwarf hosts where NRS2 photon SNR is poor, G395M is increasingly preferred ([[2023_May_GJ1132b]] argues this point).
- **PRISM vs G395H on cool hosts.** PRISM gives 0.6–5.3 μm coverage in a single visit but at R ≈ 100. For ultracool dwarfs where stellar contamination dominates the blue and stellar-model fidelity is poor, the broad coverage helps disambiguate atmosphere from photosphere — but only if stellar models keep up.
- **Detector-offset systematic.** Multiple G395H papers ([[2023_May_GJ1132b]], [[2023_Moran_GJ486b]], [[2025_Alderson_TOI-776b]]) document a per-visit NRS1/NRS2 transit-depth offset of order tens of ppm, requiring per-paper correction. Not yet handled uniformly across pipelines.
- **No noise floor above 5 ppm.** The strongest argument for NIRSpec on small planets ([[2023_Lustig-Yaeger_LHS475b]]); compares favorably to NIRISS where systematic floors have been reported.

## Open issues

- **NRS1/NRS2 detector offsets.** Several papers document them; no community standard for correction. Likely candidate for a future calibration product.
- **Stellar models in PRISM mode for late-M dwarfs.** Identified as the dominant error budget for TRAPPIST-1 and similar; flagged in [[2025_Espinoza_TRAPPIST1e]], [[2025_Glidden_TRAPPIST1e]].
- **Pipeline-induced retrieval variation.** [[2026_RoyPerez_WASP39b]] shows up to 2 dex on PRISM data; G395H-mode equivalents not yet quantified.

## Papers

### PRISM
- [[2026_RoyPerez_WASP39b]] — WASP-39 b ERS data-reduction systematics across four pipelines / six reductions.
- [[2025_LibbyRoberts_Kepler51d]] — first PRISM 0.6–5.3 μm transmission of a [[super-puff]]; sloped near-featureless spectrum; high-altitude photochemical haze.
- [[2025_PiauletGhorayeb_TRAPPIST1d]] — two PRISM transits of TRAPPIST-1 d; flat; H₂ excluded >3σ; N₂-rich consistent.
- [[2025_Espinoza_TRAPPIST1e]] — four PRISM transits of TRAPPIST-1 e; GP contamination marginalization; H₂-rich excluded >3σ.
- [[2025_Glidden_TRAPPIST1e]] — four PRISM transits of TRAPPIST-1 e; thick CO₂ ruled out at 6.9σ; stellar-model fidelity bottleneck.
- [[2025_Rathcke_TRAPPIST1bc]] — back-to-back PRISM transits of TRAPPIST-1 b + c (0.87–4.37 μm); empirical contamination correction.

### G395H
- [[2025_Teske_TOI561b]] — four G395H secondary eclipses of TOI-561 b; thick-atmosphere evidence.
- [[2025_Fisher_TOI1685b]] — five G395H transits of TOI-1685 b; bare rock.
- [[2025_Alam_L168-9b]] — three G395H transits of L 168-9 b combined with MIRI/LRS.
- [[2025_Alderson_TOI-776b]] — two G395H transits of TOI-776 b; flat after detector-offset correction.
- [[2025_Teske_TOI776c]] — two G395H transits of TOI-776 c.
- [[2025_Redai_GJ357b]] — single G395H transit of GJ 357 b (COMPASS).
- [[2024_Scarsdale_L98-59c]] — two G395H transits of L 98-59 c under COMPASS.
- [[2024_Gressier_L98-59d]] — single G395H transit of L 98-59 d (GTO 1224); 2.6σ–5.6σ atmospheric feature.
- [[2024_Banerjee_L98-59d]] — retrievals on the same GTO 1224 G395H transit.
- [[2024_Alderson_TOI-836b]] — two G395H transits of TOI-836 b; flat.
- [[2023_May_GJ1132b]] — two G395H transits of GJ 1132 b; discusses NRS1/NRS2 offsets.
- [[2023_Moran_GJ486b]] — two G395H transits of GJ 486 b; identifies NRS2 Transit-1 superbias offset.
- [[2023_Lustig-Yaeger_LHS475b]] — two G395H transits of LHS 475 b; no noise floor above 5 ppm.

### G395H + G395M
- [[2025_Bennett_GJ1132b]] — first wiki demonstration of combining G395H + G395M to fill the NRS1/NRS2 gap on GJ 1132 b.

### G395H emission / nightside (hot Jupiter)
- [[2025_LustigYaeger_WASP17b]] — back-to-back G395H transit + secondary eclipse of WASP-17 b; first JWST nightside emission spectrum extracted via iESR-PIE.
- [[2025_Sikora_HD80606b]] — 20.9-hr partial phase curve of highly eccentric hot Jupiter HD 80606 b at periapse; first wiki demonstration of NIRSpec G395H phase-resolved emission spectroscopy with time-variable atmospheric chemistry.

### G395H transit (hot-Jupiter / sub-Saturn / Neptune)
- [[2026_Radica_WASP96b]] — single G395H transit of the inflated hot Saturn WASP-96 b combined with archival NIRISS/SOSS + VLT/FORS2.
- [[2025_Gressier_HATP26b]] — single G395H transit of the warm Neptune-mass HAT-P-26 b under JWST-TST DREAMS GTO 1312; SO₂ at lnB = 13.46; first SO₂ in a Neptune-mass exoplanet.
- [[2025_Ahrer_KELT7b]] — single G395H transit of aligned hot Jupiter KELT-7 b under BOWIE-ALIGN GO 3838; weak features only; high cloud deck or low metallicity ambiguity; mirror tilt event mid-observation modeled as step function.
- [[2025_Ahrer_WASP94Ab]] — single G395H transit of misaligned hot Jupiter WASP-94 Ab under GO 3154; CO₂ at 11σ, H₂O at 4σ, tentative CO + H₂S; substellar C/O = 0.49 vs host C/O★ = 0.68; formation-tracer benchmark for above-the-Kraft-break sample.
- [[2025_Gapp_WASP121b]] — G395H transit-only extraction from the GO-1729 phase curve of ultra-hot Jupiter WASP-121 b; first definitive [[SiO]] identification at 5.2σ; introduces a custom dayside/nightside split [[NEMESISPY]] retrieval to handle [[thermal-dissociation]].

### G395H + NIRISS SOSS (sub-Neptune)
- [[2025_Felix_TOI-270d]] — joint G395H + NIRISS SOSS reanalysis of GO 4098 transits of temperate sub-Neptune TOI-270 d; demonstrates that **native-resolution retrieval with LSF convolution** is essential for sub-Neptune chemistry inference (binning to ≲16 px biases Bayes factors).
- [[2025_FernandezRodriguez_K2-18b]] — joint G395H + NIRISS SOSS reanalysis of GO 2722 transits of K2-18 b; CH₄ robust at ~4σ; CO₂ marginal at ~2σ; DMS retracted in comprehensive 13-species retrievals.
- [[2025_Luque_K2-18b]] — joint G395H + NIRISS SOSS + MIRI/LRS retrieval of K2-18 b across three reductions and two retrieval frameworks; DMS/DMDS not preferred panchromatically; ethane is an equally good explanation.
- [[2025_PicaCiamarra_K2-18b]] — joint G395H + NIRISS SOSS + MIRI/LRS 650-molecule agnostic search for K2-18 b; only 3 species reach ≥2.5σ in NIR (DMS, diethyl sulfide, methacrylonitrile).

### G395H — sub-Earth (rocky M-dwarf)
- [[2025_BelloArufe_L98-59b]] — **four NIRSpec G395H transits of L 98-59 b** under [[JWST-GO-3942]]; smallest exoplanet with a JWST transmission spectrum (R_p = 0.85 R⊕); SO₂-rich [[volcanic-atmosphere]] preferred at 3.3–3.8σ across [[ExoTR]], [[Aurora]], [[POSEIDON]].

### G395H — super-Jupiter (F-star)
- [[2025_Liu_HATP14b]] — JWST commissioning NIRSpec G395H ([[JWST-PID-1118]]) + NIRISS SOSS of the super-Jupiter HAT-P-14 b; reanalysis with updated pipeline reveals small water bumps at 1.4 / 1.9 / 2.6 μm; H₂O detected at 3.09σ.
- [[2025_Ahrer_GJ3090b]] — joint G395H + NIRISS SOSS analysis of warm sub-Neptune GJ 3090 b under GO 4098; first JWST sub-Neptune He I detection; NIRISS dominated by transit-light-source effect across two visits 6 months apart.

### G395M (sub-Saturn / panchromatic)
- [[2026_Heinke_HATP12b]] — G395M transit of HAT-P-12 b combined with NIRISS+MIRI+HST in an information-content study.

### PRISM (gas-giant on M-dwarf, GEMS class)
- [[2026_Ashtari_HATS75b]] — three PRISM transits of the M-dwarf-hosted gas giant HATS-75 b; first GEMS PRISM application; atmosphere/contamination degenerate.
- [[2025_Canas_TOI5205b]] — three PRISM transits of the M4-dwarf-hosted gas giant TOI-5205 b under [[JWST-GO-3171]] (Red Dwarfs and Seven Giants); CH₄ + H₂S detected; >20σ stellar contamination + spot-crossing events in all 3 visits; second GEMS PRISM characterization.

### G395H — limb-resolved & young-planet
- [[2025_Murphy_WASP107b]] — G395H limb-resolved transit of WASP-107 b biased by occulted starspot crossings; corrected via [[Catwoman]] injection-recovery; offsets −195 ppm evening / +240 ppm morning bring it into agreement with NIRCam.
- [[2025_Barat_V1298Tau-b]] — G395H/SUB2048 transit of the young (10–30 Myr) sub-Neptune progenitor V1298 Tau b; in-transit stellar flare requires data-driven detrending; CO₂ at 35σ + H₂O at 30σ + CO at 10σ + CH₄ at 6σ + SO₂ at 4σ; first wiki target with NIRSpec characterization of a < 50 Myr planet.

### G395M
- [[2025_Deka_WASP39b]] — note: the [[NEXOTRANS]] paper applies retrievals to NIRSpec **PRISM** WASP-39 b ERS data (5–5.5 μm overlap with MIRI), not G395M.
