## Linear Transformations

### Standard Matrix

### Example 1.

Find the standard matrix for the linear transformation $\large{T}$: $\large{\mathbb{R}^2 \rightarrow \mathbb{R}^4}$, where $\large{T}$ is defined by

$$\large{T\left(\begin{bmatrix} x_1 \\ x_2\end{bmatrix}\right) = \begin{bmatrix} 7x_1 + 2 x_2 \\ -x_1 \\ 3x_2 \\ x_1 - x_2\end{bmatrix}}$$

#### Solution:

Standard basis of $\large{\mathbb{R}^2}$ 

$$\large{e_1 = \begin{bmatrix} \,1\, \\ 0 \end{bmatrix},\;\;\;\;e_2 = \begin{bmatrix} 0 \\ 1\end{bmatrix}}$$
$$\large{T(e_1) = T\left(\begin{bmatrix} 1 \\ 0\end{bmatrix} \right) = \begin{bmatrix} 7 \\ -1 \\ 0 \\ 1\end{bmatrix}}$$
$$$\large{T(e_2) = T\left( \begin{bmatrix} 0 \\ 1\end{bmatrix} \right) = \begin{bmatrix} 2 \\ 0 \\ 3 \\ -1 \end{bmatrix}}$$
So the standard matrix of $\large{T}$ is 

$$\large{A = [\;T(e_1)\;\;\;T(e_2)\;] = \begin{bmatrix} 7 & 2 \\ -1 & 0 \\ 0 & 3 \\ 1 & -1 \end{bmatrix}}$$
### [Domain and Codomain](1.8%20Introduction%20to%20Linear%20Transformation)

### Example 2.

Let $\large{T}$: $\large{\mathbb{R}^n \rightarrow \mathbb{R^m}}$ be a linear transformation given by $\large{T(x) = Ax}$ where 

$$\underbrace{\large{A = \begin{bmatrix} -1 & 1 & -3 & -6 \\ -3 & 3 & -8 & -16 \\ 2 & -2 & 7 & 15\end{bmatrix}}}_{\huge{\text{Standard Matrix for T}}}$$
**(1)** What's the domain of $\large{T}$?
**(2)** What's the codomain of $\large{T}$?

### Solution

$\large{A = 3 \times 4}$ matrix

$$\large{\underbrace{\begin{bmatrix} -1 & 1 & -3 & -6 \\ -3 & 3 & -8 & -16 \\ 2 & -2 & 7 & 15 \end{bmatrix}}_{\huge{3 \times 4}} \underbrace{\begin{bmatrix} x_1 \\ x_2 \\ x_3 \\ x_4 \end{bmatrix}}_{\huge{4 \times 1}} = \begin{bmatrix} -x_1 + x_2 -3x_3 - 6x_4 \\ -3x_1 + 3x_2 -8x_3 -16x_4 \\ 2x_1 -2x_2 + 7x_3 +15x_4\end{bmatrix}}$$
**(1)** domain (input space) is $\large{\mathbb{R}^4}$ 

**(2)** codomain (output space) is $\large{\mathbb{R}^3}$ 

### 1 - 1 vs. Onto

### Example 3.

Let $\large{T}$: $\large{R_4 \rightarrow R_3}$ be a linear transformation given by $\large{T(x) = Ax}$ where 

$$\large{A = \underbrace{\begin{bmatrix} -1 & 1 & -3 & -6 \\ -3 & 3 & -8 & -16 \\ 2 & -2 & 7 & 15 \end{bmatrix}_{3 \times 4}}_{\huge{\text{standard matrix for T}}}}$$
**(1)** Is $\large{T}$ *onto*? (or $\large{Ax = b}$ has at least one solution for every $\large{b}$ in $\large{\mathbb{R}^m}$)

**(2)** Is $\large{T}$ *1-1*? (or $\large{Ax = b}$ has at most one solution for every $\large{b}$ in $\large{\mathbb{R}^m}$)

#### Solution Key:

$$\large{T \text{ is onto} \iff A \text{ has a pivot in every row}}$$
$$\large{T \text{ is 1-1} \iff A \text{ has a pivot in every column}}$$
Note that by row reduction (ERO), we find an EF of $\large{A}$ 

$$\large{A = \begin{bmatrix} -1 & 1 & -3 & -6 \\ -3 & 3 & 8 & -16 \\ 2 & -2 & 7 & 15 \end{bmatrix} \xrightarrow {\Huge{\text{ERO}}} \underbrace{\begin{bmatrix} \fbox{1} & -1 & 3 & 6 \\ 0 & 0 & \fbox{1} & 2 \\ 0 & 0 & 0 & 1 \end{bmatrix}}_{\Huge{EF}}}$$
**(1)** So we see that $\large{A}$ has a pivot in every row, which implies that $\large{T}$ is *ONTO*.

**(2)** But $\large{A}$ does *NOT* have pivot in every column, which shows that $\large{T}$ is *NOT* 1-1.

#### Matrix Operations

- *Matrix Addition*
- *Scalar Multiplication*
- *Matrix Transpose*
- *Matrix Multiplication*
#### Example 4.

Given the matrices $\large{A}$, $\large{B}$, $\large{C}$, and $\large{D}$, compute the following if defined, otherwise explain why it is undefined

$$\large{A \begin{bmatrix} 1 & -1 \\ 0 & 3 \\ 2 & 0 \end{bmatrix},\;\;\;B=\begin{bmatrix} 1 & 0 & -1 \\ -2 & 0 & 0 \\ 0 & 1 & 0 \end{bmatrix},\;\;\;C = \begin{bmatrix} 3 & -1 \\ 9 & 3 \end{bmatrix},\;\;\;D = \begin{bmatrix} 2 & 4 \\ 1 & 2\end{bmatrix}}$$

**(a)** $\large{3A}$

$\large{3A = 3 \times \begin{bmatrix} 1 & -1 \\ 0 & 3 \\ 2 & 0 \end{bmatrix} = \begin{bmatrix} 3 & -3 \\ 0 & 9 \\ 6 & 0 \end{bmatrix}}$

**(b)** $\large{B + C}$

Matrix Addition requires matrices of the *same dimensions*. You cannot add a $\large{3 \times 3}$ with a $\large{2 \times 2}$

**(c)** $\large{C + 2D}$


$\large{C + 2D = \begin{bmatrix} 3 & -1 \\ 9 & 3 \end{bmatrix} + 2 \times \begin{bmatrix} 2 & 4 \\ 1 & 2 \end{bmatrix} = \begin{bmatrix} 3 & -1 \\ 9 & 3 \end{bmatrix} + \begin{bmatrix} 4 & 8 \\ 2 & 4 \end{bmatrix} = \begin{bmatrix} 7 & 7 \\ 11 & 7 \end{bmatrix}}$

**(d)** $\large{A^T = \begin{bmatrix} 1 & -1 \\ 0 & 3 \\ 2 & 0 \end{bmatrix}^{T} = \begin{bmatrix} 1 & 0 & 2 \\ -1 & 3 & 0 \end{bmatrix}}$

**(e)** $\large{BC}$ is undefined as

$$\large{B_{\huge{3\times\fbox{3}}}\;\;\large{C_{\huge{\fbox{2}\times2}}}}$$

the inner dimensions do *NOT* match

**(f)** $\large{CA^T}$

$\large{C A^T = \begin{bmatrix} 3 & -1 \\ 9 & 3 \end{bmatrix} \begin{bmatrix} 1 & 0 & 2 \\ -1 & 3 & 0 \end{bmatrix} = \begin{bmatrix} 3 \times 1 + (-1) \times (-1) & 3 \times 0 + (-1) \times 3 & 3 \times 2 + (-1) \times 0 \\ 9 \times 1 + 3 \times (-1) & 9 \times 0 + 3 \times 3 & 9 \times 2 + 3 \times 0 \end{bmatrix}}$
$\large{= \begin{bmatrix} 4 & -3 & 6 \\ 6 & 9 & 18 \end{bmatrix}}$

___

### Example 5. 

Given the dimensions of matrix $\large{A}$, $\large{B}$, $\large{C}$, and $\large{D}$, determine the dimensions of the matrices below or write "*NOT* defined".

$$\large{A\;\;\;4\times2\;\;\;\;\;\;B\;\;\;5\times2\;\;\;\;\;\;C\;\;\;2\times3\;\;\;\;\;D\;\;\;3\times5}$$

**(a)** $\large{4A}$ has the same dimension as $\large{A}$ and hence $\large{4A}$ is $\large{4 \times 2}$

**(b)** $\large{B_{5 \times 2}\;C_{2\times3}}$  is $\large{5 \times 3}$ Since the inner dimensions match and the outer dimensions is $\large{5 \times 3}$.

