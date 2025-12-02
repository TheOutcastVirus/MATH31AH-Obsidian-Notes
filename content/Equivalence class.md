---
Created: 2025-09-30
Type: Zettel
aliases:
References:
Links:
  - "[[Relation]]"
tags:
  - MATH31AH
---
> Example: In $\mathbb{N}$, $aRb$ if and only if $a\equiv bmod3$meaning that $a,b$ have the same remainder when dived by 3. (you can write this as $\frac{a-b}{3}$)
> 1. This relation is reflexive because for any $m \in \mathbb{N}$, $mRm$ since $\frac{m-m}{3}=0$
> 2. This relation is symmetric because for any $m,n \in \mathbb{N}$ with $mRn$ is the same as $\frac{m-n}{3}$ is the same as $\frac{n-m}{3}$ which is $nRm$
> 3. The property is transitive as for any $m,n,p \in \mathbb{N}$ with $mRn$, $nRp$, $\implies \frac{m-n}{3} \& \frac{n-p}{3}$ . Since $m-n+n-p =m-p$ is divisble by3. Therefore, this implies that $\frac{m-p}{3}$ and $mRp$
> The equivalence classes would be for this (the division by )
>$[1]:=\{ m \in \mathbb{N}:mR1 \} \to 3k+1, k \in \mathbb{N}$
>$[2]:=\{ m \in \mathbb{N}:mR2 \} \to 3k+2, k \in \mathbb{N}$
>$[3]:=\{ m \in \mathbb{N}:mR3 \} \to 3k, k \in \mathbb{N}$

> Definition: Let $A$ be a non-empty set equipped with an equivalence relation $R$. The equivalence classes of an element $a \in A$ is defined by $[a]$ and defined as: $[a]:=\{ b \in A: bRa \}$
- The reason we use equivalence relations is because you can divide the behaviors of elements in a set  