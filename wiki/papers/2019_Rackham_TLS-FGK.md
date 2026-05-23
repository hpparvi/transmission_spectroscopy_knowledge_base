---
type: paper
bibkey: 2019_Rackham_TLS-FGK
authors: [Rackham, B. V., Apai, D., Giampapa, M. S.]
year: 2019
venue: AJ
arxiv: 1812.06184
doi: 10.3847/1538-3881/aaf892
targets: []
instruments: []
methods: [stellar-contamination-modeling]
tags: [tls, foundational, fgk-dwarf-host, methodology, theory, stellar-heterogeneity, transit-light-source-effect, hd-189733b-reinterpretation]
ingested: 2026-05-04
---

# The Transit Light Source Effect. II. The Impact of Stellar Heterogeneity on Transmission Spectra of Planets Orbiting Broadly Sun-like Stars

**Authors:** Rackham, Apai, Giampapa 2019, AJ 157:96 · [arXiv:1812.06184]
**Methods:** [[stellar-contamination-modeling]]

## TL;DR
Companion / extension of [[2018_Rackham_TLS]] to F5V–K9V dwarfs. Same forward-modeling methodology (rotating photospheres, spots ± faculae, A vs. f_spot calibration via Monte Carlo). Typical *Kepler*-sample variability amplitudes: 0.12 % (F5V) → 0.75 % (K0V) → 0.62 % (K9V); corresponding mean spot covering fractions in the spots-only case: 0.1 % (F dwarfs) → ~1 % (G dwarfs) → 1.4–2.1 % (K dwarfs). **TLSE contamination spectra for FGK are 1–2 orders of magnitude weaker than for M dwarfs** but still detectable in high-precision transmission spectra of *active* G/K hosts. Critically, **K dwarfs with unocculted spots produce visible blueward slopes** — the same Rayleigh-like signature that motivated the dust interpretation of [[2008_Pont_HD189733b]] / [[2013_Pont_HD189733b]] for HD 189733 b. The paper explicitly cites the [[2014_McCullough_HD189733b]] reinterpretation: "If the spot coverage is instead ~4 %, McCullough et al. (2014) showed that the observed transmission spectrum is consistent with a clear planetary atmosphere and a larger contribution from unocculted spots." Band-averaged transit-depth offsets for atmospheric absorbers (CH₄, CO, CO₂, H₂O, N₂O, O₂, O₃) are *not* detectable for typically active FGK dwarfs, with two exceptions: stellar **TiO/VO features may produce detectable contamination on active late-K dwarfs**, and atomic line wings of Hα and the Na D + K I doublets remain affected.

## Key findings
- **FGK variability amplitudes scale with spectral type.** From *Kepler* (McQuillan et al. 2014): median variability 0.12 % (F5V) → 0.21 % (F8V) → 0.32 % (G0V) → 0.51 % (G5V) → 0.75 % (K0V) → 0.72 % (K5V) → 0.62 % (K9V). 1σ ranges (16th–84th percentile): 0.07–0.31 % (F5V) → 0.36–1.22 % (K9V).
- **Reference activity-level spot fractions.** Spots-only models: 0.1⁺⁰·¹⁻⁰·¹ % (F5V), 0.3⁺⁰·⁴⁻⁰·² % (G0V), 0.7⁺¹·⁰⁻⁰·⁴ % (G5V), 1.8⁺²·⁶⁻⁰·⁹ % (K0V), 1.7⁺²·⁵⁻⁰·⁸ % (K5V), 1.5⁺²·⁸⁻⁰·⁸ % (K9V). Spots+faculae: 0.1–3.1 % spots + 1–28 % faculae across F5V–K9V.
- **Visual contamination dominantly a slope.** F/G dwarfs with unocculted spots show a uniform blueward slope at λ < 1.7 μm. K dwarfs show *more structured* contamination spectra with TiO/VO bands becoming prominent. **For K dwarfs with unocculted faculae**, contamination factor *decreases* below 1 (transit depth decrease) at visible wavelengths — strongest at UV.
- **K-dwarf TLS produces visible Rayleigh-like slopes — directly relevant to HD 189733 b.** Active K dwarfs at typical 0.7 % variability + ~2 % spot coverage produce contamination spectra that mimic the panchromatic blueward slope attributed to dust by [[2013_Pont_HD189733b]]. Cited explicitly: McCullough's 4 % spot scenario fits HD 189733 b's observed transmission with a clear-atmosphere interpretation. The paper does not adjudicate Pont vs. McCullough but identifies the K-dwarf TLS prediction as a viable alternative slope mechanism.
- **Most molecular features safe for typically active FGK dwarfs.** Band-averaged TLS offsets at CH₄, CO, CO₂, H₂O, N₂O, O₂, O₃ wavelengths are below detection thresholds for all considered FGK spectral types and activity levels.
- **Notable exceptions.** TiO/VO bands appreciable for active late-K dwarfs (relevant to WASP-19 / Espinoza 2019 TiO reinterpretation cited in §1); Hα and Na D / K I doublet line cores remain TLS-sensitive (relevant for high-resolution transmission spectroscopy).
- **Faculae dampen K-dwarf rotational variability** (10:1 facula:spot area at solar-like contrast) — TLSE remains comparable to spots-only at the same variability amplitude.

## Methods
Same as [[2018_Rackham_TLS]] but with PHOENIX (Husser 2013) component spectra at solar metallicity, stellar parameters from Pecaut & Mamajek 2013 + Siess 2000 mass tracks. Spot-temperature relation T_spot = 0.418 × T_phot + 1620 K (fitted from Berdyugina 2005 spot survey, excluding solar penumbra and EK Dra outliers). Faculae fixed at T_phot + 100 K. Contamination spectra computed at 0.3–5.5 μm.

Activity-level reference: median *Kepler* variability per spectral type (Table 3) → spot covering fraction via square-root scaling A = C × f_spot^0.5 with C ≈ 0.04–0.05 in *Kepler*-band (Table 2; nearly spectral-type-independent).

## Caveats & limitations
- F dwarfs have peculiar magnetic morphology — small-spatial-scale flux ropes from thin convection zones; large-scale longitudinal modulation may be absent even when activity is real (Pizzolato et al. 2003; Schmitt 1985 in F-dwarf X-ray context). Photometric variability may *underestimate* TLS spot coverage for early-F dwarfs.
- M dwarfs (Paper I) and FGK dwarfs (this paper) treated separately; the F5V boundary is somewhat sharp.
- Polar spots (sometimes seen in rapidly rotating G/K dwarfs via Doppler imaging) contribute negligibly to rotational variability but full TLS amplitude — could underestimate contamination.
- 10:1 facula:spot area assumed throughout; M dwarf faculae poorly constrained but generally cooler-photosphere/larger-contrast.
- Chromospheres not included in PHOENIX models — UV contamination prediction ignores chromospheric emission, which can dominate at λ < 0.3 μm.
- Latitude-dependent spot distributions limited to within 30° of equator (following solar butterfly diagram); extrapolated to all spectral types.

## Open questions / follow-ups
- **Spectroscopic vs. photometric activity inference.** Hα-only or Ca II HK-only datasets provide spot fraction information not available from photometric monitoring; how do these constrain TLSE for transits?
- **F-dwarf TLSE in practice.** F dwarfs are common hot-Jupiter hosts (KELT, WASP, HATNet); TLS predictions weak (~0.1 % spot fraction) but population-level transmission-spectrum biases not yet measured.
- **Hot-Jupiter K-dwarf retrievals.** Direct test on the [[HD189733b]] panchromatic dataset using a joint TLS + clear-atmosphere or TLS + dust retrieval would adjudicate Pont vs. McCullough — never carried out at the necessary precision.
- **Active vs. quiet pairs.** Are TLS effects detectable as transmission-spectrum offsets between transits acquired at different stellar activity phases? Some evidence in WFC3 transit-to-transit variability of WASP-19 b (Espinoza 2019; not ingested).

## Related
- [[2018_Rackham_TLS]] — Paper I in the series; M-dwarf-focused.
- [[2014_McCullough_HD189733b]] — directly motivates this paper's HD 189733 b discussion; the K-dwarf TLS framework here vindicates McCullough's TLS-based reinterpretation of the [[2013_Pont_HD189733b]] panchromatic slope.
- [[2008_Pont_HD189733b]] / [[2013_Pont_HD189733b]] — the slope datasets that the K-dwarf TLS prediction places in renewed methodological context.
- [[2026_Ashtari_HATS75b]] — first wiki application of joint TLS + atmosphere retrieval on a [[GEMS]]-class M-dwarf gas giant; uses Rackham et al. framework as foundational.
- [[2025_Gressier_HATP26b]] — first wiki *negative* TLS result on a K-dwarf hot Neptune; POSEIDON_TLS Bayes factor < 1 — consistent with this paper's prediction that TLS at typical K-dwarf activity is below detection threshold for molecular bands.
