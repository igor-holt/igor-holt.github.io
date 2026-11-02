# Information-Thermodynamic Technosignatures: A Feasibility Framework

## Solution

**Verdict.** Detection is feasible only where physics forces the information budget into view: entropy export, deliberately structured (low-entropy) emission, and long-lived scars in composition and dynamics. You cannot observe the content of efficient engineering. A capacity-optimal signal is spectrally indistinguishable from thermal noise (Lachmann, Newman & Moore 2004). Channels ranked by expected yield:

1. **Entropy budget (waste heat).** The second law requires it for any large-scale irreversible computation, and archival data can already test it. This is the recommended primary channel.
2. **Design features** (error-correcting codes, signal constellations, exact high-complexity repetition). This catches only beacons and leakage, but it is the only channel that can support an "artificial" claim.
3. **Cradle archaeology.** These scars persist for Gyr, but they look like natural chemical peculiarity. Use them only for secondary scoring.
4. **Gravitational/compact objects.** Lowest yield. Known physics closes the fabrication routes, and a black hole does not record how it formed.

**Premise corrections** (flagged before building on them):
- "Artificial PBH" contradicts itself, since primordial means formed in the early universe. By the no-hair theorem a hole carries only $(M,J,Q)$. Its Hawking spectrum is fixed by those plus the particle content. An "anomalous profile" would therefore point to new physics or an engineered environment, never to artificial origin.
- Kolmogorov complexity is uncomputable. For a photon-limited time series, raw $K(x)$ is dominated by shot noise. What matters is the complexity of the best model, not of the data.
- No statistic can "confirm" directed processing. A test can reject a natural model family at a stated significance. Only design features justify calling something artificial.

### 1 · Informational metrics

**Thermodynamic channel.** Compute the radiative entropy output mode by mode from the observed spectral energy distribution (SED). The emitting radius $R$ comes from interferometry or from Gaia distance plus an SED fit:

$$n_\nu=\frac{c^2I_\nu}{2h\nu^3},\quad \mathcal L_\nu=\frac{2k_B\nu^2}{c^2}\Big[(1+n_\nu)\ln(1+n_\nu)-n_\nu\ln n_\nu\Big],\quad \dot S=4\pi^2R^2\!\int\!\mathcal L_\nu\,d\nu$$

For a blackbody this reduces to $\dot S=\tfrac43L/T$. For real stars, evaluate it on the model-atmosphere SED. Wright et al. (2014) write the energy balance as AGENT: captured starlight α plus other inputs ε equals thermal waste γ plus non-thermal losses ν. Taking γ = α and ε = ν = 0:

$$\Xi\equiv\frac{\dot S_{\rm obs}}{\dot S_{\rm phot}}-1=\alpha\Big(\frac{T_\star}{T_w}-1\Big),\qquad \dot N_{\rm bit}\le\frac{\dot S_{\rm gen}}{k_B\ln2}=\frac{4\alpha L_\star}{3k_B\ln2}\Big(\frac{1}{T_w}-\frac{1}{T_\star}\Big)$$

The second expression is Landauer's bound written in entropy form: each erased bit must export at least $k_B\ln2$.

Solar anchors:
- The bare photosphere exports $8.8\times10^{22}$ W/K. In Landauer units that is $9.2\times10^{45}$ bit/s, about 5.2 bits per thermal photon.
- A complete swarm radiating at 300 K raises the erasure ceiling to $1.7\times10^{47}$ bit/s. Its radiator is about 1.7 AU in radius and peaks at 9.7 µm.
- A swarm capturing only 1% of the light already gives Ξ ≈ 0.18.

So the observable correlate of computation is Ξ. Its spectral shape is set by $T_w$, not by what is being computed.

**Photon-statistical channel (coherence).**
- Entropy per photon $\bar s=\dot S/\dot N_\gamma$ is $3.60\,k_B$ for thermal light. Coherent emission gives $\bar s\ll k_B$, because occupation per mode is $n\gg1$; in the Rayleigh–Jeans limit $n=k_BT_b/h\nu$.
- Coherence length is $\ell_c=c/\Delta\nu$. The narrowest natural lines (masers, about 0.1 km/s) give $\ell_c\lesssim10^6$ m at GHz frequencies. A signal narrower than 1 Hz gives $\ell_c\gtrsim3\times10^8$ m, after correcting for Doppler drift $\dot\nu=\nu a_{\rm los}/c$.
- The photon-correlation statistic $g^{(2)}(0)$ is 2 for thermal light and 1 for coherent light. Stellar intensity interferometry on Cherenkov arrays can measure it.
- Brightness temperature above the ~$10^{12}$ K inverse-Compton limit proves coherence, not artifice. Pulsars, electron-cyclotron maser emission (ECMI) and FRBs all exceed it.
- Polarization of quiet dwarfs is ppm-level and varies smoothly with rotation. Discrete switching between polarization states is a design feature (test 1 in §2).

**Algorithmic channel.** Use the two-part minimum description length, $L(x)=\min_M[L(M)+L(x\mid M)]$. Effective complexity is the model part, $\mathcal E=L(M^{\star})$ (Gell-Mann & Lloyd 1996). Compute it on noise-whitened residuals $\tilde r=\Sigma^{-1/2}[x-\mathcal M_0(\hat\theta)]$, where $\mathcal M_0$ is the natural model family. Practical proxies:
- LZ76 complexity.
- Permutation entropy (Bandt & Pompe 2002).
- Statistical complexity $C_\mu$ and entropy rate $h_\mu$ from ε-machine reconstruction (Crutchfield & Young 1989).
- Normalized compression distance (NCD) between observing epochs (Cilibrasi & Vitányi 2005).

These yield two invariants:
- **Model growth** $\Gamma=dL(M^{\star}_N)/d\log_2N$. Parametric natural processes saturate at $k/2$, where $k$ is the number of parameters. A learnable information stream grows in proportion to $N$.
- **Fold complexity** $\kappa(P)$: compressed bits per folded period at the noise floor. Natural periodic sources have smooth, few-component profiles with jitter. A profile with $\kappa\gg10^3$ bits whose folds stay identical (NCD → 0) is a design signature.

Observability ceiling: the most information you can recover from a fractional rms modulation $\epsilon$ on a collected photon rate Φ, when shot noise dominates at low signal-to-noise:

$$\mathcal C\approx\frac{\epsilon^2\Phi}{2\ln2}\approx70\ {\rm bit\,s^{-1}}\Big(\frac{\epsilon}{10^{-4}}\Big)^2\Big(\frac{\Phi}{10^{10}\,{\rm s^{-1}}}\Big)$$

Φ ≈ 10¹⁰ s⁻¹ corresponds to a Sun-like star at 10 pc in a JWST-class aperture. For bright solar-type targets, granulation and p-modes stay above the shot-noise floor until roughly 10 mHz. Search above that.

The companion calculator (Technosignature Information-Budget Calculator, `entropy-calculator.html`, published with this document) implements these budgets and the compact-object numbers from §3. Its defaults reproduce the solar anchors.

The calculator assumes three things. All captured power leaves as thermal radiation (γ = α). Photons carry about 10% of the Hawking output. Lifetimes are normalized to the ~5×10¹⁴ g hole that evaporates in 13.8 Gyr **under all-species (full Standard Model) emission; photon-only, the same hole lives ~3.3×10¹¹ yr**.

### 2 · Natural baselines vs. artificial modulation

Fit the full natural model family $\mathcal M_0$ before scoring any anomaly:

| Process | Fingerprint | Mimics |
|---|---|---|
| Granulation | super-Lorentzian background, minutes | low-frequency structure |
| p-modes | Lorentzian peaks, random phases, coherent ≲ days | periodic beacon |
| Spots/rotation | quasi-periodic, evolving | periodic dimming |
| Flares/CMEs | dN/dE ∝ E^(−α), α ≈ 2; coronal dimming | pulses |
| Accretion dippers | chromatic, quasi-periodic, 1–50% depth | megastructure transits |
| Rings, exocomets, dust | asymmetric, aperiodic dips | non-spherical occulters |
| Coherent radio | ECMI (~100% circular, ≳MHz wide), pulsars, long-period transients, masers | narrowband or pulsed beacon |
| Confusion | background AGN, blends, systematics, RFI | IR excess, cross-star correlation |

Tests, ranked by evidential strength:

1. **Algebraic redundancy.** Recover the symbol clock, binarize, stack the bits into m×n blocks, and compute the rank over GF(2). For random bits, $P({\rm rank}<n)\approx2^{-(m-n)}$. A persistent rank deficit means a linear error-correcting code (blind code recognition, Valembois 2001). The analog version is IQ or Stokes samples clustering into a finite constellation, as in phase or polarization keying. No natural process is known to produce either.
2. **High-κ exact periodicity.** A complex folded profile that stays phase-coherent far longer than natural damping or jitter times allow.
3. **Physical-admissibility violations.** Examples:
   - Transit kinematics that are non-Keplerian given the asteroseismic stellar density $\rho_\star$ (statites, light sails).
   - A line narrower than the maser floor in the sky-fixed frame.
   - An AGENT energy balance that closes with a featureless radiator, with no 9.7 or 18 µm silicate bands.
   - Failing the radius–temperature test in §3.
4. **Model-family rejection.**
   - Run IAAFT surrogates (Theiler et al. 1992; Schreiber & Schmitz 1996) on the residual LZ complexity, permutation entropy and nonlinear prediction error.
   - Look for outliers on the complexity–entropy plane (Rosso et al. 2007).
   - Look for unbounded Γ growth.

   Include long-memory nulls such as ARFIMA, fractional Gaussian noise and self-organized criticality. Without them, 1/f processes masquerade as unbounded complexity.
5. **Cross-target coordination.** Measure transfer entropy between stars at the lags their geometry predicts (SETI ellipsoid). Exclude zero-lag common-mode systematics.
6. **Language-likeness** (Zipf statistics, conditional-entropy decay). Weakest, because power laws are generic in nature.

Claim tiers:
- **Anomaly:** $\mathcal M_0$ rejected at ≥5σ global significance, after look-elsewhere correction (Gross & Vitells 2010) and false-discovery-rate control across the catalog.
- **Candidate:** an admissibility violation, independently re-detected.
- **Artificial:** test 1 or 2 replicated on at least two independent facilities.

Do not compute posterior odds for "artificial." With no generative likelihood for it, the Bayes factor is undefined.

### 3 · Artificial compact objects and gravitational engineering

The fabrication routes are closed:
- **Kugelblitz.** Energy is cheap: a 10⁹ kg hole costs about 0.2 s of solar output. The hoop condition, however, requires delivering $Mc^2$ within about $r_s/c$. That means $P\gtrsim c^5/4G\approx9\times10^{51}$ W, independent of mass. Separately, pair production via the Schwinger effect alone dissipates the focused energy fast enough to block kugelblitz formation across radii from 10⁻²⁹ to 10⁸ m.
- **Seed growth.** Below about 10¹¹ kg, a hole's own Hawking output exceeds its Eddington luminosity, so it cannot be fed by accretion. Above that, its femtometre-scale cross-section needs nuclear densities to feed it.
- **What remains:** capturing natural PBHs, if they exist, or seeding neutron stars so they collapse into black holes. Both look the same as natural processes. Origin can only be argued from configuration and population statistics.

| Channel | Magnitude | Verdict |
|---|---|---|
| Hawking γ-rays, 10¹² kg | kT ≈ 10.6 MeV. ~10¹⁰ W is the **all-species total**; photon-only luminosity is 3.6×10⁸ W, so the γ-ray flux is ~3×10⁻²⁵ erg cm⁻² s⁻¹ at 10 pc | ~12 orders below Fermi-LAT-class sensitivity |
| Final-second burst (~10⁶ kg, TeV) | very-high-energy γ-ray arrays | detectable only within ~0.01–0.1 pc |
| Harvested Hawking power | starless, warm, compact IR source | best channel (below) |
| High-frequency GWs from a micro-BH binary | strain h ~ 10⁻³³ at 10 pc | undetectable |
| LISA | engineered stellar-mass binaries (Dyson 1963 "gravitational machines"): ḟ inconsistent with GR + tides + mass transfer, or non-GR phasing | viable after launch |
| LVK / next-gen ground detectors | black holes below the neutron-star maximum mass (TOV limit) with tidal deformability Λ ≈ 0, i.e. transmuted neutron stars (Takhistov, Fuller & Kusenko 2021) | artificial origin arguable only if their rate decouples from local dark-matter density |
| Lensing | micro-BH: negligible. Exotic matter: negative-mass or Ellis-wormhole light curves (bounds: Takahashi & Asada 2013) | tests exotic matter, not technology |

**Radius–temperature test**, the strongest compact-object discriminant. Take $T$ from the SED and luminosity from flux plus parallax, then compute $R_{\rm eff}=\sqrt{L/4\pi\sigma T^4}$.
- A 10¹⁷ W habitat radiating at 300 K has $R_{\rm eff}\approx4{,}200$ km.
- Brown dwarfs stay near one Jupiter radius even at ~250–285 K (WISE 0855−0714).
- Free-floating rocky bodies with only internal heat radiate at about 30–40 K.
- So a warm source with $R_{\rm eff}\ll R_{\rm Jup}$ matches no natural class.

The limit is sensitivity. At 10 pc such a source is about 0.2 µJy at 10 µm, which is JWST depth. All-sky surveys only reach it within about 0.1 pc.

Gravitational engineering within known physics is best framed as stellar-lens telecom: relay probes at a star's gravitational focus (Kerby & Wright 2021). We can test this locally by searching the Sun's focal regions on the side opposite nearby stars (Gillon 2014). Closed timelike or "closed-loop" geometries require violating the averaged null energy condition and have no known formation channel. Only phenomenological templates exist, such as gravitational-wave bursts from warp-bubble collapse (Clough, Dietrich & Khan 2024). This ranks last.

### 4 · Ancestral origin ("Solar Cradle")

Thermal scars fade on the Kelvin–Helmholtz time, about 3×10⁷ yr for the Sun, and waste heat stops the moment computation stops. Only composition, structure and dynamics persist:

| Scar | Persistence | Observable |
|---|---|---|
| Star lifting: mass removed to extend the star's life (Scoggins & Kipping 2023) | nuclear timescale | asteroseismic age inconsistent with the mass implied by isochrones |
| Engineered core mixing | Gyr | asteroseismic small separations δν₀₂, mixed-mode bumping |
| Surface pollution: fission products, Tc/Pm/actinides in a dwarf (Whitmire & Wright 1980) | isotope half-lives; stable species diluted by convective-zone mass | high-resolution spectroscopy; false positives are Ap/Bp and AGB s-process stars |
| Stellar-engine relocation | until disk heating erases it (~Gyr) | velocity offset from chemically tagged birth siblings |
| Planetary architecture: dismantled or moved planets, non-primordial co-orbitals | 10⁸–10¹⁰ yr | radial velocities, transits, astrometry |
| Abandoned swarm debris: metal-rich and ice-poor; large artifacts in stable orbits (Benford 2019) | dust fades ∝ t⁻¹; artifacts last Gyr | MIRI spectroscopy; polluted-white-dwarf composition once the star has evolved |

Locating the cradle is an epicenter inversion:
1. For each modified system, estimate a modification epoch $t_i$. Clocks include injected-isotope parent/daughter ratios, debris collisional age, and swarm completion fraction.
2. Back-integrate each star's Galactic orbit $\mathbf x_i(t)$.
3. Fit for the origin $\mathbf x_0$, epoch $t_0$ and expansion-front speed $v_f$:

$$t_i=t_0+\frac{|\mathbf x_i(t_i)-\mathbf x_0|}{v_f}+\varepsilon_i$$

The cradle is the system whose back-integrated track passes $\mathbf x_0$ at $t_0$ and that shows the oldest clocks and deepest cumulative modification. Differential rotation and chaotic orbital diffusion erase positional memory after roughly 10⁸–10⁹ yr. Older expansions therefore localize only to an annulus, not to a single star.

### 5 · Facilities

| Facility | Role |
|---|---|
| JWST (MIRI 5–28 µm) | Ξ follow-up, silicate veto, $R_{\rm eff}$ of starless sources |
| Roman | bulge time-domain photometry for transit and lensing anomalies |
| Gaia DR4 | parallaxes for $R_{\rm eff}$; epoch astrometry for accelerations and orbit back-integration |
| SPHEREx (0.75–5 µm) | all-sky spectra for hot radiators |
| PLATO | asteroseismic ages for the star-lifting test |
| PRIMA | far-IR coverage for cold radiators |
| LISA | engineered compact binaries |
| LVK, next-gen ground detectors | population of black holes below the neutron-star maximum mass |
| VLBI (EVN/LBA → SKA-VLBI, ngVLA) | milliarcsecond localization rejects RFI (first VLBI SETI: Rampadarath et al. 2012). ngEHT/BHEX horizon imaging is relevant only to SMBH-scale engineering, and GRMHD variability sets a high false-positive floor there |

Current status:
- Roman launched August 30, 2026 and is in a three-month commissioning phase, with first public images targeted for early 2027.
- Gaia DR4 is planned for 2 December 2026, covering the first 5.5 years of observations, and adds epoch data for astrometry, photometry and spectroscopy.
- PLATO is now set to launch in March 2027 on Ariane 6 (ESA's current target).
- PRIMA advanced to the next development phase in September 2026, targeting a 2033 launch for a five-year mission. It will be the first major full-scale far-infrared observatory since Herschel.
- LISA is due to launch in mid-2035.

### 6 · False-positive mitigation (ordered gate)

1. Preregister statistics, thresholds and trial factors. Run blind injection–recovery tests.
2. Require provenance from at least two instruments with uncorrelated systematics. For radio, check topocentric drift and use on/off cadences.
3. Apply contamination vetoes. Use Gaia RUWE and adaptive-optics imaging to catch blends. Check for radio or X-ray counterparts that reveal background AGN, which is how the Hephaistos M-dwarf Dyson candidates failed (Suazo et al. 2024; Ren, Garrett & Siemion 2024).
4. Fit the full $\mathcal M_0$ and allow for natural classes nobody has catalogued yet. They keep arriving: minute-to-hour-period coherent radio transients have appeared since 2022, and several have been traced to white-dwarf–M-dwarf binaries.
5. Run the admissibility and design-feature tests, with independent re-detection.
6. Report on the Rio 2.0 scale (Forgan et al. 2019), using the verification framework applied to the BLC1 signal (Sheikh et al. 2021).

Base rate: every anomaly so far has resolved naturally.
- LGM-1 turned out to be a pulsar.
- KIC 8462852's dips were chromatic, so dust (Boyajian et al. 2018).
- BLC1 was RFI.
- ʻOumuamua's acceleration was H₂ outgassing (Bergner & Seligman 2023).

## Justification trace

- **"Informational density" candidates.**
  - Raw $K(x)$: rejected, because it is uncomputable and dominated by noise.
  - Shannon entropy of the power spectrum: demoted, because scale-free natural spectra score like coded signals.
  - Ξ: kept, because the second law guarantees it and archival data can measure it.
  - Effective complexity, κ and GF(2) rank: kept as the only discriminants with no known natural generator.
- **Compact objects.** Hawking-profile anomalies were rejected because of the no-hair theorem. High-frequency GWs were rejected because the strain is ~10⁻³³. Kept: the radius–temperature test and LVK population statistics.
- **Pareto gate.** An archival Ξ search (Gaia DR4 plus WISE/SPHEREx), followed by JWST and radio vetoes, improves both sensitivity and false-positive control at near-zero marginal cost. No axis degrades.
- **Confidence.**
  - High on the entropy and Landauer algebra, and on the mass-independent kugelblitz power scaling (order-unity GR factors remain open).
  - ±1 dex on Hawking powers and lifetimes below ~10¹⁰ kg, because the count of emitted particle species changes with temperature.
  - Low on the cradle inversion, which depends on unknown expansion dynamics.

## Risks & Limits

- **Load-bearing assumptions:** known physics, irreversible computation at scale, and thermal waste disposal. Two things break Ξ:
  - Non-thermal disposal (the ν term in AGENT: beamed, neutrino or kinetic losses).
  - Deferred computation, the aestivation hypothesis (Sandberg, Armstrong & Ćirković 2017; contested by Bennett, Brin & Hanson 2019).
- **Reversible computing** evades Landauer except for I/O and error correction. $\dot N_{\rm bit}$ caps erasure, not computation.
- **Cold radiators** below ~60 K peak beyond 50 µm. They stay unconstrained until PRIMA flies.
- **Incompleteness of $\mathcal M_0$** is the dominant false-positive risk, and every complexity test inherits it.
- **Logical depth** (Bennett 1988) is the formally correct measure of "evidence of computation," but it has no robust estimator.
- **Re-evaluation triggers:**
  - Gaia DR4 release.
  - Roman's first bulge season.
  - Any signal with a GF(2) rank deficit or high-κ periodicity.
  - Any black hole below the neutron-star maximum mass with Λ ≈ 0 that falls off the dark-matter-density trend.
  - Changes to the LISA schedule.

---

*Corrected edition, 2026-10-20. Corrections applied after adversarial review: (1) calculator reference now names the companion calculator published with this document instead of a dangling "below"; (2) the §3 Hawking row now separates the all-species total (~10¹⁰ W) from the photon-only luminosity (3.6×10⁸ W) and the γ-ray flux is corrected to ~3×10⁻²⁵ erg cm⁻² s⁻¹ at 10 pc; (3) the Hawking lifetime normalization is qualified as all-species emission (photon-only lifetime ~3.3×10¹¹ yr); (4) PLATO launch target updated to March 2027 (ESA).*
