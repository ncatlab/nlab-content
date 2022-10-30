
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

_Modal type theory_ is a flavor of [[type theory]] with [[type formation rules]] for [[modalities]], as in [[modal logic]]. 

A survey of the field is in ([de Paiva-Gor&#233;-Mendler](#PaivaGoreMendler)).

## Properties

### Relation to monads
 {#RelationToMonads}

At least in many cases, modalities in type theory are identified with [[monads (in computer science)|(co)monads]] on the underlying [[type]] [[universe]]. 

See for instance ([Moggi, def. 4.7](#Moggi)), ([Benton-Bierman-de Paiva, section 3.2](#BentonBiermanPaiva)), ([Kobayashi](#Kobayashi)), ([Gabbay-Nanevski, section 8](GabbayNanevski)), ([Awodey-Birkedal, section 4.2](#AwodeyBirkedal)), ([Park-Harper, section 2.6](#ParkHarper)).

## Examples

### Geometric modality -- Grothendieck topology
 {#GeometricModality}

As a special case of the [modalities-are-monads](#RelationToMonads) relation,
a [[Grothendieck topology]] on the [[site]] underlying a [[presheaf topos]] is equivalently encoded in the [[sheafification]] [[monad]] $Sh(C) \to PSh(C) \hookrightarrow Sh(C)$ induced by the [[sheaf topos]] [[geometric embedding]]. Regarded internally as a [[modality]] this is the [[Lawvere-Tierney operator]] on the [[subobject classifier]]. This modal perspective on sheafification was maybe first made explicit by [[Bill Lawvere]]:

> A Grothendieck 'topology' appears most naturally as a modal operator of the nature 'it is locally the case that' ([[Bill Lawvere]] [9]).

More discussion along these lines is in ([Goldblatt 2006](#Golblatt2006)), where this kind of modality is called a _geometric modality_.

### Closure modality

The canonical monad on a [[local topos]] has been identified, in its internal language, with a closure modality in ([Awodey-Birkedal](#AwodeyBirkedal)).

### Cohesive and differential modality

By adding to [[homotopy type theory]] three modalities that encode [[discrete object|discrete types]] and [[codiscrete object|codiscrete types]] and hence implicitly a non-(co)-discrete notion of [[cohesion]] one obtained _[[cohesive homotopy type theory]]_. Adding furthermore modalities for _infinitesimal_ (co)discreteness yields [[differential homotopy type theory]].

## References
 {#References}

A survey of the field of modal type theory is in the collections

* M. Fairtlough, M. Mendler, [[Eugenio Moggi]] (eds.), _Modalities in Type Theory_, Mathematical Structures in Computer Science, Vol. 11, No. 4, (2001)

and

* [[Valeria de Paiva]], Rajeev Gor&#233;, Michael Mendler, _Modalities in constructive logics and type theories_, Special issue of the Journal of Logic and Computation, editorial pp. 439-446, Vol. 14, No. 4, Oxford University Press, (2004) ([pdf](http://www.cs.bham.ac.uk/~vdp/publications/final-preface.pdf))
 {#PaivaGoreMendler}

and 

* [[Valeria de Paiva]], Brigitte Pientka (eds.) _Intuitionistic Modal Logic and Applications (IMLA 2008)_, . Inf. Comput. 209(12): 1435-1436 (2011) ([web](http://www.sciencedirect.com/science/article/pii/S089054011100143X))


The historically first modal type theory, the interpretation of [[sheafification]] as a modality in the internal languagr of a [[Grothendieck]] topos goes back to the notion of [[Lawvere-Tierney operator]] and is disucssed in some detail in

* [[Robert Goldblatt]], _Grothendieck topology as geometric modality_, Mathematical Logic Quarterly, Volume 27, Issue 31-35, pages 495&#8211;529, (1981)
 {#Goldblatt}

A general relation between modalities in type theory and [[monads (in computer science)]] was noted in 

* [[Eugenio Moggi]], _Notions of computation and monads_ Information And Computation, 93(1), 1991. ([pdf](http://www.disi.unige.it/person/MoggiE/ftp/ic91.pdf))
 {#Moggi}

This was observed to systematically yield constructive modal logic in (independently)

*  P.N. Benton , G.M. Bierman , [[Valeria de Paiva]], _Computational Types from a Logical Perspective I_ (1995) ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.36.5778))
 {#BentonBiermanPaiva}

and

* M. Fairlough, M. Mendler, _Propositional lax logic_, Information and computation 137(1):1-33 (1997)
 {#FairloughMendler}

and

* Satoshi Kobayashi, _Monad as modality_, Theoretical Computer Science, Volume 175, Issue 1, 30 (1997), Pages 29&#8211;74
 {#Kobayashi}

The modal systems "CL" and "PLL" in ([Benton-Bierman-Paiva](#BentonBiermanPaiva)) and ([Fairlough-Mendler](#FairloughMendler)), respectively,  turn out to be equivalent to the geoemtric modality of [Goldblatt](#Goldblatt). The system CS4 in ([Kobayashi](#Kobayashi)) yields a constructive version of [[S4 modal logic]].

See also

* [[Frank Pfenning]], _Towards modal type theory_ (2000) ([pdf](http://www.cs.cmu.edu/~fp/talks/mantova00-talk.pdf))

* [[Frank Pfenning]], _Intensionality, Extensionality, and Proof Irrelevance in Modal Type Theory_, 	Pages 221&#8211;230 of: Symposium on Logic in Computer Science (2001) ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.28.5884))

* [[Aleksandar Nanevski]], [[Frank Pfenning]], Brigitte Pientka, _Contextual Model Type Theory_ (2005) ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.61.2356), [slides](http://wips.cs.umn.edu/slides/pientka.pdf)) 

* Giuseppe Primiero, _A multi-modal dependent type theory_ ([pdf](http://logica.ugent.be/centrum/preprints/primiero_PSPL10.pdf))

* Murdoch Gabbay, [[Aleksandar Nanevski]], _Denotation of contextual modal type theory (CMTT): syntax and metaprogramming_ ([pdf](http://www.gabbay.org.uk/papers/dencmt.pdf))
 {#GabbayNanevski}

A modality in the [[internal language]] of a [[local topos]] is discussed in section 4.2 of 

* [[Steve Awodey]], [[Lars Birkedal]], _Elementary axioms for local maps of toposes_, Journal of Pure and Applied Algebra, 177(3):215-230, (2003) ([ps](http://www.itu.dk/people/birkedal/papers/elealm.ps.gz), [[AwodeyBirkedalLocalTopos.pdf:file]] )
 {#AwodeyBirkedal}


* Sungwoo Park, [[Robert Harper]], _A modal language for Effects_ (2004) ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.2.8252))
 {#ParkHarper}

* [[Dan Licata]], [[Robert Harper]], _A Monadic Formalization of ML5_ ([arXiv:1009.2793](http://arxiv.org/abs/1009.2793))
 {#LicataHarper}

A list of related references is also kept at

* [[Valeria de Paiva]], _Intuitionistic Modal Logic Selected Publications_ ([web](https://docs.google.com/document/pub?id=1ASo__R-_Bzq9D9lGUo0xrfIxt_I9az7oqSg-wmP1K10))

[[!redirects modal type theories]]

[[!redirects geometric modality]]
[[!redirects geometric modalities]]

