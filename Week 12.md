# 16.4: Green's Theorem
**Circulation density** of a vector field $\vec{F} = M\mathbf{i} + N\mathbf{j}$ at point $(x, y)$ is the scalar expression:
$$
\Large
\text{curl }\vec{F} \cdot \mathbf{k} = \frac{\partial{N}}{\partial{x}}- \frac{\partial{M}}{\partial{y}}
$$

**Divergence (flux density)** of vector field $\vec{F} = M\mathbf{i} + N\mathbf{j}$ at $(x, y)$ is:
$$
\Large
\text{div } \vec{F} = \frac{\partial{M}}{\partial{x}} + \frac{\partial{N}}{\partial{y}}
$$

## Circulation-Curl or Tangential Form
Let $C$ be piecewise smooth, simple closed curve enclosing region $R$ in the plane.
Let $\vec{F} = M\mathbf{i} + N\mathbf{j}$ be a vector field with $M$ and $N$ have continuous 1st partial derivatives in open region containing $R$.

Then:
The **counterclockwise circulation** of $\vec{F}$ around $C$ equals the double integral of $\text{curl } \vec{F} \cdot \mathbf{k}$ over $R$.
$$
\Large
\oint_C \vec{F}\cdot \vec{T}\,ds = \oint_C M\,dx + N\,dy = \iint_R \left(\frac{\partial{N}}{\partial{x}} - \frac{\partial{M}}{\partial{y}}\right)\,dx\,dy
$$
## Flux-Divergence or Normal Form
Let $C$ be piecewise smooth, simple closed curve enclosing region $R$ in the plane.
Let $\vec{F} = M\mathbf{i} + N\mathbf{j}$ be a vector field with $M$ and $N$ have continuous 1st partial derivatives in open region containing $R$.

Then:
The **outward flux** of $\vec{F}$ around $C$ equals the double integral of $\text{div } \vec{F}$ over $R$.
$$
\Large
\oint_C \vec{F}\cdot \vec{n}\,ds = \oint_C M\,dy - N\,dx = \iint_R \left(\frac{\partial{M}}{\partial{x}} + \frac{\partial{N}}{\partial{y}}\right)\,dx\,dy
$$
## Area
Green's Theorem can be used to write area in terms of a line integral.
$$
\Large
\begin{align*}
A_R &= \iint_R\,dy\,dx \\
&= \iint_R\left(\frac{1}{2} + \frac{1}{2}\right)\,dy\,dx\\
&= \frac{1}{2}\oint x\,dy - y\,dx
\end{align*}
$$

# 16.5: Surfaces and Area
## Parameterized Surfaces
A **parametrized surface** is given by: $\vec{r}(u, v) = f(u, v)\mathbf{i} + g(u,v)\mathbf{j} + h(u,v)\mathbf{k}$.
The domain is the set of points in the $uv$-plane that can be substituted into $\vec{r}$.

**Sphere**: $x^2 + y^2 + z^2 = a^2$
$\vec{r}(\phi, \theta) = a\sin\phi\cos\theta\mathbf{i} + a\sin\phi\sin\theta\mathbf{j} + a\cos\phi\mathbf{k}$ (pretty straightforward mapping of spherical coordinates)
$(0 \leq \phi \leq \pi, 0 \leq \theta \leq 2\pi)$

**Cylinder**: $x^2 + y^2 = a^2, 0 \leq z \leq b$
$\vec{r}(\theta, z) = a\cos\theta\mathbf{i} + a\sin\theta\mathbf{j} + z\mathbf{k}$ (pretty straightforward mapping of cylindrical coordinates)
$(0 \leq \theta \leq 2\pi, 0 \leq z \leq b)$

**Cone**: $z = \sqrt{x^2 + y^2}, 0 \leq z \leq b$
$\vec{r}(r, \theta) = r\cos\theta\mathbf{i} + r\sin\theta\mathbf{j} + r\mathbf{k}$
$(0 \leq r \leq b, 0 \leq \theta \leq 2\pi)$

### Example
Find the parametrization for $z = 4 - x^2 - y^2, z \geq 0$.
$$
\Large
\begin{align*}
z &= 4 - x^2 - y^2\\
&= 4 - r^2\\
\therefore r &\leq 2
\end{align*}
$$
The parametrization:
$$
\Large
\vec{r}(r, \theta) = r\cos\theta\mathbf{i} + r\sin\theta\mathbf{j} + (4 - r^2)\mathbf{k}
$$
$(0 \leq r \leq 2, 0 \leq \theta < 2\pi)$

## Surface Area
A parametrized surface $\vec{r}(u, v) = f(u, v)\mathbf{i} + g(u, v)\mathbf{j} + h(u,v)\mathbf{k}$ is **smooth** if $\vec{r}_u$ and $\vec{r}_v$ are continuous and $\vec{r}_u \times \vec{r}_v \neq 0$ on the interior of the parameter domain.

Given smooth surface $\vec{r}(u, v) = f(u, v)\mathbf{i} + g(u, v)\mathbf{j} + h(u,v)\mathbf{k}, a \leq u \leq b, c \leq v \leq d$:
$$
\Large
A = \iint_R |\vec{r}_u \times \vec{r}_v|\,dA = \int_c^d\int_a^b|\vec{r}_u \times \vec{r}_v|\,du\,dv
$$
**Surface area of an implicit surface**:
Area of surface $F(x, y, z) = c$ over closed & bounded region $R$:
$$
\Large
SA = \iint_R \frac{\|\nabla F\|}{|\nabla F \cdot \hat{p}|}\,dA
$$
(where $\hat{p} = \mathbf{i}, \mathbf{j}, \text{ or } \mathbf{k}$ is normal to $R$ and $\nabla F \cdot \hat{p} \neq 0$)

**Surface area for $z = f(x, y)$**:
$$
\Large
A = \iint_R \sqrt{f_x^2 + f_y^2 + 1}\,dx\,dy
$$
(This can be derived by creating parametrization $\vec{r}(x, y) = x\mathbf{i} + y\mathbf{j} + f(x,y)\mathbf{k}$ and applying parametrized surface integral formula)

# 16.6: Surface Integrals
## Definition
**Surface area differential**:
$$
\Large
d\sigma = |\vec{r}_u \times \vec{r}_v|\,du\,dv
$$
**Surface integral of $G$ over surface $S$**
$$
\Large
\iint_S G(x,y,z)\,d\sigma = \lim_{n\to\infty}\sum\limits_{k=1}^nG(x_k,y_k,z_k)\Delta\sigma_k
$$
## Surface integrals of scalar functions
You can substitute $d\sigma$ for the surface area formulas above ([[#Surface Area]]) depending on which condition you meet.


**Parametrized surface**
Given smooth surface $\vec{r}(u, v) = f(u, v)\mathbf{i} + g(u, v)\mathbf{j} + h(u,v)\mathbf{k}, (u, v) \in R$
$$
\Large
\iint_S G(x, y, z)d\sigma = \iint_R G(f(u, v), g(u, v), h(u, v))|\vec{r}_u \times \vec{r}_v|\,du\,dv
$$

**Implicit surface**
$$
\Large
\iint_SG(x,y,z)d\sigma = \iint_RG(x,y,z)\frac{\|\nabla F\|}{|\nabla F \cdot \hat{p}|}\,dA
$$
($S$ lies above its closed & bounded shadow region $R$ in the coordinate plane beneath it)
(where $\hat{p} = \mathbf{i}, \mathbf{j}, \text{ or } \mathbf{k}$ is normal to $R$ and $\nabla F \cdot \hat{p} \neq 0$)

**For $z = f(x, y)$**
$$
\Large
\iint_SG(x,y,z)d\sigma = \iint_RG(x,y,f(x,y))\sqrt{f_x^2 + f_y^2 + 1}\,dx\,dy
$$
($R$ is the region on the $xy$-plane)

## Surface integrals of vector fields
Let $\vec{F}$ be a vector field in 3D space with continuous components defined over a smooth surface $S$, with normal unit vectors $\hat{n}$ orienting $S$.
The **surface integral of $\vec{F}$ over $S$**:
$$
\Large
\iint_S \vec{F}\cdot\hat{n}\,d\sigma
$$
This integral is also called the **flux** of the vector field $\vec{F}$ across $S$.

If the surface being integrated over can be written as $g(x, y, z) = c$,
$$
\Large
\hat{n} = \pm \frac{\nabla{g}}{\|\nabla{g}\|}
$$

If the surface being integrated over can be parametrized as $\vec{r}(u, v)$, the surface integral can be calculated as:
$$
\Large
\iint_S \vec{F} \cdot (\vec{r}_u \times \vec{r}_v)\,du\,dv
$$
## Mass & Moment
Same as [[Week 8#Physics Definitions]], but with:
$$
\Large
dm = \delta d\sigma
$$
