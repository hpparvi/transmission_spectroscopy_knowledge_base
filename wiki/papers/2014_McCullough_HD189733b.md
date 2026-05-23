---
type: paper
bibkey: 2014_McCullough_HD189733b
authors: [McCullough, P. R., Crouzet, N., Deming, D., Madhusudhan, N.]
year: 2014
venue: ApJ
arxiv: 1407.2462
doi: 10.1088/0004-637X/791/1/55
targets: [HD-189733b]
instruments: [HST-WFC3]
methods: [transmission-spectroscopy, atmospheric-retrievals, stellar-contamination-modeling]
species_detected: [H2O]
species_ruled_out: [Na, K]
tags: [hot-jupiter, water-detection, k-dwarf-host, tls-reinterpretation, hst-wfc3-spatial-scan, pre-jwst]
ingested: 2026-05-04
---

# Water Vapor in the Spectrum of the Extrasolar Planet HD 189733b. I. The Transit

**Authors:** McCullough, Crouzet, Deming, Madhusudhan 2014, ApJ 791:55 · [arXiv:1407.2462]
**Targets:** [[HD189733b]] · **Instrument:** [[HST-WFC3]]

## TL;DR
A single HST/WFC3 G141 spatial-scanned transit of HD 189733 b (HST GO-12881, PI McCullough; 5 orbits) recovers two water vapor features: 200 ± 47 ppm at 1.4 μm and 83 ± 53 ppm at 1.15 μm, consistent with a **clear solar-composition atmosphere** with H₂O mixing ratio ~5×10⁻⁴ at T ≈ 700 K (terminator). Two independent reductions (N. Crouzet, D. Deming) agree to within Poisson noise. The headline reinterpretation: the panchromatic blueward slope from [[2008_Pont_HD189733b]] / [[2013_Pont_HD189733b]] — previously attributed to Rayleigh-scattering dust — can be **alternatively explained by unocculted starspot contamination plus a clear atmosphere**. Two-component PHOENIX modeling with T_phot = 5 000 K, T_spot = 3 700 K, spot fraction δ ≈ 5.6 % matches the entire 0.3 μm – 24 μm spectrum (the [[stellar-contamination|TLS]]-only model in their Fig. 5). Critically, low alkali line strengths can also be reproduced by Na/K condensation onto KCl/Na₂S at HD 189733 b's cool (~700–1 200 K) terminator pressures, removing the original need to invoke obscuring haze.

## Key findings
- **Two H₂O features detected.**
  - 1.4 μm: 200 ± 47 ppm — significant at ~8σ when binned over 75 nm including the two adjacent baseline points (commensurate with statistical assessment of features in adjacent figures).
  - 1.15 μm: 83 ± 53 ppm — weaker but consistent with the 1.4 μm peak under solar-composition modeling.
- **H₂O mixing ratio ~5 × 10⁻⁴**, scale height commensurate with T ≈ 700 K (slightly below the ~1 200 K dayside emission temperature but consistent with a cool terminator).
- **Alkali condensation explanation for missing Na/K.** At HD 189733 b's terminator pressures (T ~700–1 200 K, P ~ 1 bar), KCl and Na₂S condensation temperatures (~800 K, ~1 000 K respectively at 1 bar; Morley et al. 2013) can remove Na/K from the observable atmosphere by arbitrarily large factors (Fortney et al. 2005) — providing an alternative to the haze-obscuration hypothesis.
- **TLS-only reinterpretation of the 0.3–1 μm slope.** Two PHOENIX-grid models reproduce the observed monotonic blueward radius rise from the WFC3 1.4 μm point through the visible to the UV:
  - **Combined**: clear solar atmosphere (Madhusudhan & Seager 2009 retrieval; H₂O = 5 × 10⁻⁴, no alkali lines) + unocculted spots at 3 700 K covering δ = 5.6 %. *Their Fig. 5*.
  - **Spots-only (worst case)**: even with δ = 5.6 % at 3 700 K, unocculted spot water absorption contributes only ~40 ppm to the 1.4 μm feature — well below the observed 200 ppm. Thus the WFC3 H₂O detection is **not** an artifact of stellar contamination.
- **Stellar contamination dominant in visible/UV, negligible in near-IR.** A featureless flat WFC3 spectrum is ruled out; thick clouds / hazes fully obscuring the terminator are excluded. A high-pressure (≳ 0.1 bar) cloud deck is *not* excluded.
- **Alternative explanations not eliminated.** Either pure Rayleigh-scattering dust (Pont et al. interpretation) or pure clear-atmosphere + spots fits the data; "some combination" is also viable. The new paper does not claim the dust scenario is incorrect, only that **at least one viable alternative now exists**.

## Methods
Single G141 grism transit, 1.1–1.7 μm, R = 130; spatial scan at 2″ s⁻¹; 5 HST orbits, 4 in-transit, 1 first-orbit discarded as standard. Two independent reductions:
- **N. Crouzet** path: 4-column box-car smoothing; spectrum + transit fits in 28 19-nm bins.
- **D. Deming** path: Gaussian-FWHM-4 smoothing; same bin grid; differential template-subtraction approach (Deming et al. 2013, not ingested).

White-light transit fit using Mandel & Agol 2002 transit model with quadratic limb-darkening (u₁ = 0.1378, u₂ = 0.232) from Sing et al. 2009; Knutson et al. 2012 ephemeris fixed.

Madhusudhan & Seager 2009 retrieval framework for the planet atmosphere; PHOENIX NextGen models for stellar photosphere + spots (5 000 K, 3 000–5 000 K spot grid in 50 K steps, log g = 4.5, [M/H] = 0). Pont et al. 2013 transmission spectrum corrections (AC component) used as starting point; this paper investigates the additional DC (steady spot dimming) component.

## Caveats & limitations
- **Single transit**, modest in-transit duty cycle (3 %); systematics not as fully characterized as Pont et al. multi-instrument multi-visit dataset.
- The TLS reinterpretation of the 0.3–1 μm slope is **demonstrated as viable**, not proven; both clear+spots and dust+clear remain compatible with the joint dataset.
- The 5.6 % spot fraction at 3 700 K is a "limiting case" fit forcing all of the visible-to-UV slope onto unocculted spots. If actual spot fractions and temperatures differ, partial-spot + partial-dust scenarios become possible.
- Stellar polar spots / latitudinal "leopard skin" small-spot patterns (Pont et al. 2013) cannot be ruled out by these data.
- 1.4 μm peak amplitude depends on the smoothing kernel; full-width depends on the binning. The 4σ → ~8σ significance jump from 19-nm to 75-nm averaging illustrates the smoothing dependence.
- Mg H feature at ~5 000 Å expected for cool-spot models is not detected in Pont et al.'s STIS spectrum; this constrains the spot temperature *upward* (≥ 3 700 K) and was a counter-argument to the spots-only scenario in Pont et al. 2013. McCullough et al. address this only briefly.

## Open questions / follow-ups
- Sustained multi-visit, multi-instrument joint retrieval treating clear + spots and Rayleigh-haze as competing, weighted hypotheses; never carried out at the precision demanded.
- Direct UV STIS reanalysis with TLS modeling — does the slope shape better fit Mie-scattering-from-dust or temperature-difference-from-spots once both are accounted for?
- High-resolution alkali spectroscopy: does Na/K precipitation onto sulfides leave detectable narrow-core residuals at the level allowed by Pont et al.'s 2.5σ K detection?

## Related
- [[2008_Pont_HD189733b]] — first haze interpretation; this paper proposes the alternative.
- [[2013_Pont_HD189733b]] — panchromatic Pont et al. spectrum that this paper reinterprets; provides the AC-component spot corrections that McCullough et al. accept as starting point.
- [[2018_Rackham_TLS]] — formalizes the TLS effect for M-dwarfs.
- [[2019_Rackham_TLS-FGK]] — directly addresses HD 189733 b: confirms that K-dwarf unocculted spots can produce the observed blueward slope under reasonable activity assumptions, vindicating McCullough's mechanism.
- [[2025_Verma_HD209458b]] — shows for the *quiet* G-dwarf [[HD209458]] that wavelength-coverage changes alone shift retrieved abundances by 3 dex; analogous (but distinct) coverage-dependence cautionary tale.

## Tensions
- **Slope = haze (Pont 2008/2013) vs. slope = unocculted starspots (this paper).** The same 0.3 μm – 1 μm STIS+ACS spectrum admits two physically distinct explanations of comparable Bayesian merit. The wiki preserves both Pont 2008 and Pont 2013 paper pages frozen at ingest time per the [[stellar-contamination]] / "stale claims" rule; the supersession debate is recorded on the [[HD189733b]] hub page `## Tensions`. **Driver of the difference:** treatment of unocculted starspot contamination (DC component, McCullough's terminology) — Pont et al. apply only the AC component (variability-driven), McCullough et al. add a steady δ ≈ 5.6 % background.
