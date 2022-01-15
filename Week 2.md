# 12.5: Lines & Planes in Space
## Lines
The **vector equation** for line L through $P_0(x_0, y_0, z_0)$ parallel to vector $\vec{v}$:
$$
\Large \vec{r}(t) = \overbrace{\vec{r}_{0}}^{P_0} + t\vec{v} \hspace{0.5em} (-\infty < t < \infty)
$$
The **standard parametrization** through $P_0(x_{0},y_{0},z_{0})$ parallel to $\vec{v} = v_{1}\mathbf{i} + v_2\mathbf{j} + v_3\mathbf{k}$:
$$
\Large
\begin{align*}
x(t) = x_{0} + tv_{1}\\
y(t) = y_{0} + tv_{2}\\
z(t) = z_{0} + tv_{3}\\
\end{align*}
$$
If is line, $-\infty < t < \infty$. If t is bounded, is line segment.

### Distance from point to line
![[Pasted image 20220114213643.png]]
$$
\Large
d = \frac{\left\Vert\overrightarrow{PS} \times \vec{v}\right\Vert}{\Vert\vec{v}\Vert}
$$

## Planes
The **vector equation** for a plane through $P_{0}(x_{0}, y_{0}, z_{0})$ with normal vector $\vec{n} = A\mathbf{i} + B\mathbf{j} + C\mathbf{k}$ is given by:
$$
\Large
\vec{n} \cdot (\overrightarrow{P_{0}P}) = 0
$$
Component equation: 
$$\Large A(x - x_{0}) + B(y - y_{0}) + C(z-z_{0}) = 0$$
### Angle between two planes
* Parallel planes have the same normal.
* Angle between two intersecting planes = acute angle between normals $\Large \left(\cos \theta =  \frac{|\vec{n}_{1}\cdot\vec{n}_{2}|}{\Vert\vec{n}_{1}\Vert\Vert\vec{n}_{2}\Vert}\right)$

### Distance from point to plane
![[Pasted image 20220114213751.png]]
$$
\Large
d = \left\Vert\text{proj}_\hat{n}{\overrightarrow{PS}}\right\Vert = \overrightarrow{PS} \cdot \overbrace{\hat{n}}^{\mathclap{\text{normalized } \vec{n}}}
$$

Use this to find distance between skew lines
* Given lines $l_1, l_2$, find normalized normal vector $\vec{n}$, and project $\overrightarrow{PS}$
## Intersecting lines & planes

### Lines
Lines: $l_{1}, l_{2}$ can be: parallel, coincident, skew, intersecting
* coincident: same line
* skew: neither parallel nor intersecting

**If direction vectors are same, parallel or coincident**
* Pick point on $l_1$. If on $l_2$, coincident
* Else parallel

**If not, skew or intersecting**
* Check for intersecting point. If exists, intersecting
* Else skew


### Planes
Parallel, intersecting, coincident

* If normals are parallel, planes are parallel
* If normals are not parallel, cross product gives direction vector for line of intersection of the planes

### Line & Plane
* Substitute line into plane and find point where line & plane intersect

# 12.6: Cylinders and Quadric Surfaces
**Cylinder**: surface generated by moving straight line along given planar curve, holding line parallel to given fixed line
* Curve used to make cyl. is the **generating curve**
![[img/Pasted image 20220114213604.png|200]]
**Quadric Surface**: 2nd degree equation in x, y, z
$$\Large Ax^2 + By^2 + Cz^2 + Dxy +Exz + Fyz + Gx + Hy + Jz + K = 0$$

**Elliptical Paraboloid**: $\Large \frac{x^2}{a^2} + \frac{y^2}{b^2} = \frac{z}{c}$
![[img/Pasted image 20220114214234.png|200]]

**Ellipsoid**: $\Large \frac{x^2}{a^2} + \frac{y^2}{b^2} + \frac{z^2}{c^2} = 1$
![[img/Pasted image 20220114214246.png|200]]

**Elliptical Cone**: $\Large \frac{x^2}{a^2} + \frac{y^2}{b^2} = \frac{z^2}{c^2}$
![[img/Pasted image 20220114214259.png|200]]

**Hyperboloid of One Sheet**: $\Large \frac{x^2}{a^2} + \frac{y^2}{b^2} - \frac{z^2}{c^2} = 1$
![[img/Pasted image 20220114214313.png|200]]

**Hyperboloid of Two Sheets**: $\Large -\frac{x^2}{a^2} - \frac{y^2}{b^2} + \frac{z^2}{c^2} = 1$
![[img/Pasted image 20220114214324.png|200]]

**Hyperbolc Paraboloid**: $\Large \frac{y^2}{b^2} - \frac{x^2}{a^2} = \frac{z}{c}$
![[img/Pasted image 20220114214339.png|200]]

$\Large \text{\frak{Saddle from "how to theoretically turn a sphere inside out" lookin ass}}$

# 13.1, 13.2: Vector Functions
Vector function $\Large \vec{f}\text{: }\mathbb{R} \mapsto \mathbb{R}^n$
- Given real valued functions $\Large f_1, f_2, f_3$,
	- $\Large \vec{f}(t) = f_1(t)\mathbf{i} + f_2(t)\mathbf{j} + f_3(t)\mathbf{k}$
- $\Large f_1, f_2, f_3$ are the **components** of $\Large \vec{f}$
- Parametrization should be obvious

## Limits of Vector Functions
Let $\vec{r}(t) = f(t)\mathbf{i} + g(t)\mathbf{j} + h(t)\mathbf{k}$,
$$
\Large
\lim_{t \to t_0} {\vec{r}(t)} = \vec{L}
$$
if for every $\epsilon > 0$, there exists corresponding $\delta > 0$ such that for all $t \in D$,
$$
\Large
\Vert \vec{r}(t) - \vec{L}\Vert < \epsilon \text{ whenever } 0 < \vert t - t_0\vert < \delta
$$

idk why i wrote that cause basically the idea is: to find lim, find lim of each component

$\vec{f}$ is **continuous** at point $t = t_0$ if $\displaystyle \lim_{t \to t_0} {\vec{f}(t)} = \vec{f}(t_0)$ 
($\vec{f}$ is continuous if all points are continuous)

### Limit rules
Given $\Large \vec{f}(t) \to \vec{L}, \vec{g}(t) \to \vec{M}, u(t) \to U$, then:

1. $\vec{f}(t) + \vec{g}(t) \to \vec{L} + \vec{M}$
2. $\alpha\vec{f}(t) \to \alpha\vec{L}$
3. $u(t)\vec{f}(t) \to U\vec{L}$
4. $\vec{f}(t) \cdot \vec{g}(t) \to \vec{L} \cdot \vec{M}$
5. $\vec{f}(t) \times \vec{g}(t) \to \vec{L} \times \vec{M}$

## Derivatives of Vector Functions
$$
\Large
\vec{r}'(t) = \lim_{\Delta t \to 0}{\frac{\vec{r}(t+\Delta t) - \vec{r}(t)}{\Delta t}}
$$
If limit exists, $\vec{r}$ is **differentiable** at t. 
($\vec{r}$ is differentiable if all points are differentiable)

$\vec{r}'$ is the same as the sum of the derivatives of each component

### Derivative rules
1. $(\vec{f} + \vec{g})'(t) = \vec{f}'(t) + \vec{g}'(t)$
2. $(\alpha\vec{f})'(t) = \alpha\vec{f}'(t)$
3. $(\vec{f} \cdot \vec{g})'(t) = \vec{f}'(t)\cdot\vec{g}(t) + \vec{f}(t)\cdot\vec{g}'(t)$ (product rule, applies for *dot product*, *cross product*, *scalar multiplication*)
4. $(\vec{f} \circ u)'(t) = \vec{f}'(u(t))u'(t)$ (chain rule)

### Tangent Lines, Velocity, Acceleration
$\vec{r}(t)$ is **smooth** if $\frac{dr}{dt}$ is continuous & never zero

Tangent line to smooth curve $\vec{r}(t) = f(t)\mathbf{i} + g(t)\mathbf{j} + h(t)\mathbf{k} \text{ at } t = t_0$
is the line that passes $\vec{r}(t_0)$ & is parallel to $\vec{r}'(t_0)$.

If $\vec{r}$ is position,
* $\Large \vec{v} = \frac{d\vec{r}}{dt}$ (velocity)
* $\Large \vec{a} = \frac{d\vec{v}}{dt}$ (acceleration)
* direction of motion = direction of $\vec{v}$
* speed = $\Vert\vec{v}\Vert$

## Integrals of Vector Functions
$\vec{R}(t)$ is antiderivative of $\vec{r}(t)$ on interval $I$ if $\frac{d\vec{R}}{dt} = \vec{r}$ at each point in $I$.

$$
\Large
\int\vec{r}(t)\,dt = \vec{R}(t) + \vec{C}
$$
(componentize to find indef/def integral)

### Integral rules
1. $\int^b_a (\vec{f} + \vec{g})(t)\,dt = \int^b_a{\vec{f}(t)}\,dt + \int^b_a{\vec{g}(t)}\,dt$
2. $\int^b_a (\alpha\vec{f})(t)\,dt = \alpha\int^b_a{\vec{f}(t)}\,dt$
3.  $\int^b_a (\vec{c}\vec{f})(t)\,dt = \vec{c}\int^b_a{\vec{f}(t)}\,dt$
4. $\left\Vert\int^b_a (\vec{f})(t)\,dt\right\Vert \leq \int^b_a{\left\Vert\vec{f}(t)\right\Vert}\,dt$

## Projectile Motion
**Ideal projectile motion**: $\Large \text{\frak{bro use kinematics}}$