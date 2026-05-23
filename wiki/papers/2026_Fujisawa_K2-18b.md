---
type: paper
bibkey: 2026_Fujisawa_K2-18b
authors: [Fujisawa, T., Shimada, M., Yoshida, T., Kuramoto, K.]
year: 2026
venue: arXiv preprint (May 2026)
arxiv: 2605.17803
doi: ""
targets: [K2-18b]
instruments: [JWST-NIRSpec, JWST-NIRISS]
methods: [transmission-spectroscopy, atmospheric-retrievals]
species_detected: []
species_tentative: []
species_ruled_out: []
codes: [PROTEUS]
tags: [sub-neptune, m-dwarf-host, habitable-zone, hycean-debate, photochemistry, climate-modeling, c-o-ratio, ocean-buffering]
ingested: 2026-05-22
---

# A Hycean Interpretation of K2-18b Supported by Photochemical Atmospheric Compositional Structure

**Authors:** Fujisawa, Shimada, Yoshida, Kuramoto (2026, arXiv:2605.17803) · submitted May 2026
**Target:** [[K2-18b]] · **Instruments:** [[JWST-NIRSpec]] G395H + [[JWST-NIRISS]] SOSS (using literature reductions from Madhusudhan et al. 2023 (not ingested), exoTEDRF and FIREFLy from [[2025_Schmidt_K2-18b]], and Eureka! reductions A/B from [[2025_Schmidt_K2-18b]])
**Program:** [[JWST-GO-2722]] (PI: Madhusudhan; reanalysis only)

## TL;DR

Demonstrates that **Hycean (H₂ envelope over liquid-water ocean) configurations of [[K2-18b]] remain consistent with the existing JWST NIRISS+NIRSpec G395H transmission spectra** once photochemically-induced vertical gradients are properly modelled. The paper applies the 1D photochemical model [[PROTEUS]] to a 1-bar H₂ atmosphere above a liquid-water surface (T_s = 328 K) with fixed surface mixing ratios X_CH₄ = X_CO₂ = 1 % (the Madhusudhan 2023 best-fit). The CH₄ photodissociation network drives **percent-level CO** mixing ratios in the upper atmosphere and produces a **sharp CH₄ depletion layer near 600 km altitude** — yielding "**photochemical saturation**" plateaus in the 2.8–4.0 μm transmission spectrum that **better fit the data than vertically uniform mixing ratios** (R≈25 reduced χ² 3.15 vs 4.26 for the Madhusudhan reduction; 1.95 vs 2.50–2.38 for exoTEDRF / FIREFLy reductions). Mass-balance + ocean-buffering analysis allows **CO₂ to be buffered at 10⁻³–10⁻² in CO₂-poor scenarios** — consistent with the [[2025_Schmidt_K2-18b]] mini-Neptune interpretation but also reconciling Hycean with the apparent non-detection of CO₂. Concludes that **current CO and CO₂ constraints alone are not yet sufficient to rule out the Hycean interpretation**, and that mass-balance of CH₄ requires sustained interior replenishment (~10¹¹ g s⁻¹ H₂ escape) over gigayear timescales — implying K2-18 b's atmosphere, if Hycean, is a *dynamic steady state* rather than a static equilibrium.

## Key findings

- **Photochemically-driven vertical CH₄ profile**: CH₄ mixing ratio drops sharply by ~3 dex at ~600 km altitude (~10⁻² bar) due to (i) direct photodissociation, (ii) enhanced destruction by C₂ radicals produced from C₂H₆ → C₂H₂ → C₂ photolysis. The lower atmosphere remains CH₄-rich at the prescribed 1% surface mixing ratio.
- **Photochemical saturation**: across the 2.8–4.0 μm CH₄ band, the effective transit radius is set by nearly the same altitude (just below the CH₄ depletion layer), producing a **flat-topped plateau** in transit depth that mimics the observed feature shape. Vertically uniform models predict pronounced peaks/troughs that fit worse.
- **χ²_ν improvement** (R≈25 in NIRISS band, 0.8–2.8 μm):
  - Madhusudhan 2023 reduction: 3.154 (photochem) vs 4.257 (uniform).
  - exoTEDRF: 1.949 vs 2.501.
  - FIREFLy: 1.952 vs 2.379.
- **Offset constraints from the CH₄ band**: 1σ offset between NIRISS and NIRSpec G395H = −58 ppm (Madhusudhan), −55 ppm (exoTEDRF), −63 ppm (FIREFLy) — all consistent and in line with the offset values used in [[2025_Schmidt_K2-18b]].
- **CO + CO₂ constraints from 4–5 μm**:
  - For Madhusudhan 2023 (R≈55 binning): CO posterior strongly peaked at X_CO ≲ 10⁻³ (2σ); CO₂ allows X_CO₂ ≳ 10⁻³ with 53% probability.
  - For exoTEDRF (R≈100): X_CO ~ 10⁻³–10⁻² preferred (best 4.0×10⁻³); X_CO₂ ~ 10⁻¹ (best 1.0×10⁻¹). **High-CO solutions favored.**
  - For FIREFLy (R≈100): mixed; X_CO ~ 10⁻⁷ best, but P(X_CO ≥ 10⁻³) = 0.19.
  - For Eureka! Reductions A and B: similar mixed signatures; X_CO ranges 10⁻⁵–10⁻², X_CO₂ ranges 10⁻⁵–10⁻¹.
- **Conclusion on CO/CO₂**: low CO abundances inferred from R≈55 retrievals are **sensitive to binning** — when native pixel-level R≈100 data are used, the preferred CO mixing ratio for exoTEDRF jumps by 4 dex. This is the largest reduction-related systematic identified in the paper.
- **Mass-balance of CH₄**: 1-bar H₂ envelope with 1 % CH₄ has photochemical lifetime ~1.2×10⁷ yr (~3 Gyr / 250). For CH₄ to persist, interior outgassing must replenish ~5×10³ kg s⁻¹ — feasible if water-rock reactions and primordial organic decomposition provide ~3×10⁵ kg s⁻¹ organic processing rate (~7.8 % H content in Halley-comet-like material → 8.6 M⊕ K2-18 b for 3 Gyr).
- **Mass-balance of H₂**: photochemical H₂ production ≈ 2.65×10³ kg s⁻¹; H₂ escape via CH₄-cooled hydrodynamic limit ≈ 2.64×10⁴ kg s⁻¹ (Yoshida & Kuramoto 2020 not ingested). Net loss → ~4×10⁷ yr H₂ envelope depletion timescale. **Implies that a Hycean K2-18 b atmosphere is a dynamic steady-state** rather than primordial — interior replenishment is required.
- **Radiative-convective climate constraints**: a 1-bar H₂ envelope requires Bond albedo A_B ≳ 0.3 to avoid the runaway-greenhouse threshold. Photochemical hydrocarbon hazes (C₃H₈ polymerization with 1% branching ratio) yield haze production flux F_haze ~ 10² kg s⁻¹, column densities ~10⁻⁵–10⁻⁴ kg m⁻², optical depths τ_λ ~ 0.01–1 — potentially supplying the high albedo needed.
- **CO₂ mass-balance with ocean buffering**: CO₂ produced photochemically (CO + OH → CO₂ + H) at 10⁻¹ to 10² kg s⁻¹ depending on stratospheric H₂O abundance. With ocean carbonate enhancement factors β = 10²–10³ (mildly alkaline Earth-like to strongly alkaline) and ocean depth factor f ~ 1, the steady-state atmospheric CO₂ can be **buffered at 10⁻³–10⁻²** — consistent with both the Hycean inference and the Schmidt mini-Neptune scenario.

## Methods

- **Photochemistry**: [[PROTEUS]] 1D photochemical model (Nakamura 2023 not ingested) — 48 H–C–O species, 322 reactions, 100 layers from surface to 900 km (~10⁻⁸ bar). H₂O condensation at surface (liquid ocean) + H₂CO surface deposition velocity 10⁻³ m s⁻¹. Stellar spectrum from GJ 176 (MUSCLES; France 2016 not ingested) rescaled to K2-18 b's irradiation.
- **Radiative-convective climate**: Yoshida et al. 2025 (not ingested) 1D radiative–convective-equilibrium model for H₂-rich atmospheres over liquid H₂O ocean. 200 layers from 1 bar to 10⁻⁶ bar; moist adiabat below tropopause, isothermal stratosphere fitted to skin temperature. H₂–H₂ CIA + H₂O continuum (Mlawer 2023 not ingested) + Rayleigh scattering H₂/H₂O. Surface albedo 0.06 (dark ocean; Hu 2021 not ingested).
- **Transit-spectrum model** (Section 2.2.1, eqs. 1–5): plane-parallel slant-optical-depth calculation; AURA-derived parameterization for aerosols + cloud + haze + stellar contamination (Pinhas 2018 not ingested) — held fixed at Madhusudhan 2023 best-fits for each reduction.
- **Offset scan**: marginalize over wavelength-independent offset Δ_off ∈ [−100, 100] ppm with χ²_CH₄(Δ_off) restricted to 2.8–4.0 μm.
- **CO/CO₂ grid scan**: 2D grid over (X_CO, X_CO₂) ∈ [10⁻¹³, 0.18] × [10⁻¹³, 0.18], weighted by p(Δ_off) from the CH₄ band.
- **Ocean-buffering analysis** (Appendix A): Henry's law + carbonate equilibrium; DIC = β × [CO₂(aq)]; β = 1 + [HCO₃⁻]/[CO₂(aq)] + [CO₃²⁻]/[CO₂(aq)]; mass balance M_C,tot ≳ M_CO₂,prod = F_CO₂ × t.
- **Mass-balance diagnostics** (eqs. 12–37): full atmospheric H–C–O reaction-rate budget; CH₄ → CO₂ conversion rate ~5.5×10³ kg s⁻¹.
- **Haze-production estimate** (Appendix C): integrated C₃H₈ loss flux from PROTEUS (~1.77×10⁴ kg s⁻¹) × 1% polymerization branching ratio (Yoshida 2024 not ingested).

## Caveats & limitations

- **Surface mixing ratios for CH₄ and CO₂ are fixed at 1%** following Madhusudhan 2023 — the paper does *not* re-derive these from data; the photochemical model assesses *consistency with* this Hycean configuration rather than alternative starting points.
- **NH₃ and H₂S excluded** under the Hu et al. 2021 ocean-dissolution argument (highly soluble); molecular nitrogen included at 1% inert background. Both assumptions are part of the Hycean prescription.
- **P–T profile fixed** at the radiative-convective solution rather than coupled fully with photochemistry — argued robust against feedback because radiatively active species (H₂, H₂O, CO₂, CH₄, CO, C₂H₆) are dominant and the photochemically produced trace species don't change T by more than ~5 K.
- **CO depletion via ocean uptake** is computed using a simple Henry's-law + deposition framework; no explicit ocean GCM or pH evolution. CO accumulation in the upper atmosphere is sustained at percent levels under the standard Hycean model — formally in **tension with the lowest-binning CO posterior** for Madhusudhan 2023 (where X_CO ≲ 10⁻³ is preferred) but reconciled by switching to native R≈100 reductions.
- **Stratospheric H₂O range explored is 10⁻⁷ to 10⁻³** — broad enough to span the radiative-convective output but does not include lower values that would require interior cooling channels not in the simple model.
- **Mass-balance estimates depend on ocean-buffering parameters** (β, f) and assume present-day Earth-like to mildly alkaline pH. More acidic or more alkaline reservoirs would shift CO₂ buffering by orders of magnitude.
- **The photochemical Hycean scenario does not predict observable DMS** — the model does not include sulfur chemistry. The DMS biosignature debate is not addressed.

## Open questions / follow-ups

- **High-CO Hycean prediction is testable**: a 1 % atmospheric CO mixing ratio should produce a clear 4.7 μm CO feature; current data are inconclusive but next-generation NIRSpec G395H stacking should distinguish 10⁻³ vs 10⁻⁵ CO at high confidence.
- **CO₂ mass-balance requires alkaline ocean** (β ~ 10²–10³) — observational test of ocean pH not feasible, but interior models predicting more acidic conditions would falsify CO₂ buffering.
- **Photochemical haze contribution to A_B** (~0.2–0.3 from Titan-tholin analog) needs lab measurement of K2-18 b-condition refractive indices; current estimate is order-of-magnitude.
- **Whether CH₄ depletion plateaus persist** under fully coupled climate–photochemistry calculations with stratospheric drying (Bond albedo ≳ 0.5) — would test whether the photochemical-saturation explanation generalizes.
- **Comparison to mini-Neptune alternative** ([[2025_Schmidt_K2-18b]] / [[2025_FernandezRodriguez_K2-18b]] / [[2025_Luque_K2-18b]]): the photochem-Hycean vs deep-H₂-envelope mini-Neptune distinction may require **MIRI 5–12 μm data** with the photochemical vertical profile properly included.
- **Sulfur chemistry**: this model does not address the DMS biosignature debate; a full S-network photochemistry coupling is needed to test whether Hycean + CH₄-rich + percent-level CO predicts negligible DMS (which would be consistent with the [[2025_Luque_K2-18b]] / [[2025_FernandezRodriguez_K2-18b]] / [[2025_PicaCiamarra_K2-18b]] non-detections).

## Related

- [[2025_Schmidt_K2-18b]] — primary methodological counterpoint: ensemble retrieval over 60 data × retrieval combinations rejects DMS/CO₂ and supports oxygen-poor mini-Neptune (C/O ≈ 3.25); this paper's photochemical-Hycean analysis works *with* the Schmidt reductions and argues the conclusions are not yet decisive.
- [[2025_FernandezRodriguez_K2-18b]] — independent retraction of DMS + supersolar C/O ≈ 10–13 IOPF interpretation; this paper's Hycean configuration is at the opposite end of the C/O space.
- [[2025_Luque_K2-18b]] — joint NIR+MIR retrieval showing DMS+DMDS not preferred (Δln Z ≤ 2.8); ethane fits comparably. This paper's photochemistry predicts percent-level CO + low-but-not-zero ethane consistent with the Luque framework.
- [[2025_PicaCiamarra_K2-18b]] — 650-molecule agnostic search retracting DMS uniqueness; this paper's Hycean view doesn't address the DMS debate but is compatible with non-detection.
- [[2025_Madhusudhan_K2-18b-MIRI]] — the contested DMS/MIRI claim. This paper's framework does not invoke DMS but does not rule it out.
- [[2025_Taylor_K2-18b-MIRI]] — model-agnostic Gaussian critique. Independent of this paper but converges on the message that K2-18 b's atmospheric story is not yet settled.
- [[2025_Jaziri_K2-18b]] — photochemical-haze-based reconciliation of MIRI/LRS amplitude tension; complementary aerosol-side analysis to this paper's photochemical-vertical-profile angle.
- [[2025_Madhusudhan_subneptunes]] — perspective paper defining "Hycean" rigorously; this paper provides the first quantitative photochem + climate self-consistency check.
- Code: [[PROTEUS]] (this paper introduces it to the wiki).
