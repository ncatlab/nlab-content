A __semigroup__ is like a [[monoid]] where there might not be an [[identity element]].  In other words, a semigroup is an associative [[magma]], that is a set equipped with an associative binary operation.

Some semigroups happen to be monoids; even then, a semigroup homomorphism might not be a monoid homomorphism (because it might not preserve the identity element).  Nevertheless, semigroup [[isomorphism]]s must be monoid isomorphisms.  Thus, the identity element of a monoid forms a [[property-like structure]] on the underlying semigroup.

[[category theory|Category theorists]] sometimes look with scorn on semigroups, because unlike a monoid, a semigroup is not an example of a [[category]] (although it is an example of a [[semicategory]]).

However, a semigroup can be promoted to a monoid by adjoining a new element and decreeing it to be the identity.  This gives a [[full and faithful functor]] from the category of semigroups to the category of monoids.  So, a semigroup can actually be seen as a monoid with an extra property.

+-- {: .un_example}
###### Exercise

what is this property?
=--

We can [[internalization|internalize]] the concept of semigroup in any [[monoidal category]] (or even [[multicategory]]) $V$ to get a __semigroup object__ in $V$.


[[!redirects semigroups]]
[[!redirects semigroup object]]
[[!redirects semigroup objects]]