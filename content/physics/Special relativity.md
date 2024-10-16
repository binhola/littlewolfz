
## Four vectors
A four-vector is an object of four entries, under Lorentz transformation representing the change of reference frame. (transform like a (1, 0) Lorentz tensor)

$$
X^{\mu} = \begin{pmatrix} x^0 \\ x^1 \\ x^2 \\ x^3 \end{pmatrix}
$$
Change the frame $S \rightarrow S'$. We have $X^{\mu} \in S$ and $X'^{\mu} \in S'$ 

$$
X' = \begin{pmatrix} 
\gamma & -\beta \gamma & 0 & 0 \\
-\beta \gamma & \gamma & 0 & 0 \\
0 & 0 & 1 & 0 \\
0 & 0 & 0 & 1 
\end{pmatrix} X 
$$

## Coordinate transformations
### Galilean transformation
- Low velocities
$$
\begin{align}
t' &= t \\
x' &= x - vt
\end{align}
$$
Then the transformation can be written as

$$
G = \begin{pmatrix} 
1 & 0 & 0 & 0 \\
-v & 1 & 0 & 0 \\
0 & 0 & 1 & 0 \\
0 & 0 & 0 & 1 
\end{pmatrix}
$$
### Lorentz transformation

$$
L = \begin{pmatrix} 
\gamma & -\beta \gamma & 0 & 0 \\
-\beta \gamma & \gamma & 0 & 0 \\
0 & 0 & 1 & 0 \\
0 & 0 & 0 & 1 
\end{pmatrix}
$$
### Equivalent of Lorentz transformation at low velocities

Set $c=1$ 
Taylor expansion

$$
\gamma = (1-v^2)^{-1/2} = 1 + \dfrac{1}{2}v^2 + ...
$$

$$
\beta \gamma = v + \dfrac{v^3}{2} + ...
$$

Therefore,

$$
\begin{aligned}
t' &= \gamma t - \beta \gamma x = t - vx ? \\
x' &= -\beta \gamma t + \gamma x = -vt + x
\end{aligned} 
$$

## Lorentz covariance and invariance
Lorentz covariance belongs to representation of Lorentz group, transformation rule can be written using $\Lambda_\nu^\mu$ : $X'^\mu = \Lambda^{\mu}_\nu X^{\nu}$ 


## Klein-Gordon equation

Describe a particle moves really fast, behave relativistically. Physicist 1926 tried to describe $e^-$ movement. Klein-Gordon is not a successful equation for that. However, it turned out to characterise spinless relativistic particles such as pion $\pi^0,\, \pi^{\pm}$ and Higgs particle.

The relativistic dispersion relation must be followed. 

Four-momentum are defined as
$$
P^{\mu} = \left(\dfrac{E}{c},\, \vec{p} \right)
$$

$$
P^{\mu}P_{\mu} = m^2c^2 = \dfrac{E^2}{c^2} - |\vec{p}|^2
$$

Thus, 

$$
E^2 = p^2c^2 +m^2c^4
$$

In quantum mechanics, observables can be recovered by applied the operator to the wave function

$$
\hat A \psi = a\psi
$$

Energy operator

$$
E \rightarrow i\hbar c \dfrac{\partial}{\partial ct} = i\hbar c \partial_0
$$

Momentum operator

$$
\vec{p} \rightarrow -i\hbar \nabla = -i\hbar \partial_i
$$

Therefore,

$$
E^2 - p^2c^2 - m^2c^4 = 0
$$
can be replaced to be

$$
(-\hbar^2 \partial^{\mu}\partial_{\mu} - m^2 c^2)\psi = 0
$$

We can rewrite as

$$
(-\partial^\mu \partial_\mu - \kappa^2)\psi = 0 \quad \text{where} \quad \kappa^2 = \dfrac{m^2c^2}{\hbar^2}
$$
