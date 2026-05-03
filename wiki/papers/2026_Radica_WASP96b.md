---
type: paper
bibkey: 2026_Radica_WASP96b
authors: [Radica, M., Taylor, J., Rotman, Y., Blecic, J., Welbanks, L., Ahrer, E.-M., Christie, D., Coulombe, L.-P., et al.]
year: 2026
venue: arXiv:2604.05049
arxiv: 2604.05049
targets: [WASP-96b]
instruments: [JWST-NIRSpec, JWST-NIRISS, VLT-FORS2]
methods: [transmission-spectroscopy, atmospheric-retrievals]
species_detected: [H2O, CO2, Na]
species_tentative: [SO2]
codes: [exoTEDRF, NAMELESS, Eureka, juliet, POSEIDON, PyratBay, NEMESISPY, Aurora, ScCHIMERA, FastChem, Photochem, MultiNest]
tags: [hot-saturn, supersolar-metallicity, photochemistry, so2-shoreline, multi-instrument, jwst-go-4082]
ingested: 2026-04-29
---

# Super-Solar Metallicity and Tentative Evidence for Photochemistry on WASP-96 b from JWST and Ground-Based Observations

**Authors:** Radica, Taylor, Rotman, Blecic, Welbanks, Ahrer, Christie, Coulombe, et al. (2026, arXiv:2604.05049)
**Target:** [[WASP-96b]] · **Host:** [[WASP-96]] · **Instruments:** [[JWST-NIRSpec]] (G395H), [[JWST-NIRISS]] (SOSS, archival ERS reanalysis), [[VLT-FORS2]] (archival, 0.36–0.82 μm)
**Program:** [[JWST-GO-4082]]

## TL;DR

Combines a new JWST NIRSpec G395H transit of [[WASP-96b]] (Teq ~1300 K, inflated hot Saturn) with archival JWST NIRISS/SOSS and VLT/FORS2 spectra, yielding clear detections of [[H2O]], [[CO2]], and [[Na]], and **moderate evidence for [[SO2]] (lnB = 2.69)**. Self-consistent grids favor super-stellar metallicity (~2–6× stellar / 4–12× solar) at stellar-like C/O = 0.41. The tentative SO₂ places WASP-96 b on the proposed photochemical "SO₂ shoreline" (Crossfield et al. 2025; not yet ingested) at a higher Teq than [[WASP-39b]], suggesting formation beyond the H₂O snowline followed by accretion of volatile-rich material. Finds a tentative ~2.6σ limb asymmetry in the 1.4 μm H₂O band (symmetric model preferred by Bayesian comparison).

## Key findings

- **H₂O** detected: log VMR ≈ −2.82 to −2.30; consistent with Nikolov et al. 2022.
- **CO₂** detected: log VMR ≈ −4.91 to −4.15.
- **Na** detected (driven by VLT/FORS2 optical data): log VMR ≈ −4.29 to −3.53.
- **SO₂** tentatively detected at lnB = 2.69 (moderate evidence): log VMR ≈ −6.01 to −5.47; abundance well-matched to the Crossfield+2025 SO₂-shoreline grid at 10–20× solar.
- **CO unconstrained** (hidden by CO₂ at 4.3 μm + lower precision >4.5 μm); fundamentally limits free-retrieval metallicity precision.
- Metallicity 2–6× stellar (4–12× solar) from ScCHIMERA self-consistent grid; 5–12× stellar (~10–20× solar) from NemesisPy chemical equilibrium.
- C/O = 0.25–0.44, consistent with the host's stellar value (C/O★ = 0.42).
- **Optical Rayleigh slope** present (contradicts Wang et al. 2026; not yet ingested) — ascribed to small-particle aerosols (clouds or photochemical hazes) or possibly stellar contamination.
- **Tentative limb asymmetry** at the 1.4 μm H₂O band (~2.6σ via spectral amplitude index test); Bayesian comparison still prefers the symmetric model.

## Methods

- **Reductions:** [[exoTEDRF]] (nominal NIRISS+NIRSpec), [[NAMELESS]] (alt NIRISS), [[Eureka]] (alt NIRSpec).
- **Light curves:** exoUPRF, [[juliet]], `batman`, `radvel`, `catwoman` (limb asymmetry), `ExoTiC-LD`, `PandExo`.
- **Retrievals (free chemistry):** [[POSEIDON]], [[PyratBay]], [[NEMESISPY]], [[Aurora]] — multi-code cross-comparison.
- **Equilibrium / self-consistent:** [[NEMESISPY]] CE with [[FastChem]]; [[ScCHIMERA]] self-consistent radiative-convective-thermo/photochemistry grid.
- **Photochemistry:** [[Photochem]] kinetics within the ScCHIMERA framework (alternative to [[VULCAN]]).
- Patchy clouds, modified Rayleigh slope, parametric Madhusudhan & Seager P–T.

## Caveats & limitations

- **exoTEDRF vs NAMELESS NIRISS spectra diverge >1.7 μm** (1/f-correction methodology); Spitzer 3.6 μm point inconsistent with the new NIRSpec.
- **CO unconstrained** — limits metallicity precision via free retrievals.
- **H₂S main feature falls in the NIRSpec G395H detector gap** — motivates G395M/PRISM follow-up for a sulfur inventory.
- **Optical-slope origin degenerate:** photochemical haze vs. condensate cloud vs. broad Na wings vs. stellar contamination.
- **Limb asymmetry only marginally significant**; need a robust pathway for low-S/N quantification.

## Open questions / follow-ups

- Confirm SO₂ via dedicated G395M/PRISM follow-up to access the H₂S band and break sulfur-species degeneracies.
- Resolve optical-slope origin via spectro-photometric monitoring or higher-S/N optical data.
- Settle the tension with Wang et al. 2026 (sub-stellar metallicity, no slope, gray cloud deck).
- Independent confirmation of the limb asymmetry hint.

## Tensions

- **Sub-stellar vs super-stellar metallicity for WASP-96 b.** Wang et al. 2026 (not yet ingested) infers sub-stellar metallicity with a gray cloud deck and no Rayleigh slope; Radica et al. 2026 finds super-stellar metallicity and a Rayleigh slope. Status: unresolved; reduction-pipeline and retrieval-prior choices both contribute.

## Related

- [[2026_RoyPerez_WASP39b]] — methodological cousin; up-to-2-dex pipeline-induced retrieval variation on WASP-39 b ERS PRISM data.
- [[2025_Gressier_WASP17b]] — supersolar dayside H₂O on a different inflated hot giant (DREAMS).
- WASP-39 b ERS papers (not yet ingested) — first JWST SO₂ detection via photochemistry; canonical comparison.
