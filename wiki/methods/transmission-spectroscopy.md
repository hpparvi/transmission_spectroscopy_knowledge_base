---
type: method
aliases: [transit spectroscopy, transmission spectrum measurement]
tags: [observational-technique, core-method]
---

# Transmission spectroscopy

The technique of measuring a transiting planet's apparent radius as a function of wavelength, yielding a [[transmission-spectrum]] whose features encode the composition of the day–night terminator atmosphere. In practice: fit spectroscopic light curves in narrow wavelength bins, extract Rp/R⋆ per bin, and compare to forward models or perform [[atmospheric-retrievals]]. Sensitive to absorbing species above the terminator cloud deck and to [[stellar-contamination]] from unocculted heterogeneities.

## Foundational theory

The technique was introduced theoretically by Seager & Sasselov 2000 ([[2000_Seager_TheoryTransmission]]), which established the geometric framework of stellar flux passing through an optically thin "transparent atmosphere" above the limb cloud-top, predicted absorption features at the ~10⁻⁴ to ~10⁻³ level relative to total stellar flux, and identified the Na I D doublet at 589.4 nm as the strongest expected feature. Brown 2001 ([[2001_Brown_TransmissionDiagnostics]]) extended this with the formal "spectrum ratio" R(λ) = F_transit/F_out as the natural observable, parameterized cloud decks, Doppler diagnostics from winds and rotation, and Na/K UV photoionization — defining the diagnostic catalog (cloud height, metallicity, T(P), winds) the field still uses. The Na D prediction was confirmed in the historic Charbonneau et al. 2002 first-detection on HD 209458 b (HST/STIS; not yet ingested).

## Papers
- [[2026_Radica_WASP96b]] — single JWST NIRSpec G395H + archival NIRISS/SOSS + VLT/FORS2 panchromatic transit of WASP-96 b; H₂O, CO₂, Na, tentative SO₂.
- [[2026_Heinke_HATP12b]] — panchromatic NIRISS + NIRSpec G395M + MIRI/LRS + HST/STIS+WFC3 transit of HAT-P-12 b; H₂O, CO₂, CO, H₂S detections.
- [[2026_Ashtari_HATS75b]] — three NIRSpec PRISM transits of the GEMS gas giant HATS-75 b; CH₄, CO, CO₂ detections within a TLS framework.
- [[2025_Tusay_K2-22b]] — four MIRI/LRS transit windows of the disintegrating rocky planet K2-22 b; highly variable depth (0–1627 ppm); one 9.7σ detection; probes escaping dust/gas composition, not a retained atmosphere.
- [[2021_Mugnai_GJ1132b]] — five HST WFC3 G141 transits of GJ 1132 b; flat 1.1–1.6 μm spectrum; no molecular absorption; rules out H₂-dominated atmospheres; rebuts Swain et al. 2021.
- [[2025_Fisher_TOI1685b]] — five NIRSpec G395H transits of the M-dwarf super-Earth TOI-1685 b; flat; MMW ≳ 10 at ~5σ; bare rock.
- [[2025_Espinoza_TRAPPIST1e]] — four NIRSpec PRISM transits of TRAPPIST-1 e; GP stellar contamination marginalization; cloudy H₂-dominated atmospheres ruled out >3σ.
- [[2025_PiauletGhorayeb_TRAPPIST1d]] — two NIRSpec PRISM transits of TRAPPIST-1 d; flat; H₂ excluded >3σ; cloud-free terrestrial analogs excluded >95%.
- [[2025_Glidden_TRAPPIST1e]] — four JWST NIRSpec PRISM transits of the habitable-zone planet TRAPPIST-1 e; featureless; H₂-rich and thick CO₂ ruled out; stellar model fidelity (~1800 ppm) dominates over measurement precision (~89 ppm).
- [[2023_Lim_TRAPPIST1b]] — two NIRISS/SOSS transits of TRAPPIST-1 b; spectrum dominated by stellar contamination; H₂-dominated atmospheres rejected at 16–29σ; secondary atmospheres unconstrained.
- [[2025_Teske_TOI776c]] — two-visit NIRSpec G395H transmission spectrum of the sub-Neptune TOI-776 c (COMPASS); featureless 3–5 μm; rules out metallicity < 180–240× solar, with model-dependent MMW limits.
- [[2025_Redai_GJ357b]] — single NIRSpec G395H transit of GJ 357 b (COMPASS); featureless 2.87–5.14 μm; rules out MMW < 8 g/mol at 3σ.
- [[2025_Taylor_GJ357b]] — single NIRISS/SOSS transit of the super-Earth GJ 357 b; the first NIRISS transmission spectrum in this wiki; partial transit (~60% captured) still yields a useful 0.85–2.8 μm featureless spectrum; rules out ≤100× solar metallicity with cloud-top pressure > 0.01 bar at 3σ.
- [[2025_Bennett_GJ1132b]] — four-visit NIRSpec (G395H + G395M) transmission spectroscopy of GJ 1132 b; coadded spectrum is featureless.
- [[2025_Alam_L168-9b]] — first broadband 3–12 μm (NIRSpec G395H + MIRI/LRS) transmission spectrum of a rocky exoplanet; featureless.
- [[2025_Alderson_TOI-776b]] — two-visit G395H transmission spectroscopy of the super-Earth TOI-776 b; flat after detector-offset correction.
- [[2024_Scarsdale_L98-59c]] — two-visit G395H transmission spectroscopy of L 98-59 c under COMPASS; featureless.
- [[2024_Gressier_L98-59d]] — single-visit G395H transmission spectrum of L 98-59 d; atmospheric feature at 3.3–4.8 μm driven by H₂S/SO₂ (2.6σ–5.6σ).
- [[2024_Banerjee_L98-59d]] — companion retrieval analysis on the same L 98-59 d transit; same sulfur-species preference.
- [[2024_Alderson_TOI-836b]] — two-visit G395H transmission spectroscopy of the super-Earth TOI-836 b; flat spectrum rules out H₂-dominated atmospheres.
- [[2023_May_GJ1132b]] — two NIRSpec G395H transits of GJ 1132 b analyzed with three independent reductions.
- [[2023_Moran_GJ486b]] — two-visit G395H transmission spectroscopy of GJ 486 b; 2.2σ–3.3σ feature across three reductions, degenerate between water-rich atmosphere and stellar-contamination scenarios.
- [[2023_Lustig-Yaeger_LHS475b]] — two-visit G395H transmission spectroscopy of the Earth-sized LHS 475 b; featureless, rules out H₂/He atmospheres at >10σ.
