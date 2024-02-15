# Electrostatics

## Electrical Charge

**Definition**
* The source of an electrostatic field.
* The physical property of a material that causes it to experience a force when close to other electrically charged matters.
* Can be positive or negative.
* Unit: Coulomb (C).
* **Charge Conservation:** The Net charge is conserved just like energy cannot be created or destroyed.
* $e^- = -1.6*10^{-19} C$

**Coulomb's Law**

Force on $q_2$ from $q_1$ = 

$$\vec{F}_{21} = \frac{q_1 q_2}{4 \pi \epsilon_0 R_{12}^2} \hat{r}_{12}$$

,where $\hat{r}_{12}$ is the unit vector from charge $q_1$ to $q_2$.

* Magnitude is proportional to charges.
* Magnitude decreases with distance.
* $\epsilon_0 = 8.85 * 10^{-12} \frac{F}{m}$ is the permittivity of free space, and it has the unit $\frac{F}{m}$, which is the same as $C'$ from the transmission line.

## Electric Field
The vector that is equal in magnitude and direction to the force that would be exerted on a small test charge p carrying a charge of +1 from a charge with +q.

$$\vec{E}_p = \vec{F}_p = \frac{1}{4 \pi \epsilon_0} \frac{(+q) (+1)}{|\vec{R}|^2} \vec{r}_p$$

Why is it useful?

We can get the force by multiplying the E field by another charge $+q'$.

Given that we know $\vec{F}_p = \vec{E}_p (+q')$

Note: E field has the unit $\frac{N}{C}$. The +1 is unitless

**Electric Field From Multiple Charges**

Electric fields in a vacuum satisfy linear superposition.

The total field from multiple charges is the sum of fields from individual charges.

The sum of the N number of the E field at charge p:

$$\vec{E}_p = \frac{1}{4 \pi \epsilon_0} \sum_{i = 1}^{N} \frac{q_i}{|\vec{R} - \vec{R}_i|^2} \frac{\vec{R} - \vec{R}_i}{|\vec{R} - \vec{R}_i|}$$

## Charge Distribution

We characterize the charge distribution in terms of the **charge density**.

$Charge \space Density = \frac{Amount\space of\space Charge}{Unit\space of\space Space}$

**1D Line Charge Density**

$\rho_L = \frac{dq}{dl} \space (\frac{C}{m})$

$q = \int dq = \int \rho_L dl$

**2D Surface Charge Density**

$\rho_S = \frac{dq}{dA} \space (\frac{C}{m^2})$

$q = \int dq = \int \rho_S dA$

**3D Volume Charge Density**

$\rho_V = \frac{dq}{dV} \space (\frac{C}{m^3})$

$q = \int dq = \int \rho_V dV$

## Electric Field from a Charge Distribution

For a general distribution, we add up the contribution to the E field from each chunk of charge dq to point p.

$$\vec{E}_p = \int d\vec{E}_p$$

where $\vec{E}_p = \frac{dq}{4 \pi \epsilon_0 |\vec{R}|^2} \hat{R}$ and $\hat{R}$ is the vector pointing from dq to point p.

Given that we know the $\rho_V$ and $\vec{r_p} - \vec{r}$, the E field from a volume of charges is:

$$\int \frac{\rho_V(\vec{r}) dV}{4 \pi \epsilon_0 |\vec{r_p} - \vec{r}|^2} \frac{\vec{r_p} - \vec{r}}{|\vec{r_p} - \vec{r}|}$$

where $\vec{r_p} - \vec{r}$ is the vector subtraction between the position vector of the point $p$ and the chunk of volume in the integral. 

## Electric Scalar Potential

We want to solve the electrostatics problem with scalar quantity.

We know that the tiny work done along the path against the E field is $dV = -\vec{E} \cdot d\vec{l} = \frac{dW}{q}$

To move the charge from A to B, we need to do work. At point B, the charge has potential energy relative to point A: 

$$V_B - V_A = V_{AB} = \int_{A}^{B} dV = -\int_{A}^{B} \vec{E} \cdot d\vec{l} = \frac{Potential \space Energy}{Unit \space Charge} = \frac{J}{C}$$

### Potential From Point Charge

What's the electrostatic potential of a distance R from a point charge?

First, we want a reference point where there is no E field, which is at $R = \infty$

$$V(\vec{R}) = -\int_{A}^{B} \vec{E} \cdot d\vec{l} = -\int_{\infty}^{R} \frac{q}{4 \pi \epsilon_0 |\vec{R}'|^2}\hat{R}' \cdot \hat{R}' dR' = \frac{q}{4 \pi \epsilon_0 R}$$

### Potential From a Charge Distribution

The electrostatic potential at point p contributed by charge q is

$$dV_p = \frac{dq}{4 \pi \epsilon_0 |\vec{r}_p - \vec{r}|}$$

Now, the electrostatic potential from a volume charge density is:
$$V_p = \int dV_p = \int \frac{\rho_v(\vec{r})dV}{4 \pi \epsilon_0 |\vec{r}_p - \vec{r}|}$$

### Relationship to the E Field

$$\vec{E} = -\vec{\nabla} V$$

Force per charge = the negative of the change in potential per charge

## Gauss' Law

The amount of E field passes through a closed surface S

$$\oint_S \vec{E} \cdot d\vec{A} = \frac{Q}{\epsilon_0}$$

### Gauss' Law as a Tool
Applicable to the following symmetries:
* Spherical
* Cylindrical
* Planar

Steps
1. Identify symmetry in the field and write in simplified form.
2. Define S so that flux integral will be easy ($|\vec{E}|$ should be constant on S).
3. Evaluate the flux integral and enclosed charge.