---
Created: 2025-11-04
Type: Zettel
aliases:
References:
Links:
  - "[[Dot product]]"
tags:
  - MATH31AH
---
> Definition: Orthogonality:
> Let $v \in \mathbb{R}^n$. A vector $w \in \mathbb{R}^n$ is called orthogonal to $v$ if $\langle v,w \rangle = 0$.
> For all $\lambda \in \mathbb{R}$
> $\langle \lambda v,w \rangle = \lambda \langle  v,w \rangle = 0$
- This is saying no matter how we scale the vectors, they stay orthogonal to each other
	- This applied the property of [[Dot product#Bilinearity|bilinearity]] that the [[dot product]] was shown to have
> Definition:
> Let $S \subset \mathbb{R}^n$ be non-empty. Define, S-perp as $S^{\perp} := \{ v \in \mathbb{R}^n : \langle v,s \rangle = 0, s \in S\}$
- This can be show to be a linear subspace.
	- This means that means that any linear combination of orthogonal vectors will also be orthogonal
> Proposition: 
> Let $S (\neq_{0})\subset \mathbb{R}^n$. Then, $S^{\perp}$ is a [[Linear subspaces|linear subspace]] of $\mathbb{R}^n$. 
> Proof: 
> Pick $v,w \in S^{\perp}, \alpha,\beta \in \mathbb{R}$. 
> Then, $\langle v,s \rangle = 0$ and $\langle w,s \rangle = 0$, for all $s \in S$
> $\implies\alpha \langle v,s \rangle + \beta \langle w,s \rangle = 0$, for all $s \in S$
> $\implies \langle \alpha v+\beta w,s \rangle = 0$, for all $s \in S$
> $\implies\alpha v +\beta w \in S^{\perp}$. Hence, $S^{\perp}$ is a a linear subspace.

> Definition: Let $S$ be a linear subspace of $\mathbb{R}^n$. Then, $S^{\perp}$ is called the orthogonal complement of $S$. 
> $\mathbb{R}^n = S \oplus S^{\perp}$
> From this, this means that $S+S^{\perp} = \mathbb{R}^n$ and that $S \cap S^{\perp} = \{ \vec{0} \}$

> Remark:
> Let $S(\neq 0) \subset \mathbb{R}^n$ and $S^{\perp}$ be the collection of all vectors orthogonal to the elements of $S$. Then the [[Linear span|linear span]] of the set is the same as set: $(L(S))^{\perp} = S^{\perp}$.

> Pythagorean identity:
> let $v_{1},v_{2},\dots,v_{k} \in \mathbb{R}^{\infty}$ be such that $\langle v_{i}, v_{j}\rangle = 0$, whenever $i\neq j$.
> Then, $\lVert v_{1}+\dots+v_{k} \rVert^{2} = \lVert v_{1} \rVert^{2}+\lVert v_{2} \rVert^{2} +\dots+\lVert v_{k} \rVert^{2}$
> Proof:
> Base case: $\lVert v_{1} \rVert^{2} = \lVert v_{1} \rVert^{2}$
> for $k=2$. $\langle v_{1},v_{2} \rangle = 0, v_{i} \in \mathbb{R}^n$
> $\lVert v_{1}+v_{2} \rVert^{2} = \langle v_{1}+v_{2},v_{1}+v_{2} \rangle$
> $=\langle v_{1},v_{1}+v_{2} \rangle+\langle v_{2},v_{1}+v_{2} \rangle$
> $\lVert v_{1} \rVert^{2}+2\langle v_{1},v_{2}\rangle  + \lVert v_{2} \rVert^{2}$. Since we know that the dot product between the two elements must be zero, we can eliminate $2\langle v_{1},v_{2} \rangle$
> $=\lVert v_{1} \rVert^{2}+\lVert v_{2} \rVert^{2}$. This proves $k=2$
> Assume, for $k=l$,
> $\lVert v_{1}+\dots+v_{l} \rVert^{2} = \lVert v_{1} \rVert^{2} +\dots+\lVert v_{2} \rVert^{2}$, whenever $\langle v_{i}, v_{j} \rangle = 0, i\neq j$ for $k = l+1$, suppose,
> $\{ v_{1},\dots,v_{l},v_{l+1} \}$ bet such that $\langle v_{i},v_{j} \rangle = 0, i\neq j$
> $\lVert v_{1}+\dots+v_{l}+v_{l+1} \rVert^{2}$. Say that $w = v_{1}+\dots+v_{l}$
> $=\lVert w+v_{l+1} \rVert$
> $=\lVert w \rVert^{2} + 2 \langle w, v_{l+1} \rangle + \lVert v_{l+1} \rVert^{2}$
> $=\lVert w \rVert^{2}+\lVert v_{l+1} \rVert^{2}$
> By the inductive assumption, 
> $\lVert w \rVert^{2} = \lVert v_{1}+\dots+v_{l} \rVert^{2}$
> $=\lVert v_{1} \rVert^{2}+\dots+\lVert v_{l} \rVert^{2}$
> and hence $\lVert v_{1}+\dots+v_{l+1} \rVert^{2}$
> $=\lVert w \rVert^{2}+\lVert v_{l+1} \rVert^{2}$
> $=\lVert v_{1} \rVert^{2}+\dots+\lVert v_{l} \rVert^{2}+\lVert v_{l+1} \rVert^{2}$