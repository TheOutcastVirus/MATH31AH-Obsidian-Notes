---
Created: 2025-08-22
Type: Zettel
aliases: 
References: 
Links:
  - "[[Vectors]]"
  - "[[Matrix multiplication]]"
tags:
  - MATH31AH
---
> Probably no other area of mathematics has been applied in such numerous and diverse contexts as the theory of matrices. In mechanics, electromagnetics, statistics, economics, operations research, the social sciences, and so on, the list of applications seems endless. By and large, this is due to the utility of matrix structure and methodology in conceptualizing sometimes complicated relationships and in the orderly processing of otherwise tedious algebraic calculations and numerical manipulations. — _James Cochran, Applied Mathematics: Principles, Techniques, and Applications_
- The other center actor in linear algebra is the *matrix*
> **Definition: Matrices of real numbers** $m \times n$ matrix is a rectangular array of real numbers of $m$ height, $n$ wide.
> $\begin{bmatrix} a_{11} & a_{12} & \dots &  a_{1n} \\ a_{21} & a_{22} & \dots  & a_{2n} \\ \vdots  \\  a_{n_{1}}\end{bmatrix}$
> $M_{m\times n}(\mathbb{R})$ is the collection of all $m\times n$ matrices with real numbers. It also also a vector space of dimension $mn$
- Addition and scalar multiplication are the same as for [[Vectors|vectors]]
- When adding two matrices, they have to be of the same dimensionality
	- $A + B = (a_{ij} + b_{ij})_{{1\leq}}$
> Note: $A \in M_{m \times n}(\mathbb{R}) = (a_{ij})_{1 \leq i \leq m, 1 \leq j \leq n} = (a_{ij})_{m,n}$
- Scalar multiplication is also simple 
- What is the benefit of structuring numbers like this?
	- Each linear transformation corresponds to [[Matrix multiplication|multiplication by a matrix]]. This is one, and a very important reason matrix multiplication is a natural and important operation