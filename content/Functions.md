---
Created: 2025-09-25
Type: Zettel
aliases:
References:
Links:
  - "[[Relation]]"
  - "[[Injective, surjective, bijective functions]]"
tags:
  - MATH31AH
---
- A function has three things
	- two sets, the *domain* and *codomain*
	- a rule that associates any element in the domain to exactly one element in the codomain
- It must possible to evaluate the function on every element of the domain, and every output must be in the codomain
	- However, it is not needed for every element in the codomain to be a value of the function
	- The set of element actually reached by the function is called the *image*
> **Definition: Image.** The set of all values of $f$ is called its *image*: $y$ is an element of the image of a function $f:X \to Y$ if there exists an $x \in X$ such that $f(x)=y$
> Example: The codomain of the squaring function $f: \mathbb{R} \to \mathbb{R}$ given by $f(x)=x^{2}$ is $\mathbb{R}$, while the image is the nonnegative real numbers.
> Always, the image will be the subset of the codomain.
> **Definition: Preimage.** The preimage of some function $f:X \to Y$, denoted as $f^{-1}$, gives the set of the values that map to some set. 
> Formally, the preimage of some set $B \subset Y$, is $f^{-1}(B) := \{ x \in X: f(x) \in B \}$
- A function can also be described as a [[relation]] in $A \times B$ where each element of $A$ is related to a unique element of $B$. This can be described as $(a,f(a))$
	- This definition is what was introduced in lecture
		- The relation set is denoted as $\{ (a,b) , a \in, A \in B \}$
	- For one $a$, there is only one order pair $(a,b)$ in the relation set.
- Functions can be [[Injective, surjective, bijective functions|injective, surjective, or both (bijective)]]