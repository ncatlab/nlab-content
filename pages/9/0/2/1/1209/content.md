
# Bimonoids
* table of contents
{: toc}

## Definition

In a [[symmetric monoidal category]], a __bimonoid__ (or __bimonoid object__) is an object $B$ equipped with a structure of a [[monoid]] and a [[comonoid]] which are compatible in one of two equivalent ways: the comultiplication and the counit are morphisms of monoids or the multiplication and the unit are morphisms of comonoids.  The symmetry of the monoidal structure is involved in the definition of the tensor product $B\otimes B$ as monoids and as comonoids.

A bimonoid in [[Vect]] (with its usual [[tensor product]]) is generally called a __[[bialgebra]]__.

A bimonoid which additionally has an [[antipode]] (a map $s:B\to B$ satisfying an axiom that makes it act like "inverses" in a group) is called a __[[Hopf monoid]]__; a Hopf monoid in [[Vect]] is a __[[Hopf algebra]]__.

In a category with [[biproducts]], with the biproduct as the monoidal product, every object is a bimonoid in a unique way ([Caf&#233; post](http://golem.ph.utexas.edu/category/2010/09/bimonoids_from_biproducts.html).


## Non-symmetric variants

It is interesting how to generalize this notion in various nonsymmetric situations, for example involving [[braided monoidal category|braidings]], or in relative situations over noncommutative rings (e.g. Takeuchi bialgebroids). In the completely noncommutative situation of the monoidal category of endofunctors, one can look at various compatibilities between [[monad]]s and comonads or monads and tensor products, for example involving distributive laws.

As far as compatibility with tensor product is concerned, there is a notion of a bimonad and involves a version of [[distributive law]]s, hence it is related to a lifting problem:

* I. Moerdijk, Monads on tensor categories,
Category theory 1999 (Coimbra),
J. Pure Appl. Algebra 168 (2002), no. 2-3, 189--208 (MR2003e:18012)

* Korn&#233;l Szlach&#225;nyi, The monoidal Eilenberg&#8211;Moore construction and bialgebroids, J. Pure Appl. Algebra 182, no. 2--3 (2003) 287--315. 

For a dual version see 

* P. Mac Crudden, Opmonoidal monads, Theory Appl. Cat., Vol. 10, 2002, No. 19, pp 469-485, [link](http://www.tac.mta.ca/tac/volumes/10/19/10-19abs.html)

There is also a more subtle notion also called Hopf monad in

* R. Wisbauer, B. Mesablishvili, Bimonads and Hopf monads on categories, [arXiv:0710.1163](http://arxiv.org/abs/0710.1163)

In some of these generalized cases, one does not have a good notion of of antipode, so that the difference between bimonoids and Hopf monoids has to be stated in different terms.  A similar case is in the case of [[Hopf algebroid]]s and bialgebroids where there are natural general notions not involving antipodes:

* B. Day, R. Street, Monoidal bicategories and Hopf algebroids, Advances in Mathematics, 129, 1 (1997) 99--157 

* G. B&#246;hm, An alternative notion of Hopf algebroid; in "Hopf algebras in noncommutative geometry and physics",  31--53, Lecture Notes in Pure and Appl. Math., 239, Dekker, New York, 2005; [math.QA/0301169](http://arxiv.org/abs/math.QA/0301169)


[[!redirects bimonoid]]
[[!redirects bimonoids]]
[[!redirects bimonoid object]]
[[!redirects bimonoid objects]]
