---
title: Interstellar medium
draft: false
tags:
  - physics
  - astro
  - universe
---
 Baryonic matter of the universe mostly stays inside **Interstellar Medium** (ISM) containing of molecular, atomic and ionized gas, with variety of densities and temperature. In general, ISM will be heated by high-energy ionized particles so-called **Cosmic Rays** and cooled by **dust**. Molecular clouds are the most interesting and dynamical places because they are star-forming regions. Stars will also feedback to ISM through mechanical (outflows, shocks), radiation (photodissociation & photoionization) and elemement enrichments through Core-collapse Supernova (CCSN). 

Molecular clouds:
- Mass: $M = 10^2 \sim 10^5 \, \rm M_\odot$ 
- Size: $d \simeq 100 \, \rm pc$ 
- Number density: $n = 10^2 \sim 10^4 \, \rm cm^{-3}$ 
- Temperature: $T = 10-100 \rm \, K$

Stars:
- Mass: $M = 2 \times 10^{11} \, \rm M_\odot$
- Mass density: $n = 1 \, \rm g.cm^{-3}$ 
- Number density: $n = 10^{24} \, \rm cm^{-3}$
- Deposited energy per volume : $e_{star} = \dfrac{2}{3}e$

To form new star, some regions in molecular clouds should be compressed $\gtrsim 20$ order of magnitude. 

- $M_{\rm galaxy} = 10^{12} \, \rm M_\odot$ including $M_{stars} = 2 \times 10^{11} \, \rm M_\odot$ (the rest is dark matter) 
- $71\% \,  \rm m_H$ - $28\% \,  \rm m_{He}$ - $1\% \,  \rm m_{dust}$ and heavy elements (O, N, C, Si)
## Some concepts
#### Units
1. Distance
	- parsec (pc): 1 pc = 3.26 ly = $3.086 \times 10^{16}$ m (Nearest star is 1.3 pc away)
	- solar radius: 1 $R_\odot = 6.955 \times 10^8$ m
2. Mass
	- solar mass: 1 $M_\odot$ = 1.989 $\times 10^{30}$ kg
3. Luminosity
	- solar luminosity: 1 $L_\odot$ = 3.839 $\times 10^{26}$ W
#### Mean molecular mass
Ideal gas law:

$$
P = nk_BT = \dfrac{\rho k_B T}{\bar m} = \dfrac{\rho k_B T}{\mu m_H} 
$$

where
- $n$ is the number density 
- $\bar m$ is the average mass per particle
- $\mu$ is the mean molecular weight
- $m_H$ is the mass of a proton

Gas density:

$$
\rho = \sum_i n_i m_i
$$
where $n_i$ is the number density of specie $i$. 
Ex: From Big Bang nucleosynthesis, the ratio of $\dfrac{n_{He}}{n_{H}} = \dfrac{1}{10}$. Therefore

$$
\rho_{\rm gas} \simeq m_H n_H + m_{He} n_{He} = m_H n_H + 4m_H0.1n_H = 1.4m_Hn_H
$$
#### Isothermal sound speed
In an adiabatic process $p \propto \rho^\gamma$, so the sound speed can be defined as:

$$
c_s^2 = \dfrac{dp}{d\rho} = \dfrac{\gamma p}{\rho}
$$
Ideal gas law:

$$
p = \dfrac{\rho k_B T}{\mu m_H}
$$
Therefore

$$
c_s^2 = \dfrac{\gamma k_B T}{\mu m_H}
$$
#### Modified black body radiation
$$
B_\lambda(T) = \dfrac{8\pi hc}{\lambda^5}\dfrac{1}{e^{hc/\lambda kT} - 1}
$$

## Heating and cooling of a molecular cloud

The change of internal energy of a molecular cloud:

$$
dE = (H-L)dt
$$

where $H$ and $L$ are the power of heating and cooling process 

The heating process $H$ is mainly powered by the pass-through of cosmic rays:

$$
H = \zeta E_h \dfrac{M}{\mu m_H}
$$
where 
- $\zeta \simeq 10^{-17} - 10^{-15} \, \rm s^{-1} H^{-1}$ : cosmic ray ionization rate (number of ionizations per hydrogen atom per second)
- $E_h \sim 10 \rm \, eV$: Energy deposited per ionization (*heat efficiency*) 
- $\dfrac{M}{\mu m_H}$: number of hydrogen atoms

The cooling process $L$ is powered by dust grains which can be described by the modified blackbody for dust emission:

$$
I = qB_\nu(T)
$$

where $q$ is the opacity which can be characterised by the [[Fundamental Concepts|optical depth]] 

$$
\tau = n_c \sigma_e = n_H R \sigma_e
$$

where 
- $n_c$ : column number density
- $\sigma_e \simeq 10^{-25} (\dfrac{300 \mu m}{\lambda})^\beta$ : extinction cross section of dust grains per proton

We take $q = n_H R \sigma_e \simeq 3 \times 10^{-4} \left( \dfrac{n_H}{10^4 \, {\rm cm^{-3}}} \right) \left( \dfrac{R}{0.1 \, {\rm pc}} \right)$

For a molecular cloud:
- $T = 10\, \rm K$. From Wien's law: $\lambda_{\mu m} T_{\rm K} \simeq 3 \times 10^3 \, \rm \mu m K$ $\rightarrow$ $\lambda \simeq 300 \, \rm \mu m$
- $n_H \simeq 10^4 \rm \,cm^{-3}$
- $R \simeq 0.1 \, \rm pc$

### Energy 
The thermal energy can be described as

$$
K = \dfrac{3}{2} N k_B T = \dfrac{3}{2} \dfrac{M}{\mu m_H} k_BT
$$

The potential energy can be described as

$$
dU = -\dfrac{Gm(r)dm}{r}
$$

Assumption: $\rho = \rm const$ 
So, 

$$
\rho = \dfrac{M}{4/3 \pi R^3} = \dfrac{m(r)}{4/3 \pi r^3} \, \Rightarrow \, m(r) = M \dfrac{r^3}{R^3}
$$
And, 

$$
dm = \dfrac{M}{4/3 \pi R^3} 4 \pi r^2 dr = \dfrac{3M}{R^3} r^2 dr
$$

Thus

$$
dU = -\dfrac{3GM^2}{R^6}r^4dr
$$

Integrate all over from 0 to $R$ to get the total internal energy

$$
U = -\dfrac{3GM^2}{R^6} \int_0^R r^4dr = -\dfrac{3GM^2}{5R}
$$
