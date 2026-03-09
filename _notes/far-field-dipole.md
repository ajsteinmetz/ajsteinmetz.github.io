---
layout: page
title: "Far-Field Electric Dipole"
---

# Far-Field Electric Dipole

The electric field of a single point charge falls off as $$1/r^2$$. But many important charge distributions have zero net charge, so the leading Coulomb (monopole) term cancels. The simplest and most important example is the electric dipole. For an ideal dipole with dipole moment $$\mathbf p$$, the far-field electric field is

$$
\boxed{\mathbf E(\mathbf r)\approx \frac{1}{4\pi\varepsilon_0}\frac{1}{r^3}\left[3(\mathbf p\cdot\hat{\mathbf r})\hat{\mathbf r}-\mathbf p\right]} \qquad (r\gg s).
$$

This formula is compact, but it hides a great deal of structure.[^1] It tells us that

- the field falls off as $$1/r^3$$ rather than $$1/r^2$$,
- the field depends strongly on direction,
- and the dipole moment $$\mathbf p$$ is the quantity that controls the leading far-field behavior.

[^1]: This is also an example of a multipole expansion. At large distance, the field of a localized charge distribution is organized into a hierarchy: monopole, dipole, quadrupole, and so on. The dipole term is the first nonzero contribution when the total charge vanishes.

In this derivation we will build two special cases of that result directly from the superposition of the Coulomb fields of two point charges. Specifically, we will examine:

- **on-axis** (parallel to the dipole moment),
- **equatorial** (perpendicular to the dipole moment).

---

## Setup: a physical dipole and Coulomb superposition

Consider a physical dipole made from two point charges $$+q$$ and $$-q$$ separated by a distance $$s$$, centered at the origin, and aligned along the $$z$$-axis. Their positions are

$$
\mathbf r_{+}=\frac{s}{2}\hat{\mathbf z}, \qquad \mathbf r_{-}=-\frac{s}{2}\hat{\mathbf z}.
$$

Let the observation point be

$$
\mathbf r_{\rm obs}=(x,y,z), \qquad r_{\rm obs}=\sqrt{x^2+y^2+z^2}.
$$

We are interested in the far-field regime $$r_{\rm obs}\gg s$$, meaning that the observation distance is much larger than the charge separation. In that regime, the two charges are no longer resolved individually; instead, they act like a single effective object, namely an ideal dipole.

### Coulomb field of one point charge

For a point charge $$q$$ located at position $$\mathbf r_{\rm src}$$, the electric field at the observation point $$\mathbf r_{\rm obs}$$ is

$$
\mathbf E(\mathbf r_{\rm obs})=\frac{1}{4\pi\varepsilon_0}\,q\,\frac{\mathbf r_{\rm obs}-\mathbf r_{\rm src}}{|\mathbf r_{\rm obs}-\mathbf r_{\rm src}|^3}.
$$

### Exact field of the dipole

By superposition, and letting $$\mathbf r_{\rm src}=\mathbf r_{\pm}$$ and $$\mathbf r_{\rm obs}\to \mathbf r$$, the total field is the vector sum of the fields of the two charges,

$$
\mathbf E(\mathbf r)=\frac{1}{4\pi\varepsilon_0}q\left(\frac{\mathbf r-\mathbf r_{+}}{|\mathbf r-\mathbf r_{+}|^3}-\frac{\mathbf r-\mathbf r_{-}}{|\mathbf r-\mathbf r_{-}|^3}\right).
$$

We note that this expression is exact. The rest of the derivation is simply the careful extraction of its leading behavior when $$r\gg s$$.

---

## Field on the dipole axis

We first place the observation point on the dipole axis, so that

$$
\mathbf r=z\hat{\mathbf z}, \qquad z\gg s.
$$

By symmetry, the field must point purely in the $$\hat{\mathbf z}$$ direction.[^2] So it is enough to compute the scalar axial component. Using the exact superposition formula, we obtain

[^2]: On the dipole axis there is no preferred transverse direction, so any $$x$$- or $$y$$-component would violate rotational symmetry about the $$z$$-axis. The field therefore must lie along $$\hat{\mathbf z}$$.

$$
E_{\parallel}(z)=\frac{1}{4\pi\varepsilon_0}q\left[\frac{1}{(z-\tfrac{s}{2})^2}-\frac{1}{(z+\tfrac{s}{2})^2}\right].
$$

This already shows the basic mechanism: the contributions from the two charges are nearly equal at large distance, but not exactly equal. That slight mismatch is what survives as the dipole field.[^3]

[^3]: At large distance, each charge produces a field of order $$1/r^2$$. Because the charges are equal and opposite, those leading contributions cancel. The first nonvanishing remainder is smaller by one power of distance, giving the characteristic dipole scaling $$1/r^3$$.

We put the two fractions over a common denominator, yielding

$$
\frac{1}{(z-\tfrac{s}{2})^2}-\frac{1}{(z+\tfrac{s}{2})^2}=\frac{(z+\tfrac{s}{2})^2-(z-\tfrac{s}{2})^2}{\left(z^2-\tfrac{s^2}{4}\right)^2}.
$$

Now we simplify the numerator, resulting in

$$
(z+\tfrac{s}{2})^2-(z-\tfrac{s}{2})^2=2zs,
$$

so that

$$
E_{\parallel}(z)=\frac{1}{4\pi\varepsilon_0}\,q\,\frac{2zs}{\left(z^2-\tfrac{s^2}{4}\right)^2}.
$$

---

## Far-field expansion on the axis

Now use the assumption $$z\gg s$$. We can rewrite the denominator as

$$
\left(z^2-\tfrac{s^2}{4}\right)^{-2}=z^{-4}\left(1-\frac{s^2}{4z^2}\right)^{-2}.
$$

Since $$s^2/z^2\ll 1$$, the leading term is simply[^4]

[^4]: More explicitly, if $$u=s^2/(4z^2)$$, then $$(1-u)^{-2}=1+2u+3u^2+\cdots$$ for $$\abs u <1$$. Keeping only the leading term gives the far-field approximation used here.

$$
\left(z^2-\tfrac{s^2}{4}\right)^{-2}\approx z^{-4}.
$$

Substituting this back into the field yields

$$
\mathbf E_{\parallel}(z)\approx\frac{1}{4\pi\varepsilon_0}\,q(2zs)z^{-4}\,\hat{\mathbf z}=\frac{1}{4\pi\varepsilon_0}\,\frac{2qs}{z^3}\,\hat{\mathbf z}.
$$

We now define the dipole moment magnitude as $$p\equiv qs$$. Then the far-field result on the axis becomes

$$
\boxed{\mathbf E_{\parallel}\approx\frac{1}{4\pi\varepsilon_0}\,\frac{2p}{r^3}\,\hat{\mathbf z}} \qquad (r\gg s,\ \text{on-axis}).
$$

This is our first clear appearance of dipole behavior: the field scales as $$1/r^3$$. The reason is that the total charge is zero, so the monopole $$1/r^2$$ term cancels.

---

## Field on the equatorial line

We next place the observation point on the $$x$$-axis, perpendicular to the dipole axis:

$$
\mathbf r=x\hat{\mathbf x}, \qquad x\gg s.
$$

For the two charges, the displacement vectors are

$$
\mathbf r-\mathbf r_{\pm}=x\hat{\mathbf x}\mp \frac{s}{2}\hat{\mathbf z},\qquad |\mathbf r-\mathbf r_{\pm}|^2=x^2+\frac{s^2}{4}
$$

It is convenient to define

$$
R^2=x^2+\frac{s^2}{4},
$$

so that both denominators are the same. Substituting into the exact dipole field gives

$$
\mathbf E(x)=\frac{1}{4\pi\varepsilon_0}q\left(\frac{x\hat{\mathbf x}-\tfrac{s}{2}\hat{\mathbf z}}{R^3}-\frac{x\hat{\mathbf x}+\tfrac{s}{2}\hat{\mathbf z}}{R^3}\right).
$$

The $$x$$-components cancel exactly, leaving only the $$z$$-component:

$$
\mathbf E(x)=-\frac{1}{4\pi\varepsilon_0}\frac{qs}{R^3}\hat{\mathbf z}.
$$

The minus sign is physically meaningful: on the equatorial line, the field points opposite to the dipole moment direction.[^5]

[^5]: The dipole moment points from $$-q$$ to $$+q$$. On the equatorial line, the horizontal components of the two Coulomb fields cancel, while the vertical components add in the direction opposite to $$\mathbf p$$.

---

## Far-field expansion on the equatorial line

Write the exact result explicitly as

$$
\mathbf E(x)=-\frac{1}{4\pi\varepsilon_0}\frac{qs}{\left(x^2+\tfrac{s^2}{4}\right)^{3/2}}\hat{\mathbf z}.
$$

Now factor out $$x^2$$ from the denominator:

$$
\left(x^2+\frac{s^2}{4}\right)^{-3/2}=x^{-3}\left(1+\frac{s^2}{4x^2}\right)^{-3/2}.
$$

For $$x\gg s$$, the leading term is

$$
\left(x^2+\frac{s^2}{4}\right)^{-3/2}\approx x^{-3}.
$$

So the far-field equatorial result is

$$
\boxed{\mathbf E_{\perp}\approx-\frac{1}{4\pi\varepsilon_0}\frac{qs}{x^3}\hat{\mathbf z}=-\frac{1}{4\pi\varepsilon_0}\frac{p}{r^3}\hat{\mathbf z}} \qquad (r\gg s,\ \text{equatorial}).
$$

---

## Quick consistency checks

It is worth verifying that the general formula reproduces the two special cases derived above.

### On-axis: $$\hat{\mathbf r}\parallel \mathbf p$$

If $$\hat{\mathbf r}$$ is parallel to $$\mathbf p$$, then $$\mathbf p\cdot\hat{\mathbf r}=p$$, and

$$
\mathbf E=\frac{1}{4\pi\varepsilon_0}\frac{1}{r^3}\left(3p\hat{\mathbf z}-p\hat{\mathbf z}\right)=\frac{1}{4\pi\varepsilon_0}\frac{2p}{r^3}\hat{\mathbf z},
$$

which matches the on-axis result.

### Equatorial: $$\mathbf p\cdot\hat{\mathbf r}=0$$

If the observation direction is perpendicular to $$\mathbf p$$, then $$\mathbf p\cdot\hat{\mathbf r}=0$$, so

$$
\mathbf E=-\frac{1}{4\pi\varepsilon_0}\frac{\mathbf p}{r^3}.
$$

For $$\mathbf p=p\hat{\mathbf z}$$, this becomes

$$
\mathbf E=-\frac{1}{4\pi\varepsilon_0}\frac{p}{r^3}\hat{\mathbf z},
$$

which matches the equatorial result.

---

## Takeaways

A few points are worth keeping in mind:

- A physical dipole has zero net charge, so the leading $$1/r^2$$ monopole field cancels.
- The first nonzero far-field term is the dipole field, with characteristic scaling $$E\sim 1/r^3$$.
- The field is strongly directional: it is largest on-axis, smaller on the equatorial line, and in general determined by the projection $$\mathbf p\cdot\hat{\mathbf r}$$.

This is the essential physical content of the far-field dipole approximation.

---
