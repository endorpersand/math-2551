# 14.5: Directional Derivatives and the Gradient

## Directional Derivatives
$\Large f'_{\vec{u}}(x_0, y_0)$ or $\Large D_{\vec{u}}f(P_0)$ gives the **directional derivative** of $f$ in the direction of $\vec{u}$ at the point $P_0 = (x_0, y_0)$.
- The rate of change of $f$ in the $\vec{u}$ direction.

If $\Large \vec{u} = u_1\mathbf{i} + u_2\mathbf{j}$, then
$$
\Large
D_\vec{u}f(P_0) = \lim_{s \to 0} \frac{f(x_0 + su_1, y_0 + su_2) - f(x_0, y_0)}{s}
$$
provided that the limit exists.

### Example
![[Pasted image 20220118153758.png]]

## Gradients
**Gradient** of a function $f(x, y)$ is vector
$$
\Large
\nabla f(x, y) = \frac{\partial{f}}{\partial{x}}\mathbf{i} + \frac{\partial{f}}{\partial{y}}\mathbf{j}
$$
You can imagine how to extend this into 3+ dimensions.

### Properties
$$
\Large
\begin{align*}
	\nabla(f(\vec{x}) + g(\vec{x})) &= \nabla f(\vec{x}) + \nabla g(\vec{x}) \\
	\nabla(\alpha f(\vec{x})) &= \alpha\nabla f(\vec{x}) \\
	\nabla(f(\vec{x})g(\vec{x})) &= f(\vec{x})\nabla g(\vec{x}) + \nabla f(\vec{x})g(\vec{x}) \\
\end{align*}
$$
### Directional Derivative
**Directional derivative** of $f$ in the direction of $\vec{u}$ at point $P_0 = (x_0, y_0)$ can be written as:
$$
\Large
f'_{\vec{u}}(P_0) = \nabla f(P_0) \cdot \hat{u} = \|\nabla f(P_0)\|\cos\theta
$$

**Properties**
1. At $P$, function $f$ increases most rapidly in the direction of its gradient vector.
2. Function $f$ decreases most rapidly in the direction of $-\nabla f$.
3. Any direction $\vec{u}$ orthogonal to gradient $\nabla f \neq 0$ is a direction of zero change in f.
### Examples
Find the gradient of $f(x, y) = 2e^x\sin(x^2+y)$
$$
\Large
\begin{align*}
\nabla f(x, y) &= (4xe^x\cos(x^2 + y)+2e^x\sin(x^2+y))\mathbf{i} \\
&\hspace{1em}+2e^xcos(x^2 + y)\mathbf{j}\\
\end{align*}
$$
![[Pasted image 20220118155110.png]]
## Tangent Lines to Level Curves
The tangent line to level curve $f(x, y) = c$ at point $(x_0, y_0)$ is
$$
\Large
\begin{align*}
f_x(x_0, y_0)(x-x_0) + f_y(x_0, y_0)(y-y_0) = 0\\
\left.\frac{\partial{f}}{\partial{x}}\right|_{(x_0, y_0)}(x-x_0) + \left.\frac{\partial{f}}{\partial{y}}\right|_{(x_0, y_0)}(y-y_0) = 0
\end{align*}
$$
(Can be derived from implicit differentiation rule)

## Derivative Along a Path
if $\vec{r}(t) = x(t)\mathbf{i} + y(t)\mathbf{j} + z(t)\mathbf{k}$ is a smooth path $C$ and $w = f(\vec{r}(t))$ is a scalar function evaluated along $C$, then the derivative along that path is
$$
\Large
\frac{d}{dt}f(\vec{r}(t)) = \nabla f(\vec{r}(t)) \cdot \vec{r}'(t)
$$

# 14.6: Tangent Planes & Differentials
## Tangent Planes & Normal Lines
**Tangent plane** to level surface $f(x, y, z) = c$ of a differentiable function $f$ at point $P_0(x_0, y_0, z_0)$ where the gradient is not zero is the plane through $P_0$ normal to $\nabla f(x_0, y_0, z_0)$.
$$
\Large
\begin{align*}
f_x(P_0)(x-x_0) + f_y(P_0)(y-y_0) + f_z(P_0)(z-z_0) = 0\\
\nabla f(P_0) \cdot \overrightarrow{P_0P} = 0
\end{align*}
$$
**Normal line** to level surface $f(x, y, z) = c$ is the line through $P_0$ parallel to $\nabla f(x_0, y_0, z_0)$.

$$
\Large
\begin{align*}
x &= x_0 + f_x(P_0)t\\
y &= y_0 + f_y(P_0)t\\
z &= z_0 + f_z(P_0)t
\end{align*}
$$
or
$$
\Large
\vec{r}(t) = P_0 + t \nabla f(P_0)
$$
![[Pasted image 20220118205042.png]]

## Differentials
### Linearization
The **linearization** of differentiable function $f(x, y)$ at $(x_0, y_0)$ is:
$$
\Large
\begin{align*}
L(x, y) &= f(x_0, y_0) + f_x(x_0, y_0)(x - x_0) + f_y(x_0, y_0)(y - y_0)\\
L(x, y) &= f(x_0, y_0) + \frac{\partial{f}}{\partial{x}}\Delta{x} + \frac{\partial{f}}{\partial{y}}\Delta{y}
\end{align*}
$$

The approximation $f(x, y) \approx L(x,y)$ is called the **standard linear approximation** of $f$ at the point.

The **total differential of $f$** is the resulting change from $(x_0, y_0)$ to $(x_0 + dx, y_0, dy)$
$$
\Large
df = f_x(x_0, y_0)dx + f_y(x_0, y_0)dy
$$

Error in standard linear approximation when using $L$ to approximate $f$:
$$
\Large
|E| \leq \frac{1}{2}M(|x - x_0| + |y - y_0|)^2
$$
$M$ represents the upper bound of the second partials on the rectangle centered at $P_0$.

Extension of above formulas to more dimensions is trivial.

### More Differentials
They also help in estimating change in a function in a particular direction.
To estimate the change in value of a differentiable function $f$ when moving a small distance, $ds$, from point $P_0$ in the direction of the unit vector $\hat{u}$,
$$
\Large
df = f'_\hat{u}(P_0)ds = (\nabla f(P_0) \cdot \hat{u})ds
$$

# 14.7: Extreme Values
### Local Extrema
Let $f(x, y)$ be defined on a region $R$ containing point $(a, b)$. Then:
1. $f(a, b)$ is a **local maximum** of $f$ if $f(a,b) \geq f(x, y)$ for all domain points $(x, y)$ in an open disk around $(a, b)$.
2. $f(a, b)$ is a **local minimum** of $f$ if $f(a,b) \leq f(x, y)$ for all domain points $(x, y)$ in an open disk around $(a, b)$.

**First Derivative Test**: If $f(x,y)$ has a local extremum at interior point $(a, b)$, then $\nabla f(a, b) = \vec{0}$ (all the partial derivatives are 0).
- **Critical Points**: remember single variable calc?

**Saddle point**: Critical point that isn't a local extremum (some points are greater, some are less)

**Second partials test** (analogous to the 2nd derivative test):
- Used to determine if a critical point is a saddle point or a local min or max

$$
\Large
\begin{align*}
A &= f_{xx}(x_0, y_0)\\
B &= f_{xy}(x_0, y_0)\\
C &= f_{yy}(x_0, y_0)\\
D &= \begin{vmatrix}
A & B\\
B & C
\end{vmatrix} = AC - B^2
\end{align*}
$$

1. If $D < 0$, $(x_0, y_0)$ is a saddle point.
2. If $D > 0$ and $A > 0$, local minimum.
3. If $D > 0$ and $A < 0$, local minimum.
4. If $D = 0$, test is inconclusive.

### Absolute Extrema
**Absolute maximum**: Greatest value $f(x, y)$ for all $(x, y) \in D$
**Absolute maximum**: Smallest value $f(x, y)$ for all $(x, y) \in D$

Process for finding absolute extrema:
1. Find critical points in $D$.
2. Find extreme points on boundary of D.
3. Evaluate $f$ at candidates.
4. Yeah.

