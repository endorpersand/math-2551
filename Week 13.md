# 16.7: Stokes' Theorem
## $\large \nabla$, div, and curl
**The del operator**:
$$
\Large
\nabla = \mathbf{i}\frac{\partial}{\partial{x}} + \mathbf{j}\frac{\partial}{\partial{y}} + \mathbf{k}\frac{\partial}{\partial{z}}
$$

Two formulas use the $\nabla$ operator:
$$
\Large
\begin{align*}
\text{del }\vec{F} &= \nabla \cdot \vec{F}\\
\text{curl }\vec{F} &= \nabla \times \vec{F}
\end{align*}
$$
### Curl Identity
$$
\Large
\begin{align*}
\text{curl grad }f &= 0\\
\nabla \times \nabla f &= 0
\end{align*}
$$
**Why?**
$$
\Large
\nabla\times\nabla f = \begin{vmatrix}
\mathbf{i} & \mathbf{j} & \mathbf{k} \\
\frac{\partial}{\partial{x}}& \frac{\partial}{\partial{y}} & \frac{\partial}{\partial{z}} \\
f_x & f_y & f_z
\end{vmatrix}\\
$$
Mixed partials have to be equal if continuous, so everything here evals to 0.

### Example
Find the div and curl for $\vec{F} = (x^2 - yz)\mathbf{i} + ye^x \mathbf{j} + (xy + z) \mathbf{k}$.

$$
\Large
\begin{align*}
\text{div }\vec{F} = \nabla\cdot\vec{F} &= \frac{\partial}{\partial{x}}(x^2-yz) + \frac{\partial}{\partial{y}}(ye^x) + \frac{\partial}{\partial{x}}(xy+z)\\
&= 2x + e^x + 1
\end{align*}
$$

$$
\Large
\begin{align*}
\text{curl }\vec{F} = \nabla\times\vec{F} &= \begin{vmatrix}
\mathbf{i} & \mathbf{j} & \mathbf{k} \\
\frac{\partial}{\partial{x}}& \frac{\partial}{\partial{y}} & \frac{\partial}{\partial{z}} \\
x^2 - yz & ye^x & xy + z
\end{vmatrix}\\
&= \mathbf{i}\left(\frac{\partial}{\partial{y}}\left(xy+z\right) - \frac{\partial}{\partial{z}}(ye^x)\right)\\
&- \mathbf{j}\left(\frac{\partial}{\partial{x}}\left(xy+z\right) - \frac{\partial}{\partial{z}}(x^2-yz)\right)\\
&+\mathbf{k}\left(\frac{\partial}{\partial{x}}\left(ye^x\right) - \frac{\partial}{\partial{y}}(x^2-yz)\right)\\
&= x\mathbf{i} - 2y\mathbf{j} + (ye^x + z)\mathbf{k}
\end{align*}
$$


## Stokes' Theorem
Let $S$ be a piecewise smooth oriented surface with piecewise smooth boundary curve $C$.
Let $\vec{F} = M \mathbf{i} + N \mathbf{j} + P \mathbf{k}$ be a vector field with continuous 1st partial derivatives on open region containing $S$.

Then the circulation of $\vec{F}$ around C in the CCW dir:
$$
\Large
\oint_C \vec{F}\cdot d\vec{r} = \iint_S (\nabla \times \vec{F}) \cdot \hat{n}\,d\sigma = \iint_S (\text{curl }\vec{F}) \cdot \hat{n}\,d\sigma
$$
($\hat{n}$ is the unit normal vector with respect to the surface)

**Closed Loop Property**:
If $\text{curl F} = 0$ at every point of a simply connected open region $D$ in space, then on any piecewise-smooth closed path $C$ in $D$:
$$
\Large
\oint_C F\cdot d\vec{r} = 0
$$
(pretty straightforward extension of [[Week 10#Loop Property of Conservative Fields|the loop property of conservative fields]])

# 16.8: The Divergence Theorem and a Unified Theory
## Divergence Theorem
Let $S$ be a piecewise smooth oriented surface.
Let $F$ be a vector field whose components have continuous 1st partial derivatives.

Then, the flux of $\vec{F}$ across $S$ in the direction of the surface's outward unit normal field $\hat{n}$:
$$
\Large
\iint_S \vec{F}\cdot\vec{n}\,d\sigma = \iiint_D \nabla\cdot\vec{F}\,dV
$$
**Corollary**:
The outward flux across a piecewise smooth oriented closed surface is 0 for any vector field $F$ with 0 divergence at every point of the region.

**Divergence & Curl**
$$
\Large
\text{div }(\text{curl }\vec{F}) = \nabla\cdot(\nabla\times\vec{F}) = 0
$$
## Unifying Fundamental Theorem of Vector Integral Calculus
The integral of a differential operator ($\nabla$) acting on a field over a region = the sum of the field components (appropriate to the operator) over the boundary of the region

Example with Stokes' theorem:
$$
\Large
\overbrace{\oint_C \vec{F}\cdot d\vec{r}}^{\Sigma \text{ of field components over boundary } C} = \overbrace{\iint_S (\nabla \times \vec{F}) \cdot \hat{n}\,d\sigma}^{\int \text{ of } \nabla \text{ acting on } \vec{F} \text{ over } S}
$$
### Generalizations of Green's Theorem
**Tangential Form**
$$
\Large
\begin{align*}
\oint_C \vec{F}\cdot \vec{T}\,ds &= \iint_R (\nabla \times \vec{F}) \cdot \mathbf{k}\,dA \text{ (tangential form)}\\
\oint_C \vec{F}\cdot \vec{T}\,ds &= \iint_R (\nabla \times \vec{F}) \cdot \hat{n}\,dA \text{ (Stokes' theorem)}

\end{align*}
$$
**Normal Form**
$$
\Large
\begin{align*}
\oint_C \vec{F}\cdot \hat{n}\,ds &= \iint_R \nabla \cdot \vec{F}\,dA \text{ (normal form)}\\
\iint_S \vec{F}\cdot \hat{n}\,d\sigma &= \iiint_D \nabla \cdot \vec{F}\,dV \text{ (Divergence theorem)}

\end{align*}
$$
