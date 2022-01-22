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

Triple Integrals:
$$
\Large
\iiint_T \,dV = \iiint_T \rho^2\sin\phi\,d\rho\,d\phi\,d\theta
$$

# 15.8: Integration by Substitution
## Double Integrals

**Jacobian determinate** or **Jacobian** of the coordinate transformation $x = g(u, v), y = h(u, v)$:
$$
\Large
J(u, v) = \frac{\partial(x, y)}{\partial(u, v)} = \begin{vmatrix}
\frac{\partial{x}}{\partial{u}}&\frac{\partial{x}}{\partial{v}}\\
\frac{\partial{y}}{\partial{u}}&\frac{\partial{y}}{\partial{v}}\\
\end{vmatrix} = \frac{\partial{x}}{\partial{u}}\frac{\partial{y}}{\partial{v}} - \frac{\partial{y}}{\partial{u}}\frac{\partial{x}}{\partial{v}}
$$
**Substitution for Double Integrals**:
Suppose $f(x, y)$ is continuous over region $R$. Let $G$ be preimage of $R$ under transform $x = g(u, v), y = h(u, v)$ (assumed to be one-to-one on interior of $G$). If functions $g$ and $h$ have continuous 1st partial derivatives within interior of $G$:
$$
\Large
\iint_Rf(x,y)\,dx\,dy = \iint_G f(g(u, v), h(u, v))\overbrace{\left|\frac{\partial(x, y)}{\partial(u, v)}\right|}^{\text{Jacobian}}\,du\,dv
$$
## Triple Integrals
Given $x=g(u, v, w), y=h(u,v, w), z=k(u,v, w)$,
$$
\Large
J(u, v, w) = \frac{\partial(x, y, z)}{\partial(u, v, w)} = \begin{vmatrix}
\frac{\partial{x}}{\partial{u}}&\frac{\partial{x}}{\partial{v}}&\frac{\partial{x}}{\partial{w}}\\
\frac{\partial{y}}{\partial{u}}&\frac{\partial{y}}{\partial{v}}&\frac{\partial{y}}{\partial{w}}\\
\frac{\partial{z}}{\partial{u}}&\frac{\partial{z}}{\partial{v}}&\frac{\partial{z}}{\partial{w}}\\
\end{vmatrix}
$$

$$
\Large
\begin{align*}
&\iiint_R f(x,y,z)\,dx\,dy\,dz \\
&= \iiint_G f(g(u,v,w),h(u,v,w), k(u,v,w))\left|\frac{\partial(x, y, z)}{\partial(u, v, w)}\right|\,du\,dv\,dw

\end{align*}
$$