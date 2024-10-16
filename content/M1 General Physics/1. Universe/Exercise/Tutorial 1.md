---
title: Star Tutorial
draft: false
tags:
  - astro
  - physics
  - universe
---
---
### Gravitational Field and Mass Density Law

Let $S$ be a massive ball of center $O$ and radius $R$ with mass volume density $\rho(r)$ and total mass $M$.
1. We assume in this question that $\rho$ is constant.
    - a) Express the gravitational field $\vec{G}$ and potential $\phi$ created by this sphere everywhere in space.
    - b) Imagine a test particle of mass $m$, small enough to move in the field of $S$ without collision. Assuming that this particle is on a circular orbit of radius $r$, express its velocity $v(r)$ for any $r$ and plot $v$ as a function of $r$.

**Solution:**
*Case 1:* Outside of the ball ($r \geq R$)
The gravitational field follow the inverse square law of radius:

$$
\vec{G} = -\dfrac{GM}{r^2} \hat r
$$
where $\hat r$ is the unit vector of radius $r$.

*Case 2:* Inside of the ball ($r < R$)
Only enclosed mass $m(r)$ should be considered, knowing that $\rho = \rm const$, we can deduce $m(r) = \dfrac{M}{R^3} r^3$. 
Thus,

$$
\vec{G} = -\dfrac{Gm(r)}{r^2} \hat r = -\dfrac{GM}{R^3} r \hat r
$$

The potential can be described as

$$
\phi(r) = -\int^r_\infty \vec{G}(r') \cdot dr'
$$

*Case 1:* Outside of the ball ($r \geq R$)

$$
\phi(r) = -\dfrac{GM}{r}
$$
*Case 2:* Inside of the ball ($r < R$)

$$
\phi(r) = \phi(R) + \int_r^R \vec{G}(r') \cdot dr' = -\dfrac{GM}{R} - \dfrac{GM}{2R^3} (R^2 - r^2) = -\dfrac{GM}{2R^3}\left(3R^2 - r^2\right)
$$
Velocity can be solved by Newton second law:
*Case 1:*  $r \geq R$
Balancing the gravitational force and centripetal force:
$$
F_{\rm gravity} = m |\vec{G}| = ma = mv^2/r \, \Rightarrow v(r) = \sqrt{\dfrac{GM}{r}}
$$
*Case 2:* $r<R$
Similarly, we have

$$
\dfrac{GM}{R^3}r = \dfrac{v^2}{r} \Rightarrow v(r) = \sqrt{\dfrac{GM}{R^3}}r
$$
2. 
    - a) Express $m(r)$, the mass inside radius $r$. Express the potential $\phi$ created by this mass.
    - b) Use this result to express the total gravitational energy $U$ of the sphere. Cite another method to obtain this energy.
**Solution:**

The total energy equation:

$$
U = \dfrac{1}{2} \int_0^R \rho(r)\phi(r)dV
$$

We have the potential inside a sphere:

$$
\phi(r) = -\dfrac{GM}{2R^3}(3R^2 - r^2)
$$
So, 

$$
U = -\dfrac{4\pi\rho GM}{4R^3} \int_0^R (3R^3r^2 - r^4)dr = -\dfrac{\pi \rho GM}{R^3} (R^5 - R^5/5) = -\dfrac{4\pi \rho GMR^2}{5} = -\dfrac{3GM^2}{5R}
$$

3. An important case of density law in astrophysics is $\rho(r) = Ar^{-2}$. We study this for the above ball of matter.
    - a) Express the constant $A$ and $m(r)$.
    - b) Express then $U$ as a function of $M$ and $R$.

Using the mass conservation equation:

$$
\dfrac{dm}{dr} = 4\pi r^2\rho(r) = 4 \pi A \Rightarrow M = 4\pi R A \Rightarrow A = \dfrac{M}{4\pi R}
$$

Once again, we use mass conservation equation:

$$
\dfrac{dm}{dr} = 4\pi A = \dfrac{M}{R} \Rightarrow m(r) = \dfrac{M}{R}r
$$

For the total potential energy

$$
dU = -\dfrac{Gm(r)dm}{r} = -\dfrac{4 \pi GM r^2 dr}{R}
$$

Thus, 

$$
U = -\dfrac{4\pi GM}{R} \int_0^R r^2 dr = -\dfrac{4\pi GMR^2}{3}
$$

---

### Mean Molecular Mass

Depending on its state, interstellar gas is a mixture of several dominant species. We note $n_H$ the proton density and $m_H$ the proton mass. The number abundance of He is 10%.

1. Express the gas mass density $\rho$.

2. Express and compute the mean molecular mass $\mu m_H$ in the case of ionized, atomic, and molecular gas respectively.

**Solution:**

We have

$$
\rho = \sum_i n_i m_i = n_H m_H + n_{He} m_{He} = n_H m_H + 0.1 n_H 4 m_H = 1.4 n_Hm_H
$$

We have 

$$
\mu = \dfrac{\rho/m_H}{\sum_i n_i}
$$
For atomic gas

$$
\mu = \dfrac{1.4n_H}{n_H + n_{He}} = \dfrac{1.4n_H}{n_H + 0.1n_H} = \dfrac{1.4}{1.1} \simeq 1.27
$$
For molecular gas, the number density of hydrogen is only half, because 2 H atoms form 1 $\rm H_2$:

$$
\mu = \dfrac{1.4n_H}{0.5n_H + 0.1n_H} = \dfrac{1.4}{0.6} \simeq 2.33
$$

For a fully ionized gas, if $\rm H \rightarrow H^+$ and $\rm He \rightarrow He^+$ 

$$
\mu = \dfrac{1.4n_H}{2n_H + 0.1 \times 2n_H} = \dfrac{1.4}{2.2} \simeq 0.64
$$
If $\rm H \rightarrow H^+$ and $\rm He \rightarrow He^{++}$ 

$$
\mu = \dfrac{1.4n_H}{2n_H + 0.1 \times 3n_H} = \dfrac{1.4}{2.3} \simeq 0.61
$$

---

### Thermal Equilibrium of a Cloud

Consider a spherical cloud of radius $R = 0.1 \, \text{pc}$, mass $M = 2 M_\odot$, and with uniform density $n_H = 10^4 \, \text{cm}^{-3}$. The cloud is assumed isothermal with a temperature $T = 10 \, \text{K}$ resulting from the balance between heating and cooling processes. The heating is due to cosmic rays that pervade the cloud and interact with the gas at a rate of $\zeta = 10^{-16} \, \text{s}^{-1}$ per proton. For each interaction, the gas receives an average energy $E_h = 35 \, \text{eV}$. In the cloud, the extinction cross-section per proton is $\sigma_H = 10^{-25} \left( \frac{300 \, \mu m}{\lambda} \right)^2 \, \text{cm}^2/\text{H}$.

1. 
    - a) Justify the isothermal hypothesis for the cloud.
    - b) Express the cloud cooling power. What is it due to? Estimate the opacity $\tau$ of the cloud to its own radiation.
    - c) Using the thermal equilibrium condition of the cloud, express and compute its emissivity $q$. Compare it to the expected value $q = 3 \times 10^{-4}$ and comment.

2. 
    - a) Express and compute the characteristic time for heating the cloud $\tau_h$.
    - b) Express and compute $\tau_c$, the cooling time of the cloud. Compare to $\tau_h$ and comment.

**Solution:**

For a isothermal condition, we have

$$
dE = (H-L)dt = 0 
$$
Therefore we need to prove that $H = L$

$$
H = \zeta E_h \dfrac{M}{1.4 m_H} = 10^{-16} \times 35 \times 1.6 \times 10^{-19}  \times \dfrac{2 \times 1.99 \times 10^{30}}{1.4 \times 1.67 \times 10^{-27}} = 9.6 \times 10^{23} \rm \, J/s
$$

We have

$$
q_{\rm expected} = n_H R \sigma_H = 10^4 \times 0.1 \times 3.1 \times10^{18} \times 10^{-25} = 3.1 \times 10^{-4}
$$

The cooling of dust emission

$$
L = q4\pi R^2\sigma T^4 = q \times 4 \pi \times(0.1 \times 3.1 \times 10^{16})^2 \times 5.67 \times 10^{-8} \times 10^4 = H
$$

Therefore 

$$
q = 1.4 \times 10^{-5}
$$
So $q = 4 \% \, q_{\rm expected}$

---

### Cooling of a Cloud

Consider a spherical cloud of total mass $M$ and radius $R$ and temperature $T_0$. We assume the cloud emissivity to be $q = 3 \times 10^{-4}$. The effective number of protons per species in the cloud is $\mu$ and the proton mass is $m_H$.

1. 
    - a) Recall the expression of the self gravitational energy $U$ of the cloud.
    - b) Noting $K$ the thermal energy of the cloud, write the total energy of the cloud. Express $K$ as a function of $T_0, M, \mu$, and $m_H$.
    - c) The emission of the cloud is well represented by a modified blackbody law: write then the luminosity $L$ of the cloud.

2. At constant mass $M$ and radius $R$, we follow the cooling law $T(t)$ of the cloud from its initial temperature $T(0) = T_0$.

    - a) Express the energy $dE$ emitted during $dt$. Using the energy equation, write the differential equation verified by $T$.
    - b) Integrate the former equation to find $T$ and define a characteristic evolution time for cooling $\tau_c$.
    - c) Calculate $\tau_c$ for $\mu = 2.3, T_0 = 10 \, \text{K}, M = 1 M_\odot$, and $R = 0.1 \, \text{pc}$.
    - d) As a function of $\tau_c$, express the time $\tau_G$ at which the cloud becomes gravitationally unstable.

1. 
	a. $U = \dfrac{3GM^2}{5R}$ 
	b. $K = \dfrac{3}{2}\dfrac{\rho}{\mu m_H}k_B T_0$ 
	c. $L = q 4\pi R^2 \sigma T_0^4$ 
2. 


---

### Free Fall

We take a uniform ball of matter of initial radius $R_0$ and total mass $M$. The temperature and initial mass density of the ball are noted $T$ and $\rho_0$.

1. Recall the energy criterion for gravitational instability of this ball. In the case of marginal stability, calculate $T$ for $M = 2 M_\odot, R_0 = 0.1 \, \text{pc}$ and $\mu = 2.3$.

2. We now study the free fall evolution of this ball. In this context, free fall is the simultaneous, isotropic, and radial collapse of all parts of the ball. In addition, the free fall is assumed to be homologous, i.e., all the spherical layers of the ball move inward without crossing. The mass density of the free-falling ball is noted $\rho$.

    - a) Within the ball, consider a spherical layer of constant thickness $dr$. Express the mass of this layer $dm$ as a function of $\rho$.
    - b) From the homologous condition and noting $R(t)$ the ball radius, express $\rho(r, t)$ as a function of $\rho_0$.

3. 
    - a) Write the law of motion for layer $dm$ (neglecting pressure forces).
    - b) Write $m(r)$ the mass within the sphere of radius $r$. In the homologous free fall, what can be said of $m(r)$ as a function of time?
    - c) Integrate the law of motion to express $v(r)$ (note $r_0$ the radius of $dm$ before collapse and $m_0$ the enclosed mass). Determine the free fall time of layer $dm$.

---

### Halting the Free Fall

We consider a molecular cloud initially isothermal and of radius $R_0 = 0.1 \, \text{pc}$, mass $M = 2 M_\odot$, luminosity $L = 0.05 L_\odot$, and uniform density $n_0 = 10^4 \, \text{cm}^{-3}$.

1. 
    - a) Show that the emissivity of the cloud is $q = 3 \times 10^{-4}$.
    - b) Estimate the free fall time $\tau_{\text{ff}}$ of this cloud. Assuming the sound crossing time of the cloud $\tau_c$ is equal to $1.45 \tau_{\text{ff}}$, compute $c_S$ the isothermal sound speed and then $T_0$ the cloud initial temperature.
    - c) Discuss the gravitational stability of the cloud.
    - d) What is $L_0$ due to?

2. We now assume the cloud is in free fall.

    - a) Express the mass density $\rho(r, t)$ as a function of $M/R$ and then as a function of the mean density $\bar{\rho}$. Draw the cloud mass density $\rho$ as a function of $r$. Express $n_H(R)$ the proton density at the cloud border.
    - b) Define and express the opacity radius $R_p$ at which the cloud becomes opaque.
    - c) Write a condition for the free fall halt. Express and compute the radius $R_1$ at which this occurs.

3. While the free fall damps at radius $R_1$, the cloud comes in near hydrostatic equilibrium with $3 \bar{p} V = -U$, where $V$ is the volume of the cloud, $\bar{p}$ its mean thermal pressure, and $U$ its gravitational energy.

    - a) From this condition express and compute the cloud mean temperature $T_c$. Compare it to $T_0$.
    - b) Assuming that the cloud in equilibrium is also adiabatic, express the temperature profile $T(r)$ and find the radius $R_c$ where $T = T_c$. Which radius corresponds to $T = T_0$?
    - c) Why is it reasonable to assume adiabatic
