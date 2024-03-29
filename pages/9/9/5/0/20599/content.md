
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# Boolean locale
* tables of contents
{: toc}

## Definition

A [[locale]] $L$ is __Boolean__ if all of its opens (i.e. elements of the corresponding [[frame]]) are [[complemented]],
i.e., for any $a\in O(L)$ we have $a\vee\neg a=1$.
Equivalently, we could say that for all $a\in A$ we have $a=\neg\neg a$.

## Properties

The underlying [[frames]] of Boolean locales
are precisely [[complete Boolean algebras]].

Maps of Boolean locales are automatically [[open map|open]].
Their underlying [[morphisms of frames]]
are precisely [[complete Boolean homomorphisms]],
i.e., suprema-preserving homomorphisms of [[Boolean algebras]].

Thus, the opposite category of Boolean locales
is precisely the category of [[complete Boolean algebras]]
and complete homomorphisms thereof.

By [[Stonean duality]] the category of Boolean locales
is equivalent to the category of [[Stonean locales]]
and open maps thereof.
(Not every [[map of locales]] between [[Stonean locales]] is open, unlike for Boolean locales.)

Any [[locale]] $L$ has a maximal dense [[sublocale]],
whose opens are precisely the [[regular elements]] of $O(L)$,
i.e., elements $a\in O(L)$ such that $a=\neg\neg a$.
This sublocale is Boolean and is also known
as the [[double negation sublocale]].

## Related concepts

* [[complete Boolean algebra]]
* [[Stonean locale]]
* [[Stonean space]]

[[!redirects Boolean locales]]