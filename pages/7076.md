[[!redirects cartesian closed model category]]

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

A __cartesian model category__ (alias __cartesian closed model category__) is a [[cartesian closed category]] that is equipped with the structure of a [[monoidal model category]] in a compatible way, which combines the axioms for a [[monoidal model category]] and an [[enriched model category]].

## Definition

A **cartesian model category** (following Rezk (2010) and Simpson (2012)) is a cartesian closed category equipped with a [[model category|model structure]] that satisfies the following additional axioms:

* ([[pushout-product axiom|Pushout-product axiom]]). If $f : X \to Y$ and $f' : X' \to Y'$ are cofibrations, then the induced morphism $(Y \times X') \cup^{X \times X'} (X \times Y') \to Y \times Y'$ is a cofibration that is trivial if either $f$ or $f'$ is.

* (Unit axiom). The [[terminal object]] is cofibrant.


## Examples

* the standard [[Quillen model structure on topological spaces]] on [[compactly generated topological space|compactly generated]] [[weakly Hausdorff topological spaces]] is cartesian closed

* the standard [[model structure on simplicial sets]] is cartesian closed. 

## Related concepts

* [[cartesian closed category]], [[locally cartesian closed category]]

* [[cartesian closed functor]], [[locally cartesian closed functor]]

* **cartesian closed model category**, [[locally cartesian closed model category]]

* [[cartesian closed (∞,1)-category]] [[locally cartesian closed (∞,1)-category]]


## References

* [[Charles Rezk]], _A cartesian presentation of weak $n$-categories_. (2010). ([arXiv:0901.3602](http://arxiv.org/abs/0901.3602))

* [[Carlos Simpson]],  _Homotopy theory of higher categories_ (2012)

[[!redirects cartesian closed model categories]]
[[!redirects cartesian model categories]]

[[!redirects cartesian closed model structure]]
[[!redirects cartesian closed model structures]]
[[!redirects cartesian model structure]]
[[!redirects cartesian model structures]]
