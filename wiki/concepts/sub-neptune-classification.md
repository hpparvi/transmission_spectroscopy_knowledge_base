---
type: concept
aliases: [volatile-rich sub-Neptune classification, hycean classification, sub-Neptune taxonomy, Madhusudhan classification]
tags: [sub-neptune, classification, habitability, atmospheric-extent, cold-trap]
---

# Sub-Neptune classification (volatile-rich)

A two-axis classification scheme for sub-Neptune-mass exoplanets, organizing them by **equilibrium temperature** (T_eq) and **atmospheric H₂ content**, proposed by [[2025_Madhusudhan_subneptunes]]. Sub-Neptunes have no solar-system analog and span a wide range of bulk compositions and atmospheric structures; the scheme posits six discrete categories that emerge naturally from the interplay of (a) whether liquid water can exist on/near the surface (cold-trap presence vs absence), (b) whether the atmosphere is H₂-dominated or H₂O-dominated, and (c) the relative depth of the H₂ envelope. Complementary to the [[cosmic-shoreline]] which addresses the analogous question for terrestrial planets.

## The six categories

| Category | T_eq range | Atmosphere | Surface / Interior |
|---|---|---|---|
| **Ice worlds** | Cold (T_eq < ~250 K, low irradiation) | Thin H₂ over frozen H₂O ice | Solid water ice deep interior |
| **Hycean worlds** | Warm (~250 K < T_eq < T_crit) with H₂ envelope | H₂-dominated with H₂O cold trap | **Liquid water surface** under H₂ atmosphere |
| **Mini-Neptunes** | Warm with thick H₂ | Deep H₂-dominated atmosphere | High-pressure H₂O ice envelope; no liquid water |
| **Gas dwarfs** | Warm to hot with H₂ over rock | H₂-dominated thin atmosphere | Rocky core, little/no H₂O inventory |
| **Supercritical mini-Neptunes** | Hot (T_eq > T_crit) with intermediate H₂ | Mixed H₂-H₂O envelope | Supercritical H₂O dissolves H₂ at depth |
| **Steam worlds** | Hot (T_eq > T_crit) with H₂O dominant | H₂O-dominated atmosphere | Little/no H₂ envelope above |

The **critical temperature T_crit** is the threshold above which atmospheric H₂O cold-trap condensation is suppressed and atmospheres transition from low-MMW (H₂-dominated) to high-MMW (H₂O-dominated) regimes. Empirically estimated **T_crit ≳ 350 K** by [[2025_Madhusudhan_subneptunes]] from the existing 3-target sample; theoretically uncertain to within ~50–150 K.

## Wiki target placements (current readings)

Per the available data (and noting the contested readings — see § Open issues):

- **[[K2-18b]]** (T_eq = 258 K) — cold side of T_crit; H₂-rich atmosphere with cold trap → **hycean candidate** in Madhusudhan 2025 framing; alternatively a **mini-Neptune** with deep H₂ envelope (not a hycean) per [[2025_FernandezRodriguez_K2-18b]] high C/O reading; or even a **gas dwarf** at higher MMW.
- **[[TOI-270d]]** (T_eq ≈ 360 K) — straddling T_crit; "dark hycean" (Holmberg & Madhusudhan 2024 reading; not ingested) vs **supercritical mini-Neptune** ([[2025_Felix_TOI-270d]] reading; reproduces Benneke 2024).
- **GJ 9827 d** (not ingested; T_eq ≈ 600 K) — **steam world** per Piaulet-Ghorayeb et al. 2024 (not ingested); H₂O at log VMR ≈ −0.5.
- **[[LP-791-18c]]** (T_eq ≈ 355 K) — at T_crit; CH₄ + haze, no CO₂ ([[2025_Roy_LP791-18c]]); placement ambiguous in the scheme.
- **[[V1298Tau-b]]** (T_eq ≈ 670 K, age 10–30 Myr) — **gas dwarf progenitor** per [[2025_Barat_V1298Tau-b]]; ~0.6× solar metallicity, subsolar C/O ~ 0.22, primordial H/He envelope; unusually large radius (9.85 R⊕) for the mass (12 M⊕) reflects ongoing thermal contraction at high T_int (~500 K). The youngest classifiable target; may evolve to gas dwarf/mini-Neptune as mass loss enhances metallicity.

## Open issues

- **T_crit is poorly constrained.** Single-target T_crit estimates range from 300 K to 500 K depending on metallicity assumption and the specific cold-trap pressure profile.
- **Hycean candidates remain contested.** K2-18 b is the canonical case; [[2025_FernandezRodriguez_K2-18b]] argues a primordial H₂-He atmosphere with elevated C and O is consistent with the data without invoking a hycean ocean. [[2025_Felix_TOI-270d]] reaches a similar conclusion for TOI-270 d.
- **Multiple bulk-composition / atmospheric-extent solutions per target.** [[K2-18b]] alone has three published JWST analyses giving three different MMW (~2 amu hycean / ~5.5 amu mini-Neptune-like / contested). The classification depends on which is correct.
- **Need 5–10 well-characterized sub-Neptunes spanning T_eq = 200–800 K** to populate the scheme empirically. Currently 3–4 well-characterized targets globally.
- **Biosignature implications.** Hycean worlds offer the most observationally accessible biosignature targets (DMS, CS₂, OCS, CH₃Cl, N₂O at JWST precision); mini-Neptune and gas dwarf classifications eliminate the habitability case for the same target.

## Related concepts

- **[[cosmic-shoreline]]** — analogous boundary for terrestrial-planet atmosphere retention.
- **[[transmission-spectrum]]** — the primary observable used to populate the scheme.
- **[[disintegrating-planet]]** — orthogonal concept; not a sub-Neptune classification.

## Papers

- [[2025_Madhusudhan_subneptunes]] — proposes the scheme; PNAS perspective; reviews K2-18 b, TOI-270 d, GJ 9827 d as the cornerstone targets and 5+ comparators.
- [[2025_FernandezRodriguez_K2-18b]] — challenges the K2-18 b hycean placement; argues for primordial-H₂-with-elevated-O-and-C (mini-Neptune at high C/O).
- [[2025_Felix_TOI-270d]] — challenges TOI-270 d hycean / dark-hycean placement; argues for metal-rich miscible envelope (supercritical mini-Neptune class).
- [[2025_Roy_LP791-18c]] — sub-Neptune diversity reference at T_crit boundary.
- [[2025_Barat_V1298Tau-b]] — first young (10–30 Myr) sub-Neptune progenitor characterized atmospherically; gas-dwarf precursor with ~0.6× solar metallicity; the methane thermometer reveals high T_int (~500 K) inconsistent with evolutionary models.
