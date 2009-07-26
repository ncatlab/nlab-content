A semigroup is like a [[monoid]] where there might not be an [[identity element]].  In other words, a __semigroup__ is a set equipped with an associative binary operation.  Equivalently, we may define a semigroup to be an associative [[magma]].

Some semigroups happen to be monoids; even then, a semigroup homomorphism might not be a monoid homomorphism (because it might not preserve the identity element).  Nevertheless, semigroup [[isomorphisms]] must be monoid isomorphisms.  Thus, the identity element of a monoid forms a [[property-like structure]] on the underlying semigroup.

As a monoid is a [[category]] with one object, so a semigroup is a [[semicategory]] with one object.


# Attitudes Toward Semigroups #

<div style="float:left;margin:0 10px 10px 0;"><img src="http://math.ucr.edu/home/baez/centipede.jpg" alt="" width="208" height="150" /></div>
Some mathematicians consider semigroups to be a case of [[centipede mathematics]].  [[category theory|Category theorists]] sometimes look with scorn on semigroups, because unlike a monoid, a semigroup is not an example of a [[category]].    

However, a semigroup can be promoted to a monoid by adjoining a new element and decreeing it to be the identity.  This gives a [[full and faithful functor]] from the category of semigroups to the category of monoids.  So, a semigroup can actually be seen as a monoid with an extra property.

+-- {: .un_example}
###### Exercise  

What is this property?
=--

On the other hand, analysts run across semigroups often in the wild, and don\'t always want to add formal identities just to turn them into moniods.


# Internalization #

We can [[internalization|internalize]] the concept of semigroup in any [[monoidal category]] (or even [[multicategory]]) $V$ to get a __semigroup object__ in $V$.


[[!redirects semigroups]]
[[!redirects semigroup object]]
[[!redirects semigroup objects]]