---
layout: page
title: "Electric Dipole Field at (a,b): Cartesian Components"
---

# Electric Dipole Field at $$(a,b)$$

In the previous notes we considered the far-field expression for the electric field of an ideal dipole

$$
\mathbf E(\mathbf r)=\frac{1}{4\pi\varepsilon_0}\frac{1}{r^3}\left[3(\mathbf p\cdot\hat{\mathbf r})\hat{\mathbf r}-\mathbf p\right].
$$

along the dipole and equitorial axes. In many practical problems it is useful to evaluate this expression in Cartesian components at a specific point. In this note we compute the electric field at the point

$$
(x,y)=(a,b), \qquad a,b>0,
$$

for a dipole whose moment points along the $$x$$ direction.

---

## Setup: dipole aligned with $$\hat{\mathbf x}$$

Consider an ideal dipole at the origin with dipole moment

$$
\mathbf p = p\,\hat{\mathbf x}.
$$

We want the electric field at the point

$$
\mathbf r = a\,\hat{\mathbf x}+b\,\hat{\mathbf y}.
$$

The distance from the origin is therefore

$$
r=\sqrt{a^2+b^2}.
$$

The general dipole field formula will now be evaluated at this location.

---

## The dipole field formula

The electrostatic field of an ideal dipole at the origin can be rewritten[^1]

[^1]: The two expressions are identical because $$\mathbf r=r\hat{\mathbf r}$$, so $$\frac{3(\mathbf p\cdot\mathbf r)\mathbf r}{r^5}=\frac{3(\mathbf p\cdot r\hat{\mathbf r})(r\hat{\mathbf r})}{r^5}=\frac{3(\mathbf p\cdot\hat{\mathbf r})\hat{\mathbf r}}{r^3}$$.

$$
\boxed{\mathbf E(\mathbf r)=\frac{1}{4\pi\varepsilon_0}\left[\frac{3(\mathbf p\cdot\mathbf r)\mathbf r}{r^5}-\frac{\mathbf p}{r^3}\right].}
$$

To compute the field we therefore need

- the dot product $$\mathbf p\cdot\mathbf r$$,
- the vector $$\mathbf r$$,
- and the powers $$r^3$$ and $$r^5$$.

---

## Computing the dot product $$\mathbf p\cdot\mathbf r$$

With

$$
\mathbf p=p\,\hat{\mathbf x}, \qquad \mathbf r=a\,\hat{\mathbf x}+b\,\hat{\mathbf y},
$$

the dot product becomes

$$
\mathbf p\cdot\mathbf r=(p\,\hat{\mathbf x})\cdot(a\,\hat{\mathbf x}+b\,\hat{\mathbf y})=pa.
$$

The distance from the origin is

$$
r=\sqrt{a^2+b^2},
$$

so that

$$
r^3=(a^2+b^2)^{3/2}, \qquad r^5=(a^2+b^2)^{5/2}.
$$


---

## The $$x$$ and $$y$$ components

Insert $$\mathbf p\cdot\mathbf r = pa$$ and $$\mathbf r=a\hat{\mathbf x}+b\hat{\mathbf y}$$ into the general formula:

$$
\mathbf E(a,b)=\frac{1}{4\pi\varepsilon_0}\left[\frac{3(pa)(a\hat{\mathbf x}+b\hat{\mathbf y})}{(a^2+b^2)^{5/2}}-\frac{p\hat{\mathbf x}}{(a^2+b^2)^{3/2}}\right].
$$

We now extract the Cartesian components. The $$\hat{\mathbf y}$$ contribution comes only from the first term

$$
\boxed{E_y(a,b)=\frac{p}{4\pi\varepsilon_0}\frac{3ab}{(a^2+b^2)^{5/2}}}.
$$

The $$\hat{\mathbf x}$$ component receives contributions from both terms

$$
E_x(a,b)=\frac{1}{4\pi\varepsilon_0}\left[\frac{3pa\,a}{(a^2+b^2)^{5/2}}-\frac{p}{(a^2+b^2)^{3/2}}\right].
$$

Factor out $$p/(4\pi\varepsilon_0)$$ yeilding

$$
E_x(a,b)=\frac{p}{4\pi\varepsilon_0}\left[\frac{3a^2}{(a^2+b^2)^{5/2}}-\frac{1}{(a^2+b^2)^{3/2}}\right].
$$

To combine the terms, we rewrite the second denominator which gives

$$
\frac{1}{(a^2+b^2)^{3/2}}=\frac{a^2+b^2}{(a^2+b^2)^{5/2}}.
$$

Substitute this into the expression

$$
E_x(a,b)=\frac{p}{4\pi\varepsilon_0}\frac{3a^2-(a^2+b^2)}{(a^2+b^2)^{5/2}}.
$$

Simplifying the numerator gives

$$
\boxed{E_x(a,b)=\frac{p}{4\pi\varepsilon_0}\frac{2a^2-b^2}{(a^2+b^2)^{5/2}}}.
$$

---

## Quick consistency checks

Two useful limits confirm that the result behaves as expected.

### On the dipole axis ($$b=0$$)

$$
\mathbf E=\frac{p}{4\pi\varepsilon_0}\frac{2}{a^3}\hat{\mathbf x}.
$$

This matches the familiar on-axis dipole field.

### On the equatorial axis ($$a=0$$)

$$
\mathbf E=-\frac{p}{4\pi\varepsilon_0}\frac{1}{b^3}\hat{\mathbf x}.
$$

Here the field points opposite to the dipole moment, as expected for the equatorial line.

---

## The same result in polar form

It is helpful to rewrite the geometry in terms of plane polar coordinates. Let

$$
a=r\cos\theta,\qquad b=r\sin\theta,
$$

where

$$
r=\sqrt{a^2+b^2},\qquad \theta=\tan^{-1}\!\left(\frac{b}{a}\right).
$$

Substitute these into the Cartesian result:

$$
\mathbf E(a,b)=\frac{p}{4\pi\varepsilon_0}\frac{(2a^2-b^2)\hat{\mathbf x}+(3ab)\hat{\mathbf y}}{(a^2+b^2)^{5/2}}.
$$

Since $$a^2+b^2=r^2$$, the denominator becomes $$r^5$$, while the numerator becomes

$$
2a^2-b^2=2r^2\cos^2\theta-r^2\sin^2\theta=r^2(2\cos^2\theta-\sin^2\theta),
$$

and

$$
3ab=3r^2\sin\theta\cos\theta.
$$

Therefore

$$
\mathbf E(r,\theta)=\frac{p}{4\pi\varepsilon_0 r^3}\left[(2\cos^2\theta-\sin^2\theta)\hat{\mathbf x}+(3\sin\theta\cos\theta)\hat{\mathbf y}\right].
$$

Using the identities

$$
\hat{\mathbf r}=\cos\theta\,\hat{\mathbf x}+\sin\theta\,\hat{\mathbf y}, \qquad \hat{\boldsymbol\theta}=-\sin\theta\,\hat{\mathbf x}+\cos\theta\,\hat{\mathbf y},
$$

this can be rewritten in the standard polar-component form

$$
\boxed{\mathbf E(r,\theta)=\frac{p}{4\pi\varepsilon_0 r^3}\left(2\cos\theta\,\hat{\mathbf r}+\sin\theta\,\hat{\boldsymbol\theta}\right)}.
$$

This is the familiar dipole field in a plane containing the dipole axis. It makes the angular structure very clear:

- the radial component is proportional to $$2\cos\theta$$,
- the angular component is proportional to $$\sin\theta$$,
- and the overall magnitude still falls as $$1/r^3$$.

---
