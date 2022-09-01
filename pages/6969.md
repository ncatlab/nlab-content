
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

_Intensional type theory_ is the flavor of [[type theory]] in which [[identity types]] are not necessarily [[propositions]] (that is, [[(-1)-truncated]]).  [[Per Martin-Löf|Martin-Löf]]'s original definition of identity types, and the equivalent formulation as an [[inductive type]], are by default "intensional"; one has to impose extra [[axioms]] or rules in order to get [[extensional type theory]] (in which identity types are propositions).

In particular, [[homotopy type theory]] is intensional, because identity types represent [[path objects]].

Note that some type theorists use "intensional type theory" to refer to type theories which fail to satisfy [[function extensionality]].  This is in general an orthogonal requirement to how we are using the term here.

+-- {: .num_remark}
###### Remark
The origin of the names "extensional" and "intensional" is somewhat confusing.  In fact they refer to the behavior of the [[definitional equality]].  The idea is that the [[identity type]] is always an "extensional" notion of equality (although it can be more or less extensional, depending on whether further extensionality principles like [[function extensionality]] and [[univalence]] hold).  Thus, if the definitional equality *coincides* with the identity type, the former is also extensional, and so we call the type theory "extensional" --- while if the two equalities do *not* coincide, then the definitional equality has room to be more intensional than the identity type, and so we call the type theory "intensional".  (On this historical reading, "extensional type theory" should refer only to *definitionally* extensional type theory with the reflection rule, which is much stronger than merely requiring all types to be h-sets.)
=--

## Properties

### Decidability
 {#Decidability}

Only the intensional but not the [[extensional type theory|extensional]] [[Martin-Löf type theory]] has [[decidability|decidable]] type checking. ([Martin-L&#246;f 75](#MartinLof75), [Hofmann 95](#Hofmann95)).

## Examples

* [[CiC]]

## Related concepts

* [[homotopy type theory]]

* [[extensional type theory]]

* [[observational type theory]], [[higher observational type theory]]

* [[function extensionality]]

## References

* {#MartinLof75} [[Per Martin-Löf]], _An intuitionistic theory of types: predicative part_, in: H. E. Rose, J. C. Shepherdson (eds.), *Logic Colloquium '73, Proceedings of the Logic Colloquium*, Studies in Logic and the Foundations of Mathematics **80** Pages 73-118,  Elsevier 1975 (<a href="https://doi.org/10.1016/S0049-237X(08)71945-1">doi:10.1016/S0049-237X(08)71945-1</a>, [CiteSeer](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.131.926))
  

* {#Hofmann95} [[Martin Hofmann]], _Extensional concepts in intensional type theory_, Ph.D. thesis, University of
Edinburgh, (1995) ([ECS-LFCS-95-327](http://www.lfcs.inf.ed.ac.uk/reports/95/ECS-LFCS-95-327/), [[HofmannExtensionalIntensionalTypeTheory.pdf:file]])
  

[[!redirects intensional type theories]]
