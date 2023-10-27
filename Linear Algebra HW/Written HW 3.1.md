### Charles Liu

**1. (8 pts)** Consider the matrix A,

$\large{A = \begin{bmatrix} 2 & 0 & 3 \\ −1 & 1 & −2 \\ 3 & 0 & 1\end{bmatrix}}$

Find the determinant of $\large{A}$ by expanding about a row or column in 3 different ways. Please indicate which row/column you are expanding about before showing your work.

##### Solution.
- **(1) 2nd Column (Best Approach)**

- **(2) 1st Row**
>$\large{\begin{align}\det(A) &= a_{11} * C_{11} + a_{12} * C_{12} + a_{13} * C_{13} \\ \\ &= 2 * \begin{vmatrix} 1 & -2 \\ 0 & 1 \end{vmatrix} + 0 + 3 * \begin{vmatrix} -1 & 1 \\ 3 & 0 \end{vmatrix} \\ \\ &= 2 *(1 * 1 - (-2) * 0) + 3 * ((-1) * 0 - 1 * 3) \\ \\ &= 2 * 1 + 3 * (-3) = 2 - 9 = -7\end{align}}$

- **(2) 3rd Row**
>$\large{\begin{align}\det(A) &= a_{31} * C_{31} + a_{32} * C_{32} + a_{33} * C_{33}\\ \\ &= 3 * \begin{vmatrix} 0 & 3 \\ 1 & -2 \end{vmatrix} + 0 + 1 * \begin{vmatrix} 2 & 0 \\ -1 & 1 \end{vmatrix} \\ \\ &= 3 *(0 * (-2) - 3 * 1) + 1 * (2 * 1 - 0 * (-1)) \\ \\ &= 3 * (-3) + 1 * 2 = -9 + 2 = -7\end{align}}$

___

**2. (14 pts)** Consider the same matrix A,

$\large{A = \begin{bmatrix} 2 & 0 & 3 \\ −1 & 1 & −2 \\ 3 & 0 & 1\end{bmatrix}}$

**(a) (4 pts)** Multiply the first row by a nonzero constant, $\large{a}$. What is the determinant?

**Cofactor expansion across 2nd column**

$\large{M = \begin{bmatrix} 2a & 0 & 3a \\ −1 & 1 & −2 \\ 3 & 0 & 1\end{bmatrix}}$

$\large{\begin{align}\det(M) &= m_{12} * C_{12} + m_{22} * C_{22} + m_{32} * C_{32} \\ \\ &= 0 + \begin{vmatrix} 2a & 3a \\ -1 & -2 \end{vmatrix} + 0 \\ \\ &= 2a * 1 - 3a * 3 = 2a - 9a = -7a\end{align}}$

**(b) (2 pts)** Suppose we multiplied the entire matrix $\large{A}$ by $\large{a}$. Without doing any calculations, what do you think the answer will be? (no justification necessary).

$\large{-7a^3}$

**(c) (4 pts)** Calculate the determinant of $\large{aA}$.

$\large{aA = \begin{bmatrix} 2a & 0 & 3a \\ −a & a & −2a \\ 3a & 0 & a\end{bmatrix}}$

$\large{\begin{align}\det(aA) &= 0 + a * C_{22} + 0 \\ \\ &= 0 + a * \begin{vmatrix} 2a & 3a \\ 3a & a \end{vmatrix} + 0 \\ \\ &= a * (2a * 1a - 3a * 3a) = a * (2a^2 - 9a^2) = -7a^3\end{align}}$

**(d) (4 pts)**
    **(i)** Suppose B is a 4×4 matrix and the determinant of B is 6. What is the $\large{\det(3B)}$?
	$\large{\det(3B) = \det(B) * 3^4 = 6 * 3^4 = 6 * 81 = 486}$
	**(ii)** Suppose C is a 10 × 10 matrix and the determinant of C is 32. What is the $\large{\det(\frac{1}{2}C)}$?
    $\large{\det(\frac{1}{2}C) = det(C) * (\frac{1}{2})^{10} = 32 * (\frac{1}{2})^{10} = 32 * \frac{1}{1024} = \frac{1}{32}}$

___
