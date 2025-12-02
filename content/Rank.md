---
Created: 2025-11-14
Type: Zettel
aliases:
References:
Links:
  - "[[Linear independence]]"
  - "[[Linear span]]"
  - "[[Determinant]]"
  - "[[Systems of Linear Equations]]"
tags:
  - MATH31AH
---
> **Definition: Rank.** The rank of a [[Matrices|matrix]] is the maximum number of [[Linear independence|linearly independent]] rows or columns in the matrix.
- Alternatively, it can be thought of as the dimension of the [[linear span]] of the vectors in a matrix
- For a matrix to be *full rank*, the rank will be equal to the smaller of its dimensions (either rows or columns)
- There are multiple ways to show that some matrix $A$ is or is not full rank
	- If a matrix can be reduced to have a row with all zeros, this means that matrix does not have full rank
	- If the [[determinant]] of $A$, $\det A \neq 0$, it is full rank. If not, and $\det A = 0$, the the matrix is not full rank
- If the rank of a matrix is equal to the numbers of unknows in a [[Systems of Linear Equations|system of linear equations]], then the system has a unique solution
	- If the rank is less that the number of unknowns, there are infinitely many solutions