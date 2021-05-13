
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

### Decidability
 {#Decidability}

Only the intensional but not the [[extensional type theory|extensional]] [[Martin-Löf type theory]] has [[decidability|decidable]] type checking. ([Martin-L&#246;f 75](#MartinLof75), [Hofmann 95](#Hofmann95)).

## Examples

* [[CiC]]

## Related concepts

* [[homotopy type theory]]

* [[extensional type theory]], [[observational type theory]]

* [[function extensionality]]

## References

* {#MartinLof75} [[Per Martin-Löf]], _An intuitionistic theory of types: predicative part_, in: H. E. Rose, J. C. Shepherdson (eds.), *Logic Colloquium '73, Proceedings of the Logic Colloquium*, Studies in Logic and the Foundations of Mathematics **80** Pages 73-118,  Elsevier 1975 (<a href="https://doi.org/10.1016/S0049-237X(08)71945-1">doi:10.1016/S0049-237X(08)71945-1</a>, [CiteSeer](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.131.926))
  

* {#Hofmann95} [[Martin Hofmann]], _Extensional concepts in intensional type theory_, Ph.D. thesis, University of
Edinburgh, (1995) ([ECS-LFCS-95-327](http://www.lfcs.inf.ed.ac.uk/reports/95/ECS-LFCS-95-327/), [[HofmannExtensionalIntensionalTypeTheory.pdf:file]])
  

[[!redirects intensional type theories]]
