
Distribution function $f(\mathbf{r}, \mathbf{v}, t)$ of 7 independent parameters (number density)
$$
\begin{aligned}
\mathbf{r} &= x \hat i + y \hat j + z \hat k \\
\mathbf{v} &= v_x \hat i + v_y \hat j + v_z \hat k
\end{aligned}
$$
The coordinate ($\mathbf{r}, \mathbf{v}$) define particle state in the phase space
Volume in phase space $dV = d\mathbf{v}d\mathbf{r}$ 

The number density of particles in real space

$$
n(\mathbf{r}, t) = \int_{-\infty}^{\infty} d{\mathbf{v}} f(\mathbf{r}, \mathbf{v}, t)
$$

If $\hat f(\mathbf{r}, \mathbf{v}, t)$ is a normalized version of $f$ (probability of finding the particle in phase space volume)

$$
\int_{-\infty}^{\infty} d{\mathbf{v}} d{\mathbf{r}} f(\mathbf{r}, \mathbf{v}, t) = 1
$$

So $\hat f(\mathbf{r}, \mathbf{v}, t)d\mathbf{v}$ is the probability of finding the particle in between $\mathbf{v}$ and $\mathbf{v} + d\mathbf{v}$. The average speed is define as

$$
\bar v = \int v \hat f dv
$$
### Vlasov equation

$$
\dfrac{\partial f}{\partial t} + \vec{v} \cdot \nabla_r f + \vec{a} \cdot \nabla_vf = 0
$$
