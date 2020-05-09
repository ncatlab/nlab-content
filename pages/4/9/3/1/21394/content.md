
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

The notion of a _premodel category_ is a relaxation of the notion of a [[model category]].
[[combinatorial model category|Combinatorial]] premodel categories form a [[2-category]]
that has all ([[small diagram|small]]) [[limits]] and [[colimits]] and has [[representing objects]] for [[Quillen bifunctors]].

The [[2-category]] of combinatorial $V$-[[enriched category|enriched]] premodel categories is the category of [[modules over a monoid]] $V$ in this [[2-category]].
It inherits the same set of properties
and additionally admits a [[model 2-category]] structure.
In this model structure, a [[left Quillen functor]] is a [[weak equivalence]]
if and only if it is a [[Quillen equivalence]].

## Definition

A __premodel category__ is a [[bicomplete category]]
equipped with a [[pair]] of [[weak factorization systems]]
$(C,AF)$ and $(AC,F)$ such that $AC\subset C$ (equivalently, $AF\subset F$).

[[model category|Model categories]] can be singled out among premodel categories by imposing the additional requirement that the [[class]] 

$$
  W
  \coloneqq
  AF \circ AC
  \,,
$$

obtained by [[composition|composing]] [[elements]] of $AC$ with those of $AF$, is closed under the [[2-out-of-3 property]].

The members of AC are called __anodyne cofibrations__ and the members of AF are called __anodyne fibrations__ (as in _[[anodyne morphism]]_).

## Anodyne and trivial (co)fibrations

The notion of premodel category doesn't come with a good general notion of weak equivalence. But if a particular premodel category has a good notion of weak equivalence, such as one of [Barton](#Barton)'s _relaxed premodel categories_, one needs to distinguish between two types of cofibrations (and analogously between two types of fibrations):

* An __anodyne cofibration__ is a member of the class AC
* A __trivial cofibration__ is a cofibration that is also a weak equivalence

In principle one must also distinguish a third class of cofibrations that have the left lifting property with respect to fibrations between fibrant objects. However, in a relaxed premodel category, these are trivial cofibrations. ([Barton, Prop 3.5.2](#Barton))

## Related concepts

* [[model category]]

* [[weak model category]]

## References

* {#Barton} [[Reid William Barton]], _A model 2-category of enriched combinatorial premodel categories_ ([arXiv:2004.12937](https://arxiv.org/abs/2004.12937))

[[!redirects premodel categories]]