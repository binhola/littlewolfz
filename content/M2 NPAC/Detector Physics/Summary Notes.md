---
draft: false
---
### Energy loss of particles in matter

**Key concept:** Charged particles lose energy primarily through **ionization** and **excitation** when they are **MIP**. Heavier particles or those prone to radiation loss (bremsstralung) behave differently.

**Key equations:**
- Energy loss for a MIP: $-\dfrac{dE}{dx} \sim 1-2 \, \text{MeV g}^{-1} \text{cm}^{-2}$ 
- To find energy loss in a material, multiply its density and length
- Total loss:
$$
\Delta E = (dE/dx) \times \Delta x
$$
- Why muons penetrate but alphas and electrons dont?
	- **Alpha**: much heavier, charge (2e). They are non-relativistic at the same momentum and have higher ionization density, stopping quickly.
	- **Electrons**: light, so loss energy via bresstralung in dense materials, stopping quickly.
### Particle identitfication
Different subdetectors are used to measure a particle's momentum and identify its type.
- **Momentum**: Magnetic spectrometer (Tracking detectors inside a magnetic field). The curvature of the track gives the momentum
- **PID**: 
	- $e^{\pm}$ : EM Calorimeter
	- $\mu$ : Muon system (placed after all others, as muon penetrate deeply)
	- $K,\, \pi$ : Cherenkov detectors + hadronic calorimeters

**Key challenges:** Electron and muon momentum resolution
- **Problem**: electron suffers from bremsstralung, worsen their momentum resolution.
- **Mitigation:** 
	- *Software*: combine tracking information with energy deposit from EM Cal to correct for radiated energy.
	- *Design*: Minimize the material budget ($x/X_0$) in the tracking volume, where $X_0$ is the radiation length.

### Scintillators
**Key concept:** Materials that emit light when traversed by ionizing radiation.

| Properties        | Organic                   | Inorganic                                                     |
| ----------------- | ------------------------- | ----------------------------------------------------------- |
| Speed             | fast                      |                                                               |
| Light output      | lower                     |                                                               |
| Linearity         | worse (quenching effects)                                                                 |
| Cost              | cheap                     |                                                               |
| Working principle | molecular excit band-gap excitation in crystals, often with activator sites  with  tals,  |

### Gaseous Detectors
**Key concepts**: Ionizing radiation create $e^- e^+$ pairs in a gas. An electric field drifts the electrons towards the region of high field (the anode wire) to create an avalanche for signal amplication.

**Key equations:**
- Electric field in cylindrical geometry:
$$
E(r) = \dfrac{U}{\ln (R_t/R_w)} \dfrac{1}{r}
$$
where $U$ : applied voltage, $R_t$ : Tube radius, $R_w$ : wire radius
- **Avalanche condition**: $E(r) > 30 \rm \, kV/cm$ 
- **Polarity**: the central wire must be positive (anode) to attract $e^-$ and cause the avalanche near the wire for a fast, measurable signal.
- **Gas type**:
	- Noble gas (e.g. Ar): primary ionization medium.
	- Quenching gas (e.g. CH4): Absorbs UV photons from the avalanche to prevent discharge.

### Semi conductors
**Key concept:** Solid-state devices that act as solid ionization chambers. Superior energy and spatial resolution.

**Working principle:** A reversed bias *p-n junction* creates a *depletion zone*. ionizing radiation creates electron-hole pairs that are collected, generating a signal.

**Advantages:** 
- **Energy resolution:** much higher number of charge carries per MeV reduces statistical fluctuation. Govern by the **Fano** factor ($F << 1$) 
- **Spatial resolution:** can be fabricated with fine segmentation (strips, pixel)

**Doping**: 
- **n-type:** adding P (group $V$) provides an extra electron 
- **p-type**: adding Be (group $III$) provides an extra hole
### Energy resolution
The statistical limit of energy resolution is determined by the fluctuation in the number of signal carriers (electron or positron).

**Equations**:
- The relative statistical fluctuation is given by: $$ \dfrac{\sigma_Q}{Q} = \dfrac{\sqrt{F \cdot N}}{N} = \sqrt{\dfrac{F}{N}}$$
	where $N$ is the average number of carriers, $F$ is **Fano** factor (for semiconductors, $F < 1$)
- Steps:
	1. Calculate the deposited energy: $$ \Delta E = \dfrac{dE}{dx} \times \Delta x $$
	2. Calculate the average number of signal carriers: 
	
	$$ 
	\begin{aligned}
	&\text{Semiconductor:} &N &= \Delta E \times (\text{e-h pairs/MeV}) \times (\text{Collection efficiency}) \\
	&\text{Scintillator:} &N &= \Delta E \times (\text{photons/MeV}) \times (\text{Light collection eff.}) \times (\text{Quantum eff.})
	\end{aligned} 
	$$
	
	1. Relative resolution

### Electromagnetic calorimetry
The depth needed to contain an EM shower scales logarithmically with energy

**Equations**:
- **Critical energy ($E_c$)**: the energy at which ionization losses equal radiation losses.
	- **Shower depth**: The depth contains $95-98 \%$ of a shower is approximately $$t = X_0 \times \ln (E_0 / E_c) / \ln 2$$
	where $t$ is the depth in $X_0$ and $E_0$ is incident energy
- In practice a safe factor (e.g $2 \times$) applied to ensure full containment despite shower fluctuations

### Cherenkov
Particle emits Cherenkov radiation if their velocity $v$ exceeds the speed of light $c/n$ in the medium, i.e. $\beta > 1/n$ 

**Equation:**
- Cherenkov angle: 
$$
\cos \theta_n = \dfrac{1}{n \beta}
$$
- Momentum and velocity
$$
p = \gamma m_0 v
$$
For the same momentum, heavier particles have lower $\beta$ 
- PID: Choose a radiator with a refractive index $n$ so that ligher particle (e.g. $\pi$) is above threshold ($\beta_\pi > 1/n$) and heavier like $K$ is below.

### Photon attenuation and Compton scattering
Photon interacts via photoelectric effect, compton scattering and pair production. The dominant process depends on energy and material $Z$.

**Equations:**
- **Attenuation**: $I = I_0 e^{-\mu x}$
	- $\mu$ : linear attenuation coefficient
	- compound: $\mu = \sum_i \omega_i \mu_i$ 
- **Compton scattering:** 
	- Wavelength shift: $$ \lambda' - \lambda = \dfrac{h}{m_e c} (1 -\cos \theta) $$
	- Energy of scattered photon: $$E' = \dfrac{hc}{\lambda'}$$
	- Energy of recoil electron: $$E_e = E - E'$$
### Collider
**Luminosity:** number of particles per unit area per unit time
$$
L = \dfrac{f I_b^2}{4\pi S_x S_y}
$$
where
- $f$ : the revolution frequency (number of bunch cross per second)
- $I_b$ : number of particles per bunch
- $S_x$ or $S_y$ : RMS width of beam in $x$-dir or $y$-dir

**Number of events:**
$$
N = L \times \sigma
$$

**Rapidity:**
$$
y = \dfrac{1}{2} \ln \left( \dfrac{E + p_z}{E - p_z}\right) \approx - \ln \tan \dfrac{\theta}{2}
$$
where $\theta$ is polar angle from beam axis.

### Tranverse momentum resolution
$$
\dfrac{\sigma(p_T)}{p_T} = \dfrac{\sigma_x p_T}{0.3 B L^2} \sqrt{\dfrac{720}{N + 4}}
$$
where $\sigma_x = \dfrac{\rm pitch}{\sqrt{12}}$ , $N$ is number of measurement points and $L$ is the track length.
### Radiation length
Bremsstralung for electrons
$$
E = E_0 e^{-x / X_0}
$$
where $X_0$ is the radiation length.
$$
\dfrac{dE}{dx} = \dfrac{E}{X_0}
$$


