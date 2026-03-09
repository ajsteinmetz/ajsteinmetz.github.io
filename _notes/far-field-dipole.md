---
layout: page
title: "Far-Field Electric Dipole"
---

# Far-Field Electric Dipole

## What we are trying to explain

One of the most important patterns in electrostatics is the **electric dipole field**.  
Unlike the Coulomb field of a single charge, which falls as

$$
E \sim \frac{1}{r^2},
$$

the field of a neutral pair of charges decreases more rapidly with distance.  
At large distances the dominant contribution behaves as

$$
E \sim \frac{1}{r^3}.
$$

This is the **dipole field**.

Rather than starting from the standard formula, our goal is to **derive the dipole field directly from Coulomb's law** by superposing the fields of two point charges. In particular we will

1. Write the exact electric field of two charges.
2. Evaluate the field in two symmetric directions:
   - along the dipole axis,
   - along the equatorial line.
3. Expand the result in the **far-field limit** \(r\gg s\).
4. Recognize the general vector expression

$$
\boxed{
\mathbf E(\mathbf r)
\approx
\frac{1}{4\pi\varepsilon_0}
\frac{1}{r^3}
\left[
3(\mathbf p\cdot\hat{\mathbf r})\hat{\mathbf r}-\mathbf p
\right]
}
\qquad (r\gg s).
$$

This derivation also provides a first encounter with an important idea in physics:  
**multipole expansions**.

---

# Setup: a physical dipole

Consider two point charges

- \(+q\)
- \(-q\)

separated by a distance \(s\) and centered at the origin.  
Let the dipole lie along the \(z\)-axis.

The charge locations are

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

Throughout this derivation we will eventually assume the **far-field limit**

$$
r\gg s,
$$

meaning the observation point is much farther away than the charge separation.

---

# Coulomb field of a point charge

For a point charge \(q\) located at position \(\mathbf r_0\), Coulomb's law gives

$$
\mathbf E(\mathbf r)
=
\frac{1}{4\pi\varepsilon_0}
q
\frac{\mathbf r-\mathbf r_0}{|\mathbf r-\mathbf r_0|^3}.
$$

Electrostatic fields obey **superposition**, so the total field of two charges is simply the vector sum of their individual fields.

---

# Exact dipole field

Applying superposition to the two charges gives

$$
\mathbf E(\mathbf r)
=
\frac{1}{4\pi\varepsilon_0}
q
\left(
\frac{\mathbf r-\mathbf r_{+}}{|\mathbf r-\mathbf r_{+}|^3}
-
\frac{\mathbf r-\mathbf r_{-}}{|\mathbf r-\mathbf r_{-}|^3}
\right).
$$

This expression is **exact**.  
Everything that follows consists of evaluating this expression in useful limits.

---

# Field on the dipole axis

First consider the observation point on the **dipole axis**, so

$$
\mathbf r = z\,\hat{\mathbf z},
\qquad z\gg s.
$$

Because of symmetry the field must lie along \(\hat{\mathbf z}\).

Substituting into the exact expression gives

$$
E_{\parallel}(z)
=
\frac{1}{4\pi\varepsilon_0}
q
\left[
\frac{1}{(z-\tfrac{s}{2})^2}
-
\frac{1}{(z+\tfrac{s}{2})^2}
\right].
$$

The physical meaning is clear: the closer charge produces a slightly larger field than the farther one.

---

# Combining the fractions

To make the scaling clearer, combine the two terms:

$$
\frac{1}{(z-\tfrac{s}{2})^2}
-
\frac{1}{(z+\tfrac{s}{2})^2}
=
\frac{2zs}{\left(z^2-\tfrac{s^2}{4}\right)^2}.
$$

Thus

$$
E_{\parallel}(z)
=
\frac{1}{4\pi\varepsilon_0}
q
\frac{2zs}{\left(z^2-\tfrac{s^2}{4}\right)^2}.
$$

---

# Far-field expansion on the axis

Now apply the far-field assumption \(z\gg s\).

Write the denominator as

$$
\left(z^2-\frac{s^2}{4}\right)^{-2}
=
z^{-4}
\left(
1-\frac{s^2}{4z^2}
\right)^{-2}.
$$

Because \(s^2/z^2\ll1\), the leading term is

$$
\left(z^2-\frac{s^2}{4}\right)^{-2}
\approx z^{-4}.
$$

Substituting this approximation gives

$$
\mathbf E_{\parallel}(z)
\approx
\frac{1}{4\pi\varepsilon_0}
q
(2zs)z^{-4}
\hat{\mathbf z}.
$$

Simplifying,

$$
\mathbf E_{\parallel}
\approx
\frac{1}{4\pi\varepsilon_0}
\frac{2qs}{z^3}
\hat{\mathbf z}.
$$

---

# Introducing the dipole moment

Define the **electric dipole moment**

$$
\boxed{
\mathbf p = q s\,\hat{\mathbf z}.
}
$$

Its magnitude is \(p=qs\) and its direction points from \(-q\) to \(+q\).

The axial field becomes

$$
\boxed{
\mathbf E_{\parallel}
\approx
\frac{1}{4\pi\varepsilon_0}
\frac{2p}{r^3}
\hat{\mathbf z}
}
\qquad
(r\gg s).
$$

---

# Field on the equatorial line

Now place the observation point perpendicular to the dipole axis:

$$
\mathbf r = x\,\hat{\mathbf x},
\qquad x\gg s.
$$

The displacement vectors from the charges are

$$
\mathbf r-\mathbf r_{\pm}
=
x\hat{\mathbf x}
\mp
\frac{s}{2}\hat{\mathbf z}.
$$

Both have the same magnitude

$$
|\mathbf r-\mathbf r_{\pm}|^2
=
x^2+\frac{s^2}{4}.
$$

Define

$$
R^2=x^2+\frac{s^2}{4}.
$$

---

# Superposing the fields

Substituting into the exact dipole field gives

$$
\mathbf E(x)
=
\frac{1}{4\pi\varepsilon_0}
q
\left(
\frac{x\hat{\mathbf x}-\tfrac{s}{2}\hat{\mathbf z}}{R^3}
-
\frac{x\hat{\mathbf x}+\tfrac{s}{2}\hat{\mathbf z}}{R^3}
\right).
$$

The \(x\)-components cancel exactly. Only the \(z\)-component survives:

$$
\mathbf E(x)
=
-\frac{1}{4\pi\varepsilon_0}
\frac{qs}{R^3}
\hat{\mathbf z}.
$$

The minus sign indicates that on the equatorial line the field points **opposite the dipole moment**.

---

# Equatorial far-field limit

Write the field as

$$
\mathbf E(x)
=
-\frac{1}{4\pi\varepsilon_0}
\frac{qs}{\left(x^2+\tfrac{s^2}{4}\right)^{3/2}}
\hat{\mathbf z}.
$$

Factor out \(x^2\):

$$
\left(x^2+\frac{s^2}{4}\right)^{-3/2}
=
x^{-3}
\left(
1+\frac{s^2}{4x^2}
\right)^{-3/2}.
$$

For \(x\gg s\),

$$
\left(x^2+\frac{s^2}{4}\right)^{-3/2}
\approx x^{-3}.
$$

Thus

$$
\boxed{
\mathbf E_{\perp}
\approx
-\frac{1}{4\pi\varepsilon_0}
\frac{p}{r^3}
\hat{\mathbf z}
}
\qquad
(r\gg s).
$$

---

# Comparing the two directions

At the same distance \(r\),

- **On-axis**

$$
E_{\parallel}
=
\frac{2p}{4\pi\varepsilon_0 r^3}
$$

- **Equatorial**

$$
E_{\perp}
=
\frac{p}{4\pi\varepsilon_0 r^3}
$$

Thus the field along the axis is **twice as large** as the field on the equatorial line.

---

# The general dipole field

The two special cases above are unified by the vector expression

$$
\boxed{
\mathbf E(\mathbf r)
\approx
\frac{1}{4\pi\varepsilon_0}
\frac{1}{r^3}
\left[
3(\mathbf p\cdot\hat{\mathbf r})\hat{\mathbf r}-\mathbf p
\right]
}
\qquad
(r\gg s).
$$

This formula encodes both the **angular dependence** and the **distance scaling** of the dipole field.

---

# Consistency checks

## On-axis

If \(\hat{\mathbf r}\parallel\mathbf p\),

$$
\mathbf p\cdot\hat{\mathbf r}=p
$$

so

$$
\mathbf E
=
\frac{1}{4\pi\varepsilon_0}
\frac{2p}{r^3}
\hat{\mathbf z}.
$$

---

## Equatorial line

If \(\mathbf p\cdot\hat{\mathbf r}=0\),

$$
\mathbf E
=
-\frac{1}{4\pi\varepsilon_0}
\frac{\mathbf p}{r^3}.
$$

Both agree with the results derived above.

---

# Physical interpretation

Several important ideas appear in this derivation.

- A dipole has **zero net charge**, so the leading \(1/r^2\) Coulomb term cancels.
- The first surviving contribution falls as

$$
E\sim\frac{1}{r^3}.
$$

- The field is strongly **directional**: it depends on the projection
  \( \mathbf p\cdot\hat{\mathbf r} \).

---

# A preview: multipole expansions

This derivation is actually the first example of a powerful idea used throughout physics:  
**multipole expansions**.

At large distances the electric field of any localized charge distribution can be written as a hierarchy

- monopole term \( \sim 1/r^2 \)
- dipole term \( \sim 1/r^3 \)
- quadrupole term \( \sim 1/r^4 \)
- higher moments

Each term reflects a different geometric property of the charge distribution.

The dipole moment \( \mathbf p \) is therefore the **leading descriptor of any neutral system** viewed from far away.

---
