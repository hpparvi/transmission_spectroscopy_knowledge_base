---
type: target
kind: planet
class: sub-neptune
host_star: TOI-270
mass_mearth: 4.97
radius_rearth: 2.16
period_days: 11.380
teq_k: 360
discovery_year: 2019
tags: [sub-neptune, temperate, m-dwarf-host, multi-planet-system, sulfur-chemistry, hycean-debate]
---

# TOI-270 d

A temperate sub-Neptune (R = 2.16 R⊕, M = 4.97 M⊕, T_eq = 340–384 K depending on albedo, period 11.38 d) in the multi-planet TOI-270 system (Günther et al. 2019; not yet ingested), orbiting the M3V dwarf [[TOI-270]]. With three independent JWST analyses ([[2025_Felix_TOI-270d]], plus Benneke et al. 2024 and Holmberg & Madhusudhan 2024 — both not yet ingested), the planet has become a benchmark — and **point of contention** — in the sub-Neptune atmospheric-composition debate. CH₄ and CO₂ are robustly detected; SO₂ is now disfavored. Whether the atmosphere is metal-rich miscible-envelope (MMW ~5.6 amu, [M/H] ~160× solar) or hycean (MMW ~2 amu) remains unresolved across reductions. The same NIRSpec G395H visit captured a simultaneous transit of the inner super-Earth [[TOI-270b]], and TOI-270 d's larger size (1.7×) makes it a 3× more sensitive TLS-contamination probe — leveraged in [[2025_Coulombe_TOI-270b]] to rule out stellar contamination as the source of TOI-270 b's tentative water feature.

## Atmospheric composition

- **Decisive detections** ([[2025_Felix_TOI-270d]]):
  - [[CH4]] — Bayes factor 3 × 10²⁵; log VMR ≈ −1.7. Confirmed by Benneke et al. 2024 and Holmberg & Madhusudhan 2024.
  - [[CO2]] — Bayes factor 3 × 10⁷; log VMR ≈ −1.3. Confirmed by both prior analyses.
- **Moderate to weak evidence:**
  - [[CS2]] (carbon disulfide) — Bayes factor 78 in Felix et al.'s sulfur model; degenerate with CH₃Cl, CH₃F, H₂CS at JWST/NIRSpec resolution.
  - [[NH3]] — Bayes factor 4 (weak preference).
- **Ruled out / upper-limit:**
  - [[SO2]] — < 10⁻⁵ at 3σ ([[2025_Felix_TOI-270d]]); contradicts Benneke et al. 2024's tentative SO₂ inference.
  - [[CO]] — log VMR < −4 (3σ).
  - [[H2S]], OCS, SH, NS — upper limits only.
- **Mass-consistency favored model:** MMW = 5.56 ± 1.10 amu; [M/H] ≈ 160× solar; 4.97 M⊕ retrieved consistent with 4.78 M⊕ from Van Eylen et al. 2021 RVs.

## Observations to date

**JWST [[JWST-GO-4098]] (PI: Benneke & Evans-Soma):**
- **NIRSpec G395H** transit on 2023 October 4 (~5.3 hr observation window; first 1.5 hr overlaps a TOI-270 b transit). Three independent published analyses: Benneke et al. 2024 (not ingested) — fiducial; Holmberg & Madhusudhan 2024 (not ingested) — hycean reading; [[2025_Felix_TOI-270d]] — independent reanalysis with [[BeAR]] retrieval.
- **NIRISS/SOSS** transit on 2024 February 6 (~4.0 hr observation; first-order only; second-order excluded due to stellar contamination at < 0.85 μm).

**Pre-JWST HST WFC3** (Mikal-Evans et al. 2023; not yet ingested) — first H₂O detection on this target.

## Open questions

- **Why does Felix's reduction reproduce Benneke 2024 but not Holmberg & Madhusudhan 2024?** Same dataset, three analyses, two distinct conclusions. A fully independent fourth analysis is needed.
- **Is the 4.6 μm feature CS₂, CH₃Cl, CH₃F, or H₂CS?** All four produce nearly identical opacity in the JWST G395H band; MIRI/LRS or MRS at 8–14 μm is the discriminator.
- **What's driving the high CS₂ signal at 360 K?** Volcanic outgassing, photochemistry, or interior chemistry — not yet constrained. A complete sulfur reaction network (Moses et al. 2024 in prep) is the planned analysis.
- **High CO₂/CH₄ ratio in Felix vs Benneke** — first systematic difference between the analyses; reduction-dependent.

## Tensions

- **Felix vs Holmberg & Madhusudhan 2024 (unresolved).** Same NIRSpec G395H + NIRISS SOSS data, two different MMW (5.56 amu vs ~2 amu) and metallicity readings (~160× solar vs ~10× solar). [[2025_Felix_TOI-270d]] cannot reproduce the hycean fit using their Eureka! + BeAR framework; attributes the difference to T-p profile and bias-correction choices.
- **SO₂ detection (Benneke 2024) vs non-detection (Felix 2025).** Benneke et al. claimed tentative SO₂; [[2025_Felix_TOI-270d]] sets log X < −5 at 3σ — one of the cleaner pipeline-driven null retractions in the wiki.
- **High CO₂/CH₄ ratio (Felix) vs lower in Benneke.** Same data, different ratios — sub-Neptune analog of the WASP-39 b reduction divergence ([[2026_RoyPerez_WASP39b]]).

## See also
- Host: [[TOI-270]]
- Sibling: [[TOI-270b]] (used as the tentative-atmosphere super-Earth in the same visit)
- Concept: [[transmission-spectrum]]
- Comparator: [[K2-18b]], [[LP-791-18c]]
- Concept: [[sub-neptune-classification]] (T_eq ≈ 360 K straddles the proposed T_crit ~350 K boundary)
- Papers: [[2025_Felix_TOI-270d]], [[2025_Coulombe_TOI-270b]] (companion analysis of the inner planet from the same NIRSpec visit), [[2025_Madhusudhan_subneptunes]] (review/perspective; cornerstone target), [[2025_Roy_LP791-18c]] (comparative reference)
