---
title: 4. Models of universe
draft:
---
**Friedmann equation**
1. Expansion rate equation
$$
H^2(t) = H_0^2 E^2(a) \quad \text{where} \quad E^2(a) = \sum_i \Omega_i(a) + \Omega_k(a)
$$
2. Acceleration equation
$$
\dfrac{\ddot a}{a} = -\dfrac{1}{2} H_0^2 \sum_i \Omega_i(a) (1+3w_i)
$$
**Continuity equation:** 
$$\dot \epsilon_i + 3H(t)(\epsilon_i + p_i) = 0$$
**Equation of state**:
$$
p_i(t) = w_i \epsilon_i(t)
$$
$$
w_m = 0 \quad w_r = \dfrac{1}{3} \quad w_\Lambda = -1
$$
## Einstein - de Sitter universe
**Definition**: The matter-only universe with critical energy density

The universe at critical energy density is a flat universe with Euclidean geometry:
$$
\Omega_{k, 0} = 0
$$
So 
$$
\Omega_{T,0} = 1-\Omega_{k, 0} = 1
$$
In this case
$$
E^2(a) = \Omega_m(a) = \Omega_{m, 0} a^{-3} = a^{-3}
$$
From Friedmann equation 1:
$$
H^2(t) = H^2_0 E^2(a) = H_0^2 a^-3 = \left(\dfrac{\dot a}{a}\right)^2
$$
So 
$$
\sqrt a \, da = H_0 dt \quad \Rightarrow \quad \dfrac{2}{3}a^{3/2} = H_0t + C
$$
At $t=0$, the beginning of the universe - Big Bang, the scale factor is assumed to be $a(t=0)=0$. Therefore, $C=0$, we obtain:
$$
a = \left(\dfrac{t}{t_0} \right)^{2/3} \quad \text{where} \quad t_0 = \dfrac{2}{3} t_{H_0} \quad\text{is the present day time of EdS universe}
$$
## Radiation only universe with critical energy density
Similar to the previous argument, we have
$$
E^2(a) = \Omega_r(a) = \Omega_{r,0} a^{-4} = a^{-4}
$$
Solve this case, we obtain:
$$
a = \left( \dfrac{t}{t_0} \right)^{1/2} \quad \text{where} \quad t_0 = \dfrac{1}{2} t_{H_0} \quad \text{is the present day time in this universe}
$$
## De-Sitter universe
**Definition**: Cosmo-constant only universe with critical energy density 

We know $\Omega_{k,0} = 0$ and $\Omega_\Lambda =1$. So $E^2(a) = 1$
$$
H^2(t) = \left( \dfrac{\dot a}{a}\right)^2 = H_0^2
$$
So 
$$
\ln(a) = H_0 t + C
$$
In de-Sitter universe, when $a \rightarrow 0$ then $t \rightarrow -\infty$. So there is no Big Bang, as it is very far in the past (divergence solution).

We will use the convention $a(t_0) = 1$
$$
H_0 t_0 + C = 0 \quad \Rightarrow \quad C = - \dfrac{t_0}{t_{H_0}}
$$
Thus,
$$
a(t) = e^{\dfrac{t-t_0}{t_{H_0}}}
$$

## $\Lambda$CDM universe (current universe model)

Let put a relaxed condition $|\Omega_{k,0}| \leq 10^{-3}$, enough to be small and negligible 
From the measurement of Planck and other experiments, we can approximately choose
$$
\Omega_{m,0} \sim 0.3 \quad \Omega_{\Lambda} \sim 0.7 \quad \Omega_{r,0} \sim 8 \times 10^{-5}
$$
Thus,
$$
E(a) = \sqrt{\Omega_{m,0} a^{-3} + \Omega_{r,0} a^{-4} + \Omega_\Lambda}
$$
Friedmann equation gives
$$
\dfrac{da}{a E(a)} = H_0 dt
$$
There is no analytical solution!

## Age of the universe
We have 
$$
dt = t_{H_0} \dfrac{da}{a E(a)}
$$
In principle, the age of the universe at an arbitrary time t is expressed as
$$
t = \int_0^t dt' = t_{H_0} \int_0^{a(t)} \dfrac{da}{aE(a)}
$$
Given that the integral on the right hand side is well-defined, meaning provided there exists a finite time in the past, at the Big Bang $t=0$ at which $a(t=0) =0$.

Present age of the universe is expressed as
$$
t_0 = t_{H_0} \int_0^1 \dfrac{da}{aE(a)}
$$
#### General Euclidean universe filled with "stuff" $\alpha$ with constant $w_\alpha$
From equation of state, we have
$$
\Omega_\alpha(a) = \Omega_{\alpha, 0} \, a^{-3(1-w_\alpha)}
$$
We know 
$$
\Omega_{k,0} = 0
$$
So 
$$
E^2(a) = a^{-3(1-w_\alpha)}
$$
The present age of this universe
$$
t_0 = t_{H_0} \int_0^1 \dfrac{da}{a \, a^{3/2(1-w_\alpha)}} = t_{H_0} \int_0^1 a^{\dfrac{1+3w_\alpha}{2}} da
$$
##### Remarks
1. This integral diverges at $a \rightarrow 0$ for all $\dfrac{1+3w_\alpha}{2} \leq -1$
	No Big Bang for all universes which were dominated in the past by a fluid with an equation of state $w_\alpha \leq -1$
2. For $-1 < w_\alpha \leq 1/3$, the second Friedmann equation implies an accelerating universe.

## Distance in cosmology

### Radial distance 
$$
D_{phys} = a(t) D_c \quad \text{where} \quad D_c \equiv \text{radial comoving distance}
$$
Obviously, with photon $ds = 0$
$$
D_c = \int_0^{D_c} d\chi = c \int_{t_e}^{t_0} \dfrac{dt}{a(t)}
$$
We have
$$
\dfrac{dt}{a(t)} = \dfrac{1}{a(t)} \dfrac{dt}{da} da = \dfrac{da}{\dot a a} \quad \text{where} \quad \dot a = H a = aH_0 E(a)
$$
So
$$
D_c = \dfrac{c}{H_0} \int_{a(t)}^1 \dfrac{da}{a^2E(a)} = R_{H_0} \int_{a(t)}^1 \dfrac{da}{a^2E(a)}
$$
We have 
$$
a(t) = \dfrac{1}{1+z} \quad \Rightarrow \quad \dfrac{da}{a} = -\dfrac{dz}{1+z}
$$
So
$$
D_c = R_{H_0} \int_0^z \dfrac{dz}{E(z)}
$$
The physical radial distance of a galaxy at present day:
$$
D_{phys}(t_0) = a_0 D_c(z) = D_c(z)
$$
The physical radial distance at the time of emission
$$
D_{phys}(t_0) = a(t_e) D_c(z) = \dfrac{D_c(z)}{1+z}
$$




