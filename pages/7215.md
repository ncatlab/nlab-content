
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Factorization systems
+--{: .hide}
[[!include factorization systems - contents]]
=--
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A *factorization system over a subcategory* is a common generalization of an [[orthogonal factorization system]] and a [[strict factorization system]], in which factorizations are only unique up to zigzags belonging to some specified subcategory.

## Definition

Let $C$ be a [[category]], and let $J$, $E$, and $M$ be [[wide subcategories]] of $C$ with $J\subseteq E$ and $J\subseteq M$.  Given a [[morphism]] $f\colon x\to y$ in $C$, let $Fact^{E,M}_J(f)$ denote the non-full [[subcategory]] of the over-under-category ([[double comma category]]) $(x/C/y)$:

* whose objects are pairs $x\to z \to y$ such that $x\to z$ is in $E$, $z\to y$ is in $M$, and the composite $x\to y$ is $f$;
* whose morphisms from $x\to z \to y$ to $x\to z' \to y$ are morphisms $z\to z'$ which are in $J$ and make the two evident triangles commute.

We say that $(E,M)$ is a **factorization system over $J$** if $Fact^{E,M}_J(f)$ is [[connected category|connected]] (and thus, in particular, [[inhabited set|inhabited]]).

## Examples

* If $J$ consists of only the identities in $C$, then a factorization system over $J$ is a [[strict factorization system]].

* If $J$ is the [[core]] of $C$, then a factorization system over $J$ is an [[orthogonal factorization system]]

* If $J$ is the canonical inclusion of (a skeleton of) $FinSet^{op}$ into a [[Lawvere theory]] $C$, then a factorization system over $J$ is a decomposition of $C$ into a [[distributive law]] of two other Lawvere theories.

## Relation to distributive laws

Suppose given a category $J$.  Then to give a category $C$ equipped with an identity-on-objects functor $J\to C$ and a factorization system over $J$ is the same as to give a [[distributive law]] between two [[monads]] on $J$ in the bicategory [[Prof]].  The two monads are the categories $E$ and $M$, and their composite is $C$.

## References

* [[Eugenia Cheng]], *Distributive laws for Lawvere theories*, [arXiv:1112.3076](http://arxiv.org/abs/1112.3076)

[[!redirects factorization systems over a subcategory]]
