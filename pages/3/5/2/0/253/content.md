<div class="rightHandSide toc">
[[!include higher category theory - contents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}


## Idea ##

A **bicategory** is a particular [[algebraic definition of higher category|algebraic]] notion of _weak [[2-category]]_ (in fact, the earliest to be formulated, and still the one in most common use).  The idea is that a bicategory is a category _weakly_ [[enriched category|enriched]] over [[Cat]]: the [[hom-objects]] of a bicategory are [[hom-category|hom-categories]], but the associativity and unity laws of [[enriched category|enriched categories]] hold only up to coherent isomorphism.

## Definition ##

A **bicategory** $B$ consists of

* A collection of objects $x,y,z,\dots$, also called _0-cells_;
* For each pair of 0-cells $x,y$ a category $B(x,y)$, whose objects are _1-cells_ and whose morphisms are _2-cells_;
* For each 0-cell $x$ a distinguished 1-cell $1_x\in B(x,x)$;
* For each triple of 0-cells $x,y,z$ a functor $\circ:B(y,z)\times B(x,y) \to B(x,z)$; and
* Natural isomorphisms $f \circ 1_x \cong f \cong 1_y \circ f$ (the [[unitor]]s and $h\circ (g\circ f) \cong (h \circ g)\circ f$ (the [[associator]]) which satisfy the same axioms as the constraint isomorphisms in a [[monoidal category]].

If there is exactly one 0-cell, say $*$, then the definition is exactly the same as a monoidal structure on the category $B(*,*)$.  This is one of the motivating examples behind the [[delooping hypothesis]] and the general notion of [[k-tuply monoidal n-category]].


## Examples ##

* Any [[strict 2-category]] is a bicategory in which the unitors and associator are identities.  This includes [[Cat]], [[MonCat]], the algebras for any strict [[2-monad]], and so on, at least as classically conceived.

* Categories, [[anafunctor]]s, and natural transformations, which is a more appropriate definition of [[Cat]] in the absence of the [[axiom of choice]], form a bicategory that is not a strict 2-category.  Indeed, without the axiom of choice, the proper notion of bicategory is [[anabicategory]].

* [[ring|Rings]], [[bimodule]]s, and bimodule homomorphisms are the prototype for many similar examples.  Notably, we can generalize from rings to [[enriched category|enriched categories]].

* Objects, [[span]]s, and morphisms of spans in any category with [[pullback]]s also form a bicategory.

* The [[fundamental 2-groupoid]] of a space is a bicategory which is not necessarily strict (although it can be made strict fairly easily when the space is Hausdorff by quotienting by [[thin homotopy]], see [[path groupoid]] and [[fundamental infinity-groupoid]]). When the space is a CW-complex, there are easier and more computationally amenable equivalent strict 2-categories, such as that arising from the fundamental [[crossed complex]].


## Coherence theorems ##

One way to state the [[coherence theorem]] for bicategories is that every bicategory is [[equivalence of categories|equivalent]] to a strict $2$-category. This "strictification" is not obtained naively by forcing composition to be associative, but (at least in one construction) by freely adding new composites which are strictly associative.  Another way to state the coherence theorem is that every formal diagram of the constraints (associators and unitors) commutes.

Note that $n=2$ is the greatest value of $n$ for which every weak $n$-category is equivalent to a fully strict one; see [[semi-strict infinity-category]] and [[Gray-category]].

The proof of the coherence theorem is basically the same as the proof of the coherence theorem for [[monoidal categories]].  An abstract approach can be found in [[John Power|Power]]'s paper "A general coherence result."


## Terminology ##

Classically, "2-category" meant [[strict 2-category]], with "bicategory" used for the weak notion.  This led to the more general use of the prefix "2-" for strict (that is, strictly [[Cat]]-enriched) notions and "bi-" for weak ones.  For example, classically a "2-adjunction" means a Cat-enriched adjunction, consisting of two strict 2-functors $F,G$ and a strictly Cat-natural isomorphism of categories $D(F X, Y)\cong C(X, G Y)$, while a "biadjunction" means the weak version, consisting of two weak 2-functors and a pseudo natural equivalence $D(F X, Y)\simeq C(X, G Y)$.  Similarly for "2-equivalence" and "biequivalence," and "2-limit" and "bilimit."

We often use "2-category" to mean a strict or weak 2-category without prejudice, although we do still use "bicategory" to refer to the particular classical algebraic notion of weak 2-category.  We try to avoid the more general use of "bi-" meaning "weak," however.  For one thing, is it confusing; a "biproduct" could mean a weak [[2-limit]], but it could also mean an object which is both a product and a coproduct (which happens quite frequently in [[additive category|additive categories]]).

Moreover, in most cases the prefix is unnecessary, since once we know we are working in a bicategory, there is usually no point in considering strict notions at all.  Fully weak limits are really the only sensible ones to ask for in a bicategory, and likewise for fully weak adjunctions and equivalences.  Even in a strict 2-category, while we might need to say "strict" sometimes to be clear, we don\'t need to say "$2$-", since we know that we are not working in a mere category.  (Max Kelly pushed this point.)

When we do have a strict 2-category, however, other strict notions can be quite technically useful, even if our ultimate interest is in the weak ones.  This is somewhat analogous to the use of strict structures to model weak ones in [[homotopy theory]]; see [here](http://arxiv.org/abs/math/0702535) and [here](http://arxiv.org/abs/math/0607646) for good introductions to this sort of thing.

[[!redirects bicategories]]
