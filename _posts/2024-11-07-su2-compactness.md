---

layout: post  
title: "Proving that SU(2) is compact"  
categories: mathematics
tags: groups "Lie groups" 

---

The following derivation is the outcome of my own personal journey in trying to learn more group theory (and representation theory) which appears in many areas of physics. Despite the importance of groups in physics, I don't believe physicists are well-educated at the university level on this topic (or at least I wasn't) unless they go out of their way.

All too often physics texts throw out statements like "spin-1/2 particles transform under elements of the $$\text{SU}(2)$$ group" without taking the time to establish what any of this machinary means. Mathematics texts, on the other hand, are often written with a level of rigor and language that can be opaque to the average physicist. As a result, there's a plethora of books out there with titles like "Group Theory for Physicists" to varying levels of usefulness.

So the purpose of this post is to use a simple proof about the properties of the $$\text{SU}(2)$$ group as a Trojan horse to introduce concepts in group theory. I won't be starting from total scratch however, but some familiarity with mathematical notation will be needed to decipher what comes next. With that said, I'll try and stop to define vocabulary as it arises using footnotes.

### What is compactness?
Compactness of a group conveys that the set is "small" and bounded to some region of a larger space. In Euclidean space $$\mathbb{R}^n$$, the Heine-Borel theorem tells us that a set is compact if and only if it is closed and bounded. Therefore we need to verify two things about $$\text{SU}(2)$$:
1. **Closed:** A set is closed if it contains all its limit points.
2. **Bounded:** All elements in the set are within some finite distance of a fixed point.

### What is $$\text{SU}(2)$$?
The special unitary group (of degree 2)[^1] $$\text{SU}(2)$$ is defined as the set of all $$2 \times 2$$ unitary matrices $$U$$ with determinant equal to 1:

[^1]: The degree of a group tells us the size of its matrices. E.g. $$\text{SU}(n)$$ can be represented by $$n\times n$$ matrices. A specific element of the group however has $$d=n^2 - 1$$ dimensions or degrees of freedom. This makes $$\text{SU}(2)$$ have dimension $$d = 2^2 - 1 = 3$$ corresponding to three real parameters $$\mathbb{R}^3$$.

$$
\text{SU}(2) = \{ U \in \text{GL}(2, \mathbb{C}) \mid U^\dagger U = I \text{ and } \det(U) = 1 \}.
$$

If you've learned any quantum mechanics, then you'll know that such matrices are used to rotate the two-component spinors we define for spin-1/2 particles such as the electron. Let's break down the properties outlined above:
- $$\text{GL}(2, \mathbb{C})$$ is the **general linear group** of degree 2 which is all $$2\times2$$ complex matrices $$U$$ which are invertible $$U^{-1}U=I$$.
- Unitarity ($$U^\dagger U = I$$)[^2] means $$U$$ preserves inner products and thus is an isometry[^3], which implies its columns are orthonormal[^4].
- $$\det(U) = I$$ further restricts $$U$$ to matrices that can be continuously deformed[^5] to the identity matrix within the set of unitary matrices.

[^2]: The dagger notation $$U^\dagger$$ represents the complex conjugate transpose $$U^\dagger = (U^*)^T$$. For unitary matrices, the conjugate transpose is also the inverse $$U^\dagger = U^-1$$.

[^3]: An isometry is an operation $$U$$ which preserves distances and angles in a vector space. If we consider a pair of vectors $$\mathbf{u}$$ and $$\mathbf{v}$$, the inner product is then $$\mathbf{u}^\dagger\mathbf{v} = \sum_{k}^{N}u_{k}^{*}v_{k}$$. The operation $$\mathbf{v}\rightarrow U\mathbf{v}$$ therefore preserves the inner product as $$\mathbf{u}^\dagger U^\dagger U\mathbf{v} = \mathbf{u}^\dagger\mathbf{v}$$.

[^4]: If we denote the columns of $$U$$ as $$\mathbf{u}_{1}, \mathbf{u}_{2}, \dots, \mathbf{u}_n$$, then $$U^\dagger U = I$$ means that $$U^\dagger$$ times $$U$$ gives the identity matrix: $$(U^\dagger U)_{ij} = \mathbf{u}_i^\dagger \mathbf{u}_j = \delta_{ij}$$.

[^5]: A complex $$2\times2$$ unitary matrix can be parameterized by two complex phases $$(\phi,\psi)$$ and an angle $$\theta$$. For a suitable choice of complex phases and angle, this can be continuously deformed to the identity matrix within the group of unitary matrices. This property is also known as path-connectedness.

To show that $$\text{SU}(2)$$ is a compact Lie group, we need to demonstrate that:

1. $$\text{SU}(2)$$ is a Lie group.
2. $$\text{SU}(2)$$ is compact.

### 1. $$\text{SU}(2)$$ as a Lie Group

A Lie group is a group that is also a smooth manifold[^6]. The structure of $$\text{SU}(2)$$ makes it a subgroup of $$\text{GL}(2, \mathbb{C})$$, the group of invertible $$2 \times 2$$ complex matrices. Since the unitary matrices $U(n)$ form a smooth manifold, and the condition $$\det(U) = 1$$ is a smooth constraint[^7], $$\text{SU}(2)$$ inherits a smooth manifold structure, making it a Lie group. This is a very abbreviated description of Lie groups, but ultimately we want a group whose elements describe a geometry we can do calculus on.

[^6]: A smooth manifold (the underlying geometry) has the following properties: (a) We can assign coordinates (e.g. charts $$(x,y,z)$$) that define the space, (b) it locally resembles a Euclidean space $$\mathbb{R}^{n}$$, and (c) it is smooth letting us do calculus and differentiate.

[^7]: The determinant constraint doesn't stop us from doing calculus.

### 2. $$\text{SU}(2)$$ is Compact

To show compactness, we can parametrize $$\text{SU}(2)$$ explicitly. Any $$U \in \text{SU}(2)$$ can be written as

$$
U = \begin{pmatrix} \alpha & -\beta^* \\ \beta & \alpha^* \end{pmatrix},
$$

where $$\alpha, \beta \in \mathbb{C}$$ and $$\alpha\alpha^{\*} + \beta\beta^{\*} = 1$$ (a consequence of unitarity and the determinant condition). This parametrization reveals that $$U$$ depends on four $$n^2 = 2^2 = 4$$ real parameters given by the real and imaginary parts of $$\alpha$$ and $$\beta$$. Let $$\alpha = x_1 + i x_2$$ and $$\beta = x_1 + i x_4$$ where $$x_1, x_2, x_3, x_4 \in \mathbb{R}$$. Then

$$
|\alpha|^2 = x_1 ^2 + x_2 ^2\ \mathrm{and}\ |\beta|^2 = x_3 ^2 + x_4 ^2,
$$

allowing us recast the constraint as

$$
x_1 ^2 + x_2 ^2 + x_3 ^2 + x_4 ^2 = 1,
$$

which is the 3-sphere in $$\mathbb{R}^4$$. Therefore, $$\text{SU}(2)$$ is diffeomorphic[^8] to the 3-dimensional sphere $$S^3$$ in $$\mathbb{R}^4$$. Since $$S^3$$ is a compact manifold, it follows that $$\text{SU}(2)$$ is also compact.

[^8]: Diffeomorphic means we can write a (bijective) map $$f$$ between two manifolds $$f:M\rightarrow N$$ such that $f$ is smooth (preserves calculus) and smoothly invertible $$f^-1$$. This implies $$M$$ and $$N$$ are smoothly equivalent.

### How do we know the 3-sphere manifold $$S^3$$ is compact?

To see why the 3-sphere $$S^3$$ is compact, let’s go through a couple of fundamental points about compactness and spheres in general[^9]. The 3-sphere $$S^3$$ in $$\mathbb{R}^4$$ is defined as the set of points in $$\mathbb{R}^4$$ at a fixed distance (radius) from the origin:

[^9]: An n-sphere is defined by the condition $$\sum_i ^N x_i ^2 = 1$$ on $$\mathbb{R}^n$$.

$$
S^3 = \{ (x_1, x_2, x_3, x_4) \in \mathbb{R}^4 \mid x_1^2 + x_2^2 + x_3^2 + x_4^2 = 1 \}.
$$

This is the 3-dimensional analog of the 2-sphere $$S^2$$ in $$\mathbb{R}^3$$.

### Compactness of $$S^3$$
To show that $$S^3$$ is compact, we need to verify two things according to the Heine-Borel theorem:
1. **Closedness:** $$S^3$$ is a closed subset of $$\mathbb{R}^4$$.
2. **Boundedness:** $$S^3$$ is bounded in $$\mathbb{R}^4$$.

### 1. $$S^3$$ is Closed
The 3-sphere is defined by the equation $$x_1^2 + x_2^2 + x_3^2 + x_4^2 = 1$$, which represents a continuous function $$f:\mathbb{R}^4\rightarrow\mathbb{R}$$ defined by

$$
f(x_1, x_2, x_3, x_4) = x_1^2 + x_2^2 + x_3^2 + x_4^2.
$$

Since this function is continuous and $$S^3$$ is the preimage[^10] of the closed set $$\{1\}$$ under $$f$$

[^10]: The preimage $$f^{-1}(\{1\})$$ refers to all points in $$\mathbb{R}^4$$ that $$f$$ maps to 1. It's the set of solutions to $$x_1^2 + x_2^2 + x_3^2 + x_4^2 = 1$$, which defines $$S^3$$.

$$
S^3 = f^{-1}(\{1\}),
$$

therefore $$S^3$$ is closed in $$\mathbb{R}^4$$. I hope it is easy to see why $$\{1\}$$ is a _closed_ set! Due to the continuous nature of $$f$$, that closed property of $$\{1\}$$ transfers to $$S^3$$.

### 2. $$S^3$$ is Bounded
Since every point $$(x_1, x_2, x_3, x_4) \in S^3$$ satisfies $$x_1^2 + x_2^2 + x_3^2 + x_4^2 = 1$$, all points on $$S^3$$ are within a distance of 1 from the origin. Therefore, $$S^3$$ is bounded in $$\mathbb{R}^4$$.

QED -- at least in my naive way.

