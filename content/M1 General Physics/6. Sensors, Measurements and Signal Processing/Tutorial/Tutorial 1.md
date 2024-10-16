---
tags:
  - physics
  - SMS
---
### A. Temperature Sensor Response

1. Perform a second-order Taylor series expansion of the temperature-resistance relationship $R(T)$ at 300 K, 350 K, and 400 K.  
   $$ 
   R(T) = R_{T_0} \exp \left( \frac{b (T - T_0)}{T T_0} \right)
   $$
   where $T_0 = 300 \, K$, $b = 3000 \, K$, and $R_{T_0} = 1000 \, \Omega$.

2. Design a circuit using the sensor to produce a voltage output $u(T)$. Find the transfer function.

3. At 300 K, set the sensor output to 3V. Calculate the input-output dynamic range (in dB) for temperatures between 200 K and 400 K.

**Solution:**

Taylor expansion: 

$$
f(x) = f(x_0) + f'(x_0)(x-x_0) + f''(x_0)(x-x_0)^2/2 + O(x^3)
$$
Therefore,

$$
R(T) = R_{T_0} + \dfrac{b}{T_0^2} R_{T_0} (T-T_0) + \left( \dfrac{b^2}{2T_0^4} - \dfrac{b}{T_0^3} \right) R_{T_0} (T-T_0)^2
$$
Input the number 

$$
R(T) = R_{T_0} + \dfrac{R_{T_0}}{30} (T-T_0) + \dfrac{R_{T_0}}{2250}(T-T_0)^2

$$
- At $T = 300 \, \rm K \quad \Rightarrow \quad ST = 0 \, \Omega$
- At $T = 350 \, \rm K \quad \Rightarrow \quad ST \simeq 1111.11 \, \Omega$
- At $T = 400 \, \rm K \quad \Rightarrow \quad ST \simeq 4444.44 \, \Omega$

---

### B. Poisson Distribution

We assume that the emission rates of particles for a source, (a radioactive source for example) follows the Poisson distribution. A particle detector is placed at a fixed distance of the source. Assuming an average detection rate of 4 particles per second, compute the probabilities for the following events :

1. Calculate the probability of detecting 0 particles in 1 second.
2. Calculate the probability of detecting 0 particles in 2 seconds.
3. Determine the probability of detecting between 3 and 5 particles in 1 second.

**Solution:**

Poisson distribution: $f(k, \mu) = \dfrac{\mu^k e^{-\mu}}{k!}$ . We have that $\mu = 4 \rm \, particles/s$
1. $k = 0 \rm \, particles/s \quad \Rightarrow \quad f(0, 4) = e^{-4} \simeq 1.83 \%$ 
2. $f(0, 8) = e^{-8} = 0.033 \%$
3. $f(3,4) + f(4,4) + f(5,4) = 54.7 \%$
---

### C. Gaussian Distribution

Given the following values drawn from a normal (Gaussian) distribution:

$$
\{ 4.1776, -2.3447, 5.8573, 9.4942, 0.2329, 6.4320, 8.0160, -3.3749, -2.7639, 5.2846 \}
$$

Compute the unbiased estimators for the mean and variance.

**Solution:**

Mean: 
$$ 
E(x) = \dfrac{1}{n} \sum_{i=0}^n x_i = 3.1
$$

Std:

$$
\sigma = \sqrt{\dfrac{1}{n-1}\sum_{i=0}^n(x_i -\mu)^2} = 4.76
$$

---

### D. Gravitational Acceleration Measurement

The oscillation period of a pendulum is given by:

$$
T = 2\pi \sqrt{\frac{\ell}{g}}
$$

Determine $g$ and its uncertainty for $T = 1.936 \pm 0.004 \, \text{s}$ and $\ell = 92.95 \pm 0.10 \, \text{cm}$.

**Solution:**

$$
g = 4\pi^2 \dfrac{l}{T^2} = 18.81
$$

We have

$$
\sigma_g^2/g^2 = ( \sigma_l^2/l^2 + 4 \sigma_T^2/T^2)
$$
Thus,

$$
\sigma_g = g \sqrt{\left( \dfrac{\sigma_l}{l} \right)^2 + \left( 2\dfrac{\sigma_T}{T} \right)^2} = 0.08 
$$
So,
$$
\epsilon_g = \dfrac{\sigma_g}{g} = 0.4\%
$$

---

### E. Parallel Resistor Assembly

Given two resistors, $R_1 = 1800 \, \Omega$ and $R_2 = 150 \, \Omega$, in parallel:

1. Calculate the equivalent resistance $R_{\text{eq}}$ and its relative and absolute uncertainties, assuming a 10% precision for both resistors.
2. Determine which resistor to replace with a 1% precision resistor to minimize the uncertainty in $R_{\text{eq}}$.

**Solution:**
1. 

$$
\sigma(1/R) = R^{-2}\sigma(R)
$$
For parallel circuit, we have
$$
\dfrac{1}{R_{eq}} = \dfrac{1}{R_1} + \dfrac{1}{R_2}
$$
So, $R_{eq} = 138.46 \, \Omega$
We have 
$$
\sigma(R_{eq}) = \sqrt{R_{eq}^2 \left[ \left(\dfrac{1}{R_1} \dfrac{\sigma(R_1)}{R_1}\right)^2 + \left(\dfrac{1}{R_2} \dfrac{\sigma(R_2)}{R_2}\right)^2\right]} = \sqrt{R_{eq}^2 \left[ \left(\dfrac{1}{R_1} \epsilon(R_1) \right)^2 + \left(\dfrac{1}{R_2} \epsilon(R_2) \right)^2 \right]} = 0.093
$$
Therefore, the absolute uncertainty
$$
\epsilon(R_{eq}) = 0.066\%
$$
2. Because $R_1 > R_2$ so minimizing the uncertainty of $R_2$ will reduce the uncertainty of $R_{eq}$ 


---

### F. Electrical Quantities and Uncertainties

For $R = 5 \pm 0.1 \, \text{k}\Omega$, $C = 20 \pm 1 \, \mu\text{F}$, and $L = 10 \pm 0.1 \, \text{mH}$. The true impedances are randomly distributed around the central value (gaussian). Compute average and standard deviation of the following quantities:
1. Compute the time constant $\tau = RC$.
2. Compute the time constant $\tau = \frac{L}{R}$.
3. Calculate the resonance frequency $\nu_0 = \frac{1}{2\pi} \sqrt{\frac{1}{LC}}$.

**Solution**:
1. $$\tau = RC = 5 \times 20 = 100 \, \rm ms $$
$$\sigma_\tau = \tau \sqrt{\sigma_R^2/R^2 + \sigma_C^2/C^2} = 5.38 \, \rm ms$$
So,
$$
\tau = 100 \pm 5.38 \, \rm ms
$$
2. $$ \tau = L/R = 2 \rm \, \mu s$$
$$ \sigma_\tau = \tau \sqrt{\sigma_L^2/L^2 + \sigma_R^2/R^2} = 0.045 \, \rm \mu s$$
3. $$\nu_0 = \frac{1}{2\pi} \sqrt{\frac{1}{LC}} = 355.88 \, \rm Hz$$
$$
\sigma_\nu = \nu_0/2 \sqrt{\sigma_L^2/L^2 + \sigma_C^2/C^2} = 9.07 \, \rm Hz
$$

---

### G. Sensor Linearity

The following calibration data is provided:

| Input (E)  | 1    | 2    | 3    | 4    | 5    | 6    | 7    | 8    | 9    | 10   |
| ---------- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| Output (S) | 0.45 | 1.06 | 1.37 | 2.01 | 2.56 | 3.12 | 3.42 | 3.85 | 4.49 | 5.12 |

1. Determine the best linear fit assuming negligible input error and constant error $\sigma_S$ in the output.
2. Compare with the given specification:  
   $$
   S = 0.5044E + 0.0293
   $$
**Solution:**
1. $$\mathbf{S} = \mathbf{A}\mathbf{X}$$ To find $\mathbf{X}$:
$$
\mathbf{X} = \mathbf{(A^\top A)^{-1}AS}
$$

