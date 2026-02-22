---
layout: page
title: "Far-Field Electric Dipole"
---

# Far-Field Electric Dipole

Let us derive the far-field electric field of a dipole starting directly from the superposition of two Coulomb fields in Cartesian form. The goal is to connect the exact field of two separated charges to the familiar ideal dipole result,

$$
\mathbf E(\mathbf r)\approx \frac{1}{4\pi\varepsilon_0}\frac{1}{r^3}\left[3(\mathbf p\cdot\hat{\mathbf r})\hat{\mathbf r}-\mathbf p\right],\qquad r\gg s.
$$

Rather than jumping immediately to the general formula, we first examine two especially important directions:

- **On-axis** (parallel to the dipole moment)
- **Equatorial line** (perpendicular to the dipole moment)

These two cases make the $$1/r^3$$ scaling and directional structure very clear.

## 1. Setup: physical dipole and superposition

Consider a **physical dipole** made from two point charges $$+q$$ and $$-q$$, separated by a distance $$s$$, centered at the origin, and aligned with the $$z$$-axis. The charge locations are

$$
\mathbf r_{+}=\frac{s}{2}\hat{\mathbf z},\qquad\mathbf r_{-}=-\frac{s}{2}\hat{\mathbf z}.
$$

Let the observation point be

$$
\mathbf r=(x,y,z),\qquad r=\sqrt{x^2+y^2+z^2}.
$$

We are interested in the **far-field regime**, meaning $$r\gg s$$. That assumption means the observer is much farther away than the separation of the charges, so the two-charge system begins to look like an idealized point dipole.

### Coulomb field of a point charge

For a point charge $$q$$ located at $$\mathbf r_0$$, the electric field at $$\mathbf r$$ is

$$
\mathbf E(\mathbf r)=\frac{1}{4\pi\varepsilon_0}q\frac{\mathbf r-\mathbf r_0}{|{\mathbf r-\mathbf r_0}|^3}.
$$

### Dipole field by superposition

The dipole field is the field of $$+q$$ plus the field of $$-q$$. Writing it as “positive charge contribution minus negative charge contribution” gives

$$
\mathbf E(\mathbf r)=\frac{1}{4\pi\varepsilon_0}q\left(\frac{\mathbf r-\mathbf r_{+}}{|{\mathbf r-\mathbf r_{+}}|^3} - \frac{\mathbf r-\mathbf r_{-}}{|{\mathbf r-\mathbf r_{-}}|^3}\right).
$$

This expression is exact. The rest of the derivation is about simplifying it in special directions and then taking the far-field limit.

## 2. Field parallel to the dipole axis (on-axis)

To study the field **along the dipole axis**, place the observation point on the $$z$$-axis:

$$
\mathbf r=z\hat{\mathbf z},\qquad z\gg s.
$$

Because the geometry is symmetric about the $$z$$-axis, the field at this point must point purely in the $$\hat{\mathbf z}$$ direction. The exact axial field is

$$
E_{\parallel}(z)=\frac{1}{4\pi\varepsilon_0}q\left[\frac{1}{(z-\tfrac{s}{2})^2}-\frac{1}{(z+\tfrac{s}{2})^2}\right].
$$

This is already a nice result: it shows how the closer charge contributes a slightly stronger field than the farther charge, which is why the dipole field survives at long distances.

### Combine the terms

To expose the far-field scaling, combine the two fractions:

$$
\frac{1}{(z-\tfrac{s}{2})^2}-\frac{1}{(z+\tfrac{s}{2})^2}=\frac{2zs}{\left(z^2-\tfrac{s^2}{4}\right)^2}.
$$

So the exact on-axis field becomes

$$
E_{\parallel}(z)=\frac{1}{4\pi\varepsilon_0}q\frac{2zs}{\left(z^2-\tfrac{s^2}{4}\right)^2}.
$$

## 3. On-axis far-field expansion: inverse-cube leading term

Now apply the far-field assumption $$z\gg s$$. Rewrite the denominator in a form suitable for expansion:

$$
\left(z^2-\tfrac{s^2}{4}\right)^{-2}=z^{-4}\left(1-\frac{s^2}{4z^2}\right)^{-2}.
$$

For $$\frac{s^2}{z^2}\ll 1$$, the leading term is

$$
\left(z^2-\tfrac{s^2}{4}\right)^{-2}\approx z^{-4}+\mathcal O(z^{-6}).
$$

Substitute this into the field

$$
\mathbf E_{\parallel}(z)\approx\frac{1}{4\pi\varepsilon_0}q(2zs)z^{-4}\hat{\mathbf z}=\frac{1}{4\pi\varepsilon_0}\frac{2qs}{z^3}\hat{\mathbf z}.
$$

We define the dipole moment magnitude as $$p\equiv qs$$. Then the leading far-field on-axis result is

$$
\boxed{\mathbf E_{\parallel}\approx\frac{1}{4\pi\varepsilon_0}\frac{2p}{r^3}\hat{\mathbf z}\qquad (r\gg s,\ \text{on-axis})}.
$$

This is the first clear sign that a dipole field falls off as $$1/r^3$$, not $$1/r^2$$ like a single point charge. The $$1/r^2$$ behavior cancels because the net charge is zero.

## 4. Field perpendicular to the dipole axis (equatorial line)

Next, place the observation point on the $$x$$-axis, which is perpendicular to the dipole axis:

$$
\mathbf r=x\hat{\mathbf x},\qquad x\gg s.
$$

For the two charges, the displacement vectors are

$$
\mathbf r-\mathbf r_{\pm}=x\hat{\mathbf x}\mp \frac{s}{2}\hat{\mathbf z},
$$

and both have the same squared magnitude:

$$
|{\mathbf r-\mathbf r_{\pm}}|^2=x^2+\frac{s^2}{4}.
$$

Define

$$
R^2=x^2+\frac{s^2}{4}.
$$

This simplifies the algebra because the denominators are identical for the two contributions.

### Superpose the two fields

Substituting into the exact dipole field gives

$$
\mathbf E(x)=\frac{1}{4\pi\varepsilon_0}q\left(\frac{x\hat{\mathbf x}-\tfrac{s}{2}\hat{\mathbf z}}{R^3}-\frac{x\hat{\mathbf x}+\tfrac{s}{2}\hat{\mathbf z}}{R^3}\right).
$$

Now the $$x$$-components cancel exactly (by symmetry), leaving only a $$z$$-component:

$$
\mathbf E(x)=-\frac{1}{4\pi\varepsilon_0}\frac{qs}{R^3}\hat{\mathbf z}.
$$

This direction makes physical sense: on the equatorial line, the field points opposite the dipole moment direction.

## 5. Equatorial far-field expansion: inverse-cube leading term

Write the exact equatorial field explicitly as

$$
\mathbf E(x)=-\frac{1}{4\pi\varepsilon_0}\frac{qs}{\left(x^2+\tfrac{s^2}{4}\right)^{3/2}}\hat{\mathbf z}.
$$

To extract the far-field behavior for $$x\gg s$$, factor out $$x^2$$ from the denominator:

$$
\left(x^2+\frac{s^2}{4}\right)^{-3/2}=x^{-3}\left(1+\frac{s^2}{4x^2}\right)^{-3/2}.
$$

Keeping the leading term gives

$$
\left(x^2+\frac{s^2}{4}\right)^{-3/2}\approx x^{-3}+\mathcal O(x^{-5}).
$$

So the far-field equatorial result is

$$
\boxed{\mathbf E_{\perp}\approx-\frac{1}{4\pi\varepsilon_0}\frac{qs}{x^3}\hat{\mathbf z}=-\frac{1}{4\pi\varepsilon_0}\frac{p}{r^3}\hat{\mathbf z}\qquad (r\gg s,\ \text{equatorial})}.
$$

### Interpretation

Again we get the $$1/r^3$$ scaling, but the coefficient differs from the on-axis case:

- On-axis magnitude: $$\displaystyle \frac{2p}{4\pi\varepsilon_0 r^3}$$
- Equatorial magnitude: $$\displaystyle \frac{p}{4\pi\varepsilon_0 r^3}$$

So the on-axis field is twice as large (in magnitude) as the equatorial field at the same distance.

## 6. General far-field dipole result

We now package these results into the standard vector expression.

Define the dipole moment vector (pointing from $$-q$$ to $$+q$$):

$$
\mathbf p = qs\hat{\mathbf z}.
$$

For a general observation direction $$\hat{\mathbf r}=\mathbf r/r$$, the leading far-field term is

$$
\boxed{\mathbf E(\mathbf r)\approx\frac{1}{4\pi\varepsilon_0}\frac{1}{r^3}\left[3(\mathbf p\cdot\hat{\mathbf r})\hat{\mathbf r}-\mathbf p\right],\qquad r\gg s.}
$$

This compact formula encodes both magnitude and direction for any observation point in the far field.

## 7. Consistency checks with the special cases

It is always good practice to verify that the general formula reproduces the two cases we already derived.

### On-axis ($$\hat{\mathbf r}\parallel \mathbf p$$)

If $$\hat{\mathbf r}$$ is parallel to $$\mathbf p$$, then $$\mathbf p\cdot\hat{\mathbf r}=p$$, so

$$
\mathbf E = \frac{1}{4\pi\varepsilon_0}\frac{1}{r^3}\left(3p\hat{\mathbf z}-p\hat{\mathbf z}\right) = \frac{1}{4\pi\varepsilon_0}\frac{2p}{r^3}\hat{\mathbf z},
$$

which matches the on-axis result.

### Equatorial ($$\mathbf p\cdot\hat{\mathbf r}=0$$)

If the observation direction is perpendicular to $$\mathbf p$$, then $$\mathbf p\cdot\hat{\mathbf r}=0$$, so

$$
\mathbf E = -\frac{1}{4\pi\varepsilon_0}\frac{\mathbf p}{r^3}.
$$

For $$\mathbf p=p\hat{\mathbf z}$$, this becomes

$$
\mathbf E = -\frac{1}{4\pi\varepsilon_0}\frac{p}{r^3}\hat{\mathbf z},
$$

which matches the equatorial result.

## 8. Key takeaways

- A physical dipole is a **two-charge system with zero net charge**, so the leading $$1/r^2$$ monopole term cancels.
- The leading surviving term in the far field is the **dipole term**, which scales as
  $$
  \boxed{E \sim \frac{1}{r^3}}.
  $$
- The field depends on direction:
  - strongest on-axis,
  - weaker on the equatorial line,
  - and in general given by the vector formula involving $$\mathbf p$$ and $$\hat{\mathbf r}$$.

## Optional note for students

If you continue in electrostatics, this dipole result is the first example of a **multipole expansion**:

- monopole ($$1/r^2$$ field),
- dipole ($$1/r^3$$ field),
- quadrupole ($$1/r^4$$ field),
- etc.

That hierarchy is extremely useful in physics because it tells us which terms dominate at large distance.

---
