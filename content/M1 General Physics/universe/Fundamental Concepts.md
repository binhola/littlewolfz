## Fundamental concepts of radiation
### Flux and luminosity 
Radiant flux is the light energy crossing a perpendicular area per unit time
$$
dE = F dA dt
$$
For a spherically symmetric steady source with luminosity $L$ (total emitted energy per unit time). The flux drops off can be measured as:

$$
F(r) = \dfrac{L}{4\pi r^2}
$$
$L$ is total luminosity emitted at all wavelength, so $F$ will be integrated over all wavelengths:

$$
F = \int F_\nu d\nu
$$
Therefore,

$$
dE = F_\nu dA dt d\nu
$$
The unit of $F_\nu$ is energy per area per time per frequency bin, so $\rm W \, m^{-2} \, Hz^{-1}$. 
- Jansky unit: $\rm 1 \, Jy = 10^{-26} W \, m^{-2} \, Hz^{-1}$
- $F_\nu$ called "flux density"
### Solid angle
The area $dS$ is a patch of the surface is
$$
dS = r^2sin\theta \, d\theta \, d\phi \equiv r^2 d\Omega
$$
where $d\Omega$ is the solid angle subtended by the area $dS$ at the center of the sphere.  
- Unit: steradian sr
- $4\pi \rm \, sr$ cover the whole sphere 
### Specific intensity
The intensity measure the total energy passing through an area $dA$ normal to light ray. Then, consider all the light rays lie within a small solid angle $d\Omega$:
$$
dE = I_\nu \, dA\,dt\,d\nu\,d\Omega
$$
where $I_\nu$ is the specific intensity/brightness. Unit is $\rm W\,m^{-2}\,Hz^{-1}\,sr^{-1}$.

Specific intensity/brightness is constant if there is no absorption or emission.

$$
\dfrac{dI_\nu}{ds} = 0
$$
### Cross section
**Cross section** is the *effective area* $\sigma$ for reaction to occur if we fire a point-like projectile to an area $A$: 

$$
\rm \text{Probability of hitting target} = \dfrac{\sigma}{A}
$$
Consider also the thickness $x$ of a volume with area $A$

$$
N = nAx
$$
where
- $N$ is the total number of particle inside the volume
- $n$ is the number density

The number of available effective area is the number of particle

$$
N \times \sigma = nAx\sigma
$$

The probability that the reaction will take place

$$
\dfrac{nAx\sigma}{A} = nx\sigma = n_c \sigma
$$

where $n_c = nx$ is the column density (density integrated over length of column).
## Radiation processes
Intensity along the beam changes due absorption or emission. In order to formulate a radiative transfer equation, we need to consider radiation traveling through a medium. 
#### Emission
The medium is also emitting radiation, we define $j_\nu$ as:
$$
dE = j_\nu \, dV \, d\Omega \, dt \, d\nu
$$
The increase in intensity can be define as:

$$
dI = j_\nu ds
$$
#### Absorption
When the radiation travels through a gas which absorbs or scatters radiation, the energy of the beam can be reduced. *Note:* Emission process only depends on the nature of the medium, while the absorption/scattering process depends also on the radiation intensity. 

Consider a light rays passing through a cylinder of absorbers with number density $n$. Each absorber has cross-section $\sigma$, cylinder length $L$ and area $A$. 

1. Assume that absorbers do not shadow each other, fractional blocked area:

$$
\sigma_{\rm total} = nLA\sigma
$$

So the **optical depth** or fraction of blocked light:

$$
\tau = f_{\rm abs} = \dfrac{\sigma_{\rm total}}{A} = nL\sigma
$$

- If $\tau < 1 \rightarrow$ optically thin
- If $\tau > 1 \rightarrow$ optically thick
- With $\tau = 1$, we can define the **mean free path** (a typical distance travelled before getting absorbed) of a photon: $L = \dfrac{1}{n\sigma}$

2. If the absorbers shadow each other, imagine the optically thick layer as a series of optically thin layers. The change of intensity of each layer is the intensity times the depth of that layer:

$$
dI = -Id\tau
$$
Cross-section is also a function of wavelength, so we can rewrite the equation as:

$$
\dfrac{dI_\nu}{I_\nu} = -d\tau_\nu = n\sigma_\nu ds
$$
Define quantities:
- $\alpha_\nu \equiv n \sigma_\nu$ is the *absorption coefficient* (unit: m$^{-1}$)
- $\kappa_\nu \equiv \dfrac{\alpha_\nu}{\rho}$ is the *opacity* (unit: $\rm m^2.kg^{-1}$) i.e the cross-section of 1 kg of gas

To describe a pure absorption, the decrease of intensity can be represented as:

$$
dI_\nu = \alpha_\nu I_\nu ds
$$
#### Radiative transfer equation
With both emission and absorption processes, we can write the equation as:

$$
\dfrac{dI_\nu}{ds} = -\alpha_\nu I_\nu + j_\nu
$$

We can rewrite using the *optical depth* rather than distance:

$$
\dfrac{dI_\nu}{d\tau} = -I_\nu + \dfrac{j_\nu}{\alpha_\nu} = -I_\nu + S_\nu
$$
where $S_\nu$ is the *source function*. 

## Blackbody radiation
A blackbody is an object that absorbs all the incoming radiation and emits a continuous spectrum with some energy at all wavelengths. 

$$
B_\lambda(T) = \dfrac{2hc^2/\lambda^5}{e^{hc/\lambda kT} - 1}
$$

or 

$$
B_\nu(T) = \dfrac{2h\nu^3/c^2}{e^{h\nu/kT}-1}
$$
Unit of $B_\nu$ : $\rm W\, m^{-2}\, Hz^{-1}\,sr^{-1}$ 
Unit of $B_\lambda$ : $\rm W\, m^{-2}\, nm^{-1}\,sr^{-1}$ 

If we consider a star as a blackbody radiation: $I_\lambda = B_\lambda$.
### Wien displacement's law

Differential $\dfrac{\partial B_\lambda(T)}{\partial \lambda} = 0$ to find $\lambda_{\rm peak}$ as the function of $T$:

$$
\lambda_{\rm peak} = \dfrac{2.88 \times 10^{-3}}{T} \, \rm m
$$

So the hotter $T$, the smaller $\lambda_{\rm peak}$.

### Stefan-Boltzmann equation
The luminosity of blackbody of area $A$ and temperature $T$ is given by the Stefan-Boltzmann equation:

$$
L = A\sigma T^4
$$
where $\sigma = 5.67 \times 10^{-8} \, \rm W \, m^{-2} \, K^{-4}$.

For a spherical star of radius $R$ where $A = 4\pi R^2$, the luminosity is:

$$
L = 4\pi R^2 \sigma T^4
$$

### Effective temperature 
Since stars are not a perfect blackbodies, we define the effective temperature of a star as the temperature of a blackbody that have the same flux as the considered star:

$$
F_{\rm surf} = \sigma T_e^4
$$

For the Sun:

$$
L_\odot = 4 \pi R_\odot^2 \sigma T_e^4
$$

We found out that $T_e = 5770 \, \rm K$.

### Radiative transfer equation

If we consider the gas medium is in thermal equilibrium with the radiation, we can take the source function $S_\nu =\dfrac{j_\nu}{\alpha_\nu}$ as the Planck function:

$$
\dfrac{dI_\nu}{d\tau_\nu} = I_\nu - B_\nu(T)
$$

Integrate this function:

$$
I_\nu (\tau_\nu) = I_0e^{-\tau_\nu} + B_\nu (1-e^{-\tau_\nu})
$$

where $I_0$ is the intensity at $\tau_\nu = 0$ and if $\tau_\nu >> 1$ then $I_\nu \simeq B_\nu$

## Atomic processes

Radiation can be emitted or absorbed when electrons make transitions between different states. There are 3 main categories:
- **Bound-bound** (excitation and de-excitation): $e^{-}$ moves between two bound states (orbitals) in an atom or ion, and a photon can be emitted or absorbed.

$$
|E_{\rm high} - E_{\rm low}| = h \nu
$$

Energy level are characterised by the principal quantum number $n$:

$$
E_n = - \dfrac{R}{n^2}
$$

where $R = 13.6 \, \rm eV$. The $n$-th energy level has $2n^2$ degenerate quantum states with same $E$.
- **Bound-free:**
	- Bound $\rightarrow$ unbound: ionisation
	- unbound $\rightarrow$ bound: recombination
- **Free-free**: free $e^{-}$ gains/loses energy in the vicinity of an ion by exchange photon (*bremsstrahlung* or 'braking radiation')

