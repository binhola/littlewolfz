### Group and representation
A **group** describes symmetry operations. A **representation** tells how those operations act on physical objects (scalars, vectors, spinors...).  
We focus on $O(3)$ / $SO(3)$ (rotations & parity) and its algebra $\mathfrak{so}(3)$; then $SU(2)$ (double cover) and spinor reps.

---
### 1. $O(3)$ and $SO(3)$ (geometry)
- $O(3) = \{R\in\mathrm{Mat}_{3\times3}\mid R^T R = \mathbb{1}\}$.  
  For any $\mathbf x\in\mathbb{R}^3$ and $R\in O(3)$: $|R\mathbf x|^2 = |\mathbf x|^2$ (length preserved).
- Group properties (proof sketch): closure, inverse ($R^{-1}=R^T$), identity $\mathbb{1}$, associativity (matrix multiplication).
- $\det R=\pm1$.  
  - $SO(3)=\{R\in O(3)\mid \det R=1\}$ (proper rotations).
  - Parity $P=-\mathbb{1}$ has $\det P=-1$. Any $R\in O(3)$ = ($\text{something}\in SO(3)$) $\times$ $\{\mathbb{1},P\}$.

**Counting parameters:** a $3\times3$ real matrix has 9 real numbers. Orthogonality $R^T R=\mathbb{1}$ gives 6 independent constraints (symmetric matrix condition), so $\dim SO(3)=9-6=3$.

---
### 2. Infinitesimal rotations and the algebra $\mathfrak{so}(3)$
Infinitesimal rotation: $R = \mathbb{1} + \epsilon$, with orthogonality $\Rightarrow \epsilon^T = -\epsilon$ (antisymmetric).  
Parameterize small rotation by $d\boldsymbol\theta=(d\theta_x,d\theta_y,d\theta_z)$:
$$
\epsilon = 
\begin{pmatrix}
0 & d\theta_z & -d\theta_y \\
-d\theta_z & 0 & d\theta_x \\
d\theta_y & -d\theta_x & 0
\end{pmatrix}.
$$

Define Hermitian (physics) generators $J_i$ by
$$
R(\boldsymbol\theta) = e^{i \boldsymbol\theta\cdot \mathbf J}.
$$

**3×3 (vector) rep generators** (real antisymmetric form times $-i$ gives Hermitian):
$$
(J_x)_{3\times3} =
\begin{pmatrix}
0 & 0 & 0\\
0 & 0 & -i\\
0 & i & 0
\end{pmatrix},\quad
(J_y)_{3\times3} =
\begin{pmatrix}
0 & 0 & i\\
0 & 0 & 0\\
-i & 0 & 0
\end{pmatrix},\quad
(J_z)_{3\times3} =
\begin{pmatrix}
0 & -i & 0\\
i & 0 & 0\\
0 & 0 & 0
\end{pmatrix}.
$$

Commutation relations (Lie algebra):
$$
[J_i, J_j] = i \epsilon_{ijk} J_k.
$$


Finite rotation about unit axis $\mathbf n$ by angle $\theta$:
$$
R(\theta,\mathbf n)= e^{i\theta \mathbf n\cdot \mathbf J}.
$$

---

### 3. Representations (general)
A **representation** is a map
$$
\mathcal D: G \to GL(V)
$$

such that $\mathcal D(g_1 g_2)=\mathcal D(g_1)\mathcal D(g_2)$.  
For Lie algebras, a rep is $d:\mathfrak g\to \mathrm{End}(V)$ preserving commutators:
$$
[d(X), d(Y)] = d([X,Y]).
$$

Exponentiate algebra reps to get group reps:
$$
\mathcal D(g)=\exp\big(i\theta\cdot d(\mathbf J)\big).
$$

**Projective reps:** allow phases:
$$
\mathcal D(g_1 g_2) = e^{i\phi(g_1,g_2)}\mathcal D(g_1)\mathcal D(g_2).
$$

---
### 4. Casimir and labeling irreps
Casimir operator for $\mathfrak{so}(3)$:
$$
\mathbf J^2 = J_x^2 + J_y^2 + J_z^2.
$$

It commutes with all generators: $[\mathbf J^2, J_i]=0$. By Schur’s lemma, on an irreducible representation (irrep) it is scalar:
$$
\mathbf J^2 = j(j+1)\,\mathbb{1}.
$$

Label $j=0,\tfrac12,1,\tfrac32,\dots$; dimension $=2j+1$.
- $j=0$: scalar (trivial rep), $\mathcal D=1$.
- $j=1$: vector rep (3-dim) — the matrix exponentials above.
- $j=\tfrac12$: spinor rep (2-dim) — see $SU(2)$.
---
### 5. $SU(2)$ and spinors
$SU(2)=\{U\in\mathbb C^{2\times2}\mid U^\dagger U=\mathbb{1},\ \det U=1\}$ is the double cover of $SO(3)$:
- For each $R\in SO(3)$ there are two $U\in SU(2)$: $U$ and $-U$.
- This gives the $4\pi$ periodicity for spinors: rotation by $2\pi$ changes a spinor sign.

Pauli matrices (basis for $\mathfrak{su}(2)$):
$$
\sigma_1=\begin{pmatrix}0&1\\1&0\end{pmatrix},\quad
\sigma_2=\begin{pmatrix}0&-i\\ i&0\end{pmatrix},\quad
\sigma_3=\begin{pmatrix}1&0\\0&-1\end{pmatrix}.
$$

They satisfy
$$
\left[\frac{\sigma_i}{2},\frac{\sigma_j}{2}\right]=i\epsilon_{ijk}\frac{\sigma_k}{2},\qquad
\{\sigma_i,\sigma_j\}=2\delta_{ij}.
$$

Spin-$\tfrac12$ rep:
$$
\mathcal D_{1/2}(R(\theta,\mathbf n)) = \exp\!\Big(i\frac{\theta}{2}\,\mathbf n\cdot\sigma\Big)
= \cos\frac\theta2\,\mathbb{1}_2 + i\sin\frac\theta2\,\mathbf n\cdot\sigma.
$$

Acting on spinors $z=\begin{pmatrix}z_1\\z_2\end{pmatrix}$: $z'=\mathcal D_{1/2} z$.

---
### 6. Examples & properties
- **Vectors ($j=1$):** dimension $3$, transform under $e^{i\theta\cdot J}$.
- **Scalars ($j=0$):** invariant.
- **Spinors ($j=1/2$):** $SU(2)$ doublet, $2\pi$ rotation $\to -1$, $4\pi$ returns identity.
- **Add angular momenta:** tensor product $j_1\otimes j_2 = \bigoplus_{j=|j_1-j_2|}^{j_1+j_2} j$ (Clebsch–Gordan).

---

### 7. Systematic recipe for group / Lie-algebra analysis (copyable)

1. **Identify the group $G$.** geometric meaning (rotations, translations, etc.).  
2. **Find algebra $\mathfrak g$ (infinitesimal generators).** compute commutators $[X_i,X_j]=f_{ij}^{\ \ k} X_k$ (structure constants $f_{ij}^{\ \ k}$).  
3. **Find Casimir invariants.** (quantities built from generators that commute with all of them). These label irreps.  
4. **Classify irreps.** Use highest-weight or ladder-operator method (for compact simple algebras like $\mathfrak{so}(3)\simeq\mathfrak{su}(2)$ this gives $j=0,\tfrac12,1,\dots$).  
5. **Construct explicit reps.** choose matrices for generators $d(J_i)$ satisfying algebra; exponentiate: $\mathcal D(g)=\exp(i\theta\cdot d(J))$.  
6. **Check dimensions & orthogonality.** For compact groups use unitary reps; dimensions from labels (e.g. $2j+1$).  
7. **Compute characters / traces.** $\chi(g)=\mathrm{Tr}\,\mathcal D(g)$ helps identify irreps and decompose tensor products.  
8. **Tensor products & decomposition.** use Clebsch–Gordan rules or character orthogonality.  
9. **Covering groups & projective reps.** check if projective phases appear (e.g. $SO(3)$ vs $SU(2)$, spinors).  
10. **Physical interpretation:** map reps to physical objects (scalars, vectors, spinors, tensors). Check parity/time reversal behavior if needed.

---
### 8. Short answers to common physics questions
- **Why electron in H atom is “spinor” (extensive?)** — electron is described by a spin-$\tfrac12$ rep of rotations: its internal state (spin) transforms under $\mathcal D_{1/2}\in SU(2)$. This gives the two spin states and $4\pi$ periodicity.  
- **Why dimension $=2j+1$?** Ladder (raising/lowering) operators produce $2j+1$ distinct eigenstates of $J_z$ from $-j$ to $+j$.
---
### 9. Useful formulas (cheat sheet)
- Algebra: $[J_i,J_j]=i\epsilon_{ijk}J_k$.
- Casimir: $\mathbf J^2=j(j+1)\mathbb{1}$.
- Finite rotation: $R(\theta,\mathbf n)=e^{i\theta \mathbf n\cdot \mathbf J}$.
- SU(2) spinor rotation: $e^{i\frac\theta2 \mathbf n\cdot\sigma}$.
- Tensor product: $j_1\otimes j_2 = \bigoplus_{j=|j_1-j_2|}^{j_1+j_2} j$.
