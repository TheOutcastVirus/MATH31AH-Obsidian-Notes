---
Created: 2025-08-22
Type: Zettel
aliases:
References:
Links:
  - "[[Vectors]]"
  - "[[Set Theory|set]]"
tags:
  - MATH31AH
---
- Virtually all of physics deals with fields.
	- Ex: electric and magnetic fields, gravitational and other force fields, wave functions, etc
- A field is something with data that varies from point to point
	- There are scalar fields that vary point to point
		- Ex: temperature of pressure distributions
	- Fields like the Newtonian gravitation field are best described by vector fields, which associate a [[Vectors|vector]] to each point 
		- Others, like the [[Electric field|electromagnetic field]] and charge distributions are best modeled by *form fields*
		- Some others, like the Einstein field of general relativity, are none of the above
- **Definition: Vector Field**. A vector field on $\mathbb{R}^n$ is a [[Functions|function]] whose input is a point in $\mathbb{R}^n$ and whose output is a vector (also in $\mathbb{R}^n$) emanating from that point. 
> ![[Vector fields-1755887585046.webp|192x375]]

- Vector fields are distinct from functions that return points
	- The identity function in $\mathbb{R}^n$,  $f \begin{pmatrix} x \\ y \end{pmatrix} = \begin{pmatrix} x \\ y \end{pmatrix}$ takes a point in $\mathbb{R}^n$ and returns the same point. But the *vector* *field*  $\vec{F}\begin{pmatrix} x \\ y \end{pmatrix} = \begin{bmatrix} x \\ y \end{bmatrix}$ takes a point in $\mathbb{R}^n$ and assigns it to a vector starting at that point.
- Vector fields are often used to describe the flow of fluids or gases; the vector assigned to each point describes the direction and velocity of the gas at a given point