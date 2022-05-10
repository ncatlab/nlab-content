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
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea ##

In the same vein that [[commutative rings]] are to [[integral domains]], [[GCD rings]] are to [[GCD domains]], and [[prefields]] are to [[fields]], [[super prevector spaces]] are to [[super vector spaces]]. 

## Definition ##

Given a [[prefield]] $F$, an **$F$-super prevector space** or **$\mathbb{Z}/2\mathbb{Z}$-graded $F$-prevector space** is a $F$-[[prevector space]] $V$ with decomposition functions $\mathcal{D}_0:F \to F$ and $\mathcal{D}_1:F \to F$, such that 

* for all $v:V$, $v = \mathcal{D}_0(v) + \mathcal{D}_1(v)$
* for all $a:F$, $b:F$, $v:V$, and $w:V$, $\mathcal{D}_0(a v + b w) = a \mathcal{D}_0(v) + b \mathcal{D}_0(w)$
* for all $a:F$, $b:F$, $v:V$, and $w:V$, $\mathcal{D}_1(a v + b w) = a \mathcal{D}_1(v) + b \mathcal{D}_1(w)$
* for all $v:V$, $\mathcal{D}_0(\mathcal{D}_0(v)) = \mathcal{D}_0(v)$
* for all $v:V$, $\mathcal{D}_0(\mathcal{D}_1(v)) = 0$
* for all $v:V$, $\mathcal{D}_1(\mathcal{D}_0(v)) = 0$
* for all $v:V$, $\mathcal{D}_1(\mathcal{D}_1(v)) = \mathcal{D}_1(v)$

As a result, the [[image]] of the two decompostion functions $\im(\mathcal{D}_0)$ and $\im(\mathcal{D}_1)$ are [[prevector spaces]]  and there exists a [[linear isomorphism]] $i:V \cong \im(\mathcal{D}_0) \otimes \im(\mathcal{D}_1)$, where $A \otimes B$ is the [[tensor product of modules|tensor product]] of prevector spaces. There exists a parity function $\deg:\im(\mathcal{D}_0) \uplus \im(\mathcal{D}_1) \to \mathbb{Z}/2\mathbb{Z}$ where $A \uplus B$ is the [[disjoint union]] of $A$ and $B$, such that the [[fiber]] of $\deg$ at $0$ is $\im(\mathcal{D}_0)$ and the fiber of $\deg$ at $1$ is $\im(\mathcal{D}_1)$. 

The elements of $\im(\mathcal{D}_0)$ are called **even vectors** or **bosonic vectors**, and the elements of $\im(\mathcal{D}_1)$ are called **odd vectors** or **fermionic vectors**. 

## Examples ##

* Every $\mathbb{Q}$-super vector space is a $\mathbb{Q}$-super prevector space. 

* Every super classical vector space is a $F$-super prevector space for a classical [[field]] $F$ (defined using [[denial inequality]]).

* Every super Heyting vector space is a $F$-super prevector space for a [[Heyting field]] $F$. 

* Every super discrete vector space is a $F$-super prevector space for a [[discrete field]] $F$. 

* Every super residue vector space is a $F$-super prevector space for a [[residue field]] $F$. 

## See also ##

* [[prevector space]]

* [[super vector space]]

* [[prefield]]