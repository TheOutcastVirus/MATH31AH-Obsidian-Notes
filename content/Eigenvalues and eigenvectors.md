---
Created: 2025-11-06
Type: Zettel
aliases:
  - eigenvalues
  - eigenvectors
References:
Links:
  - "[[Linear transformations]]"
  - "[[Linear subspaces]]"
tags:
  - MATH31AH
---
- Given a [[linear transformations|linear map]] $T$ from $\mathbb{R}^n$ to $\mathbb{R}^n$, we want to find the directions where the inputs do not change 
	- Say that we have some [[Linear subspaces|subspace]] $H$, such as plane or line. If $T(H) \subset H$, this means that all $T$ can do is scale at most
	- This subspace $H$ is called an invariant subspace with regards to $T$
> **Definition: Eigenvalues**
> Let $T:\mathbb{R}^n \to \mathbb{R}^n$ be a linear transformation. Let $v \in \mathbb{R}^n \setminus \{ 0 \}$, and $L(v)$ is the span of $\{ v \}$.
> If $L(v)$ is invariant under $T$, then that means for some $\lambda_{0}\in \mathbb{R}$, that  $T(v) = \lambda_{0}v$. $\lambda_{0}$ is called an eigenvalue of $T$ and $v$ is an associated eigenvector.
- Essentially, for all of the eigenvectors, the transform $T$ can be simplified to multiplication by scalar $\lambda_{0}$
- Here is an alternate definition for eigenvalues and eigenvectors, with respect to matrices 
> **Definition**: Let $A \in M_{n}(\mathbb{R})$. $\lambda_{0} \in \mathbb{C}$ is called an eigenvalue of $A$ if there exists $v \in \mathbb{R}^n\setminus \{ 0 \}$ such that $Av=\lambda v$, and $v$ is called the associated eigenvector.
> $\lambda_{0}\in \mathbb{C}$ is called an eigenvalue of $A\in M_{n}(\mathbb{R})$ if $\det(A - \lambda Id) = 0$. That is, if $\lambda_{0}$ solves $\det(A-xId)$
## Finding eigenvalues
- Now, how do we actually end up finding eigenvalues?
	- You have to start with setting the transformation and scalar multiplication
> We know that the definition of an eigenvalues is that for some linear transformation $T$, that $T(v) = \lambda_{0}v \in \mathbb{R}^n$
> Rearranging the equation, we can write $T(v) - \lambda_{0}v = 0  \in \mathbb{R}^n$
> $\implies (T-\lambda_{0}Id)(v) = 0 \in \mathbb{R}^n$
>   $v \in \ker(T-\lambda_{0}Id)$
> Hence, $T-\lambda_{0}Id$ is not an isomorphism (since it is not one to one).
> The matrix associated: $[T] - \lambda_{0}Id$ is not invertible, meaning that $\det ([T]-\lambda_{0}Id) = 0$
> This gives us the *characteristic polynomial* for $T$. The solutions to this polynomial are the eigenvalues of $T$.

> **Definition: Characteristic polynomial**. For some transformation $A$, the characteristic polynomial is:
> 
$$
\det(A-xI)=0
$$
> The values of $x$ that solve this equation are the eigenvalues ($\lambda_{1},\lambda_{2},\dots$) of $A$.


> Example:
> Find the eigenvalues of $A = \begin{bmatrix}1 & 2 \\ 3 & 4\end{bmatrix}$
> Eigenvalues are zeros of $\det (A - x Id)$
> $=\det \left( \begin{bmatrix}1 & 2 \\ 3 & 4\end{bmatrix} - \begin{bmatrix}x & 0 \\ 0 & x\end{bmatrix}\right)$
> $= \det \begin{bmatrix}1-x & 2 \\ 3 & 4-x\end{bmatrix}$
> $=(1-x)(4-x)-6$
> $x^{2}-5x-2 =0$
> The solutions to this equation are the eigenvalues of $A$. In this case, there are no real solutions, so the eigenvalues are complex.

> Remark:
> Let $\lambda_{0} \in \mathbb{C}$ be an eigenvalue of $T$ and $v \in \mathbb{R}^n \setminus \{ 0 \}$ is an eigenvector associated with $\lambda_{0}$.
> Then, $T(v)=\lambda_{0} v$
> $\implies T(\alpha v)=\alpha T(v)$
> $=\alpha\lambda_{0}v$
> $=\lambda_{0}(\alpha v)$
- This remark shows that any eigenvalue $\lambda_{0}$ will have an infinite number of associated eigenvectors
	- This is because due to linearity, we can multiply the vector by any real number $\alpha$
> If $v$ is an eigenvector of $\lambda_{0}$, then $\alpha v$ is also an eigenvector of $\lambda_{0}$, for all $\alpha \in \mathbb{R} \setminus \{ 0 \}$ 
> Suppose $\{ v_{1},v_{2} \}$ is [[Linear independence|linearly independent]] of eigenvectors of $\lambda_{0}$. 
> Then all elements of $L(\{ v_{1},v_{2} \}) \setminus\{ 0 \}$ is an eigenvector of $\lambda_{0}$.
> Proof:
> TBA
## Eigenvalues and eigenvector for 3x3 matrices
- When you have an [[Special matrices|upper triangular matrix]], the eigen values are simply the values along the diagonal
> Example: Find the eigenvalues of $A= \begin{bmatrix}1 & -7 & -1 \\ 0 & 2 & -2 \\ 0 & 0 & -3\end{bmatrix}$
>$\det(A-xI)=\det \begin{bmatrix}1-x & -7 & -1 \\ 0 & 2-x & -2 \\ 0 & 0 & -3-x\end{bmatrix}=0$ 
>Notice that when $x=1$, the entire column is equal to zero, and therefore the determinant is equal to zero. This means that $\lambda=1$ is one of the eigenvalues of this matrix. The same follows for $x=2,-3$.
- To find the eigenvector for a given eigenvalue $\lambda_{n}$, we have to solve for the system of equations where $(A-\lambda_{n}I)v=0$
> Example: Find the eigenvectors for $A$ in the previous problem.
> Our eigenvector is $v\in \mathbb{R}^3 \setminus \{ 0 \}$,where $Av=1\cdot v$, as $\lambda_{1}=1$. This implies that $Av=v$. We have to solve $(A-\lambda_{1}I)v=0\in \mathbb{R}^3$. 
> $\begin{bmatrix}0 & -7 & -1 \\ 0 & 1 & -2 \\ 0 & 0 & -4\end{bmatrix}\begin{bmatrix}v_{1} \\ v_{2} \\ v_{3}\end{bmatrix}=\begin{bmatrix}0 \\ 0 \\ 0\end{bmatrix}$
> This gives us that $-7v_{2}-v_{3}=0$, $v_{2}-2v_{3}=0$, $-4v_{3}=0$
> $v_{1}$ is a free variable, so we can say that $v=\begin{bmatrix}1 \\ 0 \\ 0\end{bmatrix}$ is an example of an eigenvector of $\lambda_{1}=1$.


