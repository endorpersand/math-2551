# 13.3: Arc Length in Space

**Length** of smooth curve $\vec{r}(t) = x(t) \mathbf{i} + y(t) \mathbf{j} + z(t) \mathbf{k} \text{ } (a \leq t \leq b)$

$$
\Large
L = \int_a^b \sqrt{\left(\frac{dx}{dt}\right)^2 + \left(\frac{dy}{dt}\right)^2 + \left(\frac{dz}{dt}\right)^2}\,dt
$$
(pythagorean theorem between $dx, dy, dz$)

This is equivalent to:
$$
\Large
L = \int_a^b \Vert\vec{v}\Vert\,dt
$$

**Arc Length Parameter**: Function *s* that finds directed distance along curve starting from $P(t_0)$ to some point $P(t)$
$$
\Large
s(t) = \int_{t_0}^t \sqrt{\left(\frac{dx}{d\tau}\right)^2 + \left(\frac{dy}{d\tau}\right)^2 + \left(\frac{dz}{d\tau}\right)^2}\,d\tau = \int_{t_0}^t \Vert\vec{v}\Vert\,d\tau
$$

**Speed**:
$$
\Large
speed = \frac{ds}{dt} = \Vert\vec{v}(t)\Vert
$$

**Unit Tangent Vector**: Unit vector... that's tangent to the smooth curve idk what you expected lmao
$$
\Large
\vec{T}(t) = \frac{\vec{r}'(t)}{\Vert\vec{r}'(t)\Vert} = \frac{\vec{v}(t)}{\Vert\vec{v}(t)\Vert} = \frac{d\vec{r}/dt}{ds/dt}$$
($\vec{v}(t)$ normalized)

# 13.4: Curvature
If $\vec{T}$ is a unit vector of a smooth curve, the **curvature** function of the curve is
$$
\kappa = \left\Vert\frac{d\vec{T}}{ds}\right\Vert
$$
In the blue curve, the curvature at the point is related to circle that best fit curve at that point.
![[Pasted image 20220114225519.png]]
(seems similar to 2nd derivative)

For smooth curve $\vec{r}$, curvature can be written as scalar function:
$$
\Large
\kappa = \left\Vert\frac{d\vec{T}/dt}{ds/dt}\right\Vert = \frac{\Vert\vec{T}'(t)\Vert}{\Vert\vec{v}(t)\Vert}
$$

## Circle of Curvature
The **circle of curvature** (or **osculating circle**) at point $P$ on plane curve (2D) where $\kappa \neq 0$ is the circle of the curve that
1. is tangent to curve at $P$
2. has the same curvature the curve has at P
3. has center that lies toward the concave side of the curve

The **radius of curvature** at point $P$ is $\Large \rho = \frac{1}{\kappa}$.

* Straight lines: curvature is constantly 0
* Circle of radius $r$: Curvature is constantly $\frac{1}{r}$.

## Principal Normal Vector
If $\vec{T}(t)$ is unit tangent vector and $\vec{T}'(t) = 0$, then unit tangent vector d/n change direction.
If $\vec{T}'(t) \neq 0$, then

**Principal normal vector** = $\Large \vec{N}(t) = \frac{\vec{T}'(t)}{\Vert\vec{T}'(t)\Vert}$
($\vec{T}'$ normalized)
(this vector is $\perp$ to $\vec{T}$)

![[Pasted image 20220114230709.png]]

**Osculating plane**: Plane determined by unit tangent vector and principal normal vector
**Binormal vector**: $\Large \vec{B}(t) = \vec{T}(t) \times \vec{N}(t)$

**TNB frame / Finite frame**: The three vectors T, N, B

# 13.5: Tangential & Normal Components of Acceleration

Given position function $\vec{r}(t)$,
$$
\Large
\begin{align*}
& \vec{T}(t) = \frac{\vec{v}(t)}{ds/dt}\\
& \vec{v}(t) = \vec{T}(t) \frac{ds}{dt}\\
& \vec{a}(t) = \frac{d\vec{v}}{dt} = 
\vec{T}'(t) \frac{ds}{dt} + \vec{T}(t) \frac{d^2s}{dt^2}\\
\end{align*}
$$

Since $\Large \vec{N}(t) = \frac{\vec{T}'(t)}{\Vert\vec{T}'(t)\Vert}$,
$$
\Large
\begin{align*}
& \vec{N}(t)\Vert\vec{T}'(t)\Vert = \vec{T}'(t)\\
& \vec{a}(t) = \vec{N}(t)\Vert\vec{T}'(t)\Vert \frac{ds}{dt} + \vec{T}(t) \frac{d^2s}{dt^2}
\end{align*}
$$
So,
**Tangential component of acceleration:**
$$
\Large
a_T = \frac{d^2s}{dt^2}=\frac{d}{dt}\Vert\vec{v}\Vert
$$
* Only dependent on change of speed of object
* If speed is constant, $a_T = 0$ and acceleration is directed entirely towards center of curvature

**Normal component of acceleration:**
$$
\Large
a_N = \Vert\vec{T}'(t)\Vert \frac{ds}{dt} = \kappa\left(\frac{ds}{dt}\right)^2 = \kappa\Vert\vec{v}\Vert^2

$$
$\left(\text{recall }\Large \kappa = \frac{\Vert\vec{T}'(t)\Vert}{ds/dt}\right)$

## Curvature and Torsion
**Torsion**:

Let $\vec{B} = \vec{T} \times \vec{N}$.
$$
\Large
\tau = -\frac{d\vec{B}}{ds}\cdot \vec{N}
$$
* Measures how binormal vector changes with respect to arc length

$$
\Large
\tau = \frac{\begin{vmatrix}
\cdots & \vec{r}' & \cdots \\
\cdots & \vec{r}'' & \cdots \\
\cdots & \vec{r}''' & \cdots \\
\end{vmatrix}}{\Vert\vec{v} \times \vec{a}\Vert^2}
$$

### Formulas for Curvature and Torsion
$$
\Large
\begin{align*}
&\vec{T}\cdot\vec{a} = a_T(\vec{T}\cdot\vec{T}) + a_N(\vec{T}\cdot\vec{N}) = a_T\\
&\Vert\vec{T}\times\vec{a}\Vert = \Vert a_T(\vec{T}\times\vec{T})\Vert + \Vert a_N(\vec{T}\times\vec{N})\Vert = \Vert a_N \vec{B} \Vert = a_N
\end{align*}
$$
So,
$$
\Large
\begin{align*}
&a_T = \frac{\vec{v} \cdot \vec{a}}{ds/dt}\\
&a_N = \frac{\Vert\vec{v} \times \vec{a}\Vert}{ds/dt} = \kappa\left(\frac{ds}{dt}\right)^2
\end{align*}$$
And thus,
$$\Large
\kappa = \frac{\Vert\vec{v} \times \vec{a}\Vert}{(ds/dt)^3}$$

# 13.6: Motion in Polar Coordinates
Given coordinates $P(r, \theta)$,
position, velocity, and acceleration can be represented in terms of:
* $\Large \vec{u}_r = (\cos \theta)\mathbf{i} + (\sin \theta)\mathbf{j}$ (unit vector in direction of $\overrightarrow{OP}$)
* $\Large \vec{u}_{\theta} = -(\sin \theta)\mathbf{i} + (\cos \theta)\mathbf{j}$ ( unit vector pointing in direction of increasing $\theta$)

$$
\Large
\begin{align*}
\vec{r} = r\vec{u}_r &= r\cos\theta\mathbf{i} + r\sin\theta\mathbf{j}\\
\vec{v} = \frac{d\vec{r}}{dt} &= (-r\theta'\sin\theta +r'\cos\theta)\mathbf{i} + (r\theta'\cos\theta + r'\sin\theta)\mathbf{j}\\
&= r\theta'\vec{u}_{\theta} + r'\vec{u}_r\\
\vec{a} = \frac{d\vec{v}}{dt} &= (-r\theta'^2\vec{u}_r + (r\theta'' + r'\theta')\vec{u}_\theta) + (r''\vec{u}_r + r'\theta'\vec{u}_\theta)
\end{align*}

$$
(btw you can product rule $\vec{r} = r\vec{u}_r$ instead of expanding $\vec{r}$ and differentiating its components)

$$
\Large
\begin{align*}
\vec{r} &= r\vec{u}_r\\
\vec{v} &= r'\vec{u}_r + r\theta'\vec{u}_\theta\\
\vec{a} &= (r''-r\theta'^2)\vec{u}_r + (r\theta''+2r'\theta')\vec{u}_\theta
\end{align*}
$$

## Cylindrical Coordinates
$$
\Large
\begin{align*}
\vec{r} &= r\vec{u}_r + z\mathbf{k}\\
\vec{v} &= r'\vec{u}_r + r\theta'\vec{u}_\theta + z'\mathbf{k}\\
\vec{a} &= (r''-r\theta'^2)\vec{u}_r + (r\theta''+2r'\theta')\vec{u}_\theta + z''\mathbf{k}
\end{align*}
$$