---
Created: 2025-10-03
Type: Zettel
aliases:
References:
Links:
  - "[[Functions]]"
tags:
  - MATH31AH
---
> **Definition: Inverse image.** Let $f: X \to Y$ be a function, and $C \subset Y$ be a subset of the codomain of $f$. Then the *inverse image* (also know as the *preimage*) of $C$ under $f$, denoted as $f^{-1}(C)$, consists of those elements $\mathbf{x} \in X$ such that $f(\mathbf{x})\in C$. 
> Example: Let $f:\mathbb{R}\to \mathbb{R}$ be the (non-invertible) mapping $f(x)=x^{2}$. The inverse image of $\{ -1,4,9,16 \}$ under $f$ is $\{ -4, -3,-2,2,3,4\}$ 
> $$
f^{-1}(\{ -1,4,9,16 \})= \{ -4,-3,-2,2,3,4 \}
$$
- The inverse image is very similar to the inverse of a [[functions|function]]. It takes in the output, and gives the possible inputs
	- However, it is not a function because it also works on non-invertible ([[Injective, surjective, bijective functions|bijective]]) functions 
		- In the example above, $f^{-1}(\{ 4 \})=\{ -2,2 \}$. There are more than 1 outputs for 1 input
	- It also takes in and returns a [[Set Theory|set]]