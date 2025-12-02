---
Created: 2025-08-22
Type: Zettel
aliases:
References:
Links:
  - "[[Matrices]]"
tags:
  - MATH31AH
---
- When multiplying matrices $A$ and $B$, you can write matrix $B$ to the top and right of matrix $A$, so that their corners are touching. The resultant matrix $AB$ will fit in the space below matrix $B$
	- The first entry of the product $AB$ is given by multiplying, one by one, the entries of the first *row* of $A$ by those of the first *column* of $B$ and adding these products together
	- The second entry of $AB$ is derived from doing the same thing, but with the first row of $A$ with the second column of $B$
	- ![[Matrix Multiplication-1755890885162.webp]]
	- Matrix multiplication is not commutative, nor is able to computed for every pair of matrices. $BA$ is not able to be computed.
- If $A$ is a $m \times n$ matrix, and $B$ is a $n \times p$ matrix, then $AB$ is a $m \times p$ matrix.
> **Definition: Matrix multiplication**. If $A$ is an $m \times n$ matrix whose $(i,j)$th entry is is $a_{i,j}$, and $B$ is an $n \times p$ matrix whose $(i,j)$th entry is $b_{i,j}$, then $C = AB$ is the $m \times p$ matrix with entries:
> $$
c_{i,j} = \sum^n_{k=1} a_{i,k} b_{k,j}
$$
> $$
= a_{i,1} b_{1,j} + a_{i,2} b_{2,j} + \dots + a_{i,n} b_{n,j}
$$
## Properties of matrix multiplication
- Matrix multiplication is associative, meaning the order the operation is applied in is irrelevant 
	- $(AB)C = A(BC)$
- Matrix multiplication is non-commutative, however. $AB$ might not be the same as $BA$, or might not even be able to be computed (the number of columns and rows do not match)
## Multiplication by standard basis vectors
- When multiplying a matrix $A$ by the standard basis vector $\vec{e}_{i}$ selects out the $i$th column of $A$
	- ![[Matrix multiplication by a standard basis vector-1755892013825.webp]]
- When you multiply $A$ and $B$, and select then $n$th column, it has the same effect as multiplying $A$ with the $n$th column of $B$
	- ![[Matrix multiplication by a standard basis vector-1755896257296.webp]]
- Say that $A \in M_{m \times n}, B \in M_{n \times p}$
	- We know that $AB \in M_{m \times p}$
	- What is the $i$th column of $AB$?
- The $i$th column of $AB$ can be written as $AB\vec{e}_{i}$, 
## [[Basis]] and matrix multiplication
- Set some $\vec{v} \in \mathbb{R}^n$. Let $\vec{v} = \begin{bmatrix} v_{1} \\ \vdots  \\ v_{n}\end{bmatrix}$. 
	- We can write this using standard basis vectors as such: $v_{1} \vec{e}_{1} + v_{2}\vec{e}_{2} + \dots + v_{n}\vec{e}_{n}$
	- We can also represent this as $\begin{bmatrix}\vec{e}_{1}, \vec{e}_{2}, \dots, \vec{e}_{n}\end{bmatrix} \begin{bmatrix}v_{1} \\ v_{2}  \\  \vdots  \\  v_{n}\end{bmatrix}$
- This kind of representation will be helpful for linear transformations and change of basis