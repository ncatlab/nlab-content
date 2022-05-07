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

## Idea

One should be able to abstract away the additive structure of an [[integral domain]] and just focus on the multiplicative structure, yielding the concept of _integral monoid_. 

## Definition

An [[absorption monoid]] $M$ is an __integral monoid__ if it is nontrivial and the submonoid $M \backslash \{0\}$ is a [[cancellative monoid]] (i.e., $1 \neq 0$ and left and right multiplication by $c$ is injective if $c \neq 0$, which may be combined as left and right multiplication by $c$ is injective if and only if $c \neq 0$). 

### In constructive mathematics

in constructive mathematics, there are different inequivalent ways to define an integral monoid

#### Discrete integral monoids

+-- {: .num_defn #discrete}
###### Definition

If we replace "left and right multiplication by $c$ is injective iff $c$ is nonzero" in the above definition by "left and right multiplication by $c$ is injective [[xor]] $c$ is zero" (which is equivalent in [[classical logic]] but stronger in [[constructive logic]]), then we obtain the notion of **discrete integral monoid**.  This condition implies that $0 \neq 1$.
=--

Such an integral monoid $M$ is 'discrete' in that it decomposes as a coproduct $M = \{0\} \sqcup M^\times$ (where $M^\times$ is the submomoid of $M$ that is cancellative). An advantage is that this is a [[coherent logic|coherent theory]] and hence also a [[geometric theory]].  A disadvantage is that this axiom is not satisfied (constructively) by the multiplicative monoid of the [[real numbers]] (however these are defined), although it is satisfied by the multiplicative monoid of the [[integers]] and the multiplicative monoid of the [[rational number|rationals]].

#### Heyting integral monoids

+-- {: .num_defn #heyting}
###### Definition

If we interpret $\neq$  as a [[tight apartness relation]], such that the [[absorption monoid]] becomes [[strong extensionality|strongly extensional]], then we obtain the notion of **Heyting integral monoid**. 
=--

This is how 'practising' constructive analysts of the Bishop school would define the simple word 'integral monoid'. 

An advantage is that the multiplicative monoid of the (located Dedekind) [[real numbers]] form a Heyting integral monoid. A disadvantage is that this is not a coherent axiom and so cannot be [[internalization|internalized]] in as many categories.

Of course, if the underlying set of the monoid has [[decidable equality]] ---as is true of the multiplicative monoids of $\mathbb{N}$, $\mathbf{Z}$, $\mathbf{Q}$, $\mathbf{Z}/n$, [[finite fields]], etc--- then a Heyting integral monoid is a discrete integral monoid.

## Examples

* An integral monoid whose largest submonoid not containing $0$ is a [[GCD monoid]] is called an __GCD integral monoid__. 

* An commutative integral monoid whose largest submonoid not containing $0$ is a [[unique factorization monoid]] is called an __unique factorization integral monoid__. 

* An integral monoid whose largest submonoid not containing $0$ is a [[Bézout monoid]] is called an __Bézout integral monoid__. 

* An integral monoid whose largest submonoid not containing $0$ is a [[principal ideal monoid]] is called an __principal ideal integral monoid__. 

* An integral monoid whose largest submonoid not containing $0$ is a [[group]] is called an __division monoid__. 

## Related concepts

* [[monoid]]

* [[absorption monoid]]

* [[cancellative monoid]]

* [[integral domain]], [[field]]

[[!redirects integral monoid]]
[[!redirects integral monoids]]

[[!redirects discrete integral monoid]]
[[!redirects discrete integral monoids]]

[[!redirects Heyting integral monoid]]
[[!redirects Heyting integral monoids]]
[[!redirects heyting integral monoid]]
[[!redirects heyting integral monoids]]

[[!redirects GCD integral monoid]]
[[!redirects GCD integral monoids]]
[[!redirects unique factorization integral monoid]]
[[!redirects unique factorization integral monoids]]
[[!redirects Bézout integral monoid]]
[[!redirects Bézout integral monoids]]
[[!redirects principal ideal integral monoid]]
[[!redirects principal ideal integral monoids]]
[[!redirects division monoid]]
[[!redirects division monoids]]