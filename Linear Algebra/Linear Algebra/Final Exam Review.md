## Pages

Notes and technology will not be allowed on the exam. Bring a photo ID. Actual exam  
will be shorter than this review. Solutions are given on the last page.  
Warning: The questions given here are only sample questions. There will be questions  
on the exam that do not resemble any of these questions. You are responsible for knowing  
all the material covered in this class, including all homework problems, practice questions  
for Test 1 and 2, questions from Test 1 and 2, and Pearson problems.  

Topics:  
1. Row reduction and solving a system of equations  
(a) inconsistent  
(b) one solution  
(c) infinitely many solutions  
2. Matrix Operations  
(a) addition  
(b) multiplication  
(c) inverse  
(d) transpose  
(e) determinant  
3. Invertible Matrix Theorem - characteristics of invertible matrices  
4. Linear Transformations  
5. Subspaces of IR n  
(a) dimension  
(b) rank  
(c) basis  
6. Eigenvalues and Eigenvectors  
(a) find eigenvalues  
(b) find eigenvectors  
(c) characteristic equation.  
7. Characterizing Sets of Vectors  
(a) linear independence  
(b) span  
(c) orthogonal  
(d) orthonormal  
8. Orthogonal Projection and Least Squares  

___
# Sample Questions  
1. The following augmented matrices represent the system of equations Ax = b. Solve the  
following systems of equations for x where the systems of equations have the following  
augmented matrices. Write the solution in parametric vector form where applicable.  
Check your answers.  
(a) $\large{\begin{bmatrix} 1 & 1 & 1 & | & 2 \\ 0 & 1 & 1 & | & 2 \\ 2 & 1 & 1 & | & 2 \end{bmatrix}}$ (b)  $\large{\begin{bmatrix}1 & 1 & 2 & 3 & | & 2 \\ 2 & 1 & 1 & 0 & | & 1 \\ 1 & 2 & 1 & 3 & | & 7 \end{bmatrix}}$ (c)  $\large{ \begin{bmatrix} 3 & 6 & 1 & 1 & | & 6  \\ 1 & 2 & 2 & 3 & | & 3 \\ 4 & 8 & 3 & 2 & | & 3 \end{bmatrix}}$

2. Given the matrices $\large{A}$, $\large{B}$ and $\large{C}$ and the matrix v and u, evaluate or write not defined.  

$\large{{\bf A} =  \begin{bmatrix} 1 & 2 & 3 \\0 & 1 & 5 \end{bmatrix}}$  $\large{{\bf B} =  \begin{bmatrix} 0 & 0 & 1 \\ 0 & 1 & 0  \\ 1 & 0 & 1 \end{bmatrix}}$ $\large{{\bf C} =  \begin{bmatrix} 0 & 1 & 2 \\ 1 & 0 & 1\end{bmatrix}}$  $\large{v^T =  \begin{bmatrix} 2 \\ 1 \\ 0 \end{bmatrix}}$ $\large{u =  \begin{bmatrix} 3 \\ 3 \\ 1 \end{bmatrix}}$
**(a)** $\large{3{\bf A}}$ + $\large{\bf AB}$
 $\large{\begin{align} &=3\begin{bmatrix} 1 & 2 & 3 \\0 & 1 & 5 \end{bmatrix} + \begin{bmatrix} 1 & 2 & 3 \\0 & 1 & 5 \end{bmatrix} \times \begin{bmatrix} 0 & 0 & 1 \\ 0 & 1 & 0  \\ 1 & 0 & 1 \end{bmatrix} \\ \\ &= \begin{bmatrix} 1 & 2 & 3 \\0 & 1 & 5 \end{bmatrix} + \begin{bmatrix} 0 + 0 + 3 & 0 + 2 + 0 & 1 + 0 + 3 \\ 0 + 0 + 5 & 0 + 1 + 0 & 0 + 0 + 5 \end{bmatrix} = \begin{bmatrix} 3 & 2 & 4 \\ 5 & 1 & 5 \end{bmatrix} \end{align}}$

**(b)** $\large{{\bf B}u}$  
$\large{\begin{bmatrix} 0 & 0 & 1 \\ 0 & 1 & 0  \\ 1 & 0 & 1 \end{bmatrix} \times \begin{bmatrix} 3 \\ 3 \\ 1 \end{bmatrix}}$

**(c)** $\large{{\bf A}v}$
$\large{v = (v^T)^T = \begin{bmatrix} \,2 \\ 1 \\ 0\, \end{bmatrix}^T = \begin{bmatrix} 2 & 1 & 0 \end{bmatrix}}$
$\large{\underbrace{\begin{bmatrix} 1 & 2 & 3 \\0 & 1 & 5 \end{bmatrix} \times \begin{bmatrix} 2 & 1 & 0 \end{bmatrix}}_{2 \times 3\;\;\;1 \times 3}}$

inner dimensions do not match, $\large{3 \neq 1}$

**(d)** $\large{{\bf A}v^T}$
$\large{\begin{bmatrix} 1 & 2 & 3 \\0 & 1 & 5 \end{bmatrix} \times \begin{bmatrix} 2 \\ 1 \\ 0 \end{bmatrix} = \begin{bmatrix} 2 + 2 + 0 \\ 0 + 1 + 0\end{bmatrix} = \begin{bmatrix} 4 \\ 0 \end{bmatrix}}$

**(e)** $\large{{\bf C}^T{\bf C}}$
$\large{{\bf C}^T = \begin{bmatrix} 0 & 1 & -2 \\ 1 & 0 & -1\end{bmatrix}^T = \begin{bmatrix} 0 & 1 \\ 1 & 0 \\ -2 & -1 \end{bmatrix}}$

$\large{\begin{align} &{\bf C}^T{\bf C} = \begin{bmatrix} 0 & 1 \\ 1 & 0 \\ -2 & -1 \end{bmatrix} \times \begin{bmatrix} 0 & 1 & -2 \\ 1 & 0 & -1\end{bmatrix} = \begin{bmatrix} 0 + 1 & 0 + 0 & 0 - 1 \\ 0 + 0 & 1 + 0 & -2 + 0 \\ 0 - 1 & -2 + 0 & 4 + 1 \end{bmatrix} \\ \\ &= \begin{bmatrix} 1 & 0 & -1 \\ 0 & 1 & -2 \\ -1 & -2 & 5 \end{bmatrix} \end{align}}$

**(f)** $\large{\det(C^TC)}$. (hint: use part e)  

$\large{\begin{align} &\det(C^TC) = \underbrace{\det\left(\begin{bmatrix} 1 & 0 & -1 \\ 0 & 1 & -2 \\ -1 & -2 & 5 \end{bmatrix}\right)}_{\text{from part e}} = \underbrace{1 \times (-1)^{1+1} \times \begin{vmatrix} 1 & -2 \\ -2 & 5 \end{vmatrix} + -1 \times (-1)^{3+1} \times \begin{bmatrix} 0 & 1 \\ -1 & -2\end{bmatrix}}_{\text{cofactor expansion about first row}} \\ \\&= 1 \times (1 \times 5 - (-2) \times (-2)) + (-1) \times (0 \times -2 - 1 \times (-1)) \\ \\ &= 1 \times (5 - 4) + (-1) \times (0 + 1) = 1 \times (-1) + (-1) \times 1  = -2\end{align}}$

**(g)** $\large{(C^T C)^{-1}}$. (hint: use part f)  

$\large{(C^T C)^{-1} = \begin{bmatrix} 1 & 0 & -1 \\ 0 & 1 & -2 \\ -1 & -2 & 5 \end{bmatrix} ^{-1} = }$

By Gaussian-Jordan Method

**(h)** $\large{\text{rank}(B)}$
$\large{\text{rank}(B) = 3}$

**(i)** $\large{\text{rank}(A)}$
$\large{\text{rank}(A) = 2}$

**(j)** $\large{B^{-1}}$  

$\large{\begin{bmatrix} 0 & 0 & 1 \\ 0 & 1 & 0  \\ 1 & 0 & 1 \end{bmatrix}^{-1}}$

3. Find the determinant of the following matrices. Show all work. Which of these matrices  
are invertible?  

$\large{A = }$ $\large{\begin{bmatrix} 1 & 1 & 4 \\ 0 & 1 & 0  \\ 5 & 2 & 3 \end{bmatrix}}$  
$\large{B = \begin{bmatrix} 3 & 5 & 6 & 4  \\ 0 & 2 & 3 & 3 \\ 0 & 0 & 1 & 5 \\ 0 & 0 & 0 & 3 \end{bmatrix}}$

4. Let $\large{A}$ and $\large{B}$ be $\large{4 \rightarrow 4}$ matrices, with $\large{\det(A) = 3}$ and $\large{\det(B) = 1}$. Compute:  
**(a)** $\large{\det(AB) = \det(A) \times \det(B) = 3 \times 1 = 3}$  
**(b)** $\large{\det(B^5) = 1^5 = 1}$  
**(c)** $\large{\det(2A) = 2^4 \times 3 = 48}$ 
**(d)** $\large{\det(A^TBA)}$  
**(e)** $\large{\det(B^{-1}AB)}$  
5. For each of the following systems of linear equations, determine all value(s) of $\large{k}$ for  
which the system is consistent.  
**(a)** $\large{6x_1 5x_2 = 4}$
$\large{9x_1 + kx_2 = 1}$ 
(b) 6x 1 8x 2 = k  
9x 1 + 12x 2 = 1  
6. Let T : IR 3 ! IR 3 be a linear transformation such that T (e 1 ) = [0, 2, 1] T , T (e 2 ) =  
[1, 0, 3] T , and T (e 3 ) = [3, 1, 0] T , where {e 1 , e 2 , e 3 } is the standard basis for IR3 .  
What is T ([1, 2, 1] T )?  
7. Find the inverse of the following 3 ⇥ 3 matrix. Check your answer.  
8. Consider the following matrices  
A =  
2  
4  
2 3 1 0 1  
0 1 2 3 0  
0 0 1 2 4  
3  
5 B =  
2  
4  
2 3 1  
0 1 2  
0 0 1  
3  
5 C =  
2  
4  
2 3 1 0  
0 1 2 3  
0 0 0 0  
3  
5 .  
For each matrix, determine  
(a) The rank.  
(b) The number of free variables in the solution to the homogeneous system of equa-  
tions.  
(c) A basis for the column space.  
(d) A basis for the null space for matrices A and B.  
(e) Dimension of the column space.  
3

(f) Nullity.  
(g) Does your basis for the column space of B span IR 3 ? Explain.  
(h) For each matrix, will there be a vector b in IR 3 for which there is no solution to  
Ax = b (and correspondingly for the other two matrices)?  
9. Suppose an 82 ⇥ 53 matrix A has rank 50.  
(a) What is the dimension of Col(A)?  
(b) What is the nullity of A?  
(c) How many solutions does the system of equations Ax = 0 have?  
(d) Does Ax = b has a solution for every b in R 82 ? Why or why not?  
10. Find the eigenvalues and associated eigenvector bases for each eigenvalue of the fol-  
lowing matrices.  
(a)  
A =  
 2 1  
0 3  
  
(b)  
A 2 =  
 1 2  
2 1  
  
(c)  
A 3 =  
 2 0  
2 2  
  
11. Consider the matrices  
A =  
2  
4  
1 0 5  
0 3 2  
2 0 2  
3  
5 B =  
2  
4  
1 4 2  
0 1 0  
0 0 1  
3  
5  
(a) For each matrix, determine the eigenvalues and their algebraic multiplicity.  
(b) For each matrix, pick one eigenvalue and find a basis for the corresponding  
eigenspace.  
(c) Which of the above matrices are invertible? Why?  
12. Consider the set of vectors {v 1 , v 2 , v 3 } where  
v 1 =  
2  
4  
2  
2  
1  
3  
5 , v 2 =  
2  
4  
2  
1  
2  
3  
5 , v 3 =  
2  
4  
1  
2  
2  
3  
5 .  
4

(a) Show that the set is orthogonal.  
(b) Construct an orthonormal basis for IR3 from these vectors.  
13. Let v 1 =  
2  
4  
4  
0  
3  
3  
5, v 2 =  
2  
4  
0  
1  
0  
3  
5, w =  
2  
4  
1  
2  
3  
3  
5.  
(a) Show that the set {v 1 , v 2 } is orthogonal.  
(b) Find the point bw = (w 1 , w 2 , w 3 ) that is closest to the point w = (1, 2, 3) and in  
the subspace W = Span{v 1 , v 2 }.  
(c) Find the distance between w = (1, 2, 3) and the closest point in the subspace W .  
14. Mark T for True or F for False: (Do not assume the matrices are square unless stated  
so in the statement.)  
(a) If A and B are both n⇥n, then det(A + B) = det(A) + det(B)  
(b) If A and B are both n⇥n invertible matrices, then (AB) 1 = B 1 A 1 .  
(c) Elementary row operations do not change the determinant.  
(d) If A is n⇥n and Ax = 0 has only the trivial solution, then the nullity of A is 1.  
(e) If A is 3⇥4 then the column vectors belong to IR 3 .  
(f) If S is a set of 2 vectors, each of which is in IR3 , then S is linearly independent.  
(g) If S is a set of 4 vectors, each of which is in IR3 , then S is linearly dependent.  
(h) If S is a set of 4 vectors, each of which is in IR3 then S spans IR 3 .  
(i) If S is a set of 2 vectors, each of which is in IR3 , then S does not span IR3 .  
(j) The projection of u onto W = Span{v 1 , v 2 , ...v n } gives the shortest distance  
between u and W .  
5

#### Tags

>[!quote] Tags:
> [[Linear Algebra Information|Linear Algebra Information]]

