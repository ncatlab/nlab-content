
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

_Intensional type theory_ is the flavor of [[type theory]] in which [[identity types]] are not necessarily [[propositions]] (that is, [[(-1)-truncated]]).  [[Per Martin-Löf|Martin-Löf]]'s original definition of identity types, and the equivalent formulation as an [[inductive type]], are by default intensional; one has to impose extra axioms or rules in order to get [[extensional type theory]] (in which identity types are propositions).

In particular, [[homotopy type theory]] is intensional, because identity types represent [[path objects]].

Note that some type theorists use "intensional type theory" to refer to type theory which fails to satisfy [[function extensionality]].  This is in general an orthogonal requirement to how we are using the term here.

## Properties

### Decidibility
 {#Decidibility}

Only the intensional but not the [[extensional type theory|extensional]] [[Martin-Löf type theory]] is [[decidable]]. ([Martin-L&#246;f](#MartinLoef), [Hofmann](#Hofmann)).

## Related concepts

* [[homotopy type theory]]
* [[extensional type theory]]
* [[function extensionality]]

## References

* [[Per Martin-Löf]], _An intuitionistic theory of types: predicative part_, Logic Colloquium '73
(Amsterdam) (H. E. Rose and J. C. Shepherdson, eds.), North-Holland, 1975, pp. 73-118.
  {#MartinLoef}

* [[Martin Hofmann]], _Extensional concepts in intensional type theory_, Ph.D. thesis, University of
Edinburgh, (1995) ([web](http://www.lfcs.inf.ed.ac.uk/reports/95/ECS-LFCS-95-327/))
  {#Hofmann}

[[!redirects intensional type theories]]
