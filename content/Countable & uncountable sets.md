---
Created: 2025-09-30
Type: Zettel
aliases:
References:
Links:
  - "[[Functions]]"
  - "[[Set Theory]]"
tags:
  - MATH31AH
---
> **Definition: Countable set.**: A countable set $A$ is a set that is [[Injective, surjective, bijective functions#Bijective functions|bijective]] to $N$. 
> **Definition: Infinite set**: [[Infinite sets]] that are not countable are called uncountable sets. 
- Note that we do NOT consider finite sets to be countable. 
## Cardinality
> Definition: Cardinality.  $A$ is a set. The cardinality of $A$ is the number of elements contained in $A$. For example, if $A = \{ 1,2,3,a,b,\delta \}$, $|A|=6$
- The cardinality of $\mathbb{N}$, $|\mathbb{N}|=\aleph_{0}$
	- $|\mathbb{R}|=\aleph_{1}=2^{\aleph_{0}}$
	- This shows that there are infinities that are bigger and smaller than
- Let $A,B$ be two non-empty sets. 
	- If $|A|\leq|B|$, then there exists an [[Injective, surjective, bijective functions#Injective functions|injection]] $f: A \to B$
	- if $|B| \leq |A|$, then there exists a [[Injective, surjective, bijective functions#Surjective functions|surjection]] $f: A\to B$
## Power sets
> Definition: Power sets. Let $A$ be a non-empty set. The power set of $A$ denoted $\mathcal{P}(A)$ or $P(A)$ is the collection of all subsets of $A$. For example: Let $A = \{ 1,2 \}$. Then, $\mathcal{P}(A)= \{ \emptyset, \{ 1 \}, \{ 2 \}, \{ 1,2 \} \}$.
> $|A|=2$, $|\mathcal{P}(A)|=4=2^2$.
- For any finite set $A$ with $n$ elements $|\mathcal{P}(A)|=2^n$
## Infinite countable sets
- $\mathbb{N}$ is the smallest infinite set
	- The next largest infinite set is $\mathcal{P}(\mathbb{N}) \to \mathbb{R}$ which is bijective to $(0,1)$ $2^{|\mathbb{N}|}$
	- The next is $\mathcal{P}(\mathcal{P}(N))$ 
	- The continuum hypothesis asks if there are infinite sets that are not countable and has cardinality smaller than $|\mathcal{P}(\mathbb{N})|$ 
## Infinite uncountable sets
- There are also sets that are infinite but not countable 
	- This means that they cannot be defined as bijective to $\mathbb{N}$
- This is shown through Georg Cantor's [[Cantor's diagonal argument|diagonal argument]]