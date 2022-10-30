
#Contents#
* table of contents
{:toc}

## Idea

Canonical extension provides an algebraic formulation of [[duality]] theory and a tool to derive representation theorems. It may be regarded as an algebraic formulation of [[Stone duality]] (see [Gehrke-Vosmaer, p. 5](#GehrkeVosmaer)).

Originally ([Jonsson-Tarski](#JonssonTarski)) is was formulated for [[Boolean algebras]] with operators, but the notion was later generalized to [[distributive lattices]] and even to arbitrary [[posets]].

## Definition

### For distributive lattices

Given a [[distributive lattice]] $L$, its **canonical extension** $L^\delta$ is the [[downset]] [[lattice]] of the [[poset]] of [[prime filters]] of $L$, ordered by inclusion.

This construction extends to a [[functor]]

$$
  (-)^\delta : DistLattice \to DistLattice^+
$$

from the [[category]] of [[distributive lattices]] to that of completely distributive [[algebraic lattices]]. This is [[left adjoint]] to the corresponding [[forgetful functor]].

### For coherent categories

(...)

## Related concepts

* [[topos of types]]

## References

The study of canonical extensions originates in the articles

* B. J&#243;nsson, [[Alfred Tarski]], _Boolean algebras with operators, I_, Amer. J. Math. 73 (1951), 891&#8211;939.
 {#JonssonTarski}

Reviews include

* Mai Gehrke, Jacob Vosmaer, _A view of canonical extension_ ([arXiv:1009.2803](http://arxiv.org/abs/1009.2803))
 {#GehrkeVosmaer}

[[!redirects canonical extensions]]
