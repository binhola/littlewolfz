---
tags:
  - physics
  - plasma
draft:
---
The non-uniform magnetic field creates from 2 Helmholtz coils

Lorentz force

$$
\mathbf{F} = q(\mathbf{E} + \mathbf{v} \times \mathbf{B})
$$
We only consider magnetic field $\mathbf{B}(r, \theta, z)$ pointed primarily in $z$-direction and whose magnitude varies along $z$. Let the field be axisymmetric, with $B_\theta = 0$ 
$$
\mathbf{F} = q\mathbf{v} \times \mathbf{B} = q 
\begin{pmatrix} 
\hat r & 0 & \hat z \\ 
v_r & v_\theta & v_z \\
B_r & 0 & B_z
\end{pmatrix} = q[v_\theta B_z \hat r + (B_r v_z - v_r B_Z)\hat \theta - v_\theta B_r \hat z]
$$

So, we know that

$$
\begin{aligned}
F_r &= v_\theta B_z \\
F_z &= -v_\theta B_r
\end{aligned}
$$
From newton second law, we balance $F_r$ with centripetal force:

$$
F_r = v_\theta B_z = -\dfrac{m v_\theta^2}{r} 
$$
So,

$$
r = -\dfrac{mv_\theta}{B_z}
$$
From electromagnetism, we know that $\nabla \cdot B = 0$:

$$
\dfrac{1}{r} \dfrac{\partial(r B_r)}{\partial r} + \dfrac{\partial B_z}{\partial z} = 0
$$

Therefore,

$$
B_r = -\dfrac{r}{2} \dfrac{\partial B_z}{\partial z} = \dfrac{m v_\theta}{2B_z} \dfrac{\partial B_z}{\partial z}
$$

Thus,

$$
F_z = -\dfrac{m v_\theta^2}{2} \dfrac{1}{B_z} \dfrac{\partial B_z}{\partial z}
$$

We define the magnetic moment of the gyrating particle to be:

$$
\mu \equiv \dfrac{mv_\theta^2}{2B_z} = \rm const
$$

Thus,

$$
F_z = -\mu \dfrac{\partial B_z}{\partial z}
$$

Consider a particle with $v_\theta = v_{\perp0}$ and $v_z = v_{\parallel0}$ at the mid-plane,  $v_\theta = v'_{\perp}$ and $v_z = 0$ at its turning point. Let the field at the mid-plane be $B_0$ and the turning point be $B'$. The invariance of $\mu$ yields

$$
\dfrac{mv_{\perp0}^2}{2 B_0} = \dfrac{m'v_{\perp}^2}{2 B'}
$$
And conservation of energy requires

$$
v_{\perp 0}^2 + v_{\parallel0}^2 = v_{\perp}^2 = v_0^2
$$

Therefore,

$$
\dfrac{B_0}{B'} = \dfrac{v_{\perp0}^2}{v_\perp^2} = \dfrac{v_{\perp0}^2}{v_0^2} = \sin ^2 \theta
$$

Particles with smaller $\theta$ mirror in regions of higher $B$. If $\theta$ is too small, $B'$ exceeds $B_{\rm max}$, then the particles do not mirror at all.

Replace $B'$ by $B_{\rm m}$, given

$$
\sin^2 \theta_m = \dfrac{B_0}{B_m} = \dfrac{1}{R_m}
$$

where $R_m$ is the *mirror ratio* define the boundary of a region in velocity space in the shape of a cone, called a *loss cone*. Particle flying in this cone is not confined




