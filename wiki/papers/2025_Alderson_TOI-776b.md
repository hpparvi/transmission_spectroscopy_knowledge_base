---
type: paper
bibkey: 2025_Alderson_TOI-776b
authors: [Alderson, L., Moran, S. E., Wallack, N. L., Batalha, N. E., Wogan, N. F., Dattilo, A., Wakeford, H. R., Adams Redai, J., Alam, M. K., Aguichine, A., Batalha, N. M., Gagnebin, A., Gao, P., Kirk, J., López-Morales, M., Meech, A., Teske, J., Wolfgang, A.]
year: 2025
arxiv: 2501.14596
targets: [TOI-776b]
instruments: [JWST-NIRSpec]
methods: [transmission-spectroscopy, multi-visit-stacking]
species_detected: []
species_tentative: []
species_ruled_out: []
codes: [Eureka, ExoTiC-JEDI, PICASO]
tags: [super-earth, m-dwarf-host, rocky-planet, jwst-go-2512, compass, multi-planet-system, detector-offset]
ingested: 2026-04-22
---

# JWST COMPASS: NIRSpec/G395H Transmission Observations of the Super-Earth TOI-776 b

**Authors:** Alderson, Moran, Wallack, N. E. Batalha, Wogan, Dattilo, et al. (2025, arXiv:2501.14596; published DOI pending)
**Target:** [[TOI-776b]] · **Host:** [[TOI-776]] · **Instrument:** [[JWST-NIRSpec]] (G395H, 2.8–5.2 μm)
**Program:** [[JWST-GO-2512-COMPASS]]

## TL;DR
Two JWST NIRSpec/G395H transits of the warm super-Earth TOI-776 b (Rp=1.85 R⊕, Teq~520 K, M-dwarf host), reduced with [[Eureka]] and [[ExoTiC-JEDI]]. Median transit-depth precision 34 ppm per ~0.02 μm channel. Visit 1 prefers a flat line; Visit 2 prefers a flat line with an NRS1/NRS2 detector offset. After correcting for the offset, both reductions and both visits are **consistent with a featureless transmission spectrum**. [[PICASO]] thermochemical-equilibrium forward models rule out metallicities up to **at least 100× solar** at opaque pressure 10⁻³ bar at ≥ 3σ in all cases, with Visit 2 extending the exclusion to ~350× solar. TOI-776 b joins the growing list of super-Earths showing high-MMW or bare-rock-consistent spectra under JWST.

## Key findings
- Two G395H transits (2023-05-24, 2023-06-09); Visit 1 affected by a High Gain Antenna move ~5 hrs into observation.
- [[Eureka]] and [[ExoTiC-JEDI]] reductions agree within the data's precision.
- Visit 1 → flat line preferred; Visit 2 → flat line with NRS1/NRS2 detector offset preferred (a recurring systematic across JWST G395H analyses of small planets).
- After offset correction: both visits statistically consistent with flat; combined analysis rules out atmospheric metallicities < 100–350× solar at P_opaque = 10⁻³ bar at ≥ 3σ.
- Companion paper (Teske & Batalha et al., submitted; not yet ingested) covers the sibling TOI-776 c (water-world candidate, outer planet of the system).

## Methods
- **Observations:** two NIRSpec/G395H transits of TOI-776 b; BOTS mode, SUB2048 subarray, F290LP filter, NRSRAPID readout; 3288 integrations × 7 groups per visit over 6.6 hours.
- **Reduction:** [[ExoTiC-JEDI]] and [[Eureka]] pipelines run in parallel across both visits.
- **Light-curve fitting:** `batman` transit + polynomial systematics model; MCMC via `emcee`.
- **Forward modeling:** [[PICASO]] grid (1–1000× solar metallicity × range of opaque pressure levels) to map ruled-out parameter space.
- **Multi-visit analysis:** separate per-visit fits + combined flat-line assessment; see [[multi-visit-stacking]].

## Caveats & limitations
- HGA move during Visit 1 affects ~6 integrations; masked but introduces additional visit-level variance.
- The NRS1/NRS2 detector offset applied in Visit 2 is a modeling correction; an un-modeled offset would change the preferred flat-vs-slope interpretation.
- As in [[2024_Alderson_TOI-836b]], precision is ~1.3× worse than PandExo predictions.
- 2-visit stack; repeatability not tested as thoroughly as for [[2025_Bennett_GJ1132b]] (4 visits).
- Published DOI not yet assigned as of ingest; arXiv ID recorded instead.

## Open questions / follow-ups
- Is TOI-776 b's spectrum driven by a bare rock, high-MMW atmosphere, or high clouds? Distinguishing requires MIRI follow-up or more NIRSpec visits.
- How common are NRS1/NRS2 offsets across the COMPASS sample? Worth tabulating as a systematic.
- What does the TOI-776 c companion analysis imply for the system-level atmospheric story?

## Tensions
- Reinforces the pattern (with [[2023_May_GJ1132b]], [[2025_Bennett_GJ1132b]]) that NRS1/NRS2 detector offsets are a recurring G395H systematic on small planets — relevant both to the [[stellar-contamination]] vs atmosphere vs detector-systematic degeneracy and to [[JWST-NIRSpec]]-mode choice (G395M vs G395H) going forward.

## Related
- [[2024_Alderson_TOI-836b]], [[2025_Alam_L168-9b]] — companion JWST COMPASS super-Earth results.
- [[2023_Lustig-Yaeger_LHS475b]] — Earth-sized JWST result (CHAMPs).
- [[2023_May_GJ1132b]], [[2025_Bennett_GJ1132b]] — related discussion of NRS1/NRS2 offsets + visit-to-visit systematics.
- Teske & Batalha et al. submitted (not yet ingested) — TOI-776 c, sibling planet in the same system.
- Fridlund et al. 2024 (not yet ingested) — TOI-776 b mass/radius (4.0 M⊕, 1.85 R⊕) adopted here.
- Luque et al. 2021 (not yet ingested) — TOI-776 system discovery.
