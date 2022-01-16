# 14.1: Functions of Several Variables

## Definition
Suppose $D$ is a set of n-tuples of real numbers $(x_1, x_2, x_3, \dots, x_n)$.

A **real-valued function** $f$ on $D$ returns a real number $\Large (f : D \to \mathbb{R})$
- domain = $D$
- range = set of values returned

### Examples

Find domain of each:
1. $f(x, y) = \sqrt{xy}$

	Answer: $\{(x, y) | xy \geq 0\}$

2. $f(x, y) = \frac{1}{\sqrt{x-y}}$

	$x - y > 0$, so:
	Answer: $\{(x, y) | x > y\}$

3. $f(x, y, z) = \frac{\sqrt{z}}{x^2 - y^2}$
	
	$x^2 - y^2 \neq 0$
	$z \geq 0$
	Answer: $\{(x, y, z) | x^2 \neq y^2, z \geq 0\}$

## Boundary Points and Interior Points
**Interior point** of a set (or region) $R$: A point $(x_0, y_0)$ in the center of a disk of positive radius that lies entirely in $R$.

![[Pasted image 20220116091440.png|200]]

**Boundary point** of a set (or region $R$): A point $(x_0, y_0)$ where every disk of positive radius contains points that lie outside of $R$ and points that lie in $R$.

$(x_0, y_0)$ does not need to be in $R$.

![[Pasted image 20220116091609.png|200]]

(For the above definitions, in 3D, replace "disk" with ball)

A set is **closed** if it contains <u>all</u> of its boundary points.
A set is **open** if it contains <u>none</u> of its boundary points.
Otherwise, it is neither open nor closed.

**Bounded regions**: A region that lies inside a disk of finite radius
- **Unbounded**: a region that doesn't

![[Pasted image 20220116091913.png|500]]

## Level Curves and Surfaces
If $c$ is a value in range of 2-var $f$, we can sketch the **level curve** $f(x, y) = c$.
If $c$ is a value in range of 3-var $f$, we can sketch the **level surface** $f(x, y, z) = c$.

### Examples
1. Graph level curves of $f(x, y) = \ln(x - y^2)$ for $c = -1, 0, 1$.
$$
\Large
\color{#44F}
\begin{align*}
\ln(x-y^2) &= -1\\
x - y^2 &= e^{-1}\\
x &= y^2 + e^{-1}
\end{align*}
$$
$$
\Large
\color{#F33}
\begin{align*}
\ln(x-y^2) &= 0\\
x - y^2 &= e^0\\
x &= y^2 + 1
\end{align*}
$$
$$
\Large
\begin{align*}
\ln(x-y^2) &= 1\\
x - y^2 &= e^{1}\\
x &= y^2 + e
\end{align*}
$$
![[Pasted image 20220116092724.png|500]]

2. Describe the level curves for $\Large f(x, y) = e^{x^2 + 2y^2}$.

$$
\Large
\begin{align*}
e^{x^2 + 2y^2} &= c\\
x^2 + 2y^2 &= \underbrace{\ln{c}}_{\mathclap{\text{constant}}}\text{ }(c > 0)
\end{align*}

$$
*The level curves are ellipses.*

3. ![[Pasted image 20220116093238.png]]
- The contours are level curves.

Recognize one of the curves as $x = -y^2$, so $x + y^2 = c$, and $f(x, y) = x + y^2$.

# 14.2: Limits and Continuity
## Limits for Functions of Several Variables
Let $f(x_1, x_2, \dots, x_n)$ be a function defined (at least) on some deleted neighborhood of $\vec{x}_0$.
$$
\Large
\lim_{\vec{x} \to \vec{x}_0}{f(\vec{x}) = L}
$$
if for each $\epsilon > 0$, there exists $\delta > 0$ such that
$$\Large
0 < \Vert \vec{x} - \vec{x}_0 \Vert < \delta \implies |f(\vec{x}) - L| < \epsilon
$$
(Essentially, as $\vec{x}$ approaches $\vec{x}_0$ from anywhere, $f(\vec{x})$ approaches $L$.)

**Two paths test**: If the paths $\vec{x} \to \vec{x}_0$ approach different values for $f(\vec{x})$, the limit does not exist.

### Example: Proving a limit using the definition
This looks like a doozy.

Find $\displaystyle \Large \lim_{(x, y) \to (0,0)}{f(x, y)}$ for $\displaystyle \Large f(x, y) = \frac{2xy^2}{x^2 + y^2}$.

If the limit is true, there must be some relationship between $\epsilon$ and $\delta$.

On the $\Large \epsilon$ side:
$$
\Large
\begin{align*}
|f(x, y) - \overbrace{L}^{\mathclap{\text{After testing, we find some paths to converge to 0}}}| &< \epsilon\\
\left|\frac{2xy^2}{x^2 + y^2} - 0\right| &< \epsilon\\
\frac{2|x|y^2}{x^2 + y^2} &< \epsilon\\
\end{align*}
$$

On the $\Large \delta$ side:
$$
\Large
\begin{align*}
0 &< \sqrt{(x - x_0)^2 + (y-y_0)^2} &< \delta\\
0 &< \sqrt{x^2 + y^2} &< \delta\\
0 &< 2\sqrt{x^2 + y^2} &< 2\delta
\end{align*}
$$

Since $\Large y^2 \leq x^2 + y^2$, 
	$\Large \frac{y^2}{x^2 + y^2} \leq 1$ 
	and $\Large \frac{2|x|y^2}{x^2 + y^2} \leq 2|x|$

So:
$$
\Large
\Large \frac{2|x|y^2}{x^2 + y^2} \leq 2|x| = 2\sqrt{x^2} \leq 2\sqrt{x^2 + y^2} < \epsilon
$$

Thus, you can let $\Large \delta = \frac{\epsilon}{2}$ and so the limit exists.

## Continuity for Functions of Several Variables
A function $f(x, y)$ is *continuous* at point $(x_0, y_0)$ if:
1. $f$ is defined at $(x_0, y_0)$
2. Limit at that point exists
3. Limit is equal to $f(x_0, y_0)$

Function is continuous if it is continuous at every point in its domain.

![[Pasted image 20220116095724.png]]

# 14.3, 14.4: Partial Derivatives

## Definition
If the limit exists, the **partial derivative** of $f(x, y)$ with respect to $x$ at $(x_0, y_0)$ is:
$$
\Large
\left.\frac{\partial{f}}{\partial{x}}\right|_{(x_0, y_0)} = \lim_{\Delta x \to 0} \frac{f(x_0 + \Delta x, y_0) - f(x, y)}{\Delta x}
$$
(Differentiate $f$ with respect to $x$, while holding other variables constant)
(This extends trivially to more dimensions)

### Differentiability
Function $z = f(x, y)$ is **differentiable** at $(x_0, y_0)$ if $f_x, f_y$ (the partial derivatives) and $\Delta z = f(x_0 + \Delta x, y_0 + \Delta y) - f(x_0, y_0)$ satisfies:
$$
\Large
\Delta z = (f_x + \epsilon_1)\Delta x + (f_y + \epsilon_2)\Delta y
$$
(where each $\epsilon_1, \epsilon_2 \to 0$ as both $\Delta x, \Delta y \to 0$)

$f$ is **differentiable** if it is differentiable at every point in its domain.
$f$'s graph then is a **smooth surface**

### Example
Find all first partial derivatives of $f(x, y) = 3x^2 - 2y + xy$.
$$
\Large
\begin{align*}
f_x = \frac{\partial{f}}{\partial{x}} &= 6x + y\\
f_y = \frac{\partial{f}}{\partial{y}} &= -2 + x
\end{align*}
$$

## Second Order Partial Derivatives
$$
\Large
\begin{align*}
(f_x)_x = f_{xx} &= \frac{\partial}{\partial{x}}\left(\frac{\partial{f}}{\partial{x}}\right) = \frac{\partial^{2}{f}}{\partial{x^2}}\\
(f_x)_y = f_{xy} &= \frac{\partial}{\partial{y}}\left(\frac{\partial{f}}{\partial{x}}\right) = \frac{\partial^{2}{f}}{\partial{y}\partial{x}}\\
(f_y)_x = f_{yx} &= \frac{\partial}{\partial{x}}\left(\frac{\partial{f}}{\partial{y}}\right) = \frac{\partial^{2}{f}}{\partial{x}\partial{y}}\\
(f_y)_y = f_{yy} &= \frac{\partial}{\partial{y}}\left(\frac{\partial{f}}{\partial{y}}\right) = \frac{\partial^{2}{f}}{\partial{y^2}}\\
\end{align*}
$$
### Mixed Derivatives Theorem
If $f(x,y)$ and all of $\Large f_x, f_y, f_{xy}, f_{yx}$ are defined throughout an open region containing a point $(x_0, y_0)$ and are all continuous at $(x_0, y_0)$, then 
$$
\Large f_{xy}(x_0, y_0) = f_{yx}(x_0, y_0)
$$

### Example
Find all first & second partial derivatives of $f(x, y) = 2x^2\cos{y} + 3y^2\sin{x}$.

$$
\Large
\begin{align*}
f_x &= 4x\cos{y} + 3y^2\cos{x}\\
f_y &= -2x^2\sin{y} + 6y\sin{x}\\
\end{align*}
$$

$$
\Large
\begin{align*}
f_{xx} &= 4\cos{y} - 3y^2\sin{x}\\
f_{xy} &= -4x\sin{y} + 6y\cos{x}\\
f_{yx} &= -4x\sin{y} + 6y\cos{x}\\
f_{yy} &= -2x^2\cos{y} + 6\sin{x}
\end{align*}
$$

## Implicit Differentiation
Suppose we have a function in terms of three variables $x, y, z$ and we cannot solve the equation for $z$, but we want to find $\frac{\partial{z}}{\partial{x}}$ or $\frac{\partial{z}}{\partial{y}}$.

Do implicit differentiation as expected, but hold the necessary variables constant.

### Example
Find $\Large \frac{\partial{z}}{\partial{x}}$ and $\Large \frac{\partial{z}}{\partial{y}}$ for $\Large xy - z^2y - 2zx = 0$.

$$
\Large
\begin{align*}
y - 2zy\frac{\partial{z}}{\partial{x}} - 2z - 2x\frac{\partial{z}}{\partial{x}} &= 0 \\
\frac{\partial{z}}{\partial{x}}(-2zy - 2x) + y - 2z &= 0 \\
\frac{\partial{z}}{\partial{x}}(-2zy - 2x) &= 2z - y \\
\frac{\partial{z}}{\partial{x}} &= \frac{y - 2z}{2zy + 2x} \\
\end{align*}
$$

$$
\Large
\begin{align*}
x - z^2 - 2zy\frac{\partial{z}}{\partial{y}} - 2x\frac{\partial{z}}{\partial{y}} &= 0 \\
x - z^2 - (2zy+2x)\frac{\partial{z}}{\partial{y}} &= 0 \\
(2zy+2x)\frac{\partial{z}}{\partial{y}} &= x - z^2 \\
\frac{\partial{z}}{\partial{y}} &= \frac{x - z^2}{2zy+2x} \\
\end{align*}
$$

## Chain Rule
### Simple  
If $w = f(x, y)$ is differentiable and $x(t), y(t)$ are differentiable with respect to $t$, then $w = f(x(t), y(t))$ is differentiable with respect to $t$.
$$
\Large
\frac{dw}{dt} = \frac{\partial{w}}{\partial{x}}\frac{dx}{dt} + \frac{\partial{w}}{\partial{y}}\frac{dy}{dt}
$$
(This is trivially extendible to more dimensions)

#### Example
Find $\Large \frac{du}{dt}: u = x^2 - 3xy = 2y^2,\text{ } x(t) = \cos{t},\text{ } y(t) = \sin{t}$

$$
\Large
\begin{align*}
\frac{dx}{dt} &= -\sin{t}\\
\frac{dy}{dt} &= \cos{t}\\
\frac{\partial{u}}{\partial{x}} &= 2x - 3y\\
\frac{\partial{u}}{\partial{y}} &= -3x + 4y\\
\end{align*}
$$
So:
$$
\Large
\begin{align*}
\frac{du}{dt} &= \frac{\partial{u}}{\partial{x}}\frac{dx}{dt} + \frac{\partial{u}}{\partial{y}}\frac{dy}{dt}\\\\
&= (2\cos(t) - 3\sin(t))(-\sin(t))\\
&\hspace{1.5em} + (-3\cos(t) + 4\sin(t))(\cos(t))\\\\
&= -2\sin(t)\cos(t) + 3\sin^2(t) - 3\cos^2(t) + 4\sin(t)\cos(t)\\
&= 2\sin(t)\cos(t) + 3\sin^2(t) - 3\cos^2(t)\\
&= \sin(2t) - 3\cos(2t)
\end{align*}
$$

### UH. PANIC.
What if $u = u(x, y)$, $x = x(s, t)$, $y = y(s, t)$?

You can find partial derivatives $\Large \frac{\partial{u}}{\partial{s}}$ and $\Large \frac{\partial{u}}{\partial{t}}$, replacing $\Large \frac{dx}{dt}$ in the simpler chain rule with the respective partial derivative.

#### Example
Given $z = 4e^x\ln{y}, x = \ln(uv), y = u\sin(v)$, express $\frac{\partial{z}}{\partial{u}}$ as a function of $u$ and $v$.

$$
\Large
\begin{align*}
\frac{\partial{x}}{\partial{u}} &= \frac{1}{u}\\
\frac{\partial{y}}{\partial{u}} &= \sin(v)\\\\
\frac{\partial{z}}{\partial{x}} &= 4e^x\ln{y} \\
&= 4uv\ln(u\sin(v))\\\\
\frac{\partial{z}}{\partial{y}} &= \frac{4e^x}{y} \\
&= \frac{4v}{\sin(v)}\\
\end{align*}
$$
So:
$$
\Large
\begin{align*}
\frac{\partial{z}}{\partial{s}} &= \frac{\partial{z}}{\partial{x}}\frac{\partial{x}}{\partial{u}} + \frac{\partial{z}}{\partial{y}}\frac{\partial{y}}{\partial{u}}\\\\
&= 4uv\ln(u\sin(v))\frac{1}{u} + \frac{4v}{\sin(v)}\sin(v)\\
&= 4v\ln(u\sin(v)) + 4v
\end{align*}
$$

## Implicit Differentiation (again)
If $F(x, y)$ is differentiable and $F(x, y) = 0$ defines $y$ as differentiable function of $x$,
$$
\Large
\frac{dy}{dx} = -\frac{F_x}{F_y}
$$
In 3D,
If $z = f(x, y)$ and $F(x, y, f(x, y)) = 0$, you can do the same thing, but to find $\frac{\partial{z}}{\partial{x}}, \frac{\partial{z}}{\partial{y}}$
### Examples
![[Pasted image 20220116112825.png]]
![[Pasted image 20220116113020.png]]
