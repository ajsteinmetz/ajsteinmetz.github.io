---
layout: page
title: "Far-Field Electric Dipole"
---

# Far-Field Electric Dipole

The ideal electric dipole field is one of the first places in electromagnetism where a “simple-looking” formula hides a lot of structure. It encodes both a directional pattern and a different distance-scaling than the Coulomb field of a single charge. Rather than starting from the final answer, let us derive it directly from the superposition of two point-charge fields in Cartesian form.

Our goal is to connect the exact two-charge field to the familiar far-field dipole expression,

$$
\mathbf E(\mathbf r)\approx \frac{1}{4\pi\varepsilon_0}\frac{1}{r^3}\left[3(\mathbf p\cdot\hat{\mathbf r})\hat{\mathbf r}-\mathbf p\right],\qquad r\gg s.
$$

We will first examine two especially useful directions:

- **On-axis** (parallel to the dipole moment)
- **Equatorial line** (perpendicular to the dipole moment)

These two limits already reveal the characteristic $$1/r^3$$ behavior and make the angular dependence much easier to interpret.

## Setup: a physical dipole and Coulomb superposition

Consider a **physical dipole** made from two point charges $$+q$$ and $$-q$$ separated by a distance $$s$$, centered at the origin, and aligned with the $$z$$-axis. Their positions are

$$
\mathbf r_{+}=\frac{s}{2}\hat{\mathbf z},\qquad
\mathbf r_{-}=-\frac{s}{2}\hat{\mathbf z}.
$$

Let the observation point be

$$
\mathbf r=(x,y,z),\qquad r=\sqrt{x^2+y^2+z^2}.
$$

We are interested in the **far-field regime**,

$$
r\gg s,
$$

meaning the observation distance is much larger than the charge separation. In that limit, the pair of charges begins to look like a single “effective object” (an ideal dipole) rather than two individually resolved charges.

### Coulomb field of one point charge

For a point charge $$q$$ located at $$\mathbf r_0$$, the electric field at $$\mathbf r$$ is

$$
\mathbf E(\mathbf r)=\frac{1}{4\pi\varepsilon_0}q\frac{\mathbf r-\mathbf r_0}{|{\mathbf r-\mathbf r_0}|^3}.
$$

### Exact dipole field from superposition

The field of the dipole is just the vector sum of the fields from the two charges. Writing the contribution from $$-q$$ explicitly as a subtraction gives

$$
\mathbf E(\mathbf r)=\frac{1}{4\pi\varepsilon_0}q\left(\frac{\mathbf r-\mathbf r_{+}}{|{\mathbf r-\mathbf r_{+}}|^3}-\frac{\mathbf r-\mathbf r_{-}}{|{\mathbf r-\mathbf r_{-}}|^3}\right).
$$

This expression is exact. Everything that follows is just careful simplification in special directions, followed by a far-field expansion.

## Field on the dipole axis (parallel case)

To study the field **along the dipole axis**, place the observation point on the $$z$$-axis:

$$
\mathbf r=z\hat{\mathbf z},\qquad z\gg s.
$$

By symmetry, the field must point purely along $$\hat{\mathbf z}$$. The exact axial field is

$$
E_{\parallel}(z)=\frac{1}{4\pi\varepsilon_0}q\left[\frac{1}{(z-\tfrac{s}{2})^2}-\frac{1}{(z+\tfrac{s}{2})^2}\right].
$$

This already contains the essential physics: the nearer charge contributes slightly more strongly than the farther charge, and that mismatch is what survives at large distance.

### Combine the two terms

To expose the scaling more clearly, combine the fractions:

$$
\frac{1}{(z-\tfrac{s}{2})^2}-\frac{1}{(z+\tfrac{s}{2})^2}
=\frac{2zs}{\left(z^2-\tfrac{s^2}{4}\right)^2}.
$$

So the exact on-axis field becomes

$$
E_{\parallel}(z)=\frac{1}{4\pi\varepsilon_0}q\frac{2zs}{\left(z^2-\tfrac{s^2}{4}\right)^2}.
$$

## On-axis far-field expansion

Now use the assumption $$z\gg s$$. Rewrite the denominator in a form suitable for expansion:

$$
\left(z^2-\tfrac{s^2}{4}\right)^{-2}=z^{-4}\left(1-\frac{s^2}{4z^2}\right)^{-2}.
$$

Since $$s^2/z^2\ll 1$$, the leading term is

$$
\left(z^2-\tfrac{s^2}{4}\right)^{-2}\approx z^{-4}+\mathcal O(z^{-6}).
$$

Substituting back into the field gives

$$
\mathbf E_{\parallel}(z)\approx\frac{1}{4\pi\varepsilon_0}q(2zs)z^{-4}\hat{\mathbf z}
=\frac{1}{4\pi\varepsilon_0}\frac{2qs}{z^3}\hat{\mathbf z}.
$$

Define the dipole moment magnitude by

$$
p\equiv qs.
$$

Then the leading on-axis far-field result is

$$
\boxed{\mathbf E_{\parallel}\approx\frac{1}{4\pi\varepsilon_0}\frac{2p}{r^3}\hat{\mathbf z}\qquad (r\gg s,\ \text{on-axis})}.
$$

This is the first clean appearance of the dipole scaling law: the field falls as $$1/r^3$$ rather than $$1/r^2$$. The reason is that the net charge is zero, so the monopole (Coulomb) contribution cancels.

## Field on the equatorial line (perpendicular case)

Next, place the observation point on the $$x$$-axis, perpendicular to the dipole axis:

$$
\mathbf r=x\hat{\mathbf x},\qquad x\gg s.
$$

For the two charges, the displacement vectors are

$$
\mathbf r-\mathbf r_{\pm}=x\hat{\mathbf x}\mp \frac{s}{2}\hat{\mathbf z},
$$

and both have the same squared magnitude,

$$
|{\mathbf r-\mathbf r_{\pm}}|^2=x^2+\frac{s^2}{4}.
$$

It is convenient to define

$$
R^2=x^2+\frac{s^2}{4},
$$

so that both denominators are the same.

### Superpose the fields

Substituting into the exact dipole field,

$$
\mathbf E(x)=\frac{1}{4\pi\varepsilon_0}q\left(\frac{x\hat{\mathbf x}-\tfrac{s}{2}\hat{\mathbf z}}{R^3}-\frac{x\hat{\mathbf x}+\tfrac{s}{2}\hat{\mathbf z}}{R^3}\right).
$$

The $$x$$-components cancel exactly (as they must by symmetry), leaving only a $$z$$-component:

$$
\mathbf E(x)=-\frac{1}{4\pi\varepsilon_0}\frac{qs}{R^3}\hat{\mathbf z}.
$$

The minus sign is physically meaningful: on the equatorial line, the field points opposite to the dipole moment direction.

## Equatorial far-field expansion

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
\left(x^2+\frac{s^2}{4}\right)^{-3/2}\approx x^{-3}+\mathcal O(x^{-5}).
$$

So the far-field equatorial result is

$$
\boxed{\mathbf E_{\perp}\approx-\frac{1}{4\pi\varepsilon_0}\frac{qs}{x^3}\hat{\mathbf z}
=-\frac{1}{4\pi\varepsilon_0}\frac{p}{r^3}\hat{\mathbf z}\qquad (r\gg s,\ \text{equatorial})}.
$$

### What changed relative to the on-axis case?

Both directions have the same distance scaling $$1/r^3$$, but the coefficient differs:

- On-axis magnitude: $$\displaystyle \frac{2p}{4\pi\varepsilon_0 r^3}$$
- Equatorial magnitude: $$\displaystyle \frac{p}{4\pi\varepsilon_0 r^3}$$

So at the same distance, the on-axis field is twice the equatorial field in magnitude.

## The general far-field dipole field

We can now summarize the result in its standard vector form. Define the dipole moment vector (pointing from $$-q$$ to $$+q$$) as

$$
\mathbf p = qs\hat{\mathbf z}.
$$

Then for a general observation direction $$\hat{\mathbf r}=\mathbf r/r$$, the leading far-field term is

$$
\boxed{\mathbf E(\mathbf r)\approx\frac{1}{4\pi\varepsilon_0}\frac{1}{r^3}\left[3(\mathbf p\cdot\hat{\mathbf r})\hat{\mathbf r}-\mathbf p\right],\qquad r\gg s.}
$$

This compact expression reproduces both special cases and makes the angular structure of the dipole field manifest.

## Quick consistency checks

It is worth checking that the general expression reduces to the results derived above.

### On-axis: $$\hat{\mathbf r}\parallel \mathbf p$$

If $$\hat{\mathbf r}$$ is parallel to $$\mathbf p$$, then $$\mathbf p\cdot\hat{\mathbf r}=p$$, and

$$
\mathbf E=\frac{1}{4\pi\varepsilon_0}\frac{1}{r^3}\left(3p\hat{\mathbf z}-p\hat{\mathbf z}\right)
=\frac{1}{4\pi\varepsilon_0}\frac{2p}{r^3}\hat{\mathbf z},
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

## Takeaways

A few points are worth keeping in mind:

- A physical dipole has **zero net charge**, so the leading $$1/r^2$$ monopole field cancels.
- The first nonzero far-field term is the **dipole field**, with characteristic scaling
  $$
  \boxed{E\sim \frac{1}{r^3}}.
  $$
- The field is strongly directional: it is largest on-axis, smaller on the equatorial line, and in general determined by the projection $$\mathbf p\cdot\hat{\mathbf r}$$.

## A note for students: this is your first multipole expansion

This derivation is also a preview of a much broader idea in electromagnetism and mathematical physics: **multipole expansions**. At large distance, fields are organized into a hierarchy of terms,

- monopole ($$1/r^2$$ field),
- dipole ($$1/r^3$$ field),
- quadrupole ($$1/r^4$$ field),
- and so on.

That hierarchy is powerful because it tells us, almost immediately, which physical features of a source dominate at long range.

---
