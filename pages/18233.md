# Displayed categories

* table of contents
{: toc}

## Idea

A **displayed category** over a [[category]] $C$ is the "classifying map" of a category over $C$.  That is, it is equivalent to the data of a category $D$ and a functor $F:D\to C$, but organized differently as a "functor" associating to each object or morphism of $C$ the [[fiber]] over it.  The operation (which is an [[equivalence]]) taking a displayed category to the corresponding functor $F:D\to C$ is a generalization of the [[Grothendieck construction]].

Displayed categories are particularly useful in [[type theory]] (especially [[internal categories in homotopy type theory]]) and to preserve the [[principle of equivalence]], since they allow a more "category-theoretic" formulation of various notions (such as [[Grothendieck fibrations]] and strict [[creation of limits]]) that, if stated in terms of a functor $F:D\to C$, would involve equality of objects.

## Definition

A **displayed category** over a category $C$ is a [[lax functor]] from $C$, regarded as a bicategory with only identity 2-cells, to the [[bicategory]] [[Span]].

Better, it is a lax [[double functor]] from $C$, regarded as a [[double category]] "horizontally" with only identity vertical arrows and 2-cells, to the (pseudo) double category $Span$ with sets as objects, functions as vertical arrows, and spans as horizontal arrows.  Although this produces an equivalent notion, it is better because a **displayed functor** is then a [[vertical transformation]] between such lax double functors.

A displayed category may equivalently be described as a *[[normal lax functor|normal]]* lax functor from $C$ to [[Prof]] (either the bicategory or the double category, as appropriate), meaning one that strictly preserves identities.  Formally, this is because $Prof = Mod(Span)$, where $Mod(-)$ denotes the double category of horizontal monads and modules, and $Mod$ is a [[right adjoint]] to the inclusion of [[virtual double categories]] and [[normal lax functor|normal (lax) functors]] into all (lax) functors; see [(CS, Prop. 5.14)](#CS).

Equivalently, it is a [[double profunctor]] between $C$ and the terminal double category $1$, i.e., a double presheaf on $C$.

## Correspondence to slices

The category over $C$ corresponding to a displayed category $D:C\to Span$ is the pullback
$$ \array{ D & \to & Span_* \\ \downarrow & & \downarrow \\ C & \to & Span }$$
Where $Span_*=Span(Set_*)$ is the bicategory (or double category) of [[pointed sets]] and pointed spans.  This is a strict pullback, which exists in the 2-category of bicategories (or double categories) and lax functors because the projection $Span_* \to Span$ is not just lax but  strong.  Equivalently, it is the pullback
$$ \array{ D & \to & Prof_* \\ \downarrow & & \downarrow \\ C & \to & Prof }$$
where $Prof_*$ consists of pointed categories and pointed profunctors, a pointed profunctor $H:(A,a_0)&#8696;(B,b_0)$ being equipped with an element of $H(a_0,b_0)$.

This construction induces an [[equivalence of categories]] $Disp(C) \to Cat/C$, which restricts to the following equivalences:

* A displayed category factors through the inclusion $Set \hookrightarrow Span$ (or equivalently $Set \hookrightarrow Prof$) if and only if $F:D\to C$ is a [[discrete opfibration]].  Similarly, it factors through $Set^{op}$ if and only if $F$ is a discrete fibration.

* A factorization of a displayed category $C\to Prof$ through the inclusion $Cat^{op} \hookrightarrow Prof$ (as co[[representable profunctors]]) is equivalent to giving $F:D\to C$ the structure of a [[cloven fibration|cloven]] [[prefibred category]], i.e. equipped with a choice of weakly cartesian liftings.  The factorization is a [[pseudofunctor]] precisely when $F:D\to C$ is a [[Grothendieck fibration]]; in this case we see the usual [[Grothendieck construction]] of a pseudofunctor.

* Similarly, factorizations through $Cat\hookrightarrow Prof$ corresponds to cloven Grothendieck (pre)opfibrations.

* An arbitrary displayed category $C\to Prof$ is a pseudofunctor if and only if $F:D\to C$ is a [[Conduché functor]], i.e. an exponentiable morphism in $Cat$.


## References

The correspondence between categories over $C$ and [[normal lax functors]] $C\to Prof$ was observed by

* Jean B&#233;nabou, *Distributors at work*, Notes by Thomas Streicher from lectures given at TU Darmstadt, 2000, [pdf](http://www.mathematik.tu-darmstadt.de/~streicher/FIBR/DiWo.pdf)

The term "displayed category", and the applications to type theory, are due to:

* [[Benedikt Ahrens]], [[Peter LeFanu Lumsdaine]], *Displayed Categories*, [arxiv](https://arxiv.org/abs/1705.04296)

An unpacking of the definition as lax functors into [[Span]] is in 2.2 of

* [[Duško Pavlović]], [[Samson Abramsky]], *Specifying Interaction Categories*, [LNCS](https://link.springer.com/chapter/10.1007/BFb0026986)

Also cited above:

* [[Geoff Cruttwell]], [[Mike Shulman]], *A unified framework for generalized multicategories* [TAC](http://tac.mta.ca/tac/volumes/24/21/24-21abs.html)
 {#CS}

[[!redirects displayed categories]]
[[!redirects displayed functor]]
[[!redirects displayed functors]]
