[[!redirects super abelian groups]]

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
#### Group theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea ##

A super abelian group is an $\mathbb{Z}$-[[super module]], or a $\mathbb{Z}/2\mathbb{Z}$-graded [[abelian group]]. 

## Definition ##

An **super abelian group** is an [[abelian group]] $G$ with decomposition functions $\mathcal{D}_0:G \to G$ and $\mathcal{D}_1:G \to G$, such that 

* for all $a:G$, $a = \mathcal{D}_0(a) + \mathcal{D}_1(a)$
* for all $a:G$, and $b:G$, $\mathcal{D}_0(a + b) = \mathcal{D}_0(a) + \mathcal{D}_0(b)$
* for all $a:G$, and $b:G$, $\mathcal{D}_1(a + b) = \mathcal{D}_1(a) + \mathcal{D}_1(b)$
* for all $a:G$, $\mathcal{D}_0(\mathcal{D}_0(a)) = \mathcal{D}_0(a)$
* for all $a:G$, $\mathcal{D}_0(\mathcal{D}_1(a)) = 0$
* for all $a:G$, $\mathcal{D}_1(\mathcal{D}_0(a)) = 0$
* for all $a:G$, $\mathcal{D}_1(\mathcal{D}_1(a)) = \mathcal{D}_1(a)$

As a result, the [[image]] of the two decompostion functions $\im(\mathcal{D}_0)$ and $\im(\mathcal{D}_1)$ are abelian groups and there exists a [[group]] [[isomorphism]] $i:V \cong \im(\mathcal{D}_0) \otimes \im(\mathcal{D}_1)$, where $A \otimes B$ is the [[tensor product of abelian groups]].  

The elements of $\im(\mathcal{D}_0)$ are called **even elements** or **bosonic elements**, and the elements of $\im(\mathcal{D}_1)$ are called **odd elements** or **fermionic elements**. 

## See also ##

* [[abelian group]]

* [[graded abelian group]]

* [[super commutative monoid]]

* [[super module]]

* [[super ring]]

* [[supercommutative ring]]