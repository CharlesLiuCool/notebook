## Vector Review

Let $$\large{\vec{u} = <1, 2, 3> = \vec{i} + 2\vec{j}+3\vec{k}}$$
$$\large{\vec{v} = <2, -1, 4> = 2\vec{i} - \vec{j} + 4\vec{k}}$$

$\large{(\vec{i} =\;<1, 0, 0>, \vec{j} = <9, 1, 0>, \vec{k} = <0, 0, 1>)}$

Then the length of $\large{\vec{u}}$ is $\large{|\vec{u}| = \sqrt{1^2, 2^2 + 3^2}}$

a unit vector in the same direction as $\large{\vec{u}}$ is

$$\large{\dfrac{\vec{u}}{|\vec{u}|} = \dfrac{\text{<}1, 2, 3>}{\sqrt{14}}}$$

$\large{\vec{u} + \vec{v} = \text{<}1, 2, 3\text{>} + \text{<}2, -1, 4\text{>} = \text{<}3, 1, 7\text{>}}$

$\large{\vec{u} - \vec{v} =\text{<}1, 2, 3\text{>} - \text{<}2, -1, 4\text{>} = \text{<}-1, 3, -4\text{>}}$

The dot product of $\large{\vec{u} = \text{<}u_1,\;u_2,\;u_3\text{> and } \vec{v} = \text{<}v_1,\;v_2,\;v_3\text{> is}}$

$$\large{\vec{u} \cdot \vec{v} = u_1v_1 + u_2v_2 + u_3v_3 \;\;\text{ a number, or a scalar}}$$

### Recall:

$\large{\vec{u} \cdot \vec{v} = |\vec{u}|\,|\vec{v}|\,cos\theta}$

So $\large{\vec{u} \cdot \vec{v}}$ is

$\large{0}$ if $\large{\theta = \dfrac{\pi}{2}}$
$\large{< 0}$ if $\large{\dfrac{\pi}{2} > \theta \leq \pi}$
$\large{> 0}$ if $\large{0 <\theta < \dfrac{\pi}{2}}$

and $\large{\vec{u}}$ and $\large{\vec{v}}$ are orthogonal (perpendicular) $\large{\iff \vec{u} \cdot \vec{v} = \vec{0}}$

## Theorem 13.2

Properties of the Dot Product

Suppose $\large{{\bf u}, {\bf v}, {\bf w}}$ are vectors and let $\large{c}$ be a scalar.
1. $\large{{\bf u} \cdot {\bf v} = {\bf v} \cdot {\bf u}}$ Commutative Property
2. $\large{c({\bf u} \cdot {\bf v}) = (c{\bf u}) \cdot {\bf v} = {\bf u} \cdot (c{\bf v})}$ Associative Property
3. $\large{{\bf u} \cdot ({\bf v} + {\bf w}) = {\bf u} \cdot {\bf v} + {\bf u} \cdot {\bf w}}$ Distributive Property

The orthogonal projection of $\large{\vec{u}}$ onto $\large{\vec{v}}$:

```desmos-graph
left=-1; right=6;
top=7; bottom=-1;
---
(5,0)| hidden| label:U | BLUE
(2, 1) | hidden | label: V | RED
(2, 0) | hidden | label: projection | BLACK
y = 0 | x > 0 | x < 5 | BLUE
| y = 0.5x | x < 3 | x > 0 | RED
| y = 0 | x > 0 | x < 3 | BLACK
```

The length of the projection is $\large{|\vec{u}|\,cos(\theta) = \dfrac{|\vec{u}|\,|\vec{v}|cos\theta}{|\vec{v}|} = \dfrac{\vec{u} \cdot \vec{v}}{|\vec{v}|} = \text{scal}_{\vec{v}}\vec{u}}$

The vector is $\large{(\dfrac{\vec{u} \cdot \vec{v}}{|\vec{v}|})\dfrac{\vec{v}}{|\vec{v}|} = \left(\dfrac{\vec{u} \cdot \vec{v}}{|\vec{v}|^2} \right)\vec{v} = \left(\dfrac{\vec{u} \cdot \vec{v}}{\vec{v} \cdot \vec{v}}\right)\vec{v} = \text{proj}_\vec{v}\vec{u}}$

___

### Theorem 13.4 Properties of the Cross Product

Let $\large{\bf u}$, $\large{\bf v}$, and $\large{\bf w}$ be nonzero vectors in $\large{\mathbb{R}^3}$, and let $\large{a}$ and $\large{b}$ be scalars.

If $\large{\vec{u} = \text{<}u_1,\,u_2,\,u_3\text{>}}$ and $\large{\vec{v} = \text{<}v_1, v_2, v_3 \text{>}}$, then one way to compute $\large{\vec{u} \times \vec{v}}$ is

$$\large{}$$


An easier way to compute $\large{\vec{u} \times \vec{v}}$ uses matrix determinants:

$\large{A}$ is a 2 by 2 matrix

The *determinant* of a 2 by 2 matrix $\large{\vec v}$
$$\large{\det \begin{bmatrix} a & b \\ c & d \end{bmatrix} = \begin{vmatrix} a & b \\ c & d \end{vmatrix} = ad - bc}$$

For a 3 by 3 determinant, we can see 

Finding $\large{\vec{u} \times \vec{v}}$ using matrix determinants:

$$\large{\vec{u} \times \vec{v} = \begin{vmatrix} \vec{i} & \vec{j} & \vec{k} \\ u_1 & u_2 & u_3 \\ v_1 & v_2 & v_3 \end{vmatrix} = \vec{i} \begin{vmatrix} u_2 & u_3 \\ v_2 & v_3 \end{vmatrix} - \vec{j} \begin{vmatrix}u_1 & u_3 \\ v_1 & v_3\end{vmatrix} + \vec{k} \begin{vmatrix} u_1v_2 - u_2v_1 \end{vmatrix}}$$

#### 13.9 (27)

Find $\large{\vec{u} \times \vec{v}}$ and $\large{\vec{v} \times \vec{u}}$
$$\large{\vec{u} = 3\vec{i} - \vec{j} - 2\vec{k}, \vec{v} = \vec{i} + 3\vec{j} - 2\vec{k}}$$

#### Solution:

$$\large{\vec{u} \times \vec{v}}$$

#### 13.4 (35)

Find the area of the triangle $\large{T}$ whose vertices are $\large{A(5,6,2)}$, $\large{B(7,16,4)}$, $\large{C(6,7,3)}$

#### Solution:

#### 13.5 Lines & Planes in Space("space" means 3-D space, a.k.a $\mathbb{R}^3$)

We'll often deal with a variable 

## The equation(s) of a line in space

