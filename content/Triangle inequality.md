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
> **Proposition: Triangle inequality.** Let $v,w \in \mathbb{R}^n$
> Then, $\lVert v+w \rVert \leq \lVert v \rVert + \lVert w \rVert$
> Proof:
> $\lVert v+w \rVert^{2} - \langle v+w,v+w \rangle$
> $=\langle v,v+w \rangle + \langle w, v+w \rangle$
> $=\langle v,v \rangle+\langle v,w \rangle+\langle w,v \rangle+\langle w,w \rangle$
> $\leq\lVert v \rVert^{2}+2\lvert \langle v,w \rangle \rvert+\lVert w \rVert^{2}$, where with the [[Cauchy Schwarz Inequality]], we can rewrite this as:
> $\leq \lVert v \rVert^{2} + 2 \lVert v \rVert\lVert w \rVert + \lVert w \rVert^{2}$
> $=(\lVert n \rVert + \lVert w \rVert)^{2}$
> $\implies \lVert v+w \rVert^{2} \leq (\lVert v \rVert+\lVert w \rVert)^{2}$
> $\implies \lVert v+w \rVert \leq (\lVert v \rVert+\lVert w \rVert)$
