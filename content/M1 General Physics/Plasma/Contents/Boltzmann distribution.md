---
title: Boltzmann distribution
tags:
  - physics
  - plasma
  - statphys
draft: false
---
## Macro-state and micro-state:
A **macro-state** defines by an energy $E$ $\rightarrow$ different arrangement/configuration of atoms/molecules so called **micro-states** $E_i$.
#### Micro-canonical ensemble 
Given a state $\{\Psi_i\}$ where $i = 1,2,...$ such that $E_1 = E_2 = .... = E$ with each microstate $i$ occurs with equal probability (because all $\Psi_i$ are indistinguishable by $E_i$) 

#### Boltzmann distribution
A probability distribution giving the probability of finding a macroscopic system in a given microstate under thermal equilibrium.

*Thermal equilibrium occurs when the probability distribution of a system becomes independent of time*

Consider a closed system (only transfer heat not particles with environment) of energy $E_i$ where 
- $E_i << E_{env}$ 
- $E = E_i + E_{env} = \rm const$  
Probability finding a system in $\Psi_i$ with $\Omega(E_{env}) \equiv$ Number of microstates of environment consistent with $\Psi_i$:
$$
P(\Psi_i) \propto \Omega(E_{env}) = \Omega(E - E_{i})
$$
Assume that $E_i << E_{env}, E$
$$
\Omega(E- E_i) = e^{\log \Omega(E-E_i)}
$$
Taylor expansion for the logarithm term gives
$$
\log \Omega(E-E_i) = \log \Omega(E) - \dfrac{\partial \log \Omega(E)}{\partial E} E_i + O(E_i^2)
$$
Drop all higher derivatives:
$$
\dfrac{\partial^n }{\partial E^n} \log \Omega(E) \approx 0 \quad \text{for} \quad n \geq 2
$$
So
$$
P(\Psi_i) \propto e^{-\dfrac{\partial \log \Omega(E)}{\partial E} E_i}
$$
We can define
- *Entropy*: $S = k_B \log \Omega(E)$ 
- *Temperature*: $\dfrac{1}{T} = \dfrac{\partial S(E)}{\partial E}$  $\Rightarrow$ $\beta = \dfrac{1}{k_B T} = \dfrac{\partial \log \Omega(E)}{\partial E}$ 
After normalization, we get
$$
P(\Psi_i) = \dfrac{1}{Z} e^{-\beta E_i}
$$
Because $\sum_i P(\Psi_i) = 1$ so $Z = \sum_i e^{-\beta E_i}$ is defined as *partition function* which contain all statistical information of a system.

For a Boltzmann distribution in 1D, we have
$$
P(v) = \sqrt{\dfrac{m}{2\pi k_B T}} e^{\frac{m}{2k_BT}v^2}
$$
For a Boltzmann distribution in 3D, we have
$$
P(v) = 4\pi v^2 \left(\dfrac{m}{2\pi k_B T} \right)^{3/2} e^{\frac{m}{2k_BT}v^2}
$$
Velocity expressions:
$$ \begin{aligned}
v_{mp} &= \sqrt{\dfrac{2k_BT}{m}} \\
v_{mean} &= \sqrt{\dfrac{8k_BT}{\pi m}} = v_{th} \\
v_{rms} &= \sqrt{\dfrac{3k_BT}{m}}
\end{aligned}
$$
We have the relation:
$$
v_{mp} < v_{th} < v_{rms}
$$
### Boltzmann relation by considering the most probable state
Thermal Equilibrium $\leftrightarrow$ Most probable state (State with large number of possible arrangements of micro-states)

Consider two weakly coupled system $S_1$ and $S_2$ with energy $E_1$, $E_2$. Let $g_1$ and $g_2$ be the number of microstates of $E_1$ and $E_2$. The total microstates assuming states are independent:
$$g = g_1 g_2$$
If the total energy $E=E_1 + E_2$ fixed:
$$
g = g_1(E_1)g_2(E - E_1)
$$
and 
$$
\dfrac{dg}{dE_1} = \dfrac{dg_1}{dE}g_2 - g_1 \dfrac{dg_2}{dE}
$$The most probable state occurs when $\dfrac{dg}{dE_1} = 0$, so
$$
\dfrac{dg_1}{dE_1}g_2 - g_1 \dfrac{dg_2}{dE_2} = 0
$$
So 
$$
\dfrac{d}{dE_1} \log g_1 = \dfrac{d}{dE_2} \log g_2
$$
Thus, in equilibrium, states in thermal contact have equal values of $\dfrac{d}{dE} \log g$
We can define $\sigma = \log g$ as the *Entropy*.
And $\left(\dfrac{d}{dE} \log g \right)^{-1} = T$ as *Temperature*
The relative probability of 2 micro-states of system 1 $\equiv$ 

