
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

 
The _singular simplicial complex_ $S_\bullet(X)$ of a [[topological space]] $X$ is the [[nerve]] of $X$ with respect to the standard [[cosimplicial object|cosimplicial]] topological space $\Delta_{Top} : \Delta \to Top$:

$$
  S_n(X) = Hom_{Top}(\Delta_{Top}^n, X)
  \,.
$$

This is always a [[Kan complex]] and as such has the interpretation of the [[fundamental ∞-groupoid]] $\Pi(X)$ of $X$.


## Properties

Together with its [[adjoint functor|adjoint]] -- [[geometric realization]] $|-| : sSet \to Top$ -- the functor $Sing : Top \to sSet$ is part of the [[Quillen equivalence]] between the [[model structure on topological spaces]] and the [[model structure on simplicial sets]] that is sometimes called the [[homotopy hypothesis]]-theorem.
