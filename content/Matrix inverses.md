---
Created: 2025-08-23
Type: Zettel
aliases: 
References: 
Links:
  - "[[Matrices]]"
  - "[[Identity matrix]]"
tags:
  - MATH31AH
---
- The inverse of a [[Matrices|matrix]] $A$ is $A^{-1}$, and plays the same role as $\frac{1}{a}$ does for $a$ in matrix multiplication
	- We can use the inverse of a matrix to solve systems of linear equations
	- The only number that does not have an inverse is 0, but many matrices do not have a inverse
> **Definition: Left and right inverses of matrices.** Let $A$ be a matrix. If there is another matrix $B$ such that 
> $$
BA = I
$$> then $B$ is called a left inverse of $A$. If there is another matrix $C$ such that 
> $$
AC = I
$$> then $C$ is called a right inverse of $A$
- For example the matrix $\begin{bmatrix} 1 & 0 \\ 0  &  0\end{bmatrix}$ has no inverse, as there are no products that multiply and add to 1. to get the identity matrix.
	- For $A \in M_{m \times n} (\mathbb{R}$, for $m \leq n$, If $A$ doesn't have $m$ linearly independent columns, it doesn't have a matrix
> Proposition: If a matrix is a rectangular matrix, it has at most 1 inverse, with the number of columns in the inverse being the number of [[Linear independence|linearly independent]] columns in the matrix
> Example: Let $A = \begin{bmatrix} 1 & 0 & 1 \\ 0 & 1 & 2\end{bmatrix}$. We knew that this has at most 2 linearly independent column vectors, so it only has 1 inverse with 2 columns. We can calculate the inverse to be $B =  \begin{bmatrix} 1  &  0  \\ 0  &  1 \\ 0 & 0\end{bmatrix}$. This is the right inverse of $A$. We know it must not have a left inverse. Say that it did. We know that it must satisfy the equation $\begin{bmatrix} a_{1} & a_{2} \\ b_{1}  & b_{2} \\ c_{1} & c_{2}\end{bmatrix} \begin{bmatrix} 1 & 0 & 1 \\ 0 & 1 & 2\end{bmatrix} = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1\end{bmatrix}$ . Solving this system of linear equations, we get that $a_{1}=1, a_{2} = 0$, and $a_{1}+2a_{2} = 0$, which cannot be true.
- Remark: If $A \subset M_{m \times n}(\mathbb{R})$ is a full rank, the one of the inverses exist.
- A matrix that has both a left and right inverse is called an invertible matrix.
>**Definition: Invertible matrix**. An invertible matrix is a matrix that has both a left inverse and a right inverse.
- If a matrix $A$ has both a left and right inverse, they are identical, and such a matrix is called the inverse of $A$ and is denoted $A^{-1}$.
	- We can arrive at this result using the associative property
		- $C(AB)=CI=C$  and $(CA)B=IB=B$, so $C=B. \square$
- There is a formula for the inverse of 2 x 2 matrices: the inverse of 
$$
A = \begin{bmatrix}
a & b \\
c & d
\end{bmatrix} \text{ is } A^{-1} = \frac{1}{ad-bc}
\begin{bmatrix}
d & -b \\
-c  & a
\end{bmatrix}
$$
- A 2 x 2  matrix is invertible is $ad-bc\neq 0$
- If $A$ and $B$ are both invertible, then $AB$ is invertible, and the inverse is
$$
(AB)^{-1}=B^{-1}A^{-1}
$$
