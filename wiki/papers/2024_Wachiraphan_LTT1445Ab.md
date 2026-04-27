---
type: paper
bibkey: 2024_Wachiraphan_LTT1445Ab
authors: [Wachiraphan, P., Berta-Thompson, Z. K., Diamond-Lowe, H., Winters, J. G., Murray, C., Zhang, M., Xue, Q., Morley, C. V., Rosario-Franco, M., Duvvuri, G. M.]
year: 2024
arxiv: 2410.10987
targets: [LTT1445Ab]
instruments: [JWST-MIRI]
methods: [secondary-eclipse-spectroscopy]
species_detected: []
species_tentative: []
species_ruled_out: [CO2, thick-atmospheres]
codes: [Eureka, SPARTA]
tags: [rocky-planet, m-dwarf-host, triple-star-system, bare-rock, miri-lrs, thermal-emission, cosmic-shoreline]
ingested: 2026-04-23
---

# The Thermal Emission Spectrum of the Nearby Rocky Exoplanet LTT 1445 A b from JWST MIRI/LRS

**Authors:** Wachiraphan, Berta-Thompson, Diamond-Lowe, Winters, Murray, et al. (2024, arXiv:2410.10987; published DOI pending)
**Target:** [[LTT1445Ab]] · **Host:** [[LTT1445A]] · **Instrument:** [[JWST-MIRI]] (LRS, 5–12 μm)
**Program:** [[JWST-GO-2708]]

## TL;DR
Three JWST MIRI/LRS secondary eclipses of the nearby rocky planet LTT 1445 A b (1.34 R⊕, 2.73 M⊕, Teq=431 K; in a triple-star system) constrain its **dayside brightness temperature to 525±15 K** and temperature ratio R = T_day/T_max = **0.952±0.057** — fully consistent with a dark rocky surface. Joint modeling **rules out thick atmospheres** (100-bar CO₂ with Bond albedo >0.08 at 3σ) and pure 1/10/100 bar CO₂ atmospheres at **4.2σ/6.6σ/6.8σ**. A moderately thin atmosphere (Mars-like, Titan-like, Earth-like) remains allowed. The first [[secondary-eclipse-spectroscopy]] result in the wiki.

## Key findings
- Broadband secondary-eclipse depth 41±9 ppm across three visits (2022-08-27, 2022-12-23, 2023-08-05).
- Dayside brightness temperature 525±15 K; temperature ratio R = 0.952±0.057 — consistent with an airless, dark rocky body.
- **Pure 100 bar CO₂ atmospheres rejected at 6.8σ**; 10 bar CO₂ at 6.6σ; 1 bar CO₂ at 4.2σ.
- Low-albedo rocky-surface models (basalt, oxidized iron, ultramafic, metal-rich) all provide good fits (χ²ν ≈ 1.19–1.35).
- Only atmospheres consistent with the data have **low surface pressures (<0.1–10 bar) and small amounts of H₂O or CO₂**.
- Eccentricity constrained to 0.00086 ± 0.00016 (mid-eclipse timing).
- Prior transmission spectroscopy (Diamond-Lowe et al. 2024; not yet ingested) ruled out clear H/He atmospheres but could not distinguish bare rock from high-MMW / cloudy scenarios — this paper closes that gap on the thick-atmosphere side.
- LTT 1445 A b is the **closest known transiting rocky exoplanet** (6.86 pc); instellation similar to Mercury's (~5.77 S_Earth).

## Methods
- **Observations:** three MIRI/LRS secondary eclipses via [[JWST-GO-2708]] (PI Berta-Thompson); 14,810–22,862 integrations per visit at 0.954 s cadence.
- **Reduction:** [[Eureka]] and [[SPARTA]] (Kempton et al. 2023; not yet ingested) in parallel; agreement within ~1σ.
- **Stellar model:** SPHINX (Iyer et al. 2023; not yet ingested) at Teff=3340 K interpolated to LTT 1445 A parameters; BT-Settl cross-check.
- **Light-curve fitting:** eclipse timing, systematics (linear + exponential ramp), dayside flux per wavelength bin.
- **Forward modeling:** HELIOS (Malik et al. 2017, 2019; not yet ingested) emission spectra for bare-rock surfaces (basalt, oxidized iron, ultramafic, metal-rich, etc.) and atmospheres from 10⁻⁴ to 100 bar of pure CO₂ / pure H₂O / Earth-like.
- **Cosmic-shoreline test:** joint constraint on Bond albedo A_B and heat-redistribution factor ε; see [[cosmic-shoreline]].

## Caveats & limitations
- MIRI/LRS calibrations near 10.6 μm (the "shadowed region") are subject to charge-trapping effects; mitigated by ramp fitting and visit trimming but residual systematics possible.
- Stellar spectrum uncertainty dominates the absolute-flux calibration; an alternative BT-Settl model gives slightly different dayside temperature (propagated into final error bar).
- Moderately thin (Mars-Earth-Titan-like) atmospheres are not ruled out — requires shorter-wavelength or phase-curve follow-up.
- Triple-star system means LTT 1445 B+C dilution in photometry is possible; mitigated by position-angle constraints on JWST.

## Open questions / follow-ups
- Is LTT 1445 A b truly airless, or does it host a thin secondary atmosphere (Mars-like)? A transmission follow-up at short wavelengths or a phase-curve observation would help.
- How does LTT 1445 A b's bare-rock picture compare to other rocky-planet emission results ([[2024_WeinerMansfield_GJ486b]] on GJ 486 b; TRAPPIST-1 b/c; LHS 3844 b)?
- Can the inferred surface composition be constrained further? The basalt/ultramafic/metal-rich fits are degenerate in the 5–12 μm range.

## Tensions
- None directly with prior wiki content. Consistent with [[2024_WeinerMansfield_GJ486b]] and the broader picture of close-in M-dwarf rocky planets lacking thick atmospheres.

## Related
- [[2024_WeinerMansfield_GJ486b]] — MIRI/LRS emission of Gl 486 b; similar conclusion of an airless/near-airless body.
- [[2025_Bennett_GJ1132b]] — four-visit NIRSpec on GJ 1132 b concludes bare rock; Wachiraphan extends the picture to emission.
- Diamond-Lowe et al. 2024 (not yet ingested) — prior JWST NIRSpec transmission spectrum of LTT 1445 A b.
- Pass et al. 2023 (not yet ingested) — LTT 1445 A b system parameters.
- Winters et al. 2022 (not yet ingested) — triple-star system characterization.
- Xue et al. 2024 (not yet ingested) — MIRI/LRS emission of GJ 1132 b (same method, contemporaneous analysis).
- Kempton et al. 2023 (not yet ingested) — SPARTA pipeline paper.
