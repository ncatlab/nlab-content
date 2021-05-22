+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Monoid theory
+-- {: .hide}
[[!include monoid theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

An __absorption monoid__ or __annihilation monoid__ is a [[monoid]] $(M,1,\cdot)$ that is also an [[absorption magma]] $(M,0)$. 

## Properties

### Zero divisors

A non-zero element $a \in M$ is a __[[zero divisor]]__ if thete exists a non-zero element $b \in M$ such that $a \cdot b = 0$. 

### Localization and group completion

The [[localization of a monoid|localization]] of an absorption monoid at $0$ is the [[trivial group]]. Because of this, the [[group completion]] of any absorption monoid is the [[trivial group]]. This is why one speaks of [[division monoids]] instead of groups in the context of absorption monoids, and in particular, why the additive [[identity element]] in any [[trivial ring|nontrivial]] [[field]] has no multiplicative [[inverse]]. 

## Examples

* The [[extended natural numbers]] $(\bar{\mathbb{N}}, 0, +, \infty)$ are an absorption monoid. 

* Every [[integral monoid]] is an absorption monoid.

* The multiplicative monoid of every [[rig]] is an absorption monoid. 

* Every join-[[semilattice]] with a [[top element]] and evety meet-semilattice with a [[bottom element]] is an absorption monoid. 

## Related concepts

* [[monoid]]

* [[integral monoid]]

* [[zero divisor]]

* [[rig]], [[ring]], [[lattice]], [[field]]

[[!redirects absorption monoids]]
[[!redirects annihilation monoid]]
[[!redirects annihilation monoids]]