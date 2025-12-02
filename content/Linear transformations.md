---
Created: 2025-10-16
Type: Zettel
aliases:
  - linear map
References:
Links:
tags:
  - MATH31AH
---
- Linear transformations are also know as *linear maps*
- When are working with vector spaces, linear maps are a fundamental tool to study them
	- Many natural operations such as rotation, scaling, etc. are linear maps
> **Definition: Linear map**. A map $T : \mathbb{R}^n \to \mathbb{R}^m$ is called a linear map (or a linear transformation) if:
> $T(\alpha \vec{v} + \beta \vec{w}) = \alpha T(\vec{v}) + \beta T (\vec{w})$
> $T(\vec{v}+\vec{w}) = T(\vec{v})+T(\vec{w})$
> $T(\alpha \vec{v}) = \alpha T(\vec{v})$
> Where $\vec{v}, \vec{w} \in \mathbb{R}^n, \alpha,\beta \in \mathbb{R}$
- Examples:
	- $T:\mathbb{R}^n \to \mathbb{R}^m$ as $T(\vec{v})= \vec{0} \in \mathbb{R}^m$
		- This is called the trivial map
	- $T:\mathbb{R}^n \to \mathbb{R}^n$ as $T(\vec{v}) = \vec{v}$ called the identity map. 
- We want to show that the identity map is actually a linear map
	- pick $\vec{v},\vec{w} \in \mathbb{R}^n, \alpha, \beta \in \mathbb{R}$
	- Consider $T(\alpha \vec{v} + \beta \vec{w})$
		- $= \alpha \vec{v} +\beta \vec{w} = \alpha T(\vec{v}) + \beta T(\vec{w})$
	- So we know that this is actually a linear transformation
## Basic transformations
- Say that we have some transform $T: \mathbb{R}^n \to \mathbb{R}^m$
	- Suppose that $n < m$
		- $(x_{1},x_{2} ,\dots,x_{n}) \to (y_{1},y_{2},\dots,y_{n}, y_{n+1},\dots y_{m})$
	- Since the input and outputs have different dimensions, there is no identity map, so we want something similar
	- We can define a transformation $(x_{1},x_{2},\dots x_{n}) \to (x_{1}, x_{2}, \dots, x_{n},0,\dots_{0})$
		- This is called the *inclusion map*. 
		- This just maps all the new dimensions as 0
- Say that we have some transform $T: \mathbb{R}^n \to \mathbb{R}^m$, 
	- Suppose that $n > m$
		- $(x_{1},x_{2},\dots,x_{m},x_{m+1},\dots,x_{n}) \to (y_{1},y_{2},\dots,y_{m})$
	- We can define a map $(x_{1},x_{2},\dots,x_{m},x_{m+1},\dots,x_{n}) \to (x_{1}x_{2},\dots x_{m})$
	- This is called a projection map
- These are the only non-degenerate maps for when the dimensions do not match
	- A degenerate transformation is one that loses information when scaling down in dimension
> Remark: $T:\mathbb{R}^n \to \mathbb{R}^n$. We have sets of basis vectors $\{ \vec{b}_{1},\dots,\vec{b}_{n} \}$ and the image $\{ \vec{r}_{1},\dots \vec{r}_{n} \}$. We have some map $\vec{b}_{i} \mapsto \vec{r}_{i}$. This is defined for basis vectors only. We want to *extend the map linearly* to all of $\mathbb{R}^n$. 
> Pick some vector $\vec{v} \in \mathbb{R}^n$, $\vec{v} = \alpha_{1} \vec{b}_{1}+\dots+ \alpha_{n}\vec{b}_{n} \implies T(\vec{v}) = \alpha_{1}T(\vec{b}_{1})+\dots+\alpha_{n}T(\vec{b}_{n})$ . Since we know the transform for just the basis vectors, but since the transform holds the properties to be transform, we can plug in any $\vec{v}$ (which is just composed of basis vectors) into the transform and know the result. 

> Remark: For any linear $T: \mathbb{R}^n \to \mathbb{R}^m$, the image of $T$ on a basis determines $T$. That is, if $B = \{ \vec{b}_{1}, \dots,\vec{b}_{n} \}$ is a basis and $T(B):= \{  T(\vec{b}_{i}): 1 \leq i \leq n \}$ it is known that $T$ is determined.
- Scaling: say we have $T: \mathbb{R}^2 \to \mathbb{R}^2$. Our $\{ \vec{e}_{1}, \vec{e}_{2} \}$, $T : \vec{e}_{1} \mapsto 2\vec{e}_{1}, \vec{e}_{2} \mapsto \vec{e}_{2}$
	- This would scale any set by double only on the x-axis
- Left multiplication by a matrix: 
	- $T: \mathbb{R}^n \to \mathbb{R}^m, A \in M_{m \times n}(\mathbb{R})$
	- $T: \vec{v} \mapsto A\vec{v}$
	- $A =  \begin{bmatrix}a_{11} & \dots & a_{im} \\ \vdots \\ a_{m1}  & \dots & a_{mn}\end{bmatrix}\begin{bmatrix}v_{1} \\ v_{2} \\ \vdots \\ v_{n}\end{bmatrix}$
	- Pick $\vec{v}, \vec{w} \in \mathbb{R}^n$ and $\alpha,\beta \in \mathbb{R}$
		- Consider $T(\alpha \vec{v}+\beta \vec{w}) = A(\alpha \vec{v}+\beta \vec{w})$
		- $=A(\alpha \vec{v}) + A(\beta \vec{w})$
		- $=\alpha A(\vec{v}) + \beta A(\vec{b})$
		- $=\alpha T(\vec{v})+\beta T(\vec{w})$
- Say we have a map $T:\mathbb{R}^n \to \mathbb{R}^m$, the set $\{ \vec{e}_{1},\dots \vec{e}_{n} \}$
	- $T(\vec{v}) = T(v_{1}\vec{e}_{1}+b_{2}\vec{e}_{2}+\dots+b_{n}\vec{e}_{n})$
		- $=b_{1}T(\vec{e}_{1})+ \dots b_{n}T(\vec{e}_{n})$
	- $T(\vec{e}_{1}) \in \mathbb{R}^n$, this a $m \times 1$ vector
	- We can write this as $\begin{bmatrix}T(\vec{e}_{1}) & T(\vec{e}_{2}) & \dots & T(\vec{e}_{n})\end{bmatrix} \in M_{m \times n}(\mathbb{R})$ 
	- So you can write this as the vector of the transforms of the vectors multiplied by the coordinates of the vector
		- $\begin{bmatrix}T(\vec{e}_{1}) & T(\vec{e}_{2}) & \dots & T(\vec{e}_{n})\end{bmatrix} \begin{bmatrix} b_{1} \\ b_{2} \\ \vdots \\ b_{n}\end{bmatrix}$
	- This is a very important example
	- This proves that all linear maps are essentially left multiplication by a matrix 
## Compositions
- We want to prove that the compositions of linear maps are linear
	- Suppose that we have $T: \mathbb{R}^n \to \mathbb{R}^m$
		- Say that we have a second map $S: \mathbb{R}^m \to \mathbb{R}^l$
		- $S \cdot T: \mathbb{R}^n -. \mathbb{R}^l$ is also linear 
	- We can compose linear maps by multiplying them 
		- $\begin{bmatrix} S \circ T\end{bmatrix} = [S] [T]$
>Proof: Prove the above. 
> $=S \circ T (\alpha \vec{u} + \beta \vec{v})$
> $=S(\alpha T(\vec{u})+\beta T(\vec{v}))$
> $=\alpha S(T(u\vec{u}))+\beta S(T(\vec{v}))$
> Where $\alpha,\beta \in \mathbb{R}, \vec{u},\vec{v} \in \mathbb{R}^n$
> Pick $\vec{u} = u_{1} \vec{e}_{1} + \dots u_{n}\vec{e}_{n}$
> $S(T(\vec{u})) = S(u_{1}T(\vec{e}_{1})+\dots+u_{n}T(\vec{e}_{n}))$
> $T(\vec{e}_{1}) = t_{11}\vec{e}_{1}+\dots+t_{1m}\vec{e}_{m} \in \mathbb{R}^n$
> $\vdots$
> $T(e_{k}) = t_{k_{1}}\vec{e}_{1}+\dots+t_{km} \vec{e}_{m}$
> Going back to our composition: $ST(\vec{u})= \begin{bmatrix}ST\end{bmatrix}\begin{bmatrix}u_{1} \\ \dots \\ u_{m}\end{bmatrix}$
> $S(T(\vec{u})) = S(u_{1}(t_{11}\vec{e}_{1}+\dots+t_{1m}\vec{e}_{m}) +\dots+ u_{n}(t_{n1}+\dots+t_{nm}\vec{e}_{m}))$
> $=S\left( \sum_{k=1}^n u_{k} t_{k_{1}} \vec{e}_{1} +\dots+ \sum_{k=1}^n  u_{k} t_{km} \vec{e}_{m}\right)$
> $\begin{bmatrix}S(\vec{e}_{1})  & \dots& S(\vec{e}_{m})\end{bmatrix}\begin{bmatrix}\sum u_{k} t_{k_{1}} \\ \vdots \\ \sum u_{k}t_{km}\end{bmatrix}$
> We know enough to show that $\begin{bmatrix}\sum u_{k} t_{k_{1}} \\ \vdots \\ \sum u_{k}t_{km}\end{bmatrix} = \begin{bmatrix}T(\vec{e}_{1}) & \dots & T(\vec{e}_{n})\end{bmatrix}\begin{bmatrix}u_{1} \\ \vdots \\ u_{n}\end{bmatrix}$
> As such, we know that $[S][T]$ is a composition.
## Associated matrices
- Associated matrices are the matrices that when you multiply another vector, they transform them according to the transformation.
> Example: Finding the matrix for the scaling linear transformation
> We have the map $T: \mathbb{R}^2 \to \mathbb{R}^2, \{ \vec{e}_{1},\vec{e}_{2} \}$. We defined $T: \vec{e}_{1} \mapsto 2\vec{e}_{1}, \vec{e}_{2} \mapsto \vec{e}_{2}$
> We know that $T(\begin{bmatrix}x \\ y\end{bmatrix}) = x T(\vec{e}_{1}) + yT(\vec{e}_{2}) = 2x\vec{e}_{1}+y\vec{e}_{2} = \begin{bmatrix}2x \\ y\end{bmatrix}$

> Example: Rotation, we define as $\theta: \mathbb{R}^2 \to \mathbb{R}^2$
> $e^{i\theta} = \cos \theta + i \sin \theta$. We can also write $z=x+iy=\begin{bmatrix}x \\ y\end{bmatrix}$
> $e^{i\theta}z=e^{i\theta}(x+iy)= (\cos \theta + i \sin \theta)(x+iy)$
> $= (x\cos \theta - y\sin \theta)+ i(x\sin \theta + y \cos \theta)$
> $e^{i\theta}z \leftrightarrow \begin{bmatrix}x\cos \theta- y\sin \theta \\ x\sin \theta + y \cos \theta\end{bmatrix}$
> $\theta: \begin{bmatrix}x \\ y \end{bmatrix} = \begin{bmatrix} x \cos \theta - y \sin \theta  \\ x \sin \theta + y\cos \theta\end{bmatrix}$
> The associated matrix for this transform is: $\begin{bmatrix}\theta(\vec{e}_{1}) & \theta (\vec{e}_{2})\end{bmatrix}$
> $\begin{bmatrix}\cos \theta & -\sin \theta \\ \sin \theta & \cos \theta\end{bmatrix} =  \begin{bmatrix}\theta\end{bmatrix}$
- Suppose we have  map $T: \mathbb{R}^n \to \mathbb{R}^m$ that is linear
	- Suppose that it has basis $B_{n}$ which is the [[basis]] of $\mathbb{R}^n$
		- $B_{n} = \{ \vec{v}_{1},\dots,\vec{_{n}} \}$
	- Say that there is a basis $C_{m}$ which is the basis of $\mathbb{R}^m$
		- $C_{m} = \{ \vec{w}_{1},..,\vec{w}_{n} \}$
	- Pick some element $\vec{u} \in \mathbb{R}^n, T(\vec{u}) \in \mathbb{R}^m$
		- When plugged into the transform, $T(\vec{u}) = T(\alpha_{1} \vec{v}_{1}+\dots+\alpha_{n}\vec{v}_{n})$
			- We are not working with the vector itself, but its elements with respect to its basis
			- This becomes unclear when working with the standard basis
		- Since we are changing the basis to $C_{m}$, the transform of $T(\vec{u})$ is the coordinate with respect to the new basis $C_{m}$
	- To summarize: $T: \mathbb{R}^n \to \mathbb{R}^m$, where $\mathbb{R}^n$ has basis $B_{n}$, and $\mathbb{R}^m$ has basis $C_{m}$
		- $T(\vec{u}) =  \begin{bmatrix}[T(\vec{v}_{1})]_{C_{m}} & [T(\vec{v}_{n})]_{C_{m}}\end{bmatrix} \begin{bmatrix}\vec{u}\end{bmatrix}_{B_{n}}$
> **Definition: Linear isomorphism.** A linear map $T:\mathbb{R}^n \to \mathbb{R}^n$ is called [[Matrix inverses|invertible]] or a linear isomorphism if there exists another linear map $S: \mathbb{R}^n \to \mathbb{R}^n$ such that $S \circ T = T \circ S: Id : \mathbb{R}^n \to \mathbb{R}^n$
> Corollary: Let $T:\mathbb{R}^n \to \mathbb{R}^n$m be a linear isomorphism. Then, $[T^{-1}] = [T]^{-1}$
> Remark: $Id: \mathbb{R}^n \to \mathbb{R}^n, \vec{u} \mapsto \vec{u}$. This transform is the same as the identity matrix

### Midterm review
> $T(\vec{x}) = T(x_{1}\vec{e}_{1} +\dots+x_{n}\vec{e}_{n})$, where $[\vec{x}]_{\epsilon_{n}} = \begin{bmatrix}x_{1} \\ x_{2} \\ \vdots \\ x_{n}\end{bmatrix}$
> $= x_{1}T(\vec{e}_{1})+\dots+x_{n}T(\vec{e}_{n})$
> $= \begin{bmatrix}T(\vec{e}_{1}) & \dots & T(\vec{e}_{n})\end{bmatrix} \begin{bmatrix}x_{1} \\ x_{2} \\ \vdots \\ x_{n}\end{bmatrix}$
> Let $T:\mathbb{R} \to \mathbb{R}$
> We can have $\epsilon_{1} =\{ 1 \}$. This means the coordinate representation of $[\vec{x}]_{\epsilon_{1}} = [x]$
> This means that $T(\vec{v}) = T(x \vec{1}) =x T(\vec{1})$
> We can also write this in a form $T(\vec{x}) = \alpha x$. We can say that $\alpha = T(\vec{1})$. Here, $\alpha$ is our "associated matrix", but in scalar form.


> Suppose that there exists $x \in \mathbb{R}\setminus \{ 0 \}$ such that $T(x) \neq 0$. What is $\ker T$?
> We know that $\ker T = \{ \vec{0} \}$. 
> Let, $x_{0}\neq_{0}$ be such that $T(x_{0})\neq_{0}$. 
> Pick $x \in \mathbb{R}. T(x) =T\left( \frac{x}{x_{0}} \cdot x_{0} \right)$
> This implies that for all $x \in \mathbb{R} \setminus \{ 0 \}$ that this $=\frac{x}{x_{0}}T(x_{0})$ and that $T(x) \neq 0$

> Say that we have $T:\mathbb{R}^2 \to \mathbb{R}^2$ is a linear transform
> $T(\begin{bmatrix}1 \\ 0\end{bmatrix}) = \begin{bmatrix}1 \\ 1\end{bmatrix}$
> $T(\begin{bmatrix}1 \\ 1\end{bmatrix}) = \begin{bmatrix}1 \\ -1\end{bmatrix}$
> $T(\begin{bmatrix}x \\ y\end{bmatrix}) = ?$
> 