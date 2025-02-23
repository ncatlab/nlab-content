
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--



# Contents
* table of contents
{:toc}

## Idea

In a restrictive sense, a homomorphism is a [[function]] between (the [[underlying sets]]) of two [[algebras]] that preserves the [[algebraic structure]].

More generally, a homomorphism is a function between [[structured sets]] that preserves whatever [[structure]] there is around. Even more generally, 'homomorphism' is just a synonym for '[[morphism]]' in any [[category]], the structured sets being generalised to arbitrary [[object]]s.

*Note: The word "homomorphism" has also traditionally been used for what we call a (weak) [[2-functor]] between [[bicategories]]*.

## Definitions

### Traditional (magmas, semigroups, groups, rngs)

Traditionally, a __homomorphism__ between two [[magmas]] $A$ and $B$ is a [[function]]

$$
  \phi\colon A \to B
$$

of the underlying [[set]]s that respects the binary operation in that for all $a_1, a_2$ in $A$ we have

$$
  \phi(a_1 \cdot a_2) = \phi(a_1) \cdot \phi(a_2)
  \,.
$$

This definition gives us the correct notion of __magma homomorphism__, __[[semigroup]] homomorphism__, and __[[group]] homomorphism__, but it is actually a bit of a coincidence that it works for groups.  It does *not* give the correct definition of [[monoid]] homomorphism, since it doesn\'t properly treat the [[identity elements]].  (However, the correct notion of monoid [[isomorphism]] can still be constructed from this inadequate definition of homomorphism.)

A __rng homomorphism__ is a function between [[rngs]] that is a homomorphism for both the additive group and the multiplicative semigroup.  (For [[rings with identity]], this is again inadequate.)


### Identity-preserving (monoids, rings)

A __homomorphism__ between two [[monoids]] $A$ and $B$ is a semigroup homomorphism

$$
  \phi\colon A \to B
$$

of the underlying [[semigroup]]s that preserves [[identity elements]] in that we have

$$
  \phi(1_A) = 1_B
  \,.
$$

This definition of __monoid homomorphism__ is a special case (via [[delooping]]) of the definition of [[functor]].

It is a theorem that a semigroup homomorphism between [[groups]] must be a monoid homomorphism (and additionally must preserve [[inverse elements]], which is also necessary to be the *correct* definition of __group homomorphism__.)

A __[[ring]] homomorphism__ is a function between rings that is a homomorphism for both the additive group and the multiplicative monoid.  Traditional [[ring theory]] sometimes actually uses rng homomorphisms even when the rngs in question are assumed to have identity elements, so be careful when reading old books.

A [[rig]] **homomorphism** is a function between rigs that is a homomorphism for both the additive monoid and the multiplicative monoid.

A [[semi-ring]] **homomorphism** is a function between semi-rings that is a homomorphism for both the additive semigroup and the multiplicative monoid.

### General

More generally, a **homomorphism** between sets equipped with any algebraic structure is a map preserving this structure.  This can be made precise using [[Lawvere theories]], [[monads]], etc.  

Generalizing further, we may simply treat 'homomorphism' as a synonym for '[[morphism]]' in any [[category]], although there is a strong tendency to use 'homomorphism' in the case of 'algebraic' categories: for example, nobody seems to speak of a homomorphism between [[topological space]]s ([[continuous map]]s), or between [[manifold]]s.  Here we put 'algebraic' in scare quotes to indicate the *field* of [[algebra]]; even morphisms in [[algebraic categories]] from other fields (such as the category of [[compacta]]) are not usually called homomorphisms.

## Examples

* an [[action]] homomorphism is an [[equivariant function]]

* a [[set]] homomorphism is an [[extensional function]]

* a homomorphism of sets with [[tight apartness relation]] is a [[strongly extensional function]]

* [[homomorphism of L-infinity algebras|homomorphism of $L_\infty$-algebras]]

## Related concepts

* homomorphisms are to [[functions]] as [[logical relations]] are to [[relations]]

* [[crossed homomorphism]]

[[!redirects homomorphism]]
[[!redirects homomorphisms]]

[[!redirects magma homomorphism]]
[[!redirects magma homomorphisms]]
[[!redirects semigroup homomorphism]]
[[!redirects semigroup homomorphisms]]
[[!redirects monoid homomorphism]]
[[!redirects monoid homomorphisms]]

[[!redirects group homomorphism]]
[[!redirects group homomorphisms]]

[[!redirects homomorphism of groups]]
[[!redirects homomorphisms of groups]]

[[!redirects abelian group homomorphism]]
[[!redirects abelian group homomorphisms]]
[[!redirects rng homomorphism]]
[[!redirects rng homomorphisms]]
[[!redirects ring homomorphism]]
[[!redirects ring homomorphisms]]
[[!redirects semi-ring homomorphism]]
[[!redirects semi-ring homomorphisms]]
[[!redirects rig homomorphism]]
[[!redirects rig homomorphisms]]
[[!redirects algebra homomorphism]]
[[!redirects algebra homomorphisms]]

[[!redirects field homomorphism]]
[[!redirects field homomorphisms]]



