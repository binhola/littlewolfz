---
tags:
  - physics
  - SMS
---
Every measurement has uncertainty

$$
G = g_m + \epsilon 
$$

where 
- $\epsilon$ is the *absolute uncertainty*
- $g_m$ is the true value
- $\dfrac{\delta G}{G} = \dfrac{\epsilon}{g_m} \equiv$ *relative uncertainty*

Measurement results can be described as a random variable with its PDF characterized by the true value and the measurement process itself.

If the measurement is unbiased

$$
\langle G \rangle = g_m \quad \text{if} \quad n_{\rm measure} \rightarrow \infty 
$$

### Systematics and statistical uncertainty

$$
G = g_m + \epsilon_{\rm stat} + \epsilon_{sys}
$$

where 
- $\epsilon_{\rm stat}$ is the statistical uncertainty (random distribution of repeating measurements)
- $\epsilon_{\rm sys}$ is the systematic uncertainty (uniquely for a given measurement, unchange when repeating)

1. Systematic errors: originate from inexact methods and faulty instruments
2. Statistical errors: 
## Distribution 

### Poisson distribution

$$
f(k, \mu) = \dfrac{\mu^k e^{-\mu}}{k!} \quad \text{where} \quad k = 0, 1,2, ...
$$
- $E(k) = \mu$
- $Var(k) = \mu$

### Gaussian distribution

$$
f(r, \mu, \sigma) = \dfrac{1}{\sigma \sqrt{2\pi}} e^{-\dfrac{(r-\mu)^2}{2\sigma^2}} \quad \text{where} \quad -\infty < r < \infty
$$

- $E(r) = \mu$
- $Var(r) = \sigma^2$ 

## Error propagation 

1. Addition rule: $z = x + y$

$$
\sigma_z^2 = \sigma_x^2 + \sigma_y^2
$$

2.  Quotient rule: $z = x \times y$

$$
\left(\dfrac{\sigma_z}{z} \right)^2 = \left(\dfrac{\sigma_x}{x} \right)^2 + \left(\dfrac{\sigma_y}{y} \right)^2
$$

3. Power rule: $z = x^n$

$$
\sigma_z = |n|x^{n-1} \sigma_x
$$

4. Factor rule: $z = Cx$

$$
\sigma_z = |C| \sigma_x
$$
