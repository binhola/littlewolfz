---
title: Cosmology
draft: false
tags:
  - physics
  - universe
  - cosmo
---
## Cosmological principle
1. Copernican principle: the universe is equivalent in all locations (We are not at a special location in our universe)
2. Local isotropy: the universe looks the same in all directions.

Ultimately, they lead to the cosmological principle that the universe is *homogenous* and *isotropy*. 
## Hubble law
The further we look into the universe, the faster objects moving away from us
$$\vec{v_0} = H_0 \vec{D_0}$$ 
where $t_0$ represent present time and $H_0 = 100 \, h \, \, \rm km \, s^{-1} \, Mpc^{-1}$. The measurement for $h$ now is about 0.67 (Planck).

Generalizing to any time, we have

$$
\vec{v(t)} = H(t) \vec{D(t)}
$$
where $H(t)$ is the Hubble parameter.

We have 

$$
\dfrac{d \vec{D(t)}}{\vec{D(t)}} = H(t) dt
$$
Integrating, we have
$$
\vec{D(t)} = \vec{D_0} \, e^{\int_t H(t)dt}
$$
We can define the scale factor $a(t)$ as 
$$
a(t) = e^{\int_t H(t)dt} \quad \text{and} \quad a(t_0) = a_0 = 1
$$
We can also define the *comoving distance* or *comoving coordinate*. Imagine having a system of coordinates attached to a grid. If the object do not possess their own motion, they are fixed in this grid, so called "comoving coordinate":
$$
\vec{\chi} \equiv \vec{D_0}
$$
The only thing that make the galaxies receding away is the expansion of the universe, characterized by the scale factor $a$.
## Redshift
When the galaxies recede from us, the wavelength of emitted light from the receding objects would be stretched out. We define them as:
$$
1 + z = \dfrac{\lambda_{\rm obs}}{\lambda_{\rm emit}} = \dfrac{1}{a} 
$$
## Very brief on Einstein field equation

The universe is described by General Relativity that beautifully connects the geometry of spacetime to energy, as a famous quote by physicist J. A. Wheeler "*Matter tells spacetime how to curve. Spacetime tells matter how to move*":

$$
R_{\mu \nu} - \dfrac{1}{2} R\,g_{\mu \nu} + \Lambda g_{\mu \nu} = \dfrac{8\pi G}{c^4} T_{\mu \nu}
$$
where
- $R_{\mu \nu}$ : Ricci tensor
- $R = R^{\mu}_\mu = {\rm Tr}(R^{\mu}_{\nu})$ : Ricci scalar
- $g_{\mu \nu}$ : metric tensor
- $T_{\mu \nu}$ : stress-energy tensor
- $\Lambda$ : cosmological constant

In the case of perfect fluid, we can define the stress-energy tensor as
$$
T_{\mu \nu} = \begin{pmatrix} \epsilon & 0 & 0 & 0 \\ 0 & p & 0 & 0 \\ 0 & 0 & p & 0 \\ 0 & 0 & 0 & p \end{pmatrix}
$$
where $\epsilon$ is the total energy density and $p$ is the total pressure. 

This is a non-linear functions of $g_{\mu \nu}$ and not an easy-to-solve problem for a general solution.

If we, then, combine the cosmological principle with Einstein field equation, we can obtain a solution, so-called Friedmann equations. 

## Geometry of the universe

### Euclidean geometry
In Euclidean geometry (flat geometry) and in 3D with Cartersian coordinate, line element $dl$ is given by
$$
dl^2 = dx^2 + dy^2 + dz^2
$$
In spherical coordinates
$$
dl^2 = d\mathscr{r}^2 + \mathscr{r}^2(d\theta^2 + sin^2 \theta \, d\phi^2)
$$
### Spherical geometry 
We embed the 3D sphere $S^3$ into an embedding 4D Euclidean space $R^4$ in order to represent the curvature of space:
$$x^2 + y^2 + z^2 + w^2 = R^2$$
where $R$ is the radius of the curvature. The sphere has uniform positive curvature.

We can define
$$w^2 = R^2 - \mathscr{r}^2$$
to eliminate $w$, where $\mathscr{r}$ is the radial coordinate on the sphere. 
We have
$$
dw = -\dfrac{\mathscr{r}d\mathscr{r}}{\sqrt{(R^2-\mathscr{r}^2)}}
$$

So
$$
dl^2 = dx^2 + dy^2 + dz^2 + dw^2 = d\mathscr{r}^2 + \mathscr{r}^2(d\theta^2 + \sin^2 \theta \, d\phi^2) + \dfrac{\mathscr{r}^2}{R^2 - \mathscr{r}^2} d\mathscr{r}^2
$$
Thus,
$$
dl^2 = \dfrac{R^2}{R^2 - \mathscr{r}^2} d\mathscr{r}^2 + \mathscr{r}^2(d\theta^2 + \sin^2 \theta \, d\phi^2)
$$
### Hyperbolic geometry
Similarly, we embed the 3D hyperbolic space $H^3$ into embedding space $R^4$
$$x^2 + y^2 + z^2 - w^2 = - R^2$$
And we have 
$$
w^2 = \mathscr{r}^2 + R^2
$$
So
$$
ds^2 = dx^2 + dy^2 + dz^2 - dw^2
$$
Solve all of these equation, we arrive at
$$
dl^2 = \dfrac{R^2}{R^2 + \mathscr{r}^2} d\mathscr{r}^2 + \mathscr{r}^2(d\theta^2 + \sin^2 \theta \, d\phi^2)
$$
It is useful to write these metrics in a unified form, parameterized by $k$ in $(r, \theta, \phi)$ coordinates.
$$
dl^2 = \dfrac{d\mathscr{r}^2}{1-k\mathscr{r}^2/R^2} + \mathscr{r}^2(d\theta^2 + \sin^2 \theta \, d\phi^2) \quad \text{with} \quad k = \begin{cases} -1 & \text{Hyperbolic} \\ 0 & \text{Euclidean} \\ +1 & \text{Spherical} \end{cases}
$$
We define
$$
r = \dfrac{\mathscr{r}}{R}
$$
Then $dl$ will be simplified as
$$
dl^2 = R^2 \left[ \dfrac{dr^2}{1-kr^2} + r^2(d\theta^2 + \sin^2 \theta \, d\phi^2) \right] \quad \text{with} \quad k = \begin{cases} -1 & r \in [0,+\infty) \\ 0 & r \in[0, +\infty)  \\ +1 & r \in [0,1) \end{cases}
$$
### Friedmann-Lemaitre-Robertson-Walker (FLRW)
For Minkowski geometry of spacetime $M4$ or (1, 3):
$$
ds^2 = -c^2 dt^2 + dl^2 
$$
So, FLRW metric can be written as
$$
ds^2 = -cdt^2 + R^2(t) \left[ \dfrac{dr^2}{1-kr^2} + r^2(d\theta^2 + \sin^2\theta d\phi^2) \right]
$$
We let radial metric to be written under the comoving metric as
$$
R^2(t) \dfrac{dr^2}{1-kr^2} = a^2(t) d^2\chi
$$
where $R(t) = a(t)R_0$.
Thus
$$
d\left( \dfrac{\chi}{R_0} \right) = \dfrac{dr}{\sqrt{1-kr^2}}
$$
Then we can write the second form of FLRW metric as
$$
ds^2 = -cdt^2 + a^2(t) \left[d\chi^2 + f_k^2(\chi) (d\theta^2 + \sin^2\theta \, d\phi^2) \right] \quad f_k(\chi) = R_0 \begin{cases} \sinh \left(\dfrac{\chi}{R_0}\right) & k = -1 & \chi \in [0, \infty)\\ \dfrac{\chi}{R_0} & k = 0 & \chi \in [0, \infty)\\ \sin \left(\dfrac{\chi}{R_0}\right) & k = +1 & \dfrac{\chi}{R_0} \in [0, \pi) \end{cases}
$$
## Properties of FLRW metric

Consider a set of points with a fixed value of $\chi$ which is a surface of a sphere of comoving radius $\chi$, so-called $S_k(\chi)$

#### Spatial line element on $S_k(\chi)$
$$
dl^2 = a^2(t)f_k^2(\chi)d\Omega^2 \quad \text{where} \quad d\Omega^2 = d\theta^2 + \sin^2\theta d\phi^2
$$
#### Surface element
$$
dS_k(\chi) = a^2(t)f^2_k(\chi)^2 \sin\theta \,d\theta \, d\phi
$$
#### Area of $S_k(\chi)$
$$
S_k(\chi) = \int_0^{2\pi} \int_0^{\pi} dS_k(\chi) = 4\pi a^2(t)f^2_k(\chi)
$$
- If $k = -1$:
$$
S_{-1}(\chi) = 4\pi a^2(t) R_0^2 \sinh^2 \left(\dfrac{\chi}{R_0}\right)
$$
- If $k=0$:
$$
S_0(\chi) = 4\pi a^2(t) \chi^2
$$
- If $k=+1$:
$$
S_{1}(\chi) = 4\pi a^2(t) R_0^2 \sin^2 \left(\dfrac{\chi}{R_0}\right)
$$

##### Remarks:
1. For the case of $k = \{-1, \,1\}$ 
+ if $\dfrac{\chi}{R_0} << 1$ then we can Taylor expand and recover the Euclidean geometry.
+ if $\dfrac{\chi}{R_0} >> 1$ then we can see that $S_1(\chi) < S_0(\chi) < S_{-1}(\chi)$ 

2. Limits of surface area
For the case of $k = \{-1, \, 0\}$, because $\chi \in [0,+\infty)$ so $S_{\{-1, \,0\}}(\chi) \rightarrow +\infty$ 

For the case of $k = 1$, because $\dfrac{\chi}{R_0} \in [0,\, \pi)$ so $S_1(\chi) \rightarrow 0$ as  $\dfrac{\chi}{R_0} \rightarrow \pi$. The maximum surface area, however, defined at the point halfway from the origin $\dfrac{\chi}{R_0} = \pi/2$ with $S_1(\chi) = 4\pi R_0^2 a^2(t)$

#### Volume element 
$$
dV_k(\chi) = S_k(\chi) a(t) d\chi 
$$
#### The finite volume $V_k(\chi)$
$$
V_k(\chi) = \int dV_k(\chi) = \int_0^{\chi} S_k(\chi') a(t)d\chi'
$$
- $k = 0$ 
$$
V_0(\chi) = \int_0^{\chi} 4\pi a^3(t) \chi'^2 d\chi' = \dfrac{4}{3} \pi a^3(t) \chi^3
$$
- $k=1$
$$
V_1{\chi} = \int_0^\chi 4\pi a^3(t) R_0^2 \sin^2 \left(\dfrac{\chi'}{R_0}\right) d\chi' = \left( \dfrac{4}{3} \pi a^3(t) R_0^3 \right) \times \dfrac{3}{4}\left[ 2 \dfrac{\chi}{R_0} - \sin \left( 2 \dfrac{\chi}{R_0} \right) \right]
$$
- $k = -1$
$$
V_{-1}(\chi) = \int_0^\chi 4\pi a^3(t) R_0^2 \sinh^2 \left(\dfrac{\chi'}{R_0}\right) d\chi' = \left( \dfrac{4}{3} \pi a^3(t) R_0^3 \right) \times \dfrac{3}{4}\left[ \sinh \left( 2 \dfrac{\chi}{R_0} \right) - 2 \dfrac{\chi}{R_0}\right]
$$
##### Remarks:
1. When $\chi \rightarrow \max(\chi)$ 
- $k =-1$ : $\chi \rightarrow \infty \quad \text{then} \quad V_{-1}(\chi) \rightarrow \infty$  
- $k =0$ : $\chi \rightarrow \infty \quad \text{then} \quad V_0(\chi) \rightarrow \infty$  
- $k = 1$ : $\chi \rightarrow R_0 \pi \quad \text{then} \quad V_1(\chi) \rightarrow 2\pi^2 (a R_0)^3$ 

**Conclusion:** In spherical symmetry, the maximum volume of a sphere is finite with zero surface.
