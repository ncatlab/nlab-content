
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Homotopy theory
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[intensional type theory]] [[identity types]] behave like [[path space objects]]. This induces furthermore a notion of [[homotopy fibers]] hence of [[weak homotopy equivalence]]s between [[types]].

The _univalence axiom_ says that the original notion of paths and the notion of weak equivalence that it induces are compatible, in that 

**Univalence:** _For any two [[types]] $X,Y$, the type $X == Y$ of paths (in [[Type]]) between them is equivalent to the type $X \simeq Y$ of [[equivalences]] between them._

If this axiom is added to [[intensional type theory|intensional]] ([[Martin-Löf dependent type theory|Martin-Löf]]) [[dependent type theory]], one ontains [[homotopy type theory]].

The proposal ([Voevodsky](#Voevodsky)) that this provides a natively [[homotopy theory|homotopy theoretic]] [[foundation]] of [[mathematics]] goes by the name _Univalent Foundations Project_.

## Properties

The univalence axiom implies [[function extensionality]].


## References

The univalence axiom was introduced and promoted independntly by [[Steve Awodey]] and [[Vladimir Voevodsky]] around 2005/06.

* _Univalent Foundations Project_ ([pdf](http://www.math.ias.edu/~vladimir/Site3/Univalent_Foundations_files/univalent_foundations_project.pdf))

A quick survey is for instance in

* [[Peter Aczel]], _On Voevodsky's univalence axiom_ ([pdf](http://www.cs.man.ac.uk/~petera/Recent-Slides/Edinburgh-2011-slides_pap.pdf))

The [[HoTT]]-[[Coq]] code is at

* _[HoTT/Coq/Univalence.v](https://github.com/HoTT/HoTT/blob/master/Coq/Univalence.v)_

* _[HoTT/Coq/UnivalenceAxiom.v](https://github.com/HoTT/HoTT/blob/master/Coq/UnivalenceAxiom.v)_

A guided walk through the formal proof that univalence implies functional extensionality is at

* [[Andrej Bauer]], [[Peter LeFanu Lumsdaine]], _[[Oberwolfach HoTT-Coq tutorial]]_


For more references see _[[homotopy type theory]]_.


[[!redirects univalence]]
[[!redirects univalent foundations]]