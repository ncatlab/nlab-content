# Contents
* table of contents
{: toc}

## Definition

An __absorption monoid__ or __annihilation monoid__ is a [[monoid]] $(M,1,\cdot)$ that is also an [[absorption magma]] $(M,0)$. 

## Properties

### Zero divisors

A non-zero element $a \in M$ is a __[[zero divisor]]__ if thete exists a non-zero element $b \in M$ such that $a \cdot b = 0$. 

### Localization and group completion

The [[localization of a monoid|localization]] of an absorption monoid at $0$ is the [[trivial group]]. Because of this, the [[group completion]] of any absorption monoid is the [[trivial group]]. This is why one speaks of division monoids ([[#Division monoid|see below]]) instead of groups in the context of absorption monoids, and in particular, why the additive [[identity element]] in any [[trivial ring|nontrivial]] [[field]] has no multiplicative [[inverse]]. 

## Examples

### Integral monoids

An absorption monoid whose largest submonoid not containing $0$ is a [[cancellative monoid]] is called an __integral monoid__. 

### Unique factorization monoid

Let $M$ be an integral monoid. We say that an element $a\in M$ is a _unit_ if it is [[invertible element|invertible]]. A non-unit is called
[[irreducible element|irreducible]] if it can not be represented as a product of two non-units. 

A commutative integral monoid $M$ is a __unique factorization monoid__ if every non-unit has a factorization $u = m_1 \cdots m_n$ as a product of irreducible non-units and this decomposition is unique up to renumbering and rescaling the irreducibles by units. 

Put differently: $M$ is a unique factorization monoid precisely when the monoid of nonzero [[principal ideal of a monoid|principal ideals]] of $M$ is a [[commutative monoid]] [[free object|freely generated]] by irreducible principal ideals.

### Division monoid

An integral monoid such that all non-zero elements are invertible is called a __division monoid__. Equivalently, a  division monoid is an absorption monoid whose largest submonoid not containing $0$ is a [[group]]. 

### Other examples

* The multiplicative monoid of every [[rig]] is an absorption monoid. 

* Every join-[[semilattice]] with a [[top element]] and evety meet-semilattice with a [[bottom element]] is an absorption monoid. 

## See also

* [[monoid]]

* [[zero divisor]]

* [[rig]], [[ring]], [[lattice]], [[integral domain]] [[field]]

[[!redirects absorption monoids]]
[[!redirects annihilation monoid]]
[[!redirects annihilation monoids]]
[[!redirects integral monoid]]
[[!redirects integral monoids]]
[[!redirects unique factorization monoid]]
[[!redirects unique factorization monoids]]
[[!redirects unique factorisation monoid]]
[[!redirects unique factorisation monoids]]
[[!redirects division monoid]]
[[!redirects division monoids]]