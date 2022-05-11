[[!redirects super commutative monoids]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Super-Algebra and Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
#### Monoid theory
+-- {: .hide}
[[!include monoid theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea ##

A $\mathbb{Z}/2\mathbb{Z}$-[[graded object|graded]] [[commutative monoid]]. 

## Definition ##

An **super commutative monoid** is a [[commutative monoid]] $M$ with decomposition functions $\mathcal{D}_0:M \to M$ and $\mathcal{D}_1:M \to M$, such that 

* for all $a:M$, $a = \mathcal{D}_0(a) + \mathcal{D}_1(a)$
* $\mathcal{D}_0(0) = 0$
* for all $a:M$, and $b:M$, $\mathcal{D}_0(a + b) = \mathcal{D}_0(a) + \mathcal{D}_0(b)$
* $\mathcal{D}_1(0) = 0$
* for all $a:M$, and $b:M$, $\mathcal{D}_1(a + b) = \mathcal{D}_1(a) + \mathcal{D}_1(b)$
* for all $a:M$, $\mathcal{D}_0(\mathcal{D}_0(a)) = \mathcal{D}_0(a)$
* for all $a:M$, $\mathcal{D}_0(\mathcal{D}_1(a)) = 0$
* for all $a:M$, $\mathcal{D}_1(\mathcal{D}_0(a)) = 0$
* for all $a:M$, $\mathcal{D}_1(\mathcal{D}_1(a)) = \mathcal{D}_1(a)$

As a result, the [[image]] of the two decompostion functions $\im(\mathcal{D}_0)$ and $\im(\mathcal{D}_1)$ are commutative monoids and there exists a [[monoid]] [[isomorphism]] $i:V \cong \im(\mathcal{D}_0) \otimes \im(\mathcal{D}_1)$, where $A \otimes B$ is the [[tensor product of commutative monoids]]. 

The elements of $\im(\mathcal{D}_0)$ are called **even elements** or **bosonic elements**, and the elements of $\im(\mathcal{D}_1)$ are called **odd elements** or **fermionic elements**. 

## See also ##

* [[commutative monoid]]

* [[graded commutative monoid]]

* [[super abelian group]]