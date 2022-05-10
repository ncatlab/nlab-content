+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
#### Super-Algebra and Super-Geometry
+-- {: .hide}
[[!include supergeometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea 

A non-associative version of a [[geometric algebra]]. 

## Definition

Given a [[commutative ring]] $R$, a **non-associative geometric algebra** is an [[N-graded module|$\mathbb{N}$-graded]] $R$-[[module]] $A$ with a [[bilinear function]] $(-)(-):A \times A \to A$ and a ring [[isomorphism]] $j:\langle A \rangle_0 \cong R$ such that 

* for natural numbers $m:\mathbb{N}$ and $n:\mathbb{N}$, the product of every $m$-multivector and $n$-multivector is an $(m+n)$-multivector: for all $a \in \vert A \vert_m$ and $b \in \vert A \vert_n$, there exists $c \in \vert A \vert_{m+n}$ such that $a b = c$

* the product of every $1$-vector with itself is a $0$-vector: for all $a \in \langle A \rangle_1$ there exists $c \in \langle A \rangle_0$ such that $a^2 = c$. 

Due to the ring isomorphism $j$ and the linearity of the grade projection operation, the algebra is [[unital magma|unital]]. 

## See also

* [[geometric algebra]]

* [[N-graded module]]