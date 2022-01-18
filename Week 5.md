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
f'_{\vec{u}}(P_0) = \nabla f(P_0) \cdot \hat{u} = \|f(P_0)\|\cos\theta
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
