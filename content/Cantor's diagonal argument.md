---
Created: 2025-09-30
Type: Zettel
aliases:
References:
Links:
tags:
  - MATH31AH
  - Incomplete
---
- The goal for this is to show that there are[[ infinite sets]] that are uncountable 
	- By being [[Countable & uncountable sets|uncountable]], they can be shown to have a bijection with $\mathbb{N}$
- For this proof by inversion, we assume that$(0,1)$ is not uncountable. 
- Assume that$(0,1)$ is not uncountable. So, $(0,1)$ must be countable then. Since $(0,1)$ is countable, consider an enumeration of $(0,1)$. 
> Enumeration: Say you have some set $A = \{  \alpha, \dots \}$. To show that is is bijective to $\mathbb{N}$, you can list it in some infinite order $A=(a_{1}, a_{2},\dots)$, and $f(1)=a\to a_{1}$. This is called an enumeration.
- Now consider the decimal expansion of the elements as follows, where $\alpha_{1j} \in \{ 0,\dots 9 \}$ 
$$
a_{1} = 0.\alpha_{11} \alpha_{12} \alpha_{13}\dots
$$
$$
a_{2}=0. \alpha_{21} \alpha_{22}\alpha_{23}\dots
$$
$$
a_{3}=0. \alpha_{31} \alpha_{32}\alpha_{33}\dots
$$
$$
a_{k}=0. \alpha_{k1} \alpha_{k2}\alpha_{k3}\dots
$$
- Our goal is to find an element in $(0,1)$ whose decimal representation differs from all $\alpha_{k}$
- We need to find a $\beta=0.\beta_{1}\beta_{2}\beta_{3}\dots$ such that $\beta_{1}\neq\alpha_{11}$, $\beta_{2}\neq\alpha_{22}$, $\beta_{3}\neq\alpha_{33}$, etc.
