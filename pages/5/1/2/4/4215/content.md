> This page is about conjunctions in double (or higher) categories; see [[logical conjunction]] for the meet of truth values.

***

#Contents#
* table of contents
{:toc}

## Idea

A **conjunction** (sometimes called **adjunction**, e.g. by [[Marco Grandis|Grandis]] and [[Robert Pare|Parè]]) in a [[double category]] is a way of saying that a [[tight and loose morphisms|tight and a loose arrow]] are [[adjunction|adjoint]], even though they do not live in the same 2-category.


## Definition

Let $f\colon A \to B$ be a tight arrow and $g\colon B \nrightarrow A$ a loose arrow in a double category.  These arrows are said to be a **conjunction** if they come equipped with 2-cells:

<table>
<tr>
<td style="border: none;">
\begin{tikzcd}
  B
  \arrow["\shortmid"{marking}, r,  "g", ""{name=U, below}]
  \arrow[d, Rightarrow, no head,  ""]
  & A
  \arrow[d, "f"]
  \\
  B
  \arrow["\shortmid"{marking}, Rightarrow, no head, r, ""', ""{name=D, above}]
  & B
  \arrow[Rightarrow, from=U, to=D, "\varepsilon"]
\end{tikzcd}
</td>
<td style="border: none;">
\begin{tikzcd}
  A
  \arrow["\shortmid"{marking}, Rightarrow, no head, r,  "", ""{name=U, below}]
  \arrow[d,  "f"']
  & A
  \arrow[d, Rightarrow, no head, ""]
  \\
  B
  \arrow["\shortmid"{marking}, r, "g"', ""{name=D, above}]
  & A
  \arrow[Rightarrow, from=U, to=D, "\eta"]
\end{tikzcd}
</td>
</tr>
</table>
such that $\varepsilon \eta = id_f$ and $\eta \odot \varepsilon = id_g$, where $\odot$ denotes the loose composition, and the juxtaposition the tight composition (in diagram order) of 2-cells.

Given such a conjunction, we say that $f$ and $g$ are **conjoints** of each other, and that $g$ is the **right conjoint** of $f$ and that $f$ is the **left conjoint** of $g$.
\begin{tikzcd}
	B
	\arrow["\shortmid"{marking}, r, bend left, "g"]
	& A
	\arrow[l, bend left, "f"]
\end{tikzcd}

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
