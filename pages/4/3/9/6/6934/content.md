
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Overview

A [[dependent type|dependently typed]] [[functional programming language]] with applications to [[certified programming]]. It is also  used as a [[proof assistant]]. 

Besides [[Coq]], Agda is one of the languages in which [[homotopy type theory]] has been implemented ([Brunerie](#Brunerie)).
Agda can be compiled to Haskell, Epic or Javascript.

## Variants

### Cubical Agda
 {#CubicalAgda}

[Cubical Agda](https://agda.readthedocs.io/en/latest/language/cubical.html)  is a version of Agda (turned on by the flag `--cubical`) that implements a type theory similar to CCHM (De Morgan) [[cubical type theory]].

Its main difference from CCHM is that instead of an exotype of "cofibrant propositions" it uses the interval itself, replacing cofibrant propositions by statements of the form $r \equiv 1$ for some dimension expression $r$.  This change does not prevent the construction of a model for the theory in De Morgan [[cubical sets]], although it doesn't technically fall under the Orton-Pitts axioms since $I$ is not a subobject of $\Omega$, and no one has checked whether this model can be strengthened to a [[Quillen model category]].

More problematically, to support [[identity types]] a la Swan (which are distinct from both cubical "path types" and Martin-Lof "identity types" -- the latter sometimes called "jdentity types" to emphasize their definition relative to the J-eliminator) the type of cofibrant propositions must support a [[dominance]].  Cubical Agda thus assumes that $I$ supports a dominance, but this is not true in De Morgan cubical sets.  So the semantics of the entirety of Cubical Agda, with Swan identity types, is unclear.  (For this reason, the Cubical Agda library generally avoids using Swan identity types, although Cubical Agda supports them.)

Ordinary Martin-Lof [[jdentity types]] should, in principle, also be definable in Cubical Agda as an indexed inductive family, with computational behavior as usual for any inductive types in cubical type theory.  As of March 2021, however, there is a bug in Cubical Agda that prevents jdentity types from computing correctly.

### Guarded Cubical Agda

The guarded cubical variant extends cubical Agda to support [[guarded recursive]] definitions which can be used to formalize [[synthetic guarded domain theory]].

### Agda-flat
  {#AgdaFlat}
 

The variant `Agda-flat` implements a [[comonad|co-]][[idempotent monad|monadic]] [[modal operator]] $\flat$ ("flat", following the notation used in [[cohesive homotopy type theory]] as introduced in [[schreiber:dcct|dcct]] and type-theorertically developed in [Shulman 15](cohesive+homotopy+type+theory#Shulman15)). This makes Agda model a [[modal type theory]] and hence a [[modal homotopy type theory]], such as used, for instance, in [[schreiber:thesis Wellen|Wellen 2017]].

See:

* [`Agda-flat` documentation](https://agda.readthedocs.io/en/v2.6.2.2/language/flat.html)

* [installation instructions](http://www.cl.cam.ac.uk/~amp12/agda/internal-universes/code/agda-flat/install.txt)

## Related concepts

[[!include proof assistants and formalization projects -- list]]

## References
 {#References}

General information on Agda is at

* [Agda Wiki](http://wiki.portal.chalmers.se/agda/pmwiki.php)

* _['Hello World!' in Adga](http://progopedia.com/example/hello-world/251/)_

* _[learn-you-an-agda (and achieve enlightment)](https://github.com/liamoc/learn-you-an-agda)_


* [[Dan Licata]], Ian Voysey, _[Programming and proving in Agda](http://www.cs.cmu.edu/~drl/teaching/oplss13/)_


With emphasis on the [[dependent type theory]]-aspect:

* [[Ulf Norell]], _Towards a practical programming language based on dependent type theory_, PhD thesis (2007) &lbrack;[pdf](https://www.cse.chalmers.se/~ulfn/papers/thesis.pdf), [[Norell-PracticalDTT.pdf:file]]&rbrack;

* [[Ulf Norell]], *Dependently Typed Programming in Agda*, p. 230-266 in: *Advanced Functional Programming* AFP 2008. Lecture Notes in Computer Science **5832** (2009) &lbrack;[doi:10.1007/978-3-642-04652-0_5](https://doi.org/10.1007/978-3-642-04652-0_5), [pdf](https://www.cse.chalmers.se/~ulfn/papers/afp08/tutorial.pdf)&rbrack;


A tutorial for use of Agda as an implementation of [[homotopy type theory]] is at

* {#Brunerie} [[Guillaume Brunerie]], _Agda for homotopy type theory_ ([web](https://github.com/guillaumebrunerie/HoTT/tree/master/Agda/tutorial))
 
* [[Guillaume Brunerie]], _The Agda proof assistant_, slides,  [pdf](http://web.archive.org/web/20160101212359/http://uf-ias-2012.wikispaces.com/file/view/agda.pdf/390147250/agda.pdf)

and specifically of [[Cubical Agda]] as an implementation of [[cubical type theory]]:

* {#VMA19} [[homotopytypetheory:Andrea Vezzosi]], [[Anders Mörtberg]] and Andreas Abel, _Cubical Agda: A Dependently Typed Programming Language with Univalence and Higher Inductive Types_, 2019 ([pdf](http://www.cs.cmu.edu/~amoertbe/papers/cubicalagda.pdf))

On [[homotopy type theory]] and [[univalent foundations of mathematics]] in/with Agda:

* [[Martín Hötzel Escardó]], *Introduction to Univalent Foundations of Mathematics with Agda* &lbrack;[arXiv:1911.00580](https://arxiv.org/abs/1911.00580), [webpage](https://www.cs.bham.ac.uk/~mhe/HoTT-UF-in-Agda-Lecture-Notes/)&rbrack;

The HoTT-Agda library is at

* github, _[hott-agda](https://github.com/hott/hott-agda/)_

category: software

[[!redirects agda]]

[[!redirects Cubical Agda]]