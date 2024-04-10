# Electromagnetic Wave Propagation

In the transmission line section, we looked at wave propagation in 1 spatial coordinate. Here, we will look at 3D waves.

## Maxwell's Equation

**Integral Form**

$$\oint \vec{E} \cdot d\vec{A} = \frac{Q_{enclosed}}{\epsilon}$$

$$\oint \vec{E} \cdot d\vec{l} = -\frac{d\phi_B}{dt}$$

$$\oint \vec{B} \cdot d\vec{A} = 0$$

$$\oint \vec{B} \cdot d\vec{l} = \mu i + \mu \epsilon \frac{d \phi_E}{dt}$$

**Differential Form**

$$\vec{\nabla} \cdot \vec{E} = \frac{\rho}{\epsilon}$$

$$\vec{\nabla} \times \vec{E} = -\mu \frac{\partial \vec{H}}{\partial t}$$

$$\vec{\nabla} \cdot \vec{H} = 0$$

$$\vec{\nabla} \times \vec{H} = \epsilon \frac{\partial \vec{E}}{\partial t}$$

where $\mu_0 \epsilon_0 \frac{d \phi_E}{dt}$ is the displacement current.

**Intuition**: If we only look at the dynamic equations, the time-varying B field induces the circulating E field. Time-varying E field induces circulating B field.

![Figure14](./image/Figure14.png)

## Parallel Between the Transmission Line to Free Space

1-D Voltage and Current waves now turn to Electric and Magnetic field waves.

$$v(z, t) \implies \vec{E}(x, y, z, t)$$

$$i(z, t) \implies \vec{H}(x, y, z, t)$$

In source free ($\rho = 0, \vec{J} = 0$) vacuum, we have 

$$\vec{\nabla} \times \vec{E} = -\mu_0 \frac{\partial \vec{H}}{\partial t}$$

$$\vec{\nabla} \times \vec{H} = \epsilon_0 \frac{\partial \vec{E}}{\partial t}$$

which parallels to the lossless voltage and current PDE seen in the transmisstion line section, where

$$\frac{\partial v(z, t)}{\partial z} = - L'\frac{d i(z, t)}{d t}$$

$$\frac{\partial i(z, t)}{\partial z} = - C' \frac{dv(z, t)}{dt}$$

### Plane Wave Solution

Assume $\vec{E} = E_x(z, t) \hat{x}$ and $\vec{H} = H_y(z, t) \hat{y}$, so they are constant in planes of constant z with medium $\epsilon$ and $\mu$.

We  will get 

$$\vec{\nabla} \times \vec{E} = \frac{\partial{E_x}}{\partial z} \hat{y} $$

$$\vec{\nabla} \times \vec{H} = -\frac{\partial H_y}{\partial z}\hat{x}$$

If we plug these into the source-free vacuum equations, we will eventually get

$$\frac{\partial E_x}{\partial z} = -\mu \frac{\partial H_y}{\partial t}$$

$$\frac{\partial H_y}{\partial z} = -\epsilon \frac{\partial E_x}{\partial t}$$

they are very similar to the transmission line equation.

Furthermore, we could manipulate the equations into two **wave equations**. For example, 

$$
\begin{align}
& \frac{\partial E_x}{\partial z} = -\mu \frac{\partial H_y}{\partial t} \\
& \implies \frac{\partial}{\partial z}\frac{\partial E_x}{\partial z} = -\mu \frac{\partial}{\partial z}\frac{\partial H_y}{\partial t} \\
& \implies \frac{\partial^2 E_x}{\partial z^2} = -\mu \frac{\partial}{\partial t}\frac{\partial H_y}{\partial z} \\
& \implies \frac{\partial^2 E_x}{\partial z^2} = \mu \epsilon \frac{\partial^2 E_x}{\partial t^2}\\
\end{align}
$$

The phase velocity (**speed of light**) is $\frac{1}{\sqrt{\mu \epsilon}}$, which is parallel to $\frac{1}{\sqrt{L' C'}}$ from the transmission line.

The solution to this wave equation is 

$$E_x = E_0 cos(\omega t - k z)$$

$$H_y = \frac{E_0}{\eta} cos(\omega t - k z)$$

k is the wave number, $\frac{2 \pi}{\lambda}$

## Intrinsic Impedance

The Intrinsic Impedance relates the magnitude of E field to B field, just like the Characteristic Impedance relates the voltage and the current.

$$\eta = \sqrt{\frac{\mu}{\epsilon}}$$

where $\mu$ is the magnetic constant and $\epsilon$ is the electric constant,

and 

$$|\vec{E_x}| = \eta |\vec{H_y}| $$

In vacuum, 

$$\eta_0 = \sqrt{\frac{\mu_0}{\epsilon_0}} = 377 \space \Omega$$


## Phasors and Maxwell's Equations

**Maxwell's Equations in Phasor Domain**

If the time variation of the E and B field is sinusoidal with frequency $\omega$, then we can write the E and B field as:

$$\vec{E}(x, y, z, t) = Re \{ \bold{\vec{E}}(x, y, z) e^{j \omega t}\}$$

$$\vec{H}(x, y, z, t) = Re \{ \bold{\vec{H}}(x, y, z) e^{j \omega t}\}$$

where $\bold{\vec{E}}$ and $\bold{\vec{H}}$ are the E and B field phasors with vector quantity.

We can put the source-free Maxwell's Equation into the phasor domain by swapping the time derivatives with $j \omega$ and vectors with phasors.

$$\vec{\nabla} \cdot \bold{\vec{E}} = 0$$

$$\vec{\nabla} \times \bold{\vec{E}} = -\mu j\omega \bold{\vec{H}}$$

$$\vec{\nabla} \cdot \bold{\vec{H}} = 0$$

$$\vec{\nabla} \times \bold{\vec{H}} = \epsilon j\omega \bold{\vec{E}}$$

**Plain EM Wave in Phasor Domain**

Recall that the plain wave solutions are

$$\vec{E} = E_0 cos(\omega t - kz) \hat{x}$$

$$\vec{H} = \frac{E_0}{\eta}cos(\omega t - kz)\hat{y}$$

Since

$$\vec{E} = E_0 cos(\omega t - k z)\hat{x} = Re\{E_0 e^{j(\omega t - k z)}\hat{x}\} = Re\{E_0e^{-jkz}\hat{x}\space e^{j \omega t}\}$$

$$\vec{H} = H_0 cos(\omega t - k z)\hat{y} = Re\{H_0 e^{j(\omega t - k z)}\hat{y}\} = Re\{H_0e^{-jkz}\hat{y}\space e^{j \omega t}\}$$

In the phasor domain, they are 

$$\bold{\vec{E}} = E_0 e^{-jkz} \hat{x}$$

$$\bold{\vec{H}} = \frac{E_0}{\eta} e^{-jkz} \hat{y}$$

## Time-Harmonic Plane Waves in Any Direction

**E Field**

Assume we are in source-free condition,

Using the vector calculus property on the curl of E, we get

$$\vec{\nabla} \times (\vec{\nabla} \times \vec{E}) = \vec{\nabla} (\vec{\nabla} \cdot \vec{E}) - \vec{\nabla}^2 \vec{E}$$

Since the divergence of E is 0, we eventually will end up with 

$$ \vec{\nabla}^2 \vec{E} = \mu \epsilon \frac{\partial ^2}{\partial t^2}\vec{E}$$

Notice that this is a wave equation in 3-dimensional space.

In the phasor domain, the PDE takes in a form similar to the Helmholtz Equation in the transmission line

$$\vec{\nabla}^2 \bold{\vec{E}} + \mu \epsilon \omega^2\bold{\vec{E}} = 0$$

The general solution looks like

$$\bold{\vec{E}}(x, y, z) = \bold{\vec{E}}_0 e^{-j (k_x x+ k_y y+ k_z z)}$$

where

$$\bold{\vec{E}}_0 = \bold{E}_{0x}\hat{x} + \bold{E}_{0y}\hat{y} + \bold{E}_{0z}\hat{z}$$

**Wave Vector**

We will introduce a vector, the **wave vector**, which is 

$$\vec{k} = k_x \hat{x} + k_y \hat{y} + k_z \hat{z}$$

and 

$$\vec{k} \cdot \vec{r}(x, y, z) = k_x x + k_y y + k_z z$$

$$|\vec{k}| = k_x^2 + k_y^2 + k_z^2$$

If we put the general solution back to the phasor PDE, we get

$$|\vec{k}| = \sqrt{\mu \epsilon} \omega$$

**B Field**

By working with the E field phasor, we will get the magnetic field phasor

$$\bold{H} (\vec{r}) = \frac{1}{\eta} \hat{k} \times \bold{\vec{E}} (\vec{r})$$

where $\hat{k}$ points in the direction of $\vec{k}$

We can also find for the E field phasor that

$$\bold{E}(\vec{r}) = -\eta \hat{k} \times \bold{\vec{H}}(\vec{r})$$

**Geometric Restriction**



If we recall the Maxwell Equation in phasor form,

$$\vec{\nabla} \cdot \bold{\vec{E}} = 0$$

$$\implies (\frac{\partial}{\partial x}\hat{x} + \frac{\partial}{\partial y}\hat{y} + \frac{\partial}{\partial z}\hat{z}) \cdot \bold{\vec{E}}_0 e^{-j (k_x x+ k_y y+ k_z z)} = 0$$

$$\implies -(jk_x)E_{0x}e^{-j(k_x x+ k_y y+ k_z z)} -(jk_y)E_{0y}e^{-j(k_x x+ k_y y+ k_z z)} -(jk_z)E_{0z}e^{-j(k_x x+ k_y y+ k_z z)} = 0$$

$$\implies (-j)(\vec{k} \cdot \bold{\vec{E}}) = 0$$

Similarly, 

$$(-j)(\vec{k} \cdot \bold{\vec{H}}) = 0$$

We can conclude that 

$$\vec{k} \perp \bold{\vec{E}} $$

$$\vec{k} \perp \bold{\vec{H}} $$

From the cross product definition of E and B field, we further know that

$$\bold{\vec{E}} \perp \bold{\vec{H}} $$

## Material Property
* Nonmagnetic material means $\mu_r = 1$ and $\mu = \mu_0$
* Vacuum means $\epsilon = \epsilon_0$ and $\mu = \mu_0$
* The frequency of an EM wave is constant regardless of the material it's in. 
* The wavelength of an EM wave is NOT constant in different materials. It is $$\lambda = \frac{\lambda_0}{\sqrt{\epsilon_r \mu_r}}$$

## Conclusion

**Insert a Table**

