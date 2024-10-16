---
tags:
  - physics
  - nuclei
---

Dimensionless quantities are designed to perform the universal study and comparison between different system. 

In the Nuclei course, we do dimensionless analysis of 4 quantities: coupling constant $\alpha$, spin-orbit parameter $\eta$, action A and quantality $\Lambda$. Each dimensionless quantity has different meaning in nuclei:
- *Coupling constant $\alpha$* characterises the four fundamental forces and displays how important they are in nuclei. The notable conclusion we will see after the analysis is that *strong force dominates in the nuclei over the three others*.
- *Spin-orbit parameter $\eta$* characterises the *spin-orbit effect* (coupling of sping and orbital angular momentum) that can impact the shell structure by adding a term to potential $V_{LS}$. One of important conclusion is that by evaluating $V_{LS}$ with the help of $\eta$, we can see that it is negligible in atom but significant in nuclei. 
- *Action* A shows if the quantum effects is important in the system, as the action (a scalar quantity describes the balance between kinetic and potential energy) gets close to $\hbar$ due to Heisenberg relation. 
- *Quantality $\Lambda$* is similar to *Action* A as it determines the state of matter if it is [[State of matter|quantum Liquid]] or not
## Three quantities 
Whenever we want to understand the behavior of a many-body system, we resolve to its equation of motion, in this case, the *Schrodinger equation*. Then, we need the information on the interaction of many-body system that we are dealing with including:
- $V_0'$ : Potential energy - typical magnitude of interaction
- $r_0$ : typical range of interaction
- $m_N$ : mass of constituents
## Coupling constant $\alpha$
Coupling constant characterises the magnitude of interaction in their typical range. This quantity only depends on the interaction itself, not the constituents.

$$ \alpha = \dfrac{V_0'r_0}{\hbar c} $$
#### Exercise
Calculate the coupling constant of the 4 interactions in the case of two protons located at 1 fm from each other.

**Convention:** 
- $\hbar c = 197 \text{ MeV.fm}$
- $1 \text{ MeV.fm} = 1.6 \times 10^{-28} \text{ N.m}$
- $m_p c^2 = 938.28 \text{ MeV}$ 
1. **Electromagnetism:** we can use the electrostatic potential given by $V_0' = \dfrac{e^2}{4\pi \epsilon_0 r_0}$. Therefore, the coupling constant is given by:
$$
\alpha_{EM} = \dfrac{V_0'r_0}{\hbar c} = \dfrac{e^2}{4\pi \epsilon_0 \hbar c} = \dfrac{1.44 \text{ MeV.fm}}{197  \text{ MeV.fm}} = \dfrac{1}{137} \approx 10^{-2}
$$
2. **Strong**: We use the experimental result of a nucleon-nucleon interaction which is given by this graph:

![Strong](M1%20General%20Physics/Nuclei/images/nucleon-nucleon-potential.png)

We can choose $V_0' = 100 \text{ MeV}$ at $r_0 = 1 \text{ fm}$, thus:

$$
\alpha_{s} = \dfrac{100 \text{ MeV.fm}}{200 \text{ MeV.fm}} \approx 1
$$
3. **Gravitation**: The gravitational potential is defined as $V_0' = \dfrac{GMm}{r_0}$, thus:

$$
\alpha_g = \dfrac{Gm_p^2}{\hbar c} \approx 10^{-39}
$$

4. **Weak**: The weak interaction is mediated by the $W^\pm$ and $Z$ bosons, which have masses of $m_W = 80 \, \text{GeV}$ and $m_Z = 90 \, \text{GeV}$, respectively. According to the Heisenberg uncertainty principle, we have:

$$
m_Zc^2 t_w \simeq \hbar
$$

where $t_w$ is the characteristic time over which weak interaction between two protons occurs.
Thus: 

$$
r_w = t_w \times c \simeq \dfrac{\hbar c}{m_Z c^2} \simeq 10^{-18} \text{ m}
$$
Therefore, the coupling constant of weak interaction for two protons at 1 fm distance will be $\approx 0$

| Force            | Bosons          | Interaction Magnitude | Typical Range         |
| ---------------- | --------------- | --------------------- | --------------------- |
| Strong           | gluon $g$       | ~ 1                   | 1 $fm$ = $10^{-15}$ m |
| Electromagnetism | photon $\gamma$ | ~ $10^{-2}$           | $\infty$              |
| Weak             | $Z$, $W^{\pm}$  | ~ $10^{-6}$           | $10^{-18}$ m          |
| Gravity          | graviton ?      | ~ $10^{-39}$          | $\infty$              |
## Spin-orbit parameter $\eta$

Mass of nuclei over the depth of potential well
$$
\eta = \dfrac{m_Nc^2}{V_0'}
$$
## Action A & quantality $\Lambda$ 
**Action A** defines the significance of quantum effect in a system:

$$
A = \dfrac{r_0 \sqrt{m_N V_0'}}{\hbar} = \alpha \sqrt{\eta}
$$
If $A \gg 1$, the action $\gg \hbar$, we can treat the system classically. If $A \gtrsim 1$, the quantum effect becomes significant. 

**Quantality $\Lambda$** carries the similar information to action $A$. However, we will deduce it using the ratio of zero point kinetic energy $T_0$ and magnitude of interaction $V_0'$. In the zero point kinetic energy case, the system is at rest, but because of the non-negligible quantum effect, we have to consider $\Delta p = \dfrac{\hbar}{\Delta x} = \dfrac{\hbar}{r_0}$ and $T_0 \simeq \dfrac{\Delta p^2}{2m_N} = \dfrac{\hbar^2}{2m_Nr_0^2}$ . Thus:

$$
\Lambda = \dfrac{T_0}{V_0'} \simeq \dfrac{(\hbar c)^2}{2r_0^2m_Nc^2V_0'} = \dfrac{1}{A^2}
$$
Similar to action A, if $\Lambda$ is large $\rightarrow$ $T_0$ dominates, so the system will be delocalised (Quantum liquid)