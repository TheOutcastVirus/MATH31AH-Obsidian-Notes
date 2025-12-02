---
Created: 2025-10-09
Type: Zettel
aliases:
References:
Links:
  - "[[Linear subspaces]]"
tags:
  - MATH31AH
---
- Suppose $\vec{v}\in S$, where $S$ is some [[Linear subspaces|subspace]] of $\mathbb{R}^n$. Then $L(\vec{v}):=\{ a \vec{v}:a\in \mathbb{R} \}$. Then, $L(\vec{v})$ is a subspace of $\mathbb{R}^n$
> Proof: Pick $\vec{w}_{1},\vec{w}_{2} \in S$. 
> $\vec{w}_{1}=a_{1}\vec{v}$, for some $a_{1}\in \mathbb{R}$. 
> $\vec{w}_{2}=a_{2}\vec{v}$, for some $a_{2}\in \mathbb{R}$. 
> $\vec{w}_{1}+\vec{w}_{2}=a_{1}\vec{v}+a_{2}\vec{v}=(a_{1}+a_{2}\vec{v} \in L(\vec{v}))$
> $(a_{1}+a_{2})\vec{v}$ is a scalar multiple of $\vec{v}$, hence $(a_{1}+a_{2})\vec{v} \in L(\vec{v})$
> Pick $r \in \mathbb{R}$. $r\vec{w}_{1}=ra_{1}\vec{v}=(ra_{1})\vec{v}$
> $r\vec{w}_{1} = (ra_{1})\vec{v}$ is a scalar multiple of $\vec{v}$. $r\vec{w}_{1}=(ra_{1})\vec{v} \in L(\vec{v})$. 
> Thus, $L(\vec{v})$ is a subspace of $S$. 
> First step: Show $L(\vec{v})\subset S$ 
> Pick $\vec{w}_{1} \in L(\vec{v})$. $\vec{w}_{1} = a_{1}\vec{v}$. But $\vec{v} \in S$ and $S$ is a subspace. Since $S$ is closed under scalar multiplication, it means $L(\vec{v})$ is a subset of $S$.
- $L(\vec{v})$ is really the definition of a line 
	- ![[image-19.webp]]
> **Definition: Linear span.** Let $Q \subset \mathbb{R}^n$ be a non-empty subset of $\mathbb{R}^n$.  Define the linear span of $Q$ in $\mathbb{R}^n$ as $L(Q):= \{  a_{1}\vec{v}_{1} + \dots + a_{l}\vec{v}_{l} : \vec{v}_{i} \in Q, a_{i} \in \mathbb{R}, l \in \mathbb{N}\}$
- This is essentially picking finitely many vectors from $Q$ and consider *any* linear combination of the following vectors
	- This space is a subspace of $\mathbb{R}^n$
	- The linear span of two linearly independent subspaces with not be subsets of each other
> Proposition: For any subset $Q (\neq \{ 0 \}) \subset \mathbb{R}^n$, the linear span $L(Q)$ is a subspace of $\mathbb{R}^n$
> Proof: Pick $\vec{w}_{1}, \vec{w}_{2} \in L(Q)$. Then, $\vec{w}_{1}=r_{1}\vec{v}_{1}+\dots+r_{l}\vec{v}_{l}$ where $\vec{v}_{i}\in Q, r_{i} \in \mathbb{R}$. $\vec{w}_{2}=m_{1}\vec{v}_{n_{1}}+\dots+m_{k}\vec{v}_{n_{k}}$ is a linear combination of elements of $Q$. Thus, $\vec{w}_{1}+\vec{w}_{2} \in L(Q)$.
> Pick $\vec{w} \in L(Q), r \in R$ then $\vec{w}=m_{1}\vec{v}_{1}+\dots+m_{s}\vec{v}_{s}$ and $rw\vec{w}=(rm)\vec{v}_{1}+\dots+(rm_{s})\vec{v}_{s}$ where $\vec{v}_{i}\in Q, m_{i}\in \mathbb{R}$
> So, $r\vec{w}$ is a linear combination of the elements of $Q$. Thus, $r\vec{w} \in L(Q)$. Hence, $L(Q)$ is a subspace of $\mathbb{R}^n$ 

> Example: Say that we have a set $Q = \{ \vec{w}_{1}, \vec{w}_{2} \}$, where $\vec{w}_{1}= \begin{bmatrix}1 \\ 1\end{bmatrix}, \vec{w}_{2}=\begin{bmatrix}1 \\ -1\end{bmatrix}$. We want to show that $L(Q)=\mathbb{R}^2$. To do that, we have to show that 1) $L(Q) \subset \mathbb{R}^2$, and 2) $\mathbb{R}^2 \subset L(Q)$. 
> Case 1 is immediate, since we know that $Q \subset \mathbb{R}^2$. For case 2, pick $\begin{bmatrix}x \\ y\end{bmatrix} \subset \mathbb{R}^2$. We have to work to show that $\begin{bmatrix}x \\ y\end{bmatrix} \in L(Q)$. $L(Q)=\{ r_{1}\vec{w}_{1} + r_{2}\vec{w}_{2} : r_{i} \in \mathbb{R} \}$. 
> $r_{1}\begin{bmatrix}1 \\ 1\end{bmatrix} + r_{2}\begin{bmatrix}1 \\ -1\end{bmatrix} = \begin{bmatrix}r_{1} + r_{2} \\ r_{1} - r_{2} \end{bmatrix}$. We need to find $r_{1},r_{2} \in \mathbb{R}$ such that $\begin{bmatrix}x \\ y\end{bmatrix}=\begin{bmatrix}r_{1} + r_{2} \\ r_{1}-r_{2}\end{bmatrix} \implies r_{1} + r_{2} = x, r_{1} - r_{2} = y$
> Solving for $r_{1}, r_{2}$, we get that $r_{1}=\frac{x+y}{2}, r_{2} = \frac{x-y}{2}$. Now, we can describe any $x,y$ with the linear span of $L(Q)$. 
> $\begin{bmatrix}x \\ y\end{bmatrix} = \left( \frac{x+y}{2} \right) \begin{bmatrix}1 \\ 1\end{bmatrix} + \left( \frac{x-y}{2} \right) \begin{bmatrix}1 \\ -1\end{bmatrix} \in L(Q)$. 
> Thus, $L(Q) = \mathbb{R}^n$