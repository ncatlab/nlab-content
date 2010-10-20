
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The [[(∞,1)-category]] analog of the notion of [[cartesian closed category]]

## Definition

Let $C$ be an [[(∞,1)-category]] with all [[(∞,1)-limit|product]]s. This makes it a [[symmetric monoidal (∞,1)-category]] with tensor product the cartesian product.

If this makes $C$ a [[closed monoidal (∞,1)-category]], we say it is **cartesian closed monoidal**.

In detail, if for all [[object]]s $X \in C$ the [[(∞,1)-functor]]

$$
  (-) \times X : C \to C
$$

admits a right [[adjoint (∞,1)-functor]]

$$
  [X,-] : C \to C
$$

we say that $C$ is a **cartesian closed $(\infty,1)$-catgory.

## Properties

It should follow that the adjunction [[equivalence in a quasicategory|equivalence]]

$$
  C(X \times Y, Z) \simeq C(X,[Y,Z])
$$

is natural also in $Y$.

[[!redirects cartesian closed (∞,1)-category]]


[[!redirects cartesian closed (∞,1)-categories]]
[[!redirects cartesian closed (infinity,1)-categories]]