# 15.4: Double Integrals in Polar Form
Area of a polar region is based on the area of a sector of a circle.
- Area of a circle: $\pi r^2$
- Area of a sector: $\frac{\theta}{2\pi}\cdot\pi r^2 = \frac{1}{2}r^2\theta$
![[Screen Shot 2022-01-21 at 15.32.15.png|200]]
$$
\Large
\begin{align*}
\text{Area of polar region} &= \int_\alpha^\beta \frac{1}{2}r^2\,d\theta\\
&= \int_\alpha^\beta \int_a^b r\,dr\,d\theta\\
&= \iint_R r\,dr\,d\theta
\end{align*}
$$
(Note that $\int^b_a r\,dr = \left.\frac{1}{2}r^2\right|^b_a$)
$$
\Large
dA = r\,dr\,d\theta = dx\,dy
$$

Given $F(r, \theta)$ is continuous on $\Gamma: a \leq r \leq b, \alpha \leq \theta \leq \beta$:
$$
\Large
\iint_\Gamma F(r, \theta)r\,dr\,d\theta = \int_\alpha^\beta\int_a^b F(r, \theta)r\,dr\,d\theta
$$
Given $F(r, \theta)$ is continuous on $\Omega: \alpha \leq \theta \leq \beta, \rho_1(\theta) \leq r \leq \rho_2(\theta)$:
$$
\Large
\iint_\Omega F(r, \theta)r\,dr\,d\theta = \int_\alpha^\beta\int_{\rho_1(\theta)}^{\rho_2(\theta)} F(r, \theta)r\,dr\,d\theta
$$
Fubini's Theorem applies here. (Bounds can be switched or rearranged as described in Fubini's.)

## Volume

If $F(r, \theta) \geq 0$ over region $R$, then volume with $R$ as base, bounded above by $F(r, \theta)$ is:
$$
\Large
V = \iint_RF(r,\theta)r\,dr\,d\theta
$$
(same as double integrals above)
![[Pasted image 20220121154319.png|500]]

# 15.5: Triple Integrals
Instead of working with two variables continuous over a plane, THREE variables!

## Integration over a box
Given $f(x, y, z)$ continuous on box $B: a_x \leq x \leq b_x, a_y \leq y \leq b_y, a_z \leq z \leq b_z$
$$
\Large
\iiint_Bf(x,y,z)\,dV = \int_{a_z}^{b_z}\int_{a_y}^{b_y}\int_{a_x}^{b_x}f(x,y,z)\,dx\,dy\,dz
$$
Fubini's Theorem applies here too.

## Volume
$$
\Large
V = \iiint_D\,dV
$$
## Average Value
The average value of a function $F$ over region $D$ in space is:
$$
\Large
\text{Average Value of } F \text{ over } D = \frac{1}{\text{Volume of } D}\iiint_DF\,dV
$$
# 15.6: Applications of Double & Triple Integrals
Recall from physics:

(mass)
$$
\Large
\begin{align*}
dm &= \sigma\,dA \text{ (2 dimensions)}\\
dm &= \rho\,dV \text{ (3 dimensions)}
\end{align*}
$$
(moment)
$$
\Large
dM = r\,dm
$$
(moment of inertia)
$$
\Large
dI = r^2\,dm
$$
Rest of these formulas can essentially be defined by these relationships.

## Mass and First Moments
### In three dimensions
Mass:
$$
\Large
M = \iiint_D \rho\,dV
$$
First moments about the coordinate planes:
$$
\Large
\begin{align*}
M_{yz} &= \iiint_D x\rho\,dV\\
M_{xz} &= \iiint_D y\rho\,dV\\
M_{xy} &= \iiint_D z\rho\,dV
\end{align*}
$$
Center of mass:
$$
\Large
\begin{align*}
\bar{x} &= \frac{M_{yz}}{M}\\
\bar{y} &= \frac{M_{xz}}{M}\\
\bar{z} &= \frac{M_{xy}}{M}
\end{align*}
$$
When density of solid object is constant ($\rho = 1$), the center of mass is called the **centroid** of the object.
### In two dimensions
Mass:
$$
\Large
M = \iint_D \sigma\,dA
$$
First moments about the coordinate axes:
$$
\Large
\begin{align*}
M_{y} &= \iint_D x\sigma\,dA\\
M_{x} &= \iint_D y\sigma\,dA
\end{align*}
$$
Center of mass:
$$
\Large
\begin{align*}
\bar{x} &= \frac{M_{y}}{M}\\
\bar{y} &= \frac{M_{x}}{M}\\
\end{align*}
$$

## Moments of Inertia
### In three dimensions
$$
\Large
I = \iiint r^2\rho\,dV
$$
(Around x-axis, $r^2$ is $(y^2 + z^2)$, etc etc)

### In two dimensions
$$
\Large
I = \iint r^2 \sigma \,dA
$$
About origin:
$$
\Large
I_O = \iint (x^2 + y^2)\sigma\,dA = I_x + I_y
$$
## Joint Probability Density
**Joint probability density function** $f$ is a function that satisfies:
1. $\Large f(x, y) \geq 0$
2. $\Large \int^\infty_{-\infty}\int^\infty_{-\infty} f(x,y)\,dx\,dy = 1$
3. $\Large P((X, Y) \in R) = \iint_R f(x, y) \, dx \, dy$

