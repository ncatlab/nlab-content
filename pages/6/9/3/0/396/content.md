
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

A **full and faithful functor** is a [[functor]] which is both [[full functor|full]] and [[faithful functor|faithful]].  That is, a [[functor]] $F\colon C \to D$ from a [[category]] $C$ to a category $D$ is called _full and faithful_ if for each pair of [[objects]] $x, y \in C$, the [[function]]
$$F\colon C(x, y) \to D(F(x), F(y))$$
between [[hom sets]] is [[bijective]].  "Full and faithful" is sometimes shortened to "fully faithful" or "ff."   See also [[full subcategory]].

\begin{remark}\label{NeedForNaturality}
It is not sufficient for there simply to exist _some_ isomorphism between $C(x, y)$ and $D(F(x), F(y))$. For instance, consider the category comprising a [[parallel pair]] $f, g : x \rightrightarrows y$ and the [[identity-on-objects]] [[endofunctor]] $F$ sending $f \mapsto f$ and $g \mapsto f$. We have $C(x, y) \cong C(F(x), F(y)) = C(x, y)$, but this functor is not fully faithful.
\end{remark}

## Properties

* Together with [[bo functor|bijective-on-objects functors]], fully faithful  functors form an [[bo-ff factorization system|orthogonal factorization system]] on $Cat$; see [[bo-ff factorization system]]. More invariantly, pair them with [[essentially surjective functor]]s to get a bicategorial factorization system.

* In particular, fully faithful functors are stable under [[pullback]].

* A [[fully faithful functor]] (hence a [[full subcategory]] inclusion) [[reflected limit|reflects]] all [[limits]] and [[colimits]], also all [[isomorphisms]] (is a [[conservative functor]]).  This is evident from inspection of the defining [[universal property]].
 {#FullSubcategoryInclusionsReflectCoLimits}

* Fully faithful functors are closed under [[pushouts]] in [[Cat]].  For ordinary categories this was proven by [Fritch and Latch](#FL); for [[enriched categories]] it is proven in [Stanculescu, Prop. 3.1](#Stanculescu), and for [[(∞,1)-categories]] it is proven in [Simspon, Cor. 16.6.2](#Simpson).

* Fully faithful functors $F : C \to D$ can be characterized as those functors for which the following square is a pullback, where the vertical maps are source and target, and the horizontal maps are induced by $F$
$$
  \array{
    C^{[1]} &\to& D^{[1]}
    \\
    \downarrow && \downarrow
    \\
    C \times C &\to& D \times D
  }
$$

* The bijections exhibiting full faithfulness of $F$ form a natural isomorphism, by functoriality of $F$ and of pre- and postcomposition.

* Let $I L \dashv R$ be an [[adjunction]]. If $I$ is [[fully faithful]], then $L \dashv R I$. In this case, the two adjunctions induce the same [[monad]]. This is Proposition 1.1 of [DFH75](#DFH75). (For a converse, see [[dominant functor]].)

## Generalizations

* For [[(∞,1)-category|(∞,1)-categories]] the corresponding notion of fully faithful functor is described at [[fully faithful (∞,1)-functor]].  This is part of a bigger pattern at work here which is indicated at [[stuff, structure, property]] and [[k-surjective functor]].

* Inside a [[2-category]] there is a "representable" notion of [[ff morphism]].

* There is also a notion of fully faithful functor in [[enriched category theory]], which in general is stronger than being an ff morphism in the 2-category of enriched categories.  But it can be expressed internally in any [[proarrow equipment]].


## Related concepts

[[!include properties of functors -- contents]]

## References

* [[Francis Borceux]], Section 1.5 in: *[[Handbook of Categorical Algebra]]* Vol. 1: *Basic Category Theory* &lbrack;[doi:10.1017/CBO9780511525858](https://doi.org/10.1017/CBO9780511525858)&rbrack;

* {#DFH75} [[Aristide Deleanu]], [[Armin Frei]], [[Peter Hilton]], _Idempotent triples and completion_, Mathematische Zeitschrift **143** (1975) 91-104 &lbrack;[doi:10.1007/BF01173053](https://doi.org/10.1007/BF01173053)&rbrack;


[[!redirects full and faithful functor]]
[[!redirects full and faithful functors]]
[[!redirects fully faithful functor]]
[[!redirects fully faithful functors]]

[[!redirects full and faithful]]
[[!redirects fully faithful]]
[[!redirects fully faithfully]]
