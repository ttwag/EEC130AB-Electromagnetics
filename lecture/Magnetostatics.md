# Magnetostatics

Studies the magnetic field when current does not vary with time.

## 1. Current Density

We are interested in how much charge crosses the plane P in time $\Delta t$

![Figure10](./image/Figure10.png)

$\Delta l = |\vec{u}| \Delta t$

The charge inside the volume moved $\Delta l$ distance in time $\Delta t$, so

$\Delta q = (\Delta l \Delta s')\rho_v = |\vec{u}| \Delta t \Delta s' \rho_v$

Current = $\frac{\Delta q}{\Delta t} = |\vec{u}| \Delta s' \rho_v$

$$\vec{J} = \rho_v \vec{u} = \frac{Current}{Area}$$

$$I = \int_S \vec{J} \cdot d\vec{A} = |\vec{u}| \rho_v \Delta s' = \frac{Current}{Area} \Delta s'$$



**Continuity Equation of Current**

$$\vec{\nabla} \cdot \vec{J} + \frac{d\rho_v}{dt} = 0$$

Current density diverging from a point is the negative of the change in charge density at a point.

## 2. Magnetic Field and Force
Moving charges produce magnetic fields and those fields exert forces on moving charges.

The force exerted by the B field on a moving charge:

$$\vec{F}_{mag} = q \vec{v} \times \vec{B}$$

on a current carrying wire:

$$\vec{F}_{mag} = \int Id\vec{l} \times \vec{B}$$

where $d\vec{l}$ points in the direction of the current flow

Since the force points to a perpendicular direction, an electric charge moving through the B field follows a curved trajectory.

**Magnetic Field Does No Work**

The force is always perpendicular to the direction that the charge is moving toward.

## 3. Biot-Savart Law

Similar to the superposition of the E field, we can find the total E field by adding individual contributions of the B field.

$\vec{B}_p = \int d\vec{B}_p$

Each contribution of the B field is given by the Biot-Savart Law:

$$d\vec{B}_p = \frac{\mu_0}{4 \pi} \frac{Id\vec{l} \times \hat{R}}{|\vec{R}|^2}$$

where $\mu_0 = 4 \pi * 10^{-7} \frac{H}{m}$ is the permeability of free space and $\hat{R}$ is the vector from the current to the location of the B field.

**B field by a wire of length L on the z-axis in Cylindrical Coordinate**

$$\vec{B}_p = \frac{\mu_0 I}{4 \pi} \frac{L \hat{\phi}}{r \sqrt{r^2 + (\frac{L^2}{4})}}$$

Note that when r << L or when L approaches infinity, 

$$\vec{B}_p = \frac{\mu_0 I}{2\pi r} \hat{\phi}$$

## 4. Ampère's Laws

**Applicable only on Infinite cylinders or lines of current.**

**Although current in a finite cylinder produces a constant B field in the $\hat{\phi}$ direction from the previous calculation, it is not physical and the actual field is more complicated.**

If we have current flowing through space, we can draw a contour c and the B field piercing through the contour is proportional to the enclosed current.

$$\oint_c \vec{B} \cdot d\vec{l} = \mu_0 i$$

How to Use?
1. Find c so that $|\vec{B}|$ is constant.
2. $\oint_c \vec{B} \cdot d\vec{l} = |\vec{B}| \oint_c d\vec{l} = |\vec{B}|l = \mu_0 i$

**Differential Form**
$$\oint_c \vec{B} \cdot d\vec{l} = \mu_0 i \implies \int_S \Big( \vec{\nabla \times \vec{B}}\Big) d\vec{A} = \int_S \mu_0 \vec{J} \cdot d\vec{A}$$

$$\implies \vec{\nabla} \times \vec{B} = \mu_0 \vec{J}$$

## 5. Inductor
### Magnetic Flux
**Magnetic Flux:** magnetic fields flowing through an open surface S that has a boundary.

$$\phi_B = \int_S \vec{B} \cdot d\vec{A}$$

### Inductance

By applying the Biot-Savart Law on a closed loop to get the B field, we get the magnetic flux through the loop as:

$$\phi_B = \Big(\frac{\mu_0}{4 \pi}g\Big) I$$

with some constant g, and we could simplify the expression to

$$N \phi_B = LI$$

with N as the number of loop and L be the **inductance** of the loop

**Intuition**

By applying current to the wire, we produce magnetic flux, and vice versa. This is analogous to the capacitor, where the charge in the plate is proportional to the applied voltage and vice versa.

### Infinite Sheet of Current

Given an infinite sheet of current in the x-y plane with current flowing in the +x direction with a linear density of K, find the B field everywhere.

![Figure11](./image/Figure11.png)

If we look down from the top of the z-y plane, we will find that the B field produced by these currents only exists in $\hat{y}$ direction because of the symmetry.

![Figure12](./image/Figure12.png)

The B field is

$$\oint_c \vec{B} \cdot d\vec{l} = \mu_0 \int Kd\vec{l}$$

$$\implies |\vec{B}| l + |\vec{B}|l = \mu_0 Kl$$

$$\implies |\vec{B}| = \frac{\mu_0 K}{2}$$

$$
\vec{B}(z) =

\begin{cases}
    \big( \frac{\mu_0 K}{2} \big) \hat{y} & z < 0 \\
    -\big( \frac{\mu_0 K}{2} \big) \hat{y} &  z > 0
\end{cases}
$$


### Solenoid

![Figure13](./image/Figure13.png)

Consider a solenoid pointing in the z direction with current flowing out of the page.

If we think of the solenoid as two infinite sheets of current, we will find that the B field outside of the solenoid is zero and inside of the solenoid is: 

$$\vec{B} = 2 \Big(\frac{\mu_0 K}{2}\Big)\hat{z} = \frac{\mu_0 N I}{l}\hat{z}$$

where $K = \frac{NI}{l}$

$$N\phi_B = \int \vec{B} \cdot d\vec{A} = |\vec{B}| \int dA = |\vec{B}|A$$

$$L' = \frac{N\phi_B}{Il} = \frac{\mu_0 N^2}{l^2}A$$

## 6. Magnetic Material

Applying B field to materials causes the material to form magnetized domains that could be thought of a bar magnet with north and south pole.

$$\vec{B} = \mu_0 \vec{H} + \mu_0 \vec{M} = \mu_0\vec{H} + \mu_0 \chi_m \vec{H}$$

$$\implies \vec{B} = \mu_0(1 + \chi_m)\vec{H} = \mu_0 \mu_r \vec{H}$$

$$\vec{B} = \mu \vec{H}$$

where $\vec{H}$ is the applied field and $\vec{B}$ is the total field, and $\mu$ is the general permeability.

However, the magnetic response of the material depends on the material, and not all material gives a magnetic response.

This is in contrast to the polarization of material under the E field, which is a common response among different materials.


**In summary**,

$$\vec{\nabla} \times \vec{H} = \vec{J}_F$$

where $\vec{J}_F$ is the free current density.

Since 

$$\vec{\nabla} \times \vec{B} = \vec{\nabla} \times (\mu_0 \vec{H} + \mu_0 \vec{M}) = \vec{\nabla} \times \mu \vec{H} = \mu (\vec{\nabla} \times\vec{H}) = \mu \vec{J}_F$$

we could swap the free space permeability with the permeability of the material that we want to find the B field in.

## 7. Summary

* **Bio-Savart Law**: Go from current to B field.
* **Ampere's Law**: For symmetric currents with an infinite cylinder or line of current.
* **Inductance**: relate current to magnetic flux.

