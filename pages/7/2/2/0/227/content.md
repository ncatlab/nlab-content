#Definition#

A (unital, non-commutative) **ring** is (equivalently)

* a [[monoid]] [[internalization|internal to]] [[Ab]].  
* a [[enriched category|category enriched over]] [[Ab]] with one object.
* a [[ringoid]] with one object.

Here $Ab$ is the category of [[abelian group|abelian groups]], made into a monoidal category using the tensor product of abelian groups.  A *commutative* (unital) ring is an [[abelian monoid]] object in [[Ab]].

+--{: .query}
[[Mike Shulman]]: I think this is a bit confusing.  I've never heard anyone talk about "a monoid enriched over" something.  A ring is a one-object *category* enriched over Ab, or a monoid in the monoidal category Ab.

Zoran: I agree wit Mike. Toby ?

_Toby_:  What could a monoid enriched over $C$ be other than a $1$-object (or pointed connected) category enriched over $C$?
=--

Don't worry: these definitions equivalent to [the one you're used to](http://en.wikipedia.org/wiki/Ring_mathematics#Definition).

In usual ring theory people often talk about nonunital rings as well: multiplicative [[semigroup]]s with additive [[abelian group]] structure where the multiplication is distributive toward addition.  As in the unital case, if the semigroup is abelian then the ring is said to be **commutative**.  One can define a semigroup object in any [[monoidal category]] simply by leaving off the unit condition of a monoid object; then a semigroup object in $Ab$ is a nonunital ring.  In order to talk about commutative semigroups, of course the monoidal category needs to be symmetric. To internalize $Ab$ to internal abelian group objects in a monoidal category it also needs to be symmetric. Thus one has a notion of a (unital or not) ring object in any symmetric monoidal category. 

There is another generalization of rings: generalizing $k$-algebras to $A$-rings. Instead of a commutative unital ring $k$ (for algebras) take any (nonunital noncomutative) ring $A$. An $A$-ring $R$ is simply a monoid in the (nonsymmetric) monoidal category of $A$-bimodules. Every $A$-ring is a ring in the usual sense, in the sense that there is an obvious forgetful functor to the usual rings. In fact the unit map $A\to R$ is a morphism of rings, and the category of $A$-rings is precisely the [[coslice category]] $A/Ring$. Unfortunately, by the tradition, apart from being called $A$-rings, the objects (in Ring) *under* $A$ are usually called *rings over* $A$. Unlike for the $k$-algebras, the multiplication $R\times R\to R$ is not $A$-linear in the second factor, but only $\mathbb{Z}$-linear. 

So sometimes for a notion of a ring in a monoidal category one does not ask for an additive group structure if it is already present on the objects in that category: examples are simplicial rings and dg-rings, and $A$-rings. In other context e.g. a ring in a topos, one needs explicitly to combine a semigroup and an abelian group. The rings will be algebras over a composed operad (or monad) of a semigroup operad and an abelian group operad, using a standard [[distributive law]] for that situation in the sense of operads (or monads).

A dual notion to an $A$-ring is an $A$-[[coring]]. 

See the discussion 'quick algebra quiz' at [cafe](http://golem.ph.utexas.edu/category/2008/12/a_quick_algebra_quiz.html).

#Higher rings#

By replacing in the sentence "a ring is a [[monoid]] in [[Ab]]" the [[category]] of abelian groups with a [[higher category theory|higher category]] of _symmetric monoidal_ higher groupoids, one obtains higher notion of rings.

Of particular interest is the maximal case of symmetric monoidal [[∞-groupoid]]s and, even more generally, that of [[spectrum|spectra]]. A [[monoid in an (∞,1)-category]] in the [[stable (∞,1)-category of spectra]] is an [[A-infinity-ring]] or [[associative ring spectrum]]. The commutative case is a [[commutative monoid in an (∞,1)-category]]: an [[E-infinity ring]] or [[commutative ring spectrum]].


[[!redirects rings]]
[[!redirects unital ring]]
[[!redirects unital rings]]
[[!redirects associative ring]]
[[!redirects associative rings]]
[[!redirects associative unital ring]]
[[!redirects associative unital rings]]
[[!redirects commutative ring]]
[[!redirects commutative rings]]
[[!redirects commutative unital ring]]
[[!redirects commutative unital rings]]
