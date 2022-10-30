
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Discrete and concrete objects
+-- {: .hide}
[[!include discrete and concrete objects - contents]]
=--
#### Category Theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

For $\Gamma : \mathcal{E} \to \mathcal{B}$ a [[functor]] we say that it _has [[codiscrete object]]s_ if it has a  [[full and faithful functor|full and faithful]] [[right adjoint]] $coDisc : \mathcal{B} \hookrightarrow \mathcal{E}$. 

This is for instance the case for the [[global section]] [[geometric morphism]] of a [[local topos]] $ (Disc \dashv \Gamma \dashv coDisc) \mathcal{E} \to \mathcal{B}$. 

In this situation, we say that a  **concrete object** $X \in \mathcal{E}$ is one for which the $(\Gamma \dashv coDisc)$-[[unit of an adjunction]] is a [[monomorphism]].

If $\mathcal{E}$ is a [[sheaf topos]], this is called a [[concrete sheaf]].

If $\mathcal{E}$ is a [[cohesive (∞,1)-topos]] then this is called a [[concrete (∞,1)-sheaf]] or the like.

The dual notion is that of a [[co-concrete object]].

## Properties

$\Gamma$ is a [[faithful functor]] on [[morphisms]] whose [[codomain]] is concrete. 


## Related concepts

[[!include cohesion - table]]


## References

* [[Mike Shulman]], _Discreteness, Concreteness, Fibrations, and Scones_ ([blog post](http://golem.ph.utexas.edu/category/2011/11/discreteness_concreteness_fibr.html))
 {#Shulman}

[[!redirects concrete objects]]