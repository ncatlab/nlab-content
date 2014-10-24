+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}

### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{:toc}

[[!redirects coHeyting boundary]]
[[!redirects Co-Heyting boundary]]
[[!redirects boundary operator]]


## Idea

In a [[co-Heyting algebra]] it is possible to define an equivalent to the [[boundary]] operation in [[topology]]. In applications this affords an intrinsic view of [[mereology]] without consideration of the embedding of bodies into an ambient space.

## Remark

As the lattice of [[subtopos|subtoposes]] of a given [[topos]] $\mathcal{E}$ comes naturally with a co-Heyting structure it becomes (in principle) possible to define the boundary $\partial\mathcal{A}$ of subtopos $\mathcal{A}$ in this lattice and then in turn the boundary $\partial T'$ of the [[geometric theory]] $T'$ that $\mathcal{A}$ classifies which is an extension of the theory $T$ classified by $\mathcal{E}$ (cf. Lawvere 1991, Caramello 2009).[^Law]

[^Law]: The boundary operation is one in Lawvere's arsenal of (mereological) tools for the study of logical theories in the context of a topos and its subtoposes (besides e.g. the [[Aufhebung|Aufhebungs relation]]). For a more complete picture of the toolbox see Lawvere (2002).

##Definition

Let $a$ be an element of a [[co-Heyting algebra]]. The **(co-Heyting) boundary** of $a$ is defined as $\partial a :=a\wedge\sim a$.

##Properties

* $\partial (a\wedge b) = (\partial a \wedge b)\vee (a\wedge\partial b)\quad$. (**Leibniz rule**)

* $\partial (a\vee b)\vee\partial (a\wedge b) =\partial a\vee\partial b\quad$.

* The boundaries $x=\partial a$ can be characterized as those $x$ with $\partial x = x$ (in particular, $\partial^2=\partial$), or, alternatively, those $x$ with $\sim x=1$, showing that boundary parts are precisely the (intuitively) _thin parts_.

* Every part is the sum of its _regular core_ and its boundary: $a=\sim\sim a\vee\partial a$. This suggests to view $\partial a$ as the _irregular_ part of $a$.

##Related entries

* [[boundary]]
* [[co-Heyting algebra]]
* [[Heyting algebra]]
* [[Heyting category]]
* [[mereology]]
* [[subtopos]]
* [[Aufhebung]]

##References


* [[Olivia Caramello|O. Caramello]], _Lattices of theories_ , arXiv:0905.0299v1 (2009). ([pdf](http://arxiv.org/pdf/0905.0299v1))

* {#KL89}[[G. M. Kelly]], F. W. Lawvere, _On the Complete Lattice of Essential Localizations_ , Bull.Soc.Math. de Belgique **XLI** (1989) pp.261-299.

* {#KRRZ10} C. Kennett, [[Emily Riehl|E. Riehl]], M. Roy, M. Zaks, _Levels in the toposes of simplicial sets and cubical sets_ , JPAA **215** no.5 (2011) pp.949-961. ([preprint](http://arxiv.org/abs/1003.5944))

* {#RRZ04} M. La Palme Reyes, [[Gonzalo E. Reyes|G. E. Reyes]], H. Zolfaghari, _Generic Figures and their Glueings_ , Polimetrica Milano 2004.

* {#Law86} [[William Lawvere|F. W. Lawvere]], _Introduction_ , pp.1-16 in _Categories in Continuum Physics_ , Springer LNM **1174** 1986.

* {#Law91a} F. W. Lawvere, _Intrinsic Co-Heyting Boundaries and the Leibniz Rule in Certain Toposes_ , pp.279-281 in Springer LNM **1488** (1991).

* {#Law94b} F. W. Lawvere, _Tools for the Advancement of Objective Logic: Closed Categories and Toposes_, pp.43-56 in: J. Macnamara, G. E. Reyes (eds.), _The Logical Foundations of Cognition_ , Oxford UP 1994.

* {#Law02} F. W. Lawvere, _Linearization of graphic toposes via Coxeter groups_ , JPAA **168** (2002) pp.425-436.

* [[Matías Menni|M. Menni]], C. Smith, _Modes of Adjointness_ , J. Philos. Logic **43** no.3-4 (2014) pp.365-391.

* T. Mormann, _Heyting Mereology as a Framework for Spatial Reasoning_ , Axiomathes **23** no.1 (2013) pp.237-264. ([draft](http://philpapers.org/go.pl?id=MORCMA-3&proxyId=&u=http%3A%2F%2Fphilpapers.org%2Farchive%2FMORCMA-3.pdf))

* P. Pagliani, _Intrinsic co-Heyting boundaries and information incompleteness in Rough Set Analysis_ , pp.123-130 in 
Polkowski, Skowron (eds.), _RSCTC 1998_ , Springer LNCS **1424** (2009).

* M. van Lambalgen, _Logical constructions suggested by vision_ , Proceedings of ITALLC98, CLSI 2000. ([draft](http://staff.science.uva.nl/~michiell/docs/ITALLCCSLI.pdf))

* C. Rauszer, _Semi-Boolean algebras and their applications to intuitionistic logic with dual operations_, Fund. Math. **83** no.3 (1974) pp.219-249. ([pdf](http://matwbn.icm.edu.pl/ksiazki/fm/fm83/fm83120.pdf))

* [[Gonzalo E. Reyes|G. E. Reyes]], H. Zolfaghari,  _Bi-Heyting Algebras, Toposes and Modalities_ , J. Phi. Logic **25** (1996) pp.25-43.

* M. Zarycki, _Quelque notions fondamentales de l'Analysis Situs au point de vue de l'Alg&#232;bre de la Logique_ , Fund. Math. **IX** (1927) pp.3-15. ([pdf](http://matwbn.icm.edu.pl/ksiazki/fm/fm9/fm912.pdf))

* H. Zolfaghari, _Topos et Modalit&#233;s_ , Th&#232;se de doctorat Universit&#233; de Montr&#233;al 1991.