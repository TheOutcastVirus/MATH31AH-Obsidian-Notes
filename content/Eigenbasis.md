---
Created: 2025-11-25
Type: Zettel
aliases:
References:
Links:
  - "[[Diagonalization]]"
tags:
  - MATH31AH
---
> Proposition: Let $\lambda_{1}, \lambda_{2},\dots,\lambda_{k}$ be two [[Eigenvalues and eigenvectors|eigenvectors]] of $A$, $\lambda_{1}\neq\lambda_{2}$, and $v_{1},v_{2}, \dots,v_{k}$ be two associated eigenvectors
> Then, $\{ v_{1},\dots,v_{k} \}$ are [[Linear independence|linearly independent]].
> Proof: 
> Consider for now, $c_{i}\in \mathbb{R}$
> $c_{1}v_{1}+\dots+c_{k}v_{k}=\vec{0}\in \mathbb{R}^n$
> $\implies A(c_{1}v_{1}+\dots+c_{k}v_{k})=\vec{0}\in \mathbb{R}^n$
> $=c_{1}Av_{1}+\dots+c_{k}Av_{k}=\vec{0}\in \mathbb{R}^n$
> $=c_{1}\lambda_{1}v_{1}+\dots+c_{k}\lambda_{k}v_{k}=0$
> 
> Proof by induction:
> By induction on $k$
> For $k=2$: $\{ v_{1},v_{2} \}$
> $c_{1}v_{1}+c_{2}v_{2}=0$
> $A(c_{1}v_{1}+c_{2}v_{2})=0$
> $c_{1}\lambda_{1}v_{1}+c_{2}\lambda_{2}v_{2}=0$
> $(T)x\lambda_{1} \implies c_{1}\lambda_{1}v_{1}+c_{2}\lambda_{1}v_{2}=0$
> TBA
## Algebraic and geometric multiplicity
- How many eigen values can a $n\times n$ matrix have?
	- Let $p(x)=a_{0}x^n+a_{1}x^{n-1}+\dots+a_{n}$
		- This is a polynomial with real entries
	- The fundamental theorem of algebra has $n$ complex zeros counted with multiplicity
- An eigenvalue $\lambda$ of $A$ can be a multiple zero of the characteristic polynomial
	- That multiplicity of $\lambda$ is called the *algebraic multiplicity* of $\lambda$
- Recall: The eigenspace of $\lambda$ is the [[Linear subspaces|subspace]] of all eigenvectors of $\lambda$
	- The dimension of this subspace is called the *geometric multiplicity* of $\lambda$
## Def. of Eigenbasis
> Definition: Eigenbasis.
> A basis of $\mathbb{R}^n$ is called an eigenbasis of $A\in M_{n}(\mathbb{R})$ if the [[basis]] vectors are eigenvectors of $A$
- What are the properties of an eigenbasis?
	- It can be used for [[diagonalization]]
## Main result 12/2/2025
> For $A\in M_{n}(\mathbb{R})$ the following are equivalent
> 1) $A$ is [[Diagonalization|diagonalizable]] 
> 2) Algebraic multiplicity is equal to the geometric multiplicity for all eigenvalues of $A$

> Proof: Let $A\in M_{n}(\mathbb{R})$, $\lambda$ an eigenvalue
> Then, geometric multiplicity of $\lambda \leq$ alg. multiplicity of $\lambda$  
> HW: 
> $A=\begin{bmatrix}aId_{m} & C \\ 0 & D \end{bmatrix}$, where $aId_{m}$ is $m \times m$, $C$ is $m \times n-m$, $0$ is $n-m \times n$, and $D$ is $n-m\times n-m$.
> Then, $\det(A-xId_{n})=(a-x)^n\det(D-xId_{n})$
> $x(A)=(a-x)^mx(D)$
> Proof cont.
> Suppose the eigenspace associated to $\lambda$ has dimension $m$.
> Let $\{ v_{1},\dots,v_{m} \}$ be a bass of this eigenspace. 
> Now, complete $\{ v_{1},\dots,v_{m} \}$ to a bass of $\mathbb{R}^n$ by considering a basis of $v_{\lambda}^\perp$. Say the basis is $\{ w_{1},\dots,w_{n-m} \}$. Note that $v_{\lambda} +v_{\lambda}^\perp=\mathbb{R}^n$.
> Define $S=\begin{bmatrix}v_{1} & v_{2} & \dots & v_{m} & w_{1} & \dots & w_{n-m}\end{bmatrix}_{n\times m}$
> and consider 
> $S^{-1}AS=S^{-1}A\begin{bmatrix}v_{1} & \dots & v_{m} & w_{1}\dots & w_{n-m}\end{bmatrix}$
> $=S^{-1}\begin{bmatrix}\lambda v_{1} & \lambda v_{2} & \dots & \lambda v_{m} & Aw_{1} & \dots & Aw_{n-m}\end{bmatrix}$
> Since $S^{-1}S=Id_{n}$
> $S^{-1}\begin{bmatrix}v_{1} & \dots & v_{2} & w_{1} & \dots & w_{n-m}\end{bmatrix}$
> $=\begin{bmatrix}S^{-1}v_{1} & \dots & S^{-1}v_{m} & S^{-1}w_{1} & \dots & S^{-1}w_{n-m}\end{bmatrix}$
> $=\begin{bmatrix}e_{1} & e_{2} & \dots & e_{m} &  \dots\end{bmatrix}$
> Coming back to the proof:
> $=\begin{bmatrix}\lambda e_{1} & \dots & \lambda e_{m} & S^{-1}Aw_{1} & \dots & A^{-1}Aw_{n-m}\end{bmatrix}$
> $\chi(S^{-1}AS)=\chi(A)$
> $=(\lambda-x)^m\chi(D)=\chi(A)$
> $=(\lambda-x)^{a_{i}}P(x)$
> Since $(\lambda-x)^m|\chi(A)$, $m \leq$ alg. mult. of $\lambda$
- Recall: $\chi(A)=\chi(S^{-1}AS)$
	- $\det(A-xId_{n})=\det(S^{-1}AS-xId_{n})$
	- $=\det(S^{-1}AS-xS^{-1}S)$
	- $=\det(S^{-1}(A-xId_{n})S)$
	- $=\det(S^{-1})\det(A-xId_{n})\det(S)$
	- $\det(A-Id_{n})$
	- This shows that [[Similar matrices]] have the same [[Eigenvalues and eigenvectors|characteristic polynomial]]
> Proof: 
> Case 1:
> $\det \{ v_{1},..,v_{n} \}$ be an eigenbasis of $\mathbb{R}^n$ associated to $A$.
> Define, $S=\begin{bmatrix}v_{1} & \dots & v_{n}\end{bmatrix}$
> Consider
> $S^{-1}AS$
> $=S^{-1}A\begin{bmatrix}v_{1} & v_{2} & \dots & v_{n}\end{bmatrix}$
> $=S^{-1}\begin{bmatrix}\lambda_{1} v_{1} & \lambda_{2} v_{2} & \dots & \lambda_{n}v_{n}\end{bmatrix}$
> $=\begin{bmatrix}\lambda_{1}S^{-1}v_{1} & \dots & \lambda_{n}S^{-1}v_{n}\end{bmatrix}$
> $=\begin{bmatrix}\lambda_{1}e_{1} & \dots & \lambda_{n}e_{n}\end{bmatrix}$
> Which is a diagonal matrix, so this case is proven.
> Case 2:
> Since $A$ is diagonalizable, there exists an invertible $S$ such that $S^{-1}AS$ is a diagonal matrix
> $S^{-1}AS=D=\begin{bmatrix}\lambda_{1} &  &  \\  & \lambda_{2} &  \\  &  &  & \lambda_{n}\end{bmatrix}$  
> $S^{-1}ASe_{k}=De_{k}=\lambda_{k}e_{k}$
> $\implies SS^{-1}ASe_{k}=S\lambda_{k}e_{k}=\lambda_{k}Se_{k}$
> $\implies ASe_{k}=\lambda_{k}Se_{k}$
> Therefore, $Se_{k}$ are eigenvectors associated with eigenvalue $\lambda_{k}$.
> Thus, $\{ Se_{k} : 1 \leq k \leq n \}$ is an eigenbasis of $\mathbb{R}^n$ associated to $A$
> Case 3
> Alg. mult. = geo. mult. for all eigenvalues 
> $\implies$sum of geo. mult. = $n$
> $\implies$ sum of all dim of eigenspaces = $n$
> $\implies$ There exists an eigenbasis
> Case 4:
> There exists an eigenbasis. This implies that the sum of dimension of eigenspace is equal to the sum of geo. mult. which is less that the sum of alg. mult. 
> Therefore, geo. mult. is equal to the alg. mult. for each eigenvalue. 

> Corollary: $A\in M_{n}(\mathbb{R})$ has $n$-distinct eigenvalues, then $A$ is diagonalizable.

> Corollary: Let $P(A)$ be a polynomial.
> $[P(A)=A^3+10A^{2}-20A^1+Id_{n}]$
> If $A$ is diagonalizable, then so is $P(A)$.
> Proof: There exists $S$ non-singular such that $S^{-1}AS$ is $\implies(S^{-1}AS)=(S^{-1}AS)(S^{-1}AS)(S^{-1}AS)=S^{-1}A^kS$
> Substituting this into our polynomial
> $P(S^{-1}AS)=S^{-1}A^3S+S^{-1}A^2A-20S^{-1}A^1S+Id_{n}$
> Therefore, $S^{-1}(A^3+10A^2-20A^1+Id_{n})S$
> $=SP(A)S$
> So, $P(A)$ is similar to the diagonal matrix $P(S^{-1}AS)$
> Hence, it is also diagonalizable

> Spectral theorem:
> Recall: $A\in M_{n}(\mathbb{R})$ is called symmetric if $A^T=A$
> $A\in M_{n}(\mathbb{C})$ is called *Hermitian* if $\bar{A}^T=A$
> $z=x+iy\implies \bar{z}=x-iy$
> Let $\left< , \right>$ denote the [[dot product]].
> $\left< v,Aw \right> = v^TAw$, $v,w\in \mathbb{R}^n$.
> $=\left< A^Tv,w \right>$
> $=(A^Tv)^Tw$
> $=v^T(A^T)^Tw=v^TAw$
> Therefore, $\left< v,Aw \right> = \left< A^Tv,w \right>$

> Proposition: Let $A\in M_{n}(\mathbb{C})$ is such that $\bar{A}^T=A$. Then,
> $A=(a_{ij})_{m,n}, \bar{A}=(\bar{a}_{ij})_{m,n}$
> All eigenvalues of $A$ are real numbers
> Proof: Let $\lambda$ be an eigenvector of $A$ with $v$ an associated eigenvector
> Now, $\left< \bar{A}^Tv,v \right> = \left< v,Av \right>$
> $\lambda \left< v,v \right> = \bar{\lambda}\left< v,v \right>$
> Therefore, $\lambda \lVert v \rVert^{2}=\lambda \lVert v \rVert^{2}$
> Therefore, $\lambda=\bar{\lambda}$, meaning that $\lambda$ is real.

> Proposition: Let $A\in M_{n}(\mathbb{R})$ and $v,w$ be eigenvectors of $A$ associated with $\lambda , \mu$ with with $\lambda\neq \mu$. Then, 
> $\left< v,w \right> = 0$
> Proof: $\left< A^Tv,w \right> = \left< v,Aw \right>$
> $\implies \left< Av,w \right> = \left< v,Aw \right>$
> $\implies \left< \lambda v,w \right> = \left< v,\mu w \right>$
> $\implies\lambda \left< v,w \right> = \mu \left< v,w \right>$
> $=(\lambda-\mu)\left< v,w \right> = 0$
> $\left< v,w \right> = 0$

> Definition: A matrix $A\in M_{n}(\mathbb{R})$ is said to have simple spectrum if all its eigenvalues are different.
> Lemma: Any symmetric matrix $A\in M_{n}(\mathbb{R})$ can be approximated by matrices with simple spectrum. 