## What is a star ?

A star is a complex system held together by self-gravity, collapse is resisted by internal pressure. Since stars continually radiate into space, there must be a continual energy source.

Some assumptions for studying a star:
- Stars are spherical and symmetry $\rightarrow$ all physical quantities depends on radius $r$
- Ignore rotation, outside gravitational influences.
- Uniform *initial* composition
- Newtonian gravity (no relativistic effects)
- Change slowly with time $\rightarrow$ neglect $\frac{d}{dt}$ terms

To described an isolated, static, symmetric star, we need 4 equations:
1. Conservation of mass
2. Conservation of energy
3. Equation of hydrostatic equilibrium
4. Equation of energy transport

In addition, to solve these equations, we need to describe:
1. Equation of state $p(\rho, \, T)$
2. Opacity (how transparent the gas to radiation)
3. Nuclear energy generation rate as $f(r,\, T)$

### Conservation of mass
If $m(r)$ is the mass interior to radius r, then $m$, $r$, $\rho$ are not independent. 

Consider a thin shell inside the star, radius $r$ and thickness $dr$. The volume is $dV = 4\pi r^2 dr$, so the mass shell is:

$$
dm = \rho(r)dV = 4\pi r^2\rho(r)dr
$$
or 

$$
\dfrac{dm}{dr} = 4\pi r^2 \rho(r)
$$

the equation of *mass conservation*.

### Hydrostatic equilibrium
Consider a small gas parcel  at a distance $r$ to the center of star, with density $\rho(r)$, area $A$ and thickness $dr$. 
- Outward force: $P(r) A$
- Inward force: $P(r+dr)A + \dfrac{Gm(r)dm}{r^2}$  = $P(r+dr)A + \dfrac{Gm(r)A\rho(r)dr}{r^2}$ 
In equilibrium, forces balance so:

$$
P(r)A = P(r+dr)A + \dfrac{Gm(r)A\rho(r)dr}{r^2}
$$

So,

$$
\dfrac{P(r+dr) - P(r)}{dr} = - \dfrac{Gm(r)\rho(r)}{r^2}
$$

Thus,

$$
\dfrac{dP}{dr} = - \dfrac{Gm}{r^2} \rho
$$

#### Central pressure
We can use hydrostatic equilibrium to estimate *central pressure* $P_c$: we approximate the pressure gradient as a constant:

$$
\dfrac{dP}{dr} = - \dfrac{\Delta P}{\Delta R} = \dfrac{P_c}{R} = \dfrac{GM}{R^2} \rho
$$

Now, we assume that the star has constant density, so:

$$
\rho_c = \bar \rho = \dfrac{M}{V} = \dfrac{M}{4/3\pi R^3}
$$

Thus,

$$
P_c = \dfrac{3GM^2}{4\pi R^4}
$$
So we have the relationship that $P_c \propto \dfrac{M^2}{R^4}$
For the Sun, we can estimate $P_c \sim 3 \times 10^{14} \, \rm Nm^{-2}$

### Virial theorem 
Consider a particle in a circular orbit of radius $r$ around a mass $M$. 
The potential energy is:

$$
\Omega = -\dfrac{GMm}{r}
$$

The Keplerian velocity of particle is 

$$
v = \sqrt{\dfrac{GM}{r}}
$$

The kinetic energy is 

$$
K = \dfrac{1}{2} mv^2 = \dfrac{1}{2} \dfrac{GMm}{r} = -\dfrac{1}{2}\Omega
$$

Or, 

$$
2K+\Omega = 0
$$

The total energy

$$
E = K + \Omega = -\dfrac{\Omega}{2} + \Omega = \dfrac{\Omega}{2} < 0
$$
The virial theorem also true for variety of systems, from clusters of galaxies to ideal gas, for a star, we also have:

$$
2U + \Omega = 0
$$

> If there is a decrease in total energy $E$, potential $\Omega$ decreases, but thermal/internal energy $U$ increases, hence $T$ increases. 

> When a star loses energy, it heats up
