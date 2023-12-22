**1. (a)** Find the standard matrix for the linear transformation $\large{T}$: $\large{\mathbb{R}^2 → \mathbb{R}^2}$ which first  
reflects about the line $\large{x_2 = x_1}$ and then rotates clockwise by $\large{90\degree}$.  

reflect about $\large{x_2 = x_1}$

$\large{\begin{bmatrix} 0 & 1 \\ 1 & 0 \end{bmatrix}}$

rotate clockwise by $\large{90 \degree}$ from there

$\large{\begin{bmatrix} \cos(90\degree) & -\sin(90\degree) \\ \sin(90\degree) & \cos(90\degree) \end{bmatrix}}$

= $\large{\begin{bmatrix} 0 & -1 \\ 0 & 1 \end{bmatrix}}$

>**Recall:** Rotational matrix: $$\large{\begin{bmatrix} \cos(\theta\degree) & -\sin(\theta\degree) \\ \sin(\theta \degree) & \cos(\theta\degree) \end{bmatrix}}$$ for $\theta$ degrees counter clockwise


**(b)** Find the standard matrix for the linear transformation $\large{T}$: $\large{\mathbb{R}^4 \rightarrow \mathbb{R}^3}$ where $\large{T}$ is  
defined by the formula  
$$\large{T (x_1, x_2, x_3, x_4) = (7x_1 + 2x_2 − x_3 + x_4, x_2 + x_3, −x_1) }$$ Since the transformation is $\large{\mathbb{R}^4 \rightarrow \mathbb{R}^3}$, the size of the standard matrix must be $\large{3 \times 4}$. 

The standard matrix is
$$\large{\begin{bmatrix} 7 & 2 & -1 & 0 \\ 0 & 1 & 1 & 0 \\ -1 & 0 & 0 & 0\end{bmatrix}}$$

___

**2.** Given the matrices $\large{A}$, $\large{B}$, $\large{C}$, and $\large{D}$ evaluate or write "is not defined":  

$\large{A}$ =  $\large{\begin{bmatrix} 1 & −1  \\ 0 & 3 \\ 2 & 0 \end{bmatrix}}$ ,  $\large{B}$ =  $\large{\begin{bmatrix} 1 & 0 & −1 \\  −2 & 0 & 0  \\ 0 & 1 & 0  \end{bmatrix}}$ ,  $\large{C}$ =  $\large{\begin{bmatrix} 3 & −1  \\ 9 & 3  \end{bmatrix}}$,  $\large{D}$ = $\large{\begin{bmatrix} 2 & 4 \\  1 & 2 \end{bmatrix}}$ 

$\large{v^T}$ =  $\large{\begin{bmatrix} \,2\, \\ 1 \\ 0 \end{bmatrix}}$ ,   $\large{u = \begin{bmatrix} 3 \\ 3 \\ 1 \end{bmatrix}}$  

**a) $\large{2D}$**
$\large{2D = 2\times \begin{bmatrix} 2 & 4 \\ 1 & 2 \end{bmatrix} = \begin{bmatrix} 4 & 8 \\ 2 & 4 \end{bmatrix}}$

**b) $\large{AC}$**
$\large{AC = \begin{bmatrix} 1 & −1  \\ 0 & 3 \\ 2 & 0 \end{bmatrix} \times \begin{bmatrix} 3 & −1  \\ 9 & 3  \end{bmatrix} = \begin{bmatrix} 1 \times 3 + (-1) \times 9 & 1 \times (-1) + (-1) \times 3 \\ 0 \times 3 + 3 \times 9 & 0 \times (-1) + 3 \times 3 \\ 2 \times 3 + 0 \times 9 & 2 \times (-1) + 0 \times (3) \end{bmatrix}}$

$\large{= \begin{bmatrix}-6 & -4 \\ 27 & 9 \\ 6 & -2 \end{bmatrix} }$

**c) $\large{AB}$**

$\large{\begin{bmatrix} 1 & −1  \\ 0 & 3 \\ 2 & 0 \end{bmatrix}}$ is a $\large{3 \times \fbox{2}}$ matrix

$\large{\begin{bmatrix} 1 & 0 & −1 \\  −2 & 0 & 0  \\ 0 & 1 & 0  \end{bmatrix}}$ is a $\large{\fbox{3} \times 3}$ matrix

The inner product is not the same (# of columns of $\large{A \neq}$ # of rows of $\large{B}$ )

Thus, it is not defined.

**d) $\large{C^{−1}}$**

$\large{\begin{bmatrix} 3 & −1  \\ 9 & 3  \end{bmatrix}^{- 1} = \huge{\frac{1}{3 \times 3 - (-1) \times 9}}\large{\begin{bmatrix} 3 & 1 \\ -9 & 3 \end{bmatrix} = \frac{1}{18} \begin{bmatrix} 3 & 1 \\ -9 & 3 \end{bmatrix} = \begin{bmatrix} \frac{1}{6} & \frac{1}{18} \\ -\frac{1}{2} & \frac{1}{6} \end{bmatrix}}}$

**e) $\large{D^{−1}}$**  

$\large{\det(D) = \det \left(\begin{bmatrix} 2 & 4 \\  1 & 2 \end{bmatrix}\right) = 2 \times 2 - 1 \times 4 = 0}$

$\large{D}$ is not invertible since its determinant is zero (by *IMT*)


**f) $\large{B^T}$** 

$\large{\begin{bmatrix} 1 & 0 & −1 \\  −2 & 0 & 0  \\ 0 & 1 & 0  \end{bmatrix}^T = \begin{bmatrix} 1 & -2 & 0 \\  0 & 0 & 1  \\ -1 & 0 & 0  \end{bmatrix}}$

**g) $\large{C + D}$** 

$\large{\begin{bmatrix} 3 & −1  \\ 9 & 3  \end{bmatrix} + \begin{bmatrix} 2 & 4 \\  1 & 2 \end{bmatrix} = \begin{bmatrix} 5 & 3 \\  10 & 5 \end{bmatrix}}$

**h) $\large{(C + D)^{T}}$** 

$\large{\left(\begin{bmatrix} 3 & −1  \\ 9 & 3  \end{bmatrix}+ \begin{bmatrix} 2 & 4 \\  1 & 2 \end{bmatrix}\right)^T = \begin{bmatrix} 5 & 3 \\  10 & 5 \end{bmatrix}^T = \begin{bmatrix} 5 & 10 \\  3 & 5 \end{bmatrix}}$

**i) $\large{(C^{−1})^{T}}$**

$\large{C^{-1} = \begin{bmatrix} \frac{1}{6} & \frac{1}{18} \\ -\frac{1}{2} & \frac{1}{6} \end{bmatrix}}$

$\large{(C^{-1})^{T} = \begin{bmatrix} \frac{1}{6} & \frac{1}{18} \\ -\frac{1}{2} & \frac{1}{6} \end{bmatrix}^T = \begin{bmatrix} \frac{1}{6} & -\frac{1}{2} \\ \frac{1}{18} & \frac{1}{6} \end{bmatrix}}$

**j) $\large{A^{-1}}$**

$\large{A}$ is *NOT* a square matrix, so it cannot be invertible.

Not defined.

**k) $\large{AA^T}$** 

 $\large{\begin{align}AA^T &= \begin{bmatrix} 1 & −1  \\ 0 & 3 \\ 2 & 0 \end{bmatrix} \begin{bmatrix} 1 & 0 & 2 \\ -1 & 3 & 0 \end{bmatrix} = \begin{bmatrix} \;1 \times 1 + (-1) \times (-1) & 1 \times 0 + (-1) \times 3 & 1 \times 2 + (-1) \times 0\; \\ 0 \times 1 + 3 \times -1 & 0 \times 0 + 3 \times 3 & 0 \times 2 + 3 \times 0 \\ 2 \times 1 + 0 \times -1 & 2 \times 0 + 0 \times 3 & 2 \times 2 + 0 \times 0 \end{bmatrix} \\  \\ &= \begin{bmatrix} 2 & −3 & 2  \\ -3 & 9 & 0 \\ 2 & 0 & 4 \end{bmatrix}\end{align}}$
 
 

**l) $\large{A^TA}$**

 $\large{\begin{align}A^TA &=  \begin{bmatrix} 1 & 0 & 2 \\ -1 & 3 & 0 \end{bmatrix} \begin{bmatrix} 1 & −1  \\ 0 & 3 \\ 2 & 0 \end{bmatrix} =  \begin{bmatrix} \;1 \times 1 + 0 \times 0 + 2 \times 2 & 1 \times -1 + 0 \times 3 + 2 \times 0\; \\ (-1) \times 1 + 3 \times 0 + 0 \times 2 & (-1) \times (-1) + 3 \times 3 + 0 \times 0 \end{bmatrix} \\ \\ &= \begin{bmatrix} 2 & −3 & 2  \\ -3 & 9 & 0 \\ 2 & 0 & 4 \end{bmatrix}\end{align}}$
 
**m) $\large{vu}$**

$\large{v^T = \begin{bmatrix} \,2\, \\ 1 \\ 0 \end{bmatrix} \implies v = \begin{bmatrix} \,2 & 1 & 0\, \end{bmatrix}}$ ,   $\large{u = \begin{bmatrix} 3 \\ 3 \\ 1 \end{bmatrix}}$ 

$\large{\begin{align} vu &= \begin{bmatrix} \,2 & 1 & 0\, \end{bmatrix}\begin{bmatrix} 3 \\ 3 \\ 1 \end{bmatrix} = \begin{bmatrix} 2 \times 3 \\ 1 \times 3 \\ 0 \times 1 \end{bmatrix} \\ \\ &= \begin{bmatrix} \,6\, \\ 3 \\ 0 \end{bmatrix}\end{align}}$

**n) $\large{\text{rank}(A)}$**

$\large{A}$ =  $\large{\begin{bmatrix} 1 & −1  \\ 0 & 3 \\ 2 & 0 \end{bmatrix}}$

Reduce to EF 

An EF of $\large{A}$ = $\large{\begin{bmatrix} \fbox{1} & −1  \\ 0 & \fbox{3} \\ 0 & 0 \end{bmatrix}}$

Two pivot columns, so $\large{\fbox{rank(A) = 2}}$

___

3. Given the size of the matrices $\large{A}$, $\large{B}$, $\large{C}$, and $\large{D}$, determine whether the following  
operations are defined, and if defined, determine the size of the resulting matrix.  
$$\large{A\;\;3\times2\;\;\;\;\;B\;\;2\times2\;\;\;\;\;C\;\;2\times3\;\;\;\;\;D\;\;3\times3}$$
**(a) $\large{5A}$**

Defined. $\large{3 \times 2}$

**(b) $\large{B − C}$**

Defined. The two matrices involved are the same size. $\large{2 \times 2}$ 

**(c) $\large{(A − C^T )^T}$** 

Undefined. $\large{A}$ is $\large{3 \times 2}$ and $\large{C^T}$ is $\large{2 \times 2}$. Matrix subtraction requires both matrices to be the same size.

**(d) $\large{C^T A^T + 2D^T }$**

Defined. $\large{C^T}$ is $\large{3 \times 2}$ and $\large{A^T}$ is $\large{2 \times 3}$. These two can be multiplied since their inner products are the same, and yield a $\large{3 \times 3}$ matrix (outer dimensions). $\large{D^T}$ is a $\large{3 \times 3}$, and scalar multiplication does not change this, so $\large{2D^T}$ is also $\large{3 \times 3}$. Matrix of the same dimensions can be added. The result is a $\large{3 \times 3}$.

4. Find the determinant of the following matrices. Show all work. Which of these matrices  
are invertible?  
$$\large{A =  \begin{bmatrix} 1 & −1 & 4  \\ 0 & 1 & 0 \\ 5 & 2 & 3 \end{bmatrix}},\;\;\;\; \large{B =  \begin{bmatrix} 3 & 5 & −6 & 4 \\ 0 & −2 & 3 & −3 \\ 0 & 0 & 1 & 5 \\ 0 & 0 & 0 & 3 \end{bmatrix}}$$

Cofactor expansion along *second row*

$\large{\begin{align}\det(A) &= \det\left( \begin{bmatrix} 1 & −1 & 4  \\ 0 & 1 & 0 \\ 5 & 2 & 3 \end{bmatrix}\right) = 1^{(2 +2)} \times \det\left(\begin{bmatrix} 1 & 4 \\ 5 & 3 \end{bmatrix}\right) = 1 \times (1 \times 3 - 4 \times 5) \\ \\ &= 3 - 20 = -17 \neq 0\end{align}}$ 

Since $\large{\det(A) \neq 0}$, $\large{A}$ is invertible

Since the matrix $\large{B}$ is a triangular matrix, the determinant is the product of the main diagonals

$\iff \large{\det(B) = 3 \times (-2) \times 1 \times 3 = -18}$

5. Determine whether the set of vectors are linearly independent. Give reasons for your  
answer.  
**(a)**  

$\large{ \left\{ \begin{bmatrix} 16 \\ -8 \\ 12 \end{bmatrix}, \begin{bmatrix} -4 \\ 2 \\ -4 \end{bmatrix}\right\}}$ 

$\large{\begin{bmatrix} 16 \\ -8 \\ 12 \end{bmatrix} \neq c \times \begin{bmatrix} -4 \\ 2 \\ -4 \end{bmatrix}}$    $\large{c \in \mathbb{R}^n}$

Linearly independent, since one vector is a scalar multiple of the other

**(b)**  

$\large{\left\{\begin{bmatrix} 2  \\ −5  \\ 1\end{bmatrix}, \begin{bmatrix} -6  \\ 5  \\ 3 \end{bmatrix}, \begin{bmatrix} 0  \\ 0  \\ 0 \end{bmatrix}\right\}}$

Not linearly independent, since one vector is the zero vector
 
**(c)**  

$\large{\left\{ \begin{bmatrix} 5  \\ 5  \\ 1\end{bmatrix},\begin{bmatrix} -1  \\ 0  \\ 1\end{bmatrix}, \begin{bmatrix} 3  \\ 6  \\ 1\end{bmatrix}, \begin{bmatrix} 2  \\ 0  \\ 0 \end{bmatrix}\right\}}$

Not linearly independent, since there are more vectors than entries per vector

**(d)**  

$\large{\left\{\begin{bmatrix} 1  \\ 1  \\ 3 \end{bmatrix}, \begin{bmatrix} -3  \\ 0  \\ 4\end{bmatrix}, \begin{bmatrix} 5  \\ -1  \\ 2\end{bmatrix}\right\}}$

Linearly independent, since the echelon form of the matrix of the column vectors has a pivot in each column


$\large{\begin{bmatrix} 1 & -3 & 5 \\ 1 & 0 & -1 \\  3 & 4 & 2 \end{bmatrix} \xrightarrow {\huge{R_3 \rightarrow R_3 - 3 \times R_1}}\begin{bmatrix} 1 & 0 & -1 \\ 0 & 1 & 1 \\ 0 & 4 & 5 \end{bmatrix} \xrightarrow {\huge{R_3 \rightarrow R_3 + (-4) \times R_2}}\begin{bmatrix} \fbox{1} & 0 & -1 \\ 0 & \fbox{1} & 1 \\ 0 & 0 & \fbox{1} \end{bmatrix}}$


___

6. Given Ax = b is represented by the augmented matrix  


$\large{\begin{bmatrix} -1 & 1 & -3 & -6 & -4 \\-3 & 3 & -8 & -16 & -10 \\2 & -2 & 7 & 14 & 10 \end{bmatrix}}$ ~ $\large{\begin{bmatrix} 1 & -1 & 3 & 6 & 4 \\ 0 & 0 & 1 & 2 & 2 \\ 0 & 0 & 0 & 0 & 0 \end{bmatrix}}$

**(a)** How many solutions does the system of equations have?  
Infinite solutions.

**(b)** Are the columns of A independent? Explain.  
No. There are more columns than entries per vector, so the column vectors of A cannot be linearly independent.

**(c)** Do the columns of A span $\large{\mathbb{R^3}}$?  
No. $\large{A}$ only has $\large{2}$ pivot rows in the first and second row, so it can only span $\large{\mathbb{R^2}}$, not $\large{\mathbb{R}^3}$

**(d)** Is Ax = b consistent for every b? Explain.  
No. If $\large{b}$ is a vector that after row reduction in the augmented matrix has a non-zero entry as its third entry, then the last column of the augmented matrix for $\large{Ax = b}$ would become a pivot column. This means $\large{Ax = b}$ would be inconsistent.

**(e)** If $\large{T}$: $\large{\mathbb{R^n} \rightarrow \mathbb{R}^m}$ is a linear transformation given by $\large{T(x) = Ax}$, what is $\large{n}$?  What is $\large{m}$?  
$\large n$ is the number of columns in the matrix $\large{A}$, or $\large{\fbox{4}}$ (The augmented matrix $\large{[\;A\;|\;b\;]}$ has $\large{5}$ columns, so $\large{A}$ as $\large{5 - 1 = 4}$).
$\large{m}$ is the number of rows in the matrix $\large{A}$, or $\large{\fbox{3}}$

**(f)** Find a basis for the column space of $\large{A}$.  

The pivot positions of $\large{A}$ are:
$\large{\begin{bmatrix} \fbox{-1} & 1 & -3 & -6 \\-3 & 3 & \fbox{-8} & -16 \\2 & -2 & 7 & 14\end{bmatrix}}$ 

So a basis for the column space of $\large{A}$ is 

$\large{\left\{ \begin{bmatrix} -1 \\ -3 \\ 2 \end{bmatrix} \begin{bmatrix} -3 \\ -8 \\ 7\end{bmatrix}\right\}}$

**(g)** What is the rank of A?  
The rank of $\large{A}$ is $\large{\fbox{2}}$ since there are two elements in the basis of the column space of $\large{A}$.

**(h)** What if the nullity of A?  
By the Rank Theorem,
rank($\large{A}$) + nullity($\large{A}$) = # of columns

So 2 + nullity($\large{A}$) = 4

Thus, the nullity of $\large{A}$ is $\large{4 - 2 = \fbox{2}}$

___

7. Determine $\large{A^{-1}}$ if $\large{A = \begin{bmatrix} 1 & 1 & 2 \\ 2 & 3 & -2 \\ 3 & 3 & 7 \end{bmatrix}}$.

By Gaussian-Jordan Method,

$\large{\begin{align}&\begin{bmatrix} 1 & 1 & 2 & | & 1 & 0 & 0\\ 2 & 3 & -2 & | & 0 & 1 & 0 \\ 3 & 3 & 7 & | & 0 & 0 & 1\end{bmatrix} \xrightarrow[\huge{R_3 \rightarrow R_3 + (-3) \times R_1}]{\huge{R_2 \rightarrow R_2 + (-2) \times R_1}} \begin{bmatrix} 1 & 1 & 2 & | & 1 & 0 & 0\\ 0 & 1 & -6 & | & -2 & 1 & 0 \\ 0 & 0 & 1 & | & -3 & 0 & 1\end{bmatrix} \\ \\ & \xrightarrow[\huge{R_2 \rightarrow R_2 + (6) \times R_3}]{\huge{R_1 \rightarrow R_1 + (-2) \times R_3}} \begin{bmatrix} 1 & 1 & 0 & | & 7 & 0 & -2\\ 0 & 1 & 0 & | & -20 & 1 & 6 \\ 0 & 0 & 1 & | & -3 & 0 & 1\end{bmatrix} \xrightarrow{\huge{R_1 \rightarrow R_1 + (-1) \times R_2}} \\ \\ &\begin{bmatrix} 1 & 0 & 0 & | & 27 & -1 & -8\\ 0 & 1 & 0 & | & -20 & 1 & 6 \\ -3 & 0 & 1 & | & -3 & 0 & 1\end{bmatrix}\end{align}}$

Therefore, $\large{A^{-1}} = \begin{bmatrix} 27 & -1 & -8 \\ -20 & 1 & 6 \\ -3 & 0 & 1 \end{bmatrix}$

10. Matrix $\large{A}$ is given below. Your classmate claims $\large{A^{−1}}$ is the matrix $\large{B}$. Is the classmate  
right or wrong? How do you know?  

$\large{A = \begin{bmatrix} 1 & -1 & -2 \\ 2 & -3 & -5 \\ -1 & 3 & 5 \end{bmatrix}}$,    $\large{B = \begin{bmatrix} 0 & 1 & 1 \\ 5 & -3 & -1 \\ -3 & 1 & 0 \end{bmatrix}}$

If $\large{A^{-1} = B}$, then $\large{AA^{-1} = AB = I}$

However, we can see that $$\large{\begin{align}AB &= \begin{bmatrix} 1 & -1 & -2 \\ 2 & -3 & -5 \\ -1 & 3 & 5 \end{bmatrix} \begin{bmatrix} 0 & 1 & 1 \\ 5 & -3 & -1 \\ -3 & 1 & 0 \end{bmatrix} \\ \\  &= \begin{bmatrix} 1 \times 0+(-1)\times5+(-2) \times (-3) & 1 \times 1 + (-1) \times (-3) + (-2) \times 1 & 1 \times 1 + (-1) \times (-1) + (-2) \times 0 \\ 2 \times 0 + (-3) \times 5 + (-5) \times (-3) & 2 \times 1 + (-3) \times (-3) + (-5) \times (1) & 2 \times 1 + (-3) \times (-1) + (-5) \times 0 \\ -1 \times 0 + 3 \times 5 + 5 \times (-3) & -1 \times 0 + 3 \times 5 + 5 \times (-3) & (-1) \times 1 + 3 \times (-1) + 5 \times 0 \end{bmatrix} \\ \\ & = \begin{bmatrix} 1 & 2 & 2 \\ 0 & -6 & 5 \\ 0 & 0 & -4 \end{bmatrix} \neq \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix}\end{align}}$$
Therefore, $\large{B}$ cannot be the inverse of $\large{A}$

___

9. Given that $\large{A}$, $\large{B}$, and $\large{C}$ are all invertible $\large{n \times n}$ matrices, find the inverse of $\large{ABC}$ and  
show that what you think is the inverse, really is the inverse.  

$$\large{(ABC)^{-1} = ((AB)C)^{-1} = C^{-1}(AB)^{-1} = C^{-1}B^{-1}A^{-1}}$$
If $\large{C^{-1} B^{-1} A^{-1}}$ is the inverse of $\large{ABC}$, then $\large{ABC \times C^{-1} B^{-1} A^{-1} = I}$

$$\large{\begin{align}&ABC \times C^{-1} B^{-1} A^{-1} = AB(CC^{-1})B^{-1}A^{-1} = AB (I)B^{-1} A^{-1} = ABB^{-1}A^{-1} \\ &= A(BB^{-1})A^{-1} = A(I)A^{-1} = AA^{-1} = I\end{align}}$$

Therefore, $\large{C^{-1} B^{-1} A^{-1}}$ is the inverse of $\large{ABC}$

___

10. True or False: For all n×n matrices A, B, and C (no explanation required):  
**(a)** $\large{A + B = B + A }$
True

**(b)** $\large{(A + B)^T = A^T + B^T}$
False

**(c)** $\large{(AB)^T = A^T B^T}$
False

**(d)** $\large{(A^T)^T = A}$
True

**(e)** $\large{\det(A + B) = \det(A) + \det(B) }$
False

**(f)** $\large{\det(AB) = \det(A) \det(B)}$
True

**(g)** If A is invertible, then $\large{\det(AA^{−1}) = 1}$
True

**(h)** If AB = AC then B = C.  
False

**(i)** If B = C then AB = AC.  
True

___

11. True or False: (no explanation required):  
**(a)** Every linear transformation rotates a vector.  
False

**(b)** Not every linear transformation from $\large{\mathbb{R}^{n}}$ to $\large{\mathbb{R}^{m}}$ is a matrix transformation.  
False

**(c)** If an $\large{n\times n}$ matrix $\large{A}$ can be row reduced to the identity matrix, then $\large{A}$ must be  
invertible.  
True

**(d)** If the columns of an $\large{n\times n}$ matrix A are linearly dependent, then A is invertible.  
False

**(e)** If $\large{A}$ and $\large{B}$ are both $\large{n\times n}$ invertible matrices then $\large{(AB)^{−1} = A^{−1}B^{−1}}$.  
False

**(f)** If A is $\large{n \times n}$ and $\large{Ax = 0}$ has only the trivial solution, then the dimension of the  
Nul(A) is 1.  
False

**(g)** If A is a $\large{3 \times 4}$ matrix, then the column vectors belong to $\large{\mathbb{R}^3}$.  
True

**(h)** If A is a $\large{3 \times 4}$ matrix that has $\large{3}$ pivot columns, then the linear transformation  
$\large{T}$: $\large{x \rightarrow Ax}$ is onto.  
True

**(i)** All sets of vectors in $\large{\mathbb{R}^2}$ have a basis. 
False

**(j)** If $\large{S}$ is a set of 2 vectors, each of which is in $\large{\mathbb{R}^3}$, then $\large{S}$ is linearly independent.  
False

**(k)** If $\large{S}$ is a set of 4 vectors, each of which is in $\large{\mathbb{R}^3}$, then $\large{S}$ is linearly dependent.  
True

**(l)** If $\large{S}$ is a set of 4 vectors, each of which is in $\large{\mathbb{R}^3}$, then  $\large{S}$ spans $\large{\mathbb{R}^3}$.  
False

**(m)** If $\large{S}$ is a set of 2 vectors, each of which is in $\large{\mathbb{R}^3}$, then $\large{S}$ does not span $\large{\mathbb{R}^3}$.
True

#### Tags

>[!quote] Tags:
> [[Linear Algebra Information|Linear Algebra Information]]

