---
type: paper
bibkey: 2025_Felix_TOI-270d
authors: [Felix, L., Kitzmann, D., Demory, B.-O., Mordasini, C.]
year: 2025
venue: A&A
arxiv: 2509.04003
doi: 10.1051/0004-6361/202555194
targets: [TOI-270d]
instruments: [JWST-NIRSpec, JWST-NIRISS]
methods: [transmission-spectroscopy, atmospheric-retrievals]
species_detected: [CH4, CO2]
species_tentative: [CS2, NH3]
species_ruled_out: [SO2, CO, H2S, OCS]
codes: [Eureka, BeAR, HELIOS-K, MultiNest]
tags: [sub-neptune, sulfur-chemistry, methyl-chemistry, line-spread-function, data-binning-systematics, native-resolution-retrieval]
ingested: 2026-05-03
---

# Competing chemical signatures in the atmosphere of TOI-270 d: Inference of sulfur and carbon chemistry

**Authors:** Felix, Kitzmann, Demory, Mordasini (2025, A&A 701:A296)
**Targets:** [[TOI-270d]] · **Instruments:** [[JWST-NIRSpec]] G395H + [[JWST-NIRISS]] SOSS · **Program:** [[JWST-GO-4098]] (PI: Benneke & Evans-Soma)

## TL;DR

An independent reanalysis of the JWST GO 4098 NIRSpec G395H + NIRISS SOSS transit observations of the temperate sub-Neptune TOI-270 d (T_eq = 340 K, R = 2.16 R⊕, M = 4.97 M⊕). Custom Eureka! reduction + custom MCMC light-curve fitting + the [[BeAR]] retrieval framework (Bern Atmospheric Retrieval; the renamed HELIOS-R2). **Reproduces** Benneke et al. 2024 (not yet ingested) — H₂/He-dominated atmosphere with mean molecular weight 5.56 amu and metallicity ~160× solar — but **cannot reproduce** the lower-MMW, higher-T_p hycean-world solution of Holmberg & Madhusudhan 2024 (not yet ingested). Decisive detections of [[CH4]] (Bayes factor 3 × 10²⁵) and [[CO2]] (3 × 10⁷). Moderate evidence for [[CS2]] (Bayes factor 78); weak evidence for [[NH3]] (4); H₂O surprisingly low (~10⁻⁴, consistent with condensation below the probed pressures). The CS₂ signal at 4.6 μm is degenerate with methyl chloride (CH₃Cl) and methyl fluoride (CH₃F), which produce nearly identical opacity in the JWST band — Bayesian inference cannot statistically distinguish among CS₂, CH₃Cl, CH₃F, or H₂CS scenarios. **Critical methodology finding:** atmospheric retrievals must run at native instrument resolution with a forward-model line-spread-function convolution; binning data to ≲16 pixels biases the Bayes factors and produces unphysical solutions. SO₂ is **not detected**, contradicting tentative claims by Benneke et al. 2024.

## Key findings

- **Mean molecular weight = 5.56 ± 1.10 amu** for the fiducial model — places TOI-270 d firmly in the **metal-rich miscible-envelope** category (Benneke 2024 framing) rather than the hycean (low-MMW) regime (Holmberg & Madhusudhan 2024).
- **CH₄ decisive** (Bayes factor 3 × 10²⁵ at native resolution); log VMR ≈ −1.7. CO₂ decisive (Bayes factor 3 × 10⁷); log VMR ≈ −1.3.
- **High CO₂/CH₄ ratio** in this reduction vs. Benneke 2024's lower CO₂/CH₄ ratio — first systematic difference flagged.
- **Strong sulfur signal at 4.6 μm.** Best-fit fiducial sulfur model includes CS₂ (log VMR ≈ −2.13; Bayes factor 78), with CS upper limit ~10⁻⁵ and H₂S/SH/OCS ≲ 10⁻⁵; SO₂ < 10⁻⁵ (3σ upper limit).
- **CS₂ vs CH₃Cl/CH₃F/H₂CS degeneracy.** All four species produce essentially identical absorption opacity over 1–4 μm; cannot be distinguished by current data. Distinguishability requires MIRI/LRS or MRS at 8/10/14 μm (paper Fig. 10).
- **DMS not preferred.** Tested following [[K2-18b]] (Madhusudhan et al. 2023; not yet ingested) framing; Bayes factor < 1 vs sulfur model.
- **H₂O strongly low (~10⁻⁴; Bayes factor 1).** Suggests condensation below the probed pressures (T = 360 K is above water condensation at typical sub-Neptune pressures, but the lower atmosphere is not constrained); this is a methodological finding — H₂O is essentially "non-detected" in the upper atmosphere despite the high inferred metallicity.
- **Holmberg & Madhusudhan 2024 not reproduced.** Their atmosphere has T = 300 K (vs. 360 K), 5.56 amu MMW (vs. ~2 amu), and ~160× solar (vs. ~10× solar) — but Felix et al. cannot match their data reduction or retrieval result with their own framework. Tension flagged.
- **Mass-consistency check.** The 4.97 ± 0.56 M⊕ derived from the retrieval matches Van Eylen et al. 2021 (4.78 ± 0.43 M⊕) without additional non-absorbing background species — supporting the metal-rich envelope model. Holmberg & Madhusudhan 2024's MMW = 2.0 amu would require N₂ as a non-absorbing background to match the mass — inconsistent with their reported [Fe/H].
- **Native-resolution retrieval is essential.** Binning data to bins of 2, 4, 8, or even 16 pixels biases the molecular-abundance posteriors and the Bayes factors significantly (Fig. 5). Using R ≈ 50 binning (as Benneke 2024 did) hides the bimodal posterior for CS₂ that becomes apparent at native resolution. The Bayes factor for CS₂ varies from 31 (R≈50) to 31,000 (16-pixel) to 78 (full LSF) — large enough to flip detections in either direction.
- **NRS1/NRS2 detector offset retrieved at −14 ± 13 ppm** (consistent with zero); NIRISS/NRS1 offset −42 ± 9 ppm (significant).

## Methods

Two transit observations under [[JWST-GO-4098]] (PI: Benneke & Evans-Soma):
- **NIRSpec G395H BOTS** on 2023 October 4 (1763 integrations, 11 groups, 4.9 hr exposure including the early TOI-270 b transit overlap).
- **NIRISS SOSS GR700XD** on 2024 February 6 (189 integrations, 3 groups, 4.0 hr).

Reduction: customized [[Eureka]] (custom 1/f at group level; smooth bias correction; jump threshold 8σ; aperture extractions 4 px NRS1, 3 px NRS2; PASTASOSS for NIRISS trace), with all settings logged on Zenodo. Custom MCMC light-curve fitting using BATMAN + linear-trend systematics + simultaneous fit of TOI-270 b's overlapping transit at the start of NIRSpec.

Retrieval: **[[BeAR]]** (Bern Atmospheric Retrieval, the renamed HELIOS-R2; Kitzmann et al. 2020; not yet ingested) — Bayesian nested sampling via [[MultiNest]] (800 live points). Forward model at native NIRISS+NIRSpec G395H resolution at R = 10⁰⁰⁰⁰ then convolved with the **wavelength-dependent line-spread function** (FWHM ≈ 2 pixels). Opacities computed with [[HELIOS-K]] (Grimm & Heng 2015) using line lists primarily from ExoMol, with HITRAN CIA. Cloud-free isothermal atmosphere as fiducial; non-isothermal and gray/non-gray cloud variants tested but not preferred.

Stellar contamination: NIRISS-SOSS second order excluded due to evidence of strong stellar contamination at < 0.85 μm; first order only retained.

## Caveats & limitations

- **Single transit per instrument.** All molecular detections rest on one G395H + one SOSS transit. The methodology paper makes the case that native-resolution retrieval is robust but more visits would tighten posteriors.
- **CS₂ vs CH₃Cl/CH₃F/H₂CS not distinguishable.** All four molecules produce nearly identical 4.6 μm features at the data's noise level. Distinguishing requires MIRI/LRS or MRS at 8/10/14 μm where opacity profiles diverge.
- **Cannot reproduce Holmberg & Madhusudhan 2024.** Despite using the same data, Felix et al. cannot match either the data reduction or retrieval result of Holmberg & Madhusudhan 2024 (low-MMW hycean). The reasons are not pinpointed; Felix et al. attribute this to (a) Holmberg's more complex T-p profile choice, (b) different stellar/limb-darkening priors, (c) potentially different bias-correction handling. Tension is real and should be flagged.
- **DMS opacity data is sparse.** Sharpe et al. 2004 cross-sections at three temperatures and 1 bar only; uncertain at upper-atmosphere conditions.
- **NS not in line list databases for retrievals; only OCS, SH, CS₂, CS, CH₃Cl, CH₃F, H₂CS, (CH₃)₂S possible.** A fuller sulfur-chemistry network (Moses et al. 2024 in prep) is required to assess plausibility of CS₂ at 10⁻²·¹³.
- **No formal stellar-contamination retrieval.** TOI-270 is M3V; stellar contamination should be modeled; not done in this paper.

## Open questions / follow-ups

- **Why does Felix's reduction reproduce Benneke 2024 but not Holmberg & Madhusudhan 2024?** Independent third party reduction of the same dataset with a fourth retrieval framework would be highly informative.
- **Can MIRI/LRS or MRS distinguish CS₂ from CH₃Cl/CH₃F/H₂CS?** The 8–14 μm region shows opacity divergence (Fig. 10); this is the critical observational follow-up.
- **What atmospheric chemistry produces 1% CS₂ at 360 K on a sub-Neptune?** Moses et al. 2024 photochemistry network (in prep) is the planned framework to test plausibility.
- **Is the TOI-270 d sulfur signature volcanic, photochemical, or something else?** A tidally heated sub-Neptune scenario (analogous to L 98-59 d) is one option; deeper-pressure interior contribution another. Not yet constrained.
- **What about a fourth, fully independent reanalysis of the same data?** With three published analyses giving three different MMW (~2 amu, ~5.5 amu, and now confirming the ~5.5 amu reading), TOI-270 d is now in the same regime as WASP-39 b ([[2026_RoyPerez_WASP39b]]) for pipeline-divergence concerns.

## Related

- [[2025_Roy_LP791-18c]] — temperate sub-Neptune comparator: LP 791-18 c (T_eq ≈ 355 K) shows CH₄ + haze but NO CO₂; TOI-270 d shows CH₄ + CO₂ + tentative CS₂. Sub-Neptune diversity is real at similar T_eq.
- [[K2-18b]] — Hycean candidate (Madhusudhan et al. 2023, not ingested); MMW debate; comparator that motivated TOI-270 d sulfur testing in the first place.
- [[2026_RoyPerez_WASP39b]] — pipeline-systematics study analog for hot Jupiters; Felix 2025 documents the same kind of reduction-divergence concern for sub-Neptunes.
- Benneke et al. 2024 (TOI-270 d, GO 4098, not ingested) — fiducial reading of these data; broadly reproduced.
- Holmberg & Madhusudhan 2024 (TOI-270 d, GO 4098, not ingested) — hycean reading of these data; not reproduced by Felix.
