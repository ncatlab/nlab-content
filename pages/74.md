
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea 

**Enriched category theory** is the [[category theory]] of [[enriched categories]].

Pretty much every notion of ordinary category theory has its analog in enriched category theory, and, by taking the enriching category to be [[Set]], enriched category theory subsumes all of the theory of [[locally small categories]].

Enriched categories have a multitude of uses and applications, that makes studying their general theory quite worthwhile.

## Applications

### As a tool in higher category theory 

Enriched categories may be used to model objects in [[higher category theory]]: if the objects of the enriching category $V$ behave themselves as [[(n,r)-categories]], then a $V$-[[enriched category]] behaves like a (possibly special) $(n+1,r+1)$-category.

For instance 

* a [[Cat]]-enriched category is a [[strict 2-category]];

* since a [[simplicial set]] that is a [[Kan complex]] is a model for an [[∞-groupoid]], a [[Kan complex]]-enriched category is a model for an [[(∞,1)-category]];

* since a simplicial set that is a [[quasi-category]] is a model for an [[(∞,1)-category]], a quasi-category-enriched category is a model for an [[(∞,2)-category]].

In practice it is often useful to handle enriched categories such that only certain enriched [[full subcategories]] of them are the the desired models for objects in higher category theory. For instance often it is useful to work with general [[sSet-categories]] and have a prescription for how to find a [[Kan complex]]-enriched full subcategory inside them.

This is achieved notably by combining enriched category theory with [[model category]] theory:

an [[enriched model category]] or more generally an [[enriched homotopical category]] is an enriched category with extra information on how it behaves as a model in higher category. Notably [[sSet-model categories]] serve as models for [[(∞,1)-category theory]].


##Literature##

Textbook accounts include

* [[Max Kelly]], _Basic Concepts of Enriched Category Theory_, Cambridge University Press, Lecture Notes in Mathematics 64 (1982)

  Republished as: Reprints in Theory and Applications of Categories, No. 10 (2005) pp. 1-136 ([tac:10](http://www.tac.mta.ca/tac/reprints/articles/10/tr10abs.html), [pdf](http://www.tac.mta.ca/tac/reprints/articles/10/tr10.pdf))

* [[Francis Borceux]], Vol 2, chapter 6 of _[[Handbook of Categorical Algebra]]_, Cambridge University Press (1994)



Also

* [[Francis Borceux]], I. Stubbe, _Short introduction to enriched categories_ ([pdf](http://www-lmpa.univ-littoral.fr/~stubbe/PDF/EnrichedCatsKLUWER.pdf))


* [[Emily Riehl]], chapter 3 _Basics of enriched category theory_ in _[[Categorical Homotopy Theory]]_

For more references see at _[[enriched category]]_.



## Entries on Enriched Category Theory

### Monoidal categories

* [[monoidal category]]

  * [[tensor product]]

* [[closed category]]

  * [[internal hom]]

* [[closed monoidal category]]

* [[cartesian monoidal category]]

* [[braided monoidal category]], [[symmetric monoidal category]]

* [[Day convolution]]

* [[Bénabou cosmos]]

### Enriched functors

* [[enriched functor]]

* [[strong functor]]

* [[closed functor]], [[cartesian closed functor]]

### Generalizations of monoidal categories

* [[multicategory]]

* [[bicategory]]

* [[double category]]

* [[virtual double category]]


### Enriched categories

* [[enriched category]]

* [[enriched functor]]

  * [[enriched functor category]]

* [[category of V-enriched categories]]

* [[profunctor]]

* [[change of enriching category]]

### Universal constructions

* [[weighted limit]]

* [[end|ends and coends]]

* [[Kan extension]]

### Homotopical enrichment

* [[enriched homotopical category]]

* [[enriched model category]]

* [[model structure on homotopical presheaves]]

[[!redirects Enriched Category Theory]]
[[!redirects enriched]]