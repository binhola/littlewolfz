---
tags:
  - physics
  - SMS
---
### A- Statistical and Systematic Uncertainty

A length measurement device has an input dynamic range covering $\ell : 10 \, \text{cm to } 10 \, \text{m}$, a statistical uncertainty $\sigma_{\text{stat}} = 10 \, \text{mm}$ and a relative systematic uncertainty $\sigma_{\text{sys}}/\ell = 1\%$.

1. Compute the overall absolute and relative uncertainty for a single measurement of a length $\ell$ for $\ell \sim 0.1 \, \text{m}, 1 \, \text{m}, 10 \, \text{m}$.

The device is used for making repeated measurement of the same length $N$ times, $\ell_k$, $k = 1 \dots N$, with the aim of decreasing the overall measurement uncertainty.

2. What would be the best estimate $\hat{\ell}$ of the measured length using the $N$ individual measurements?  
Determine also the corresponding statistical and systematic uncertainties.

3. Determine the overall uncertainty on $\hat{\ell}$ for $\ell \sim 0.1 \, \text{m}, 1 \, \text{m}, 10 \, \text{m}$, for $N = 20$ measurements.

4. Determine the value of $N$ for which the statistical error becomes negligible compared to the systematic error $\epsilon_{\text{stat}} \lesssim \epsilon_{\text{sys}}/10$.
$$\sigma_{tot}^2 = \sigma_{stat}^2 + \sigma_{sys}^2$$
$$\sigma_{stat} = \sigma_{stat}/\sqrt{N}$$

$$\sigma_{\text{stat}}/\sqrt{N} \lesssim \sigma_{\text{sys}}/10 \quad \implies N \gtrsim \left(\dfrac{10\sigma_{stat}}{\sigma_{sys}}\right)^2 = (10/l)^2$$

---

### B- Uncertainties when Combining Measurements

1. Consider a quantity $X$ measured with the uncertainty $\epsilon_X$. Considering the measurement errors as a random variable with mean zero and variance $\xi_X^2$, determine the uncertainty $\epsilon_Y$ on $Y = 4X$.
What result would you get if you consider $Y = X + X + X + X$, as a sum of 4 independent quantities?

2. Determine also the uncertainty on $\epsilon_Z$ on $Z = X^3$. What result would you get if you consider $Z = X \times X \times X$ as a product of three independent quantities?

We assume that we have measured the four sides of a square, getting the following results:

$$ a_1 = 23.9 \pm 0.2 \, \text{m} \quad a_2 = 23.8 \pm 0.4 \, \text{m} \quad a_3 = 24.05 \pm 0.1 \, \text{m} \quad a_4 = 24.3 \pm 0.4 \, \text{m} $$

4. Compute the perimeter $P$ of the square and its uncertainty $\epsilon_P$.

5. Assuming that the figure corresponds to a perfect square, determine the length of the square side $a$, and its uncertainty.

6. Compute also the perimeter $P$ of the perfect square, its uncertainty $\epsilon_P$, as well as the surface $S$ with its uncertainty $\epsilon_S$.

**Solution:**
$\epsilon_Y = \left| \dfrac{dY}{dX} \right|\epsilon_X$
$\epsilon_Y^2 = 4\epsilon_X^2 \implies \epsilon_Y = 2\epsilon_X$ 
1. $\mu_Y = 0$ and $\epsilon_Y = 2\epsilon_X$
2. for $Z = X^3$, $\epsilon_Z = 3X^2\epsilon_X$
	for $Z= X \times X \times X$, $\epsilon_Z = \sqrt{3}X^2 \epsilon_X$ 
4. $$P = a_1 + a_2 + a_3 + a_4 = 96.05$$$$\epsilon_P = \sqrt{\epsilon_1^2 + \epsilon_2^2 + \epsilon_3^2 + \epsilon_4^2} = 0.61$$
5. $$a = \dfrac{a_1+a_2+a_3+a_4}{4}=24.01$$
$$\epsilon_a = \dfrac{1}{4} \sqrt{\epsilon_1^2 + \epsilon_2^2 + \epsilon_3^2 + \epsilon_4^2} = 0.15$$
6. $P=4a = 96.05$ and $\epsilon_P = 4\epsilon_a = 0.61$
Surface 
$$S = a^2 = 567.48$$
$$\epsilon_S = 2a\epsilon_a = 7.203$$

