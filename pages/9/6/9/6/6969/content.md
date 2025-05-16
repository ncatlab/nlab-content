
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

By _intensional type theory_ one means (but see Rem. \ref{RemarkOnTerminology}) the flavor of [[type theory]] in which [[identity types]] are not forced to be [[mere propositions]] (that is: not necessarily [[(-1)-truncated]]).  

The original definition of [[identity types]] in [[Martin-Löf dependent type theory]] &lbrack;[Martin-Löf (1975, §1.7 and p. 94)](#Martin-Löf75)&rbrack; is by default *intensional*: It takes an additional [[axiom]] or rule --- the *identity reflection rule*, cf. [Streicher (1993, p. 4, 13 )](#Streicher93); [Hofmann (1995, p. 16)](#Hofmann95) --- to turn intensional into [[extensional type theory]] (in which identity types are then [[truncated type|truncated]] to [[mere propositions]]).

In particular, [[homotopy type theory]] is intensional: the [[categorical semantics]] of its [[identity types]] are [[path space objects]].


\begin{remark}
\label{RemarkOnTerminology}
**(terminology)**
\linebreak
Beware that some authors take the words "intensional type theory" to refer to [[type theories]] which *fail to satisfy [[function extensionality]]*.  This is in general a requirement orthogonal to the (-1)-truncation of identity types.

Generally, the origin of the names "extensional" and "intensional" is somewhat confusing. Even where the term refers to the behaviour of [[equality]], it in fact refers not to the [[typal equality]] expressed by [[identity types]], but to *[[judgmental equality]]*:  

The idea is that the [[identity type]] is *always* an "[[extension (semantics)|extensional]]" notion of [[equality]] (although it can be more or less extensional, depending on whether further extensionality principles like [[function extensionality]] and [[univalence]] hold). Thus, if the judgmental equality *coincides* with the identity type, then the former is also extensional, whence the type theory is called "extensional" --- while if the two equalities do *not* coincide, then the judgmental equality has room to be more intensional than the identity type, making the type theory "intensional" (but see also [Hofmann (1995, ftn. 3)](#Hofmann95), [p. 17](https://ncatlab.org/nlab/files/HofmannExtensionalIntensionalTypeTheory.pdf#page=17)).

(On this historical reading, "[[extensional type theory]]" should refer only to *judgmentally* extensional type theory with the reflection rule, which is much stronger than merely requiring all types to be [[h-sets]].)
\end{remark}

## Properties

### Decidability
 {#Decidability}

Only the intensional but not the [[extensional type theory|extensional]] [[Martin-Löf type theory]] has [[decidability|decidable]] type checking. ([Martin-L&#246;f 75](#MartinLof75), [Hofmann 95](#Hofmann95)).

## Examples

* [[calculus of inductive constructions]]

## Related concepts

* [[homotopy type theory]]

* [[extensional type theory]]

* [[observational type theory]], [[higher observational type theory]]

* [[function extensionality]]

## References

* {#Martin-Löf75} [[Per Martin-Löf]], _An intuitionistic theory of types: predicative part_, in: H. E. Rose, J. C. Shepherdson (eds.), *Logic Colloquium '73, Proceedings of the Logic Colloquium*, Studies in Logic and the Foundations of Mathematics **80** Pages 73-118,  Elsevier 1975 (<a href="https://doi.org/10.1016/S0049-237X(08)71945-1">doi:10.1016/S0049-237X(08)71945-1</a>, [CiteSeer](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.131.926))

* {#Streicher93} [[Thomas Streicher]], *Investigations into Intensional Type Theory*, Habilitation Thesis, Darmstadt (1993) &lbrack;[pdf](https://www2.mathematik.tu-darmstadt.de/~streicher/HabilStreicher.pdf), [[Streicher-IntensionalTT.pdf:file]]&rbrack;

  
* {#Hofmann95} [[Martin Hofmann]], _Extensional concepts in intensional type theory_, Ph.D. thesis, University of
Edinburgh, (1995) ([ECS-LFCS-95-327](http://www.lfcs.inf.ed.ac.uk/reports/95/ECS-LFCS-95-327/), [[HofmannExtensionalIntensionalTypeTheory.pdf:file]])
  
Intensional type theory is discussed in chapter 4 of:

* {#AngiuliGratzer} [[Carlo Angiuli]], [[Daniel Gratzer]], *Principles of Dependent Type Theory* ([pdf](https://www.danielgratzer.com/papers/type-theory-book.pdf))

[[!redirects intensional type theories]]
