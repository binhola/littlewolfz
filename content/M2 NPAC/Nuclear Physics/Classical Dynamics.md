### Theory of local laws
Physical theories start from local laws:
1. Newton's 2nd law (ODEs)
2. Snell-Descartes laws
3. Maxwell's equations (differential laws of EM)
4. Thermodynamics laws

For Newtonian mechanics: particle mass $m$, trajectory $\mathbf{x}(t)$, force $\mathbf{F}$:
$$
m \frac{d^2 \mathbf{x}(t)}{dt^2} = \mathbf{F}(\mathbf{x}(t))
$$
If force conservative: $\mathbf{F} = -\nabla V$
$$
E = \frac{m}{2} \dot{\mathbf{x}}^2 + V(\mathbf{x}) \quad \text{with} \quad \frac{dE}{dt} = 0
$$

#### Difficulties with Newton's formulation
- Vector equations not easy except in orthogonal coordinates  
- Global system properties hard to deduce  
- Symmetry analysis cumbersome  
- Constraints difficult to incorporate  

---
## Lagrange Formalism

### Action principle
System with $N$ d.o.f described by:
- Generalized coordinates $\{q_i\} \in \mathcal{M}$ (configuration space)
- Generalized velocities $\{\dot q_i\}$

Action: $S[q]$ functional  
Variation via Gateaux derivative:
$$
\frac{dS[q + \epsilon r]}{d\epsilon} = \int_{t_i}^{t_f} dt \frac{\delta S}{\delta q} r
$$

For closed system:
$$
S[q] = \int_{t_i}^{t_f} dt\, L(q(t), \dot q(t))
$$
$$
\begin{aligned}
S[q + \epsilon r] &= \int_{t_i}^{t_f} dt\, L(q + \epsilon r, \dot q + \epsilon \dot r) \\
&= \int dt \left[L + \frac{\partial L}{\partial q} \epsilon r + \frac{\partial L}{\partial \dot q} \epsilon \dot r + \cdots \right]
\end{aligned}
$$
$$
\frac{dS[q + \epsilon r]}{d\epsilon} = \int_{t_i}^{t_f} dt \left[ \frac{\partial L}{\partial q} r + \frac{\partial L}{\partial \dot q} \dot r \right]
$$

Integration by parts:
$$
\frac{dS}{d\epsilon} = \int_{t_i}^{t_f} dt \left[ \frac{\partial L}{\partial q} - \frac{d}{dt} \left( \frac{\partial L}{\partial \dot q} \right) \right] r + \left[ \frac{\partial L}{\partial \dot q} r \right]_{t_i}^{t_f}
$$

Boundary conditions:
1. Dirichlet: $r(t_i) = r(t_f) = 0$  
2. Neumann: (specify momentum)  

Stationary action $\delta S = 0$ gives Euler-Lagrange:
$$
\frac{\delta S}{\delta q} = \frac{\partial L}{\partial q} - \frac{d}{dt} \left( \frac{\partial L}{\partial \dot q} \right)
$$
For $N$ d.o.f:
$$
\frac{\partial L}{\partial q_i} = \frac{d}{dt} \left( \frac{\partial L}{\partial \dot q_i} \right), \quad 1 \leq i \leq N
$$

**Example:** Particle of mass $m$, potential $V(x)$  
$$
L = \frac{1}{2} m \dot{x}^2 - V(x)
$$
E-L: $-\frac{\partial V}{\partial x} = m \ddot{x}$

---
## Hamiltonian Formalism
Transition from configuration space $(q_i, \dot q_i)$ to phase space $(q_i, p_i)$
### Canonical transformation
- Conjugate momentum: $p_i(t) = \frac{\partial L}{\partial \dot q_i} (q_i, \dot q_i)$  
- Require invertibility: $\det \frac{\partial p_i}{\partial \dot q_j} = \det \frac{\partial^2 L}{\partial \dot q_i \partial \dot q_j} \neq 0$

Hamiltonian via Legendre transform:
$$
H(q,p) = p \dot q(q,p) - L(q, \dot q(q, p))
$$
### Hamilton's equations
Differential:
$$
dH = \frac{\partial H}{\partial q} dq + \frac{\partial H}{\partial p} dp
$$
From definition:
$$
\begin{aligned}
dH &= d(p \dot q - L) \\
&= \dot q dp + p d\dot q - \frac{\partial L}{\partial q} dq - \frac{\partial L}{\partial \dot q} d\dot q \\
&= \dot q dp - \frac{\partial L}{\partial q} dq \quad (\text{since } p = \frac{\partial L}{\partial \dot q})
\end{aligned}
$$
Using E-L: $\frac{\partial L}{\partial q} = \dot p$
$$
dH = \dot q dp - \dot p dq
$$
Compare coefficients:
$$
\frac{\partial H}{\partial q} = -\dot p, \quad \frac{\partial H}{\partial p} = \dot q
$$

---
### Poisson brackets
For $f(q,p), g(q,p)$:
$$
\{f,g\} = \frac{\partial f}{\partial q} \frac{\partial g}{\partial p} - \frac{\partial f}{\partial p} \frac{\partial g}{\partial q}
$$

Properties (Lie bracket):
1. Linearity: $\{f, \alpha_1 g_1 + \alpha_2 g_2\} = \alpha_1 \{f,g_1\} + \alpha_2 \{f,g_2\}$  
2. Skew-symmetry: $\{f,g\} = -\{g,f\}$  
3. Jacobi: $\{\{f,g\},h\} + \{\{g,h\},f\} + \{\{h,f\},g\} = 0$

Fundamental brackets:
- $\{p_i, p_j\} = 0$
- $\{q_i, q_j\} = 0$
- $\{q_i, p_j\} = \delta_{ij}$

**Example:** For $f(q,p)$ with no explicit time dependence:
$$
\{f, H\} = 0 \Rightarrow f \text{ constant of motion}
$$
Proof:
$$
\{f, H\} = \frac{\partial f}{\partial q} \frac{\partial H}{\partial p} - \frac{\partial f}{\partial p} \frac{\partial H}{\partial q} = \frac{\partial f}{\partial q} \dot q + \frac{\partial f}{\partial p} \dot p = \frac{df}{dt} = 0
$$

---

**Example:** 1D harmonic oscillator $(m, \omega)$  
$$
L = \frac{1}{2} m \dot x^2 - \frac{1}{2} m \omega^2 x^2
$$
E-L: $\ddot x + \omega^2 x = 0$
$$
p = \frac{\partial L}{\partial \dot x} = m \dot x
$$
$$
H = p \dot x - L = \frac{p^2}{2m} + \frac{1}{2} m \omega^2 x^2
$$
Hamilton's equations:
$$
\frac{\partial H}{\partial x} = m \omega^2 x = -\dot p, \quad \frac{\partial H}{\partial p} = \frac{p}{m} = \dot x
$$
