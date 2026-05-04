---
type: paper
bibkey: 2025_Coulombe_TOI-270b
authors: [Coulombe, L.-P., Benneke, B., Krissansen-Totton, J., L'Heureux, A., Piaulet-Ghorayeb, C., Radica, M., Roy, P.-A., Ahrer, E.-M., Cadieux, C., Miguel, Y., Schlichting, H. E., Delgado-Mena, E., Monaghan, C., Adamski, H., Raul, E., Cloutier, R., Komacek, T. D., Taylor, J., Gapp, C., Allart, R., Bouchy, F., Canto Martins, B. L., Cook, N. J., Doyon, R., Evans-Soma, T. M., Larue, P., Suárez Mascareño, A., Wardenier, J. P.]
year: 2025
venue: AJ
arxiv: ""
doi: 10.3847/1538-3881/adfc6a
targets: [TOI-270b, TOI-270d, TOI-270]
instruments: [JWST-NIRSpec, NIRPS]
methods: [transmission-spectroscopy, atmospheric-retrievals, stellar-contamination-modeling, joint-interior-atmosphere-retrieval]
species_tentative: [H2O]
codes: [exoTEDRF, Tiberius, Eureka, SCARLET, smint, nestle, HELIOS-K, PACMAN-P]
tags: [super-earth, terrestrial, water-world, m-dwarf-host, multi-planet-system, atmosphere-tentative, cosmic-shoreline-test, simultaneous-multi-transit]
ingested: 2026-05-04
---

# Possible Evidence for the Presence of Volatiles on the Warm Super-Earth TOI-270 b

**Authors:** Coulombe, Benneke, Krissansen-Totton, L'Heureux, Piaulet-Ghorayeb, Radica, Roy, Ahrer, Cadieux, Miguel et al. (2025, AJ 170:226) · [DOI:10.3847/1538-3881/adfc6a]
**Targets:** [[TOI-270b]] (primary), [[TOI-270d]] (control planet) · **Instruments:** [[JWST-NIRSpec]] (G395H), [[NIRPS]] (host-star abundances)

## TL;DR
A single JWST/NIRSpec G395H visit of the M3V system [[TOI-270]] captures simultaneous transits of the warm super-Earth [[TOI-270b]] (Rₚ = 1.306 R⊕, T_eq,A=0 = 569 K) and the larger sub-Neptune [[TOI-270d]]. The white-light depth tightens the planetary radius by a factor of 1.4–1.6 and yields an updated bulk density ρₚ = 3.7 ± 0.5 g cm⁻³ — **inconsistent with an Earth-like composition at 4.4σ**, requiring a percent-level water mass fraction (best fit ~5.6%, < 10% at 4σ). The transmission spectrum shows a tentative water absorption feature near the bluest NRS1 wavelengths, favoring an H₂O-rich steam atmosphere over a flat spectrum at lnB = 0.3–3.2 (inconclusive to moderate, depending on whether an NRS1/NRS2 detector offset is included). The crucial novelty is **using the simultaneous TOI-270 d transit (3× more sensitive to TLS contamination because it is 1.7× larger) to rule out unocculted starspots/faculae as the source of the b feature** — a methodological first for multi-planet systems. Coupled atmosphere–interior evolution modeling (PACMAN-P) shows that, despite high XUV irradiation placing TOI-270 b on the airless side of the [[cosmic-shoreline]] (next to TRAPPIST-1 b/c, GJ 486 b, GJ 1132 b, LTT 1445 A b), a sufficiently large initial volatile inventory could sustain an H₂O-, O₂-, or H₂-dominated atmosphere over Gyr timescales.

## Key findings

- **Bulk density.** ρₚ = 3.7 ± 0.5 g cm⁻³ from Rₚ = 1.306 ± 0.028 R⊕ (1.4× more precise than Van Eylen et al. 2021; 1.6× more precise than Kaye et al. 2022) and Mₚ = 1.48 ± 0.18 M⊕. This is **2.4σ above pure rock and 4.4σ below Earth-like (33% iron)** — the planet is *underdense for its mass*.
- **Water mass fraction (WMF).** [[smint]] interior-structure modeling with stellar Fe/Mg = 0.81 ± 0.22 (measured by NIRPS) as a Gaussian CMFI prior gives WMF = 5.1 ± 1.1%; with the solar Fe/Mg as prior, 5.1 ± 1.0%. With a log-uniform Fe/Mg prior the WMF is 5.6⁺²·⁵⁻²·² %. WMF < 10% at 4σ regardless of CMFI prior — **rules out pure-rock and matches expectations for a water-world**.
- **Atmosphere — self-consistent forward models ([[SCARLET]]).** Solar-C/O equilibrium-chemistry H₂/He atmospheres at metallicities ≤ 300× solar are ruled out by the small spectrum amplitude (lnB ≥ 26.7 vs. flat). Pure-CH₄ and pure-CO₂ 100-bar atmospheres also worse than flat. **Pure-H₂O is preferred over flat at lnB = 5.2 in the exoTEDRF reduction** (5.5 in Tiberius); robust to surface pressure between 1 and 100 bar.
- **Atmosphere — free-chemistry retrievals.** With H₂ as fill gas: > 50% H₂O at the 2σ–3σ level when surface pressure > 10⁻³ bar. With a fictitious species X (free MMW) as fill gas: > 50% H₂O at 1.5σ; below 90% the global MMW is loosely constrained between ~5 and ~30 amu. **Both H₂-rich (steam-on-top) and H₂O-dominated scenarios are admissible** within 2σ.
- **Stellar contamination ruled out.** Free-TLS retrievals on the simultaneous [[TOI-270d]] transit (which is 1.7× larger and therefore 3× more sensitive to TLS for any given spot/facula configuration) constrain f_spot and ΔT_spot to be near zero. Imposing the d-derived TLS posterior as a prior on b's joint atmosphere+TLS retrieval **leaves the H₂O posterior nearly unchanged from the no-TLS case** — the tentative feature is not stellar.
- **NRS1/NRS2 offset matters.** The Bayes factor for an atmosphere is lnB ≈ 3.2 (moderate) when a δ_NRS1,2 offset is fit, vs. lnB ≈ 0.8 (inconclusive) without. The exoTEDRF reduction prefers a 26 ± 11 ppm offset (2–2.5σ from zero); the Tiberius reduction prefers 20 ± 12 ppm. A control retrieval on the simultaneously fit TOI-270 d spectrum yields δ_NRS1,2 = 2 ± 18 ppm (consistent with zero), arguing the b offset is real (likely missing opacity rather than a detector systematic).
- **Reduction sensitivity.** Three independent reductions (exoTEDRF, Tiberius, Eureka!) agree well across NRS1; Eureka! diverges past 4.5 μm and shows significant inter-channel covariance (skipped for the atmospheric analysis). Tiberius and exoTEDRF give consistent retrieval posteriors.
- **Cosmic shoreline.** TOI-270 b sits firmly on the **airless side** of the Zahnle & Catling 2017 [[cosmic-shoreline]], next to TRAPPIST-1 b/c, GJ 486 b, GJ 1132 b, LTT 1445 A b. PACMAN-P coupled atmosphere–interior simulations (Krissansen-Totton et al. 2024) show this is *not* in fact prohibitive: with a large initial volatile inventory, escape can leave behind H₂O-, O₂-, or H₂-dominated atmospheres on Gyr timescales depending on the C/H/O budget and magma-ocean equilibrium.

## Methods

- **Data reduction.** Three independent JWST/NIRSpec G395H reductions of one transit (2023-10-13): [[exoTEDRF]] (Schmidt et al. 2025 protocol), [[Eureka]], and [[Tiberius]]. White light curves jointly fit (b + d transits with shared LDCs and 4-parameter linear systematics) using `batman` + `emcee`. Spectroscopic R = 200 binning → 53 NRS1 + 60 NRS2 channels (113 total). exoTEDRF chosen for the headline analysis (lower channel-to-channel covariance than Eureka!; tighter errors than Tiberius).
- **Stellar contamination via simultaneous d transit.** Because TOI-270 b and d transit at nearly the same time, both planets sample similar transit chords. Free-TLS retrievals on d (large amplitude → sharp TLS constraint) supply a 2-D KDE prior on (f_spot, ΔT_spot) for the b joint atmosphere+TLS retrieval — implemented with [[nestle]] sampling because emcee (used by Holmberg & Madhusudhan 2024) cannot natively handle such priors.
- **Atmospheric retrievals.** [[SCARLET]] free-chemistry framework with MMW-aware fill-gas treatments: (i) H₂ as fill (steam-on-top); (ii) fictitious species X with free MMW (agnostic). Centered-log-ratio prior on abundances. PHOENIX ACES models with [Fe/H] = −0.2 for spot spectra. [[HELIOS-K]] line-by-line opacities; POKAZATEL H₂O.
- **Stellar abundances.** [[NIRPS]] high-resolution NIR spectrograph (λ = 0.98–1.80 μm; R ~ 70 000) at La Silla under the NIRPS-GTO TOI-270 c/d sub-program: 4 × c-transit + 2 × d-transit visits coadded. χ²-minimization fits to PHOENIX ACES models with the Jahandar et al. 2024–2025 line-list methodology yield [M/H] = −0.13 ± 0.07 and Fe/Mg = 0.81 ± 0.22 — comparable to solar.
- **Interior structure.** [[smint]] (Piaulet-Ghorayeb et al. 2022; Aguichine et al. 2021 grid) with hydrosphere on top of mantle + iron core. CMF re-parameterized in Fe/Mg (avoids the biased uniform-CMF prior). Joint posterior over WMF–CMF–T_irr–Mₚ via emcee.
- **Coupled atmosphere–interior evolution.** PACMAN-P (Krissansen-Totton et al. 2024) Monte Carlo over initial volatile inventories, mantle viscosity, escape (XUV-limited or diffusion-limited), magma-ocean speciation. Three illustrative outcomes shown: H₂-dominated retention (high initial inventory), H₂O-dominated steam (intermediate), O₂-dominated post-H-escape (oxidized inventory).

## Caveats & limitations

- **Significance is moderate at best and offset-dependent.** lnB = 0.3 (no offset) to 3.2 (with offset) for water absorption. The offset is statistically supported but may compensate for unmodeled effects (1/f leftover, residual systematics) rather than being a true detector zero-point.
- **Multiple atmospheric scenarios admissible.** H₂-dominated, H₂O-dominated, and intermediate steam-on-top scenarios all fit within 2σ. The data cannot yet distinguish a 100-bar H₂O-dominated atmosphere from a 1-bar pure-H₂O cap on a magma-ocean surface.
- **Tentative nature of any rocky-planet H₂O claim.** The authors emphasize that convincing evidence for rocky-planet atmospheres should come from **repeatable measurements of atomic or molecular features**. The wiki's twin cautionary tales ([[2025_Bennett_GJ1132b]] retiring [[2023_May_GJ1132b]]; [[2024_WeinerMansfield_GJ486b]] retiring [[2023_Moran_GJ486b]]) apply.
- **TOI-270 d as a single-system control.** The TLS-rule-out method assumes b and d sample similar transit chords (justified by their consistent impact parameters and lack of crossing events) and similar out-of-chord stellar surfaces. Systematic differences between transit chords could bias the TLS marginalization.
- **χ²/N elevated above 1.** Tiberius gives χ²/N = 1.21 (no offset) to 1.13 (with offset); exoTEDRF gives 1.39–1.34. The authors attribute this to underestimated transit-depth uncertainties or residual astrophysical/instrumental signal not captured by the model.

## Open questions / follow-ups

- **MIRI 15 μm thermal emission ([[JWST-GO-3730]] Hot Rocks Survey).** Will tightly constrain heat redistribution and Bond albedo; complementary to transmission.
- **Additional NIRISS/SOSS transmission visits.** Cover 0.6–2.85 μm where multiple H₂O bands and Rayleigh scattering can break the H₂-vs-H₂O degeneracy.
- **More repeats at G395H.** A second visit would directly test the offset's significance and the water-feature reproducibility — the GJ 486 b / GJ 1132 b lesson.
- **Origin of volatiles.** Was TOI-270 b assembled beyond the snow line and migrated inward (consistent with the system's near-resonant configuration), or did the volatiles come from H₂/He–FeO interaction with the magma ocean (Schlichting & Young 2022)?
- **Population context.** TOI-270 b joins a small group of nominally underdense super-Earths (water-world candidates) whose atmospheric retention against M-dwarf XUV is the open question — Luque & Pallé 2022 sample plus subsequent JWST work.

## Tensions

- **TLS offset sensitivity vs Holmberg & Madhusudhan 2024 (not yet ingested).** Their analysis of the same NIRSpec G395H visit found H₂-rich atmosphere preferred at >3σ and a tentative preference for H₂-rich over stellar contamination at 2.7σ. This work obtains weaker preference (lnB up to 3.2 with offset; 0.8 without) and emphasizes the offset and TLS marginalization. See § 5.4 of the paper.
- **No NRS1/NRS2 offset on the simultaneously analyzed TOI-270 d.** δ_NRS1,2 = 2 ± 18 ppm on d (consistent with zero) but 20–26 ppm on b (2–2.5σ from zero). The authors suggest the b offset reflects missing opacity in the model rather than a detector systematic — but this is unresolved.

## Related

- [[2025_Felix_TOI-270d]] — independent reanalysis of the *companion* TOI-270 d transit from the same visit; CH₄ + CO₂ decisive, SO₂ retracted.
- [[JWST-GO-4098]] — parent program (Benneke & Evans-Soma); now associated with two ingested papers.
- [[2025_Madhusudhan_subneptunes]] — review/perspective on small-planet classification; TOI-270 b sits at the super-Earth side of the radius-valley boundary.
- [[2025_Bennett_GJ1132b]], [[2024_WeinerMansfield_GJ486b]] — the rocky-M-dwarf H₂O cautionary tales.
- [[2023_Moran_GJ486b]], [[2023_May_GJ1132b]] — earlier tentative rocky-planet H₂O claims that the authors implicitly compare against.
