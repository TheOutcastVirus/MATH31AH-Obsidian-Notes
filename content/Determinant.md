---
Created: 2025-11-06
Type: Zettel
aliases:
References:
Links:
  - "[[Matrix inverses]]"
  - "[[Linear independence]]"
  - "[[Systems of Linear Equations]]"
  - "[[Rank]]"
tags:
  - MATH31AH
---
> Definition: Determinant
> $$
\det \begin{bmatrix}
a_{1} & a_{2} \\
b_{1} & b_{2}
\end{bmatrix} = a_{1}b_{2}-a_{2}b_{1}
$$
- The geometric interpretation is this is the area of the parallelogram formed by the two vectors
	- This expands to higher dimensions as well
	- For the determinant of a 3 by 3 [[Matrices|matrix]], it would be the volume of the parallel piped in 3 dimensions
> Definition: Determinant of a 3 by 3 matrix
> $$
 \begin{bmatrix}
a_{1} & a_{2} & a_{3} \\
b_{1} & b_{2} & b_{3} \\
c_{1} & c_{2} & c_{3}
\end{bmatrix} = a_{1} \det \begin{bmatrix}
b_{2} & b_{3} \\
c_{2} & c_{3}
\end{bmatrix} - a_{2} \det \begin{bmatrix}
b_{1} & b_{3} \\
c_{1} &  c_{3}
\end{bmatrix} + a_{3} \det \begin{bmatrix}
b_{1} & b_{2} \\
c_{1} & c_{2}
\end{bmatrix}
$$
- The reason that determinants are useful is because they give us the constant that any area on the plane is increased or decreased by following a linear transformation
	- This can give use information about the nature of the transformation
- For some matrix $A$, if $\det A \neq 0$, then the following are true:
	- The matrix is [[Matrix inverses|invertible]] (non-singular)
	- Its columns/rows are [[Linear independence|linearly independent]]
	- The associated [[Systems of Linear Equations|linear system]] $A \mathbf{x} =  \mathbf{b}$ has a unique solution
	- The linear transformation preserves volume (meaning that it does not collapse the space to a lower dimension)
	- The matrix has full [[rank]]
- In the case that $\det A = 0$
	- The matrix is non-invertible
	- Its columns/rows are linearly dependent
	- The associated linear system has no solution or infinitely many solutions
	- The linear transformation collapses the space to a lower dimension
	- The matrix is rank-deficient
> Property: 
> $$
\det A  = \det A^{T}
$$

> Property:
> $$
\det (XY)=\det X\det Y
$$