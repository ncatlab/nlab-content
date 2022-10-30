
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The version of [[type theory]] in which [[function extensionality]] does not hold as an identification: 

two [[terms]] $f, g$ of [[function types]] are _not_ necessarily identified if $\forall x : f(x) = g(x)$. Rather, the two functions may differ by _how_ they compute this result.

If this distinction is not made, one speaks of [[extensional type theory]].

## Properties

### Identity types

In particular two terms of a [[propositions as types|proposition type]] may give the same result ("[[true]]" or "[[false]]"), hence be [[proof]]s of the given proposition, but be _different_ proofs. This is implemented by the notion of [[identity types]] (as opposed to "equality types") in intensional type theory.

However, intensional identity types induce (see [[homotopy type theory]]) a notion of [[equivalence]] and allow to formulate the [[univalence axiom]]. When this holds, then function extensionality holds by equivalences.

### Decidibility

Only the intensional but not the [[extensional type theory|extensional]] [[Martin-Löf type theory]] is [[decidable]]. ([Martin-L&#246;f](#MartinLoef), [Hofmann](#Hofmann)).

## Related concepts

* [[function extensionality]]

## References

* [[Per Martin-Löf]], _An intuitionistic theory of types: predicative part_, Logic Colloquium '73
(Amsterdam) (H. E. Rose and J. C. Shepherdson, eds.), North-Holland, 1975, pp. 73-118.
  {#MartinLoef}

* [[Martin Hofmann]], _Extensional concepts in intensional type theory_, Ph.D. thesis, University of
Edinburgh, (1995)
  {#Hofmann}

[[!redirects intensional type theories]]
