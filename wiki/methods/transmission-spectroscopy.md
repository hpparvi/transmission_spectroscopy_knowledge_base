---
type: method
aliases: [transit spectroscopy, transmission spectrum measurement]
tags: [observational-technique, core-method, hub]
---

# Transmission spectroscopy

Measurement of a transiting planet's apparent radius as a function of wavelength. The wavelength-dependent transit depth — the [[transmission-spectrum]] observable — encodes absorption by atmospheric species along the day–night terminator chord, modulated by the cloud-top pressure, scale height (hence temperature), and any [[stellar-contamination]] from unocculted photospheric heterogeneities. The dominant atmospheric-characterization technique in this wiki: 27+ ingested papers use it as their primary observable, spanning rocky planets through hot Jupiters and from HST/WFC3 through every JWST mode.

In practice: fit spectroscopic light curves in narrow wavelength bins, extract Rp/R⋆(λ), and compare to forward models or perform [[atmospheric-retrievals]]. Sensitive to absorbers above the limb cloud deck.

## Foundational theory

- **[[2000_Seager_TheoryTransmission]]** — Seager & Sasselov 2000 establishes the geometric framework of stellar flux passing through an optically thin "transparent atmosphere" above the cloud-top, predicts absorption features at the ~10⁻⁴ to ~10⁻³ level relative to total stellar flux, and identifies the Na I D doublet at 589.4 nm as the strongest expected feature on HD 209458 b. Motivates the historic Charbonneau et al. 2002 first-detection (HST/STIS; not yet ingested).
- **[[2001_Brown_TransmissionDiagnostics]]** — Brown 2001 introduces the formal "spectrum ratio" R(λ) = F_transit/F_out as the natural observable, parameterizes cloud decks, and adds Doppler diagnostics from winds and rotation plus Na/K UV photoionization. Defines the diagnostic catalog (cloud height, metallicity, T(P), winds) the field still uses.

## Variants

- **HST WFC3 G141 spatial-scanning.** The pre-JWST workhorse for 1.1–1.7 μm; defines the H₂O 1.4 μm feature era. [[2014_McCullough_HD189733b]] (HD 189733 b H₂O detection at 1.4 μm) is the canonical wiki example; [[2021_Mugnai_GJ1132b]] applies it to a rocky M-dwarf planet.
- **HST UV-to-NIR panchromatic transmission (pre-JWST archetype).** [[2013_Pont_HD189733b]] combines HST/STIS + ACS + WFC3 + NICMOS + Spitzer/IRAC + Spitzer/MIPS for a 0.3–24 μm coherent spectrum on HD 189733 b — the pre-JWST gold standard for panchromatic coverage and the dataset against which JWST hot-Jupiter spectra are still benchmarked.
- **JWST single-mode transits** — the core JWST configuration. [[JWST-NIRSpec]] G395H/G395M/PRISM, [[JWST-NIRISS]] SOSS, [[JWST-MIRI]] LRS each appear as primary instruments across the wiki.
- **Panchromatic multi-instrument transits** — [[2026_Radica_WASP96b]] (NIRSpec + NIRISS + VLT/FORS2 on WASP-96 b), [[2026_Heinke_HATP12b]] (NIRISS+NIRSpec G395M+MIRI/LRS+HST/STIS+WFC3 on HAT-P-12 b), [[2025_Alam_L168-9b]] (NIRSpec G395H + MIRI/LRS — first broadband 3–12 μm on a rocky planet).
- **Multi-visit single-mode coadds.** Standard for rocky M-dwarf planets where per-visit SNR barely matches expected feature amplitude — see [[multi-visit-stacking]]. Examples: [[2025_Bennett_GJ1132b]] (4 visits), [[2025_Fisher_TOI1685b]] (5 visits), [[2025_Espinoza_TRAPPIST1e]] / [[2025_Glidden_TRAPPIST1e]] (4 visits each).
- **Disintegrating-planet "transmission".** [[2025_Tusay_K2-22b]] applies MIRI/LRS to K2-22 b's variable dust/gas tails; depths span 0–1627 ppm across four windows — probes escaping material rather than a retained atmosphere.
- **Limb-resolved transmission.** Asymmetric two-semicircle transit-light-curve fitting ([[Catwoman]]) recovers separate morning-limb and evening-limb spectra. [[2025_Fu_limb-asymmetry]] applies this to all nine published JWST/NIRISS/SOSS hot-Jupiter datasets and finds 3/9 show > 5σ morning–evening 1.4 μm water-band contrast — see [[limb-asymmetry]].

## Trade-offs

- **Vs. emission/eclipse spectroscopy.** Transmission probes the terminator at low pressures; emission probes the dayside at higher pressures. Transmission is sensitive to light absorbers and high-altitude hazes; emission constrains thermal structure and surface conditions. The two are increasingly used as complementary arbiters of the same target — see [[secondary-eclipse-spectroscopy]] and the canonical pairing on [[GJ486b]].
- **[[stellar-contamination]] as primary confounder.** On M-dwarf hosts the transit chord is biased relative to the disk-average photosphere, generating wavelength-dependent features that mimic absorption (transit light source effect). Almost every M-dwarf paper in the wiki addresses this as the leading systematic. The same effect is now understood to be a viable alternative to a Rayleigh-scattering haze on active K-dwarf hot-Jupiter hosts ([[2014_McCullough_HD189733b]], [[2019_Rackham_TLS-FGK]]) — recorded as a tension on the [[HD-189733b]] hub.
- **Multi-visit requirement on small planets.** Single-visit "tentative detections" of CH₄ and H₂O have been retired by multi-visit follow-up on [[GJ1132b]] (Visit 1 → 4-visit coadd) and indirectly on [[GJ486b]] (transmission → emission). Single-visit small-planet claims are no longer credible.
- **Pipeline-induced retrieval variation.** [[2026_RoyPerez_WASP39b]] documents up to 2 dex pipeline-induced variation in retrieved abundances on the same WASP-39 b ERS PRISM dataset — pipeline choice is itself a non-trivial systematic for transmission spectroscopy.
- **Limb-averaging bias.** Limb-averaged retrievals on planets with strong morning–evening aerosol asymmetry **inflate metallicity by up to +2 dex and deflate temperature by up to ½×** ([[2025_Fu_limb-asymmetry]] Eq. 3, after Line & Parmentier 2016). Documented on [[WASP-39b]], [[WASP-94Ab]], [[WASP-17b]] — see [[limb-asymmetry]].

## Open issues

- **NRS1/NRS2 detector offsets** on G395H ([[JWST-NIRSpec]]) — per-paper corrections; no community standard.
- **Stellar-model fidelity floor** on ultracool dwarfs (~1800 ppm/pixel for TRAPPIST-1) exceeds observational precision (~89 ppm); flagged in [[2025_Glidden_TRAPPIST1e]] as the dominant systematic.
- **MMW inferences from featureless spectra** are model-dependent (equilibrium vs mixture priors span 2.8–7.7 g mol⁻¹ on TOI-776 c — [[2025_Teske_TOI776c]]).

## Papers

### Foundational theory
- [[2000_Seager_TheoryTransmission]] — Seager & Sasselov 2000.
- [[2001_Brown_TransmissionDiagnostics]] — Brown 2001.

### Limb-resolved population study
- [[2025_Fu_limb-asymmetry]] — Fu et al. 2025, ApJL 989:L17 — uniform NIRISS/SOSS reanalysis of nine hot Jupiters; 3/9 (WASP-39 b, WASP-94 Ab, WASP-17 b) show > 5σ muted-morning / clear-evening 1.4 μm water contrast; introduces LSM and asymmetry horizon.

### Hot Jupiter / sub-Saturn / Neptune / GEMS — multi-instrument
- [[2025_Gressier_HATP26b]] — single NIRSpec G395H transit of warm Neptune-mass HAT-P-26 b (JWST-TST DREAMS GTO 1312); H₂O, CO₂, SO₂ detected; ~10× solar metallicity; subsolar C/O = 0.14.
- [[2025_Ahrer_KELT7b]] — single NIRSpec G395H transit of aligned hot Jupiter KELT-7 b (BOWIE-ALIGN GO 3838); weak/tentative H₂O + CO₂; high-altitude cloud deck or low-metallicity atmosphere; third BOWIE-ALIGN target.
- [[2026_Radica_WASP96b]] — NIRSpec G395H + NIRISS/SOSS + VLT/FORS2 on WASP-96 b; H₂O, CO₂, Na, tentative SO₂.
- [[2026_Heinke_HATP12b]] — NIRISS+NIRSpec G395M+MIRI/LRS+HST panchromatic on HAT-P-12 b.
- [[2026_Ashtari_HATS75b]] — three NIRSpec PRISM transits of GEMS gas giant HATS-75 b.
- [[2025_Crouzet_HATP12b]] — single NIRSpec G395M transit + archival HST WFC3 on HAT-P-12 b.

### Disintegrating planet
- [[2025_Tusay_K2-22b]] — four MIRI/LRS windows; one 9.7σ detection.

### Pre-JWST HST workhorse
- [[2021_Mugnai_GJ1132b]] — five HST WFC3 G141 transits of GJ 1132 b; flat 1.1–1.6 μm.

### Rocky M-dwarf planets — multi-visit JWST
- [[2025_Fisher_TOI1685b]] — five G395H transits; bare rock.
- [[2025_Bennett_GJ1132b]] — four G395H + G395M transits; flat coadd retires Visit-1 inference.
- [[2025_Espinoza_TRAPPIST1e]] — four PRISM transits + GP contamination marginalization.
- [[2025_Glidden_TRAPPIST1e]] — four PRISM transits; thick CO₂ ruled out at 6.9σ.
- [[2025_PiauletGhorayeb_TRAPPIST1d]] — two PRISM transits; H₂ excluded > 3σ.
- [[2025_Rathcke_TRAPPIST1bc]] — back-to-back PRISM transits + empirical contamination correction.
- [[2025_Howard_TRAPPIST1_flares]] — flare-mitigated NIR transmission of TRAPPIST-1 b/c/f/g.
- [[2023_Lim_TRAPPIST1b]] — two NIRISS/SOSS transits; H₂ rejected at 16–29σ.

### Rocky M-dwarf planets — single-mode JWST
- [[2025_Alam_L168-9b]] — first 3–12 μm broadband (NIRSpec G395H + MIRI/LRS).
- [[2025_Alderson_TOI-776b]] — two G395H transits.
- [[2025_Teske_TOI776c]] — two-visit G395H sub-Neptune.
- [[2025_Redai_GJ357b]] — single G395H COMPASS transit.
- [[2025_Taylor_GJ357b]] — first NIRISS/SOSS transmission spectrum in the wiki (partial transit).
- [[2024_Scarsdale_L98-59c]] — two-visit G395H COMPASS.
- [[2024_Gressier_L98-59d]] — single G395H transit; sulfur-rich atmosphere preferred 2.6σ–5.6σ.
- [[2024_Banerjee_L98-59d]] — companion retrievals on the same transit.
- [[2024_Alderson_TOI-836b]] — two-visit G395H COMPASS.
- [[2023_May_GJ1132b]] — two G395H transits, three reductions.
- [[2023_Moran_GJ486b]] — two-visit G395H; degenerate with stellar contamination.
- [[2023_Lustig-Yaeger_LHS475b]] — first JWST transmission of an Earth-sized planet.

### Sub-Neptune
- [[2025_Roy_LP791-18c]] — temperate sub-Neptune; CH₄ + haze, no CO₂.
- [[2025_Felix_TOI-270d]] — temperate sub-Neptune; NIRSpec G395H + NIRISS SOSS reanalysis; CH₄ + CO₂ decisive, tentative CS₂; SO₂ retracted; methodology argument for native-resolution + LSF retrieval.
- [[2025_FernandezRodriguez_K2-18b]] — habitable-zone sub-Neptune; NIRISS SOSS + NIRSpec G395H reanalysis; CH₄ at ~4σ; CO₂ marginal at ~2σ; DMS retracted; supersolar C/O ≈ 10–13 supports Inside-Out Planet Formation.
- [[2025_Barat_V1298Tau-b]] — JWST/NIRSpec G395H + HST/WFC3 panchromatic 1.0–5.2 μm transmission of the **young (10–30 Myr) sub-Neptune progenitor V1298 Tau b**; CO₂ at 35σ + H₂O at 30σ + CO at 10σ + CH₄ at 6σ + SO₂ at 4σ + tentative OCS; haze-free H/He atmosphere with metallicity ~0.6× solar and subsolar C/O ≈ 0.22; the lack of CH₄ relative to chemical-equilibrium expectations requires high internal temperature ~500 K — inconsistent with formation/evolution models predicting ~100–200 K; demonstrates **mass measurement from atmospheric scale height** (12 ± 1 M⊕, ~10% precision) for a young active host.

### Hot Jupiter — panchromatic + limb-resolved
- [[2025_Murphy_WASP107b]] — JWST 1–12 μm panchromatic limb-resolved transmission of WASP-107 b (NIRCam F322W2 + F444W, NIRISS/SOSS, NIRSpec G395H, MIRI/LRS); confirms ~180 K evening–morning T gradient and **resolves chemical heterogeneity** between limbs (5× SO₂, 40× CO₂, uniform H₂O, broad 6–11 μm cloud only on morning limb); develops [[stellar-contamination-modeling]] correction for occulted-starspot bias on limb-resolved spectra.
