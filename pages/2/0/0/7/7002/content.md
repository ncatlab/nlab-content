
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

For $\Gamma : \mathcal{E} \to \mathcal{B}$ a [[functor]] we say that it _has [[discrete objects]]_ if it has a  [[full and faithful functor|full and faithful]] [[left adjoint]] $Disc : \mathcal{B} \hookrightarrow \mathcal{E}$. 

An object in the [[essential image]] of $Disc$ is called a **discrete object.

This is for instance the case for the [[global section]] [[geometric morphism]] of a [[connected topos]] $ (Disc \dashv \Gamma ) : \mathcal{E} \to \mathcal{B}$. 

In this situation, we say that a **co-concrete object** $X \in \mathcal{E}$ is one for which the $(Disc\dashv \Gamma)$-[[counit of an adjunction]] is an [[epimorphism]].

The dual concept is the of a _[[concrete object]]_.

## References

* [[Mike Shulman]], _Discreteness, Concreteness, Fibrations, and Scones_ ([blog post](http://golem.ph.utexas.edu/category/2011/11/discreteness_concreteness_fibr.html))
 {#Shulman}

[[!redirects co-concrete objects]]

[[!redirects coconcrete object]]
[[!redirects coconcrete objects]]