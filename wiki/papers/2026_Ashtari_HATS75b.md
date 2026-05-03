---
type: paper
bibkey: 2026_Ashtari_HATS75b
authors: [Ashtari, R., Lustig-Yaeger, J., Libby-Roberts, J., Müller, S., Kanodia, S., Stevenson, K. B., Cañas, C. I., Guzmán Caloca, G., et al.]
year: 2026
venue: AJ (accepted)
arxiv: 2604.07268
targets: [HATS-75b]
instruments: [JWST-NIRSpec]
methods: [transmission-spectroscopy, atmospheric-retrievals, stellar-contamination-modeling]
species_detected: [CH4, CO, CO2]
species_ruled_out: []
codes: [Eureka, POSEIDON, fleck, spotrod, MultiNest]
tags: [gas-giant, m-dwarf-host, gems, sub-solar-metallicity, tls, jwst-go-3171]
ingested: 2026-04-29
---

# GEMS JWST: HATS-75 b — A giant planet with a sub-solar metallicity atmosphere orbiting an M-dwarf

**Authors:** Ashtari, Lustig-Yaeger, Libby-Roberts, Müller, Kanodia, Stevenson, Cañas, Guzmán Caloca, et al. (2026, AJ; arXiv:2604.07268)
**Target:** [[HATS-75b]] · **Host:** [[HATS-75]] (early M, T_eff ≈ 3790 K) · **Instrument:** [[JWST-NIRSpec]] (PRISM)
**Program:** [[JWST-GO-3171]] (GEMS-JWST)

## TL;DR

Three JWST NIRSpec PRISM transits of [[HATS-75b]] — the **first wiki paper on a Giant Exoplanet around an M-dwarf Star ([[GEMS]])** — yield a transmission spectrum jointly shaped by atmospheric absorption and stellar contamination ([[stellar-contamination]] / TLS). Independent stellar-activity evidence (rotation, spot-crossings) favors the contamination scenario; retrievals within that framework recover [[CH4]], [[CO]], [[CO2]] at >3σ but only an upper limit on [[H2O]] (likely masked by spots). Atmospheric metallicity log [M/H] = −1.74 +0.92/−0.76 (sub-solar; ~1% solar) with super-solar C/O ≈ 1.04 — sharply contrasting with a much higher inferred bulk planetary metallicity Z_p ≈ 0.20, implying inefficient vertical mixing.

## Key findings

- **Detections (free-chemistry retrievals, TLS scenario):** [[CH4]], [[CO]], [[CO2]] at >3σ.
- **Upper limit only on [[H2O]]** — likely masked by stellar contamination from cool spots.
- **Atmospheric metallicity:** log [M/H] = −1.74 +0.92/−0.76 (~1% solar; sub-solar) — surprising for a giant planet.
- **C/O = 1.04 +0.40/−0.09** — super-solar, consistent with unity.
- **Bulk planetary metallicity Z_p = 0.20 ± 0.04** — ~2 dex more metal-rich than the atmospheric inference, implying inefficient vertical mixing.
- **Internal temperature** T_int ≈ 72 K.
- **Stellar contamination parameters:** T_spot ≈ 3365 K (retrieval) / ~3300 K (spot-crossing fits); T_fac ≈ 3909 K; f_spot ≈ 0.23, f_fac ≈ 0.25.
- **Two competing forward-model families** are tested: (A) hazy clear atmosphere; (B) TLS / unocculted spot+facula contamination. Independent activity evidence favors (B).

## Methods

- **Observations:** Three transits (2024 Aug 9, 15, 17); JWST NIRSpec PRISM, BOTS, SUB512 subarray, 5 groups/integration, 14402 integrations/exposure (~5.5 h/visit).
- **Two independent reductions:** (i) Optimized [[Eureka]] + [[fleck]] + `emcee`; (ii) Manual Eureka + [[spotrod]] + `dynesty`.
- **Transit model:** `batman`; spot models: [[fleck]] / [[spotrod]].
- **Atmospheric retrievals:** [[POSEIDON]] in both free-chemistry and chemical-equilibrium modes; isothermal T–P; [[MultiNest]] sampler.
- **Bulk-interior modeling:** MCMC tying mass, radius, atmospheric [M/H], and age (1–10 Gyr) to infer Z_p and T_int.

## Caveats & limitations

- **Atmosphere vs. stellar-contamination degeneracy is fundamental** — both can fit the spectrum; preference for TLS rests on independent activity evidence (rotation, spot-crossings), not the spectrum alone.
- **H₂O upper limit only;** could be intrinsic or masked.
- **Isothermal T–P** may bias retrievals; T_iso is poorly constrained.
- **Equilibrium-chemistry retrievals** initially gravitated to a spurious high-metallicity solution; required prior tightening.
- **Period was fixed** (computational cost); Teq taken from discovery paper (Jordán et al. 2022; not yet ingested).
- **2σ-level offsets** between spot temperatures from the spotrod flux-ratio fits and from retrievals.

## Open questions / follow-ups

- **Bulk-vs-atmospheric metallicity tension:** Z_p ≈ 0.20 vs log [M/H] = −1.74 is a ~2-dex gap. Does inefficient vertical mixing fully explain it, or are formation-history (sequestration, late-stage planetesimal accretion) effects involved?
- **Is the stellar-contamination preference robust?** Multi-epoch monitoring or a near-airless reference system would strengthen the TLS interpretation.
- **First wiki target in the GEMS class:** how do other GEMS targets compare? (GO 3171 surveys 7 such planets.)

## Related

- [[2026_Radica_WASP96b]], [[2025_Gressier_WASP17b]] — hot/warm gas giant chemistry retrievals on F/G/K-dwarf hosts; contrast with the M-dwarf-host stellar-contamination challenge here.
- [[stellar-contamination]] (hub) — the underlying TLS phenomenon, previously a central concern for M-dwarf rocky-planet papers; now a major systematic for [[GEMS]] giants too.
- [[2023_Lim_TRAPPIST1b]], [[2023_Moran_GJ486b]] — earlier wiki cases of atmosphere-vs-contamination degeneracy on M-dwarf rocky planets.
