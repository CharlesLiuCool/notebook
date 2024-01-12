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

Last time:
![[Review Graphic 1]]

### Examples:

#### 13.3 (26)

>[!question]
Compute $\large{\vec{u} \cdot \vec{v}}$ and find the angle between $\large{\vec{u}}$ and $\large{\vec{v}}$:

$$\large{\vec{u} = \text{<}3,-5,2\text{>}, \vec{v} = \text{<}-9,5,1\text{>}}$$

>[!check]- Solution
>$\large{\vec{u} \cdot \vec{v} = 3 \times (-9) + (-5) \times 5 + 2 \times 1 = -50}$
>Recall: $\large{\vec{u} \cdot \vec{v} = | \vec{u} | | \vec{v} | \cos\theta \implies \cos\theta = \dfrac{\vec{u} \cdot \vec{v}}{|\vec{u} ||\vec{v}|}}$
>$\large{\implies \theta = \cos^{-1}(\dfrac{\vec{u} \cdot \vec{v}}{|\vec{u}||\vec{v}|})}$
>
>So: $\large{|\vec{u}| = \sqrt{9 + 25 +4} = \sqrt{38}}$, $\large{|\vec{v}| = \sqrt{81 + 25 + 1} = \sqrt{107}}$,
>
>and $\large{\theta = \cos^{-1}\left(\dfrac{-50}{\sqrt{38}\sqrt{107}}\right) = \pi - \cos^{-1}\left(\dfrac{-50}{\sqrt{38}\sqrt{107}}\right)}$
>![[Review Graphic 2]]

#### 13.3 (40)

>[!question] Calculate $\large{\text{proj}_\vec{v}\,\vec{u}}$ and $\large{\text{scal}_\vec{v}\,\vec{u}}$:
>$$\large{\vec{u} = \vec{i} + 4 \vec{j} + 7 \vec{k} = \text{<}1, 4, 7 \text{>},\;\;\;\vec{v} = -2\vec{i} - 4\vec{j} + 2 \vec{k} = \text{<} -2, -4, 2\text{>}}$$

>[!check]- Solution
> $\large{\text{scal}_\vec{v}\,\vec{u} = \dfrac{\vec{u} \cdot \vec{v}}{|\vec{v}|} = \dfrac{-2 + (-16) + 14}{\sqrt{4 + 16 +4}} = \dfrac{-4}{24} = \dfrac{-4}{2\sqrt{6}} = \dfrac{-2}{\sqrt{6}}}$
> 
>$\large{\begin{align}\text{proj}_\vec{v}\,\vec{u} = (\dfrac{\vec{u} \cdot \vec{v}}{\vec{v} \cdot \vec{v}}) &= \dfrac{-4}{24} \text{<}-2, 4, 2\text{>} \\ \\ &= -\dfrac{1}{6}\text{<}-2, -4, 2 \text{>} \\ \\ &= -\dfrac{1}{6} \cdot (-2)\text{<}1,2,-1\text{>} \\ \\ &= \dfrac{1}{3} \text{<} 1, 2, -1\text{>} \\ \\ &= \text{<} \dfrac{1}{3}, \dfrac{2}{3}, -\dfrac{1}{3} \text{>}\end{align}}$

>[!book] Cross-Product
The *cross-product* of $\large{\vec{u}}$ with $\large{\vec{v}}$ is a vector, denoted $\large{\vec{u} \times \vec{v}}$, with these properties:
> 1. $\large{\vec{u} \times \vec{v}}$ is orthogonal to both $\large{\vec{u}}$ and $\large{\vec{v}}$
> 2. The direction of $\large{\vec{u} \times \vec{v}}$ is determined by the 
>    right hand rule":
>    ![[Review Graphic 3]]
> 3. $\large{|\vec{u} \times \vec{v}| = |\vec{u}| |\vec{v}|\,\sin\theta}$
>  = area of parallelogram below.
>  ![[Review Graphic 4]]


## Theorem 13.4 Properties of the Cross Product

Let $\large{\bf u}$, $\large{\bf v}$, and $\large{\bf w}$ be nonzero vectors in $\large{\mathbb{R}^3}$, and let $\large{a}$ and $\large{b}$ be scalars.

1. $\large{{\bf u} \times {\bf v} = -({\bf v} \times {\bf u})}$ Anticommutative property
2. $\large{(a{\bf u}) \times (b{\bf v}) = ab({\bf u} \times {\bf w})}$ Associative property
3. $\large{({\bf u}) \times ({\bf v} + {\bf w}) = ({\bf u} \times {\bf v}) + ({\bf u} \times {\bf w})}$ Distributive property
4. $\large{({\bf u} + {\bf v} \times {\bf w}) = ({\bf u} \times {\bf w}) + ({\bf v}) \times {\bf w}}$ Distributive property

Note: 
$\large{{\vec i} \times {\vec j} = {\vec k}}$
$\large{\vec{j} \times \vec{i} = -\vec{k}}$
$\large{\vec{j} \times \vec{k} = \vec{i}}$
etc.

![[Review Graphic 5|300]]

### Compute Cross Product

If $\large{\vec{u} = \text{<}u_1,\,u_2,\,u_3\text{>}}$ and $\large{\vec{v} = \text{<}v_1, v_2, v_3 \text{>}}$, then one way to compute $\large{\vec{u} \times \vec{v}}$ is

$$\large{\begin{align} \vec{u} \times {\vec{v}} &= (u_1\vec{i} + u_2 \vec{j} + u_3 \vec{k}) \times (v_1\vec{i} + v_2 \vec{j} + v_3 \vec{k}) \\ &= \text{... distribute, get 9 terms, use the facts that }\vec{i} \times \vec{j} = \vec{k}, \vec{j} \times \vec{i} = -\vec{k}, \text{etc.}\end{align}}$$


An easier way to compute $\large{\vec{u} \times \vec{v}}$ uses matrix determinants:

Let $\large{A}$ be a $\large{2}$ by $\large{2}$ matrix
and $\large{B}$ be a $\large{3}$ by $\large{3}$ matrix

$$\large{A = \begin{bmatrix} a & b \\ c & d \end{bmatrix}}$$

$$\large{B = \begin{bmatrix} a & b & c \\ d & e & f \\ g & h & i \end{bmatrix}}$$

The *determinant* of a $\large{2}$ by $\large{2}$ matrix $\large{\vec v}$
$$\large{\det \begin{bmatrix} a & b \\ c & d \end{bmatrix} = \begin{vmatrix} a & b \\ c & d \end{vmatrix} = ad - bc}$$

For a $\large{3}$ by $\large{3}$ determinant, we can use a *"cofactor expansion about the top row"*

$\large{\det\begin{bmatrix} a & b & c \\ d & e & f \\ g & h & i \end{bmatrix} =}$

$\large{= a \times \begin{vmatrix} e & f \\ h & i \end{vmatrix} - b \begin{vmatrix} d & f \\ g & i \end{vmatrix} + c \begin{vmatrix} d & e \\ g & h \end{vmatrix}}$

$\large{= a(ei -fh) - b(di - fg) + c(dh - eg)}$

Finding $\large{\vec{u} \times \vec{v}}$ using matrix determinants:

$$\large{\begin{align}\vec{u} \times \vec{v} &= \begin{vmatrix} \vec{i} & \vec{j} & \vec{k} \\ u_1 & u_2 & u_3 \\ v_1 & v_2 & v_3 \end{vmatrix} = \vec{i} \begin{vmatrix} u_2 & u_3 \\ v_2 & v_3 \end{vmatrix} - \vec{j} \begin{vmatrix}u_1 & u_3 \\ v_1 & v_3\end{vmatrix} + \vec{k} \begin{vmatrix} u_1 & u_2 \\ v_1 & v_2 \end{vmatrix} \\ \\ &= \text{<} u_2v_3 - u_3v_2, - (u_1v_3 - u_3v_1), u_1v_2-u_2v_1 \text{>} \end{align}}$$

#### 13.4 (27)

>[!question] 
> Find $\large{\vec{u} \times \vec{v}}$ and $\large{\vec{v} \times \vec{u}}$
$$\large{\vec{u} = 3\vec{i} - \vec{j} - 2\vec{k},\;\;\;\vec{v} = \vec{i} + 3\vec{j} - 2\vec{k}}$$

>[!check]- Solution
> $$\large{\vec{u} \times \vec{v} = \begin{vmatrix} \vec{i} & \vec{j} & \vec{k} \\ 3 & -1 & -2 \\ 1 & 3 & -2 \end{vmatrix} = \text{<} 8, 4, 10 \text{>}}$$
> 
$$\large{\vec{v} \times \vec{u} = -(\vec{u} \times \vec{v}) = \text{<} -8, -4, -10\text{>}}$$

#### 13.4 (35)

>[!question] Find the area of the triangle $\large{T}$ whose vertices are $\large{A(5,6,2)}$, $\large{B(7,16,4)}$, $\large{C(6,7,3)}$

>[!check]- Solution
>![[Review Graphic 6]]
>$\large{\overrightarrow{AB} \times \overrightarrow{AC} = \begin{vmatrix} \vec{i} & \vec{j} & \vec{k} \\ 2 & 10 & 2 \\ 1 & 1 & 1 \end{vmatrix} = \text{...} = \text{<}8,0,-8 \text{>}}$
>So the area of the parallelogram is $\large{|8, 0, -17| = \sqrt{128}}$, so the 
>
>area of the triangle is $\large{\dfrac{\sqrt{128}}{2} = \dfrac{8\sqrt{2}}{2} = 4\sqrt{2}}$

#### 13.5 Lines & Planes in Space ("space" means 3-D space, a.k.a $\mathbb{R}^3$)

**Preliminary Info:**
When a vector is drawn or pictured with its tail at the origin, it's called a *"position vector"*, because the vector's components then correspond to the coordinates of the point (position) at its tip:

![[Review Graphic 7]]

We'll often deal with a variable point $\large{(x, y, z)}$, and its position vector $\large{\text{<}x, y, z \text{>}}$. Just as we often give a name to a specified vector:
$$\large{\vec{v} = \text{<} 1, 2, -4\text{>}}$$
we can also give a name to the variable vector $\large{\text{<} x, y, z\text{>}}$.
Our text chooses to use $\large{\vec{r}}$ most of the time:
$$\large{\vec{r} = \text{<} x, y, z\text{>}}$$
much like functions are usually called $\large{f}$.

## The equation(s) of a line in space
![[Review Graphic 8|400]]