---
Created: 2025-11-17
Type: Zettel
aliases:
References:
Links:
  - "[[Matrices]]"
  - "[[Matrix inverses]]"
tags:
  - MATH31AH
---
> Definition: Similar matrices. $A \in M_{n}(\mathbb{R})$ is called *similar* to $B \in M_{n}(\mathbb{R})$ if there exists an invertible matrix $Q$ such that $QAQ^{-1}=B$.
- We can think of $A,B$ as the same linear transformation written in two different bases
	- $Q$ is the matrix that converts coordinates from one basis to another
- When $A,B$ are similar they share the following:
	- [[determinant]]
	- [[Eigenvalues and eigenvectors|eigenvalues]]
	- characteristic polynomial
	- [[rank]]
> Proof: Similar matrices have the same determinant and characteristic polynomial
> Let $A$ be some linear transformation. A similar matrix $A_{1}=PAP^{-1}$ can be defined as followed.
> 