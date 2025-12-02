---
Created: 2025-10-09
Type: Zettel
aliases:
References:
Links:
tags:
  - MATH31AH
---
> **Definition: Linear independence.** A subset $Q \subset \mathbb{R}^n$ is called linearly independent if for any $r_{1}\vec{v}_{1}+\dots+r_{k}\vec{v}_{k}=\vec{0} \in \mathbb{R}^n$ implies that $r_{1}, r_{2},\dots r_{k}$ must be equal to 0 and zero only. 
- Essentially, if there is no way to add the vectors in the set to get back to zero without multiplying by them zero, they are linearly independent.
- Examples of linearly independent vectors include any basis vectors, among others
	- Non-examples are sets of vectors where multiple are co-linear
> Example: Say we have some $Q = \{  \begin{bmatrix}1 \\ 0\end{bmatrix}, \begin{bmatrix} 0 \\ 1\end{bmatrix} \}$. Suppose that $r_{1}\begin{bmatrix}1 \\ 0 \end{bmatrix}+ r_{2}\begin{bmatrix}0  \\  1\end{bmatrix} = \begin{bmatrix}0 \\ 0\end{bmatrix}$. The only solution for this is $\begin{bmatrix}r_{1} \\ r_{2}\end{bmatrix} =  \begin{bmatrix} 0 \\ 0\end{bmatrix} \implies r_{1} =r_{2} = 0$. Thus, $Q$ is linearly independent. 
- There is a special set of linearly independent vectors: $\{ \vec{e}_{1}, \vec{e}_{2},\dots, \vec{e}_{n} \}$ 
	- They are vectors where the $n$th element is 1 and the rest are zero. $\vec{e}_{1} = \begin{bmatrix}1 \\ 0 \\ \vdots  \\ 0\end{bmatrix}$
> Remark: If $Q \subset \mathbb{R}^n$ is linearly independent, $\vec{0} \notin Q$
- This makes sense because any real number times zero equals zero
	- For a set of vectors to be linearly independent, they must reach zero through multiplying only by zero. 
> Proof: Suppose some $\vec{v} \in Q \subset \mathbb{R}^n$ and $\vec{v}\in L(Q \setminus \{ \vec{V} \})$. Then $Q$ is not linearly independent. 
- This claims that if there is $\vec{v}$ in $Q$, and we can make that vector through [[Linear span|linear combinations]] of other vectors in the set, it is not linearly independent
> As $\vec{v}\in L(Q \setminus \{ \vec{v} \})$, then there exists $w_{i} \in Q \setminus \{ \vec{v} \}, r_{i} \in \mathbb{R}$ . We want to see if $\vec{v}$ can be made by these combinations. 
> $\vec{v} = r_{1}\vec{w}_{1}+\dots+r_{k}\vec{w}_{k}$
> $0=(-1)\vec{v}+r_{1}\vec{w}_{1}+\dots+r_{k}\vec{w}_{k}$
> Since the coefficient of $\vec{v}=-1\neq 0$, and the total sums to 0, we can conclude that $\{ \vec{w}_{1},\dots,\vec{w}_{k} \} \subset Q$ is not linearly independent.

> Remark: If $A\subset B\subset \mathbb{R}^n$ and $A$ is not linearly independent, then $B$ is also not linearly independent. 
- This is just saying that is a subset of a set is not linearly independent, any larger sets that contain it are also not linearly independent. 
### Midterm review
- Say that $S \subset \mathbb{R}^n$ is linearly independent. This means that $|S| \leq n$
- Say that $S\subset \mathbb{R}^n$ [[Linear span|spans]] $\mathbb{R}^n$, then $|S| \geq n$.