---
title: <% tp.file.title %>
draft: false
tags:
---
## Cosmological Horizon
### The horizon (particle horizon)
**Definition**: the maximum distance at which a particle could have travelled freely since the Big Bang. 

Bounded from above by light propagation (second postulate of Special Relativity - nothing travels faster than the speed of light)

Photon following the geodesis of the light-like interval 
$$
D_{hor, c}(t) = R_{H_0} \int_0^{a(t)} \dfrac{da}{a^2 E(a)} = R_{H_0} \int_0^z \dfrac{dz}{E(z)}
$$
Physical horizon
$$
D_{hor}(t) = a(t) D_{hor,c}(t)
$$
Present day horizon:
$$
D_{hor,c}(t_0) = a_0 D_{hor,c}(t_0) = R_{H_0} \int_0^1 \dfrac{da}{a^2 E(a)} = R_{H_0} \int_0^{\infty} \dfrac{dz}{E(z)}
$$
The final term coming from the fact that:
$$
a = \dfrac{1}{z+1} \quad \Rightarrow \quad da = -\dfrac{dz}{(z+1)^2}
$$
So, 
$$
\dfrac{da}{a^2 E(a)} = -\dfrac{dz}{E(z)}
$$
When $a = 0 \rightarrow z=\infty$ and $a=1 \rightarrow z = 0$.

#### Exercise
1. Compute the present day horizon in the Eds universe with critical density

**Solution**: 
- Critical density = flat geometry, so $\Omega_{k,0} = 0$
- We have the rebb b.        lation: $$\Omega_{k,0} + \Omega_{T,0} = 1$$

So 
$$\Omega_{T,0} = 1$$
 For Eds - matter only universe, we have
$$E^2(a) = \Omega_m (a) = \Omega_{m,0} a^{-3} = a^{-3}$$
And 
$$
E^2(z) = \Omega_m(z) = \Omega_{m,0}(z+1)^3 = (z+1)^3
$$
So
$$
D_{hor} = a_0D_{hor,c} = R_{H_0}\int_0^1 \dfrac{da}{a^2 E(a)} = R_{H_0}\int_0^1 \dfrac{da}{a^2 a^{-3/2}} = R_{H_0}\int_0^1 a^{-1/2}\,da = 2 R_{H_0}
$$
2. Compute the horizon at $z_{CMB}$

**Solution:**

At CMB time
$$
\Omega_\Lambda = 0.7 \quad \Omega_{m,0} = 0.3 \quad \Omega_{r,0} = 8 \times 10^{-5} \quad \Omega_{k,0} = 0
$$
So
$$
E^2(a) = \Omega_{m,0} \, a^{-3} + \Omega_{r,0} \, a^{-4} + \Omega_\Lambda
$$
And
$$
\Omega_{m,0} + \Omega_{r,0} + \Omega_\Lambda = 1
$$
At $z_{CMB} = 1100 \quad \Rightarrow \quad a \sim 9\times 10^{-4}$

Cosmological constant is negligible compared to other two components
So
$$
\begin{aligned}
D_{hor, CMB} &= a_{CMB} \, R_{H_0} \int_0^{a_{CMB}} \dfrac{da}{a^2 E(a)} = R_{H_0} \int_0^{a_{CMB}}  \dfrac{da}{a^2(\Omega_{m,0}a^{-3} + \Omega_{r,0}a^{-4})^{1/2}}
\\
&= a_{CMB} \, R_{H_0} \int_0^{a_{CMB}}  \dfrac{da}{(\Omega_{m,0}a + \Omega_{r,0})^{1/2}} \\
&= \dfrac{2\,a_{CMB} \,R_{H_0}}{\Omega_{m,0}} \left(\sqrt{\Omega_{m,0} \, a_{CMB} + \Omega_{r,0}} - \sqrt{\Omega_{r,0}}\right) = 6 \times 10^{-5} R_{H_0}
\end{aligned}
$$
And given that $$R_{H_0} = 2996.89\, \mathrm{h^{-1}\,Mpc} \quad \text{where} \quad \mathrm{h = \dfrac{H_0}{100 \, km/s/Mpc}}$$
With $H_0 = 70 \, \mathrm{km/s/Mpc}$

3. Present day horizon in $\Lambda CDM$ (numerical)
4. Consider a universe with $k=0$, containng only one fluid of EoS $w(=\text{const})$. Find the expression of $D_{hor}(t)$ in this case
$$
D_{hor}(t) = a(t) R_{H_0}\int_0^{a(t)} \dfrac{da}{a^2 E(a)}
$$
We have
$$
E^2(a) = \Omega_{i,0} a^{-3(1+w_i)} = a^{-3(1+w_i)}
$$
Then
$$
D_{hor}(t_0) = a_0 R_{H_0}\int_0^{1} \dfrac{da}{a^2 a^{\frac{-3(1+w_i)}{2}}} = R_{H_0}\int_0^{1} a^{\frac{-1+3w_i}{2}} da = R_{H_0} \dfrac{2}{1+3w_i}
$$
We have to stop before the last step because we see that for $\dfrac{-1+3w_i}{2}\leq-1 \quad \text{or} \quad w_i \leq \dfrac{-1}{3}$ then the integral at 0 will go to infinite, meaning that the horizon is at infinite, the Big Bang is infinitely far in the past.

**Note:** The age of the universe at time $t$:
$$
t = t_{H_0} \int_0^{a(t)} a^{\frac{1+3w_i}{2}} da
$$
becomes diverges when $\dfrac{1+3w_i}{2} \leq -1$ or $w_i \leq -1$.
So if the fluid has $w_i \in (-1, -1/3]$, it would have finite age with infinite horizon.

### Cosmological event horizon
**Definition:** Maximum distance from which light emitted today will be able to reach us (in the future).

**Note**: we consider the universe to expand forever in this case.

$$
D_{ev,c}(t_0) = \int_0^{D_{ev,c}} d\chi = c \int_{t_0}^{t} \dfrac{dt}{a(t)} \quad \text{where} \quad t > t_0
$$
Suppose expansion continues to infinity, so $\max(t) =\infty$, then
$$
D_{ev,c}(t_0) = R_{H_0} \int_{a_0}^{a(t)} \dfrac{da}{a^2 E(a)}
$$
For $\Lambda$CDM, we have
$$
D_{ev,c}(t_0) = R_{H_0} \int_{a_0}^{a(t)} \dfrac{da}{a^2 \sqrt{\Omega_{m,0}a^{-3} + \Omega_{r,0}a^{-4}+\Omega_\Lambda}}
$$
Intuitively, in $\Lambda$CDM, we know that it is the cosmological constant dominated era and radiation is just a very small fraction, but also because $\Omega_{r,0}$ and $a^{-4}$ will be extremely small.
$$
D_{ev,c}(t_0) = R_{H_0} \int_{a_0}^{a(t)} \dfrac{da}{ \sqrt{\Omega_{m,0}\, a + \Omega_\Lambda\, a^4}}
$$
*Remark*: In reality, we can not actually measure $D_c(z)$ and $D(z)$, so we need a new distance notions defined by measurable quantities.
### Angular diameter distance
**Definition:** Distance defined by the physical size $\ell$ of the observed object projected on the sky and the angle $\theta$ that it subtends on the celestial sphere.

Usually,  we have $\theta = \dfrac{\ell}{d}$ , limit at small angles of $\tan(\theta)=\dfrac{\ell}{d}$ where the source of size $\ell$ has a redshift of $z$.

Back to FLRW metric, an object with redshift $z$ sitting at a given (fixed) $\chi$
$$
d\ell^2 = a^2(t) f_k^2(t) (d\theta^2 + \sin^2\theta \, d\phi^2)
$$
We choose a fixed $\phi$.
The equation reduces to 
$$
d \ell = a(t) f_k(t) d\theta
$$
Then
$$
\ell = a(t) f_k(t) \theta
$$
So
$$
D_{A}(a) = a(t) f_k(t) \quad \text{where} \quad D_A(z) = \dfrac{f_k(t)}{1+z} 
$$
where
$$
f_k(t) = R_0
\begin{cases}
& \sin \left(\dfrac{\chi}{R_0} \right) & k=1\\
& \dfrac{\chi}{R_0} & k=0\\
& \sinh \left( \dfrac{\chi}{R_0} \right) & k=-1
\end{cases}
$$
with $\chi$ is the comoving distance of the observed source:
$$
\chi = D_c(z)
$$
So
$$
D_A{z} = a(z) D_c(z)
$$
#### Exercises
1. In the Eds universe, find the value $Z_c$ of $z$ above which the recession velocity of the galaxy is larger than $c$

**Solution:**
$$
v_0 = H_0 D_0
$$
where $D_0$ is the present day radial distance to the source of light.
Then
$$
H_0 D_0 > c \Leftrightarrow D_0 > R_{H_0}
$$
So
$$
R_{H_0} \int_z^0 \dfrac{dz}{E(z)} > R_{H_0}
$$
Then
$$
\int_z^0 \dfrac{dz}{E(z)} > 1 \Leftrightarrow \int_z^0 (1+z)^{-3/2} dz > 1
$$
Thus,
$$
2\left(1-(1+z)^{-1/2}\right) > 1
$$
So
$$
z > 3
$$

For, dS universe (cosmological constant only universe), we have $z > 1$

For a radiation only universe, we have $z =\infty$, so we always see the light coming towards us.

2. In the Eds universe, consider a source with redshift $z=z_c=3$. Suppose it emits light today, will we ever see that light in the future? If so, when? If so, at what maximum distance?

### Luminosity distance
Normally, in the every day life scale, the relation between the intrinsic luminosity $L_s$ of the source and its distance to us $d$ is given by the flux
$$
F = \dfrac{L_s}{4 \pi d^2}
$$
In cosmology, the luminosity distance is defined by
$$
D_L = \sqrt{\dfrac{L_s}{4\pi F}}
$$
*Note:* The issue is that
- $L_s$ is the intrinsic luminosity defined in the frame of the source.
- $F$ is the observed flux defined in the frame of the observer
We need to move into the same frame

We have the luminosity in the frame of the source (emission)
$$
L_s = \dfrac{\Delta E_{\rm e}}{\Delta t_{\rm e}}
$$
In the frame of the observer:
$$
L_o = \dfrac{\Delta E_o}{\Delta t_o}
$$
For simplicity, we assume that the source is monochromatic
$$
\Delta E_e = h\nu_e \quad \text{and} \quad \Delta E_o = h \nu_o
$$
Then
$$
\dfrac{\Delta E_e}{\Delta E_o} = \dfrac{\nu_e}{\nu_o} = \dfrac{\lambda_o}{\lambda_e} = 1 + z 
$$
In addition
$$
\dfrac{\Delta t_e}{\Delta t_o} = \dfrac{\nu_o}{\nu_e} = \dfrac{1}{1+z}
$$
So, we have
$$
\dfrac{L_o}{L_s} = \dfrac{1}{(1+z)^2}
$$
The received flux $F$, by definition, the luminosity uniformly distributed on the surface $\sum$ of the sphere centering on the source and intercepting the observer.

$\sum$ is the surface of the sphere whose center is at the comoving coordinate $\chi_s$ of the source.
$$
\sum(t) = 4 \pi a^2(t) f_k^2(\chi)
$$
Today, $\sum (t_0) = 4 \pi f^2_k \left(D_{com}(z) \right)$
$$
D_{L} = \sqrt{\dfrac{L_s}{4\pi F}} = \sqrt{\dfrac{L_s}{4 \pi \dfrac{L_o}{\sum(t_0)}}} = (1+z) f_k(D_{\rm com}(z))
$$
where $D_{\rm com}(z) = R_{H_0} \int_{1/(1+z)}^1 \dfrac{da}{a^2 E(a)} = R_{H_0} \int_0^z \dfrac{dz}{E(z)}$

Angular diameter distance
$$
D_A(z) = \dfrac{1}{1+z} f_k(\chi)
$$
Luminosity distance
$$
D_L(z) = (1+z) f_k(\chi)
$$
So, we have *Duality relation*
$$
D_L(z) = (1+z)^2 D_A(z)
$$
Duality relation holds in any arbitrary metric, if some process like absorption, diffusion, transformation, etc happens, the duality relation will be violated.

#### Magnitudes
##### Apparent magnitude (m)
**Definition:** the measure of the brightness of the source by comparison with the brightness of the reference source
$$
m = -2.5 \log_{10} \left( \dfrac{F}{F_{\rm ref}} \right)
$$
Ranking of the visible to the naked eye from the brightest: 1 - 5
- For $m = 1$ we have about $F \sim 40\% F_{\rm ref}$
- For $m = 5$ we have about $F \sim 1\% F_{\rm ref}$

There are several magnitude system depends on the $F_{\rm ref}$ that we choose. When not specified, reference source is Vega.

##### Absolute magnitude (M)
**Definition**: the magnitude of the source would have if it is located 10 pc from us.

The distance modulus
$$
\mu = m - M
$$
Then we have
$$
\mu = 5 \log_{10}\left( \dfrac{d}{10 \rm \,pc} \right)
$$
