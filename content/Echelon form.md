---
Created: 2025-11-06
Type: Zettel
aliases:
References:
Links:
  - "[[Matrices]]"
tags:
  - MATH31AH
---
> Definition: Echelon form. A [[Matrices|matrix]] is in echelon form if:
> - in every row the first non-zero element is 1, called a pivotal 1
> - the pivotal 1 of a lower row is always to the right of the pivot of a higher row
> - every column that contains a pivotal 1 has all other entries as zero
> - any rows consisting entirely of zeros must be at the bottom
> Example of a matrix in echelon form looks like this. The elements with an asterisk are called pivots.
> 
$$
\begin{bmatrix}
1^* & 1 & 0 & 0 & 0 \\
0 & 0 & 1^* & 2 & 0 \\
0 & 0 & 0 & 0 & 1^*
\end{bmatrix}
$$

> Example:
> Start with the following matrix $\begin{bmatrix}1 & 0 & 0  & 2\\ 0 & 0 & 1 & -1 \\ 0 & 1 & 0 & 1\end{bmatrix}$.
> $R_{2}' = R_{3}$
> $R_{3}' = R_{2}$
> $\begin{bmatrix} 1 & 0 & 0 & 2 \\ 0 & 1 & 0 & 1 \\ 0 & 0 & 1 & -1\end{bmatrix}$
> Now, this matrix is in echelon form. 
> 
- To convert to echelon form, you need to find the candidate to find a pivot