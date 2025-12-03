---
Created: 2025-12-02
Type: Zettel
aliases:
References:
Links:
  - "[[Eigenbasis]]"
tags:
  - MATH31AH
---
> Definition: Let $A\in M_{n}(\mathbb{R})$
> $A$ is called a diagonalizable if there exists $S\in M_{n}(\mathbb{R})$, invertible such that $S^{-1}AS$ is a [[Special matrices|diagonal matrix]].
- Recall: A [[Matrices|matrix]] is diagonal is all its non-diagonal entries are equal to zero
>Let $\{ v_{1},\dots,v_{n} \}$ be an [[eigenbasis]] of $A\in M_{n}(\mathbb{R})$
> $Av_{j}=\lambda_{j}v_{j}, j=1,\dots,n$
> Recall:
> $[T]_{B}=\begin{bmatrix}[Tv_{1}]_{B} & \dots  & [Tv_{n}]_{B}\end{bmatrix}$
> $\implies[A]_{B}=\begin{bmatrix}[Av_{1}]_{B} & \dots & [Av_{n}]_{B}\end{bmatrix}$
> $=\begin{bmatrix}[\lambda_{1}v_{1}]_{B} & \dots & [\lambda_{n}v_{n}]_{B}\end{bmatrix}$
> We know that
> $[\lambda_{1}v_{1}]_{B}= \begin{bmatrix}\lambda_{1} \\ 0 \\ 0 \\ \dots\end{bmatrix}$
> $[\lambda_{j}v_{j}]_{B} = \begin{bmatrix}0 \\ \dots \\ 0 \\ \lambda_{j} \\ 0 \\ \dots\end{bmatrix}$
> Therefore, the matrix written out is a diagonal matrix
> $=\begin{bmatrix}\lambda_{1} & 0 & 0 & \dots & 0 \\ 0 & \lambda_{2} & 0 & \dots & 0 \\ 0 & 0 & \lambda_{3} & \dots & 0 \\ \vdots \\ 0 & 0 & 0 & \dots & \lambda_{n}\end{bmatrix}$
- When does an eigenbasis exist?
	- There exist $Q\in M_{n}(\mathbb{R})$, invertible, such that $Q^{-1}AQ=\begin{bmatrix}\lambda_{1} & \dots \\ \vdots & \lambda_{n}\end{bmatrix}$
> Example:
> $A =\begin{bmatrix}1 & -1 & 0 \\ -1 & 2 & -1 \\ 0 & -1 & 1\end{bmatrix}$
> $\det(A-xI_{3}) = \det \begin{bmatrix}1-x & -1 & 0 \\ -1 & 2-x & -1 \\ 0 & -1 & 1-x\end{bmatrix}$
> $=(1-x)[(2-x)(1-x)-1]$

## Review
