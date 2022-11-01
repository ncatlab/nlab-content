+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

\tableofcontents

## Idea

In [[(n,1)-categories]] and [[(infinity,1)-categories]], the usual definition of [[invertible morphism]] is too strict and would violate the [[principle of equivalence]]. There are a few options to resolve this issue: one is by using [[weak inverses]]; but another is by using bi-invertible morphisms, which are a generalization of the notion of bi-invertible function in [[type theory]]. 

## Definition

A morphism $f:Mor(A, B)$ in a [[(n,1)-category]] or [[(infinity,1)-category]] is **bi-invertible** if there are morphisms $\mathrm{sec}(f):Mor(B, A)$ and $\mathrm{ret}(f):Mor(B, A)$ such that $\mathrm{sec}(f)$ is a [[section]] of $f$ and $\mathrm{ret}(f)$ is a [[retraction]] of $f$, with section and retraction defined using [[path space objects]] rather than strict equality. 

## Examples

An [[integers object]] in an [[(n,1)-category]] $C$ with a [[terminal object]] is defined as the (homotopy) initial object $\mathbb{Z}$ with a [[global element]] $0:Mor(1, \mathbb{Z})$ and a bi-invertible [[endomorphism]] $\mathrm{succ}:Mor(\mathbb{Z}, \mathbb{Z})$ with section $\mathrm{pred}_1:Mor(\mathbb{Z}, \mathbb{Z})$ and retraction $\mathrm{pred}_2:Mor(\mathbb{Z}, \mathbb{Z})$. This corresponds to a definition of the [[integers]] [[higher inductive type]] in the [[internal logic]] of an [[(n,1)-category]]. 

## See also

* [[invertible morphism]]

* [[weak inverse]]

* [[equivalence of types]]

## References

For the integers object as defined with a bi-invertible morphism in the internal logic of a [[(infinity,1)-category]] see

* [[Thorsten Altenkirch]], [[Luis Scoccola]], *The Integers as a Higher Inductive Type*, [arXiv](https://arxiv.org/abs/2007.00167)

[[!redirects bi-invertible morphism]]
[[!redirects bi-invertible morphisms]]