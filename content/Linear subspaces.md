---
Created: 2025-10-07
Type: Zettel
aliases:
  - subspace
References:
Links:
  - "[[Vectors]]"
tags:
  - MATH31AH
---
- Goal: study properties of the model space ($\mathbb{R}^n$, the Euclidean space)
	- Understand the definition of vector spaces 
- $\mathbb{R}$ is the [[Set Theory|set]] of all real numbers
	- we can add two real numbers $a,b$ and if we add or subtract them, they are still real numbers
		- This means real numbers are *closed* under addition
	- Same thing for $a,b \to a \cdot b$ , real numbers are closed under scalar multiplication
- $\mathbb{R}^2$ is the set of all ordered pairs: $\{ (a,b) : a,b \in \mathbb{R} \}$
	- We can think of $(a,b)$ as a point 
		- We could think of this as an absolute position on the space
	- Or, we can think of $(a,b)$ as a [[Vectors|vector]].
		- Instead, we think of it as a translation
		- It has a magnitude and direction
- Points cannot be added, but vectors can
	- Under the definitions for vector addition and subtraction, we can say that $\mathbb{R}^2$ is closed under vector addition
- $\mathbb{R}^n:=\{ (a_{1},a_{2},\dots,a_{n}): a_{i} \in \mathbb{R} \}$
	- Vector addition and subtraction is defined in the exact same way in $\mathbb{R}^n$
	- $\mathbb{R}^n$ is closed under vector addition and subtraction for any $n$
	- This property is not unique for a finite $n$, it works for when $n$ is infinite as well
		- say $S := \{ (a_{1}, a_{2},a_{3},\dots) : a_{i} \in \mathbb{R}, i \in \mathbb{N} \}$
		- $S$ is still closed under addition
		- $S$ is the space of all "sequences" of real numbers
- $\mathbb{R}^2$, as well as $\mathbb{R}^n$ are closed under scalar multiplication as well
- $S$ is also closed under scalar multiplication
	- say $\vec{\alpha}=\begin{bmatrix}a_{1} \\ a_{2} \\ \dots \end{bmatrix}$, multiplying it by some $r$ would be $r\vec{\alpha}=\begin{bmatrix}ra_{1} \\ ra_{2} \\ \dots \end{bmatrix}$
- There are subsets of $\mathbb{R}^n$, $S \subset \mathbb{R}^n$
	- For example: $\{ \vec{\alpha} \in \mathbb{R}^n: x_{1} = 0\} \subset \mathbb{R}^n$
		- This would be the $(n-1)$-plane
	- The set $\{ \vec{\alpha} \in \mathbb{R}n=^n : x_{1}=0,x_{2} =1, x_{3}=5,\dots \}$ would define a line
- Other subsets include:
	- $\mathbb{Q}^n \subset \mathbb{R}^n$
	- This is the unit  (n-1) sphere in $\mathbb{R}^n$: $S^n-1:= \{ (x_{1},\dots,x_{n}) \in \mathbb{R}^n: x_{1}^2+x_{2}^2+\dots+x_{n}^2=1 \}$
		- In $\mathbb{R}$, this would be a two points at 1 and -1.
		- In $\mathbb{R}^2$, this would be the 2d unit circle that we know: $\{ \vec{x} \in \mathbb{R}^2 : x_{1}^2+x_{2}^2=1 \}$
			- We denote this as $S^1 \in \mathbb{R}^2$ 
			- This is a 1 dimensional object, even though it seems like 2 dimensions. This is because at one point, you can only back and forward
			- If you take the tangent to the circle, you get a line
		- In $\mathbb{R}^3$, we get an actual sphere $S^2 \subset \mathbb{R}^3$ 
			- This is a 2 dimensional object, because when you zoom in on the surface, it is flat like a plane
			- Think about a tangent plane to the sphere
			- ![[image-18.webp|591x363]]
> Note: $\mathbb{R}$ is NOT a subset of $\mathbb{R}^n$ or $\mathbb{R}^2$, because they contain tuples of different lengths. As a result, no real number is in the set of tuples, and no 2-tuple is in the set of 2 tuples, and so on so forth. 
>**Definition: Subspaces.** A subspace of $\mathbb{R}^n$ is a subset of $S$ with the property:
>1. if $\vec{x},\vec{y} \in S$, then $\vec{x}+\vec{y}\in S$
>2. if $a \in R$ then $a \vec{x} \in S$
- Let $S \subset \mathbb{R}^n$ be a subspace
	- We know that $0 \in S$
	- $\mathbb{R}^n \subset \mathbb{R}^n$, $\mathbb{R}^n$ is a subspace of itself
	- These two examples are trivial subspaces of $\mathbb{R}^n$
> Non-example: Circle: $S^1 =\{ x_{1}^2 + x_{2}^2 =1 \}$. If we add two elements from this, $(1,0), (0,1)$, we get $(1,1)$, which is not in $S^1$
### Midterm review
> What is the smallest subspace that contains subspaces $S_{1},S_{2}$? it is called $\tilde{S}$. 
> It is the smallest if $V \subset \mathbb{R}^n$ is a subspace containing $S_{1},S_{2}$ them $V$ also contains $\tilde{S}$.
> $\tilde{S}=S_{1}+S_{2} := \{ \vec{v}+\vec{w} : \vec{v} \in S_{1}, \vec{w} \in S_{2} \}$. 
> Pick $\vec{v}_{1}, \vec{v}_{2} \in S_{1} + S_{2}$. 
> $\vec{v}_{1} = \vec{v}_{11} + \vec{w}_{11}$, where $\vec{v}_{11} \in S_{1}, \vec{w}_{11} \in S_{2}$. 
> $\vec{v}_{2} = \vec{v}_{21}+\vec{w}_{21}$, where $\vec{v}_{21} \in S_{1}, \vec{w}_{21} \in S_{2}$
> For any $\alpha,\beta \in \mathbb{R}$, $\alpha \vec{v}_{1} + \beta \vec{v}_{2}$. Expand this as 
> $\alpha \vec{v}_{11}+\alpha \vec{w}_{11} + \beta \vec{v}_{21} + \beta \vec{w}_{21}$ 
> We know that we can group them like this to see that the sums of the elements are contained by $S_{1},S_{2}$.
> $(\alpha \vec{v}_{11}+\beta \vec{v}_{21}) \in S_{1} + (\alpha \vec{w}_{11}+\beta \vec{w}_{21})\in S_{2} \in S_{1}+S_{2}$
> We know that $S_{1}+S_{2}$ is the smallest subspace containing $S_{1}$ and $S_{2}$. 
> Say that we have some $V \subset \mathbb{R}^n$ is a subspace with $S_{1} \subset V$ and $S_{2} \subset V$ . 
> Pick, $\vec{v}_{1} + \vec{w}_{1} \in S_{1} + S_{2}$.
> Since $\vec{v}_{1},\vec{w}_{1} \in V \implies \vec{v}_{1} + \vec{w}_{1} \in V$
> Therefore, $S_{1}+S_{2} \subset V$

> Say that $L(S_{1} \subset S_{2}) = S_{1} + S_{2}$
> $L(S_{1} \cup S_{2}) \subset S_{1} + S_{2}$ and $S_{1} +S_{2}  \subset L(S_{1} \cup S_{2})$
> Pick some $\vec{v} \in L(S_{1} \cup S_{2})$
> $\vec{v} = \alpha_{1}\vec{v}_{1}+\dots+\alpha_{k}\vec{v}_{k} \in S + \beta_{1}\vec{w}_{1}+\dots+\beta_{k}+\vec{w}_{k} \in S_{2},\in S_{1}+S_{2}$
> $\vec{v}_{i} \in S_{1}, \vec{w}_{i} \in S_{2}, \alpha_{i}, \beta_{i} \in \mathbb{R}$.
> Pick $\vec{v} \in S_{1}+S_{2}$
> Then$\vec{v}=\vec{v}_{1}+\vec{w}_{1}, \vec{v}_{1} \in S,\vec{w}_{1} \in S_{2} \subset S_{1} \cup S_{2}$
> Therefore, $\vec{v} \in L(S_{1} \cup S_{2})$

