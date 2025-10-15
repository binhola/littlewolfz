### The Postulates
To define a theory, we start with postulates. For Galilean (Newtonian) mechanics, they are:
1.  **Principle of Causality:** Cause precedes effect.
2.  **Principle of Relativity:** The laws of physics are identical in all inertial reference frames (frames moving at constant velocity relative to each other).
### Deriving the Transformation Laws
Consider two inertial frames $R(x, t)$ and $R'(x', t')$, with $R'$ moving at velocity $v$ relative to $R$.

The most general linear transformations consistent with:
*   The Principle of Relativity
*   Homogeneity of space and time
*   Isotropy of space

are given by:
$$
\begin{aligned}
x' &= \gamma(v) (x - vt) \\
t' &= \gamma(v) (t - \alpha v x)
\end{aligned}
$$
where $\alpha$ is a real number, and the function $\gamma(v)$ is to be determined. We can find it by demanding that these transformations form a **group**—the essence of the Principle of Relativity. The composition of two boosts must be equivalent to a single boost.

**Proof of Group Structure:**
Let's perform two successive transformations.
1.  $(x, t) \xrightarrow{v_1} (x_1, t_1)$
    $$
    \begin{aligned}
    x_1 &= \gamma(v_1) (x - v_1t) \\
    t_1 &= \gamma(v_1) (t - \alpha v_1 x)
    \end{aligned}
    $$

2.  $(x_1, t_1) \xrightarrow{v_2} (x_2, t_2)$
    $$
    \begin{aligned}
    x_2 &= \gamma(v_2) (x_1 - v_2 t_1) \\
    &= \gamma(v_2) \gamma(v_1) \left[ (x - v_1t) - v_2 (t - \alpha v_1 x) \right] \\
    &= \gamma(v_2) \gamma(v_1) \left[ (1 + \alpha v_1 v_2)x - (v_1 + v_2)t \right] \\
    &= \gamma(v_2) \gamma(v_1) (1 + \alpha v_1 v_2) \left[ x - \frac{v_1 + v_2}{1 + \alpha v_1 v_2} t \right]
    \end{aligned}
    $$

For this to be a pure boost with velocity $V$, we must have:
$$
x_2 = \gamma(V) (x - V t), \quad \text{where} \quad V = \frac{v_1 + v_2}{1 + \alpha v_1 v_2}
$$

Comparing the two expressions, we find the consistency condition:
$$
\gamma(V) = \gamma(v_1) \gamma(v_2) (1 + \alpha v_1 v_2)
$$
Substituting $V$ into the right-hand side and solving for $\gamma(v)$ reveals that the only solution satisfying the group property is:
$$
\gamma(v) = \frac{1}{\sqrt{1 - \alpha v^2}}
$$
Now, let's analyze the three physical cases for $\alpha$.

### The Three Cases for $\alpha$
1.  **$\alpha < 0$ ($\alpha = -1/\kappa^2$):**
    *   Velocity addition: $V = \frac{v_1 + v_2}{1 - v_1 v_2 / \kappa^2}$. This allows $V$ to become negative even for positive $v_1, v_2$, leading to a breakdown of temporal order.
    *   Time transformation: $\Delta t' = \gamma(v) (\Delta t + \frac{v}{\kappa^2} \Delta x)$. This can make $\Delta t' < 0$ even for $\Delta t > 0$, **violating causality**. This case is unphysical.

2.  **$\alpha > 0$ ($\alpha = 1/c^2$):**
    *   Here, $\gamma(v) = \frac{1}{\sqrt{1 - v^2/c^2}}$. This is the **Lorentz factor**.
    *   Velocity addition: $V = \frac{v_1 + v_2}{1 + v_1 v_2 / c^2}$. There is a universal speed limit $c$.
    *   Time transformation: $\Delta t' = \gamma(v) (\Delta t - \frac{v}{c^2} \Delta x)$. Causality is preserved as long as no signal travels faster than $c$ (time-like intervals). This is the domain of **Special Relativity**.

3.  **$\alpha = 0$:**
    *   This is the limit of the previous case where $c \to \infty$.
    *   $\gamma(v) = 1$.
    *   The transformations become the **Galilean transformations**:
    $$
    \begin{aligned}
    x' &= x - vt \\
    t' &= t
    \end{aligned}
    $$
    *   Velocity addition is simple: $V = v_1 + v_2$.

### The Geometry of Galilean Spacetime
The Galilean group is the isometry group of **Galilean Spacetime**. This spacetime is a smooth manifold, $T \times S$, where:
*   $T = (\mathbb{R})$ is the time axis (Euclidean line, $\mathbb{E}$).
*   $S = (\mathbb{R}^3, \delta)$ is space (Euclidean 3-space, $\mathbb{E}^3$).

We define canonical projections:
*   $\pi_T: T \times S \to T$ projects an event $(t, \vec{x})$ to its time $t$. The preimage $\pi_T^{-1}(t)$ is the set of all **simultaneous events** (a "time-slice").
*   $\pi_S: T \times S \to S$ projects an event $(t, \vec{x})$ to its spatial coordinate $\vec{x}$.

A key feature of Galilean spacetime is that while all observers agree on the time between two events ($\Delta t' = \Delta t$), they **cannot agree on a universal notion of "space at different times."** The set of events occurring at the same spatial point for one observer ($\pi_S^{-1}(\vec{x})$) is not the same for another moving observer.

This structure is elegantly described by a **fibre bundle**: Spacetime is a bundle where the base space is the time axis $T$, and the fibre at each time $t$ is the Euclidean space $S_t$. Galilean transformations tell us how to "connect" these different spatial fibres in a way that depends on the observer's state of motion.
