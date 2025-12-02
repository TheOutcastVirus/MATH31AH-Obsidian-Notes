---
Created: 2025-08-23
Type: Zettel
aliases:
  - symmetric matrix
  - anti-symmetric matrix
  - diagonal matrix
  - triangular matrix
References:
Links:
  - "[[Matrices]]"
  - "[[Identity matrix]]"
  - "[[Transpose]]"
tags:
  - MATH31AH
---
> **Definition: Symmetric matrix**. A symmetric matrix is equal to its transpose. An anti-symmetric matrix is equal to minus its [[transpose]]. All symmetric matrices are square matrices.
- For a symmetric matrix, $a_{12} = a_{21}$, etc.
>**Definition: Anti-symmetric**: $A^T = -A$
> All anti-symmetric matrices are also square matrices.
- For all anti-symmetric matrices, the diagonal elements are zero. 
- For any matrix $A \in M_{n \times m}(\mathbb{R})$, you can write it as the sum of symmetric and anti-symmetric matrices
	- $A = \frac{1}{2}(A+A^T) + \frac{1}{2}(A \cdot A^T)$
	- 
> **Definition: Triangular matrix**. An upper triangular matrix is a square matrix with nonzero entries on or above the main diagonal. A lower triangular matrix is a square matrix with nonzero entries only on or below the main diagonal.
- Again, all of the triangular matrices are square matrices
- For some $A = (a_{ij})_{n\times n}$, Any element $a_{ij} \in A$ is below the diagonal, then their row index must be larger than their column index.
	- $i$ is the row index, and $j$ is the column index
- So, a matrix $A$ is upper triangular if $a_{ij}= 0$, where $i > j$.
- A matrix $A$ is lower triangular is $a_{ij}=0$, where $j > i$. 
> **Definition: Diagonal matrix**. A diagonal matrix is a square matrix with nonzero entries (if any) only on the main diagonal (top left to bottom right). Similar to the [[Identity matrix|identity matrices]] $I$, multiplied by some constant
- Another way of defining these matrices is $A = (a_{ij})_{n \times n}$, $a_{ij}= 0$, if $i \neq j$. 
- Diagonal matrices are symmetric, anti-symmetric, and triangular
- If $A$ is symmetric, and $A$ is [[Matrix inverses|invertible]], does that force $A^-1$ to be symmetric?
	- If $A$ is anti-symmetric, same question
	- If a diagonal matrix $A$ is invertible, is $A^{-1}$ necessarily diagonal?