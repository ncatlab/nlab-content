
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Categorical algebra
+-- {: .hide}
[[!include categorical algebra -- contents]]
=--
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
 {#Idea}

In [[functional programming]] using [[monads (in computer science)|monads for computational effects]], *monad transformers* &lbrack;[Espinosa 1994 §4](#Espinosa94), [1995 §2.6](#Espinosa95)&rbrack; are type constructors which take one monad to another in a compatible way.


In practice this is typically motivated by and used for *combining* a monadic effect $\mathcal{E}_{new}$ into any given one $\mathcal{E}$ by $\mathcal{E} \mapsto \mathcal{E}_{new} \circ \mathcal{E} $ via a universal [[distributive law]].

Formally, a monad transformer on a given category $\mathbf{C}$ (of [[data types|data]] [[types]]) is a [[pointed endofunctor]] on the [category of monads](monad#TransformationOfMonadsOnFixedCategory) $Mnd(\mathbf{C})$ (this is made explicit in [Winitzki 2022, p. 474](#Winitzki22)), namely:

1. an [[endofunctor]] $\mathcal{E} \mapsto \mathcal{E}'$ taking monads to monads

1. for each $\mathcal{E}$ a [morphism of monads](monad#TransformationOfMonadsOnFixedCategory) $trans_{\mathcal{E}} \,\colon\, \mathcal{E} \longrightarrow \mathcal{E}'$ (a *[[monad transformation]]*)

1. such that these are [[natural transformations|natural]] with respect to [morphism of monads](monad#TransformationOfMonadsOnFixedCategory).

This construction is sometimes viewed (see [HP07](#HP07), and at *[[Eff]]*) as a complication resulting from passing to monads from the setting of [[Lawvere theories]], where any two theories may be naturally combined.

## Related concepts

* [[monad transformation]]

## References

Original discussion:

* {#Espinosa94} [[David A. Espinosa]], §3.2 in: *Building Interpreters by Transforming Stratified Monads* (1994) &lbrack;[pdf](https://github.com/davidespinosa01/papers/blob/master/E/Espinosa%20David/espinosa-stratified-monads.pdf), [[Espinosa-StratifiedMonads.pdf:file]]&rbrack;

* {#Espinosa95} [[David A. Espinosa]], §2.6 in: *Semantic Lego*, PhD thesis, Columbia University (1995) &lbrack;[pdf](https://github.com/davidespinosa01/papers/blob/master/E/Espinosa%20David/espinosa-stratified-monads.pdf), [[Espinosa-SemanticLego.pdf:file]], slides:[pdf](https://github.com/davidespinosa01/papers/blob/346c2ded6af78805701106d51daee8f7a756c948/E/Espinosa%20David/espinosa-thesis-slides.pdf), [[Espinosa-SemanticLego-slides.pdf:file]]&rbrack;

* {#LiangHudakJones95} Sheng Liang, [[Paul Hudak]], [[Mark Jones]], *Monad transformers and modular interpreters*, POPL '95 (1995) 333–343 &lbrack;[doi:10.1145/199448.199528](https://doi.org/10.1145/199448.199528)&rbrack;


Textbook account:

* {#Winitzki22} [[Sergei Winitzki]], Section 14 of: *The Science of Functional Programming -- A tutorial, with examples in Scala* (2022) &lbrack;[leanpub:sofp](https://leanpub.com/sofp), [github:sofp](https://github.com/winitzki/sofp)&rbrack;

See also:

* Wikipedia, *[Monad transformer](https://en.wikipedia.org/wiki/Monad_transformer)*

* Haskell, *[Monad transformers](https://en.wikibooks.org/wiki/Haskell/Monad_transformers)*

* Bryan O'Sullivan, Don Stewart, and John Goerzen, _Monad transformers_, [Chapter 18](http://book.realworldhaskell.org/read/monad-transformers.html) of Real World Haskell.

* Chung-Chieh Shan, _Monad transformers_, [blog post](http://conway.rutgers.edu/~ccshan/wiki/blog/posts/Monad_transformers/)

* Mauro Jaskelioff, [[Eugenio Moggi]], _Monad Transformers as Monoid Transformers_, [pdf](http://www.disi.unige.it/person/MoggiE/ftp/tcs10.pdf)

* Oleksandr Manzyuk, _Calculating monad transformers with category theory_, [pdf](https://oleksandrmanzyuk.files.wordpress.com/2012/02/calc-mts-with-cat-th1.pdf)

* {#HP07} [[Martin Hyland]], [[John Power]], _The Category Theoretic Understanding of Universal Algebra: Lawvere Theories and Monads_, Electronic Notes in Theoretical Computer Science (ENTCS) archive Volume 172, April, 2007 Pages 437-458  ([pdf](https://www.dpmms.cam.ac.uk/~martin/Research/Publications/2007/hp07.pdf))

[[!redirects monad transformers]]

