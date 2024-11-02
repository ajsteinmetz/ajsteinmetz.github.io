---

layout: post  
title: "Why E = mc² and not E = ½mc²?"  
categories: physics

---

$\mathfrak{G}$

$$
\mathfrak{G}
$$

```math
\mathfrak{G}
```

It's easy to notice that the famous equation $E = mc^2$ is similar to the classical expression for kinetic energy $T = \frac{1}{2}mv^2$. Both are proportional to mass, and both have a "speed" (c or v) which is squared. That they are alike might prompt the question: why doesn't Einstein's equation include the factor of 1/2 like kinetic energy does? Did Einstein overlook this factor?

## Understanding rest energy vs. kinetic energy

First, it's important to recognize that $E = mc^2$ represents the **rest energy** of an object—the energy due to its mass when it is not in motion. In contrast, $T = \frac{1}{2}mv^2$ describes the kinetic energy arising from an object's motion in classical (nonrelativistic) mechanics.

Einstein didn't forget the 1/2; rather, his equation is included within a more comprehensive relationship between energy, mass, and momentum. To see how the kinetic energy term with the 1/2 factor emerges, let's delve into the full relativistic energy-momentum relation.

## The relativistic energy-momentum relation

In special relativity, the total energy $E$ and momentum $p$ of an object with rest mass $m$ are connected through the equation

$$
E^2 = m^2 c^4 + p^2 c^2.
$$

This fundamental relation arises from the Minkowski spacetime framework (defined by the metric tensor $\eta_{\mu\nu}$) and the definition of the four-momentum vector. The four-momentum is a combination of the traditional three-momentum you see $\vec{p}=(p_{1},p_{2},p_{3})$ and a time component $p_{0}$. Let's call the four-momentum capital $P^{\mu}=(p_{0},\vec{p})$ where $\mu\in{0,1,2,3}$. In a similar fashion to how we can take the dot product between Euclidean three-vectors to get the inner product $\vec{p}\cdot\vec{p}=p^{2}=p_{1}^{2}+p_{2}^{2}+p_{3}^{2}$, we can do the same with four-vectors. The "dot product" between four-vectors however uses the metric tensor $\eta_{\mu\nu}$

$$
P^{\mu}P_{\mu} = \eta_{\mu\nu}p^{\mu}p^{\nu} = m^{2}c^{2} = E^{2}/c^{2} - p^{2}.
$$

We see the above equation is our energy-momentum relation from earlier. When the object is at rest ($p = 0$), the equation simplifies to

$$
E = mc^2,
$$

which is the well-known rest energy formula. As an aside, if $m=0$, then we get the expression for the energy for massless particles such as the photon

$$
E = pc.
$$

## Expanding energy for small velocities

To bridge the gap between the relativistic and classical expressions, consider an object moving at a speed much less than the speed of light $(v \ll c)$, so that its momentum $p = mv$ is much smaller than $mc$. Under this condition, we can approximate the total energy by expanding the square root in the energy equation.

Starting with the energy $E$, we Factor out $m^2 c^4$ and write

$$
E = \sqrt{m^2 c^4 + p^2 c^2} = mc^2 \sqrt{1 + \left( \frac{p}{mc} \right)^2}.
$$

Let $x = \frac{p}{mc}$. Since $x \ll 1$ in the nonrelativistic limit, we can use the Taylor series expansion for $\sqrt{1 + x^2}$

$$
\sqrt{1 + x^2} = 1 + \frac{x^2}{2} - \frac{x^4}{8} + \ldots
$$

Neglecting higher-order terms ($x^4$ and beyond), we approximate

$$
\sqrt{1 + x^2} \approx 1 + \frac{x^2}{2}.
$$

Substituting back for $x$ we obtain

$$
E \approx mc^2 \left( 1 + \frac{1}{2} \left( \frac{p}{mc} \right)^2 \right) = mc^2 + \frac{p^2}{2m}
$$

so we see the energy of an object $(p\ll mc)$ is a mass-term and a momentum-term.

## Recovering classical kinetic energy

The first term $mc^2$ is the rest energy, and the second term $\frac{p^2}{2m}$ represents the kinetic energy in the nonrelativistic limit. Using the classical expression for momentum $p = mv$, we find

$$
T = \frac{p^2}{2m} = \frac{(mv)^2}{2m} = \frac{1}{2}mv^2.
$$

This shows us that the familiar 1/2 factor in kinetic energy naturally arises from the relativistic energy equation when considering low velocities. In this nonrelativistic limit, the equations of special relativity seamlessly transition into those of classical Newtonian mechanics.

_This post is based on a reddit comment I wrote in 2019._

---
