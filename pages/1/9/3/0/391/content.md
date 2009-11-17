#Contents#
* automatic table of contents goes here
{:toc}

## Idea ##

The concept of _enriched homotopical category_ is the generalization of the concept of [[homotopical category]] to the context of [[enriched category theory]] and hence to [[homotopy coherent category theory]].

The idea is that the [[homotopy category]] $Ho_C$ of a category $C$ which is enriched over a suitable [[monoidal category|monoidal]]  and [[homotopical category|homotopical]] category $V$ is itself a $Ho_V$-enriched category.

## Definition ##

For $V$ a [[closed monoidal homotopical category]],
a $V$-[[enriched category]] $C$ with [[power|powers]] and [[copower|copowers]] and with the structure of a [[homotopical category]] on its underlying category $C_0$ is a **$V$-homotopical category** when equipped with a [[deformation retract for the enrichment]].

## Examples ##

If $V$ is a [[monoidal model category]], then any $V$-[[enriched model category]] is automatically a $V$-homotopical category.

## Consequences ##

[[closed monoidal homotopical category|Recall]] that for $V$ as above, $Ho_V$ is closed monoidal.

+-- {: .un_prop}
###### Proposition
With $C$ a $V$-homotopical category, $Ho_{C_0}$ is the underlying category of a $Ho_V$-enriched category.
=--

Write $Ho_C$ for this $Ho_V$-enriched category.  This is the enriched analogue of the [[homotopy category]] of $C$.

So schematically we have (with all of the above qualifiers suppressed):
$$
  (C \in V-Cat) \Rightarrow (Ho_C \in Ho_V-Cat)
$$

## Construction of the enriched homotopy category ##

For $C$ an enriched homotopical $V$-category as above, the  $Ho_V$-category $Ho_C$ is constructed from the homotopy category $Ho_{C_0}$ of the ordinary category underlying $C$ by constructing a $Ho_V$-[[closed monoidal category module|module structure]], essentially following 
section 4.3.2 of Hovey: _Model categories_.

## References ##

The definition appears as [definition 16.1, p. 46](http://arxiv.org/PS_cache/math/pdf/0610/0610194v1.pdf#page=46) in Shulman: [Homotopy limits and colimits in enriched homotopy theory](http://arxiv.org/abs/math.AT/0610194v1), the proposition is [proposition 16.2, p. 46](http://arxiv.org/PS_cache/math/pdf/0610/0610194v1.pdf#page=46). The construction of $Ho_C$ follows the proof of [proposition 15.4, p. 45](http://arxiv.org/PS_cache/math/pdf/0610/0610194v1.pdf#page=46).
