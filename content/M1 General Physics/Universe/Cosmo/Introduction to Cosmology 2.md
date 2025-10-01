---
title: 2. Hubble Lemaitre law
---

Given the FLRW metric and the geometry of universe, there are two unknowns that we need to solve: $k$ and $a(t)$

We can comeback to define some of observational physics that we know: Hubble-Lemaitre law and Redshift

## Hubble - Lemaitre Law

From the Cosmological Principle, we obtain the FLRW metric describing the geometry of the universe. 

We define the physical distance $D(t)$ and we know that it links to our pre-defined comoving distance $\chi = \int_0^{\chi} d\chi'$ through the scale factor $a(t)$:
$$
D(t) = a(t) \chi 
$$
Take the derivative, knowing that $\chi$ does not change when the objects do not possess their own motions:
$$
\dfrac{d D(t)}{dt} = \dfrac{d a(t)}{dt} \chi = \dot{a} \chi = \dfrac{\dot{a}}{a} D(t)
$$
So we recover the H-L law:
$$
\vec{v(t)} = H(t) \vec{D(t)}
$$
where $$H(t) = \dfrac{\dot{a}}{a}$$
By definition
$$
H_0 \equiv \dfrac{\dot{a(t_0)}}{a(t_0)} = \dfrac{\dot{a_0}}{a_0} = \dot{a_0}
$$
## Redshift
By definition, we have
$$
1 + z =\dfrac{\lambda_{\rm obs}}{\lambda_{\rm emit}}
$$
We know that, when the photon follows the geodesis, it is a light-like interval (only consider the radial direction):
$$
ds^2 = 0 \quad \Rightarrow \quad cdt = a(t) d\chi
$$
So 
$$
\chi = \int_0^{\chi} d\chi' = \int_0^{\chi} \dfrac{cdt}{a(t)} = c \int_{t_{e}}^{t_0} \dfrac{dt}{a(t)}
$$
Consider a second photon leaves the source at $t_{e} + \delta t_{e}$ and reaches us at $t_0 + \delta t_0$
The comoving distance is still the same
$$
\chi = c \int_{t_{e}}^{t_0} \dfrac{dt}{a(t)} = c \int_{t_{e} + \delta t_e}^{t_0 + \delta t_0} \dfrac{dt}{a(t)}
$$
Expand the integral, we have
$$
 \int_{t_{e}}^{t_e + \delta t_e} \dfrac{dt}{a(t)} = \int_{t_0 }^{t_0 + \delta t_0} \dfrac{dt}{a(t)}
$$
Let call $F(t) = \int_t \dfrac{dt}{a(t)}$

Thus
$$
F(t_e + \delta t_e) - F(t_e) = F(t_0 + \delta t_0) - F(t_0)
$$
We do the Taylor expansion 
$$
F(t + \delta t) = F(t_a) + \dfrac{\partial F(t)}{\partial t}\Big|_{t=t_a} \delta t_a
$$
So we have
$$
\dfrac{\delta t_e}{a(t_e)} = \dfrac{\delta t_0}{a(t_0)}
$$
Naturally take $\delta t_0 = \dfrac{1}{\nu_0}$ and $\delta t_e = \dfrac{1}{\nu_e}$ and we know that $c = \lambda \nu$

So we have 
$$
\dfrac{\lambda_0}{\lambda_{e}} = \dfrac{a(t_0)}{a(t_e)} = \dfrac{1}{a(t)}
$$
Finally, we obtain
$$
1+z = \dfrac{1}{a(t)}
$$
## Natural units
1. Hubble time
$$
t_{H_0} = \dfrac{1}{H_0} 
$$
2. Hubble radius
$$
R_{H_0} = c t_{H_0} = \dfrac{c}{H_0}
$$

