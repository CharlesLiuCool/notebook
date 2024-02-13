1. Suppose $\large{\mathbf{v} = 3\mathbf{i} - \mathbf{j} + 2\mathbf{k}}$ and $\large{\mathbf{w} = 5\mathbf{i} + 4\mathbf{j} - \mathbf{k}}$.
	**a)** Use the dot product to determine whether the angle between $\large{\mathbf{v}}$ and $\large{\mathbf{w}}$ is acute or obtuse.
		$\large{\mathbf{v} \cdot \mathbf{w} = \langle 3, -1, 2 \rangle \cdot \langle 5, 4, -1\rangle = 3 \cdot 5 - 1 \cdot 4 + 2 \cdot (-1) = 15 - 4 - 2 = 9}$
		Since $\large{9 > 0}$, the angle is **acute**.
		
	**b)** Find a vector that is perpendicular to both $\large{\mathbf{v}}$ and $\large{\mathbf{w}}$.
		Use cross product
		
		$\large{\begin{align} &\mathbf{v} \times \mathbf{w} = \begin{vmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ 3 & -1 & 2 \\ 5 & 4 & -1 \end{vmatrix} = \mathbf{i} \cdot \begin{vmatrix} -1 & 2 \\ 4 & -1 \end{vmatrix} - \mathbf{j} \cdot \begin{vmatrix} 3 & 2 \\ 5 & -1 \end{vmatrix} + \mathbf{k} \cdot \begin{vmatrix} 3 & -1 \\ 5 & 4 \end{vmatrix} \\ \\ &= \mathbf{i} \cdot ((-1) \cdot (-1) - 2 \cdot 4) - \mathbf{j} \cdot (3 \cdot (-1) - 2 \cdot 5) + \mathbf{k} \cdot (3 \cdot 4 - (-1) \cdot 5) \\ &= \langle 1, 0, 0 \rangle \cdot (-7) - \langle 0, 1, 0 \rangle \cdot (-13) + \langle 0, 0, 1 \rangle \cdot 17 = \color{magenta} \langle -7, 13, 17 \rangle\end{align}}$
	.

2. **a)** Find a vector equation for the line through the points $\large{(3, 2, 1)}$ and $\large{(5, -1, 7)}$.
	$\large{\mathbf{r}_0 = \langle 3,2,1\rangle}$
	$\large{\mathbf{v} = \langle 5, -1, 7 \rangle - \langle 3, 2, 1\rangle = \langle 2, -3, 6\rangle}$
	$\large{\color{magenta} \mathbf{r}(t) = \mathbf{r}_0 + t \cdot \mathbf{v} = \langle 3, 2, 1 \rangle + t \langle 2, -3, 6 \rangle}$
	
	**b)** Find an equation for the plane which contains $\large{(-4, 1, 0)}$ and is orthogonal to the line $\large{x = 3 + t}$, $\large{y = -4 - 2t}$, $\large{z = 5t}$.
	normal direction vector $\large{ = \langle 1, -2, 5 \rangle}$
	$\large{x - 2y + 5z = D}$
	$\large{-4 - 2 \cdot 1 + 5 \cdot 0 = -4 -2 + 0 = -6 = D}$
	$\large{\color{magenta} x - 2y + 5z = -6}$
    .
3. Given the space curve $\large{\mathbf{r}(t) = \langle \sin(\pi t), 4 - \dfrac{1}{2}t^2, \cos(\pi t) \rangle}$, $\large{t \geq 0}$:
	**a)** If this curve represents the position of a particle in space (with time in seconds and position coordinates in meters), find the *velocity*, *speed*, and *acceleration functions* for the particle. Also, find the velocity, speed, and acceleration at time $\large{\color{magenta} t = 3}$.
	$\large{\mathbf{v}(t) = \mathbf{r}'(t) = \color{magenta} \langle \pi\cos(\pi t), -t, -\pi \sin(\pi t) \rangle}$
	
	$\large{\begin{align}\mathbf{s}(t) &= |\mathbf{v}(t)| = \sqrt{(\pi\cos(\pi t))^2 + (-t)^2 + (-\pi \sin(\pi t)^2)} \\ &= \sqrt{\pi^2\cos^2(\pi t) + t^2 + \pi^2 \sin^2(\pi t)} = \sqrt{\pi^2(\cos^2(\pi t) + \sin^2(\pi t)) + t^2} \\ &= \color{magenta} \sqrt{\pi^2 + t^2}\end{align}}$ 
	**Recall speed is scalar!**
	
	$\large{\mathbf{a}(t) = \mathbf{v}'(t) = \color{magenta} \langle -\pi^2 \sin(\pi t), -1, -\pi^2 \cos(\pi t) \rangle}$
	
	$\large{\mathbf{v}(3) = \langle \pi\cos(3\pi), -3, -\pi \sin(3\pi) \rangle = \color{magenta} \langle -\pi, -3, 0 \rangle}$
	
	$\large{\mathbf{s}(3) = \sqrt{\pi^2 + 3^2} = \color{magenta} \sqrt{\pi^2 + 9}}$
	
	$\large{\mathbf{a}(3) = \langle -\pi^2 \sin(3\pi), -1, -\pi^2 \cos(3\pi) \rangle = \color{magenta} \langle 0, -1, \pi^2 \rangle}$
	
	**b)** Find the unit tangent vector $\large{\mathbf{T}(t)}$.
	
	$\large{\begin{align} \mathbf{T}(t) &= \dfrac{\mathbf{r}'(t)}{|\mathbf{r}'(t)}| = \dfrac{\mathbf{v}(t)}{\mathbf{s}(t)} = \dfrac{\langle \pi\cos(\pi t), -t, -\pi \sin(\pi t) \rangle}{\sqrt{\pi^2 + t^2}} \\ \\ &= \color{magenta} \left\langle \dfrac{\pi\cos(\pi t)}{\sqrt{\pi^2 + t^2}}, -\dfrac{t}{\sqrt{\pi^2 + t^2}}, -\dfrac{\pi \sin(\pi t)}{\sqrt{\pi^2 + t^2}} \right\rangle\end{align}}$
	
	**c)** Find parametric equations for the line that is tangent to this curve at the point $\large{(0, 2, 1)}$.
	
	$\large{\langle x, y, z \rangle = \left\langle \dfrac{\pi\cos(\pi t)}{\sqrt{\pi^2 + t^2}}, -\dfrac{t}{\sqrt{\pi^2 + t^2}}, -\dfrac{\pi \sin(\pi t)}{\sqrt{\pi^2 + t^2}} \right\rangle}$
	
	
	**d)** Graph the curve for $\large{0 \leq t \leq 2}$. Indicate positive orientation, and label the points at $\large{t = 0}$, $\large{t = 1}$, and $\large{t = 2}$ with their coordinates.
    
4. For the curve $\large{\mathbf{r}(t) = t^2\mathbf{i} + (1 - t^2)\mathbf{j} + (2 + t^3)\mathbf{k}}$: a) Find expressions for the tangential acceleration, normal acceleration, and curvature at any $\large{t}$ value. b) Find the length of the piece of the curve from $\large{t = 0}$ to $\large{t = 1}$.
    
5. Sketch and describe the surfaces $\large{x^2 + 4y = 4}$ and $\large{z^2 + 4y^2 - 2x = 1}$ as well as you can.
    
6. For the function/surface $\large{z = f(x, y) = \sqrt{4x^2 + y^2}}$, plot level curves for $\large{z}$-levels of 0, 1, 2, 3, 4. Label each level curve with its $\large{z}$-level.
    
7. For the multivariable function $\large{G(x, y, z) = \ln(x^2 + y^2 + z^2 - 1)}$, do the following: a) Compute $\large{G(1, 2, 3)}$. b) Describe the domain of $\large{G}$. c) Describe the level surfaces of $\large{G}$.
    
8. Show that $\large{\lim_{(x,y) \to (0,0)} \dfrac{2xy}{x^2 + 2y^2}}$ does not exist.
    
9. Find the value of $\large{\lim_{(x,y) \to (2,2)} \dfrac{x^2 - y^2}{x - y}}$, and discuss the continuity of $\large{f(x, y) = \dfrac{x^2 - y^2}{x - y}}$.
    
10. Given the following relations, use the chain rule to find expressions for $\large{\dfrac{\partial w}{\partial t}}$ and $\large{\dfrac{\partial w}{\partial r}}$: $\large{w = x \sin(4z - 3y)}$, $\large{x = e^{3t-r^2}}$, $\large{y = rt^2}$, $\large{z = \dfrac{1}{rt}}$
    
11. Given that $\large{z = x^2y + \ln(2x + 3y)}$, $\large{x = t^2}$, $\large{y = e^{1-t}}$, find the value of $\large{\dfrac{dz}{dt} \bigg|_{t=1}}$.
    
12. For each question, write the letter for the correct answer in the blank. i) Which of the following statements is true? (A) $\large{\mathbf{j} \times \mathbf{i} = \mathbf{k}}$ (B) $\large{\mathbf{k} \times \mathbf{j} = \mathbf{i}}$ (C) $\large{\mathbf{k} \times \mathbf{i} = \mathbf{j}}$ ii) Which is the domain of the function $\large{f(x, y) = \dfrac{x}{\sqrt{x + y}}}$? (A) all points in $\large{\mathbb{R}^2}$ except those on the line $\large{y = x}$ (B) all points in $\large{\mathbb{R}^2}$ except those on the line $\large{y = -x}$ (C) all points in $\large{\mathbb{R}^2}$ below the line $\large{y = -x}$ (D) all points in $\large{\mathbb{R}^2}$ above the line $\large{y = -x}$ iii) For which function is it true that $\large{f_x = 2x + 4y}$ and $\large{f_y = 4x + 3y^2}$? (A) $\large{f(x, y) = x^2 + y^3 + 4xy}$ (B) $\large{f(x, y) = x^2 + 4x + 4y + y^3}$ (C) $\large{f(x, y) = x^2y^3 + 4xy}$