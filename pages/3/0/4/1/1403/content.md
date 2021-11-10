
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
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

In [[higher algebra]]/[[higher category theory]] one can define (generalized) [[algebra|algebraic structures]] [[internalization|internal]] to [[categories]] which themselves are equipped with certain algebraic structure, in fact with the _same kind_ of algebraic structure. In ([Baez-Dolan 97](#BaezDolan)) this has been called the _microcosm principle_.

> **Microcosm principle**: _Certain [[algebra|algebraic structures]] can be defined [[internalization|in]] any category equipped with a [[categorification|categorified version]] of the same structure._ 

A standard example is the notion of _[[monoid object]]_ which make sense in a _[[monoidal category]]_, and the notion of _[[commutative monoid object]]_ which makes sense in a _[[symmetric monoidal category]]_.

Moreover, in many cases the "internal" version of the structure can be identified with [[lax morphisms]] of categorified structures with [[terminal object|terminal]] domain.  For instance, a monoid in a monoidal category is equivalently a [[lax monoidal functor]] with terminal domain.  More generally, the categorified structure can often be generalized to a "virtual" ([[generalized multicategory]]-like) structure.

The term "microcosm principle" arises from the idea that the monoid object (the 'microcosm') can only thrive in a category (a 'macrocosm') that resembles itself. 

## Examples

* [[monoid objects]] can be defined in [[monoidal categories]] (categorified monoids), or more generally [[multicategories]] (virtual monoidal categories).
* [[commutative monoid objects]] can be defined in [[symmetric monoidal categories]], or more generally in [[braided monoidal categories]].
* Categorifying these examples, [[monoidal categories]] are instances of [[pseudomonoids]], which can be defined in any [[monoidal bicategory]].  There are also versions for braided, symmetric, closed, compact closed, and so on.
* [[trace in a bicategory|traces]] can be defined in bicategories equipped with a [[shadow]] (a categorified trace).
* [[categories]] are instances of [[monads]], which can be defined in any [[bicategory]] or more generally any [[double category]] (both a kind of categorified category) or [[virtual double category]].  This generalization includes [[internal categories]] and [[enriched categories]].
* [[enriched categories]] are also objects of the free cocompletion of an [[enriched bicategory]] under a kind of [[Kleisli object]].
* [[generalized multicategories]] are naturally defined internal to a [[virtual double category]], which is itself a kind of generalized multicategory.
* [[double categories]] are instances of [[intermonads]], which can be defined in any [[intercategory]] (a categorified double category).
* [[duoids]] (objects with two monoidal structures) can be defined in any [[duoidal category]] (a category with two monoidal structures).
* [[Frobenius algebras]] can be defined in any [[star-autonomous category]], and cocomplete $\ast$-autonomous posets are Frobenius algebras in the $\ast$-autonomous category [[Sup]], while [[promonoidal category|pro]]-$\ast$-autonomous categories are [[Frobenius pseudomonoids]] in the $\ast$-autonomous (indeed, compact closed) bicategory [[Prof]].
* The prototypical example of a [[2-fibration]] consists of internal [[fibrations in a 2-category]].
* [[type theories]] can be defined inside a "2-type theory"; see [[adjoint type theory]] and [[logical framework]].

## Formalizations

The microcosm principle is a general heuristic, but in some contexts, general versions of it can be defined and proven formally.  These do not generally include all examples, but often include many of them.

### For $n$-categorical operad algebras

[Baez and Dolan](#BaezDolan) gave the following precise definition: for any [[operad]] $\mathcal{O}$, an $n$-categorical $\mathcal{O}$-algebra internal to an $(n+1)$-categorical $\mathcal{O}$-algebra $A$ is a [[lax morphism]] from the [[terminal object|terminal]] $(n+1)$-categorical $\mathcal{O}$-algebra to $A.$

### For categorical algebras over cartesian monads

[Batanin](#Batanin) gave the following definition: for a [[cartesian monad]] $T$, an internal $T$-algebra in an algebra $A$ for the extension of $T$ to [[internal categories]] is a lax $T$-morphism from the [[terminal object|terminal]] such algebra to $A$.  More generally, $A$ can be an algebra for some other monad, for instance which builds in some commutativity.

### For categorical algebras over Lawvere theories

[Hasuo, Jacobs, and Sokolova](#HJS) gave the following very similar definition: for a [[Lawvere theory]] $L$, an internal $L$-algebra in a categorical $L$-algebra (an $L$-algebra in [[Cat]]) is a lax $L$-morphism from the [[terminal object|terminal]] such algebra to $A$.  They used this to prove a general result about the liftings of $L$-algebra structures to coalgebras.

### For algebras over (∞,1)-operads
 {#ForAlgebrasOverInfinityOperads}

Another such formalization was given (independently) in ([Lurie](##Lurie)) in the context of [[higher algebra]] in [[homotopy theory]]/[[(∞,1)-category theory]]:

given an [[(∞,1)-operad]] $\mathcal{O}$ we have:

1. an [[(∞,1)-category]] $\mathcal{C}$ equipped with algebraic structure as encoded by $\mathcal{O}$ -- an $\mathcal{O}$-[[monoidal (∞,1)-category]] -- is equivalently encoded by a [[coCartesian fibration of (∞,1)-operads]] $\mathcal{C}^\otimes \to \mathcal{O}^\otimes$;

1. an [[(∞,1)-algebra over an (∞,1)-operad]] over $\mathcal{O}$ can be defined internal to such a $\mathcal{O}$-monoidal $(\infty,1)$-category  $\mathcal{C}$ and is equivalently given by a [[section]] of this map. 

See at _[[(∞,1)-algebra over an (∞,1)-operad]]_ for examples and further details.

## Reference

The term "microcosm principle" was coined in

* [[John Baez]], [[James Dolan]], _Higher-Dimensional Algebra III_ ([arXiv:q-alg/9702014](http://arxiv.org/abs/q-alg/9702014))
 {#BaezDolan}

Discussion is in

* [The Microcosm Principle](http://golem.ph.utexas.edu/category/2008/12/the_microcosm_principle.html)

Other formalizations can be found in

* [[Michael Batanin]], _The Eckman-Hilton argument and higher operads_, [arxiv:0207281](https://arxiv.org/abs/math/0207281)
 {#Batanin}

* Ichiro Hasuo, [[Bart Jacobs]], and Ana Sokolova. (2008)  _The Microcosm Principle and Concurrency in Coalgebra_.  In: Amadio R. (eds) _Foundations of Software Science and Computational Structures_. FoSSaCS 2008. Lecture Notes in Computer Science, vol 4962. Springer, Berlin, Heidelberg. [doi:10.1007/978-3-540-78499-9_18](https://doi.org/10.1007/978-3-540-78499-9_18), [paper](http://cs.uni-salzburg.at/~anas/papers/HasuoJS.pdf), [slides](http://cs.uni-salzburg.at/~anas/papers/MicrocosmPresentation.pdf), [more slides](http://cs.uni-salzburg.at/~anas/papers/Ohrid2008ana.pdf)
 {#HJS}

* Ichiro Hasuo, Chris Heunen, Bart Jacobs, Ana Sokolova, _Coalgebraic Components in a Many-Sorted Microcosm_,  International Conference on Algebra and Coalgebra in Computer Science CALCO 2009: Algebra and Coalgebra in Computer Science pp 64-80, ([pdf](http://homepages.inf.ed.ac.uk/cheunen/publications/2009/component/component.pdf))

* [[Jacob Lurie]], _[[Higher Algebra]]_
 {#Lurie}
