
A fluid is a continuous medium characterized by following parameters
- Mass density $\rho$
- Pressure $p$
- Velocity $\vec{v}$
- Temperature $T$ (Plasma is collisional and Maxwellian)

## Continuity equation

### Flux

Consider particles in a box where the number of particle

$$
N = n A l
$$
where 
- $A$ is the cross-section area
- $l$ is the length of the box
- $n$ is the number density

Number of particles leave the box in time $\Delta t$

$$
\dfrac{N}{\Delta t} = \dfrac{nAl}{\Delta t} = n A v
$$
where $v$ is the velocity of particle moving perpendicular to the cross-section area

Particle flux $\equiv \dfrac{N}{\Delta t A} = n \vec{v}$

Mass flux $\equiv m n \vec{v} = \rho \vec{v}$

### Continuity equation

The continuity equation states that 

$$
\text{rate of change in the box = mass flow rate out - mass flow rate in}
$$

$$
\dfrac{dm}{dt} = \dfrac{dm_o}{dt} - \dfrac{dm_i}{dt}
$$

where $\dfrac{dmx_{o}}{dt} = \rho_{x_{o}} v_{x_{o}} dy dz$, similar for $x_i$

Therefore

$$
\dfrac{\partial \rho}{\partial t} dxdydz = (\rho_{x_o} v_{x_o} - \rho_{x_i} v_{x_i})dydz + (\rho_{y_o} v_{y_o} - \rho_{y_i} v_{y_i})dxdz + (\rho_{z_o} v_{z_o} - \rho_{z_i} v_{z_i})dxdy
$$

So,

$$
\dfrac{\partial \rho}{\partial t} = -\dfrac{\partial \rho_x v_x}{\partial x}-\dfrac{\partial \rho_y v_y}{\partial y}-\dfrac{\partial \rho_z v_z}{\partial z} = -\nabla (\rho \vec{v})
$$

Thus,

$$
\dfrac{\partial \rho}{\partial t} + \nabla(\rho \vec{v}) = 0
$$
## Momentum equation

We have

$$
\dfrac{dv}{dt} = \dfrac{\partial v}{\partial t} + \dfrac{\partial v}{\partial x} \dfrac{dx}{dt} + \dfrac{\partial v}{\partial y} \dfrac{dy}{dt} + \dfrac{\partial v}{\partial z} \dfrac{dz}{dt}
$$
Thus

$$
\dfrac{d\vec{v}}{dt} = \dfrac{\partial \vec{v}}{\partial t} + (\vec{v} \cdot \nabla) \vec{v}
$$

Multiply both side by $\rho$, we have the force

$$
\rho\dfrac{d\vec{v}}{dt} = \rho\dfrac{\partial \vec{v}}{\partial t} + \rho(\vec{v} \cdot \nabla) \vec{v} = n \vec{F} - \nabla P
$$


