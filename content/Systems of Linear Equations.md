---
Created: 2025-10-23
Type: Zettel
aliases:
References:
Links:
  - "[[Matrices]]"
tags:
  - MATH31AH
---
- Suppose we have equations:
	- $2x+y+3z=1$
	- $x-y=1$
	- $2x-z = 1$
- When you have a system where every equation is equal to zero on the right, it is called a *homogeneous system*
	- When you have non-zero values of constants on the side, it is called an *inhomogeneous system*
	- If you inhomogeneous system has a solution, it has as many solutions as its corresponding homogenous system
		- This relates to [[Null Spaces]], since every solution of the kernel will be equal to zero
	- $\lambda(w_{1},w_{2},w_{3}) + (v_{1},v_{2},v_{3})$ where $\lambda$ is a real numbers, and w is the homogenous solutions solves the inhomogeneous
- We can represent the problem as $\begin{bmatrix}\end{bmatrix}$
> Example: Solving a system of linear equations
> $2x+y+3z=1$
> $x-y=1$
> $2x-z = 1$
> We can write this as a matrix as $\begin{bmatrix}2 & 1 & 3 \\ 1 & -1 & 0 \\  2 & 0 & 1\end{bmatrix}\begin{bmatrix}x \\ y \\ z\end{bmatrix} = \begin{bmatrix}1 \\ 1 \\ 1\end{bmatrix}$. Eventually, we want to get to $\begin{bmatrix}1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1\end{bmatrix}\begin{bmatrix}x \\ y \\ z\end{bmatrix} = \begin{bmatrix}- \\ - \\ -\end{bmatrix}$.
> Alternatively, we can write this as an augmented matrix: $\begin{bmatrix}2 & 1 & 3 & | & 1 \\ 1 & -1 & 0 & | & 1 \\ 2 & 0 & 1 & | & 1\end{bmatrix}$
> We want to perform row operations on this to get to our desired state. We can interchange rows, multiply rows by non-zero scalars, and subtract and add rows from others. We can show that these operations are also [[Linear transformations|linear isomorphisms]].
> We can set row 2 to row 1 plus row 2, and row one as row 1 minus row 3.
> $\begin{bmatrix}0 & 1 & 2 & 0 \\ 3 & 0 & 3 & 2 \\ 2 & 0 & 1 & 1\end{bmatrix}$
> We can set row 2 as row 2 minus 3/2 times row 3
> $\begin{bmatrix}0 & 1 & 2 & 0 \\ 0 & 0 & \frac{3}{2}  & \frac{1}{2}  \\ 2 & 0 & 1 & 1\end{bmatrix}$
> We can write row 3 as row 3 minus 2/3 row 2
> $\begin{bmatrix}0  & 1 & 2 & 0 \\ 0 & 0 & \frac{3}{2}  & \frac{1}{2} \\ 2 & 0 & 0 & \frac{2}{3}\end{bmatrix}$
> We can write row 1 and row 1 minus 4/3 times row 2
> $\begin{bmatrix}0 & 1 & 0 & -\frac{2}{3} \\ 0 & 0 & \frac{3}{2}  &  \frac{1}{2} \\ 2 & 0 & 0 & \frac{2}{3}\end{bmatrix}$
> Finally, we can scale to get 1s
> $\begin{bmatrix}0 & 1 & 0 & -\frac{2}{3} \\ 0 & 0 & 1 & \frac{1}{3} \\ 1 & 0 & 0 & \frac{1}{3}\end{bmatrix}$
> Interchange the rows to get 
> $\begin{bmatrix}1 & 0 & 0 & \frac{1}{3} \\ 0 & 1 & 0 & -\frac{2}{3} \\ 0 & 0 & 1 & \frac{1}{3}\end{bmatrix}$
> And we get our solution here.

>Example: Unsolvable system 
>$x_{1}+x_{2} = a_{1}$
>$x_{2}+x_{3} = a_{2}$
>$x_{3}+x_{4}=a_{3}$
>$x_{4}+x_{1}=a_{4}$
>We can write this as $\begin{bmatrix}1 & 1 & 0 & 0 & a_{1} \\ 0 & 1 & 1 & 0 & a_{2} \\ 0 & 0 & 1 & 1 & a_{3} \\ 1 & 0 & 0 & 1 & a_{4}\end{bmatrix}$. 
>r'1 = r1 - r2
>r'2 = r2 - r3
>$\begin{bmatrix}1 & 0 & -1 & 0 & a_{1}-a_{2} \\ 0 & 1 & 0 & -1 & a_{2}-a_{3} \\ 0 & 0 & 1 & 1 & a_{3} \\ 1 & 0 & 0 & 1 & a_{4}\end{bmatrix}$
>r'1 = r1 - r3 
>r'4 = r4 -r1 
>$\begin{bmatrix}1 & 0 & 0 & 1 & a_{1}-a_{2}+a_{3} \\ 0 & 1 & 0 & -1 & a_{2}-a_{3} \\ 0 & 0 & 1 & 1 & a_{3} \\ 0 & 0 & 0 & 0 & a_{4}-a_{1}+a_{2}-a_{3}\end{bmatrix}$
>Since the last row has all zeros, we know that this system is not solvable, unless $a_{4}-a_{1}+a_{2}-a_{3}=0$, in which it might be. 

> Example: Row reduction as a matrix multiplication.
> Suppose we have a matrix $\begin{bmatrix}2 & 0 & 2  \\ 5 & 1 & 0\end{bmatrix}$. 
> Let r'2 = r2 - 5/2 r1. Our matrix becomes $\begin{bmatrix}2 & 0 & 2 \\ 0 & 1 & -5\end{bmatrix}$. Doing this row operations is the same as left multiplication by this matrix: $\begin{bmatrix}1 & 0 \\ -\frac{5}{2} & 1\end{bmatrix}$
> We can see this as $\begin{bmatrix}1 & 0 \\ -\frac{5}{2} & 1\end{bmatrix} \begin{bmatrix}2 & 0 & 2 \\ 5 & 1 & 0\end{bmatrix} = \begin{bmatrix}2 & 0 & 2 \\ -\frac{5}{2}*2 + 5  & 0+1 & -5 + 0\end{bmatrix} = \begin{bmatrix}2 & 0 & 2 \\ 0 & 1 & -5\end{bmatrix}$.

> Example: Computing an [[Matrix inverses|inverse of a matrix ]]
> $\begin{bmatrix}2 & 3 & 5 \\ 0 & 4 & 1 \\ 0  & 0 & 7\end{bmatrix} \to \begin{bmatrix}2 & 3 & 5 & | & 1 & 0 & 0 \\ 0 & 4 & 1 & | & 0 & 1 & 0 \\ 0 & 0 & 7 & | & 0 & 0 & 1\end{bmatrix}$. 
> We want to do row operations such that we get an identity matrix on our left, so we get out inverse on the right.
> $\begin{bmatrix}2 & 3 & 0 & | & 1 & 0 & -1 \\ 0 & 4 & 0 & | & 0 & 1 & -1 \\ 0 & 0 & 1 & | & 0 & 0 & 1\end{bmatrix}$
> $\begin{bmatrix}1 & 0 & 0 & | & \frac{1}{2} & -\frac{3}{8} & -\frac{1}{8} \\ 0 & 1 & 0 & | & 0 & \frac{1}{4} & -\frac{1}{4}  \\ 0 & 0 & 1 & | & 0 & 0 & 1\end{bmatrix}$
> 