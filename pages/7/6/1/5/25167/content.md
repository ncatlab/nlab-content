
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

\tableofcontents

## Definition

A **reduced local ring** is a [[commutative ring]] which is both a [[local ring]] and a [[reduced ring]], hence a commutative ring such that:

* The ring is nontrivial $0 \neq 1$;

* if the sum of two elements $x + y$ is equal to $1$, then $x$ is [[invertible]] or $y$ is invertible;

* every [[nilpotent element]] is equal to [[zero]]; equivalently, every element which squares to zero is equal to zero. 

## Examples

* Every [[Heyting field]] is a reduced local ring which is also a [[Artinian ring]]. 

* Given a [[discrete field]] $K$, the ring of [[power series]] $K[[x]]$ is a reduced local ring which is not a [[Heyting field]]. 

## Properties

Unlike the [[theory]] of [[Heyting fields]], the theory of reduced local rings is a [[coherent theory]]. It is the condition that a reduced local ring is an [[Artinian ring]] that fails in [[coherent logic]], since it relies on either negation to refer to non-invertible elements or proper ideals/maximal ideals (see [[Artinian local ring]]) or the [[natural numbers]] to refer to the [[descending chain condition]]. Even if one has the natural numbers around to define a [[dependent sequence]] of [[monomorphisms]] for the [[descending chain condition]], such as working internally in an [[arithmetic pretopos]], it is not necessarily the case that every such [[Artinian local ring]] has a maximal ideal or that [[Nakayama's lemma]] holds in [[coherent logic]]. 

## See also

* [[reduced ring]]

* [[local ring]]

* [[local integral domain]]

* [[Heyting field]]

* [[ordered reduced local ring]]

[[!redirects reduced local ring]]
[[!redirects reduced local rings]]