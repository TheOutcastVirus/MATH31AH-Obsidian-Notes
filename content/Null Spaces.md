---
Created: 2025-10-21
Type: Zettel
aliases:
  - Kernel
References:
Links:
tags:
  - MATH31AH
---

> **Definition: Null space.** Let $T: \mathbb{R}^n \to \mathbb{R}^n$ be linear. The null space of $T$ or the kernel of $T$ (denoted $\ker(T)$). 
> $\ker(T):= \{ \vec{v} \in \mathbb{R}^n : T(\vec{v})= \vec{0} \}$
> We know that $\ker(T) \neq \emptyset$ as $T(\vec{v})=0$

> Proposition: $T:\mathbb{R}^n \to \mathbb{R}^n$, linear
> $ker(T)$ is a linear subspace of $\mathbb{R}^n$. 
> Proof: Pick $\vec{u}, \vec{v} \in \ker(T), \alpha, \beta \in \mathbb{R}$
> TBA

> Proposition: $T:\mathbb{R}^n \to \mathbb{R}^n$ is linear then $\ker(T) = \{ \vec{0} \}$ if and only if $T$ is one-one. 
> Proof: Pick $\vec{u},\vec{v}$ such that $T(\vec{u}) = T(\vec{v})$
> $=T(\vec{u}-\vec{v}) = \vec{0}$, as $T$ is a linear map
> So, $\vec{u}, \vec{v} \in \ker(T) = \{ \vec{0} \}$
> Therefore, $\vec{u}-\vec{v}=0, \vec{u} = \vec{v}$
> Hence, $T$ is one to one. 
> Other side: Note, $\vec{0} \in \ker(T)$
> Pick $\vec{v} \in \ker(T)$
> Then, $T(\vec{v}) = \vec{0} = T(\vec{0})$
> Since $T$ is one to one, $\vec{v} = 0$
> $\ker(T) \subset \{ \vec{0} \}$
> $\ker(T) = \{ \vec{0} \}$
- So essentially, we have a lot of vectors in the domain that map to zero
	- But we also have a lot of vectors that map to non-zero vectors, which gives the transform its non-triviality
- $*$Say some $S \subset \mathbb{R}^n$ is linear $\implies T(S)$ is also linear, and a subspace
	- What follows is that is you have transform $T:\mathbb{R}^n \to \mathbb{R}^m$ is linear, then $T(\mathbb{R}^n)$ is a subspace
- In conclusion, the vectors in $\ker(T)$ all map to $\vec{0}$, and the rest of the vectors span $T(R^n)$
>Example: $T: \mathbb{R}^2 \to \mathbb{R}^4$, $\begin{bmatrix}x \\ y\end{bmatrix} \mapsto \begin{bmatrix} x \\ 0 \\ y \\ x+y\end{bmatrix}$
>$ker(T)= \{ \begin{bmatrix} 0 \\ 0 \\ 0 \\ 0\end{bmatrix} \}$ 
>$T(R^2)= \{ \begin{bmatrix}x \\ 0 \\ y \\ x+y\end{bmatrix} : x,y \in \mathbb{R}\}$
>$=\{ x \begin{bmatrix}1 \\ 0 \\ 0 \\ 1\end{bmatrix} + y \begin{bmatrix}0 \\ 0 \\ 1 \\ 1\end{bmatrix}: x,y \in \mathbb{R}\}$
>$=L(\begin{bmatrix}1 \\ 0 \\ 0 \\ 1\end{bmatrix}, \begin{bmatrix}0 \\ 0 \\ 1 \\ 1\end{bmatrix})$
>$T(\begin{bmatrix}1 \\ 0\end{bmatrix}) =\begin{bmatrix}1 \\ 0 \\ 0 \\ 1\end{bmatrix},T(\begin{bmatrix}0 \\ 1\end{bmatrix})=\begin{bmatrix}0 \\ 0 \\ 1 \\ 1\end{bmatrix}$

> Definition: Rank-nullity. Rank is the dimension of $T(\mathbb{R}^n)$, nullity is the dimension of $ker(T)$
> Let $T: \mathbb{R}^n \to \mathbb{R}^m$ be a linear map. Then, $\dim \ker(T) + \dim T(\mathbb{R}^n)= n$
> Proof: Since $ker (T)$ is a subspace, let $\{ \vec{v}_{1},\dots,\vec{v}_{k} \}$ be a basis of $ker(T), (k < n)$.
> Pick $\vec{w}_{1} \not\in ker(T), T(\vec{w}_{1}) \neq \vec{0}$
> $\{ \vec{v}_{1},\dots,\vec{v}_{k}, \vec{w}_{1} \}$ is [[Linear independence|linearly independent]]. 
> $c_{1}\vec{w}_{1}+ b_{1}\vec{v}_{1}+\dots+b_{k}\vec{v}_{k}= \vec{0}$
> as $\{ \vec{v}_{i} \}^k_{i}$ is a basis, $b_{i}=0$, 
> Pick $\vec{w} \not\in L(\{ \vec{w}_{1}, \vec{v}_{1},\dots,\vec{v}_{k} \})$ and complete it to a basis of $\mathbb{R}^n$
> Remains to show $\{ T(\vec{w}_{i}),\dots,T(\vec{w}_{n_{0}k}, \vec{v}_{1}) \}$


> Proof of rank nullity: Note that $T(\mathbb{R}^n)$ is a linear subspace of the codomain $\mathbb{R}^m$. Thus, there exists $\{ w_{1},\dots,w_{l} \} \subset \mathbb{R}^n$ such that $\{ T(w_{1}),\dots,T(w_{l}) \}$, which is a basis of $T(\mathbb{R}^n)$.
> Now, we shall show that $\{ w_{1},\dots,w_{l} \} \subset \mathbb{R}^n$ is [[Linear independence|linearly independent]]. Suppose $c_{1}\vec{w}_{1}+\dots+c_{l}\vec{w}_{l} = \vec{0} \in R^n$. This implies that $T(c_{1}\vec{w}_{1}+\dots+c_{l}\vec{w}_{l}) = \vec{0} \in \mathbb{R}^n$. We can apply the linear property such that $c_{1}T(\vec{w}_{1})+\dots+c_{l}T(\vec{w}_{l}) = \vec{0} \in \mathbb{R}^n$. Therefore, $c_{1}=c_{2}=\dots=c_{l}=0 \in \mathbb{R}$
> Since $\ker (T) \subset \mathbb{R}^n$ is a subspace, say, $\{ v_{1},\dots,v_{k} \} \subset \mathbb{R}^n$ is a basis of $\ker(T)$. 
> Claim: $\{ v_{1},\dots,v_{k} \}  or \{ w_{1},\dots,w_{l} \}=B$ is a basis of $\mathbb{R}^n$. We know this because the union of two linearly independent sets is linearly independent from our homework. 
> Pick $\vec{u} \in \mathbb{R}^n$. Either $T(\vec{u} = \vec{0}) \implies \vec{u} \in \ker(T) \implies \vec{u} \in L(B)$, or $T(\vec{u})(\neq \vec{0}) \in T(\mathbb{R}^n)$
> This implies that $T(\vec{u}) = \alpha_{1}T(\vec{w}_{1})+\dots+\alpha_{l}T(w\vec{w}_{l})$, given $\alpha_{i} \in \mathbb{R}$.
> This implies that $T(\vec{u}) = T(\alpha_{1}\vec{w}_{1} + \dots \alpha_{l}\vec{w}_{l})$
> which implies that $T(\alpha_{1}\vec{w}+\dots+\alpha_{l}\vec{w}_{l}) - T(\vec{u}) = \vec{0}\in \mathbb{R}^m$
> Which implies that $T(\alpha_{1}\vec{w}+\dots+\alpha_{l}\vec{w}_{l} - \vec{u}) = \vec{0} \in \mathbb{R}^m$
> $\alpha_{1}\vec{w}+\dots+\alpha_{l}\vec{w}_{l} - \vec{u} \in \ker (T)$
> $\alpha_{1}\vec{w}+\dots+\alpha_{l}\vec{w}_{l} - \vec{u}  = \beta_{1}v_{1}+\dots+\beta_{2}v_{k}$
> $\vec{u} = \alpha_{1}\vec{w}_{1}+\dots+\alpha_{l}\vec{w}_{l} - \beta_{1}\vec{v}_{1} -\dots-\beta_{k}\vec{v}_{k} \in L(B)$ So, $B$ is a basis of $R^n$. P. 

> Example: $T: \mathbb{R}^3 \to \mathbb{R}^2$ as $\begin{bmatrix}x \\ y \\ z\end{bmatrix}\mapsto \begin{bmatrix}x \\ y+z\end{bmatrix}$
> $\ker T = \{ \begin{bmatrix}x \\ y \\ z\end{bmatrix} : \begin{bmatrix}x \\ y+z \end{bmatrix} = \begin{bmatrix}0 \\ 0\end{bmatrix} \}$
> $= L(\{ \begin{bmatrix}0 \\ 1 \\ -1\end{bmatrix} \})$. Therefore, $\dim \ker (T) = 1$
> $T(\mathbb{R}^3) := \{ \begin{bmatrix}x \\ y+z\end{bmatrix} : x,y ,z\in \mathbb{R}\} = L\{ \begin{bmatrix}1 \\ 0\end{bmatrix}, \begin{bmatrix}0 \\ 1\end{bmatrix} \} = \mathbb{R}^n$ 
> Therefore, $\dim T(\mathbb{R}^3) = 2$
> Thus, $\dim \ker(T) + \dim T(\mathbb{R}^3) = 3$

