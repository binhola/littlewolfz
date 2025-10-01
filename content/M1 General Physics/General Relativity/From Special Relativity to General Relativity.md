---
tags: 
draft: false
---
## Special Relativity
### Affine spacetime
**Definition:** an affine space is a triple $(E, V, \vec{..})$ where
- $E$ is a set (the set of events)
- $V$ is an $\mathbb{R}$-vector space
- $\vec{..}$ is a mapping
$$\begin{aligned}&E\times E \rightarrow V \\ &(A,B) \rightarrow \mathbf{AB}\end{aligned}$$
satifies
1. **Translation**: $\forall \, A,B,C \in E: \quad \mathbf{AB} + \mathbf{BC} = \mathbf{AC}$ 
2. **Uniqueness:** $\forall \, A \in E, \, \forall \mathbf{v} \in V: \quad \exists ! B \in E \text{ so that } \mathbf{AB} = \mathbf{v}$
3. The dimension of $(E,V,\vec{..})$ is $\dim(V)$ 

*Example*: $(\mathbb{R}^4, \mathbb{R}^4, \vec{..})$ where $\forall \, A,B \in \mathbb{R}^4: \, \mathbf{AB} = B - A$ is a 4-dim affine space.
### Frame
**Definition:** A frame in $(E, V, \vec{..})$ is a pair of $(O,B)$ where
- $O \in E$ is the origin of the frame
- $B = \{e_\mu: \mu=0,...,3\}$ is a basis of $V$

Given a frame $(O, B = \{e_\mu\})$ in $(E, V, \vec{..})$ we have
$$
\forall \, M \in E: \, \mathbf{OM} = \sum_{\mu = 0}^3 x^\mu(M) e_\mu = x^\mu e_\mu
$$
Therefore, we have a bijection $\Phi$:
$$ 
\begin{aligned}
E &\rightarrow \mathbb{R}^4 \\
M &\mapsto \Phi(M) = \big(x^0(M), ... ,x^3(M)\big) \in \mathbb{R}^4
\end{aligned}
$$
*Note:* This is indeed a homomorphism, i.e. continuous bijection with continuous reciprocal

Frames of $(E, V, \vec{..})$ is global coordinate system over $E$.

Given another frame $(O', B' = \{e'_{\mu'} \, ; \, \mu'=0,...,3 \})$ we have
$$
\forall \, M \in E: \mathbf{O'M} = x'^{\mu'}(M) e'_{\mu '}
$$
Now, there exists
$$
e'_{\mu '} = \Lambda^\mu_{\mu '} e_\mu
$$
Hence
$$
\mathbf{O'M} = x'^{\mu '} (M) \Lambda^\mu_{\mu '} e_\mu
$$
And setting
$$
\mathbf{OO'} = a^{\mu} e_\mu
$$
We finally get
$$
\mathbf{OM} = x^{\mu} (M) e_{\mu} = \mathbf{OO'} + \mathbf{O'M} = (a^\mu + \Lambda^\mu_{\mu '} x'^{\mu '}(M)) e_{\mu}
$$
So we can define the *Affine transformation* as
$$
x^\mu = a^\mu + \Lambda^\mu_{\mu '} x'^{\mu '}
$$
where $a^\mu \in \mathbb{R}^4$ and $\Lambda^\mu_{\mu '} \in GL(4, \mathbb{R})$. 
They form a group called *Affine group*: $IGL(4, \mathbb{R}) = \mathbb{R} \rtimes GL(4,\mathbb{R})$.
### Worldline
A history of a point particle in $(E, V, \vec{..})$ is a curve $\gamma : \mathbb{R} \rightarrow E$ called *worldline*

The point particle will have a motion of rectilinear uniform translation if its worldline is a straight line in $E$.

Since *affine transformation* is the only transformation of $E$ sending any straight line to a straight line, galilean frame and the transformation between them can be identified with a class of frames of $E$ and a subgroup of $IGL(4, \mathbb{R})$

## Galilean and Einstein relativity
1. **Principle of relativity**: No experiment can distinguish between two Galilean frames i.e. the laws of physics have the same form in all Galilean frames.

Galilean relativity assume absolute time with transformation defined by Galilean group, that not preserve the form of Maxwell's equations. Then, this assumption should be renounced in Einstein relativity. As the consequence, the simultaneity is lost.

2. **Principle of causality:** in any Galilean frame, there exists a maximal speed for the transport of matter, energy, information, ....

Combined with relativity principle, it turns out that there should be a unique maximal speed. Experimentally, that speed is $c$ - the speed of light in vacuum.
#### Worldline of a photon
A photon emitted at $t=0$ at $\mathbf{x} =0$ is a generatrix of the light cone.
$$
0 = -(ct)^2 + \mathbf{x}^2
$$
Define a bilinear form $\eta$
$$
\begin{aligned}
V \times V \rightarrow \mathbb{R}
\end{aligned}
$$
by setting
$$
\eta (e_\mu, e_\nu) = \eta_{\mu\nu} = 
\begin{pmatrix} 
-1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 0 & 1 & 0 \\
0 & 0 & 0 & 1
\end{pmatrix}
$$
In this setting, the worldline of a photon can be expressed as
$$
\eta(X, X) = 0 \quad \text{where} \quad X = x^\mu e_\mu
$$
Or
$$
\eta_{\mu \nu} x^\mu x^\nu = 0
$$
In a different galilean frame $(O' = O, B' = \{ e'_{\mu'} \})$
We have
$$
\eta_{\mu \nu} \Lambda^{\mu}_{\mu '} \Lambda^{\nu}_{\nu '} x'^{\mu '} x'^{\nu '} = 0
$$
In order to ensure the causality principle, it suffices (actually necessary) to take $\Lambda^{\mu}_{\mu '}$ in $O(1,3)$:
$$
\Lambda^\mu_{\mu '} \in GL(4, \mathbb{R}) : \Lambda^\mu_{\mu '} \Lambda^\nu_{\nu '} \eta_{\mu \nu} = \eta_{\mu ' \nu '}
$$
This is the *Lorentz group*.

A change of Galilean frame can always be connected to the identity. Hence, $\Lambda^\mu_{\mu '}$ should actually be in the connected component of $\mathbb{1}_4$ in $O(1,3)$, i.e.
$$
\Lambda^\mu_{\mu '} \in SO^+(1,3) = \text{connected component of } \mathbb{1}_4 \text{ in } O(1,3) 
$$
$SO^+(1,3)$ is the special orthochronous Lorentz group. 

*Notes:* 
- Remember that, we are excluding
$$
T = \begin{pmatrix} 
-1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 0 & 1 & 0 \\
0 & 0 & 0 & 1 \\
\end{pmatrix} 
\quad 
P = \begin{pmatrix} 
1 & 0 & 0 & 0 \\
0 & -1 & 0 & 0 \\
0 & 0 & -1 & 0 \\
0 & 0 & 0 & -1 \\
\end{pmatrix}
$$
- $O(1,3)$ can be obtained from $SO^+(1,3)$, $P$, $T$ and $PT$.
- In SR, spacetime is represented by Minkowski $Mink_4 = (E, V, \vec{..}, \eta)$
- Transformation from Galilean frame to Galilean frame through $ISO^+(1,3) = \mathbb{R}^4 \rtimes SO^+(1,3)$ which is the *special orthochronous Poincare group*.
## Tensors and Lorentz covariance
In order to implement the relativity principle, we need to write the laws of physics in terms of representation of $SO^+(1,3)$
- Let $V^*$ is the dual of $V$. It's the space of linear form $\theta$ : $V \rightarrow \mathbb{R}$ 
- Let $\{e_\mu\}$ be the basis in $V$. We define the dual basis of $V^*$ : $\{ e^\mu: \mu = 0,...,3 \}$ by setting $$e^\mu(e_\nu) = \delta^\mu_\nu$$
- Now, let $\{e'_{\mu '}\}$ be another basis of $V$ and let $\{e'^{\mu '}\}$ be the dual basis of $V^*$. There exists $\Lambda^\mu_{\mu '} \in SO^+(1,3)$ ( or $GL(4, \mathbb{R}$) ) 
$$
e'_{\mu '} = \Lambda^{\mu}_{\mu '} e_{\mu}
$$
and 
$$
e'^{\mu '} = \widetilde{\Lambda}^{\mu '}_{\mu} e^{\mu}
$$
where $\widetilde{\Lambda}^\mu_{\mu '} \in SO^+(1,3)$ ( or $GL(4, \mathbb{R}$) ).
Then, by definition
$$
\delta^{\mu '}_{\nu '} = e'^{\mu '} (e'_{\nu '}) = e'^{\mu'}(\Lambda^\nu_{\nu'} e_\nu) = \Lambda^\nu_{\nu '} e'^{\nu '}(e_\nu) = \Lambda^\nu_{\nu '} \widetilde{\Lambda}^{\mu '}_{\mu}e^{\nu}(e_\nu) = \Lambda^\nu_{\nu '} \widetilde{\Lambda}^{\mu '}_{\mu} \delta^{\mu}_{\nu} = \widetilde{\Lambda}^{\mu '}_{\mu} \Lambda^\mu_{\nu '} 
$$
Hence,
$$
\widetilde{\Lambda}^{\mu '}_{\mu} = \text{inverse of } \Lambda^\mu_{\mu '}
$$
- Define $\forall \, r,s \in \mathbb{N}$ 
$$
V^{(r,s)} = \underbrace{V \otimes \dotsb \otimes V}_{\text{r times}} \otimes \underbrace{V^* \otimes \dotsb \otimes V^*}_{\text{s times}}
$$
Element in $V^{(r,s)}$ are $(r,s)$ tensors
- For any basis $\{e_\mu\}$ of $V$ and its dual basis $\{e^\mu \}$ of $V^*$ 
$$
\{ e_{\mu_1} \otimes \dotsb \otimes e_{\mu_r} \otimes e^{\nu_1} \otimes \dotsb \otimes e^{\nu_s}\}
$$
is the basis of $V^{(r,s)} \, \forall \, r,s \in \mathbb{N}$. In particular, $\forall \, T \in V^{(r,s)}$ 
$$
T = T^{\mu_1 \dotsc \mu_r}_{\nu_1 \dotsc \nu_s} e_{\mu_1} \otimes \dotsb \otimes e_{\mu_r} \otimes e^{\nu_1} \otimes \dotsb \otimes e^{\nu_s}
$$
- Given another basis $\{e'_{\mu '}\}$ with dual $\{e'^{\mu '}\}$ we have
$$
\begin{aligned}
T &= T'^{\mu'_1 \dotsc \mu'_r}_{\nu'_1 \dotsc \nu'_s} e_{\mu'_1} \otimes \dotsb \otimes e_{\mu'_r} \otimes e^{\nu'_1} \otimes \dotsb \otimes e^{\nu'_s} \\
&= T'^{\mu'_1 \dotsc \mu'_r}_{\nu'_1 \dotsc \nu'_s} \Lambda^{\mu_1}_{\mu'_1} \dotsc \Lambda^{\mu_r}_{\mu'_r} \, \widetilde{\Lambda}^{\nu'_1}_{\nu_1} \dotsc \widetilde{\Lambda}^{\nu'_s}_{\nu_s} \, e_{\mu_1} \otimes \dotsb \otimes e_{\mu_r} \otimes e^{\nu_1} \otimes \dotsb \otimes e^{\nu_s} \\
&\stackrel{!}{=} T^{\mu_1 \dotsc \mu_r}_{\nu_1 \dotsc \nu_s} \, e_{\mu_1} \otimes \dotsb \otimes e_{\mu_r} \otimes e^{\nu_1} \otimes \dotsb \otimes e^{\nu_s}
\end{aligned}
$$
Hence,
$$
T^{\mu_1 \dotsc \mu_r}_{\hspace{3em} \nu_1 \dotsc \nu_s} = T'^{\mu'_1 \dotsc \mu'_r}_{\hspace{3em} \nu'_{1} \dotsc \nu'_{s}} \Lambda^{\mu_1}_{\mu'_1} \dotsc \Lambda^{\mu_r}_{\mu'_r} \, \widetilde{\Lambda}^{\nu'_1}_{\nu_1} \dotsc \widetilde{\Lambda}^{\nu'_s}_{\nu_s}
$$
Thus, it suffices to write the laws of physics in term of tensors, i.e,
$$
T = 0 \Leftrightarrow T^{\mu_1 \dotsc \mu_r}_{\hspace{3em} \nu_1 \dotsc \nu_s} = 0
$$
to realize the relativity principle $\rightarrow$ manifestation of Lorentz covariant

*Notes:*
- It suffices, not necessary $SO^+(1,3)$ multiply connected and hence, admits non-trivial projective representation that are not tensorial like spinorial representations
- Generalization to $SO^+(1,3)$ of the covariance already used in classical mechanics for Galilean of $SO(3)$ group laws of physics in terms of scalars, vectors, tensors, etc
- Everything we did above still works for $\Lambda^{\mu}_{\mu '} \in GL(4,\mathbb{R})$ instead of simply $SO^+(1,3)$
## Indexology
$\eta$ is non-degenerate, hence it sets up an isomorphism of $\mathbb{R}$-vector spaces, called the musical isomorphism
$$
^b : \quad \begin{aligned}
V &\rightarrow V^* \\
v &\mapsto v^b(-) = \eta(v, -)
\end{aligned}
$$

with reciprocal
$$
^\# : \quad \begin{aligned}
V^* &\rightarrow V \\
\theta &\mapsto \theta^\#
\end{aligned}
$$
where $(\theta^\#)^b = \theta$ 
- Let $\{e_\mu\}$ be a basis of $V$ with dual basis $\{e^{\mu}\}$ 
- Let $v = v^\mu e_{\mu}$ 
$$
v^b(e_\nu) = \eta(v, e_\nu) = \eta(v^\mu e_\mu, e_\nu) = v^\mu \eta(e_\mu, e_\nu) = v^\mu \eta_{\mu \nu}
$$
We also have
$$
v^b(e_\nu) = v^b_\mu e^\mu(e_\nu) = v^b_\mu \delta^\mu_\nu = v^b_\nu
$$
So
$$
v^b_\nu = v^\mu \eta_{\mu \nu}
$$
Converting the index with metric
- Let $\theta = \theta_\mu e^\mu$ 
$$
(\theta^\#)^b(e_\nu) = \eta (\theta ^\#, e_\nu) = \eta(\theta^{\# \mu} e_{\mu}, e_\nu ) = \theta^{\# \mu} \eta_{\mu \nu}
$$
$\eta_{\mu \nu}$ is its own inverse. Denoting that inverse as $\eta^{\mu \nu}$ we get
$$
\theta^{\# \mu} = \eta^{\mu \nu} \theta_\nu
$$
*Notes:*
- Only use $V$ and $\eta$ in $(E, V, X, \eta)$
- works with more general non-degenerate symmetric bilinear forms other than $\eta$ . The inverse does not necessary to be the same like in the $\eta$ case.
- Musical isomorphism is trivial in euclidean geometry, raising/lowering with $\delta_{ij}$ or $\delta^{ij}$ does not matter.
- $\_^b$ and $\_^\#$ can be extended to $V^{(r,s)}$
#### Contractions
$\forall \, n,s \in \mathbb{N}$ and $\forall \, m = 1, \cdots, r$ and $\forall \, n = 1, \cdots, s$
$$
<\_>_{m,n} \, : V^{r,s} \rightarrow V^{r-1, s-1} \quad \text{is defined } \forall \, T \in V^{r,s}
$$
We have
$$
\begin{aligned}
<T>_{m,n} &= < T^{\mu_1 \dotsc \mu_r}_{\hspace{3em} \nu_1 \dotsc \nu_s} e_{\mu_1} \otimes \dotsc \otimes e_{\mu_r} \otimes e^{\nu_1} \otimes \dotsc \otimes e^{\nu_s} >_{m,n} \\
&= T^{\mu_1 \dotsc \mu_r}_{\hspace{3em} \nu_1 \dotsc \nu_s} \, \underbrace{e^{\nu_n}(e_{\mu_m})}_{\delta^{\nu_n}_{\mu_m}} \, e_{\mu_1} \otimes \dotsc \otimes e_{\mu_{m-1}} \otimes e_{\mu_{m+1}} \otimes \dotsc \otimes e_{\mu_r} \otimes e^{\nu_1} \otimes e^{\nu_{n-1}} \otimes e^{\nu_{n+1}} \otimes \dotsc \otimes e^{\nu_s} \\
&= T^{\mu_1 \dotsc \mu_{m-1} \mu_{m+1} \dotsc \mu_r}_{\hspace{5em} \nu_1 \dotsc \nu_{n-1} \nu_{n+1} \dotsc \nu_s} \, e_{\mu_1} \otimes \dotsc \otimes e_{\mu_{m-1}} \otimes e_{\mu_{m+1}} \otimes \dotsc \otimes e_{\mu_r} \otimes e^{\nu_1} \otimes e^{\nu_{n-1}} \otimes e^{\nu_{n+1}} \otimes \dotsc \otimes e^{\nu_s}
\end{aligned}
$$
#### Functions
Let $f: E \rightarrow \mathbb{R}$ be a $C^1$ function
- Define $df : E \rightarrow V^*$ by setting, in any frame $(O, \{ e_\mu \})$ with dual basis $\{e^\mu \}$
$$
df = \dfrac{\partial f}{\partial x^\mu} e^\mu = (\partial_\mu f) e^\mu \text{ with  } \mu = 0,...,3
$$
- Given another frame $(O', \{e'_{\mu'}\})$ with dual basis $\{e'^{\mu '}\}$ we have
$$
df = \dfrac{\partial x'^{\mu '}}{\partial x^\mu} \dfrac{\partial f}{ \partial x'^{\mu '}} e^{\mu} = \widetilde{\Lambda}^{\mu '}_{\mu} \dfrac{\partial f}{\partial x'^{\mu '}} e^\mu = \dfrac{\partial f}{\partial x'^{\mu '}} e'^{\mu '} = (\partial '_{\mu '}f) e'^{\mu '}
$$
- Generalise to $T: E \rightarrow V^{r,s}$ by setting
$$
\begin{aligned}
dT &= d(T^{\mu_1 \dotsc \mu_r}_{\hspace{3em} \nu_1 \dotsc \nu_s} \, e_{\mu_1} \otimes \dotsc \otimes e_{\mu_r} \otimes e^{\nu_1} \otimes \dotsc \otimes e^{\nu_s}) \\
&= \partial_\mu(T^{\mu_1 \dotsc \mu_r}_{\hspace{3em} \nu_1 \dotsc \nu_s}) \, e_{\mu_1} \otimes \dotsc \otimes e_{\mu_r} \otimes e^{\nu_1} \otimes \dotsc \otimes e^{\nu_s} \otimes e^{\mu} \\
&= T^{\mu_1 \dotsc \mu_r}_{\hspace{3em} \nu_1 \dotsc \nu_s, \, \mu} \, e_{\mu_1} \otimes \dotsc \otimes e_{\mu_r} \otimes e^{\nu_1} \otimes \dotsc \otimes e^{\nu_s} \otimes e^{\mu}
\end{aligned}
$$
## Free point particle
- Worldline of a point particle is a curve
$$
\gamma : \mathbb{R} \rightarrow E
$$
- Given a frame $(O, \{e_\mu\})$ of $Mink_4$ we have a global coordinate system $\phi = (x^0, \dotsc, x^3)$ so that
$$
\phi \cdot \gamma = (x^0 \gamma_0, \dotsc, x^3 \gamma_3) = (X^0, \dotsc, X^3)
$$
We shall say $\gamma$ is $C^1$ if $\phi \cdot \gamma$ is satisfied
If $\gamma$ is $C^1$, define $\forall \, s \in \mathbb{R}$
$$
\dot{\gamma}(s) = \dfrac{d x^\mu \cdot \gamma}{ds} e_{\mu}
$$
This 4-velocity of point particle
- Under a change of frames
$$
\begin{aligned}
\dot{\gamma}(s) &= \dfrac{d \Lambda^{\mu}_{\mu '} x'^{\mu '} \cdot \gamma}{ds} e_\mu \\
&= \Lambda^\mu_{\mu '} \dfrac{d x'^{\mu '} \cdot \gamma}{ds} e_\mu \\
&= \dfrac{d x'^{\mu '} \cdot \gamma}{ds} e'_{\mu'}
\end{aligned}
$$
We shall say that $\dot{\gamma}$ points towards the future or is future-oriented iff $\dfrac{d x^0 \cdot \gamma}{ds} > 0$ (well-defined in any Galilean frame since $SO^+(1,3)$, time component is conserved)

In that case, $x^0 \cdot \gamma$ is an increasing function, hence a bijection and we can parameterize $\gamma$ with $s$ or $x^0 \cdot \gamma$

Then
$$
\begin{aligned}
\eta(\dot{\gamma}(s), \dot{\gamma}(s)) &= \eta \left( \dfrac{d x^{\mu} \cdot \gamma}{ds} e_\mu, \dfrac{dx^\nu \cdot \gamma}{ds} e_\nu \right) = \eta_{\mu \nu} \dfrac{d x^{\mu} \cdot \gamma}{ds} \dfrac{dx^\nu \cdot \gamma}{ds} \\
&= -c^2 \left( \dfrac{dt}{ds} \right)^2 + \left( \dfrac{d \mathbf{x}}{ds} \right)^2 = -c^2 \left( \dfrac{dt}{ds} \right)^2 \left( 1 - \dfrac{\mathbf{v}^2}{c^2} \right) \leq 0 \text{ (causal curve)}
\end{aligned} 
$$
We shall say that *timeline* $\gamma \geq 0$ is parameterized by proper time $\tau$ if $\forall \, \tau \in \mathbb{R}$
$$
\eta(\dot{\gamma}(\tau),\dot{\gamma}(\tau)) = -1
$$
Then
$$
+1 = + c^2 \left( \dfrac{dt}{ds} \right)^2 \left( 1 - \dfrac{\mathbf{v}^2}{c^2} \right) 
$$
So
$$
d\tau = dt \sqrt{1-\dfrac{\mathbf{v}^2}{c^2}}
$$
Coordinate time in a frame in which the particle is at rest $\rightarrow$ comoving frame
**Definition:** given a causal curve $\gamma$ : $\mathbb{R} \rightarrow E$ with $M \leq N \in \gamma(\mathbb{R})$ 
Then, set the pseudo-length between $M$ and $N$ along $\gamma$ as
$$
\ell(\gamma, M, N) = \int_{S_M}^{S_N} ds \left[ \, -\eta(\dot{\gamma}(s), \dot{\gamma}(s)) \, \right]^{1/2}
$$
*Properties:*
1. $\ell(\gamma, M, N)$ is additive, i.e. for $M \leq N \leq P \in \gamma(\mathbb{R})$
$$
\ell(\gamma, M, P) = \ell(\gamma, M, N) + \ell(\gamma, N, P)
$$
2. $\ell(\gamma, M, N)$ is independent of the chosen frame
3. $\ell(\gamma, M, N)$ is independent of  parameterization of $\gamma$
4. $\ell(\gamma, M, N) = \int^{\tau_N}_{\tau_M} d\tau=\tau_N - \tau_M$

In some frame
$$
\ell(\gamma, M, N) = \int_{S_M}^{S_N} ds \left[ -\eta(\dot{\gamma}(s), \dot{\gamma}(s)) \right]^{1/2} = \int_{S_M}^{S_N} ds \left[\, -\eta_{\mu \nu} \dot{X}^{\mu}(s) \dot{X}^{\nu}(s) \, \right]^{1/2}
$$
Or
$$
\ell(\gamma, M, N) = \int_{S_M}^{S_N} ds \, L_0 (\dot{X}^0, \dotsc, \dot{X}^3)
$$
Hence, Euler-Lagrange equation
$$
0 = \dfrac{d}{ds} \dfrac{\partial L_0}{\partial \dot{x}^{\mu}} = -\dfrac{d}{ds}\left( \dfrac{\eta_{\mu \nu} \dot{X}^{\nu}}{L_0} \right)
$$
Parameterized $\gamma$ in term of proper time $\tau$
$$
0 = - \dfrac{d}{d\tau} \eta_{\mu \nu} \dot{X}^{\nu} = - \eta_{\mu \nu} \ddot{X}^{\nu}
$$
So 
$$
\ddot{X}^\mu = 0
$$


