---
Created: 2025-11-04
Type: Zettel
aliases:
References:
  - https://en.wikipedia.org/wiki/Inner_product_space
Links:
  - "[[Vectors]]"
tags:
  - MATH31AH
---
> **Definition: Dot Product.** Let $v,w \in \mathbb{R}^n$ with $v = \begin{bmatrix} v_{1} \\ \vdots  \\ v_{n}\end{bmatrix}$ and $w = \begin{bmatrix}w_{1} \\ \vdots  \\  w_{n}\end{bmatrix}$, with $v_{n},w_{n} \in \mathbb{R}$. The dot product of $v$ and $w$ is denoted as $v \cdot w$ and is defined by $\begin{bmatrix}v_{1} & \dots & v_{n}\end{bmatrix}\begin{bmatrix}w_{1} \\ \vdots  \\ w_{n}\end{bmatrix} = v_{1}w_{1}+\dots+v_{n}w_{n}$ 
> So, dot product in $\mathbb{R}^n$ is a map $:\mathbb{R}^n \times \mathbb{R}^n \to \mathbb{R}$ 
- The geometric interpretation of the dot product is that it shows [[orthogonality]] between vectors in $\mathbb{R}^n$
	- When two vectors are orthogonal, the dot product will be zero
	- When they are aligned, it will be equal to the product of their magnitudes
- The computation of the dot product is very simple
	- simply line up the components, multiply, and sum
- Length relates to dot product in the following way (note that $\left< , \right>$ is another notation for the dot product)
	-  $v \cdot v= \langle v,v \rangle = || v ||^2$. We know that $||v||$ is the length of $v$
## Bilinearity
> **Definition: Bilinear map.** A map of $f:\mathbb{R}^n \times \mathbb{R}^n \to \mathbb{R}$ is called bilinear if $f$ is [[Linear transformations|linear map]] in one component when the other component is fixed.
> $f:(v,w)\mapsto f(v,w)$
> $f:(v_{0}, \cdot) \mapsto f(v_{0}, \cdot)$
> $f(v_{1},\lambda w_{1}+w_{2}) = \lambda f(v_{1},w_{1}) + f(v_{1},w_{2})$ 
- Essentially, this is saying that the map acts linear for one component at a time
	- Meaning that the map is consistent under scalar multiplication and addition when one of the values is held constant
> Example: Bilinearity for the dot product in 
> $\langle , \rangle:\mathbb{R}^n \times \mathbb{R}^n \to \mathbb{R}$ and $v_{0} \in \mathbb{R}^n$ 
> Then, $\langle v_{0}, \rangle:\mathbb{R}^n \to \mathbb{R}$ is linear (as the fist element is fixed to $v_{0}$)
> $\langle ,v_{0} \rangle:\mathbb{R}^n \to \mathbb{R}$ is also linear.
## Inner product
> Example: $v,w \in \mathbb{R}^n$
> $\begin{bmatrix}v_{1} & v_{2}\end{bmatrix}\begin{bmatrix}1 & 0 \\ 0 & 1\end{bmatrix}\begin{bmatrix}w_{1} \\ w_{2}\end{bmatrix}$
> $= v_{1}w_{2}+v_{2}w_{2}$
> Say instead of $I$, we have
> $\begin{bmatrix}v_{1} & v_{2}\end{bmatrix}\begin{bmatrix}1 & 0 \\ 0 & 2\end{bmatrix}\begin{bmatrix}w_{1} \\ w_{2}\end{bmatrix}$
> This would be similar to dot product, but a bit scaled in one of the axes
- This introduces the idea of the *inner product*, a concept that is introduced in class but not fully developed
	- [From Wikipedia](https://en.wikipedia.org/wiki/Inner_product_space):  Inner products allow formal definitions of intuitive geometric notions, such as lengths, angles, and orthogonality (zero inner product) of vectors
> Remark: Inner product in $\mathbb{R}^n$. All dot products are a class of inner products. All inner products are bilinear, but not all bilinear maps are inner products.
 
> Remark: There are a class of matrices called positive definite matrices. If $A \in M_{2}(\mathbb{R})$ is positive definite, then $\begin{bmatrix}v_{1} & v_{2}\end{bmatrix}A\begin{bmatrix}w_{1} \\ w_{2}\end{bmatrix}$ defines an inner product and after a choice of basis, all inner products are of this above form. 
> Positive definite means that for $v^TAv \geq 0$ and $v^TAv = 0$ only if $v = \vec{0} \in \mathbb{R}^n$.