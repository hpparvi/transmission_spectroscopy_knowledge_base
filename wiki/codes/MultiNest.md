---
type: code
aliases: [MultiNest sampler, PyMultiNest]
tags: [nested-sampling, bayesian, retrieval]
---

# MultiNest

A multimodal nested-sampling algorithm and code (Feroz & Hobson 2008; Feroz, Hobson & Bridges 2009; Buchner et al. 2014), widely used as the sampler backend for Bayesian atmospheric retrievals. Produces posterior distributions and Bayesian evidences for model comparison. Used as the sampler in the [[PSG]]-based retrieval of [[2026_RoyPerez_WASP39b]].

## Papers

- [[2025_Gressier_HATP26b]] — sampler (1500 live points, evidence tolerance 0.5) for TauREx + POSEIDON free-chemistry retrievals on HAT-P-26 b NIRSpec G395H spectrum.
- [[2025_Ahrer_KELT7b]] — sampler (PyMultiNest 1000 live points for POSEIDON, 500 for petitRADTRANS, NemesisPy via PyMultiNest) on KELT-7 b NIRSpec G395H + HST joint retrievals.
- [[2025_Felix_TOI-270d]] — sampler (800 live points) for BeAR retrievals on TOI-270 d NIRSpec G395H + NIRISS SOSS native-resolution data.
- [[2025_FernandezRodriguez_K2-18b]] — PyMultiNest sampler (3000 live points) for TauREx3 retrievals across 12 K2-18 b spectrum variants × 4–6 chemical model setups.
- [[2025_Jaziri_K2-18b]] — PyMultiNest sampler (800 live points) for TauREx 3.1 retrievals on K2-18 b NIRISS+NIRSpec+MIRI joint spectrum across 11+ chemical-model and aerosol-model permutations.
- [[2025_Sikora_HD80606b]] — emcee (24-48 walkers, ~10⁵ samples) used as the petitRADTRANS sampler; MC3 snooker differential-evolution MCMC (4×10⁶ samples) for PyratBay retrievals on HD 80606 b emission phases.
- [[2026_RoyPerez_WASP39b]] — sampler for PSG atmospheric retrieval of WASP-39 b across six independent reductions.
- [[2025_LustigYaeger_WASP17b]] — sampler for POSEIDON v1.2 free-chemistry retrieval on WASP-17 b dayside + nightside iESR-PIE spectra.
- [[2025_Gressier_WASP17b]] — sampler for TauREx 3.1 retrievals on WASP-17 b NIRISS/SOSS dayside emission spectrum.
- [[2026_Radica_WASP96b]] — sampler for POSEIDON / NEMESISPY / Aurora / PyratBay / ScCHIMERA retrievals on WASP-96 b.
- [[2026_Heinke_HATP12b]] — sampler for ARCiS retrievals across all instrument combinations in the HAT-P-12 b information-content analysis.
- [[2026_Holmberg_GJ3473b]] — sampler for batman + celerite light-curve fits to four GJ 3473 b MIRI F1500W eclipses.
- [[2026_Ashtari_HATS75b]] — sampler for POSEIDON retrievals on HATS-75 b NIRSpec PRISM transits.
- [[2025_Crouzet_HATP12b]] — sampler (2500 live points) for ARCiS retrievals on HAT-P-12 b NIRSpec G395M data.
- [[2025_AcunaAguirre_WASP80b]] — sampler (PyMultiNest) for the joint interior–atmosphere retrieval on WASP-80 b.
- [[2025_Verma_HD209458b]] — sampler (PyMultiNest, 2000 live points, tolerance 0.5) for SANSAR retrievals on HD 209458 b across three instrument combinations.
- [[2025_Deka_WASP39b]] — sampler (PyMultiNest with 100 live points) for [[NEXOTRANS]] Bayesian retrievals; benchmarked alongside UltraNest and four ML algorithms.
- [[2025_Barat_V1298Tau-b]] — sampler for [[PICASO]] free-chemistry retrievals on V1298 Tau b; mass measurement from atmospheric scale height (~10% precision, 12 ± 1 M⊕).
- [[2025_Luque_K2-18b]] — PyMultiNest sampler (1000 live points, Importance Nested Sampling) for [[PLATON]] retrievals on K2-18 b panchromatic spectrum.
- [[2025_Madhusudhan_K2-18b-MIRI]] — MultiNest sampler (2000 live points) for AURA/Aurora retrievals on K2-18 b MIRI/LRS spectrum; cross-checked with UltraNest.
- [[2025_PicaCiamarra_K2-18b]] — sampler for [[POSEIDON]] + [[petitRADTRANS]] + VIRA retrievals in the 650-molecule agnostic K2-18 b search.
- [[2025_BelloArufe_L98-59b]] — PyMultiNest sampler (800 live points; 2000 for POSEIDON) for [[ExoTR]] + [[Aurora]] + [[POSEIDON]] retrievals on L 98-59 b NIRSpec G395H spectrum.
- [[2025_Canas_TOI5205b]] — PyMultiNest sampler (400 live points; Δ ln Z = 5 convergence) for [[POSEIDON]] retrievals on TOI-5205 b NIRSpec PRISM with spots + faculae.
- [[2025_Liu_HATP14b]] — PyMultiNest sampler (2000 live points) for [[petitRADTRANS]] free-chemistry + equilibrium-chemistry retrievals on HAT-P-14 b combined NIRISS + NIRSpec G395H.
- [[2025_Mukherjee_GJ436b]] — PyMultiNest sampler (2000 live points) for [[PICASO]] 17-parameter free-chemistry retrieval on GJ 436 b panchromatic emission spectrum.
- [[2025_Taylor_K2-18b-MIRI]] — MultiNest sampler for Gaussian-feature Bayesian-evidence calculations on K2-18 b MIRI/LRS spectrum (6 model variants).
- [[2025_RoyPerez_WASP39b]] — MultiNest sampler (via custom in-house wrapper around [[PSG]]/PUMAS) for cloud-extinction-parameterization analysis on WASP-39 b NIRSpec PRISM; 4 cloud-extinction models × ~14 free parameters each; Bayes factors decisively favor Ångström (ln B = 8.02) and MOPSMAP (ln B = 5.57) over flat clouds.
- [[2025_Schmidt_K2-18b]] — PyMultiNest sampler (1000 live points; ~50 CPU-years total) for >240 [[POSEIDON]] retrievals on K2-18 b across 60 NIRISS+NIRSpec data combinations.
- [[2025_Ohno_GJ1214b]] — PyMultiNest grid retrieval over 2184 PM-haze profiles for GJ 1214 b panchromatic transmission spectrum.
