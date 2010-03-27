
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

In a more restrictive sense, a **homomorphism** is a map of set's that preserves certain algebraic structure on these sets.

More generally, a _homomorphism_ may preserve whatever structure there is around. Even more generally, a homomorphism is just a [[morphism]] in the given [[category]] in which the gadgets under consideration are [[object]]s.

## As a map that respects binary products operations

Traditionally, a _homomorphism_ between two [[monoid]]s or [[group]]s or [[algebra]]s $A$ and $B$ is a map

$$
  \phi : A \to B
$$

of the underlying [[set]]s, that respects the product operation in that for all $a_1, a_2$ in $A$ we have

$$
  \phi(a_1 \cdot a_2) = \phi(a_1) \cdot \phi(a_2)
  \,.
$$

In this sense, the notion of homomorphism is a special case of that of [[functor]].

## More general definitions

But more generally a **homomorphism** between sets equipped with any algebraic structure is a map preserving this structure.  This can be made precise using [[Lawvere theories]] or [[monads]].  

Generalizing further, we may simply treat 'homomorphism' as a synonym for [[morphism]] in any [[category]], although there is a strong tendency to use 'homomorphism' in the case of 'algebraic' categories: for example, nobody seems to speak of a homomorphism between [[topological space]]s ([[continuous map]]s), or between [[manifold]]s.


[[!redirects homomorphisms]]