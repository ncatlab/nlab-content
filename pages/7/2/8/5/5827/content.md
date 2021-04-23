
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--


# Bilinear forms
* table of contents
{: toc}

## Definitions

A __bilinear form__ is simply a [[linear map]] $\langle -,-\rangle\colon V \otimes V \to k$ out of a [[tensor product]] of $k$-[[module]]s into the [[ring]] $k$ (typically taken to be a [[field]]).

It is called __symmetric__ if $\langle x,y\rangle = \langle y,x\rangle$ for all $x,y \in V$. For variants on this, such as the property of being _conjugate-symmetric_, see [[inner product space]]. 

It is called _nondegenerate_ if the [[mate]] $V \to V^\ast = \hom(V, k)$ is injective (a [[monomorphism]]). 

Let $k = \mathbb{R}$ be the [[real number]]s. A symmetric bilinear form is called

* [[positive definite]] if $\langle x,x\rangle \gt 0$ if $x \neq 0$.

* [[negative definite]] if $\langle x,x\rangle \lt 0$ if $x \neq 0$.


## Examples

* An _[[inner product]]_ on a real vector space is an example of a symmetric bilinear form. (For some authors, an inner product on a real vector space is precisely a positive definite symmetric bilinear form. Other authors relax the positive definiteness to nondegeneracy. Perhaps some authors even drop the nondegeneracy condition (citation?).) 

* If $f \colon \mathbb{R}^n \to \mathbb{R}$ is of class $C^2$, then the [[Hessian]] of $f$ at a point defines a symmetric bilinear form. It may be degenerate, but in [[Morse theory]], a [[Morse function]] is a $C^2$ function such that the Hessian at each critical point is nondegenerate. 

## Categorification and $n$POV
 {#CategorificationsAndnPOV}

Concepts which relate to (non-degenerate) bilinear forms from the [[nPOV]] and/or [[categorification|categorifications]] of the concept of bilinear forms  include

* [[2-Hilbert space]]

* [[Calabi-Yau object]], [[Calabi-Yau A-infinity category]]

## Related concepts

* [[quadratic form]], [[polarization identity]]

* [[sesquilinear form]]

* [[symplectic form]], [[Kähler form]], [[Hermitian form]]

* [[characteristic element of a bilinear form]]


* [[Riemannian metric]]

* [[Pythagorean theorem]]

* [[Cauchy–Schwarz inequality]]


[[!redirects bilinear form]]
[[!redirects bilinear forms]]

[[!redirects positive definite bilinear form]]
[[!redirects positive definite bilinear forms]]

[[!redirects positive semi-definite bilinear form]]
[[!redirects positive semi-definite bilinear forms]]

[[!redirects indefinite bilinear form]]
[[!redirects indefinite bilinear forms]]

[[!redirects symmetric bilinear form]]
[[!redirects symmetric bilinear forms]]


