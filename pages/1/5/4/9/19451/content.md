

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--


# Contents
* table of contents
{:toc}

## Idea

A *lax monoidal category* or *skew monoidal category* &lbrack;[Szlachányi 2012](#Szlachányi12)&rbrack; is a [[monoidal category]] in which the [[associator]]- and [[unitor]]-[[natural transformation|transformations]] are not required to be [[invertible morphism|invertible]], i.e. are not required to be [[natural isomorphisms]] (as they are for ordinary [[monoidal categories]]).  

In this case there needs to be made a choice in which direction these structure morphisms go. For the opposite of the "evident" direction one speaks of *oplax* monoidal categories.

## Overview of variations

For ordinary monoidal categories, the [[biased]] and unbiased definitions coincide up to equivalence (though this is a nontrivial [[coherence theorem]]), but in the lax and oplax cases this is no longer true.  Moreover, in the biased cases we can make independent choices of the directions of various of the morphisms.  This yields the following variations (in all cases we omit the coherence axioms for now):

* An **unbiased lax monoidal category** has $n$-ary tensor products $(a_1\otimes \cdots\otimes a_n)$ for all $n\ge 0$, including a 0-ary unit $I = ()$, and generalized associativity maps such as

  $$((a\otimes b\otimes c) \otimes () \otimes (d\otimes e)) \to (a\otimes b\otimes c\otimes d\otimes e)$$

  and a unit map $a\to (a)$.  It is **(strictly) normal** if the later is an isomorphism (identity).  It is a special case of a [[lax algebra for a 2-monad]].  

* Dually, an **unbiased oplax monoidal category** has generalized associativity maps in the opposite direction

  $$(a\otimes b\otimes c\otimes d\otimes e) \to ((a\otimes b\otimes c) \otimes () \otimes (d\otimes e))$$

  and a unit map $(a) \to a$.  It is a special case of an oplax algebra for a 2-monad.

* A **left-biased lax monoidal category** has a binary tensor product $a\otimes b$, a unit $I$, and constraints

  $$(a\otimes b)\otimes c\to a \otimes (b\otimes c) \qquad I \otimes a\to a \qquad a\otimes I\to a $$

* A **right-biased lax monoidal category** has a binary tensor product $a\otimes b$, a unit $I$, and constraints

  $$a \otimes (b\otimes c) \to (a\otimes b)\otimes c \qquad I \otimes a\to a \qquad a\otimes I\to a $$

* A **left-biased oplax monoidal category** has a binary tensor product $a\otimes b$, a unit $I$, and constraints

  $$(a\otimes b)\otimes c\to a \otimes (b\otimes c) \qquad a\to I \otimes a \qquad a\to a\otimes I $$

* A **right-biased oplax monoidal category** has a binary tensor product $a\otimes b$, a unit $I$, and constraints

  $$a \otimes (b\otimes c) \to (a\otimes b)\otimes c \qquad a\to I \otimes a \qquad a\to  a\otimes I $$

* A **left-skew monoidal category** has a binary tensor product $a\otimes b$, a unit $I$, and constraints

  $$(a\otimes b)\otimes c\to a \otimes (b\otimes c) \qquad  I \otimes a\to a \qquad a\to a\otimes I $$

* A **right-skew monoidal category** has a binary tensor product $a\otimes b$, a unit $I$, and constraints

  $$a \otimes (b\otimes c) \to (a\otimes b)\otimes c \qquad a\to I \otimes a \qquad a\otimes I\to a $$

Terminologically, note that we use "right" and "left" to indicate the direction of the biased associator, while the direction of the unitors is indicated by "lax" or "oplax" (if they are in the same direction) or "skew" (if they are in different directions).

The relationship between these concepts is summarised in the following table.

| If $V$ is a ___ monoidal category then... | $V^{rev}$ is... | $V^{op}$ is... | $V^{rev,op}$ is... |
|-----------------------|-------|------|--------------|
| left-biased lax | right-biased lax | right-biased oplax | left-biased oplax |
| right-biased lax | left-biased lax | left-biased oplax | right-biased oplax |
| left-biased oplax | right-biased oplax | right-biased lax | left-biased lax |
| right-biased oplax | left-biased oplax | left-biased lax | right-biased lax |
| left-skew | right-skew | right-skew | left-skew |
| right-skew | left-skew | left-skew | right-skew |

In other words, [[reverse monoidal category|$rev$]] and [[opposite category|$op$]] always swap direction; whilst $op$ interchanges lax and oplax (and has no effect on skew-monoidal categories).

There are two other possibilities, in which the definitions of left-skew and right-skew monoidal category are modified so that the associator is reversed, but they seem not to have been studied.

This use of "lax" and "oplax" in the biased case is justified by the fact that *biased (op)lax monoidal categories are a special case of unbiased ones*, with the $n$-ary tensor products defined in terms of the binary one by left- or right-associativity.  The unbiased structures arising in this way can be characterized as those in which certain generalized associativities are identities (or, up to equivalence, isomorphisms).

## Definitions

The above definitions are complete except for the coherence axioms.  In the unbiased case these can be deduced from the general notion of lax algebra.  In the biased cases, the axioms are roughly the same as those in MacLane's original definition of monoidal category: one pentagon, three unit triangles, and one unit-unit axiom.  (Kelly's later reduction of these to one pentagon and one unit triangle relies on invertibility of the constraints.)  In all cases it is possible to orient all of these axioms so as to make sense.

## Normalisation

\begin{theorem}
**([Lack and Street 2014](#LS14), Theorem 8.1)**
The inclusion of right-normal left-skew monoidal categories (i.e. those for which the right unitor is invertible) and [[lax monoidal functors]] into left-skew monoidal categories admits a partial right [[pseudoadjoint]], defined on those skew  monoidal categories with [[reflexive coequalisers]] preserved by tensoring on the right, sending a skew monoidal category $C$ to the skew monoidal category $C^I$ of $I$-[[modules]].
\end{theorem}

Consequently, any skew monoidal category with such coequalisers may be replaced by a right-normal skew monoidal category with the same monoids.

## Related notions

First note that all kinds of lax monoidal categories can be generalized to **lax monoids** in a [[monoidal bicategory]].  Using this generalization, we can make connections to many other kinds of monoidal structures:

* Oplax monoidal categories (i.e. oplax monoids in [[Cat]]) can be identified with [[multicategories]] that are "weakly representable".

* Multicategories themselves are precisely lax monoids in [[Span]], and also normal lax monoids in [[Prof]].

* We obtain various kinds of lax [[promonoidal category]] by working in [[Prof]] instead of [[Cat]].

* In particular, non-unital [[closed categories]] can be defined as biased lax monoids in [[Prof]] whose multiplication is corepresentable in the first argument and whose left unitor is invertible.  If the identity is also representable, we obtain a (unital) closed category.  The identification of biased lax monoids with particular unbiased ones thereby specializes to the identification of closed categories with closed multicategories.

* Just as the [[delooping]] of a [[monoidal category]] is a [[bicategory]], so too is the delooping of a skew-monoidal category a **skew-bicategory**.

## References

The definition of skew-monoidal category essentially appears in §2.2 of the following, but with only 2 of the 5 coherence axioms (i.e. [[Max Kelly]]'s simplified axioms for [[monoidal categories]], rather than [[Mac Lane]]'s original axioms):

* [[Marek Zawadowski]], _Lax monoidal fibrations_, [arXiv:0912.4464](https://arxiv.org/abs/0912.4464) (2009).

The notion was later rediscovered in Theorem 4 of:

* [[Thorsten Altenkirch]], [[James Chapman]], and [[Tarmo Uustalu]], _Monads need not be endofunctors_, Proceedings of the 13th international conference on Foundations of Software Science and Computational Structures (2010).

The definition was isolated in, and the terminology introduced in:

* {#Szlachányi12} [[Kornél Szlachányi]], *Skew-monoidal categories and bialgebroids*, Advances in Mathematics **231** 3-4 (2012) 1694-1730 &lbrack;[arXiv:1201.4981](https://arxiv.org/abs/1201.4981), [doi:10.1016/j.aim.2012.06.027](https://doi.org/10.1016/j.aim.2012.06.027)&rbrack;

and the dual notion of skew-[[closed categories]]:

* [[Ross Street]], *Skew-closed categories*, Journal of Pure and Applied Algebra **217** 6 (2013) 973-988 &lbrack;[arXiv:1205.6522](https://arxiv.org/abs/1205.6522), [doi:10.1016/j.jpaa.2012.09.020](https://doi.org/10.1016/j.jpaa.2012.09.020)&rbrack;


See also:

* [[John Bourke]], [[Stephen Lack]], _Skew monoidal categories and skew multicategories_, Journal of Algebra **506** (2018), 237-266. &lbrack;[arXiv:1708.06088](https://arxiv.org/abs/1708.06088), [doi:10.1016/j.jalgebra.2018.02.039](https://doi.org/10.1016/j.jalgebra.2018.02.039)&rbrack;

* Ben Fuller, _Semidirect products of monoidal categories_, [arXiv:1510.08717](https://arxiv.org/abs/1510.08717) (2015).

Examples of skew-closed monoidal structures on [[model categories]] which become monoidal on the [[homotopy category of a model category|homotopy category]]:

* [[John Bourke]], *Skew structures in 2-category theory and homotopy theory*, J. Homotopy Relat. Struct. **12** 1 (2017) 31-81 &lbrack;[arXiv:1510.01467](https://arxiv.org/abs/1510.01467), [doi:10.1007/s40062-015-0121-z](https://doi.org/10.1007/s40062-015-0121-z)&rbrack;

Skew monoidal closed structures on the category of [[Gray categories]] are considered in:

* [[John Bourke]], [[Gabriele Lobbia]], _A skew approach to enrichment for Gray-categories_, Advances in Mathematics **434** (2023) &lbrack;[arXiv:2212.12358](https://arxiv.org/abs/2212.12358), [doi.org/10.1016/j.aim.2023.109327](https://doi.org/10.1016/j.aim.2023.109327)&rbrack;

Lax monoidal categories are called **multitensors** in:

* [[Michael Batanin]], [[Mark Weber]]: _Algebras of higher operads as enriched categories_, Applied Categorical Structures **19** (2011) 93-135 &lbrack;[arXiv:0803.3594](https://arxiv.org/abs/0803.3594)&rbrack;

See also:

* {#LS14} [[Stephen Lack]], [[Ross Street]]: _On monads and warpings_, [[Cahiers]] de topologie et géométrie différentielle **55** 4 (2014) 244-266. &lbrack;[pdf](http://cahierstgdc.com/wp-content/uploads/2017/05/LackStreet_55-4.pdf)&rbrack;

The **biased d-lax 2-category** in the following provide yet another kind of skew-monoidal category (in which the associator is the same as in a right-skew monoidal category, but the unitors as are in a left-skew monoidal category):

* Marco Grandis, _Lax $2 $-categories and directed homotopy_, Cahiers de topologie et géométrie différentielle catégoriques 47.2 (2006): 107-128.

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

[[!redirects skew monoidal]]
[[!redirects skew monoidal categories]]
[[!redirects skew-monoidal category]]
[[!redirects skew-monoidal categories]]
[[!redirects right-skew monoidal categories]]
[[!redirects left-skew monoidal categories]]

[[!redirects lax monoid]]
[[!redirects lax monoids]]
[[!redirects oplax monoid]]
[[!redirects oplax monoids]]
[[!redirects colax monoid]]
[[!redirects colax monoids]]

[[!redirects multitensor]]
[[!redirects multitensors]]


[[!redirects skew-closed category]]
[[!redirects skew-closed categories]]
[[!redirects skew closed category]]
[[!redirects skew closed categories]]

[[!redirects lax-closed category]]
[[!redirects lax-closed categories]]
[[!redirects lax closed category]]
[[!redirects lax closed categories]]
