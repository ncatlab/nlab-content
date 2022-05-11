[[!redirects super rings]]

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
=--
=--

#Contents#
* table of contents
{:toc}

## Idea ##

A super ring is an $\mathbb{Z}$-[[super algebra]]. 

## Definition ##

A **super ring** is a [[ring]] $R$ with decomposition functions $\mathcal{D}_0:R \to R$ and $\mathcal{D}_1:R \to R$, such that 

* for all $a:R$, $a = \mathcal{D}_0(a) + \mathcal{D}_1(a)$
* for all $a:R$, and $b:R$, $\mathcal{D}_0(a + b) = \mathcal{D}_0(a) + \mathcal{D}_0(b)$
* for all $a:R$, and $b:R$, $\mathcal{D}_1(a + b) = \mathcal{D}_1(a) + \mathcal{D}_1(b)$
* for all $a:R$, and $b:R$, $\mathcal{D}_0(a \cdot b) = \mathcal{D}_0(a) \cdot \mathcal{D}_0(b) - \mathcal{D}_1(a) \cdot \mathcal{D}_1(b)$
* for all $a:R$, and $b:R$, $\mathcal{D}_1(a \cdot b) = \mathcal{D}_0(a) \cdot \mathcal{D}_1(b) + \mathcal{D}_1(a) \cdot \mathcal{D}_0(b)$
* for all $a:R$, and $b:R$, $\mathcal{D}_0(1) = 1$
* for all $a:R$, and $b:R$, $\mathcal{D}_1(1) = 1$
* for all $a:R$, $\mathcal{D}_0(\mathcal{D}_0(a)) = \mathcal{D}_0(a)$
* for all $a:R$, $\mathcal{D}_0(\mathcal{D}_1(a)) = 0$
* for all $a:R$, $\mathcal{D}_1(\mathcal{D}_0(a)) = 0$
* for all $a:R$, $\mathcal{D}_1(\mathcal{D}_1(a)) = \mathcal{D}_1(a)$

As a result, the [[image]] of the two decompostion functions $\im(\mathcal{D}_0)$ and $\im(\mathcal{D}_1)$ are rings and there exists an [[abelian group]] [[isomorphism]] $i:V \cong \im(\mathcal{D}_0) \otimes \im(\mathcal{D}_1)$, where $F:Ring \to Ab$ is a forgetful functor and $F(A) \otimes F(B)$ is the [[tensor product of abelian groups]].  

The elements of $\im(\mathcal{D}_0)$ are called **even elements** or **bosonic elements**, and the elements of $\im(\mathcal{D}_1)$ are called **odd elements** or **fermionic elements**. 

## See also ##

* [[ring]]

* [[exterior ring]]

* [[Clifford ring]]

* [[graded ring]]

* [[super abelian group]]

* [[super algebra]]

* [[supercommutative ring]]