# 16.1: Line Integrals
If $f$ is defined on a curve $C$ given parametrically by $\vec{r}(t) = x(t)\mathbf{i} + y(t)\mathbf{j} + z(t)\mathbf{k}$, the line integral of $f$ over C is:
$$
\Large
\int_C f(x,y,z)\,ds = \lim_{n \to \infty} \sum\limits_{k=1}^n f(x_k, y_k, z_k)\Delta s_k
$$

(This is the form for a **line integral of a scalar field**)

To integrate a continuous function $f(x, y, z)$ over a curve $C$:
1. Find a smooth parametrization of $C$:
$$
\Large
\vec{r}(t) = x(t)\mathbf{i} + y(t)\mathbf{j} + z(t)\mathbf{k}
$$ (where $a \leq t \leq b$)
3. Evaluate the integral as:
$$
\Large
\int_C f(x,y,z)\,ds = \int_a^bf(x(t),y(t),z(t))|\vec{v}(t)|\,dt
$$
(recall $\frac{ds}{dt} = |\vec{v}|$)

## Mass and Moment Calculations
Suppose we need to find the mass & moment for coil springs and then rods lying along a smooth curve $C$ in space.

Recall [[Week 8#Physics Definitions|physics definitions]] from 15.6.
They apply here, too.
**Mass**
$$
\Large
m = \int_C \lambda\,ds
$$
(this is a pretty straightforward extension of 15.6 so I don't think there needs to be notes here)

# 16.2: Vector Fields & Line Integrals
Let $\vec{F}$ be a vector field with continuous components defined along smooth curve $C$ parametrized by $\vec{r}(t), a \leq t \leq b$.

The **line integral of $\vec{F}$ along $C$** is:
$$
\Large
\int_C \vec{F}\cdot\vec{T}\,ds = \int_C \left(F \cdot \frac{d\vec{r}}{ds}\right)ds = \int_C\vec{F}\cdot d\vec{r}
$$
(This is the form for a **line integral of a vector field**)


To evaluate, write $\vec{F}$ and $d\vec{r}$ in terms of t and apply dot product.

Line integrals may also be written as:
$$
\Large
\begin{align*}
&\int_C M\,dx + \int_C N\,dy + \int_C P\,dz\\
&= \int_C M(x,y,z)\,dx + \int_C N(x,y,z)\,dy + \int_C P(x,y,z)\,dz\\
\end{align*}
$$
(same idea, write everything in terms of $t$)

## Example
Evaluate $\int_C\vec{F}\cdot dr$, where $\vec{F} = \langle xy, x^2z, xyz\rangle$ along $y = x^2$ from $(0,0,0)$ to $(1,1,0)$ followed by the straight-line segment from $(1,1,0)$ to $(1,1,1)$.
$$
\Large
\begin{align*}
C_1: \vec{r}_1(t) &= \langle t, t^2, 0\rangle\\
\vec{r}'_1(t) &= \langle 1, 2t, 0\rangle\\\\
C_2: \vec{r}_2(t) &= \langle 1, 1, t\rangle\\
\vec{r}'_2(t) &= \langle0, 0, 1\rangle
\end{align*}
$$
$$
\begin{align*}
&\int_C \vec{F} \cdot d\vec{r} \\
&= \int_0^1 \langle (t)(t^2), 0, 0\rangle\cdot\langle1, 2t, 0\rangle\,dt + \int_0^1 \langle (1)(1), (1)^2(t), (1)(1)(t)\rangle\cdot\langle0, 0, 1\rangle\,dt\\
&= \int_0^1 \langle t^3, 0, 0\rangle\cdot\langle1, 2t, 0\rangle\,dt + \int_0^1 \langle 1, t, t\rangle\cdot\langle0, 0, 1\rangle\,dt
\end{align*}
$$

## Physics
 ### Work 
$$\Large W = \int_C \vec{F}\cdot d\vec{r}$$
($\vec{F}$ is force)

 ### Flow 
$$\Large \text{Flow} = \int_C \vec{F}\cdot \vec{T}\,ds$$
($\vec{F}$ is velocity)
This integral is called a **flow integral**. If the curve starts and ends at the same point, the flow is called the *circulation* around the curve.

 ### Flux
$$
\Large
\Phi = \int_C \vec{F}\cdot\vec{N}\,ds
$$
($\vec{F}$ is velocity, $C$ is a smooth simple closed curve (starts & ends at same place and does not cross itself))

**Calculating flux across a smooth closed plane curve**
Let $\vec{F} = M\mathbf{i} + N\mathbf{j}$ and $\vec{r} = x(t)\mathbf{i} + y(t)\mathbf{j}$,
then:
![[Pasted image 20220123124512.png]]

(Integral is evaluated at any parametrization $\vec{r}$ that traces $C$ counterclockwise exactly once)
$$
\Large
\left\|\vec{F} \times \frac{d\vec{r}}{ds}\right\| = \begin{vmatrix}
M & N \\
\frac{dx}{ds} & \frac{dy}{ds}
\end{vmatrix} = M \frac{dy}{ds} - N \frac{dx}{ds}
$$
(Computing line integral with respect to $ds$ gives you the above)

# 16.3: Path Independence, Conservative Fields, Potential Functions
## Definitions
Let $\vec{F}$ be a vector field defined on open region $D$ in space.
Suppose that for any two points $A$ and $B$ in $D$, $\int_C \vec{F}\cdot d\vec{r}$ along path $C$ from $A$ to $B$ is the same over all paths from $A$ to $B$.
The integral is **path independent** and the field is **conservative on $D$**.

If $\vec{F}$ is a vector field on $D$ and $F = \nabla f$ for some scalar function $f$ on $D$, $f$ is called a **potential function for $F$**.

### Example
Find a potential function $f$ for $\vec{F} = (y \sin z)\mathbf{i} + (x \sin z)\mathbf{j} + (xy\cos z) \mathbf{k}$.

Let $\vec{F} = f_x\mathbf{i} + f_y\mathbf{j} + f_z\mathbf{k}$.
$$
\Large
\begin{align*}
\frac{\partial{f}}{\partial{x}} &= y \sin z\\
f = \int y \sin z\,dx &= xy \sin z + \overbrace{g(y, z)}^{\mathclap{\text {remember } +C \text{?}}}\\
\frac{\partial{f}}{\partial{y}} &= x \sin z + \frac{\partial{g}}{\partial{y}}\\
\frac{\partial{f}}{\partial{z}} &= xy \cos z + \frac{\partial{g}}{\partial{z}}\\
\end{align*}
$$

So,
$$
\Large
\begin{align*}
x \sin z + \frac{\partial{g}}{\partial{y}} = x \sin z &\implies \frac{\partial{g}}{\partial{y}} = 0\\
xy \cos z + \frac{\partial{g}}{\partial{z}} = xy \cos z &\implies \frac{\partial{g}}{\partial{z}} = 0

\end{align*}
$$

Therefore,
$$
\Large
f(x,y,z) = xy \sin z + C
$$
## Conservative Fields & Gradient Fields
### Theorem
Let $\vec{F} = M\mathbf{i} + N\mathbf{j} + P\mathbf{k}$ (and $M, N, P$ are continuous throughout open connected region $D$).
$F$ is conservative iff $\vec{F}$ is a gradient field $\nabla f$ for a differentiable function $f$.

### Component Test for Conservative Fields
Let $\vec{F} = X(x, y, z)\mathbf{i} + Y(x, y, z)\mathbf{j} + Z(x, y, z)\mathbf{k}$ on open simply connected domain ($X, Y, Z$ have continuous first partial derivatives).
then $\vec{F}$ is conservative iff:
$$
\Large
\begin{align*}
\frac{\partial{X}}{\partial y} &= \frac{\partial{Y}}{\partial x}\\
\frac{\partial{X}}{\partial z} &= \frac{\partial{Z}}{\partial x}\\
\frac{\partial{Y}}{\partial z} &= \frac{\partial{Z}}{\partial y}\\
\end{align*}
$$
If $\vec{F}$ is a gradient field for $f$, then $F = \nabla f = f_x\mathbf{i} + f_y\mathbf{j} + f_z\mathbf{k}$.
Then, second mixed partials need to be equivalent ($f_{xy} = f_{yx}, f_{xz} = f_{zx}, f_{yz} = f_{zy}$) for this to be true.

## Fundamental Theorem of Line Integrals
Let $C$ be a smooth curve joining points $A$ and $B$, parametrized by $\vec{r}(t)$.
Let $f$ be a differentiable function with continuous gradient vector $\vec{F} = \nabla f$ on domain $D$ containing $C$.
$$
\Large
\int_C \vec{F}\cdot d\vec{r} = f(B) - f(A)
$$
### Loop Property of Conservative Fields
Equivalent statements
(pretend that is the ccw integral)
1. $\oint_C F \cdot d\vec{r} = 0$ around every loop (every closed curve $C$) in $D$.
2. The field $F$ is conservative on $D$.

### Exactness
**Differential form**: Expression of the form $M(x,y,z)\,dx + N(x,y,z)\,dy + P(x,y,z)\,dz$.
A differential form is **exact** on domain $D$ if:
$$
\Large
M\,dx + N\,dy + P\,dz = \frac{\partial{f}}{\partial{x}}\,dx + \frac{\partial{f}}{\partial{y}}\,dy + \frac{\partial{f}}{\partial{z}}\,dz = df
$$
for some scalar function $f$ throughout $D$.
In other words, a differential form is exact iff $\langle M, N, P \rangle = \nabla f$ (iff $\vec{F} = \langle M, N, P\rangle$ is conservative).

