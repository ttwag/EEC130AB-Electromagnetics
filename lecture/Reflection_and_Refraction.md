# EM Wave Reflection and Refraction

Reflection Coefficient for EM wave that propagates from $\eta_1$ to $\eta_2$.

$$\Gamma = \frac{\eta_2 - \eta_1}{\eta_2 + \eta_1}$$

To find out the reflection and refraction behavior of EM waves, we need to use the boundary condition of the E and H fields.

## Reflection and Transmission

**Normal Incidence**: the wave vector k is perpendicular to the surface of the materials' boundary. 

Assume that we have a uniform plane wave traveling in the z direction and passing from medium 1 to medium 2

| | Incident | Reflected | Transmitted |
|---:| ---:|---:|---:|
| E Field | $\widetilde{E}^i(z) = \hat{x} E_0 ^i e^{-jk_1 z}$ | $\widetilde{E}^ \Gamma (z) = \hat{x} E_0 ^\Gamma e^{jk_1 z}$ | $\widetilde{E}^T(z) = \hat{x} E_0 ^T e^{-jk_2 z}$ |
| H Field | $\widetilde{H}^i(z) = \hat{y} \frac{E_0 ^i}{\eta_1} e^{-jk_1 z}$ | $\widetilde{H}^\Gamma (z) = -\hat{y} \frac{E_0 ^\Gamma}{\eta_1} e^{-jk_1 z}$ | $\widetilde{H}^i(z) = \hat{y} \frac{E_0 ^T}{\eta_2} e^{-jk_2 z}$ |

Due to the field's boundary conditions at z = 0, the **Incident wave + Reflected Wave = Transmitted Wave** at the boundary.

Therefore,

$$E_0^i + E_0 ^\Gamma = E_0 ^T$$

$$\frac{E_0 ^ i }{\eta_1} - \frac{E_0 ^ \Gamma}{\eta_1} = \frac{E_0 ^T}{\eta_2}$$

**Reflection Coefficient**

$$\Gamma = \frac{\eta_2 - \eta_1}{\eta_2 + \eta_1}$$

**Transmission Coefficient**

$$\tau = \frac{2\eta_2}{\eta_2 + \eta_1}$$

In addition,

$$\tau = 1 + \Gamma$$

Notice that the result is the same as those from the transmission line if we replace the intrinsic with characteristics impedance.

The transmission line could be thought of as a 1D EM Wave traveling from medium to medium.

## Standing Wave

The incidence and reflected wave form a standing wave

**Standing Wave Ratio**


## Power Flow in Reflection and Transmission

Power flow in medium 1

$$\vec{S}_{av} = \Big(\frac{|E_0^i|}{2 \eta_1} - |\Gamma|^2 \frac{|E_0^i|}{2 \eta_1} \Big)\hat{z}$$

Power flow in medium 2

$$\vec{S}_{av} =|\Gamma|^2 \frac{|E_0^i|}{2 \eta_2} \hat{z}$$

