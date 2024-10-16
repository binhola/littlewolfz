---
tags:
  - physics
  - plasma
---
## Debye shielding and Debye sphere
Debye shielding is a phenomenon when we insert a test charge inside a plasma, the free charged particles inside the plasma will surround the test charge, shielding the electrostatic potential from charge. This can happen if free charges do not have enough kinetic energy to overcome the attractive potential energy of the test charge. 

From the definition of [[Debye Length]], we can define a *Debye sphere* surrounding the test particle and also the number of particle inside the sphere:


$$

N_D = \dfrac{4}{3}\pi \lambda_D^3n_0

$$


where $\lambda_D$ is the Debye length, $n_0$ is the number density of plasma outside the Debye sphere.

We can insert the equation of *Debye length* and get:


$$

N_D = \dfrac{4}{3}\pi \dfrac{1}{\sqrt{n_0}} \left(\dfrac{\epsilon_0 k_B T}{e^2}\right)^{3/2} 

$$
## Characteristic time
In plasma, the *characteristic time* or *response time* represents the time scale over which the plasma responds to perturbations or external influences. In our case, the perturbation is our test charge. 

It suggests the ability of plasma to restore equilibrium when perturbation occur, linked to *plasma frequency*, which is the natural oscillation frequency of electrons in the plasma. 

### Continuity equation
Starting with the continuity equation:

$$

\frac{\partial \rho}{\partial t} + \nabla \cdot \mathbf{J} = 0

$$

where $\rho$ is the density of the plasma and $\mathbf{J}$ is the current density. 

We can linearly expand $\rho$ and $\mathbf{J}$ as:

$$

\rho(t) = en(t) = e(n_0+\delta n)

$$

$$

\mathbf{J}(t) = e(n_0 + \delta n)(v_0 + \delta \mathbf{v})

$$

Substitute into the continuity equation, we can reduce the derivatives over constant $n_0$ and $v_0$:

$$

\dfrac{\partial \delta n}{\partial t} + n_0 \nabla \cdot \delta \mathbf{v} + v_0 \cdot \nabla \delta n = 0

$$

Because the thermal equilibrium condition, we can ignore the last term on the left side ($v_0 = 0$):

$$

\dfrac{\partial \delta n}{\partial t} + n_0 \nabla \cdot \delta v = 0

$$

Differentiate the equation with respect to time $t$:

$$

\dfrac{\partial^2 \delta n}{\partial t^2} + n_0 \nabla \cdot \dfrac{\partial}{\partial t} \delta v = 0

$$
### Gauss's law
We know that  $\dfrac{\partial}{\partial t} \delta v=\mathbf{a}=\dfrac{\mathbf{F}}{m} = \dfrac{-e\mathbf{E}}{m}$. 

Substitute into the equation above:

$$

\dfrac{\partial^2 \delta n}{\partial t^2} + \dfrac{n_0(-e)}{m} \nabla \cdot \mathbf{E} = 0

$$

According to the Gauss's law:

$$

\nabla \cdot \mathbf{E} = \dfrac{\rho}{\epsilon_0} = \dfrac{-e\delta n}{\epsilon_0}

$$

This becomes:

$$

\dfrac{\partial^2 \delta n}{\partial t^2} + \dfrac{n_0(e^2)}{m\epsilon_0} \delta n = 0

$$

This is a second-order differential equation whose solutions represent a harmonic oscillator. 
By defining $\omega^2 =  \dfrac{n_0(e^2)}{m\epsilon_0}$, we can deduce the *characteristic time* $T$ as:

$$

T = \dfrac{2\pi}{\omega} = \dfrac{2\pi}{e} \sqrt{\dfrac{m\epsilon_0}{n_0}}

$$
