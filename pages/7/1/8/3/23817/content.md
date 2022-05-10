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

* for all $v:V$, $v = \mathcal{D}_0(v) + \mathcal{D}_1(v)$
* for all $v:V$, and $w:V$, $\mathcal{D}_0(v + w) = \mathcal{D}_0(v) + \mathcal{D}_0(w)$
* for all $v:V$, and $w:V$, $\mathcal{D}_1(v + w) = \mathcal{D}_1(v) + \mathcal{D}_1(w)$
* for all $v:V$, $\mathcal{D}_0(\mathcal{D}_0(v)) = \mathcal{D}_0(v)$
* for all $v:V$, $\mathcal{D}_0(\mathcal{D}_1(v)) = 0$
* for all $v:V$, $\mathcal{D}_1(\mathcal{D}_0(v)) = 0$
* for all $v:V$, $\mathcal{D}_1(\mathcal{D}_1(v)) = \mathcal{D}_1(v)$

As a result, the [[image]] of the two decompostion functions $\im(\mathcal{D}_0)$ and $\im(\mathcal{D}_1)$ are $R$-[[modules]]  and there exists a [[linear isomorphism]] $i:V \cong \im(\mathcal{D}_0) \otimes \im(\mathcal{D}_1)$, where $A \otimes B$ is the [[tensor product of abelian groups]]. There exists a parity function $\deg:\im(\mathcal{D}_0) \uplus \im(\mathcal{D}_1) \to \mathbb{Z}/2\mathbb{Z}$ where $A \uplus B$ is the [[disjoint union]] of $A$ and $B$, such that the [[fiber]] of $\deg$ at $0$ is $\im(\mathcal{D}_0)$ and the fiber of $\deg$ at $1$ is $\im(\mathcal{D}_1)$. 

The elements of $\im(\mathcal{D}_0)$ are called **even elements** or **bosonic elements**, and the elements of $\im(\mathcal{D}_1)$ are called **odd elements** or **fermionic elements**. 

## See also ##

* [[abelian group]]

* [[graded abelian group]]

* [[super module]]