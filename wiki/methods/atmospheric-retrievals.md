---
type: method
aliases: [atmospheric retrieval, spectral retrieval, Bayesian retrieval]
tags: [bayesian, inverse-problem, core-method, hub]
---

# Atmospheric retrievals

Bayesian inversion of an exoplanet [[transmission-spectrum]] (or emission spectrum) to recover posterior distributions over composition, temperature structure, cloud/haze properties, and — when needed — [[stellar-contamination]] parameters. A forward model maps parameters → spectrum; a sampler (nested sampling or MCMC) explores the posterior; model comparison via Bayes factors quantifies support for specific species or scenarios. The default analysis layer above any [[transmission-spectroscopy]] or [[secondary-eclipse-spectroscopy]] dataset in this wiki — 19+ ingested papers run retrievals as their primary inference step.

## Variants

- **Free chemistry** — independent log-VMR priors per species; minimal physical assumptions. Used when the data are precise enough to constrain individual abundances ([[2026_Radica_WASP96b]], [[2025_LustigYaeger_WASP17b]], [[2025_Gressier_WASP17b]], [[2026_Ashtari_HATS75b]], [[2025_Redai_GJ357b]]).
- **Chemical equilibrium** — composition parameterized by metallicity [M/H] and C/O ratio; reduces dimensionality but inherits forward-model assumptions. Used when free retrievals are degenerate or for cross-comparison ([[2025_Crouzet_HATP12b]], [[2026_Heinke_HATP12b]], [[2025_Teske_TOI776c]], [[2026_Ashtari_HATS75b]]).
- **Self-consistent radiative-convective + photochemistry grids** — replace free T–P and free chemistry with physically-motivated forward models ([[ScCHIMERA]] + [[Photochem]] in [[2026_Radica_WASP96b]]; [[GENESIS]] + [[HyDRo]] in [[2025_Teske_TOI561b]]).
- **Joint stellar-contamination + atmosphere** — fit photospheric heterogeneity parameters simultaneously with atmospheric ones to break the TLSE/atmosphere degeneracy ([[2023_Lim_TRAPPIST1b]], [[2023_Moran_GJ486b]], [[2024_Banerjee_L98-59d]]; see [[stellar-contamination-modeling]]).
- **Joint interior + atmosphere** — single likelihood combining bulk-density priors with atmospheric forward models ([[2025_AcunaAguirre_WASP80b]] is the wiki's first; see [[joint-interior-atmosphere-retrieval]]).
- **GP marginalization over contamination** — fold a Gaussian-process model for wavelength-correlated stellar contamination directly into the retrieval likelihood when stellar models are inadequate ([[2025_Espinoza_TRAPPIST1e]], [[2025_Glidden_TRAPPIST1e]]).
- **CLR-prior compositional retrievals** — centred-log-ratio priors on mixing ratios for unbiased multi-species inference under the simplex constraint ([[2024_Banerjee_L98-59d]] uses [[NEMESISPY]]).

## Codes (active in the wiki)

The retrieval-code ecosystem is balkanized; cross-code consistency is becoming a standard cross-check. Codes that drive retrievals on multiple wiki papers:

- [[POSEIDON]] (7 papers) — transmission + emission, joint stellar+atmosphere; dominant on small-planet G395H.
- [[CHIMERA]] / [[ScCHIMERA]] — free-chemistry + self-consistent variants.
- [[ARCiS]] — ExoMIRI standard; information-content retrievals ([[2026_Heinke_HATP12b]]).
- [[TauREX3]] — ARES legacy + ongoing JWST use ([[2024_Gressier_L98-59d]], [[2025_Gressier_WASP17b]]).
- [[NEMESISPY]] — CLR-prior small-planet retrievals.
- [[Aurora]], [[PyratBay]], [[SCARLET]], [[PICASO]], [[HyDRo]], [[GENESIS]] — appear as primary or cross-check engines on specific papers.

[[MultiNest]] / PyMultiNest is the dominant nested-sampling backend; UltraNest, dynesty, emcee see use as alternatives.

## Trade-offs

- **Free vs equilibrium chemistry on small planets.** Featureless rocky-planet spectra under-constrain free retrievals; equilibrium grids give tighter (but model-dependent) MMW / metallicity bounds. [[2025_Teske_TOI776c]] documents a 2.8–7.7 g mol⁻¹ MMW spread between equilibrium and mixture priors on the same TOI-776 c data.
- **Stellar-contamination handling on M-dwarf hosts.** Atmosphere-only retrievals are biased; joint stellar+atmosphere retrievals can be statistically equivalent to atmosphere-only ([[2023_Moran_GJ486b]], [[2023_May_GJ1132b]]) or strongly preferred ([[2024_Banerjee_L98-59d]]). Independent emission constraints are the cleanest disambiguator (see [[2024_WeinerMansfield_GJ486b]]).
- **Pipeline-induced abundance variation.** [[2026_RoyPerez_WASP39b]] documents up to 2 dex pipeline-induced variation in retrieved abundances on the same NIRSpec PRISM dataset — retrievals inherit and amplify upstream reduction systematics.
- **Limb-averaging bias on hot Jupiters with aerosol asymmetry.** [[2025_Fu_limb-asymmetry]] shows that limb-averaged retrievals on planets with patchy terminator clouds inflate metallicity by up to **+2 dex** and deflate temperature by **~½×** for terminator cloud fraction f = ½ (Eq. 3, after Line & Parmentier 2016). Documented examples: WASP-39 b free retrievals span ~2 dex in H₂O abundance (Lueber 2024 vs Espinoza 2024); WASP-94 Ab and WASP-17 b limb-averaged temperatures fall hundreds of K below T_eq. Recommended workaround: grid retrievals leveraging H₂O–CO₂ ratios are more robust than free retrievals; or use [[Catwoman]]-based limb-resolved retrievals when ingress/egress SNR allows.
- **Cross-code consistency.** [[2026_Radica_WASP96b]] runs four free-chemistry frameworks ([[POSEIDON]], [[PyratBay]], [[NEMESISPY]], [[Aurora]]) on the same WASP-96 b spectrum; broad agreement on H₂O / CO₂ / Na, tentative SO₂ replicated. Increasingly the standard for high-significance claims.

## Open issues

- **Information attribution by instrument / wavelength.** [[2026_Heinke_HATP12b]] introduces an information-content framework (Δln Z per instrument combination) on HAT-P-12 b — generalizable to other panchromatic targets. See [[information-content-analysis]].
- **Bulk vs atmospheric metallicity.** Joint interior + atmosphere retrievals on hot Jupiters can disagree on metallicity by an order of magnitude depending on chemistry mode and prior choices ([[2025_AcunaAguirre_WASP80b]]; [[2026_Ashtari_HATS75b]] tension on TLS-framework metallicity).
- **TLSE+atmosphere degeneracy on cool ultracool-dwarf hosts.** Where stellar models fail (<3 μm on TRAPPIST-1) only GP marginalization or empirical [[back-to-back-transit-correction]] currently enable atmospheric inference.

## Papers

### Hot Jupiter / sub-Saturn / Neptune / GEMS — multi-framework
- [[2025_Gressier_HATP26b]] — TauREx + POSEIDON (4 configurations) + PICASO grid + Photochem on HAT-P-26 b NIRSpec G395H; SO₂ at lnB = 13.46 reproduced across frameworks; population-level SO₂–[M/H] reanalysis of 11 JWST giants.
- [[2025_Ahrer_KELT7b]] — POSEIDON + petitRADTRANS (free + equilibrium) + NemesisPy on KELT-7 b NIRSpec G395H ± HST joint; equilibrium chemistry preferred at Δ ln Z = 1.6–3.1 over free chemistry; high-T species set ruled out on physical grounds despite formal Bayes-factor preference.
- [[2026_Radica_WASP96b]] — four free-chemistry retrievals + ScCHIMERA + Photochem on WASP-96 b.
- [[2026_Heinke_HATP12b]] — ARCiS retrievals across all instrument combinations on HAT-P-12 b.
- [[2026_Ashtari_HATS75b]] — POSEIDON free + equilibrium under TLS framework on HATS-75 b.
- [[2025_LustigYaeger_WASP17b]] — POSEIDON v1.2 dayside + nightside on WASP-17 b iESR-PIE.
- [[2025_Gressier_WASP17b]] — TauREx 3.1 + POSEIDON on WASP-17 b NIRISS dayside.
- [[2025_Crouzet_HATP12b]] — equilibrium retrievals; foundational HAT-P-12 b paper.
- [[2026_RoyPerez_WASP39b]] — PSG + MultiNest on six independent WASP-39 b reductions.
- [[2025_AcunaAguirre_WASP80b]] — joint interior + atmosphere (GASTLI + petitRADTRANS).

### Sub-Neptune
- [[2025_Roy_LP791-18c]] — SCARLET + Photochem on LP 791-18 c PRISM.
- [[2025_Felix_TOI-270d]] — [[BeAR]] (Bern Atmospheric Retrieval) at native instrument resolution + LSF convolution on TOI-270 d NIRSpec G395H + NIRISS SOSS; documents that **binning to ≤16 px biases Bayes factors by orders of magnitude** — first wiki paper to make this methodology argument explicit. CS₂, CH₃Cl, CH₃F, H₂CS degenerate at JWST resolution.
- [[2025_FernandezRodriguez_K2-18b]] — [[TauREX3]] retrievals across 12 K2-18 b spectrum variants × 4–6 chemical model setups; documents that **simplified retrievals (1–2 species) inflate detection significance** vs comprehensive (full 13-species) retrievals; DMS detection retracted under comprehensive setup despite simplified-setup preference. Argues for binning before retrieval (R~100) plus comprehensive chemistry as the methodologically robust regime.
- [[2025_Jaziri_K2-18b]] — [[TauREX3]] + TauREx-PyMieScatt aerosol module with **complex refractive indices** for 7 tholin analogs on K2-18 b NIRISS+NIRSpec+MIRI joint spectrum; documents that **including absorbing aerosols (not just gray cloud decks) fundamentally changes inferred composition** — CH₄ abundance drops 2 dex, metallicity 20× → 0.3× solar with the same data. First wiki paper to use complex-refractive-index aerosol modeling for JWST sub-Neptune retrievals.

### Rocky M-dwarf planets — joint stellar+atmosphere or featureless retrievals
- [[2025_Fisher_TOI1685b]] — BeAR nested sampling; MMW ≳ 10 at ~5σ.
- [[2025_PiauletGhorayeb_TRAPPIST1d]] — SCARLET on TRAPPIST-1 d PRISM.
- [[2025_Glidden_TRAPPIST1e]] — petitRADTRANS forward grid + GP contamination.
- [[2025_Espinoza_TRAPPIST1e]] — GP-marginalized atmospheric inference.
- [[2025_Teske_TOI776c]] — PICASO physical retrievals.
- [[2025_Redai_GJ357b]] — free + equilibrium on GJ 357 b NIRSpec G395H.
- [[2025_Taylor_GJ357b]] — TLS-mode and atmospheric retrievals on GJ 357 b NIRISS.
- [[2024_Gressier_L98-59d]] — TauREx3 + exoretrievals on L 98-59 d.
- [[2024_Banerjee_L98-59d]] — NEMESISPY CLR-prior retrievals on the same L 98-59 d transit.
- [[2024_Scarsdale_L98-59c]] — featureless-spectrum H₂/CO₂ exclusion.
- [[2024_Alderson_TOI-836b]] — featureless rules out H₂-dominated < 250× solar.
- [[2025_Alderson_TOI-776b]] — featureless rules out < 100× solar.
- [[2025_Alam_L168-9b]] — featureless 3–12 μm rules out < 100× solar.
- [[2023_May_GJ1132b]] — POSEIDON atmosphere vs starspots; equal evidence.
- [[2023_Moran_GJ486b]] — POSEIDON 6-gas + rfast + starspot retrievals.
- [[2023_Lustig-Yaeger_LHS475b]] — 5-component on the featureless spectrum.
- [[2023_Lim_TRAPPIST1b]] — SCARLET + POSEIDON joint stellar+atmosphere.
- [[2021_Mugnai_GJ1132b]] — TauREX3 + MultiNest on five HST WFC3 transits.

### Emission
- [[2025_Teske_TOI561b]] — HyDRo + GENESIS emission retrievals on TOI-561 b dayside.
- [[2025_Sikora_HD80606b]] — petitRADTRANS chemical-equilibrium + PyratBay free-chemistry retrievals on HD 80606 b NIRSpec G395H emission spectra at 10 orbital phases through periapse passage; first phase-resolved retrieval study on an eccentric hot Jupiter.

### Frameworks introduced
- [[2025_Verma_HD209458b]] — **SANSAR** retrieval framework demonstrated on HD 209458 b panchromatic HST/STIS + WFC3 + JWST/NIRCam observations; supports free, equilibrium-chemistry (via PYFASTCHEM), and self-consistent grid retrievals; opacity-sampling and correlated-k methods both validated against POSEIDON, ATMO, CHIMERA, Aurora; demonstrates that NIRCam-only retrievals overestimate H₂O and CO₂ abundances by ~3 orders of magnitude relative to STIS+WFC3+NIRCam.
- [[2025_Deka_WASP39b]] — **NEXOTRANS** retrieval framework demonstrated on WASP-39 b panchromatic JWST NIRISS+PRISM+MIRI data; integrates Bayesian inference (PyMultiNest, UltraNest) with four ML algorithms (Random Forest, Gradient Boosting, kNN, Stacking Regressor); introduces **modified hybrid equilibrium** and **modified equilibrium-offset** chemistry frameworks (Constantinou & Madhusudhan 2024-style); equilibrium-chemistry module **NEXOCHEM** benchmarked against [[FastChem]]. Best-fit hybrid model gives O/H = 14× solar, C/H = 21× solar, S/H = 5× solar, C/O = 1.35× solar.
