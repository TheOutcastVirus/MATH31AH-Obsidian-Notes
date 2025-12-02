---
Created: 2025-11-04
Type: Zettel
aliases:
References:
Links:
  - "[[Dot product]]"
tags:
  - MATH31AH
---
>**Proposition: Cauchy Schwarz Inequality.** Let $v,w \in \mathbb{R}^n$. Then, 
> 
$$
\lvert v \cdot w \rvert \leq \lVert v \rVert \lVert w \rVert 
$$
>With the equality holding only when $v =\lambda w$, for some $\lambda \in \mathbb{R}$
- In other words, the [[Dot product|dot product]] of two vectors will always be less than or equal to the magnitudes of the two vectors
	- The only case where they are equal is when the vectors are linearly dependent, or when the angle between them either 0 or 180.
> Remark: $|\langle v,w \rangle| \leq ||v||\cdot||w||$ implies that $\frac{|\langle v,w \rangle|}{||v|| \cdot ||w||} \leq 1$, meaning that $(v,w)\neq(0,0)$
> Therefore, $-1 \leq \frac{\langle v,w \rangle}{||v|| \cdot ||w||} \leq 1$
> Therefore, we can see that $\cos \theta = \frac{\langle v,w \rangle}{||v|| \cdot ||w||}$, where $\theta$ is the angle between the two vectors.  
- This remark relates to another definition of the dot product
	- We know the dot product can also be defined as: $v \cdot w = \lVert v \rVert \lVert w \rVert\cos \theta$, where $\theta$ is the angle between vectors
> Proof: Pick $v,w \in \mathbb{R}^n$. Consider:
> $\langle v-tw, v-tw \rangle$
> $=\langle v,v-tw \rangle+ \langle -tw,v-tw \rangle$
> $=\langle v,v-tw \rangle - t\langle w,v-tw \rangle$
> $=\langle v,w \rangle - t \langle v,w \rangle - t(\langle w,v \rangle-t\langle w,v \rangle)$
> $=||v||^2-t\langle v,w \rangle-t\langle w,v \rangle+t^{2}||w||^{2}$
> $=||v||^{2}-2t\langle v,w \rangle+t^{2}||w||^{2}$
> This is a quadratic equation in the variable $t$. 
> If $\{ v,w \}$ is [[Linear independence|linearly independent]], then $||v-tw||^{2} \geq 0$. This forces the discriminant of the polynomial $P(t)$  to be negative, meaning it has no solutions. 
> $(-2\langle v,w \rangle)^{2}-4 ||w||^{2}||v||^{2}$
> $=4|\langle v,w \rangle|^{2} - 4 ||v||^{2}||w||^{2} <0$
> $\implies |\langle v,w \rangle| < ||v||\cdot||w||$
> When $v$ is a scalar multiple of $w$, meaning that $v= \lambda w$ for some $\lambda \in \mathbb{R}$, then $P(t)=0$ has only one root: $\lambda$. This means the discriminant of $P$ is zero, so:
> $|\langle v,w \rangle|^{2} = ||v||^{2}\cdot||w||^{2}$
> $\implies |\langle v,w \rangle| = ||v||\cdot||w||$

