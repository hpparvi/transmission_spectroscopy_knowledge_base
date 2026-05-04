---
type: code
aliases: [pRT, petitRADTRANS retrieval code]
tags: [radiative-transfer, retrieval-code, forward-model, transmission, emission]
---

# petitRADTRANS

An open-source radiative-transfer and atmospheric retrieval code for exoplanet atmospheres (Mollière et al. 2019; not yet ingested). Computes transmission and emission spectra for user-defined pressure–temperature profiles and chemical compositions using line-by-line or correlated-k opacity tables. Commonly used for forward-model grids and free-chemistry retrievals across the near- and mid-infrared. A widely adopted alternative to [[PICASO]] and [[POSEIDON]] for atmospheric forward modeling in the JWST era.

## Papers
- [[2025_Ahrer_KELT7b]] — pRT v3.1 free-chemistry + equilibrium-chemistry retrievals on KELT-7 b NIRSpec G395H; cross-check against POSEIDON; equilibrium-chemistry result preferred at Δ ln Z = 1.6–3.1 over free chemistry.
- [[2025_Crossfield_SO2shoreline]] — synthetic transmission spectra at R = 30,000 for the 936-model SO₂ shoreline grid; 21 species opacities; couples downstream of HELIOS T-p + VULCAN photochemistry.
- [[2025_Sikora_HD80606b]] — chemical-equilibrium retrievals on HD 80606 b emission spectra at 10 phases via easyCHEM-derived abundances; Guillot 2010 4-parameter T-p; gray cloud deck; chemical-equilibrium model preferred over PyratBay free-chemistry retrievals at all post-periapse phases.
- [[2025_Glidden_TRAPPIST1e]] — forward models for H₂-CO₂, pure CO₂, N₂-CO₂, N₂-only, and N₂+CH₄ scenarios for TRAPPIST-1 e; used to derive the μ > 8.6 u MMW constraint and the 5–6.9σ CO₂-ruled-out results.
- [[2025_Crouzet_HATP12b]] — synthetic spectra coupled with VULCAN photochemistry for the HAT-P-12 b NIRSpec G395M analysis.
- [[2025_AcunaAguirre_WASP80b]] — atmospheric forward model in the [[joint-interior-atmosphere-retrieval]] framework on WASP-80 b; coupled with [[GASTLI]] interior structure.
- [[2025_Gordon_COMPASS-G395H]] — used for cross-target model spectra in the COMPASS uniform reanalysis.
