## Idea

A **companion pair** in a [[double category]] is a way of saying that a horizontal arrow and a vertical arrow are "isomorphic," even though they do not live in the same 2-category.

## Definition

Let $f\colon A\to B$ be a vertical arrow and $f\colon A\to B$ a horizontal arrow in a double category.  These arrows are said to be a **companion pair** if they come equipped with 2-cells
$$
\array{ A & \overset{f'}{\to} & B \\
^f\downarrow & ^{\phi}\swArrow & \downarrow^{id} \\
B & \underset{id}{\to} & B} 
\qquad and\qquad
\array{ A & \overset{id}{\to} & A \\
^{id} \downarrow & ^{\psi}\swArrow & \downarrow^f \\
A & \underset{f'}{\to} & B }
$$
such that $\psi \circ_h \phi = id_f$ and $\phi \circ_v \psi = id_{f'}$, where $\circ_h$ and $\circ_v$ denote horizontal and vertical composition of 2-cells.

Given such a companion pair, we say that $f$ and $f'$ are **companions** of each other.

## Examples

* In the double category $\mathbf{Sq}(K)$ of squares ("quintets") in any 2-category $K$, a companion pair is simply an invertible 2-cell between two parallel 1-morphisms of $K$.

* In the double category $T$-**Alg** of algebras, lax morphisms, and colax morphisms for a [[2-monad]], an arrow (of either sort) has a companion precisely when it is a *strong* (= pseudo) $T$-morphism.  This is important in the theory of [[doctrinal adjunction]].

## Remarks

* The horizontal (or vertical) dual of a companion pair is a [[conjunction]].

* Companion pairs (and conjunctions) have a [[mate]] correspondence generalizing the calculus of mates in 2-categories.

* If every vertical arrow in some double category $D$ has a companion, then the functor $f\mapsto f'$ is a [[pseudofunctor]] $V D\to H D$ from the vertical 2-category to the horizontal one, which is the identity on objects, and locally fully faithful by the mate correspondence.  A choice of companions that make this a strict 2-functor is called a [[connection on a double category|connection]] on $D$.  On the other hand, if every vertical arrow also has a conjoint, then this makes $D$ into a [[proarrow equipment]], or equivalently a [[framed bicategory]].

* Companion pairs and mate-pairs of 2-cells between them in any double category $D$ form a 2-category $Comp(D)$.  The functor $Comp\colon DblCat \to 2Cat$ is right adjoint to the functor $Sq\colon 2Cat \to DblCat$ sending a 2-category to its double category of squares.

[[!redirects companion]]
[[!redirects companions]]
[[!redirects companion pairs]]
[[!redirects companion pair in a double category]]
