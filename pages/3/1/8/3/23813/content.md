[[!redirects super modules]]
[[!redirects super prevector space]]
[[!redirects super prevector spaces]]

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
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea ##

A more general version of [[super vector space]]

## Definition ##

Given a [[commutative ring]] $R$, an **$R$-super module** or **$\mathbb{Z}/2\mathbb{Z}$-graded $R$-module** is a $R$-[[module]] $V$ with decomposition functions $\mathcal{D}_0:V \to V$ and $\mathcal{D}_1:V \to V$, such that 

* for all $v:V$, $v = \mathcal{D}_0(v) + \mathcal{D}_1(v)$
* for all $a:R$, $b:R$, $v:V$, and $w:V$, $\mathcal{D}_0(a v + b w) = a \mathcal{D}_0(v) + b \mathcal{D}_0(w)$
* for all $a:R$, $b:R$, $v:V$, and $w:V$, $\mathcal{D}_1(a v + b w) = a \mathcal{D}_1(v) + b \mathcal{D}_1(w)$
* for all $v:V$, $\mathcal{D}_0(\mathcal{D}_0(v)) = \mathcal{D}_0(v)$
* for all $v:V$, $\mathcal{D}_0(\mathcal{D}_1(v)) = 0$
* for all $v:V$, $\mathcal{D}_1(\mathcal{D}_0(v)) = 0$
* for all $v:V$, $\mathcal{D}_1(\mathcal{D}_1(v)) = \mathcal{D}_1(v)$

As a result, the [[image]] of the two decompostion functions $\im(\mathcal{D}_0)$ and $\im(\mathcal{D}_1)$ are $R$-[[modules]]  and there exists a [[linear isomorphism]] $i:V \cong \im(\mathcal{D}_0) \otimes \im(\mathcal{D}_1)$, where $A \otimes B$ is the [[tensor product of modules]]. There exists a parity function $\deg:\im(\mathcal{D}_0) \uplus \im(\mathcal{D}_1) \to \mathbb{Z}/2\mathbb{Z}$ where $A \uplus B$ is the [[disjoint union]] of $A$ and $B$, such that the [[fiber]] of $\deg$ at $0$ is $\im(\mathcal{D}_0)$ and the fiber of $\deg$ at $1$ is $\im(\mathcal{D}_1)$. 

The elements of $\im(\mathcal{D}_0)$ are called **even elements** or **bosonic elements**, and the elements of $\im(\mathcal{D}_1)$ are called **odd elements** or **fermionic elements**. 

## See also ##

* [[module]]

* [[graded module]]

* [[super vector space]]

* [[commutative ring]]

* [[super abelian group]]