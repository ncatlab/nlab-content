> This page is about conjunctions in double (or higher) categories; see [[logical conjunction]] for the meet of truth values.

***

#Contents#
* table of contents
{:toc}

## Idea

A **conjunction** (sometimes called **adjunction**, e.g. by [[Marco Grandis|Grandis]] and [[Robert Pare|Parè]]) in a [[double category]] is a way of saying that a [[tight and loose morphisms|tight and a loose arrow]] are [[adjunction|adjoint]], even though they do not live in the same 2-category.


## Definition

Let $f\colon A \to B$ be a tight arrow and $g\colon B \nrightarrow A$ a loose arrow in a double category.  These arrows are said to be a **conjunction** if they come equipped with 2-cells:

\begin{tikzcd}
	A & B && B & B \\
	A & A && A & B
	\arrow[""{name=0, anchor=center, inner sep=0}, "g", "\shortmid"{marking}, from=1-1, to=1-2]
	\arrow[Rightarrow, no head, from=1-1, to=2-1]
	\arrow["f", from=1-2, to=2-2]
	\arrow[""{name=1, anchor=center, inner sep=0}, "\shortmid"{marking}, Rightarrow, no head, from=1-4, to=1-5]
	\arrow["f"', from=1-4, to=2-4]
	\arrow[Rightarrow, no head, from=1-5, to=2-5]
	\arrow[""{name=2, anchor=center, inner sep=0}, "\shortmid"{marking}, Rightarrow, no head, from=2-1, to=2-2]
	\arrow[""{name=3, anchor=center, inner sep=0}, "g"', "\shortmid"{marking}, from=2-4, to=2-5]
	\arrow["\varepsilon", shorten <=4pt, shorten >=4pt, Rightarrow, from=0, to=2]
	\arrow["\eta", shorten <=4pt, shorten >=4pt, Rightarrow, from=1, to=3]
\end{tikzcd}

such that $\varepsilon \circ_\lambda \eta = id_f$ and $\eta \circ_\tau \varepsilon = id_g$, where $\circ_\lambda$ and $\circ_\tau$ denote, respectively, loose and tight composition of 2-cells.

Given such a conjunction, we say that $f$ and $g$ are **conjoints** of each other, and that $g$ is the **right conjoint** of $f$ and that $f$ is the **left conjoint** of $g$.

## Examples

* In the double category $\mathbf{Sq}(K)$ of squares ([[quintets]]) in any 2-category $K$, a conjunction is simply an internal [[adjunction]] in $K$.

* In the [[double category of algebras | double category $T$-$\mathbf{Alg}$ of algebras, lax morphisms, and colax morphisms]] for a [[2-monad]] $T$, an conjunction is precisely a [[doctrinal adjunction]] between a colax morphism an a lax morphism.

## Remarks

* The horizontal (or vertical) dual of a conjunction is a [[companion pair]].

* Conjunctions (and companion pairs) have a [[mate]] correspondence generalizing the calculus of mates in 2-categories.

* If every vertical arrow in some double category $D$ has a right conjoint, then the functor $f\mapsto g$ is a [[pseudofunctor]] $L D^{op}\to T D$ from the loose [[bicategory]] to the tight 2-category, which is the identity on objects, and [[locally fully faithful 2-functor|locally fully faithful]] by the mate correspondence.  If every tight arrow also has a [[companion]], then this makes $D$ into a [[proarrow equipment]], or equivalently a [[framed bicategory]].

* A double category $\mathbb{C}$ admits all conjoints iff the underlying spans $C_0 \xleftarrow{s} C_1 \xrightarrow{t} C_0$ is a two-sided opfibration, i.e. if its opposite span is a [[two-sided fibration]]. See at [[companion pair]] for a sketch of the proof of why this is the case.

## Related concepts

* [[adjunction]]
* [[companion pair]]

## References

The concept is due to (there called **orthogonal adjoint**):

* [[Marco Grandis]] and [[Robert Pare]], *Adjoints for double categories*

The terminology "conjoint" is due to:

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
