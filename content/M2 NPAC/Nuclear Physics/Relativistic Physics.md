## Relativistic Physics

### Lorentz Transformations
Starting from the general linear transformation, choosing $\alpha = 1/c^2$ gives the **Lorentz transformations**:
$$
\begin{aligned}
\Delta x' &= \gamma(v)(\Delta x - v\,\Delta t) \\
\Delta t' &= \gamma(v)\!\left(\Delta t - \frac{v}{c^2}\,\Delta x\right)
\end{aligned}
$$
with the **Lorentz factor**:
$$
\gamma(v) = \frac{1}{\sqrt{1 - v^2/c^2}}
$$

---
### Minkowski Spacetime
Minkowski spacetime $\mathcal{M} = \mathbb{R} \times \mathbb{R}^3$ is equipped with the metric:
$$
\eta_{\mu \nu} = \text{diag}(1, -1, -1, -1)
= \begin{pmatrix}
1 & 0 & 0 & 0 \\
0 & -1 & 0 & 0 \\
0 & 0 & -1 & 0 \\
0 & 0 & 0 & -1
\end{pmatrix}
$$

**Comparison:**
- **Galilean case:** Isometry group $O(3)$ preserves $ds^2 = dx^2 + dy^2 + dz^2$
- **Lorentz case:** Isometry group $O(3,1)$ preserves $ds^2 = dt^2 - dx^2 - dy^2 - dz^2$

---
### Basis and Coordinates

**Standard basis:**
$$
e_0 = \begin{pmatrix}1\\0\\0\\0\end{pmatrix}, \quad
e_1 = \begin{pmatrix}0\\1\\0\\0\end{pmatrix}, \quad
e_2 = \begin{pmatrix}0\\0\\1\\0\end{pmatrix}, \quad
e_3 = \begin{pmatrix}0\\0\\0\\1\end{pmatrix}
$$

**4-vector decomposition:**
$$
A = A^\mu e_\mu = A^0 e_0 + A^1 e_1 + A^2 e_2 + A^3 e_3
$$
- $A^0$ → time component  
- $A^i$ ($i=1,2,3$) → spatial components  

**Inner product:**
$$
\eta_{\mu\nu} = e_\mu \cdot e_\nu
$$
Hence:
- $e_0 \cdot e_0 = 1$ (time-like)  
- $e_i \cdot e_i = -1$ for $i=1,2,3$ (space-like)  
- $e_\mu \cdot e_\nu = 0$ for $\mu \neq \nu$

**Covariant vs Contravariant:**
- Contravariant: $A^\mu$ in $A = A^\mu e_\mu$
- Covariant: $A_\mu = A^\nu \eta_{\mu\nu}$

**Example:**
$$
A_0 = A^0, \quad A_i = -A^i
$$

---
### Lorentz Group
The **Lorentz group** $O(3,1)$ is the group of isometries preserving the Minkowski metric:
$$
\eta(\Lambda x, \Lambda y) = \eta(x, y) \quad \forall x,y \in \mathcal{M}
$$

In matrix form:
$$
\eta = \Lambda^T \eta \Lambda
$$
Taking determinants:
$$
\det \Lambda = \pm 1
$$
In components:
$$
\eta_{\rho\sigma} = \Lambda^\mu_{\ \rho} \eta_{\mu\nu} \Lambda^\nu_{\ \sigma}
$$

---
### Time Component Constraint
From $\eta_{00} = \Lambda^\mu_{\ 0} \eta_{\mu\nu} \Lambda^\nu_{\ 0}$:
$$
1 = (\Lambda^0_{\ 0})^2 - \sum_{i=1}^3 (\Lambda^i_{\ 0})^2
$$
Hence:
$$
(\Lambda^0_{\ 0})^2 \ge 1 \quad \Rightarrow \quad \Lambda^0_{\ 0} \ge 1 \text{ or } \Lambda^0_{\ 0} \le -1
$$

---
### Connected Components of $O(3,1)$
The Lorentz group splits into **4 connected components**:

1. **$SO^+(3,1)$ (proper, orthochronous):**  
   $\det \Lambda = 1$, $\Lambda^0_{\ 0} \ge 1$

2. **PT (improper, non-orthochronous):**  
   $\det \Lambda = 1$, $\Lambda^0_{\ 0} \le -1$

3. **P (parity):**  
   $\det \Lambda = -1$, $\Lambda^0_{\ 0} \ge 1$

4. **T (time reversal):**  
   $\det \Lambda = -1$, $\Lambda^0_{\ 0} \le -1$

**Structure:**
Every $\Lambda \in O(3,1)$ can be expressed as:
$$
\Lambda = L \cdot k, \quad L \in SO^+(3,1), \quad k \in \{\mathbb{1}, P, T, PT\}
$$
where $\{\mathbb{1}, P, T, PT\} \cong K_4$ is the **Klein 4-group**.
