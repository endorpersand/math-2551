# 15.7: Triple Integrals in Cylindrical & Spherical Coordinates
## Cylindrical Coordinates
- Represent point $P$ in space by ordered triples $(r, \theta, z) \text{ } (r \geq 0)$

1. $r$ and $\theta$ are polar coordinates for the projection of $P$ onto the $xy$-plane
2. $z$ is the rectangular vertical coordinate

### Usage
Should be used when...
- there is an axis of symmetry
- an integrand involves $x^2 + y^2$
- we're integrating over a circle (or part of) in the $xy$-plane

Very similar to using polar coordinates w/ double integrals, but with an added $z$ component for triple integrals.

## Spherical Coordinates
- Represent point $P$ in space by ordered triples $(\rho, \phi, \theta)$

1. $\rho$ is distance from $P$ to the origin $(\rho \geq 0)$
2. $\phi$ is the angle $\overrightarrow{OP}$ makes with the $+z$-axis $(0 \leq \phi \leq \pi)$
3. $\theta$ is the angle from cylindrical coordinates

![[Pasted image 20220122000934.png|400]]
![[Screen Shot 2022-01-22 at 00.09.45.png|400]]

### Converting Rectangular to Spherical
$$
\Large
\begin{align*}
\rho^2 &= x^2 + y^2 + z^2 = r^2 + z^2\\\\
r &= \rho \sin \phi\\
z &= \rho \cos \phi\\\\
x &= r \cos\theta = \rho \sin \phi \cos \theta\\
y &= r \sin\theta = \rho \sin \phi \sin \theta\\

\end{align*}
$$

### Triple Integral Definition
$$
\Large
\iiint_T \,dV = \iiint_T \rho^2\sin\phi\,d\rho\,d\phi\,d\theta
$$

**Why?**

![[IMG_6645.jpg]]

$\Delta V$ is the curved box above. Assuming $\Delta V$ is a rectangular prism (when $\Delta V$ is very small, it's essentially a rectangular prism),
$$
\Large
\begin{align*}
\Delta V &= (\Delta \rho)\overbrace{(\rho \,\Delta \phi)}^{\mathclap{\text{arclength from the side}}}\underbrace{(r \,\Delta \theta)}_{\mathclap{\text{arclength from the top}}}\\\\
&= \rho r \,\Delta\rho \,\Delta\phi \,\Delta\theta\\
&= \rho (\rho \sin \phi) \,\Delta\rho \,\Delta\phi \,\Delta\theta\\
&= \rho^2 \sin\phi \,\Delta\rho \,\Delta\phi \,\Delta\theta\\\\
dV &= \rho^2 \sin\phi \,d\rho \,d\phi \,d\theta
\end{align*}
$$
Related: [[#Derivation of Spherical Triple Integral by Jacobians|purely algebraic derivation]]
# 15.8: Integration by Substitution
## Jacobians

**Jacobian determinate** or **Jacobian** of the coordinate transformation $x = g(u, v), y = h(u, v)$:
$$
\Large
J(u, v) = \left|\frac{\partial(x, y)}{\partial(u, v)}\right| = \begin{vmatrix}
\frac{\partial{x}}{\partial{u}}&\frac{\partial{x}}{\partial{v}}\\
\frac{\partial{y}}{\partial{u}}&\frac{\partial{y}}{\partial{v}}\\
\end{vmatrix} = \frac{\partial{x}}{\partial{u}}\frac{\partial{y}}{\partial{v}} - \frac{\partial{y}}{\partial{u}}\frac{\partial{x}}{\partial{v}}
$$
The two coordinate systems are related by:
$$
\Large
dx\,dy = \left|\frac{\partial(x, y)}{\partial(u, v)}\right|du\,dv
$$
**Why?**
The Jacobian transform maps the $uv$-coordinate system onto the $xy$-coordinate system.
In a mapping from $uv$ to $xy$, the area $du\,dv$ will be multiplied by a factor of the determinant of the transform (recall from linear algebra) to get the corresponding area $dx\,dy$.

**Extension into 3D**
Jacobians can also be extended pretty trivially to 3 dimensions.
Given $x=g(u, v, w), y=h(u,v, w), z=k(u,v, w)$,
$$
\Large
J(u, v, w) = \left|\frac{\partial(x, y, z)}{\partial(u, v, w)}\right| = \begin{vmatrix}
\frac{\partial{x}}{\partial{u}}&\frac{\partial{x}}{\partial{v}}&\frac{\partial{x}}{\partial{w}}\\
\frac{\partial{y}}{\partial{u}}&\frac{\partial{y}}{\partial{v}}&\frac{\partial{y}}{\partial{w}}\\
\frac{\partial{z}}{\partial{u}}&\frac{\partial{z}}{\partial{v}}&\frac{\partial{z}}{\partial{w}}\\
\end{vmatrix}
$$

## Double Integrals
Suppose $f(x, y)$ is continuous over region $R$. Let $G$ be preimage of $R$ under transform $x = g(u, v), y = h(u, v)$ (assumed to be one-to-one on interior of $G$). If functions $g$ and $h$ have continuous 1st partial derivatives within interior of $G$:
$$
\Large
\iint_Rf(x,y)\,dx\,dy = \iint_G f(g(u, v), h(u, v))\overbrace{\left|\frac{\partial(x, y)}{\partial(u, v)}\right|}^{\text{Jacobian}}\,du\,dv
$$
## Triple Integrals
$$
\Large
\begin{align*}
&\iiint_R f(x,y,z)\,dx\,dy\,dz \\
&= \iiint_G f(g(u,v,w),h(u,v,w), k(u,v,w))\left|\frac{\partial(x, y, z)}{\partial(u, v, w)}\right|\,du\,dv\,dw

\end{align*}
$$

### Derivation of Spherical Triple Integral by Jacobians
Spherical coordinates:
$$
\Large
\begin{align*}
x &= \rho\sin\phi\cos\theta \\
y &= \rho\sin\phi\sin\theta \\
z &= \rho\cos\phi
\end{align*}
$$

Derivation:
$$
\Large
\begin{align*}
dx\,dy\,dz &= \overbrace{\left|\frac{\partial(x, y, z)}{\partial(\rho, \phi, \theta)}\right|}^{\mathclap{\text{What we're trying to find}}}d\rho\,d\phi\,d\theta\\\\
\frac{\partial(x, y, z)}{\partial(\rho, \phi, \theta)}&=\begin{vmatrix}\frac{\partial{x}}{\partial\rho} & \frac{\partial{x}}{\partial\phi} & \frac{\partial{x}}{\partial\theta}\\
\frac{\partial{y}}{\partial\rho} & \frac{\partial{y}}{\partial\phi} & \frac{\partial{y}}{\partial\theta}\\
\frac{\partial{z}}{\partial\rho} & \frac{\partial{z}}{\partial\phi} & \frac{\partial{z}}{\partial\theta}
\end{vmatrix}\\
&= \begin{vmatrix}\sin\phi\cos\theta & \rho\cos\phi\cos\theta & -\rho\sin\phi\sin\theta\\
\sin\phi\sin\theta & \rho\cos\phi\sin\theta & \rho\sin\phi\cos\theta\\
\cos\phi & -\rho\sin\phi & 0
\end{vmatrix}\\\\
&= \cos\phi(\rho^2\sin\phi\cos\phi\cos^2\theta + \rho^2\sin\phi\cos\phi\sin^2\theta)\\
&+ \rho\sin\phi(\rho\sin^2\phi\cos^2\theta + \rho^2\sin\phi^2\sin^2\theta)\\\\
&= \cos\phi(\rho^2\sin\phi\cos\phi)\\
&+ \rho\sin\phi(\rho\sin^2\phi)\\\\
&= \rho^2\sin\phi\cos^2\phi + \rho^2\sin\phi\sin^2\phi\\\\
&= \rho^2\sin\phi
\end{align*}
$$
Therefore, $dV = dx\,dy\,dz = \rho^2\sin\phi\,d\rho\,d\phi\,d\theta$
