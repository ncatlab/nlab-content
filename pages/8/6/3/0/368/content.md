
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The concept of an [[identity-on-objects functor]] is important for defining various structures in [[category theory]], such as [[Freyd categories]] and [[dagger categories]]. However, in a [[structural set theory]] such as [[ETCS]] or [[SEAR]], there is no concept of [[equality]] of [[sets]], and thus, an [[identity-on-objects functor]] cannot be defined via the usual definition. Instead, equality of sets is expressed through [[bijection]] of sets, which, when applied to the definition of identity-on-objects functor, yields a bijective-on-objects functor. 

In [[foundations]] where categories are weak by default and thus the collection of objects do not form a set, the concept of a bijective-on-objects functor still makes sense for [[strict categories]], where the functor is a [[strict functor]] by definition. 

## Definition

A [[strict functor]] between two [[strict categories]] is called **bijective-on-objects**, or **bo**, if it is a [[bijection]] on [[objects]].  

One reason bo functors are important is because together with [[full and faithful functors]] they form an [[weak factorization system|orthogonal factorization system]] on [[StrCat]]; see [[bo-ff factorization system]]. This factorization system can also be constructed using a [[generalized kernel]].

## Principle of equivalence

To be more in accord with the [[principle of equivalence]], one could require that the functor be bijective on objects only up to isomorphism; that is, it is [[essentially surjective functor|essentially surjective]] and [[full functor|full]] on isomorphisms.  However, from the point of view of [[factorization systems]], the version of the concept of a  bo functor which is in accord with the [[principle of equivalence]] is nothing more or less than an [[essentially surjective functor]], since essentially surjective functors and ff functors form a bicategorical factorization system on the [[bicategory]] $Cat$.

## Properties

[[R. Street]] in _[Categorical and combinatorial aspects of descent theory](http://arxiv.org/pdf/math/0303175)_ proves

Proposition. A functor is bijective on objects if and only if it exhibits its
codomain as the (2-categorical) [[descent object|codescent object]] of some simplicial category.

This can be generalized to any [[regular 2-category]].

## Related pages

* [[identity-on-objects functor]]

[[!include properties of functors -- contents]]

[[!redirects bijective-on-objects]]
[[!redirects bijective on objects]]

[[!redirects bijective on objects functor]]
[[!redirects bijective on objects functors]]

[[!redirects bijective-on-objects functor]]
[[!redirects bijective-on-objects functors]]


[[!redirects bo functor]]
[[!redirects bo functors]]

[[!redirects b.o. functor]]
[[!redirects b.o. functors]]

