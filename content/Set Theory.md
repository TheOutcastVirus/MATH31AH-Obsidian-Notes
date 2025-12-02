---
Created: 2025-08-06
Type: Zettel
aliases:
  - set
References:
  - Vector Calculus, Linear Algebra, and Differential Forms
Links:
  - "[[Intersection]]"
  - "[[Subset]]"
tags:
  - MATH31AH
---
> At the level at which we are working, set theory is a language, with a vocabulary consisting of seven words. In the late 1960's and early 1970's, under the sway of the "New Math," they were a standard part of the elementary school curriculum, and set theory was taught as a subject in its own right. This was a resounding failure, possibly because many teachers, understandably not knowing why set theory was being taught at all, made mountains out of molehills. Asa result the schools (elementary, middle, high) have often gone to the opposite extreme, and some have dropped the subject altogether.
- A set is a well defined collection of objects
- The seven vocabulary words are 
	- $\in$ : "is an element of"
	- $\{a|p(a)\}$: "the set of a such that p(a) is true"
	- $\subset$ : "is a [[subset]] of" (or equals, when $A \subset A$)
	- $\cap$ :   "[[Intersection]]", $A \cap B$ is the set of elements of both $A$ and $B$ 
	- $\cup$ : "union", $A \cup B$ is the set of elements of either $A$ or $B$ 
	- $\times$ : "cross", $A \times B$ is the set of pairs $(a,b)$ with $a \in A$ and $b \in B$
	- $-$ or $\setminus$ : "complement", $A - B$  is the set of elements in $A$ that are not in $B$
- One set has a standard name: the empty set $\emptyset$  
	- Others include
	- $\mathbb{N}$ : Natural numbers, (0,1,2,..) 
	- $\mathbb{Z}$ : Integers, (..., -1, 0, 1, ...)
	- $\mathbb{Q}$ : Rational numbers, $\frac{p}{q}$, with $p,q \in \mathbb{Z}, q\neq_{0}$
	- $\mathbb{R}$ : Real numbers, infinite decimals
	- $\mathbb{C}$ : Complex numbers, $\{a + ib |a,b\in\mathbb{R}\}$
- More examples of sets:
	- Algebraic numbers
		- $\{x \in \mathbb{C} : p(x)=0\}$
		- $\{x\in\mathbb{R}:p(x)=0$
		- Where p is a polynomial with integer or rational coefficients
	- $\{n|n \in \mathbb{N} \text{ and } n \text{ is even} \} = \{0,2,4,\dots\}$
		- Where the $|$ means "such that"
	- Expressions can be condensed
		- $\{x \in \mathbb{R}| x \text{ is a square }\}$ means $\{x|x \in \mathbb{R} \text{ and } x \text{ is a square }\}$
- We will use exponents to denote multiple products of sets
	- $A \times A \times \dots \times A$ with $n$ terms is denoted $A^n$: the set of $n$-tuples of elements of $A$
	- For examples, the two dimensional coordinate plane is denoted as $\mathbb{R}^2$, because it the set of coordinate pairs of two real numbers (something like $(\mathbb{R}, \mathbb{R})$)
> If this is all there is to set theory, what is the fuss about? For one thing, historically, mathematicians apparently did not think in terms of sets, and the introduction of set theory was part of a revolution at the end of the 19thcentury that included topology and measure theory. We explore another reason in Section 0.5, concerning infinite sets and Russell's paradox.
