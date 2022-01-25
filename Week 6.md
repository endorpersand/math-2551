# 14.8: Lagrange Multipliers
- Can be used to help solve optimization problems that have constraints

## Orthogonal Gradient Theorem
Suppose $f(x, y, z)$ is differentiable in region whose interior contains smooth curve:
$$
\Large
C: \vec{r}(t) = x(t)\mathbf{i} + y(t)\mathbf{j} + z(t)\mathbf{k}
$$

If $P_0$ is a point on $C$ where $f$ has a local extremum relative to its values on $C$, $\nabla f$ is orthogonal to $C$ at $P_0$.

**Corollary**
At the points on a smooth curve $\vec{r}(t) = x(t)\mathbf{i} + y(t)\mathbf{j}$ where a differentiable function $f(x, y)$ takes on its local extrema relative to its values on the curve, $\nabla f \cdot r' = 0$.

## Method
Suppose $f(x, y, z)$ and $g(x, y, z)$ are differentiable and $\nabla g \neq 0$ when $g(x, y, z) = 0$. To find local extremum of $f$ subject to $g(x, y, z) = 0$, find $x, y, z, \lambda$ satisfying:
$$
\Large
\begin{align*}
\nabla f &= \lambda \nabla g\\
g(x, y, z) &= 0
\end{align*}
$$
## Example
Maximize $xy$ on ellipse $4x^2 + 9y^2 = 36$.
$$
\Large
\begin{align*}
f(x, y) &= xy\\
\nabla f(x, y) &= y\mathbf{i} + x\mathbf{j}\\\\
g(x, y) &= 4x^2 + 9y^2 - 36\\
\nabla g(x, y) &= 8x\mathbf{i} + 18y\mathbf{j}
\end{align*}
$$

Equations formed:
$$
\Large
\begin{align*}
y &= \lambda (8x)\\
x &= \lambda (18y)\\
4x^2 + 9y^2 - 36 &= 0
\end{align*}
$$
We get values for x and y. This gives us points we can use to maximize $xy$.
$\lambda$ is unused.

# 14.9: Taylor's Formula for $\large f(x, y)$
**Taylor Polynomial** (recap)
If function $f$ has $n$ derivatives at point where $x = a$, then the nth Taylor Polynomial for $f$ at $a$ is:
$$
\Large
P_n(x) = \sum\limits^n_{k = 0}{\frac{f^{(k)}(a)(x-a)^k}{k!}}
$$
**The theorem**
If $f$ has $n + 1$ derivatives on an open interval containing $a$, then for every $x$ in that open interval, we have:
$$
\Large
f(x)=P_n(x) + \frac{f^{(n+1)}(c)}{(n+1)!}(x-a)^{n+1}
$$
for some (estimated) value $c$ between $a$ and $x$ that maximizes that term.

The absolute value of new term is called the error when using $P_n(x)$ to approximate $f(x)$.
$$
\Large
\text{error} = |f(x) - P_n(x)| = \frac{|f^{(n+1)}(c)|}{(n+1)!}|x-a|^{n+1}
$$
![[Pasted image 20220119184824.png]]
(I believe this was done in BC)
## Two Variables
Suppose $f(x, y)$ and its partials thru order $n+1$ are continuous throughout open rectangular region $R$ centered around $(a, b)$. Then, throughout R:
$$
\Large
f(a + h, b + k) = \sum\limits_{i=0}^{n+1}{\left.\frac{1}{i!}\left(h\frac{\partial}{\partial x} + k\frac{\partial}{\partial y}\right)^{i}f\right|_{(a,b)}}
$$
Error term is the last one, last is also an approximate error term.

# 14.10: Partial Derivatives w/ Constraints
Steps
1. Decide which variables are dependent & independent
2. Eliminate the other dependent variables
3. Differentiate and solve

## Example
If $\Large w = x^2 + y - z + \sin(t)$ and $\Large x + y = t$, find $\Large \left(\frac{\partial{w}}{\partial{y}}\right)_{z, t}$
(notation designates that $z, t$ are independent)

$$
\Large
\begin{align*}
x &= t - y\\
w &= (t - y)^2 + y - z + \sin(t)\\
\frac{\partial{w}}{\partial{y}} &= -2(t-y) + 1
\end{align*}
$$