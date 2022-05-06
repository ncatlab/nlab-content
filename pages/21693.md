
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


* table of contents
{: toc}


## Idea

In the context of an account of [[logic]] described in terms of $n$-theories ([Shulman 18a](#Shulman18a)), a *3-theory* specifies a kind of [[2-category]].
It does so by prescribing the allowable judgment structures of the [[2-theories]] that can be expressed within it.

## Examples

1.  The 3-theory of (totally unstructured) 2-categories.  Syntactically, this corresponds to "unary type (2-)theories" with judgments such as $x:A \vdash b:B$ with exactly one type to both the left and the right of the turnstile ([LS 15](#LS15)). 

1. The 3-theory of cartesian monoidal 2-categories (or cartesian 2-multicategories).  Syntactically, this corresponds to "simple type (2-)theories" with judgments such as $x:A, y:B, z:C \vdash d:D$ with a finite list of types to the left but exactly one type to the right, and no dependent types ([LSR 17](#LSR17)).

1. The 3-theory of first-order logic. Syntactically, this corresponds to type 2-theories with one layer of dependency: there is one layer of types which cannot depend on anything, and then there is a second layer of types (“propositions” in the logical reading) which can depend on types in the first layer, but not on each other. 2-theories here are for hyperdoctrines and indexed monoidal categories, and include (typed) first-order classical logic, first-order intuitionistic logic, first-order linear logic, the type theory of indexed monoidal categories, first-order modal logic, etc. Semantic 2-theories in this 3-theory should be a sort of “2-hyperdoctrine”. 

1. The 3-theory that corresponds syntactically to "dependent type (2-)theories" with judgments such as $x:A, y:B(x), z:C(x, y) \vdash d:D(x, y, z)$. The semantic version of this should be some kind of "comprehension 2-category" ([Shulman 18b](#Shulman18b)). [[Homotopy type theory]] is a 2-theory defined in this 3-theory.

1. The 3-theory that corresponds syntactically to "classical simple type (2-)theories" with judgments such as $A,B,C \vdash D,E$ that allow finite lists of types on both sides of the turnstile.  For instance, the 2-theory of $\ast$-autonomous categories (classical linear logic), and also of Boolean algebras (classical nonlinear logic), live in this 3-theory, as does the 2-theory for symmetric monoidal categories described in ([Shulman 19](#Shulman19)). Variants would allow composition along multiple types at once (corresponding to a prop), composition only along one type at a time (corresponding to a polycategory), or both.

A 3-theory may be said to subsume another 3-theory, in the sense that a [[2-theory]] written in the latter may be formulated in the former. Here the first four 3-theories are ordered in terms of increasing expressivity. (5) subsumes (2), but (4) and (5) are not comparable.


## References

* {#Shulman18a} [[Mike Shulman]], _What Is an n-Theory?_, ([blog post](https://golem.ph.utexas.edu/category/2018/04/what_is_an_ntheory.html))

* {#LS15} [[Dan Licata]], [[Mike Shulman]], _Adjoint logic with a 2-category of modes_, in _[Logical Foundations of Computer Science 2016](http://lfcs.info/lfcs-2016/)_ ([pdf](http://dlicata.web.wesleyan.edu/pubs/ls15adjoint/ls15adjoint.pdf), [slides](http://dlicata.web.wesleyan.edu/pubs/ls15adjoint/ls15adjoint-lfcs-slides.pdf))

* {#LSR17} [[Daniel Licata]], [[Mike Shulman]], and [[Mitchell Riley]], _A Fibrational Framework for Substructural and Modal Logics (extended version)_, in Proceedings of 2nd International Conference on Formal Structures for Computation and Deduction (FSCD 2017) ([doi: 10.4230/LIPIcs.FSCD.2017.25](http://drops.dagstuhl.de/opus/volltexte/2017/7740/), [pdf](http://dlicata.web.wesleyan.edu/pubs/lsr17multi/lsr17multi-ex.pdf))

* {#Shulman18b} [[Mike Shulman]], _Type 2-theories_, ([HoTTEST seminar](https://www.uwo.ca/math/faculty/kapulkin/seminars/hottest.html))

* {#Licata18} [[Dan Licata]], _Synthetic Mathematics in Modal Dependent Type Theories_, tutorial at _[Types, Homotopy Theory and Verification](https://www.him.uni-bonn.de/programs/current-trimester-program/types-sets-constructions/workshop-types-homotopy-type-theory-and-verification/)_, 2018 ([pdf](http://dlicata.web.wesleyan.edu/pubs/lsr17multi/him-tutorial.pdf))

* {#Shulman19} [[Mike Shulman]], _A practical type theory for symmetric monoidal categories_, ([arXiv:1911.00818](https://arxiv.org/abs/1911.00818))