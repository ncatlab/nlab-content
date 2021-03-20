
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Modalities, Closure and Reflection
+-- {: .hide}
[[!include modalities - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea

The refinement of [[modal type theory]] to [[homotopy type theory]]: hence homotopy type theory equipped with [[modalities]] as in [[modal logic]] (and in [[modal type theory]]).

## Definitions

There are a number of different but equivalent ways to define a [[modality]] in [[homotopy type theory]]. From [Rijke, Shulman, Spitters 17](#RSS):

* Higher modality: A modality consists of a modal operator $L : {Type} \to {Type}$ and for every type $X$ a modal unit $(-)^L : X \to LX$ together with 

1. an induction principle of type
$$\text{ind} : ((a : A) \to LB(a^L)) \to ((u : LA) \to LB(u))$$
for any type $A$ and type $B$ depending on $LA$

1. a computation rule
$$\text{com} : \text{ind}(f)(a^L) = f(a).$$

1. a witness that for any $x, y : LA$, the modal unit $(-)^L : (x = y) \to L(x = y)$ is an equivalence.

* Uniquely eliminating modality: A modality consists of a modal operator and modal unit such that operation 
$$f \mapsto f \circ (-)^L : ((u : LA) \to LB(u)) \to ((a : A) \to LB(a^L))$$
is an equivalence for all types $A$ and types $B$ depending on $LA$.

* $\Sigma$-closed reflective subuniverse (aka localization): A reflective subuniverse (a.k.a. localization) consists of a proposition $isLocal : {Type} \to {Prop}$ together with an operator $L : {Type} \to {Type}$ and a unit $(-)^L : X \to LX$ such that $LX$ is local for any type $X$ and for any local type $Z$, then function 
$$f \mapsto f \circ (-)^L : (LA \to Z) \to (A \to Z)$$
is an equivalence. A localization is $\Sigma$-closed if whenever $A$ is local and for all $a : A$, $B(a)$ is local, then the dependent sum $\Sigma_{a : A} B(a)$ is local. 

* Stable factorization systems: A modality consists of an orthogonal factorization system $(\mathcal{L}, \mathcal{R})$ in which the left class is stable under pullback. 

* A localization (reflective subuniverse) whose units $(-)^L : X \to LX$ are $L$-connected.

We say that a type $X$ is $L$-modal if the unit $(-)^L : X \to LX$ is an equivalence. We say a type $X$ $L$-connected if $LX$ is contractible. 

In terms of the other structure, the stable factorization system associated to a modality $L$ has

* left class the $L$-connected maps, whose fibers are $L$-connected.

* right class the $L$-modal maps, whose fibers are $L$-modal.

Conversely, given a stable factorization system, the modal operator and unit are given by factorizing the terminal map.

## Related concepts

* [[reflective subuniverse]]

* [[stable homotopy type]]

* [[equivariant homotopy type]]

* [[geometric homotopy type theory]]

* [[cohesive homotopy type theory]]

* [[directed homotopy type theory]]

## References

See also the references at _[[modal type theory]]_.

### Review

* {#LicataWellen18} [[Dan Licata]], [[Felix Wellen]], _Synthetic Mathematics in Modal Dependent Type Theories_, tutorial at _[Types, Homotopy Theory and Verification](https://www.him.uni-bonn.de/programs/current-trimester-program/types-sets-constructions/workshop-types-homotopy-type-theory-and-verification/)_, 2018

  Tutorial 1, Dan Licata:  _A Fibrational Framework for Modal Simple Type Theories_
([recording](https://www.youtube.com/watch?v=uLLbSAYd3yI))

  Tutorial 2, Felix Wellen: _The Shape Modality in Real cohesive HoTT and Covering Spaces_ ([recording](https://www.youtube.com/watch?v=ACGjJDarEc4))

  Tutorial 3, Dan Licata: _Discrete and Codiscrete Modalities in Cohesive HoTT_ ([recording](https://www.youtube.com/watch?v=OHN9vEVPBN8))

  Tutorial 4, Felix Wellen, _Discrete and Codiscrete Modalities in Cohesive HoTT, II_ ([recording](https://www.youtube.com/watch?v=KXx9UDQdWPw))

  Tutorial 5, Dan Licata: _A Fibrational Framework for Modal Dependent Type Theories_ ([recording](https://www.youtube.com/watch?v=R4SsxUnIcng))

  Tutorial 6, Felix Wellen: _Differential Cohesive HoTT_, ([recording](https://www.youtube.com/watch?v=uEZXHPdwvJU&t=226s))

* {#Licata18} [[Dan Licata]], _Synthetic Mathematics in Modal Dependent Type Theories_, notes for tutorial at _[Types, Homotopy Theory and Verification](https://www.him.uni-bonn.de/programs/current-trimester-program/types-sets-constructions/workshop-types-homotopy-type-theory-and-verification/)_, 2018 ([pdf](http://dlicata.web.wesleyan.edu/pubs/lsr17multi/him-tutorial.pdf))

### General

* [[UF-IAS-2012]], _[Modal type theory](http://uf-ias-2012.wikispaces.com/Modal+type+theory)_

* {#HoTTBook} [Univalent Foundations Project](http://ncatlab.org/nlab/show/UF-IAS-2012), section 7.7 of _[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]_

* {#Shulman} [[Mike Shulman]], _Higher modalities_, talk at [[UF-IAS-2012]], October 2012  ([pdf](http://uf-ias-2012.wikispaces.com/file/view/modalitt.pdf))

* {#RSS} [[Egbert Rijke]], [[Mike Shulman]], [[Bas Spitters]], _Modalities in homotopy type theory_,  Logical Methods in Computer Science, January 8, 2020, Volume 16, Issue 1 ([arXiv:1706.07526](https://arxiv.org/abs/1706.07526), [episciences:6015](https://lmcs.episciences.org/6015))

* [[Mike Shulman]], _[http://homotopytypetheory.org/2015/07/05/modules-for-modalities/](http://homotopytypetheory.org/2015/07/05/modules-for-modalities/)_  (2015)

* [[Egbert Rijke]], [[Bas Spitters]], around def. 1.11 of _Sets in homotopy type theory_ ([arXiv:1305.3835](http://arxiv.org/abs/1305.3835))

* Kevin Quirin and Nicolas Tabareau, _Lawvere-Tierney Sheafification in Homotopy Type Theory_, [Workshop](http://hott-uf.gforge.inria.fr/2015/) talk 2015 ([pdf](http://hott-uf.gforge.inria.fr/2015/HOTTUF_Kevin.pdf)), Kevin Quirin [thesis](https://kevinquirin.github.io/thesis/main.pdf)

For a discussion of the [[reflective factorization system]] generated by a modality, see

* [[Felix Cherubini]], [[Egbert Rijke]], _Modal Descent_, ([arXiv:2003.09713](https://arxiv.org/abs/2003.09713))

See also 

* {#ChristensenRijke20} [[J. Daniel Christensen]], [[Egbert Rijke]], _Characterizations of modalities and lex modalities_ ([arXiv:2008.03538](https://arxiv.org/abs/2008.03538))

Outlook in view of [[cohesive homotopy type theory]]:

* {#Schreiber15} [[Urs Schreiber]], _[[schreiber:Some thoughts on the future of modal homotopy type theory]]_ , talk at: _[Homotopy Type Theory and Univalent Foundations - Mini-Symposium](https://sites.google.com/site/dmv2015hott/)_, within the _[German Mathematical Society meeting 2015](http://www.math.uni-hamburg.de/DMV2015/)_ 21st - 25th Sept 2015, Hamburg ([pdf notes](https://ncatlab.org/schreiber/files/SchreiberDMV2015b.pdf))


Introduction from the perspective of [[philosophy]]:

* [[David Corfield]], _Modal homotopy type theory_, 2017 ([PhilSci archive:15260](http://philsci-archive.pitt.edu/15260/))

* {#Corfield20} [[David Corfield]], _Modal homotopy type theory_, Oxford University Press 2020 ([ISBN: 9780198853404](https://global.oup.com/academic/product/modal-homotopy-type-theory-9780198853404))

Specifically for [[localization of a space|localization]] in the classical sense of [[algebraic topology]]:

* [[J. Daniel Christensen]], [[Morgan Opie]], [[Egbert Rijke]], [[Luis Scoccola]], _Localization in Homotopy Type Theory_, Higher Structures, 4(1) (2020), 1-32 ([arXiv:1807.04155](https://arxiv.org/abs/1807.04155))



Specifically for [[cohesive homotopy type theory]] see:

* [[Urs Schreiber]], [[Michael Shulman]], _[[schreiber:Quantum gauge field theory in Cohesive homotopy type theory]]_, in [[Ross Duncan]], [[Prakash Panangaden]] (eds.) _Proceedings 9th Workshop on Quantum Physics and Logic_, Brussels, Belgium, 10-12 October 2012 ([arXiv:1408.0054](http://arxiv.org/abs/1408.0054))

* {#Shulman15} [[Mike Shulman]], _Brouwer's fixed-point theorem in real-cohesive homotopy type theory_, Mathematical Structures in Computer Science Vol 28 (6) (2018): 856-941 ([arXiv:1509.07584](https://arxiv.org/abs/1509.07584), [doi:10.1017/S0960129517000147](https://doi.org/10.1017/S0960129517000147))

* {#Wellen18} [[Felix Wellen]], _[[schreiber:thesis Wellen|Cartan Geometry in Modal Homotopy Type Theory]]_ ([arXiv:1806.05966](https://arxiv.org/abs/1806.05966), [thesis pdf](http://www.math.kit.edu/iag3/~wellen/media/diss.pdf) following [Schreiber 15](#Schreiber15))

* {#Myers08} [[David Jaz Myers]], _Good Fibrations through the Modal Prism_ ([arXiv:1908.08034](https://arxiv.org/abs/1908.08034))

Formalization of the [[shape modality|shape]]/[[flat modality|flat]]-[[fracture square]] ([[differential cohomology hexagon]]) in [[cohesive homotopy type theory]]: 

* [[David Jaz Myers]], _Modal Fracture of Higher Groups_,  talk at _[CMU-HoTT Seminar](https://www.cmu.edu/dietrich/philosophy/hott/seminars/index.html), 2021 ([pdf](http://davidjaz.com/Talks/CMU_March_2021.pdf), [[MyersModalFracture2021.pdf:file]])


[[!redirects modal homotopy type theories]]

[[!redirects modal homotopy type]]
[[!redirects modal homotopy types]]