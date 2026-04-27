---
type: paper
bibkey: 2024_WeinerMansfield_GJ486b
authors: [Weiner Mansfield, M., Xue, Q., Zhang, M., Mahajan, A. S., Ih, J., Koll, D. D. B., Bean, J. L., Coy, B. P., Eastman, J. D., Kempton, E. M.-R., Kite, E. S.]
year: 2024
venue: ApJL
doi: 10.3847/2041-8213/ad8161
targets: [GJ486b]
instruments: [JWST-MIRI]
methods: [secondary-eclipse-spectroscopy]
species_detected: []
species_tentative: []
species_ruled_out: [earth-like-atmospheres, venus-like-atmospheres]
codes: [Eureka, SPARTA]
tags: [rocky-planet, m-dwarf-host, bare-rock, miri-lrs, thermal-emission, cosmic-shoreline, supersession]
ingested: 2026-04-23
---

# No Thick Atmosphere on the Terrestrial Exoplanet Gl 486 b

**Authors:** Weiner Mansfield, Xue, Zhang, Mahajan, Ih, Koll, Bean, et al. (2024, ApJL 975:L22) · [doi:10.3847/2041-8213/ad8161]
**Target:** [[GJ486b]] · **Host:** [[GJ486]] · **Instrument:** [[JWST-MIRI]] (LRS, 5–12 μm)
**Program:** [[JWST-GO-1743]]

## TL;DR
Two JWST MIRI/LRS secondary eclipses of the rocky planet Gl 486 b (= GJ 486 b; 1.289 R⊕, 2.77 M⊕, 1.47-day period, M3.5 host) constrain its dayside temperature to **865±14 K** and the temperature ratio **R = T_day/T_max = 0.97 ± 0.01** — consistent with an **airless body**. [[secondary-eclipse-spectroscopy]] forward models rule out **Earth- or Venus-like atmospheres**; allowed scenarios include airless bodies with slight nonzero albedo or very thin atmospheres with <1% H₂O or <1 ppm CO₂. The result is **incompatible with the water-rich atmosphere interpretation** previously proposed from NIRSpec transmission observations (Moran et al. 2023; not yet ingested), attributing the transmission features instead to stellar contamination. **The most precise JWST thermal-emission constraint on a terrestrial exoplanet to date**, placing a strong constraint on the position of the [[cosmic-shoreline]].

## Key findings
- Broadband eclipse depth 133.3±5.0 ppm ([[SPARTA]]) / 133.7±6.6 ppm ([[Eureka]]); consistent within 1σ.
- Dayside temperature **T_day = 865 ± 14 K**; temperature ratio **R = 0.97 ± 0.01** — within 2–3σ of the zero-albedo zero-redistribution bare-rock limit.
- Observations inconsistent with **Earth- or Venus-like thick atmospheres**; also inconsistent with the water-rich atmosphere inferred from transmission by Moran et al. 2023 (not yet ingested).
- Allowed atmospheres: O₂-rich with ≤100 ppm H₂O or CO₂ at ≤1–10 bar; pure H₂O/CO₂ atmospheres only at surface pressures <0.1 bar; Earth-like only if <0.1 bar.
- Low-albedo rocky surfaces (basalt, oxidized iron, ultramafic, metal-rich) all match within χ²ν ≤ 1.5.
- Precise eccentricity constraint: e = 0.00086 (from mid-eclipse timing).
- Given Gl 486's high XUV activity (Diamond-Lowe et al. 2024; not yet ingested) over ≥6.6 Gyr, thin atmospheres are unlikely to survive → bare-rock is the most parsimonious scenario.
- On the [[cosmic-shoreline]] diagram (escape velocity vs cumulative XUV irradiation), Gl 486 b sits on the **airless-body side**.

## Methods
- **Observations:** two MIRI/LRS secondary eclipses under [[JWST-GO-1743]] (PI M. Mansfield) on 2023-05-29 and 2023-06-01; 4.6 hr each with 14,810 integrations at 6 groups/integration.
- **Reduction:** [[SPARTA]] (Kempton et al. 2023; not yet ingested) primary + [[Eureka]] cross-check; agreement within 1σ.
- **Stellar model:** joint JWST+TESS+HST fit via EXOFASTv2 (Eastman et al. 2019; not yet ingested); SPHINX stellar model, PHOENIX cross-check; stellar radius tightened 3.5× over prior values.
- **Forward modeling:** HELIOS (Malik et al. 2017, 2019; not yet ingested) emission spectra for bare rock (surface compositions from Hu et al. 2012) and thin atmospheres (10⁻⁴–100 bar pure H₂O, pure CO₂, O₂+trace); Planck blackbody reference.
- **Cosmic-shoreline analysis:** dayside-temperature-ratio R → joint constraint on Bond albedo A_B and heat-redistribution factor ε (Cowan & Agol 2011; Koll 2022).

## Caveats & limitations
- Only two eclipse visits; per-visit systematics not thoroughly tested.
- MIRI/LRS shadowed-region (near 10.6 μm) systematics present but bracketed by the two reductions.
- The airless interpretation neglects surface-roughness thermal effects (Spencer 1990; Emery et al. 1998), which could marginally inflate T_day.
- Non-zero-albedo atmospheres with very low H₂O / CO₂ mixing ratios are still allowed — "airless" is most parsimonious but not uniquely required.

## Open questions / follow-ups
- Does Gl 486 b have any residual thin atmosphere (<0.1 bar Earth-like or <1 ppm CO₂)? A transmission re-analysis incorporating the stellar-contamination solution favored by this paper's emission constraint could sharpen the picture.
- How do the Bond-albedo constraints from this paper compare with expectations for different rocky-surface compositions?
- Can shorter-wavelength MIRI/NIRSpec emission help distinguish among the rocky-surface compositions (basalt vs ultramafic vs metal-rich)?

## Tensions
- **vs. Moran et al. 2023 (not yet ingested) transmission interpretation of GJ 486 b:** Moran 2023's NIRSpec/G395H transmission spectrum was consistent with either a water-rich atmosphere or unocculted starspots. This paper's **emission constraint (R = 0.97) is inconsistent with a water-rich atmosphere** — so the Moran 2023 transmission features must be due to stellar contamination, not atmosphere. Recorded as a formal tension on [[GJ486b]]. This is the first case in the wiki where an emission observation retires a tentative transmission-based atmospheric detection.

## Related
- [[2024_Wachiraphan_LTT1445Ab]] — same method (MIRI/LRS emission); same conclusion (consistent with bare rock).
- [[2025_Bennett_GJ1132b]] — NIRSpec transmission + MIRI emission on GJ 1132 b; also concludes bare rock.
- Moran et al. 2023 (not yet ingested) — GJ 486 b NIRSpec transmission referenced for the tension.
- Diamond-Lowe et al. 2024 (not yet ingested) — XUV history of Gl 486 showing sufficient flaring to erode atmospheres over system's ≥6.6 Gyr age.
- Xue et al. 2024 (not yet ingested) — GJ 1132 b MIRI/LRS emission; sibling methodology.
- Zieba et al. 2023; Greene et al. 2023; Ih et al. 2023 (all not yet ingested) — TRAPPIST-1 b/c MIRI emission.
- Kempton et al. 2023 (not yet ingested) — SPARTA pipeline.
