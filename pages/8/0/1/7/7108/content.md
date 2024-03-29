
# Graded sets
* table of contents
{: toc}

## Definition

Let $S$ be a [[set]].  Frequently, $S$ is a [[group]] or [[monoid]] (usually [[commutative monoid|commutative]]).

An **$S$-graded set** is an $S$-indexed [[family of sets]] $\{X_s\}_{s\in S}$. This can equivalently be described as a [[function]] $S \to Set$, or as a function $X \to S$ (a [[bundle]] with $X_s$ the [[fiber]] over $s\in S$).

The elements of $X_s$ are often said to have **degree** $s$.

Given a [[pair]] of $S$-graded sets $\{X_s\}_{s\in S}$ and $\{Y_s\}_{s\in S}$, a [[homomorphism]] between them is an $S$-indexed family of functions $\{f_s \colon X_s \to Y_s \}_{s\in S}$.  This can equivalently be described as a [[natural transformation]] between the two associated functions $S \to Set$, or as a function from $X$ to $Y$ that make the [[diagram]] with the associated functions $X \to S$ and $Y \to S$ [[commuting diagram|commute]].


## Examples

The most common choices of $S$ are probably:

* the [[natural numbers]] $\mathbb{N}$.

* the [[integers]] $\mathbb{Z}$.

* the [[cyclic group of order 2|2-element set]] $\mathbb{Z}/2$.  In this case, the elements of degree $0$ are often called **even**, and those of degree $1$ **odd**.


## Monoidal structures and enrichment

Suppose $(S,0,+)$ is a monoid, written additively.  Then the [[category]] $Set^S$ of $S$-graded sets has a [[closed monoidal category|closed]] [[monoidal category|monoidal]] [[mathematical structure|structure]], where

$$ (X \otimes Y)_s = \coprod_{u+v = s} (X_u \times Y_v) $$

This is a special case of [[Day convolution]].

Furthermore, this monoidal structure laxly interchanges with the pointwise product of graded sets:

$$ (X \times Y)_s := X_s \times Y_s $$

where the lax interchange maps $(X \times Y) \otimes (Z \times W) \to (X \otimes Z) \times (Y \otimes W)$ are given by inclusions. These interacting monoidal structures make $Set^S$ into a [[duoidal category]].

A $Set^S$-[[enriched category]] is a [[category]] whose [[morphisms]] all have degrees in $S$, and such that [[identity morphisms]] have degree $0$ and $deg(g f) = deg(g) + deg(f)$.  Note that its underlying ordinary category, in the usual sense of [[enriched category theory]], is the category of degree-$0$ morphisms.

More generally, we may grade by a monoidal category. This leads to the notion of [[locally graded category]].

## Graded objects

Given any set $S$ and any [[category]] $C$, the [[category]] of __$S$-graded objects of $C$__ is simply the [[functor category]] $C^S$ (identifying $S$ with its [[discrete category]]).  This includes graded sets as above, as well as [[graded abelian groups]], [[graded modules]], [[graded vector spaces]].  However, [[graded rings]] and [[graded algebras]] are not the same (and in particular require $S$ to be a [[monoid]]).

## Related concepts

* [[bigraded object]]

* [[graded module]]

* [[graded ring]]

* [[graded manifold]]

* [[differential-graded algebra]]

[[!redirects graded set]]
[[!redirects graded sets]]

[[!redirects graded object]]
[[!redirects graded objects]]
