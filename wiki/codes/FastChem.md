---
type: code
aliases: [FastChem equilibrium chemistry]
tags: [chemical-equilibrium, atmospheric-modeling]
---

# FastChem

An open-source chemical equilibrium code for gas-phase planetary atmospheres (Stock et al. 2018, 2022). Rapidly computes number densities for hundreds of species across temperature–pressure grids under the assumption of chemical equilibrium. Used in [[2026_Coy_HD3167b]] alongside [[GENESIS]] to model emission spectra for a range of volatile atmospheric compositions for HD 3167 b.

## Papers

- [[2026_Coy_HD3167b]] — chemical equilibrium abundances for HD 3167 b atmospheric forward models.
- [[2026_Radica_WASP96b]] — chemical equilibrium abundances within the [[NEMESISPY]] CE retrieval framework on WASP-96 b.
- [[2025_Verma_HD209458b]] — coupled to [[SANSAR]] via PyFastChem for equilibrium-chemistry retrievals on HD 209458 b; varying C/H or O/H independently to control C/O.
- [[2025_Deka_WASP39b]] — used to benchmark [[NEXOTRANS|NEXOCHEM]] (NEXOTRANS's in-house equilibrium-chemistry module); agreement well within typical observational uncertainties.
