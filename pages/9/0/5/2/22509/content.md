
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A *Church monoid* is a particular type of [[algebra|algebraic]] [[mathematical structure]] that provides [[semantics]] for a flavour of [[relevance logic]], a weak form of [[substructural logic]].

## Definition

A Church monoid is a [[partially ordered set|partially ordered]] [[commutative monoid]] $(M,\circ, 1,\leq)$ that is has a binary operation, "implication", written $a\to b$ that as an operation $b\mapsto (a\to b)$ is [[right adjoint]] to the [[functor]] $-\circ a$. Here $M$ is considered as a [[thin category]] associated to the underlying [[poset]]. Additionally, for all $a\in M$, $a \leq a\circ a$, resulting in a [[monoidal category with diagonals]], where $\circ$ is the monoidal product.


## Related concepts

* [[relevance monoidal category]]
* [[relevance logic]]
* [[Ackermann groupoid]] (where "groupoid" means [[magma]])
* [[Heyting algebra]]

## References

Church monoids were introduced in

* Robert K. Meyer, _Conservative extension in relevant implication_, Studia Logica volume 31 (1973) pp39–46, doi:[10.1007/BF02120525](https://doi.org/10.1007/BF02120525).