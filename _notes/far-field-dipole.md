---
layout: page
title: "Far-Field Electric Dipole"
---

# Far-Field Electric Dipole

## What we are trying to explain

The electric field of a single point charge falls off as $$1/r^2$$.  
But many important charge distributions have **zero net charge**, so the leading Coulomb
(monopole) term cancels. The simplest and most important example is the
**electric dipole**.

For an ideal dipole with dipole moment $$\mathbf p$$, the far-field electric field is

$$
\boxed{
\mathbf E(\mathbf r)\approx \frac{1}{4\pi\varepsilon_0}\frac{1}{r^3}
\left[3(\mathbf p\cdot\hat{\mathbf r})\hat{\mathbf r}-\mathbf p\right]
}
\qquad (r\gg s).
$$

This formula is compact, but it hides a great deal of structure. It tells us that

- the field falls off as $$1/r^3$$ rather than $$1/r^2$$,
- the field depends strongly on direction,
- and the dipole moment $$\mathbf p$$ is the quantity that controls the leading far-field behavior.

In this derivation we will build that result directly from the superposition of the
Coulomb fields of two point charges. We will first examine two especially important
directions:

- **on-axis** (parallel to the dipole moment),
- **equatorial** (perpendicular to the dipole moment),

and then summarize the result in the standard vector form.

> **Remark.**  
> This is also your first real example of a **multipole expansion**.  
> At large distance, the field of a localized charge distribution is organized into a hierarchy:
> monopole, dipole, quadrupole, and so on. The dipole term is the first nonzero term
> when the total charge vanishes.

---

## Setup: a physical dipole and Coulomb superposition

Consider a **physical dipole** made from two point charges $$+q$$ and $$-q$$ separated by
a distance $$s$$, centered at the origin, and aligned along the $$z$$-axis.

Their positions are

$$
\mathbf r_{+}=\frac{s}{2}\hat{\mathbf z},
\qquad
\mathbf r_{-}=-\frac{s}{2}\hat{\mathbf z}.
$$

Let the observation point be

$$
\mathbf r=(x,y,z),
\qquad
r=\sqrt{x^2+y^2+z^2}.
$$

We are interested in the **far-field regime**

$$
r\gg s,
$$

meaning that the observation distance is much larger than the charge separation.
In that regime, the two charges are no longer resolved individually; instead, they act
like a single effective object, namely an ideal dipole.

### Coulomb field of one point charge

For a point charge $$q$$ located at position $$\mathbf r_0$$, the electric field at the
observation point $$\mathbf r$$ is

$$
\mathbf E(\mathbf r)=\frac{1}{4\pi\varepsilon_0}\,
q\,\frac{\mathbf r-\mathbf r_0}{|\mathbf r-\mathbf r_0|^3}.
$$

### Exact field of the dipole

By superposition, the total field is the vector sum of the fields of the two charges:

$$
\mathbf E(\mathbf r)=
\frac{1}{4\pi\varepsilon_0}q
\left(
\frac{\mathbf r-\mathbf r_{+}}{|\mathbf r-\mathbf r_{+}|^3}
-
\frac{\mathbf r-\mathbf r_{-}}{|\mathbf r-\mathbf r_{-}|^3}
\right).
$$

This expression is exact. The rest of the derivation is simply the careful extraction
of its leading behavior when $$r\gg s$$.

---

## Field on the dipole axis

We first place the observation point on the dipole axis, so that

$$
\mathbf r=z\hat{\mathbf z},
\qquad z\gg s.
$$

By symmetry, the field must point purely in the $$\hat{\mathbf z}$$ direction.
So it is enough to compute the scalar axial component.

Using the exact superposition formula, we obtain

$$
E_{\parallel}(z)=
\frac{1}{4\pi\varepsilon_0}q
\left[
\frac{1}{(z-\tfrac{s}{2})^2}
-
\frac{1}{(z+\tfrac{s}{2})^2}
\right].
$$

This already shows the basic mechanism: the contributions from the two charges are nearly
equal at large distance, but not exactly equal. That slight mismatch is what survives.

### Combine the two terms

Put the two fractions over a common denominator:

$$
\frac{1}{(z-\tfrac{s}{2})^2}-\frac{1}{(z+\tfrac{s}{2})^2}
=
\frac{(z+\tfrac{s}{2})^2-(z-\tfrac{s}{2})^2}
{\left(z^2-\tfrac{s^2}{4}\right)^2}.
$$

Now simplify the numerator:

$$
(z+\tfrac{s}{2})^2-(z-\tfrac{s}{2})^2=2zs.
$$

Therefore,

$$
E_{\parallel}(z)=
\frac{1}{4\pi\varepsilon_0}\,
q\,\frac{2zs}{\left(z^2-\tfrac{s^2}{4}\right)^2}.
$$

---

## Far-field expansion on the axis

Now use the assumption $$z\gg s$$. Rewrite the denominator as

$$
\left(z^2-\tfrac{s^2}{4}\right)^{-2}
=
z^{-4}\left(1-\frac{s^2}{4z^2}\right)^{-2}.
$$

Since $$s^2/z^2\ll 1$$, the leading term is simply

$$
\left(z^2-\tfrac{s^2}{4}\right)^{-2}\approx z^{-4}.
$$

Substitute this back into the field:

$$
\mathbf E_{\parallel}(z)
\approx
\frac{1}{4\pi\varepsilon_0}\,
q(2zs)z^{-4}\,\hat{\mathbf z}
=
\frac{1}{4\pi\varepsilon_0}\,
\frac{2qs}{z^3}\,\hat{\mathbf z}.
$$

Now define the dipole moment magnitude

$$
p\equiv qs.
$$

Then the far-field result on the axis becomes

$$
\boxed{
\mathbf E_{\parallel}
\approx
\frac{1}{4\pi\varepsilon_0}\,
\frac{2p}{r^3}\,\hat{\mathbf z}
}
\qquad
(r\gg s,\ \text{on-axis}).
$$

This is our first clear appearance of dipole behavior: the field scales as $$1/r^3$$.
The reason is that the total charge is zero, so the monopole $$1/r^2$$ term cancels.

---

## Field on the equatorial line

Next place the observation point on the $$x$$-axis, perpendicular to the dipole axis:

$$
\mathbf r=x\hat{\mathbf x},
\qquad
x\gg s.
$$

The displacement vectors from the two charges to the observation point are

$$
\mathbf r-\mathbf r_{\pm}
=
x\hat{\mathbf x}\mp \frac{s}{2}\hat{\mathbf z}.
$$

Their magnitudes are the same:

$$
|\mathbf r-\mathbf r_{\pm}|^2=x^2+\frac{s^2}{4}.
$$

Define

$$
R^2=x^2+\frac{s^2}{4}.
$$

Then the exact electric field becomes

$$
\mathbf E(x)=
\frac{1}{4\pi\varepsilon_0}q
\left(
\frac{x\hat{\mathbf x}-\tfrac{s}{2}\hat{\mathbf z}}{R^3}
-
\frac{x\hat{\mathbf x}+\tfrac{s}{2}\hat{\mathbf z}}{R^3}
\right).
$$

Now the $$x$$-components cancel exactly, leaving

$$
\mathbf E(x)=
-\frac{1}{4\pi\varepsilon_0}\frac{qs}{R^3}\hat{\mathbf z}.
$$

So the field on the equatorial line points in the **negative** $$\hat{\mathbf z}$$ direction,
that is, opposite to the dipole moment.

---

## Far-field expansion on the equatorial line

Write the exact result as

$$
\mathbf E(x)=
-\frac{1}{4\pi\varepsilon_0}
\frac{qs}{\left(x^2+\tfrac{s^2}{4}\right)^{3/2}}
\hat{\mathbf z}.
$$

Factor out $$x^2$$ from the denominator:

$$
\left(x^2+\frac{s^2}{4}\right)^{-3/2}
=
x^{-3}\left(1+\frac{s^2}{4x^2}\right)^{-3/2}.
$$

When $$x\gg s$$, the leading term is

$$
\left(x^2+\frac{s^2}{4}\right)^{-3/2}\approx x^{-3}.
$$

Therefore,

$$
\boxed{
\mathbf E_{\perp}
\approx
-\frac{1}{4\pi\varepsilon_0}\frac{qs}{x^3}\hat{\mathbf z}
=
-\frac{1}{4\pi\varepsilon_0}\frac{p}{r^3}\hat{\mathbf z}
}
\qquad
(r\gg s,\ \text{equatorial}).
$$

---

## Compare the two special directions

Both special cases have the same distance dependence:

$$
E\sim \frac{1}{r^3}.
$$

But the coefficients are different:

- on-axis magnitude:
  $$
  \frac{2p}{4\pi\varepsilon_0 r^3},
  $$
- equatorial magnitude:
  $$
  \frac{p}{4\pi\varepsilon_0 r^3}.
  $$

So at the same distance, the field on the axis is **twice** as large as the field on the
equatorial line.

This is our first indication that the dipole field is strongly directional.

---

## Dipole moment vector and the general far-field form

Define the dipole moment vector to point from the negative charge toward the positive charge:

$$
\mathbf p = qs\,\hat{\mathbf z}.
$$

Then the leading far-field term of the dipole field can be written in the standard vector form

$$
\boxed{
\mathbf E(\mathbf r)\approx
\frac{1}{4\pi\varepsilon_0}\frac{1}{r^3}
\left[
3(\mathbf p\cdot\hat{\mathbf r})\hat{\mathbf r}-\mathbf p
\right]
}
\qquad
(r\gg s).
$$

This single expression contains both of the special cases derived above.

> **Remark.**  
> The combination $$\mathbf p\cdot\hat{\mathbf r}$$ is the projection of the dipole moment
> onto the observation direction. This is what makes the angular dependence explicit.

---

## Quick consistency checks

It is always worth checking that the general expression reproduces the special cases.

### On-axis: $$\hat{\mathbf r}\parallel \mathbf p$$

If the observation direction is parallel to the dipole moment, then

$$
\mathbf p\cdot\hat{\mathbf r}=p.
$$

So

$$
\mathbf E=
\frac{1}{4\pi\varepsilon_0}\frac{1}{r^3}
\left(3p\hat{\mathbf z}-p\hat{\mathbf z}\right)
=
\frac{1}{4\pi\varepsilon_0}\frac{2p}{r^3}\hat{\mathbf z},
$$

which agrees with the axial result.

### Equatorial line: $$\mathbf p\cdot\hat{\mathbf r}=0$$

If the observation direction is perpendicular to the dipole moment, then

$$
\mathbf p\cdot\hat{\mathbf r}=0.
$$

So

$$
\mathbf E=
-\frac{1}{4\pi\varepsilon_0}\frac{\mathbf p}{r^3}.
$$

For $$\mathbf p=p\hat{\mathbf z}$$, this becomes

$$
\mathbf E=
-\frac{1}{4\pi\varepsilon_0}\frac{p}{r^3}\hat{\mathbf z},
$$

which matches the equatorial result.

---

## Why the dipole field falls off faster than the Coulomb field

A single isolated charge produces a field that behaves like

$$
E\sim \frac{1}{r^2}.
$$

A dipole, however, consists of two opposite charges whose total charge is zero. That means
the leading monopole contribution cancels. What remains is the next term in the large-distance
expansion, namely the dipole term, and that term behaves like

$$
\boxed{
E\sim \frac{1}{r^3}.
}
$$

This is a general and very important principle: whenever a lower multipole moment vanishes,
the next nonzero multipole moment controls the far-field behavior.

---

## Takeaways

A few central ideas are worth keeping in mind:

- A physical dipole has **zero net charge**, so the usual Coulomb $$1/r^2$$ term cancels.
- The first nonzero far-field contribution is the **dipole term**.
- The dipole field has characteristic scaling
  $$
  \boxed{E\sim \frac{1}{r^3}}.
  $$
- The field is not isotropic. It depends on direction through the factor
  $$
  \mathbf p\cdot\hat{\mathbf r}.
  $$

In other words, the dipole field is weaker at long distance than the field of a single charge,
but it also carries much richer directional structure.

---

## A note for students: this is your first multipole expansion

This derivation is the beginning of a much broader idea in electromagnetism and mathematical
physics. At large distance, the field of any localized source can be expanded into a sequence
of terms:

- monopole,
- dipole,
- quadrupole,
- and higher multipoles.

Each successive term falls off more rapidly with distance. So once you know which lower-order
moments vanish, you can often predict the large-distance behavior immediately.

For the dipole, the monopole moment is zero, so the dipole term becomes the leading contribution.
That is why the field falls as $$1/r^3$$ and why the dipole moment $$\mathbf p$$ becomes the key
quantity.

---
