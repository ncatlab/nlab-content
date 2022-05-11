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

A more general version of [[super vector space]]. 

## Definition ##

### $\mathbb{Z}/2\mathbb{Z}$-graded $R$-modules ###

Given a [[commutative ring]] $R$, an **$\mathbb{Z}/2\mathbb{Z}$-graded $R$-module** is a $R$-[[module]] $V$ with decomposition functions $\mathcal{D}_0:V \to V$ and $\mathcal{D}_1:V \to V$, such that 

* for all $v:V$, $v = \mathcal{D}_0(v) + \mathcal{D}_1(v)$
* for all $a:R$, $b:R$, $v:V$, and $w:V$, $\mathcal{D}_0(a v + b w) = a \mathcal{D}_0(v) + b \mathcal{D}_0(w)$
* for all $a:R$, $b:R$, $v:V$, and $w:V$, $\mathcal{D}_1(a v + b w) = a \mathcal{D}_1(v) + b \mathcal{D}_1(w)$
* for all $v:V$, $\mathcal{D}_0(\mathcal{D}_0(v)) = \mathcal{D}_0(v)$
* for all $v:V$, $\mathcal{D}_0(\mathcal{D}_1(v)) = 0$
* for all $v:V$, $\mathcal{D}_1(\mathcal{D}_0(v)) = 0$
* for all $v:V$, $\mathcal{D}_1(\mathcal{D}_1(v)) = \mathcal{D}_1(v)$

As a result, the [[image]] of the two decomposition functions $\im(\mathcal{D}_0)$ and $\im(\mathcal{D}_1)$ are $R$-[[modules]]  and there exists a [[linear isomorphism]] $i:V \cong \im(\mathcal{D}_0) \otimes \im(\mathcal{D}_1)$, where $A \otimes B$ is the [[tensor product of modules]]. 

The elements of $\im(\mathcal{D}_0)$ are called **even elements** or **bosonic elements**, and the elements of $\im(\mathcal{D}_1)$ are called **odd elements** or **fermionic elements**. 

### Super modules ###

The tensor product of $\mathbb{Z}/2\mathbb{Z}$-graded $R$-modules $A \otimes B$ for $a:A$, $b:B$ is defined as the following: 

$$\mathcal{D}_0(a \otimes b) = \mathcal{D}_0(a) \otimes \mathcal{D}_0(b) + \mathcal{D}_1(a) \otimes \mathcal{D}_1(b)$$

$$\mathcal{D}_1(a \otimes b) = \mathcal{D}_0(a) \otimes \mathcal{D}_1(b) + \mathcal{D}_1(a) \otimes \mathcal{D}_0(b)$$

This plus the linearity of the $\mathcal{D}_0$ and $\mathcal{D}_1$ functions result in the category of $\mathbb{Z}/2\mathbb{Z}$-graded $R$-modules to be a [[monoidal category]]. 

A **super module** is an object of the category of $\mathbb{Z}/2\mathbb{Z}$-graded $R$-modules with the braiding for the tensor product $A \otimes B$:

$$t_{A, B}:(A \otimes B) \to (B \otimes A)$$

such that 

$$\mathcal{D}_0(t_{A, B}(a, b)) = \mathcal{D}_0(a) \otimes \mathcal{D}_0(b) - \mathcal{D}_1(a) \otimes \mathcal{D}_1(b)$$

$$\mathcal{D}_1(t_{A, B}(a, b)) = \mathcal{D}_0(a) \otimes \mathcal{D}_1(b) + \mathcal{D}_1(a) \otimes \mathcal{D}_0(b)$$

## See also ##

* [[module]]

* [[graded module]]

* [[super vector space]]

* [[commutative ring]]

* [[super abelian group]]

* [[super algebra]]