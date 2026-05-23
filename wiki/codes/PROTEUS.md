---
type: code
aliases: [PROTEUS-photochem]
tags: [photochemistry, 1d-photochem, H-C-O-network, hycean-modeling]
---

# PROTEUS

1D photochemical model for plane-parallel exoplanet atmospheres (Nakamura et al. 2023; not ingested). Originally developed for Solar System bodies (Jovian ionosphere, Mars, Earth) and adapted to exoplanet contexts. Tracks 48 H–C–O species and 322 bimolecular / termolecular / photolysis reactions across configurable altitude grids. Used in [[2026_Fujisawa_K2-18b]] for the first quantitative photochem + climate self-consistency check of a Hycean atmosphere on [[K2-18b]] — finds **photochemically-driven CH₄ depletion near 600 km altitude** produces a "photochemical saturation" plateau in transit depth that explains observed flat-topped CH₄ band shapes better than vertically uniform mixing.

Distinct from [[VULCAN]] (Tsai et al. 2017+; widely used in this wiki for gas-giant photochemistry) and [[Photochem]] (Wogan et al. 2023+; coupled with climate for rocky and sub-Neptune work). PROTEUS's network is less extensive than VULCAN's SNCHO_PHOTO_NETWORK (no S/N chemistry by default in the published version) but includes hydrocarbon polymerization channels (C₂H₆ → C₂H₂ → C₂ radicals) that contribute to the K2-18 b CH₄ depletion layer interpretation. Public network at Zenodo (Fujisawa et al. 2026 not ingested).

## Papers
- [[2026_Fujisawa_K2-18b]] — first wiki usage; Hycean K2-18 b atmosphere photochemistry + transit spectrum forward model.
