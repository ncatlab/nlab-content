
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--


# Nuclear adjunctions
* table of contents
{: toc}


## Definition

A **nuclear adjunction** or **bimonadic adjunction** is an [[adjunction]] that is both [[monadic adjunction|monadic]] and [[comonadic adjunction|comonadic]].

One point in favour of the terminology "nuclear" over "bimonadic" is that the term **bimonadic functor** is sometimes used in the literature for a [[functor]] that is both [[monadic functor|monadic]] and [[comonadic functor|comonadic]], which is a different concept that is related to [[bimonads]].

## Properties

* Consider an adjunction $F \dashv G$, generating a [[monad]] $T$ and a [[comonad]] $D$. Under minimal assumptions on the categories, there is an adjunction between the category of $T$-algebras, and the category of $D$-coalgebras, and this adjunction is nuclear. See [Pavlovic–Hughes](#PavlovicHughes20).

* Consider an adjunction $F \dashv G : B \to A$, generating a [[monad]] $T$ and a [[comonad]] $D$. Assuming that $B$ is [[Cauchy complete]], $F$ is [[comonadic]] if and only if the free–forgetful adjunction associated to the [[Eilenberg–Moore category]] of $T$ is nuclear. See [Mesablishvili](#Mesablishvili06).

## References

* [[Michael Barr]]. _Coalgebras in a category of algebras_. Category Theory, Homology Theory and their Applications I: Proceedings of the Conference held at the Seattle Research Center of the Battelle Memorial Institute, June 24–July 19, 1968 Volume One. Berlin, Heidelberg: Springer Berlin Heidelberg, 2006.

* Paul Taylor's email to the [[categories mailing list]] "monadic completion of adjunctions" ([link](https://github.com/punkdit/categories/blob/26b751bbcbe6765fe447e805629ff6416f4c38b1/www.mta.ca/~cat-dist/catlist/1999/monadic-compl))

* {#Mesablishvili06} Bachuki Mesablishvili. _Monads of effective descent type and comonadicity_. Theory and Applications of Categories 16.1 (2006): 1-45. ([pdf](http://www.tac.mta.ca/tac/volumes/16/1/16-01.pdf))

* [[Matias Menni]]. _Bimonadicity and the explicit basis property_. Theory and Applications of Categories 26.22 (2012): 554-581. ([pdf](http://www.tac.mta.ca/tac/volumes/26/22/26-22.pdf))

* {#PavlovicHughes20} [[Dusko Pavlovic]], Dominic J. D. Hughes, _The nucleus of an adjunction and the Street monad on monads_ ([arXiv:2004.07353](https://arxiv.org/abs/2004.07353))


[[!redirects nuclear adjunctions]]
[[!redirects bimonadic adjunction]]
[[!redirects bimonadic adjunctions]]