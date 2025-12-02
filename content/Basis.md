---
Created: 2025-10-09
Type: Zettel
aliases:
References:
Links:
  - "[[Linear independence]]"
  - "[[Linear span]]"
tags:
  - MATH31AH
---
> **Definition: Basis.** A subset $E$ of $\mathbb{R}^n$ that is: 1) [[Linear independence|linearly independent]], 2) $L(E) = \mathbb{R}^n$ is called a *basis* of $\mathbb{R}^n$  
- Let $S\subset \mathbb{R}^n$ be a subset of $\mathbb{R}^n$
	- A subset $E_{s}$ of $S$ is a basis of $S$ if $E_{s}$ is linearly independent and $L(E_{s})=S$
- Examples of basis include $\{ \vec{e}_{1}, \dots, \vec{e}_{n} \}$, which is a basis of $\mathbb{R}^n$
	- This is called the *canonical basis* of $\mathbb{R}^n$
	- This is a basis because it is clearly linearly independent, and we can make any vector in $\mathbb{R}^n$ from these vectors
- Another example of basis [[Vectors]] include $\vec{w}_{1}=\begin{bmatrix}1 \\ 1\end{bmatrix}$ and $\vec{w}_{2}=\begin{bmatrix}1 \\ -1\end{bmatrix}$
> Proposition: Say we have a [[Matrices|matrix]] $M \in M_{n}(\mathbb{R})$, where $M_{n}(\mathbb{R})$ is the set of all $n \times n$ matrices with real numbers (square matrices). If $M$ is non-singular, meaning that is square with a non-zero determinant ($\det(M) \neq 0$), the set column vectors and the set of row vectors of $M$ are a basis of $\mathbb{R}^n$. 

> Theorem: Let $B$ be a basis of $\mathbb{R}^n$, $B =\{ \vec{v}_{1}, \dots, \vec{v}_{n} \}$. Then, any vector $\vec{w} \in \mathbb{R}^n$ can be uniquely (no other form) represented as 
$$
\vec{w} = r_{1}\vec{v}_{1}+\dots+ r_{n}\vec{v}_{n}, r_{i} \in \mathbb{R}
$$
- Basis are how we have vector representations in the first place
	- We implicitly use the canonical basis when not specifying basis
- The coordinate with a specific basis is denoted as $\begin{bmatrix} \vec{w}\end{bmatrix}_{B} = \begin{bmatrix}r_{1} \\ r_{2} \\ \vdots \\ r_{n}\end{bmatrix}$
> Proof: The representation of some $\vec{w}\in \mathbb{R}^n$ is unique.
> Pick $\vec{w} \in \mathbb{R}^n$. Since $\mathbb{R}^n=L(B)$ there exists $r_{i}\in \mathbb{R}$ such that $\vec{w}=r_{1}\vec{v}_{1} +\dots+ r_{n}\vec{v}_{n}$. Now to prove uniqueness of the above representation, suppose that an alternate representation $\vec{w}=m_{1}\vec{v}_{1}+\dots+m_{n}\vec{v}_{n}, m_{i} \in \mathbb{R}$. This means that if you subtract the following representations, you get $\vec{0}=(r_{1}-m_{1})\vec{v}_{1}+\dots+(r_{n}-m_{n})\vec{v}_{n}$. Since $B$, the basis, is linearly independent, all the coefficients of the vectors must be 0.
> $r_{1}-m_{1}=0, r_{2}-m_{2}=0, \dots, r_{n}-m_{n}=0$. Therefore $r_{i}=m_{i}$ for all $1 \leq i\leq n$ thus the representation is unique. 

> **Definition: Dimensions of a subspace** Let $S \subset \mathbb{R}^n$ be a linear subspace of $\mathbb{R}^n$. The dimensions of S is the number of elements in any basis of $S$. 
> Example: Let $S := \{  (x,y,0), x,y \in \mathbb{R} \} \subset \mathbb{R}^3$. See that $\{ (1,0,0), (0,1,0) \}$ is a basis of $S$. So, $\text{dim}S = 2$
- Observations: Any two basis of $S$ has the same number of elements
	- Any linearly independent subset of $\mathbb{R}^n$ can have at most $n$ elements