---
Created: 2025-10-03
Type: Zettel
aliases:
References:
Links:
tags:
  - MATH31AH
---
## Injective [[functions]]
- Also know as one-to-one
	- This is if every input to the function has only 1, unique output
- Let $f: A \to B$, $f$ is called a injective function if 
	- for each $b \in B$, $f(a)=b$, **at most one** solution
	- $f(a_{1})=f(a_{2})$, then $a_{1}=a_{2}$
> Example: let $f: \mathbb{N} \to \mathbb{N}$, as $f(x)=n^2$
## Surjective functions
- This can be described as 'onto'
	- Basically, if every element in the codomain has a solution
- Let $f: A \to B$. $f$ is called surjective if 
	- for each $b \in B$, the equation $f(a)=b$ **has at least one** solution
> Example: $f: \mathbb{N} \to \mathbb{N}$ , $f(n)=n$ (inc.)
## Bijective functions
- Also known as an invertible function 
- Let $f: A \to B$. $f$ is called bijective if 
	- $f$ is one-one
	- for each $b\in B$, $f(x)=b$ **has exactly one** solution
> Example: $f:A\to A$ . $f(a)=a$, the identity 
- Key point: to prove that a function is bijective, you have to prove that it is both injective and surjective

![[image-17.webp]]