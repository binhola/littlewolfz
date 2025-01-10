
Friedmann equations are two equations derived from Einstein field equations with the Cosmological principles:
### 1. Expansion rate equation
$$
\left(\dfrac{\dot{a}}{a} \right)^2 = \dfrac{8\pi G}{3c^2} \epsilon + \dfrac{\Lambda c^2}{3} - \dfrac{kc^2}{R^2(t)}
$$
### 2. Acceleration equation
$$
\dfrac{\ddot a}{a} = - \dfrac{4\pi G}{3c^2} ( \epsilon + 3p ) + \dfrac{\Lambda c^2}{3}
$$
### 3. Continuity equation
By taking the derivative of the equation 1 and combine with equation 2:
$$
\dot\epsilon + 3 H(t)\big(\epsilon + p ) = 0
$$
##### Remarks
1. Equation 3 is *not* independent of equation 1 and 2
2. $k$ does not appear in equation 2, no dynamics induced by geometry
3. There are 3 unknowns: $\epsilon,\, p, \, a$ 
So, we need additional information. We need to introduce equation of state

### 4. Equation of state
$$
p_i(t) = w_i(t) \epsilon_i(t)
$$
for each fluid denoted by $i$.
For the fluids that do not change the nature with time
$$
w_i(t) = w_i = \text{const}
$$
## Solutions of 4 equations for different fluids 
### Radiation (ultra relativistic species)
Photons and all light particles (neutrino)
$$
p_r = \dfrac{1}{3} \epsilon_r \quad \text{where} \quad w_r = \dfrac{1}{3}
$$
### Cold matter
Any species with energy density dominated by rest mass energy density
$$
E = \gamma mc^2 = \dfrac{1}{\sqrt{1-v^2/c^2}} mc^2 \approx mc^2 + \dfrac{1}{2}mv^2
$$
Energy density for the fluid
$$
\epsilon = \dfrac{NE}{V} = n\gamma mc^2 = nmc^2 + \dfrac{1}{2}nm\sigma_v^2
$$
where $\sigma_v$ is the velocity dispersion of the system
Pressure
$$
p = nk_BT \quad \text{and} \quad \dfrac{3}{2}k_BT = \dfrac{1}{2} m\sigma_v^2
$$
We have 
$$
p = \dfrac{1}{3} nm\sigma_v^2
$$
For cold matter we have
$$
p_m << \epsilon_m \quad \Rightarrow \quad p_m = 0 \quad \Rightarrow \quad w_m = 0
$$
### Solve the continuity equation 
Having the equation of state relating energy density and pressure, we can try to solve the continuity equation for constant $w_i$ of a fluid with unchanged nature over time.
$$
\begin{aligned}
\dot\epsilon_i + 3H(\epsilon_i + p_i) &= 0 \\
\dot\epsilon_i + 3\dfrac{\dot a}{a}(\epsilon_i + w_i \epsilon_i) &= 0 \\
\dfrac{d\epsilon_i}{\epsilon_i} &= - 3(1 + w_i)\dfrac{da}{a} 
\end{aligned}
$$
Finally, we have
$$
\epsilon_i(t) = \epsilon_0\, a^{-3(1+w_i)}
$$
- Radiation : $w_r = \dfrac{1}{3} \quad \Rightarrow \quad \epsilon_r \sim a^{-4}$
- Cold matter : $w_m = 0 \quad \Rightarrow \quad \epsilon_m \sim a^{-3}$

### Cosmological constant
$$
\left(\dfrac{\dot{a}}{a} \right)^2 = \dfrac{8\pi G}{3c^2} (\epsilon_r+\epsilon_m + ...) + \dfrac{\Lambda c^2}{3} - \dfrac{kc^2}{R^2(t)}
$$
Given that $\Lambda$ appears in both Friedmann equations, we can interpret it as a "stuff" (can be a fluid or anything) associated with energy density
$$
\left(\dfrac{\dot{a}}{a} \right)^2 = \dfrac{8\pi G}{3c^2} \left(\epsilon_r+\epsilon_m + ...+ \dfrac{\Lambda c^4}{8\pi G}\right) - \dfrac{kc^2}{R^2(t)}
$$
And we define
$$
\epsilon_\Lambda = \dfrac{\Lambda c^4}{8\pi G} = \text{const}
$$
Continuity equation of $\epsilon_\Lambda$
$$
\dot\epsilon_\Lambda + 3H(\epsilon_\Lambda + p_\Lambda) = 0
$$
We have 
$$
p_\Lambda = -\epsilon_\Lambda \quad \Rightarrow \quad w_\Lambda = -1
$$
##### Remark
$$
\dfrac{\ddot a}{a} = -\dfrac{4\pi G}{3c^2} \sum_i (\epsilon_i + 3p_i)
$$
This model of the universe can only accelerates when 
$$
\epsilon_i + 3p_i < 0 \quad \Rightarrow \quad w_i < -1/3
$$
Now, we can rewrite the equation 1 as
$$
H^2(t) = \dfrac{8\pi G}{3c^2} \epsilon_T - \dfrac{kc^2}{R^2(t)}
$$
where $\epsilon_T = \epsilon_m + \epsilon_r + \epsilon_\Lambda$

### The concordance model of Cosmology: $\Lambda$CDM Model
##### Friedmann equations
1. Expansion rate equation:
$$
\left(\dfrac{\dot{a}}{a} \right)^2 = \dfrac{8\pi G}{3c^2} \left(\epsilon_r+\epsilon_m + \epsilon_\Lambda + ...\right) - \dfrac{kc^2}{R^2(t)}
$$
2. Acceleration equation:
$$
\dfrac{\ddot a}{a} = - \dfrac{4\pi G}{3c^2} ( \epsilon_m - 2\epsilon_\Lambda )
$$

### Critical Density
From equation 1, we know that
$$
H^2(t) = \dfrac{8\pi G}{3c^2} \epsilon_T - \dfrac{kc^2}{R^2}
$$
Thus
$$
kc^2 = R^2(t) \left[ \dfrac{8\pi G}{3c^2} \epsilon_T - H^2(t) \right] = R^2_0 \left[ \dfrac{8\pi G}{3c^2} \epsilon_{T,0} - H^2_0 \right]
$$
- $k = 0$, we obtain the critical density as
$$
\epsilon_c = \dfrac{3H_0^2c^2}{8 \pi G}
$$
- $k = -1$, we obtain
$$
R_0^2 = \dfrac{-c^2}{H_0^2 
\left(\dfrac{\epsilon_{T,0}}{\epsilon_c} -1\right)} = \dfrac{R_{H_0}^2}{1- \dfrac{\epsilon_{T,0}}{\epsilon_c}}
$$
Therefore $1 - \epsilon_{T, 0} / \epsilon_c <0$ , as the result
$$
\epsilon_{hyperbolic} < \epsilon_c
$$
- $k = 1$, we obtain
$$
R_0^2 = \dfrac{R_{H_0}^2}{\dfrac{\epsilon_{T,0}}{\epsilon_c} -1}
$$
Therefore, 
$$
\epsilon_{spherical} > \epsilon_c
$$
### Reduction form of Friedmann equations
Equation 1 can be written as
$$
H^2(t) = H_0^2 \dfrac{\epsilon_T}{\epsilon_c} - \dfrac{kc^2}{R^2(t)}
$$
where $\epsilon_c = \dfrac{3c^2H_0^2}{8 \pi G}$ 

Define the ratio of energy density as 
$$
\Omega_T(t) = \dfrac{\epsilon_T(t)}{\epsilon_c} = \dfrac{\epsilon_m(t) + \epsilon_r(t)+\epsilon_\Lambda}{\epsilon_c} = \Omega_m(t) + \Omega_r(t) + \Omega_\Lambda
$$
Continuity equation and equation of states:
$$
\Omega_i(t) = \Omega_{i, 0} a^{-3(1+w_i)}
$$
Further reduction
$$
H^2(t) = H_0^2 [\,\Omega_T(t) + \Omega_k(t) \,] \quad \text{where} \quad \Omega_k(t) = - \dfrac{kc^2}{R^2(t) H_0^2} = -k \left( \dfrac{R_{H_0}}{R(t)} \right)^2
$$
Finally, we reduce to 
$$
H^2(t) = H^2_0 E^2(t)
$$
##### Remarks
1. $k \rightarrow$ Geometry, so $\Omega_k$ is **not** an energy density ratio
2. $\Omega_k$ depends on the geometry $k$ and how much the radius of curvature $R(t)$ different from the Hubble radius $R_{H_0}$.  
3. At present time
$$
\Omega_{T, 0} + \Omega_{k, 0} = 1
$$
- $\Omega_{T, 0} = 1 \quad \rightarrow \quad \Omega_{k,0} = 0 \quad \text{Euclidean}$ 
- $\Omega_{T, 0} < 1 \quad \rightarrow \quad \Omega_{k,0} > 1 \quad \text{Spherical}$ 
- $\Omega_{T, 0} > 1 \quad \rightarrow \quad \Omega_{k,0} < 1 \quad \text{Hyperbolic}$ 

Equation 2 can also be written as
$$
\dfrac{\ddot a}{a} = -\dfrac{1}{2} H_0^2 \sum_i \Omega_i(t) (1+3w_i)
$$
### Cosmological Eras
We know that
$$
\begin{cases}
\Omega_\Lambda &\text{const} \\
\Omega_m &\sim a^{-3} \\
\Omega_r &\sim a^{-4} 
\end{cases}
$$
From measurement of CMB:
$$
\begin{cases}
\Omega_\Lambda & \sim 0.7 \\
\Omega_{m,0} & \sim 0.3 \\
\Omega_{r,0} & \sim 8 \times 10^{-5}
\end{cases}
$$
#### Equalities: the time of equivalent energy density
1. Matter - radiation equality:
$$
\Omega_m(t_{\rm eq}) = \Omega_r(t_{eq})
$$
Thus
$$
\Omega_{m,0} a_{eq}^{-4} = \Omega_{r, 0} a_{eq}^{-3}
$$
So
$$
a_{eq} = \dfrac{\Omega_{m,0}}{\Omega_{r,0}} \sim 2.7 \times 10^{-4} \quad \Rightarrow \quad z_{eq} \sim 3749 
$$
This is before the time of CMB $z_{CMB} \sim 1100$
2. Matter - $\Lambda$ equality
$$
\Omega_m(t_{\Lambda m}) = \Omega_\Lambda(t_{\Lambda m})
$$
So
$$
a_{\Lambda m} = \left(\dfrac{\Omega_{m,0}}{\Omega_\Lambda} \right)^{-1/3} = 0.75 \quad \Rightarrow \quad z_{\Lambda m} = 0.33
$$




