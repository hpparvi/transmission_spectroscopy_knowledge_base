---
type: species
aliases: [water, water vapor]
tags: [volatile, dominant-absorber, near-infrared, hub]
---

# H₂O

Water vapor — the dominant near-infrared opacity source in warm-to-hot planetary atmospheres, with broad absorption bands across 1–5 μm and a strong contribution to mid-infrared emission. The most commonly detected molecule in exoplanet transmission spectra and historically the first to be predicted theoretically ([[2001_Brown_TransmissionDiagnostics]]) and the first to drive a high-significance JWST hot-Jupiter detection (WASP-39 b ERS data, original ERS papers not yet ingested; later confirmed across all four pipelines in [[2026_RoyPerez_WASP39b]]). H₂O appears in 15+ wiki papers spanning every host-star spectral type from F to ultracool M.

## Detection status

- **Confirmed detection (hot Jupiter / sub-Saturn):**
  - [[WASP-39b]] — confirmed across all four reduction pipelines of the ERS PRISM dataset ([[2026_RoyPerez_WASP39b]]).
  - [[WASP-17b]] — 6.4σ on the dayside, supersolar (3σ lower limit > 3× solar; peak likelihood ~100× solar) across all 8 retrievals ([[2025_Gressier_WASP17b]]); tentative 1.5σ on the nightside via iESR-PIE ([[2025_LustigYaeger_WASP17b]]).
  - [[WASP-96b]] — clearly detected in transmission across all four free-chemistry retrievals; log VMR ≈ −2.82 to −2.30; supersolar ([[2026_Radica_WASP96b]]).
  - [[HAT-P-12b]] — 6.0σ on NIRSpec G395M ([[2025_Crouzet_HATP12b]]); >12σ in panchromatic NIRISS+NIRSpec+MIRI+HST joint retrieval ([[2026_Heinke_HATP12b]]); 11–15× solar metallicity; NIRISS-driven.
  - [[WASP-80b]] — present in joint interior–atmosphere retrieval (per cited input retrievals; [[2025_AcunaAguirre_WASP80b]]).
- **Tentative — current (warm super-Earth, M-dwarf):**
  - [[TOI-270b]] — tentative water absorption near the bluest NRS1 wavelengths; H₂O-rich steam atmosphere preferred over flat at lnB = 0.3 (no NRS1/NRS2 offset) to 3.2 (with offset) — inconclusive to moderate; stellar contamination ruled out via simultaneous [[TOI-270d]] transit as TLS control ([[2025_Coulombe_TOI-270b]]).
- **Tentative, then retired (rocky M-dwarf planets):**
  - [[GJ1132b]] — tentatively dominant in Visit 1 (log X(H₂O) ≈ −0.01) but degenerate with unocculted starspots ([[2023_May_GJ1132b]]); thin-steam atmospheres remain marginally consistent with the four-visit coadd but the fit is driven entirely by Visit 1, retiring the H₂O inference ([[2025_Bennett_GJ1132b]]).
  - [[GJ486b]] — [[POSEIDON]] retrievals favored H₂O at >10% (2σ) with Bayes factors 133/8 (3.6σ/2.6σ) in [[Eureka]]/[[FIREFLy]] reductions but were equally well explained by ~10% unocculted starspots ([[2023_Moran_GJ486b]]); MIRI/LRS emission later rules out water-rich atmospheres, retiring the transmission interpretation ([[2024_WeinerMansfield_GJ486b]]).
- **Ruled out / upper-limited (rocky M-dwarf planets):**
  - [[LHS475b]] — 3σ upper limit of 61 ppm on any 2.8 μm absorption feature; pure-H₂O still consistent at high MMW ([[2023_Lustig-Yaeger_LHS475b]]).
  - [[L168-9b]] — pure-H₂O atmospheres ruled out at < 100× solar metallicity by the featureless 3–12 μm spectrum ([[2025_Alam_L168-9b]]).
  - [[TOI-1685b]] — pure-H₂O atmospheres ruled out by the flat coadded G395H spectrum; MMW ≳ 10 at ~5σ ([[2025_Fisher_TOI1685b]]).
  - [[TOI-776c]] — featureless G395H rules out metallicity < 180–240× solar; H₂O-mediated low-MMW models excluded ([[2025_Teske_TOI776c]]).
- **Upper limit / contamination-masked (M-dwarf gas giant):**
  - [[HATS-75b]] — only an upper limit on NIRSpec PRISM; likely masked by M-dwarf host stellar contamination ([[2026_Ashtari_HATS75b]]).

## History

- **Theoretical foundation.** [[2001_Brown_TransmissionDiagnostics]] predicts H₂O bands across 0.7–2.5 μm at 0.08–0.17% below continuum on HD 209458 b — one of the canonical molecular diagnostics. [[2000_Seager_TheoryTransmission]] frames the theoretical expectation but emphasizes Na D as the strongest single feature.
- **Pre-JWST HST/WFC3 era.** Foundational HST WFC3 G141 detections on hot Jupiters and sub-Neptunes (not yet ingested) made H₂O the workhorse molecule for the 1.4 μm spectral feature.
- **JWST Cycle 1 — small-planet phase.** First JWST claims appear on rocky M-dwarf planets ([[2023_Moran_GJ486b]], [[2023_May_GJ1132b]]) but are degenerate with [[stellar-contamination]]; null results elsewhere ([[2023_Lustig-Yaeger_LHS475b]]).
- **Eclipse-side resolution (2024).** [[2024_WeinerMansfield_GJ486b]] uses MIRI/LRS emission to rule out water-rich atmospheres on Gl 486 b — the canonical case for emission as arbiter of transmission ambiguity.
- **Multi-visit retraction (2025).** [[2025_Bennett_GJ1132b]] retires the GJ 1132 b H₂O inference via four-visit coadding + leave-one-out; the second cautionary tale for single-visit small-planet H₂O claims.
- **Hot-Jupiter benchmarks (2025–2026).** [[2025_Gressier_WASP17b]], [[2026_Radica_WASP96b]], [[2025_Crouzet_HATP12b]], [[2026_Heinke_HATP12b]] establish high-significance H₂O on warm-to-hot gas giants, with metallicities consistently supersolar.

## Open issues

- **Single-visit H₂O claims on rocky M-dwarf planets are unreliable.** [[GJ486b]] (resolved by emission) and [[GJ1132b]] (resolved by multi-visit stacking) are now twin cautionary tales. [[multi-visit-stacking]] and [[secondary-eclipse-spectroscopy]] are de facto requirements for any new claim.
- **Stellar-contamination–H₂O degeneracy.** Cool unocculted starspots imprint near-IR features that mimic H₂O bands; resolution depends on either independent emission constraints, joint stellar+atmosphere retrievals, or empirical [[back-to-back-transit-correction]] on systems with airless reference planets.
- **Metallicity inferences on hot Jupiters.** Independent JWST datasets converge on supersolar H₂O abundances ([[WASP-17b]], [[WASP-96b]], [[HAT-P-12b]]) but specific metallicity values vary with retrieval framework and data combination; cross-target population-level synthesis still pending in this wiki.

## Papers

### Hot Jupiter / sub-Saturn / Neptune — confirmed detections
- [[2025_Gressier_HATP26b]] — moderate detection (lnB = 4.06, ~3σ) on Neptune-mass HAT-P-26 b NIRSpec G395H; log X(H₂O) ≈ −2.07; significance limited by stellar-contamination degeneracy at NRS1 short-wavelength end and by NRS1/NRS2 detector offset; full SOSS-driven constraint forthcoming (R. J. MacDonald & DREAMS 2025, in prep).
- [[2025_Ahrer_KELT7b]] — **tentative only** (Δ ln Z = 1.0–1.9, ~2–2.5σ by Sellke mapping) on aligned hot Jupiter KELT-7 b NIRSpec G395H; weak feature compatible with high-altitude cloud deck or low-metallicity atmosphere; first BOWIE-ALIGN target with H₂O sub-detection.
- [[2025_Sikora_HD80606b]] — detected at 4.2–5.5σ on highly eccentric hot Jupiter HD 80606 b NIRSpec G395H **emission** spectrum post-periapse; absorption in NRS2 (3.7–4.4 μm).

### Sub-Neptune
- [[2025_Felix_TOI-270d]] — **surprisingly low** log X(H₂O) ≈ −4.1 (Bayes factor 1; effectively non-detection in the upper atmosphere) on temperate sub-Neptune TOI-270 d at T ≈ 360 K; condensation below the probed pressures hypothesized; H₂O abundance increases by ~10× when methyl chloride / methyl fluoride are added to the retrieval — degeneracy diagnostic.
- [[2026_Heinke_HATP12b]] — >12σ panchromatic; NIRISS-driven; 11–15× solar.
- [[2026_Radica_WASP96b]] — supersolar across four free-chemistry retrievals.
- [[2025_Crouzet_HATP12b]] — 6.0σ NIRSpec G395M (foundational HAT-P-12 b paper).
- [[2025_LustigYaeger_WASP17b]] — tentative 1.5σ nightside via iESR-PIE.
- [[2025_Gressier_WASP17b]] — 6.4σ dayside; supersolar.
- [[2026_RoyPerez_WASP39b]] — confirmed across four pipelines.
- [[2025_AcunaAguirre_WASP80b]] — present in joint interior–atmosphere retrieval.

### Rocky / warm super-Earth — current tentative
- [[2025_Coulombe_TOI-270b]] — H₂O steam atmosphere preferred over flat at lnB = 0.3–3.2 on warm super-Earth [[TOI-270b]] (Tₑq = 569 K); offset-dependent, TLS contamination ruled out via simultaneous TOI-270 d transit; underdense bulk (4.4σ vs. Earth-like) requires nonzero water mass fraction (~5–6%).

### Rocky M-dwarf planets — degenerate / retired claims
- [[2025_Bennett_GJ1132b]] — four-visit retraction of the [[2023_May_GJ1132b]] inference.
- [[2024_WeinerMansfield_GJ486b]] — MIRI emission retires the [[2023_Moran_GJ486b]] water-rich interpretation.
- [[2023_Moran_GJ486b]] — H₂O at >10% (2σ) but degenerate with starspots.
- [[2023_May_GJ1132b]] — Visit-1 H₂O-dominated; not reproduced in Visit 2.

### Rocky M-dwarf planets — null / upper limits
- [[2025_Fisher_TOI1685b]] — pure-H₂O ruled out; MMW ≳ 10 at ~5σ.
- [[2025_Teske_TOI776c]] — featureless rules out < 180–240× solar.
- [[2025_Alam_L168-9b]] — pure-H₂O ruled out at < 100× solar.
- [[2023_Lustig-Yaeger_LHS475b]] — 61 ppm 3σ feature upper limit at 2.8 μm.

### M-dwarf gas giant
- [[2026_Ashtari_HATS75b]] — upper limit only; likely contamination-masked.

### Limb-resolved
- [[2025_Murphy_WASP107b]] — H₂O **uniform between limbs** on WASP-107 b panchromatic limb-resolved spectrum (log VMR ≈ −2.4 morning, −2.5 evening); χ² grid sweep 1σ-overlapping. Consistent with theoretical predictions that H₂O is rapidly homogenized by atmospheric circulation, in contrast to the SO₂ and CO₂ heterogeneities measured on the same data.

### Methodology / wavelength-coverage tests
- [[2025_Verma_HD209458b]] — HD 209458 b H₂O detected at 12.6σ in STIS+WFC3+NIRCam free-chemistry SANSAR retrieval (log VMR = −4.53); but NIRCam-only retrieval gives log VMR ≈ −1.62 (a 3-dex overestimate). Demonstrates that retrievals on broadband NIR-only data systematically inflate H₂O abundances without optical baseline.
- [[2025_Barat_V1298Tau-b]] — H₂O detected at 30σ on the young (10–30 Myr) sub-Neptune progenitor V1298 Tau b NIRSpec G395H + HST WFC3 panchromatic transmission; the atmospheric scale height (~1500 km) is dominated by the strong 2.7 μm H₂O feature; supports an H/He-dominated low-metallicity atmosphere.

### Pre-JWST hot-Jupiter detections (HD 189733 b)
- [[2014_McCullough_HD189733b]] — two HST/WFC3 G141 features: 200 ± 47 ppm at 1.4 μm + 83 ± 53 ppm at 1.15 μm on HD 189733 b; H₂O mixing ratio ~5×10⁻⁴ at T ≈ 700 K (terminator); ~8σ at 75 nm binning. Robust to a worst-case unocculted-spot scenario (T_spot ≈ 4 250 K contamination contributes only ~40 ppm to the 1.4 μm feature). The detection is **not** an artifact of stellar contamination, even under the McCullough TLS-only reinterpretation of the panchromatic UV-to-visible slope.
- [[2013_Pont_HD189733b]] — broad H₂O bands **muted to ≤ 1 scale height** in the panchromatic 0.3–24 μm transmission; consistent with either a high-altitude haze obscuring the deeper atmosphere (Pont's preferred reading) or a clear atmosphere with H₂O at terminator temperatures cool enough to suppress feature amplitude.

### Theory
- [[2001_Brown_TransmissionDiagnostics]] — predicts 0.7–2.5 μm H₂O bands at 0.08–0.17% below continuum on HD 209458 b.
