---

layout: post  
title: "How do we show that SU(2) is compact?"  
categories: mathematics

---

To show that $\text{SU}(2)$ is a compact Lie group, we need to demonstrate that:

1. $\text{SU}(2)$ is a Lie group.
2. $\text{SU}(2)$ is compact.

### 1. $\text{SU}(2)$ as a Lie Group

The group $\text{SU}(2)$ is defined as the set of all $2 \times 2$ unitary matrices $U$ with determinant equal to 1:

```math
\text{SU}(2) = \{ U \in \text{GL}(2, \mathbb{C}) \mid U^\dagger U = I \text{ and } \det(U) = 1 \}.
```

Here:
- Unitarity ($U^\dagger U = I$) means $U$ preserves inner products and thus is an isometry, which implies its columns are orthonormal.
- $\det(U) = 1$ further restricts $U$ to matrices that can be continuously deformed to the identity matrix within the set of unitary matrices.

The structure of $\text{SU}(2)$ makes it a subgroup of $\text{GL}(2, \mathbb{C})$, the group of invertible $2 \times 2$ complex matrices. Since the unitary matrices form a smooth manifold, and the condition $\det(U) = 1$ is a smooth constraint, $\text{SU}(2)$ inherits a smooth manifold structure, making it a Lie group.

### 2. $\text{SU}(2)$ is Compact

To show compactness, we can parametrize $\text{SU}(2)$ explicitly. Any $U \in \text{SU}(2)$ can be written as

```math
U = \begin{pmatrix} \alpha & -\beta^* \\ \beta & \alpha^* \end{pmatrix},
```

where $\alpha, \beta \in \mathbb{C}$ and $|\alpha|^2 + |\beta|^2 = 1$ (a consequence of unitarity and the determinant condition).

This parametrization reveals that $U$ depends on four real parameters (the real and imaginary parts of $\alpha$ and $\beta$), subject to the constraint $|\alpha|^2 + |\beta|^2 = 1$. Therefore, $\text{SU}(2)$ is diffeomorphic to the 3-dimensional sphere $S^3$ in $\mathbb{R}^4$.

Since $S^3$ is a compact manifold, it follows that $\text{SU}(2)$ is also compact.

### Conclusion

Since $\text{SU}(2)$ is both a Lie group (a smooth manifold with a group structure) and compact, we conclude that $\text{SU}(2)$ is a compact Lie group.

---

### How do we know the 3-sphere manifold $S^3$ is compact?

To see why the 3-sphere $S^3$ is compact, let’s go through a couple of fundamental points about compactness and spheres in general.

### Definition of $S^3$
The 3-sphere $S^3$ in $\mathbb{R}^4$ is defined as the set of points in $\mathbb{R}^4$ at a fixed distance (radius) from the origin:

```math
S^3 = \left\{ (x_1, x_2, x_3, x_4) \in \mathbb{R}^4 \mid x_1^2 + x_2^2 + x_3^2 + x_4^2 = 1 \right\}.
```

This is the 3-dimensional analog of the 2-sphere $S^2$ in $\mathbb{R}^3$.

### Compactness of $S^3$
To show that $S^3$ is compact, we need to verify two things:
1. **Closedness:** $S^3$ is a closed subset of $\mathbb{R}^4$.
2. **Boundedness:** $S^3$ is bounded in $\mathbb{R}^4$.

#### 1. $S^3$ is Closed
The 3-sphere is defined by the equation $x_1^2 + x_2^2 + x_3^2 + x_4^2 = 1$, which represents a level set of a continuous function $f(x_1, x_2, x_3, x_4) = x_1^2 + x_2^2 + x_3^2 + x_4^2$. Since this function is continuous and $S^3$ is the preimage of the closed set $\{1\}$ under $f$, $S^3$ is closed in $\mathbb{R}^4$.

#### 2. $S^3$ is Bounded
Since every point $(x_1, x_2, x_3, x_4) \in S^3$ satisfies $x_1^2 + x_2^2 + x_3^2 + x_4^2 = 1$, all points on $S^3$ are within a distance of 1 from the origin. Therefore, $S^3$ is bounded in $\mathbb{R}^4$.

### Conclusion
Since $S^3$ is both closed and bounded in $\mathbb{R}^4$, the Heine-Borel theorem tells us that $S^3$ is compact. This compactness of $S^3$ implies that any topological space that is homeomorphic to $S^3$, including $\text{SU}(2)$, is also compact.