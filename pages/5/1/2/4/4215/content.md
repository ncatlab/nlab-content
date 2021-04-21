> This page is about conjunctions in double (or higher) categories; see [[logical conjunction]] for the meet of truth values.

***

#Contents#
* table of contents
{:toc}

## Idea

A **conjunction** in a [[double category]] is a way of saying that a horizontal arrow and a vertical arrow are [[adjunction|adjoint]], even though they do not live in the same 2-category.


## Definition

Let $f\colon A\to B$ be a vertical arrow and $g\colon B\to A$ a horizontal arrow in a double category.  These arrows are said to be a **conjunction** if they come equipped with 2-cells
$$
\array{ A & \overset{id}{\to} & A \\
^f\downarrow & ^{\eta}\swArrow & \downarrow^{id} \\
B & \underset{g}{\to} & A} 
\qquad and\qquad
\array{ B & \overset{g}{\to} & A \\
^{id} \downarrow & ^{\varepsilon}\swArrow & \downarrow^f \\
B & \underset{id}{\to} & B }
$$
such that $\varepsilon \circ_h \eta = id_g$ and $\eta \circ_v \varepsilon = id_{f}$, where $\circ_h$ and $\circ_v$ denote horizontal and vertical composition of 2-cells.

Given such a conjunction, we say that $f$ and $g$ are **conjoints** of each other, and that $g$ is the **right conjoint** of $f$ and that $f$ is the **left conjoint** of $g$.

## Examples

* In the double category $\mathbf{Sq}(K)$ of squares ([[quintets]]) in any 2-category $K$, a conjunction is simply an internal [[adjunction]] in $K$.

* In the [[double category of algebras | double category $T$-$\mathbf{Alg}$ of algebras, lax morphisms, and colax morphisms]] for a [[2-monad]] $T$, an conjunction is precisely a [[doctrinal adjunction]] between a colax morphism an a lax morphism.

## Remarks

* The horizontal (or vertical) dual of a conjunction is a [[companion pair]].

* Conjunctions (and companion pairs) have a [[mate]] correspondence generalizing the calculus of mates in 2-categories.

* If every vertical arrow in some double category $D$ has a right conjoint, then the functor $f\mapsto g$ is a [[pseudofunctor]] $V D^{op}\to H D$ from the vertical 2-category to the horizontal one, which is the identity on objects, and [[locally fully faithful 2-functor|locally fully faithful]] by the mate correspondence.  If every vertical arrow also has a [[companion]], then this makes $D$ into a [[proarrow equipment]], or equivalently a [[framed bicategory]].

## References

* [[Marco Grandis]] and [[Robert Pare]], *Adjoints for double categories*

* [[Robert Dawson]] and [[Robert Pare]] and [[Dorette Pronk]], *The Span construction*, [TAC](http://www.tac.mta.ca/tac/volumes/24/13/24-13abs.html).

* [[Michael Shulman]], *Framed bicategories and monoidal fibrations*, [TAC](http://www.tac.mta.ca/tac/volumes/20/18/20-18abs.html)


[[!redirects conjunction]]
[[!redirects conjunctions]]
[[!redirects conjunctionss]]
[[!redirects conjoint]]
[[!redirects conjoint pair]]
[[!redirects conjoints]]
[[!redirects conjoint pairs]]
[[!redirects conjunction in a double category]]
[[!redirects conjunctions in a double category]]
[[!redirects left conjoint]]
[[!redirects right conjoint]]
[[!redirects left conjoints]]
[[!redirects right conjoints]]
[[!redirects orthogonal adjunction]]
[[!redirects orthogonal adjunctions]]
