
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

### For maps between topological spaces

A [[function]]  $f : X \to Y$ between [[topological space]]s  is called __open__ if the [[image]] of every [[open set]] in $X$ is also open in $Y$.  Typically 


Recall that $f$ is __[[continuous map]]__ if the [[preimage]] of every [[open subspace|open set]] in $Y$ is open in $X$.  For defining open maps typically one restricts attention to open [[continuous map]]s, although it also makes sense to speak of open functions that are not continuous.


### For morphisms between locales

A continuous map $f\colon X \to Y$ of topological spaces defines a homomorphism $f^*\colon Op(Y) \to Op(X)$ between the [[frames]] of open sets of $X$ and $Y$.  If $f$ is open, then this frame homomorphism is also a [[Heyting algebra]] homomorphism; the converse holds for [[sober spaces]] (maybe as long as $Y$ is $T_0$?).  Accordingly, we define a map $f\colon X \to Y$ of [[locales]] to be __open__ if it is, as a frame homomorphism $f^*\colon Op(Y) \to Op(X)$, a Heyting algebra homomorphism.


### For geometric morphisms of toposes

[[categorification|Categorifying]], a [[geometric morphism]] $f\colon X \to Y$ of [[toposes]] is an [[open geometric morphism]] if its [[inverse image functor]] $f^*\colon Y \to X$ is a [[Heyting functor]].

[[!redirects open maps]]

[[!redirects open geometric morphism]]
[[!redirects open geometric morphisms]]