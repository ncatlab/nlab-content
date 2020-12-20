# Lax monoidal categories

* table of contents
{:toc}

## Idea

A *lax monoidal category* is a [[monoidal category]] in which the associativity and isomorphisms are replaced by not-necessarily-invertible transformations.  An *oplax monoidal category* is similar except that the transformations go in the other direction.

## Overview of variations

For ordinary monoidal categories, the [[biased]] and unbiased definitions coincide up to equivalence (though this is a nontrivial coherence theorem), but in the lax and oplax cases this is no longer true.  Moreover, in the biased cases we can make independent choices of the directions of various of the morphisms.  This yields the following variations (in all cases we omit the coherence axioms for now):

* An **unbiased lax monoidal category** has $n$-ary tensor products $(a_1\otimes \cdots\otimes a_n)$ for all $n\ge 0$, including a 0-ary unit $I = ()$, and generalized associativity maps such as

  $$((a\otimes b\otimes c) \otimes () \otimes (d\otimes e)) \to (a\otimes b\otimes c\otimes d\otimes e)$$

  and a unit map $a\to (a)$.  It is **(strictly) normal** if the later is an isomorphism (identity).  It is a special case of a [[lax algebra for a 2-monad]].  

* Dually, an **unbiased oplax monoidal category** has generalized associativity maps in the opposite direction

  $$(a\otimes b\otimes c\otimes d\otimes e) \to ((a\otimes b\otimes c) \otimes () \otimes (d\otimes e))$$

  and a unit map $(a) \to a$.  It is a special case of an oplax algebra for a 2-monad.

* A **right-biased lax monoidal category** has a binary tensor product $a\otimes b$, a unit $I$, and constraints

  $$a \otimes (b\otimes c) \to (a\otimes b)\otimes c \qquad I \otimes a\to a \qquad a\otimes I\to a. $$

* A **left-biased lax monoidal category** has a binary tensor product $a\otimes b$, a unit $I$, and constraints

  $$(a\otimes b)\otimes c\to a \otimes (b\otimes c) \qquad I \otimes a\to a \qquad a\otimes I\to a. $$

* A **right-biased oplax monoidal category** has a binary tensor product $a\otimes b$, a unit $I$, and constraints

  $$a \otimes (b\otimes c) \to (a\otimes b)\otimes c \qquad a\to I \otimes a \qquad a\to  a\otimes I. $$

* A **left-biased oplax monoidal category** has a binary tensor product $a\otimes b$, a unit $I$, and constraints

  $$(a\otimes b)\otimes c\to a \otimes (b\otimes c) \qquad a\to I \otimes a \qquad a\to a\otimes I. $$

* A **right-skew monoidal category** has a binary tensor product $a\otimes b$, a unit $I$, and constraints

  $$a \otimes (b\otimes c) \to (a\otimes b)\otimes c \qquad a\to I \otimes a \qquad a\otimes I\to a. $$

* A **left-skew monoidal category** has a binary tensor product $a\otimes b$, a unit $I$, and constraints

  $$(a\otimes b)\otimes c\to a \otimes (b\otimes c) \qquad  I \otimes a\to a \qquad a\to a\otimes I. $$

There are two other possibilities, but they seem not to have been studied; we could call them "coskew" to have a name.  Terminologically, note that we use "right" and "left" to indicate the direction of the biased associator, while the direction of the unitors is indicated by "lax" or "oplax" (if they are in the same direction) or "skew" (if they are in different directions).

This use of "lax" and "oplax" in the biased case is justified by the fact that *biased (op)lax monoidal categories are a special case of unbiased ones*, with the $n$-ary tensor products defined in terms of the binary one by left- or right-associativity.  The unbiased structures arising in this way can be characterized as those in which certain generalized associativities are identities (or, up to equivalence, isomorphisms).

## Definitions

The above definitions are complete except for the coherence axioms.  In the unbiased case these can be deduced from the general notion of lax algebra.  In the biased cases, the axioms are roughly the same as those in MacLane's original definition of monoidal category: one pentagon, three unit triangles, and one unit-unit axiom.  (Kelly's later reduction of these to one pentagon and one unit triangle relies on invertibility of the constraints.)  In all cases it is possible to orient all of these axioms so as to make sense.

## Related notions

First note that all kinds of lax monoidal categories can be generalized to **lax monoids** in a [[monoidal bicategory]].  Using this generalization, we can make connections to many other kinds of monoidal structures:

* Oplax monoidal categories (i.e. oplax monoids in [[Cat]]) can be identified with [[multicategories]] that are "weakly representable".

* Multicategories themselves are precisely lax monoids in [[Span]], and also normal lax monoids in [[Prof]].

* We obtain various kinds of lax [[promonoidal category]] by working in [[Prof]] instead of [[Cat]].

* In particular, non-unital [[closed categories]] can be defined as biased lax monoids in [[Prof]] whose multiplication is corepresentable in the first argument and whose left unitor is invertible.  If the identity is also representable, we obtain a (unital) closed category.  The identification of biased lax monoids with particular unbiased ones thereby specializes to the identification of closed categories with closed multicategories.

## References

* [[John Bourke]], [[Stephen Lack]], _Skew monoidal categories and skew multicategories_, Journal of Algebra 506 (2018), 237-266.  ([arxiv](https://arxiv.org/abs/1708.06088))


[[!redirects lax monoidal category]]
[[!redirects unbiased lax monoidal category]]
[[!redirects biased lax monoidal category]]
[[!redirects right-biased lax monoidal category]]
[[!redirects left-biased lax monoidal category]]

[[!redirects colax monoidal category]]
[[!redirects unbiased colax monoidal category]]
[[!redirects biased colax monoidal category]]
[[!redirects right-biased colax monoidal category]]
[[!redirects left-biased colax monoidal category]]

[[!redirects oplax monoidal category]]
[[!redirects unbiased oplax monoidal category]]
[[!redirects biased oplax monoidal category]]
[[!redirects right-biased oplax monoidal category]]
[[!redirects left-biased oplax monoidal category]]

[[!redirects skew monoidal category]]
[[!redirects right-skew monoidal category]]
[[!redirects left-skew monoidal category]]

[[!redirects lax monoidal categories]]
[[!redirects unbiased lax monoidal categories]]
[[!redirects biased lax monoidal categories]]
[[!redirects right-biased lax monoidal categories]]
[[!redirects left-biased lax monoidal categories]]

[[!redirects colax monoidal categories]]
[[!redirects unbiased colax monoidal categories]]
[[!redirects biased colax monoidal categories]]
[[!redirects right-biased colax monoidal categories]]
[[!redirects left-biased colax monoidal categories]]

[[!redirects oplax monoidal categories]]
[[!redirects unbiased oplax monoidal categories]]
[[!redirects biased oplax monoidal categories]]
[[!redirects right-biased oplax monoidal categories]]
[[!redirects left-biased oplax monoidal categories]]

[[!redirects skew monoidal categories]]
[[!redirects right-skew monoidal categories]]
[[!redirects left-skew monoidal categories]]

[[!redirects lax monoid]]
[[!redirects lax monoids]]
[[!redirects oplax monoid]]
[[!redirects oplax monoids]]
[[!redirects colax monoid]]
[[!redirects colax monoids]]
