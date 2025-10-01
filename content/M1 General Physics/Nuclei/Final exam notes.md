
## Radioactivities and decays of nuclei

### Fermi Golden rule
- Described by the transformation from initial state $\psi_i$ to final state $\psi_f$ through one of these interactions: electromagnetic, strong or weak
$$
\langle \psi_f | V_{int} |\psi_i \rangle
$$
From this we can compute decay period $\lambda$ or cross section $\sigma$.

### Threshold energy
- Define a spontaneous process
$$
Q = \sum_i m_i c^2 - \sum_f m_f c^2 \quad \text{where} \quad 
\begin{cases} 
& Q > 0 \rightarrow \text{spontaneous} \\
& Q < 0 \rightarrow \text{need to provide Energy for reaction occurrence}
\end{cases}
$$
#### Electromagnetic interaction decays
$$
X^* \rightarrow X + \gamma
$$
where 
$$
E = h\nu = E_f - E_i
$$
We have
$$
\begin{aligned}
E_f - E_i + m_{X^*}c^2 &= m_{X}c^2 + T_X + E_\gamma \\
\vec{p_X} &= -\vec{p_\gamma} \\
T &= \dfrac{p^2}{2m}
\end{aligned}
$$
#### Weak interaction decays
An important relation to remember:
$$
m_X c^2 = N m_n c^2 + Z m_p c^2 - B
$$
There are some typical types of decays: $\beta^+$, $\beta^-$, electron capture.

Maybe, we need to use this relation:
$$
M_{at}c^2 = m_Xc^2 + Zm_e c^2 - B_e
$$
##### $\beta^+$
$$
^A_ZX^N \rightarrow ^A_{Z+1}Y^{N-1} + e^- + \overline{\nu_e}
$$
##### $\beta^-$
$$
^A_ZX^N \rightarrow ^A_{Z-1}Y^{N+1} + e^+ + \nu_e
$$
##### Electron capture
$$
^A_ZX^N + e^- \rightarrow ^A_{Z-1}Y^{N+1} + \nu_e
$$
*Notes*: 
1. If we use $Q$ and atomic mass relation, we can have the relation between $\beta^+$ and electron capture as:
$$
Q_{\beta^+} = Q_{EC} - 2m_e c^2
$$
2. Applications:
	1. PET Scan: 
		- $\beta^+$ emitter: $^{11}_5C \rightarrow ^{11}_6B + e^{+} + \nu_e$ 
		- Positron annihilates with the electron in body: $e^+ + e^- \rightarrow \gamma + \gamma$ . 
		- The energy of the photon is 0.511 MeV in opposite direction with each other.
	2. $^{40}_{19}K$ in our body has half life time of $13 \times 10^{19}$ yrs.

#### Strong interaction decays
From Yukawa theory, we have
$$
\mu^{-1} = \dfrac{\hbar c}{mc^2} = \text{Range}
$$
So the time of propagate can be approximate as
$$
\dfrac{\mu^{-1}}{c} = \dfrac{\hbar}{mc^2} =\dfrac{\hbar c}{mc^2} \dfrac{1}{c}
$$
Compute for pion with $mc^2 = 140$ Mev, we have the typical time scale of strong interaction is very short at $10^{-23}$ s.

##### $\alpha$ decay
$$
X \rightarrow Y + \alpha
$$
We have
$$
Q = m_X c^2 - m_Y c^2 - m_\alpha c^2
$$
From relativistic kinematics, we have
$$
\begin{aligned}
m_X c^2 &= m_Y c^2 + T_Y + m_\alpha c^2 + T_\alpha \\
0 &= \vec{p_Y} + \vec{p_\alpha}
\end{aligned}
$$
So, we have
$$
Q = T_Y + T_\alpha = T_\alpha (1 + \dfrac{m_\alpha}{m_Y})
$$
- Only heavy nuclei are $\alpha$ emitter ($A > 150$) , so $m_Y >> m_\alpha$, then
$$
T_\alpha \approx Q \quad, \quad T_y \approx 0
$$
### Decay probabilities

#### Production rate
$$
dN = -\lambda N dt + n_idt
$$
where 
- $\lambda$ is the decay probability of a given nucleus per second ($s^{-1}$)
- $n_i$ is the production rate

#### Decay rate
$$
dN = -\lambda N dt
$$
#### Half-life time
$$
T_{1/2} = \dfrac{\ln(2)}{\lambda}
$$
#### Activity
The measure of rate of decay of a substance or a system
$$
A(t) = \lambda N(t)
$$
For a normal human body, the typical $A(\text{human}) = 10^4\,\text{Bq}$
- 1 **Becquerel (Bq)** is the unit of **radioactive activity**: 1 Bq = 1 decay per second

### Liquid drop model
$$
B = \underset{\text{volume}}{a_V A} - \underset{\text{surface}}{a_S A^{2/3}} - \underset{\text{coulomb}}{a_C \dfrac{Z^2}{A^{1/3}}} - \underset{\text{N-Z balance}}{a_A \dfrac{(N-Z)^2}{A}} + \underset{\text{parity}}{\delta}
$$
where
- $a_V = 16$ MeV
- $a_S = 17$ MeV
- $a_C = 0.7$ MeV 
- $a_A = 23$ MeV
- For pairing effects
$$ \delta = 
\begin{cases}
& \dfrac{12}{\sqrt{A}} \quad &\text{even-even} \\ 
& 0 \quad &\text{even-odd} \\
& - \dfrac{12}{\sqrt{A}} \quad &\text{odd-odd}
\end{cases}
$$
- Assumption: for isobaric weak decay, $A = \text{const}$.
- Stable nuclei can be found by
$$
\dfrac{\partial B(A,Z)}{\partial Z} = 0
$$
We found that
$$
Z = \dfrac{A}{\dfrac{a_C}{2 a_A} A^{2/3} + 2} \sim \dfrac{A}{0.015 A^{2/3} + 2}
$$
- For fission to happens, the nucleus has to be deformed: the Coulomb repulsion have to be larger than surface effect.
$$
a \dfrac{Z^2}{A^{1/3}} > b A^{2/3} \quad \Rightarrow \quad \text{fissility}:\dfrac{Z^2}{A} > 30
$$
	Only happens for heavy nuclei like $_{92}U$ or $Th$.
- For fusion or fission to happens $Q > 0$:
$$
\langle B/A\rangle_{\text{output}} > \langle B/A \rangle_{\text{input}}
$$
	The most stable nuclei is around $Fe$

## Probing nuclei
### Kinematics
$$
\dfrac{dp}{dt} = \gamma m \dfrac{v^2}{R} = qvB \quad \Rightarrow \quad BR = \dfrac{\gamma m v}{q} = \dfrac{p}{q}
$$
### Conservation laws
For a process:
$$
1+ 2 \rightarrow 3+ 4
$$
- Energy conservation:
$$
E_1 + E_2 = E_3 + E_4
$$
- Momentum conservation:
$$
\vec{p}_1 + \vec{p}_2 = \vec{p}_3 + \vec{p}_4
$$
- Charge conservation:
$$
q_1 + q_2 = q_3 + q_4
$$
- Spin
$$
\vec{J_1} +\vec{J_2} + \vec{L_i} = \vec{J_3} + \vec{J_4} + \vec{L_f} 
$$
**Not for weak interaction**
- Parity: strong and EM
$$
\pi_1 \pi_2 (-1)^{L_i} = \pi_3 \pi_4 (-1)^{L_f}
$$
- Isospin: strong
$$
\vec{T_1} + \vec{T_2} = \vec{T_3} + \vec{T_4}
$$
- Isospin projection: strong and EM
$$
T_{31} + T_{32} = T_{33} + T_{34}
$$
### Total kinetic energy
$$
T_{tot} = \dfrac{1}{2} m_1 v_1^2 + \dfrac{1}{2} m_2 v_2^2
$$
Define $\vec{v} = \vec{v_2} - \vec{v_1}$ and $M = m_1 + m_2$

$$
\vec{v_1} = \vec{V} - \dfrac{m_2}{M} \vec{v}
$$
$$
\vec{v_2} = \vec{V} - \dfrac{m_1}{M} \vec{v}
$$
Then
$$
T_{tot} = \dfrac{1}{2} M \vec{V}^2 + \dfrac{1}{2} \mu \vec{v}^2
$$
where $\mu = \dfrac{m_1 m_2}{M}$

### Interactions in different frame
1. Centre of mass frame
2. Fixed target frame

- **Invariant**: $$I = \Big(\sum_i E_i\Big)^2 - \Big(\sum_i p_i c\Big)^2$$
- In this case $Q < 0$, so we need to determine the minimum kinetic energy to produce the particle of interest.
#### Center of mass (CMS) frame
$$I = \Big(\sum_i E_i\Big)^2 - \Big(\sum_i p_i c\Big)^2 = (E_1 + E_2)^2 = \Big(2T_s + \sum_i m_i c^2\Big)^2 = \Big(\sum_f p_f c \Big)^2$$
So
$$
T_s = -\dfrac{Q}{2}
$$
#### Fixed target frame
$$
I = \Big(\sum_i E_i\Big)^2 - \Big(\sum_i p_i c\Big)^2 = (m_1c^2 + T_s + m_2c^2)^2 - p_1^2 c^2
$$
And
$$
p_1^2 c^2 = E_1^2 - m_1^2 c^4 = (T_s + m_1 c^2)^2 - m_1^2 c^4 = T_s^2 + 2 m_1 c^2 T_s
$$
So,
$$
T_s = -\dfrac{Q}{2} \dfrac{\sum_{if} m_{if}c^2}{m_{\rm target} c^2} \geq -Q
$$
##### LHC case example
$$
T_1 = T_2 = 7 \rm \, TeV
$$
For CMS case, we have $Q = -14 \, \rm TeV$, because we use proton with energy $\sim 1 \rm \, GeV$, so we can produce the particle of $14 \, \rm TeV$ energy.

For fixed target, to produce the particle of same energy in CMS frame, we would need $\sim 10^5$ TeV.

### Cross section and reaction
Consider a beam of intensity $\phi$ particle per second, shot the target of thickness $e$ and density of $N$ nuclei per volume.

We have the number of event per second to be
$$
n_o = \phi N e \sigma
$$
where $\sigma$ is the cross section
- $\dfrac{n_o}{\phi}$ is the rate of nuclei in the beam interact with target
- $N = \dfrac{\rho}{A}N_A \sim 10^{21} \, \rm cm^{-3}$ 
- Simple contact model of $\sigma$:
$$
\sigma \sim \pi (R_1 + R_2)^2
$$
where $R_1$ is the incident radius and $R_2$ is the target radius
- $\sigma \sim 10^{-28} \, \rm m^2 = 1b$ for nuclei.
##### Solid angle case
$$
dn_o = \phi (Ne) \dfrac{d\sigma}{d{\Omega}} d\Omega
$$
We have
$$dr = \dfrac{S}{d^2}$$ where $S$ is the surface of detector and $d$ is the distance from target to detector.

We have
$$
\sigma = 2\pi \int \dfrac{d \sigma}{dr} \sin \theta d\theta
$$

We compute $n_o$
$$
n_o = \int dn_o 
$$
### Multipolarities
- We determine the multipolarities as $E$ (electric) or $M$ (magnetic) based on *parity*
- Type based on $L = \Delta J$

For example:
$$
\dfrac{7}{2}^+ \rightarrow \dfrac{3}{2}^+ + \gamma
$$
So,
$$
|7/2 - 3/2|\leq L \leq |7/2 + 3/2| \quad \Rightarrow \quad L = 2, 3, 4, 5
$$
And the parity
$$
(+1) = (+1) \pi_\gamma
$$
So $\pi_\gamma = +1$
For $L = 2$, the multipolarity should be $E_2$ so that $\pi_\gamma = (-1)^L$.
For $L = 3$, the multipolarity should be $M_3$ so that $\pi_\gamma = (-1)^{L+1}$.

After all we will have the probabilities as this order
$$
E_2 > M_3 > B_4 > M_5
$$
### Total angular momentum and parity
#### even-even nucleus
- At ground state
$$
J = 0^+
$$
- First excitation state
$$
J = 2^+
$$

### 

Mol 
$$
n = \dfrac{N}{N_A} 
$$
Mass
$$
m = n \times A
$$
so
Total number of nuclei
$$
N = \dfrac{m}{A} N_A 
$$
