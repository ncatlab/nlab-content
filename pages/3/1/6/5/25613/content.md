+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Essentially injective functors
* table of contents
{: toc}

## Idea

A [[functor]] $F\colon C \to D$ is **essentially injective** if it is [[injective]] on objects "up to isomorphism", namely on [[isomorphism classes]] of objects.


## Definition

$F\colon C \to D$ is **essentially injective** or **essentially injective on objects** if, for any two objects $c$ and $c'$ of $C$, if there is an [[isomorphism]] $F(c) \cong F(c')$ in $D$, then $c \cong c'$ in $C$. (The converse holds trivially, since functors preserve isomorphisms.) Equivalently, a functor is essentially injective if and only if it is [[injective]] on [[isomorphism classes]].

## Examples

* A functor between [[discrete categories]] (or, more generally, [[skeletal categories]]) is essentially injective iff it is a [[injective function]] between the classes of objects.

* An [[injective-on-objects functor]] is essentially injective if its image is [[skeletal category|skeletal]], but not generally otherwise.

* A [[composite]] of any two essentially injective functors is essentially injective.

* If $g f$ is essentially injective, then $f$ is essentially injective.

* A [[conservative functor]] is essentially injective when it is [[full functor|full]]. More generally, any [[pseudomonic functor]] is essentially injective. More generally still, any [[fully faithful functor]] is essentially injective.

* An [[isocofibration]] is a functor that is (strictly) injective on objects, and is hence essentially injective.

## Remark on terminology

Some sources call this property "isomorphism [[reflected limit|reflecting]]" or "isomorphism [[created limit|creating]]". However, such terminology more accurately refers to [[conservative functors]].

## Related concepts

[[!include properties of functors -- contents]]

## References

* [[Jiří Rosický]]. _Generalized Brown representability in homotopy categories_. Theory and Applications of Categories 20 (2008): 18-24.

[[!redirects essentially injective functors]]
[[!redirects essentially injective]]
[[!redirects essentially-injective-on-objects functor]]
[[!redirects essentially-injective-on-objects functors]]
[[!redirects essentially injective on objects functor]]
[[!redirects essentially injective on objects functors]]
[[!redirects essentially-injective-on-objects]]
[[!redirects essentially injective on objects]]
