---
Created: 2025-11-06
Type: Zettel
aliases:
References:
Links:
  - "[[Determinant]]"
  - "[[Orthogonality]]"
tags:
  - MATH31AH
  - Incomplete
---
> **Definition: Cross product on $\mathbb{R}^3$** 
> Take some $v,w \in \mathbb{R}^3$. Cross product of the vector will be based on the [[determinant]] of the components of $v,w$ in the following way:
> $$\begin{bmatrix}v_{1} \\ v_{2} \\ v_{3}\end{bmatrix} \times \begin{bmatrix}w_{1} \\ w_{2} \\ w_{3}\end{bmatrix} = \begin{bmatrix}\det \begin{bmatrix}v_{2} & w_{2} \\ v_{3} & w_{3}\end{bmatrix}  \\ \det \begin{bmatrix} v_{3} & w_{3} \\ v_{1} & w_{1}\end{bmatrix} \\ \det \begin{bmatrix}v_{1} & w_{1} \\ v_{2} & w_{2}\end{bmatrix}\end{bmatrix}$$
> 
- The cross product will be a vector also in $\mathbb{R}^3$ that is [[Orthogonality|orthogonal]] to both of the vectors $v,w$
	- We can see this by taking the plane formed by $v$ and $w$, and creating a vector that is orthogonal to that plane
> Proof: Cross product orthogonality
> For our first case, we have to work to show that $v \cdot (v \times w) = 0 \in \mathbb{R}$.
> $\begin{bmatrix}v_{1} \\ v_{2} \\ v_{3}\end{bmatrix} \cdot \begin{bmatrix} v_{2}w_{3} - v_{3}w_{2} \\ v_{3}w_{1}-v_{1}w_{3} \\ v_{1}w_{2}-v_{2}w_{1}\end{bmatrix}$
> $= v_{1}(v_{2}w_{2}-v_{3}w_{2}) + v_{2}(v_{3}w_{1}-v_{1}w_{3}) + v_{3}(v_{1}w_{2}-v_{2}w_{1})$
> When expanded, this simplifies to zero.
> For our second case, we have to show that $w \cdot (v \times w) = 0 \in \mathbb{R}$
> $\begin{bmatrix}w_{1} \\ w_{2} \\ w_{3}\end{bmatrix} \cdot \begin{bmatrix} v_{2}w_{3} - v_{3}w_{2} \\ v_{3}w_{1}-v_{1}w_{3} \\ v_{1}w_{2}-v_{2}w_{1}\end{bmatrix}$
> $= w_{1}(v_{2}w_{2}-v_{3}w_{2}) + w_{2}(v_{3}w_{1}-v_{1}w_{3}) + w_{3}(v_{1}w_{2}-v_{2}w_{1})$
> Which when expanded, also simplifies to zero.

> Proof: Say that $v,w,u \in \mathbb{R}^3$. Then, $\det \begin{bmatrix}v & w & u\end{bmatrix} = w \cdot (w \times u)$
> TBA 


