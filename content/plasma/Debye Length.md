---
title: Debye Length
draft: false
tags: []
---
The **Debye length** $\lambda_D$ characterizes the distance over which *electrostatic potentials* are screened in a plasma due to the presence of mobile charges. It shows how the potential of a charge is reduced due to the rearrangement of surrounding charges in the plasma.
## Assumptions
1. **Potential Impact**: Since ions are much heavier than electrons, we can assume that only electrons react to the potential source. 
2. **Boltzmann Distribution**: Describes how electron density $n_e$ responds to an electrostatic potential.
3. **Quasi-Neutrality**: The net charge density is small, but local perturbations can exist. 
## Poisson's Equation
Poisson's equation relates the Laplacian of the electrostatic potential $\phi$ to the charge density $\rho$:
$$

\nabla^2 \phi = -\frac{\rho}{\varepsilon_0}

$$
where:
- $\nabla^2 \phi$ is the Laplacian of the potential.
- $\rho$ is the charge density.
- $\varepsilon_0$ is the permittivity of free space.  
## Express Charge Density in Terms of Ion and Electron Densities
The total charge density $\rho$ in a plasma is given by:
$$\rho = e(n_i - n_e) $$
where:
- $e$ is the elementary charge.
- $n_i$ is the ion number density.
- $n_e$ is the electron number density.

In a quasi-neutral plasma, $n_i \approx n_0$ (the background ion density), and $n_e$ varies slightly with the potential $\phi$.
## Boltzmann Distribution for Electrons
The electron density $n_e$ in response to an electrostatic potential $\phi$ follows the Boltzmann distribution:
$$

n_e = n_0 \exp\left(-\frac{e \phi}{k_B T}\right)

$$
where:
- $n_0$ is the equilibrium electron density.
- $k_B$ is the Boltzmann constant.
- $T$ is the electron temperature.
## Linearize the Boltzmann Distribution

Assuming the potential $\phi$ is small ($e \phi / k_B T \ll 1$), we can linearize the exponential using a first-order Taylor expansion:
$$

n_e \approx n_0 \left(1 - \frac{e \phi}{k_B T}\right)

$$
The charge density $\rho$ then becomes:
$$

\rho = e(n_i - n_e) \approx e\left(n_0 - n_0 + n_0 \frac{e \phi}{k_B T}\right) = \frac{e^2 n_0 \phi}{k_B T}

$$
## Substitute into Poisson's Equation
Substitute the linearized charge density $\rho$ into Poisson's equation:
$$

\nabla^2 \phi = -\frac{\rho}{\varepsilon_0} = -\frac{1}{\varepsilon_0} \left(\frac{e^2 n_0 \phi}{k_B T}\right)

$$
This simplifies to:
$$

\nabla^2 \phi = \frac{\phi}{\lambda_D^2}

$$
where $\lambda_D$ is the **Debye length**.
## Debye Length
The **Debye length** $\lambda_D$ is given by:
$$

\lambda_D = \sqrt{\frac{\varepsilon_0 k_B T}{e^2 n_0}}

$$