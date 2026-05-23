---
type: concept
aliases: [thermal dissociation, H2 dissociation, H2O dissociation, molecular dissociation]
tags: [ultra-hot-jupiter, dayside-chemistry, hemispheric-heterogeneity]
---

# Thermal dissociation

In **ultra-hot-Jupiter** atmospheres (T_eq ≳ 2000 K), dayside photospheric temperatures are high enough to dissociate molecular species — including H₂O and even H₂ itself — into atoms (H, O), substantially altering the gaseous opacity, mean molecular weight, and atmospheric scale height. On the cooler nightside, dissociated species recombine. This **dayside–nightside chemical asymmetry** is the dominant 3D effect that biases 1D retrievals of ultra-hot-Jupiter transmission spectra.

## Observational consequences

- **Inflated dayside scale height** (low MMW from H₂ dissociation) increases the apparent transit-radius contribution from the dayside — molecules abundant on the dayside (e.g., CO, which is more stable than H₂O at these temperatures) have **enhanced** absorption-feature amplitudes; molecules abundant only on the nightside (e.g., H₂O) have **suppressed** amplitudes (Pluriel et al. 2020, Caldas et al. 2019).
- **C/O bias**: 1D spherical-symmetry retrievals with prescribed equilibrium chemistry tend to **overestimate C/O** because the negative correlation between H₂ dissociation and CO abundance is uncaptured.
- **Doppler signatures**: high-resolution Doppler tracking (e.g., Wardenier 2024 IGRINS) shows H₂O lines blue-shifting toward the trailing limb during transit (signature of the limb where H₂O is depleted) while CO lines are uniform — a complementary diagnostic.

## Mitigations

- **Dayside/nightside split atmospheric model** (Gapp et al. 2025): two separate P–T profiles, abundances, and opacity sources combined with appropriate weighting; an upgrade over 1D that captures the leading hemispheric asymmetry.
- **GCM-coupled retrievals**: emulator-based or hierarchical 3D retrievals — broadly emerging.
- **Limb-resolved retrievals** ([[Catwoman]]): orthogonal to the dayside/nightside split; partially captures evening/morning differences.

## Papers

- [[2025_Gapp_WASP121b]] — direct evidence for thermal dissociation of H₂O and H₂ on [[WASP-121b]] dayside via JWST NIRSpec G395H; introduces a custom dayside/nightside [[NEMESISPY]] split model demonstrating that ignoring hemispheric heterogeneity biases C/O.
