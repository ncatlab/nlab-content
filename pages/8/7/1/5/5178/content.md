## Idea

When doing [[category theory]] relative to a base [[topos]] $S$ (or other more general sort of [[category]]), the objects of $S$ are thought of as replacements for [[sets]].  Since often in category theory we need to speak of "a set-indexed family of objects" of some category, we need a corresponding notion in "category theory over $S$."  An **$S$-indexed category** is a category $\mathbb{C}$ together with, for every object $X\in S$, a notion of "$X$-indexed family of objects of $\mathbb{C}$."

## Definition

For any category $S$, an **$S$-indexed category** is simply a [[pseudofunctor]] $S^{op}\to Cat$.  (Equivalently, we may think of it as a [[Grothendieck fibration]] over $S$, and this is sometimes convenient.)  We write the image of $X\in S$ as $\mathbb{C}^X$ and call it "the category of $X$-indexed families of objects of $\mathbb{C}$."  Similarly, we write the image of a morphism $u\colon X\to Y$ as $u^*\colon \mathbb{C}^Y\to \mathbb{C}^X$.

Similarly, an [[indexed functor]] is a [[pseudonatural transformation]], and an indexed natural transformation is a [[modification]].  This defines the [[2-category]] $S IndCat$ of $S$-indexed categories.

## Examples

* If $S$ has [[pullbacks]], then its [[codomain fibration]] is an $S$-indexed category denoted $\mathbb{S}$, with $\mathbb{S}^X = S/X$.  This indexed category represents $S$ itself in the world of $S$-indexed categories.

* If $F\colon S\to T$ is a [[functor]] and $\mathbb{C}$ is a $T$-indexed category, then we have an $S$-indexed category $F^*\mathbb{C}$ defined by $(F^*\mathbb{C})^X = \mathbb{C}^{F(X)}$.

* In particular, if $S$ and $T$ are [[finitely complete categories]] and $F\colon S\to T$ is a [[left exact functor]], then $F^*\mathbb{T}$ is an $S$-indexed category that represents $T$.  This situation frequently arises when $S$ and $T$ are [[toposes]] and $F$ is the [[inverse image]] part of a [[geometric morphism]].  In this way, if $S$ is a topos, then any topos *over* $S$ (i.e. an object of the [[slice 2-category]] $Topos/S$) gives rise to a topos *relative to* $S$, i.e. a "topos object" in the 2-category of $S$-indexed categories, and this operation can be shown to be fully faithful.

[[!redirects indexed categories]]
