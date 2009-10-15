A (unital, non-commutative) **ring** is (equivalently)

* a [[monoid]] [[internalization|internal to]] [[Ab]].  
* a [[monoid]] [[enriched category|enriched over]] [[Ab]].
* a [[ringoid]] with one object.

Here $Ab$ is the category of [[abelian group|abelian groups]], made into a monoidal category using the tensor product of abelian groups.  A *commutative* (unital) ring is an [[abelian monoid]] object in [[Ab]].

+--{: .query}
[[Mike Shulman]]: I think this is a bit confusing.  I've never heard anyone talk about "a monoid enriched over" something.  A ring is a one-object *category* enriched over Ab, or a monoid in the monoidal category Ab.
=--

Don't worry: these definitions equivalent to [the one you're used to](http://en.wikipedia.org/wiki/Ring_mathematics#Definition).

In usual ring theory people often talk about nonunital rings as well: multiplicative [[semigroup]]s with [[abelian group]] structure where the multiplication is distributive toward addition.  As in the unital case, if the semigroup is abelian than the ring is said to be **commutative**.  One can define a semigroup object in any [[monoidal category]] simply by leaving off the unit condition of a monoid object; then a semigroup object in $Ab$ is a nonunital ring.  In order to talk about commutative rings, of course the monoidal category needs to be symmetric.


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
