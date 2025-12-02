---
Created: 2025-09-25
Type: Zettel
aliases:
References:
Links:
  - "[[Set Theory]]"
tags:
  - MATH31AH
---
- Suppose $A$ is a non-empty set. A binary relation is an ordered pair of two elements of the set. This is denoted as $(m,n)$ or $mRn$
> Example: Our set is $\mathbb{N}$, relation = divisibility by 3. We will say $mRn$ if $\frac{m}{n} \in \mathbb{N}$
> Elements related with 3 are $3Rn$, which are natural numbers divisible by 3. 
> Example: $\{\mathbb{N},3\mathbb{N},5\mathbb{N},\mathbb{Z},\mathbb{Q},\mathbb{R}-\mathbb{Q}\}$
> Define $ARB <=> A \subset B$
> Then, $3\mathbb{N}R\mathbb{N} \implies 3\mathbb{N} \subset \mathbb{N}$
- Given that $S$ is a non-empty set, $R$ is a binary relation, $R$ is **reflexive** if $aRa$ for all $a \in S$.
- A relation is **symmetric** if $aRb$ and $bRa$ are equal, for all $a,b$ in $S$
	- A trivial example of a symmetric relation is equivalence ($=$)
- If a relation is **transitive**, then if $aRb$ and $bRc$ then $aRc$, for all $a,b,c$ in $S$
> Example: $(\mathbb{R}, \leq)$ is an example of a transitive relation.
> Example: In $\mathbb{N}$, $R$ is a a binary relation defined as $mRn <=> mn$ is even. This relation is not transitive because $3R2$ is 6 which is even, and $2R5$ is 10 which is even, but $3R5$ is 15 which is not even
- A relation $R$ on a non-empty set $S$ is called an *equivalence relation* if $R$ is reflexive, symmetric, and transitive. 
> Example: Consider two sets, $A,B$. 
> $A \times B = \{ (a,b) : a \in A, b\in B \}$
> Relate each element of $A$ to a unique element of $B$
- A nicer way to describe relations is a [[Functions]].
