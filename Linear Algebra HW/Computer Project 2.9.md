### Charles Liu

Recall that MatLab can be accessed online by googling: Matlab online. Examples of how to input matrices and how to get a matrix into reduced row echelon form (MATLAB does not have a command for echelon form - why not?) within MATLAB is given in a file on Canvas called Matlab for MATH 220 Students.

We know that a system of linear equations has zero, one, or infinitely many solutions. But there are different sizes of infinity - the dimension of the null space gives us an idea of how many solutions there are. The dimension of the column space gives us an idea of how big the range is (i.e. how many b’s we can get to by taking a linear combination of the columns).

___

**1. (20 pts)** Recall Newton’s law of Cooling problem from written HW 1.2. We have 2 unknowns ($K$ and $q_r$), and 9 data points. The equation is:

$$q = −K∆T + qr.  $$
Let us suppose that the data points $(∆T,q)$ are given by:

$$\large{(3, 1.5)\;(3, 1.8)\;(3, 1.9)\;(7, 5.8)\;(7, 6.3)\;(7, 6.5)\;(14, 13.1) \;14.13.2)\;(14, 13.5)}.$$ 
Consider the first point, $∆T = 3$, $q = 1.5$. This gives us

$$−K(3)+q_r =1.5 $$ 
Repeating this process with all of our measured points, our augmented matrix is:

$$\large{\begin{bmatrix} -3 & 1
&\bigm | & 1.5 \\ -3 & 1 & \bigm | & 1.8 \\ -3 & 1 & \bigm | & 1.9 \\ -7 & 1 & \bigm | & 5.8 \\ -7 & 1 & \bigm | & 6.3 \\ -7 & 1 & \bigm | & 6.5 \\ -14 & 1 & \bigm | & 13.1 \\ -14 & 1 & \bigm | & 13.2 \\ -14 & 1 & \bigm | & 13.5 \end{bmatrix}}$$

Let $\large{A}$ be the *coefficient matrix*. Use Matlab to find the reduced echelon form of $\large{A}$. This matrix is put into a companion WORD document so that you can copy and paste it into Matlab. To find the reduced echelon form in Matlab of a matrix $\large{A}$, type `rref(A)`.

____________________________________________________________________________

**(a)** Find a basis for the Nul($\large{A}$) and Col($\large{A}$).

>Nul($\large{A}$) is the $\large{\color{cyan}\text{set of all solutions to Ax = 0}}$.

Since the reduced echelon form of the augmented matrix of $\large{Ax = 0}$ is:
$$\large{\begin{bmatrix} 1 & 0 & \bigm | & 0\\ 0 & 1 & \bigm | & 0\\ 0 & 0 & \bigm | & 0\\ 0 & 0 & \bigm | & 0\\ 0 & 0 & \bigm | & 0\\ 0 & 0 & \bigm | & 0 \\ 0 & 0 & \bigm | & 0\\ 0 & 0 & \bigm | & 0\\ 0 & 0 & \bigm | & 0\end{bmatrix}}$$
We can see that
> $\large{x_1} = 0$
> $\large{x_2} = 0$
and there are NO free variables.

This means the only solution to $\large{Ax = 0}$ is 
$$\large{x = \begin{bmatrix} x_1 \\ x_2\end{bmatrix} = \begin{bmatrix} \;0\; \\ 0\end{bmatrix}}$$
and thus the $\large{\color{cyan}\text{basis of Nul(\large{A})}}$ is the empty set

$$\Huge{\begin{Bmatrix}& \end{Bmatrix}}$$

>Col($\large{A}$) is the $\color{cyan}\large{\text{set of all vectors spanned by the column vectors of A}}$.
>$\Rightarrow$ A possible basis of Col($\large{A}$) is the set containing the pivot columns of $\large{A}$

$$\large{\begin{bmatrix} \fbox{1} & 0\\ 0 & \fbox{1} \\ 0 & 0 \\ 0 & 0 \\ 0 & 0 \\ 0 & 0 \\ 0 & 0 \\ 0 & 0 \\ 0 & 0 \end{bmatrix}}$$

Since each column is a pivot column, the $\large{\color{cyan}\text{basis for Col(\large{A}}})$ is

$$\large{\begin{Bmatrix}\begin{bmatrix} -3 \\ -3 \\ -3 \\ -7 \\ -7 \\ -7 \\ -14 \\ -14 \\ -14\end{bmatrix},\begin{bmatrix} 1 \\ 1 \\ 1 \\ 1 \\ 1 \\ 1 \\ 1 \\ 1  \\ 1 \end{bmatrix}\end{Bmatrix}}$$

___

**(b) (5 pts)** Determine the dimension of Nul($\large{A}$) and the dimension of the Col($\large{A}$).
>Since there are 0 elements in Nul($\large{A}$), the $\large{\color{cyan}\text{dimension of Nul(\large{A}) is }\fbox{0}}$.
>Since there are 2 elements in Col($\large{A}$), the $\large{\color{cyan}\text{dimension of Col(\large{A}) is }\fbox{2}}$.

___

**(c) (5 pts)** How many solutions are there to Ax = 0? Explain.
> There is only $\large{\text{\color{cyan}one solution}}$, since the only the trivial solution $\large{x = 0}$ satisfies the equation.

___

**(d)  (5 pts)** How many possible solutions are there to Ax = b, where b is the right-hand side represented by the augmented matrix? Explain.

There are $\large{\text{\color{cyan}NO solutions}}$ to Ax = b.
The reduced echelon form of the augmented matrix \[A | b] is below
$$\large{\begin{bmatrix} \fbox{1} & 0 & \bigm | & 0 \\ 0 & \fbox{1} & \bigm | & 0 \\ 0 & 0 & \bigm | & \fbox{1} \\ 0 & 0 & \bigm | & 0 \\ 0 & 0 & \bigm | & 0 \\ 0 & 0 & \bigm | & 0 \\ 0 & 0 & \bigm | & 0 \\ 0 & 0 & \bigm | & 0 \\ 0 & 0 & \bigm | & 0 \end{bmatrix}}$$

As we can clearly see, the third (right-most) column of $\large{A}$ is a pivot column, and thus the matrix must be inconsistent. Therefore, it has no solutions.

___

**(e)  (5 pts)** Will collecting more data points increase the number of solutions? Explain.

$\color{cyan}\large{\text{No}}$. Collecting more data points cannot change the fact that the right-most column is a pivot column, it only appends more rows to our existing augmented matrix. Since the right-most column is still a pivot column, the system is still inconsistent.

___

**2. (32 pts)** Recall the CT scan problem from HW 1.2 (see the first figure given on the last page). Recall that there are 44 unknowns (one for each pixel), which we label as $\large{x_1,\; x_2,\; x_3,\;...,\; x_{44}}$ (see the second figure given given on the last page).

___

**(a) (12 pts)** First consider inputting rays vertically and horizontally.

   **i. (6 pts)** Write down the first two equations corresponding to an x-ray passing through the first 2 rows of our object, and the last two equations corresponding to an x-ray passing through the last two columns of our object.
   $$\text{1. (First Row)}\;\;\;\large{x_1 + x_2 + x_3 + x_4 + x_5 + x_6 + x_7 + x_8 + x_9 + x_{10} + x_{11} = 9}$$$$\text{2. (Second Row)}\;\;\; \large{x_{12} + x_{13} + x_{14} + x_{15} + x_{16} + x_{17} + x_{18} + x_{19} + x_{20} + x_{21} + x_{22} = 9}$$$$\text{3. (Second To Last Column)}\;\;\; \large{x_{10} + x_{21} + x_{32} + x_{43} = 3}$$$$\text{4. (Last Column)}\;\;\; \large{x_{11} + x_{22} + x_{33} + x_{44} = 3}$$
   
   **ii. (4 pts)** The augmented matrix for this problem is given by matrix B = \[A | b] in the companion WORD document. What is the dimension of the column space of the coefficient matrix A? What is the dimension of the null space of A?  (Hint: In Matlab, after copying augmented matrix B, we can obtain the coefficient matrix by typing A = B(:, 1 : end−1). To find the rank of a matrix A, type rank(A).
   From MatLab, after inputting matrix $\large{B}$, finding the coefficient matrix $\large{A}$, we see that
   $$\large{\text{rank(A) = \color{cyan}dim(Col(A)) = }\color{cyan}\fbox{14}}$$
   by the Rank Theorem, we know that 
   $$\large{\text{dim(Nul(A)) + dim(Col(A)) = \# of columns}}$$
   $$\large{\Rightarrow \text {dim(Nul(A)) + 14 = 44}}$$
   
   This means $\large{\color{cyan}\text{dim(Nul({A})) = 44 - 14 = }\fbox{30}}$

   **iii. (2 pts)** Explain why we want the dimension of the null space of A to be zero.
   If the dimension of the null space of A were zero, then by the Rank Theorem, the dimension of Col(A) has to be equal to the amount of columns, which means every column in the matrix A is a pivot column. This means that Ax = b has a unique solution if B = \[A | b] doesn't have a pivot in the right-most column, and we can find the 44 variables $\large{x_1}$ to $\large{x_{44}}$


**(b) (20pts)** adding diagonal measurements (for example there can be a measurement going diagonally through the upper left pixel).

   **i. (6 pts)** Write down the equations for an x-ray going directly southwest (down and to the left) from the $\large{x_2}$ pixel, and another equation for going directly southeast (down and to the right) from the $\large{x_2}$ pixels.
   $$\text{1. (Southwest)}\;\;\; \large{x_{2} + x_{11} = 2}$$$$\text{2. (Southeast)}\;\;\; \large{x_{2} + x_{14} + x_{26} + x_{38} = 4}$$

   **ii. (4 pts)** How many total unique diagonal measurements can we make? Explain (if you like, use the 2nd figure below and sketch the diagonal measurements only).
   
   >The four corners can only go one direction (inwards)
   >The sides excluding the corners can each go two directions diagonally (opposite from the side they are facing)
  > All of the middle pixels can go any of the four directions diagonally
   
   Therefore, since there are $\large{4}$ corners, $\large{2 + 2 + 16 + 16 = 36}$ side pixels, and $\large{2 * 8 = 16}$ middle pixels,
   
   We have a total of:
   
   $\large{4 * 1 + 36 * 2 + 16 * 4 = 4 + 72 + 64 = 140}$ measurements
 
   **iii. (2 pts)** How many total measurements do we have (counting horizontal, vertical, and diagonal)?
   
   >There are $\large{11 + 4 = 15}$ measurements for horizontal / vertical
   >There are $\large{140}$ diagonal measurements (solved previously)
   >
   Total: $\large{140 + 15 = 155}$ measurements
   
**iv. (4 pts)** Consider the coefficient matrix corresponding to the system of equations including the horizontal, vertical, and diagonal measurements. What would you expect the rank of the matrix to be? Explain.
>I expect the rank of the matrix to be 44 since there are 44 unknowns and so many equations, it is very likely that each unknown is determined, yielding a unique solution, and thus each column is a pivot column. Since there are 44 columns, I expect the rank to be 44.

**v. (4 pts)** What is the rank and nullity of the coefficient matrix C corresponding to the system of equations including the horizontal, vertical, and diagonal measurements? What is your conclusion about using catscan measurements to determine where there is skin versus bone? 
Hint: The corresponding augment matrix is given by matrix D in the companion WORD document. You can copy D into Matlab. To get the coefficient matrix, type C=D(:,1:end−1). To find the rank of C, type rank(C).


![[Screen Shot 2023-10-24 at 8.54.30 PM 2.png]]
