
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Higher category theory
+-- {: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[higher category theory]], a concept of _opetopic omega-category_ is one of _[[weak omega-category]]_ modeled [[opetope|opetopic]] [[geometric shape for higher structures|shapes]].

There arevarious flavors of the definition. Typically they all say that an opetopic omega-catgeory is an [[opetopic set]] equipped with certain [[structure]] and [[property]]. 

## Definitions

### By Baez-Dolan

([Baez-Dolan 97](#BaezDolan97))

### By Makkai

([Hermida-Makkai-Power 01](#HermidaMakkaiPower01), [Makkai](#Makkai))

The actual definition of opetopic $\omega$-categories, called "multitopic $\omega$-categories" here, appears on p.57 of ([Makkai](#Makkai)).

### By Palm
 {#DefinitionByPalm}

In the definition by ([Palm](#Palm)) of opetopic $\omega$-category, the extra [[structure]] on an [[opetopic set]] is that some cells are labeled as "thin" (as [[equivalences]]) and the extra [[property]] are two classes of higher dimensional [[horn]]-filler conditions:

1. given a [[horn]] ("niche", "nook") obtained from an [[opetope]] by discarding the [[codimension]]-0 interior and the outgoing [[codimension]]-1 face, then there is a filler opetope whose codimension-0 interior is marked as an equivalence. The filling outgoing codimension-1 face is marked an equivalence if all the other codimension-1 faces are.

1. given a [[horn]] ("niche", "nook") obtained from an [[opetope]] by discarding the [[codimension]]-0 interior and an incoming codimension-1 face such that all the remaining codimension-1 faces are marked as equivalences, then there exists a filler both whose codimension-1 and codimension-0 cell are marked as equivalences.

This definition has been given a [[syntax|syntactic]] formulation by ([Finster 12](#Finster12)) in terms of _[[opetopic type theory]]_.

However, there is no saturation condition in this definition.

## References

An overview is in [chapter 4](http://cheng.staff.shef.ac.uk/guidebook/guidebook-new.pdf#page=63) of 

* [[Eugenia Cheng]], [[Aaron Lauda]], _Higher dimensional categories: an illustrated guidebook_ ([pdf](http://cheng.staff.shef.ac.uk/guidebook/guidebook-new.pdf))

and in chapter 7 of 

* [[Tom Leinster]], _Higher operads, higher categories_, London Math. Soc. Lec. Note Series __298__, [math.CT/0305049](http://arxiv.org/abs/math.CT/0305049)

Opetopes were introduced here:

* {#BaezDolan97} [[John Baez]], [[James Dolan]], Higher-dimensional algebra
III: $n$-categories and the algebra of opetopes, _Adv. Math._ **135** (1998), 145--206. ([arXiv:q-alg/9702014](http://arxiv.org/abs/q-alg/9702014))

Some mistakes were corrected in subsequent papers:

* [[Eugenia Cheng]], The category of opetopes and the category of opetopic sets,
_Th. Appl. Cat._ **11** (2003), 353--374.
[arXiv:0304284](http://arxiv.org/abs/math/0304284))

* [[Tom Leinster]], _Structures in higher-dimensional
category theory_, ([arXiv:0109021](http://arxiv.org/abs/math/0109021))

Makkai and collaborators introduced a slight variation they called 'multitopes':

* {#HermidaMakkaiPower01} [[Claudio Hermida]], [[Michael Makkai]], [[John Power]], _On weak higher-dimensional categories I, II_ _Jour. Pure Appl. Alg._ **157** (2001), 221--277 ([journal](http://www.sciencedirect.com/science/article/pii/S0022404999001796), [ps.gz files](http://www.math.mcgill.ca/makkai/multitopicsets/))

* {#Makkai} [[Michael Makkai]], The multitopic $\omega$-category of all multitopic $\omega$-categories. 
([pdf](http://www.math.mcgill.ca/makkai/mltomcat04/mltomcat04.pdf), [web](http://www.math.mcgill.ca/makkai/mltomcat04/))

Cheng has carefully compared opetopes and multitopes, and various approaches to opetopic $n$-categories:

* {#Cheng03} [[Eugenia Cheng]], _Weak $n$-categories: comparing opetopic foundations_, Jour. Pure Appl. Alg. **186** (2004), 219--231.
 ([arXiv:0304279](http://arxiv.org/abs/math/0304279))

* {#Cheng04} [[Eugenia Cheng]], _Weak $n$-categories: opetopic and multitopic
foundations_, Jour. Pure Appl. Alg._**186** (2004), 109--137.([arXiv:0304277](http://arxiv.org/abs/math/0304277))


She has also shown that opetopic [[bicategories]] are "the same" as the ordinary kind:

* [[Eugenia Cheng]], Opetopic bicategories: comparison with the classical theory.  ([arXiv](http://arxiv.org/abs/math/0304285))

A higher dimensional [[string diagram]]-notation for opetopes was introduced (as "zoom complexes" in section 1.1) in

* {#KockJoyalBataninMascari07} [[Joachim Kock]], [[André Joyal]], [[Michael Batanin]], [[Jean-François Mascari]], _Polynomial functors and opetopes_ ([arXiv:0706.1033](http://arxiv.org/abs/0706.1033)) 

Animated exposition of this higher-dimensional string-diagram notation is in 

* [[Eric Finster]], _Opetopic Diagrams 1 - Basics_ ([video](http://www.youtube.com/watch?v=OANwLohwJqk))

* [[Eric Finster]], _Opetopic Diagrams 2 - Geometry_ ([video](http://www.youtube.com/watch?v=E7OvuA1jRKM))


The variant of [Palm opetopic omega-categories](opetopic+omega-category#DefinitionByPalm) is due to 

* {#Palm} [[Thorsten Palm]], ...

A [[syntax|syntactic]] formalization of [[opetopic omega-categories]] in terms of [[opetopic type theory]] is in 

* {#Finster12} [[Eric Finster]], _Type Theory and the Opetopes_, talk at [Polish Seminar on Category Theory and its Applications, June 2012](http://www.mimuw.edu.pl/~zawado/SemTK/OSTKA.html)  ([pdf](http://sma.epfl.ch/~finster/opetope/types-and-opetopes.pdf))





[[!redirects opetopic omega-categories]]

[[!redirects opetopic ∞-category]]
[[!redirects opetopic ∞-categories]]