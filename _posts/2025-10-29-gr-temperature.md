---

layout: post  
title: "Time, Temperature, and Black Holes"  
categories: physics  
tags: time gravity "black holes" thermodynamics  

---

In physics, there is a very cool, but niche relationship between **temperature** and **time**. This relationship crops up in the realms of statistical mechanics, quantum theory, black holes, gravity, and spacetime. And it may offer insight into the relationship of gravity to the other fundamental interactions. On the face of it, the two concepts have little to do with one another: Time $$t$$ is the parameter in which we mark the separation between events in sequence as a system evolves, while temperature $$T$$ is a measure of the internal heat energy of a substance. But if we dig a little deeper into what exactly time and temperature _are_, we'll stumble into some intriguing links.

## What is temperature?

Temperature is... Well, it's actually a rather hard concept to pin down. Earlier we stated that it is the heat energy of something, and that is most people's understanding. If you touch something hotter than you, the vibrating energetic molecules in that substance will transfer energy into you, causing warming or even burning. In kinetic theory of gases, the temperature of an ideal gas is understood to be related to the kinetic energy via

$$
k_{B}T = \frac{1}{3}mv^{2} = \frac{2}{3}E_{\text{KE}}.
$$

Here, $$k_{B}$$ is the Boltzmann constant, $$m$$ the mass of the gas particles, and $$v$$ the average speed of the particles. This is perhaps the cleanest expression of temperature as kinetic energy, as we don't have any pesky intermolecular forces to get in the way like we do for non-ideal gases, liquids, or solids.

But this kinetic view isn't the full picture. In thermodynamics, temperature is more fundamentally defined in terms of entropy $$S$$ and internal energy $$E$$. The general definition is

$$
\beta \equiv \frac{1}{k_{B}T} = \frac{1}{k_{B}}\left( \frac{\partial S}{\partial E} \right)_{V,N},
$$

where the derivative is taken at constant volume $$V$$ and number of particles $$N$$. This expression tells us that temperature is a measure of how the entropy of a system changes with its energy. In other words, temperature quantifies the system's tendency to change its internal configurations (microstates) when energy is added.

This thermodynamic definition allows for some intriguing concepts, such as **negative temperatures**. In certain systems with a finite number of energy states—like spin systems in a magnetic field—it's possible for the population of particles to invert, meaning higher energy states become more populated than lower ones. In these cases, adding energy can actually decrease the entropy, leading to a negative value for $$(\partial S/\partial E)$$ and thus a negative temperature. Interestingly, negative temperatures are hotter than any positive temperature, as they represent systems with an inverted population distribution.

## What is time?

Now that I've hopefully convinced you that temperature is actually complicated, I wish to do the same for time. In classical mechanics and quantum mechanics, **time** is treated as an independent variable that parameterizes the evolution of a system. In quantum mechanics, the time evolution of a system is governed by the Schrödinger equation

$$
i\hbar \frac{\partial}{\partial t} \psi(t) = \hat{H} \psi(t),
$$

where $$\hbar$$ is the reduced Planck constant, $$\psi(t)$$ is the wave function at time $$t$$, and $$\hat{H}$$ is the Hamiltonian operator representing the total energy of the system. Here, time acts as a continuous parameter that moves the system from one state to another.

In Einstein's theory of **special relativity**, time is intertwined with space to form a four-dimensional spacetime. Time becomes a coordinate similar to spatial dimensions, but with a crucial difference in its signature $$(-,+,+,+)$$ in the spacetime interval

$$
ds^2 = -c^2 dt^2 + dx^2 + dy^2 + dz^2.
$$

This unification means that what one observer perceives as time may be a mix of time and space for another observer moving at a different velocity. Time dilation and length contraction are direct consequences of this relationship.

However, in the realm of quantum gravity, the concept of time becomes even more perplexing. The **problem of time** arises when attempting to merge quantum mechanics with general relativity. One notable manifestation is the Wheeler-DeWitt equation

$$
\hat{H} \Psi = 0,
$$

where $$\Psi$$ is the wave function of the universe, and $$\hat{H}$$ is the gravitational Hamiltonian constraint operator. Interestingly, this equation lacks an explicit time variable, suggesting that at a fundamental level, time might not exist in the way we perceive it.

## So how do time and temperature mix?

Now, you might be wondering how these two intricate concepts are connected. The bridge between time and temperature emerges in the mathematical formulations of quantum mechanics and statistical mechanics, particularly when we consider **imaginary time**. In quantum mechanics, the time evolution of a system is described by the unitary operator

$$
\hat{U}(t) = e^{-i \hat{H} t / \hbar}.
$$

In statistical mechanics, the partition function $$\mathcal{Z}$$, which encodes all thermodynamic information of a system, is given by

$$
\mathcal{Z} = \text{Tr}\left( e^{- \beta \hat{H}} \right),
$$

Notice the resemblance between these two expressions. If we perform a substitution known as a **Wick rotation**, where we replace real time $$t$$ with imaginary time $$t \rightarrow -i \tau$$, we get

$$
\hat{U}(-i \tau) = e^{- \hat{H} \tau / \hbar}.
$$

Setting $$\tau = \hbar \beta$$, we find

$$
\hat{U}(-i \hbar \beta) = e^{- \beta \hat{H} }.
$$

This suggests that evaluating quantum mechanical systems in imaginary time is mathematically equivalent to analyzing statistical systems at a finite temperature. Essentially, thermal fluctuations in a system at temperature $$T$$ correspond to quantum fluctuations over an imaginary time interval $$\tau$$.

This connection indicates that temperature can be viewed as a manifestation of periodicity in imaginary time. In path integral formulations, where one sums over all possible histories of a system, the imaginary time formalism becomes a powerful tool for studying finite-temperature quantum systems.

## How Do Black Holes and Hawking Radiation Fit Into This?

Black holes provide a fascinating context where the interplay between time and temperature becomes especially significant, particularly through the phenomenon of **Hawking radiation** where black holes are predicted to emit blackbody radiation at a temperature as a function of their mass. To see how this works, let's consider the Schwarzschild metric, which describes the spacetime geometry around a non-rotating, uncharged black hole

$$
ds^2 = -\left(1 - \frac{2GM}{rc^2}\right) c^2 dt^2 + \left(1 - \frac{2GM}{rc^2}\right)^{-1} dr^2 + r^2 d\Omega^2,
$$

where $$G$$ is the gravitational constant, $$M$$ is the mass of the black hole, and $$d\Omega^2$$ represents the angular part. By performing a Wick rotation to imaginary time, $$t \rightarrow i \tau$$, we obtain the Euclidean version of the metric

$$
ds_{E}^2 = \left(1 - \frac{2GM}{rc^2}\right) c^2 d\tau^2 + \left(1 - \frac{2GM}{rc^2}\right)^{-1} dr^2 + r^2 d\Omega^2.
$$

Near the event horizon $$(r \approx r_s = 2GM / c^2)$$, the metric simplifies, and the $$(\tau, r)$$ part resembles the flat two-dimensional Euclidean space in polar coordinates:

$$
ds^2 \approx \kappa^2 \rho^2 d\tau^2 + d\rho^2,
$$

where $$\kappa$$ is the surface gravity of the black hole, and $$\rho$$ is a radial coordinate related to $$r$$.

To avoid a conical singularity at the horizon (which would imply infinite curvature), the imaginary time coordinate $$\tau$$ must be periodic with period:

$$
\tau \sim \tau + \beta,
$$

where

$$
\beta = \frac{2\pi}{\kappa} = \frac{2\pi \hbar c^3}{G M k_B}.
$$

This periodicity corresponds to a temperature known as the **Hawking temperature**:

$$
T_H = \frac{\hbar c^3}{8\pi G M k_B}.
$$

The requirement of periodicity in imaginary time leads to the conclusion that black holes emit radiation like a blackbody at temperature $$T_H$$. This is Hawking radiation—a quantum effect arising from the interplay between gravity and quantum mechanics.

The near-horizon geometry exhibiting a $$2\pi$$ symmetry in imaginary time is isomorphic to the rotational symmetry of flat 2D Euclidean space in polar coordinates. This symmetry ensures smoothness of the spacetime manifold and links the concept of temperature to the geometry of spacetime.

In essence, the transformation to imaginary time reveals that the black hole's event horizon imposes a thermal structure on the spacetime, bridging the concepts of time and temperature. The black hole's temperature emerges from the periodicity in imaginary time, and the thermal radiation is a direct consequence of quantum fields interacting with the curved spacetime.

---

_The above is based in part on:_

- Gibbons, G. W., and S. W. Hawking. "Cosmological event horizons, thermodynamics, and particle creation." _Physical Review D_ **15.10** (1977): 2738. [10.1103/PhysRevD.15.2738](https://doi.org/10.1103/PhysRevD.15.2738)

- Antonelli, R. "A geometric proof of Hawking radiation, through imaginary time." _Hologrammata_ (2016). [https://rantonels.github.io/a-geometric-proof-of-hawking-radiation-through-imaginary-time/](https://rantonels.github.io/a-geometric-proof-of-hawking-radiation-through-imaginary-time/)

The second link is to a blog post by reddit user /u/rantonels who introduced me to the idea.

---

### The General Form of the Tolman–Ehrenfest effect

In a static spacetime characterized by a metric with a time–time component \( g_{00}(\vec{x}) \), the Tolman relation states that

\[
T(\vec{x}) \sqrt{-g_{00}(\vec{x})} = \text{constant}.
\]

This equation ensures that although the locally measured temperature \( T(\vec{x}) \) may vary with position, the “redshifted temperature” remains constant throughout the system. The quantity \( \sqrt{-g_{00}(\vec{x})} \) serves as the gravitational redshift factor.

---

### Weak-Field Approximation

In many practical scenarios—for instance, in a weak gravitational field—the metric can be written approximately as

\[
g_{00} \approx -\Bigl(1 + \frac{2\Phi(\vec{x})}{c^2}\Bigr),
\]

where \( \Phi(\vec{x}) \) is the gravitational potential (with the sign chosen so that it is negative in a gravitational well). In this approximation, the Tolman relation becomes

\[
T(\vec{x}) \approx \frac{T_0}{\sqrt{1 + \frac{2\Phi(\vec{x})}{c^2}}} \approx T_0 \left( 1 - \frac{\Phi(\vec{x})}{c^2} \right),
\]

with \( T_0 \) being the constant redshifted temperature observed at a reference location.

---

### Application to a Uniform Gravitational Field

Consider a uniform gravitational field. In many cases, the gravitational potential can be taken as

\[
\Phi(z) = -gz,
\]

where \( z \) is the vertical coordinate (with \( z = 0 \) at some reference level) and \( g \) is the gravitational acceleration. Substituting into the weak-field approximation:

\[
T(z) \approx T(0) \left( 1 + \frac{gz}{c^2} \right).
\]

Alternatively, thinking in differential form, the temperature gradient is given by

\[
\frac{dT}{dz} = -\frac{g}{c^2}\, T,
\]

which has the solution

\[
T(z) = T(0) \exp\left(-\frac{gz}{c^2}\right).
\]

**Note on Signs:**  
Be aware that the precise form (and whether the temperature increases or decreases with height) depends on the sign conventions chosen for the gravitational potential and the coordinate system. In many settings—especially in general relativity—the relation is best expressed in its invariant form, \( T(\vec{x}) \sqrt{-g_{00}(\vec{x})} = \text{constant} \), which avoids any ambiguity.

This effect, first derived by Richard C. Tolman (and developed with Paul Ehrenfest), implies that in a gravitational field, the condition for thermal equilibrium requires the local temperature to vary in a specific way with the gravitational potential, ensuring no net heat flow due to gravitational redshift.

---






