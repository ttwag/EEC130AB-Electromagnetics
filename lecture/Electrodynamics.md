# Electrodynamics - Induction and Faraday's Law

Electrostatics and magnetostatics are separate in the static case.

In dynamics, they are related.

**Changes in the Magnetic Field Induce Electromotive Force that Results in a Current in a Wire Loop**

## 1. Maxwell's Equations

### Maxwell's Equation in Electrostatics

$$\oint \vec{E} \cdot d\vec{A} = \frac{Q_{enclosed}}{\epsilon_0}$$

$$\oint \vec{E} \cdot d\vec{l} = 0$$

$$\oint \vec{B} \cdot d\vec{A} = 0$$

$$\oint \vec{B} \cdot d\vec{l} = \mu_0 i$$

where $\mu_0 \epsilon_0 \frac{d \phi_E}{dt}$ is the displacement current.

### Maxwell's Equation in Electrodynamics

$$\oint \vec{E} \cdot d\vec{A} = \frac{Q_{enclosed}}{\epsilon_0}$$

$$\oint \vec{E} \cdot d\vec{l} = -\frac{d\phi_B}{dt}$$

$$\oint \vec{B} \cdot d\vec{A} = 0$$

$$\oint \vec{B} \cdot d\vec{l} = \mu_0 i + \mu_0 \epsilon_0 \frac{d \phi_E}{dt}$$

where $\mu_0 \epsilon_0 \frac{d \phi_E}{dt}$ is the displacement current.

## 2. Faraday's Law

It was found that a change in magnetic flux through N closed wire loop induces electromotive force (EMF)

$$V_{emf} = -N\frac{d\phi_B}{dt}$$

The EMF produced will result in current in a wire loop with resistance R:

$$I_{loop} = \frac{V_{emf}}{R}$$

### Lenz's Law
From the experiment, it was found that the polarity of the induced EMF always results in a current that produces a magnetic field that **opposes the change in magnetic flux**.