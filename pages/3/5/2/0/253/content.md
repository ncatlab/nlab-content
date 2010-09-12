<div class="rightHandSide toc">
[[!include 2-category theory - contents]]
----
[[!include higher category theory - contents]]
</div>

# Bicategories
* automatic table of contents goes here
{:toc}

## Idea

A **bicategory** is a particular [[algebraic definition of higher category|algebraic]] notion of _weak [[2-category]]_ (in fact, the earliest to be formulated, and still the one in most common use).  The idea is that a bicategory is a category _weakly_ [[enriched category|enriched]] over [[Cat]]: the [[hom-objects]] of a bicategory are [[hom-category|hom-categories]], but the associativity and unity laws of [[enriched category|enriched categories]] hold only up to coherent isomorphism.


## Definition

A **bicategory** $B$ consists of

* A collection of objects $x,y,z,\dots$, also called _$0$-cells_;
* For each pair of $0$-cells $x,y$, a category $B(x,y)$, whose objects are _$1$-cells_ and whose morphisms are _$2$-cells_;
* For each $0$-cell $x$, a distinguished $1$-cell $1_x\in B(x,x)$;
* For each triple of $0$-cells $x,y,z$, a functor ${\circ}\colon B(y,z)\times B(x,y) \to B(x,z)$;
* For each pair of $0$-cells $x,y$, [[natural isomorphisms]], called _[[unitors]]_, $id_{B(x,y)} \circ const_{1_x} \cong id_{B(x,y)} \cong const_{1_y} \circ id_{B(x,y)}\colon B(x,y) \to B(x,y)$; and
* For each quadruple of $0$-cells $w,x,y,z$, a natural isomorphism, called the _[[associator]]_, between the two functors from $B_{y,z} \times B_{x,y} \times B_{w,x}$ to $B_{w,z}$ built out of ${\circ}$; such that
* The same axioms as the constraint isomorphisms in a [[monoidal category]] (which we do not write out in full here) are satisfied.

If there is exactly one $0$-cell, say $*$, then the definition is exactly the same as a monoidal structure on the category $B(*,*)$.  This is one of the motivating examples behind the [[delooping hypothesis]] and the general notion of [[k-tuply monoidal n-category]].


### Details
{#detailedDefn}

Here we spell out the above definition in full detail.  Compare to the [detailed definition of strict $2$-category](/nlab/show/strict+2-category#detailedDefn), which is written in the same style but is simpler.

A bicategory $B$ consists of

*  a collection $Ob B$ or $Ob_B$ of _objects_ or _$0$-cells_,
*  for each object $a$ and object $b$, a collection $B(a,b)$ or $Hom_B(a,b)$ of _morphisms_ or _$1$-cells_ $a \to b$, and
*  for each object $a$, object $b$, morphism $f\colon a \to b$, and morphism $g\colon a \to b$, a collection $B(f,g)$ or $2Hom_B(f,g)$ of _$2$-morphisms_ or _$2$-cells_ $f \Rightarrow g$ or $f \Rightarrow g\colon a \to b$,

equipped with

*  for each object $a$, an _identity_ $1_a\colon a \to a$ or $\id_a\colon a \to a$,
*  for each $a,b,c$, $f\colon a \to b$, and $g\colon b \to c$, a _composite_ $f ; g\colon a \to c$ or $g \circ f\colon a \to c$,
*  for each $f\colon a \to b$, an _identity_ or _$2$-identity_ $1_f\colon f \Rightarrow f$ or $\Id_f\colon f \to f$,
*  for each $f,g,h\colon a \to b$, $\eta\colon f \Rightarrow g$, and $\theta\colon g \Rightarrow h$, a _vertical composite_ $\theta \bullet \eta\colon f \Rightarrow h$,
*  for each $a,b,c$, $f\colon a \to b$, $g,h\colon b \to c$, and $\eta\colon g \Rightarrow h$, a _left whiskering_ $\eta \triangleleft f\colon g \circ f \Rightarrow h \circ f$,
*  for each $a,b,c$, $f,g\colon a \to b$, $h\colon b \to c$, and $\eta\colon f \Rightarrow g$, a _right whiskering_ $h \triangleright \eta \colon h \circ f \Rightarrow h \circ g$,
*  for each $f\colon a \to b$, a _left unitor_ $\lambda_f\colon f \circ \id_a \Rightarrow f$ and an _inverse left unitor_ $\bar{\lambda}_f\colon f \Rightarrow f \circ \id_a$,
*  for each $f\colon a \to b$, a _right unitor_ $\rho_f\colon \id_b \circ f \Rightarrow f$, and an _inverse right unitor_ $\bar{\rho}_f\colon f \Rightarrow \id_b \circ f$, and
*  for each $a \overset{f}\to b \overset{g}\to c \overset{h}\to d$, an _associator_ $\alpha_{f,g,h}\colon h \circ (g \circ f) \Rightarrow (h \circ g) \circ f$ and an _inverse associator_ $\bar{\alpha}_{f,g,h}\colon (h \circ g) \circ f \Rightarrow h \circ (g \circ f)$,

such that

*  for each $\eta\colon f \Rightarrow g\colon a \to b$, the vertical composites $\eta \bullet \Id_f$ and $\Id_g \bullet \eta$ both equal $\eta$,
*  for each $f \overset{\eta}\Rightarrow g \overset{\theta}\Rightarrow h \overset{\iota}\Rightarrow i\colon a \to b$, the vertical composites $\iota \bullet (\theta \bullet \eta)$ and $(\iota \bullet \theta) \bullet \eta$ are equal,
*  for each $a \overset{f}\to b \overset{g}\to c$, the whiskerings $\Id_g \triangleleft f$ and $g \triangleright \Id_f$ both equal $\Id_{g \circ f }$,
*  for each $f\colon a \to b$ and $g \overset{\eta}\Rightarrow h \overset{\theta}\Rightarrow i\colon b \to c$, the vertical composite $(\theta \triangleleft f) \bullet (\eta \triangleleft f)$ equals the whiskering $(\theta \bullet \eta) \triangleleft f$,
*  for each $f \overset{\eta}\Rightarrow g \overset{\theta}\Rightarrow h\colon a \to b$ and $i\colon b \to c$, the vertical composite $(i \triangleright \theta) \bullet (i \triangleright \eta)$ equals the whiskering $i \triangleright (\theta \bullet \eta)$,
*  for each $\eta\colon f \Rightarrow g\colon a \to b$, the vertical composites $\lambda_g \bullet (\eta \triangleleft \id_a)$ and $\eta \bullet \lambda_f$ are equal,
*  for each $\eta\colon f \Rightarrow g\colon a \to b$, the vertical composites $\rho_g \bullet (\id_b \triangleright \eta)$ and $\eta \bullet \rho_f$ are equal,
*  for each $a \overset{f}\to b \overset{g}\to c$ and $\eta\colon h \Rightarrow i\colon c \to d$, the vertical composites $\alpha_{f,g,i} \bullet (\eta \triangleleft (g \circ f)$ and $((\eta \triangleleft g) \triangleleft f) \bullet \alpha_{f,g,h}$ are equal,
*  for each $f\colon a \to b$, $\eta\colon g \Rightarrow h\colon b \to c$, and $i\colon c \to d$, the vertical composites $\alpha_{f,h,i} \bullet (i \triangleright (\eta \triangleleft f))$ and $((i \triangleright \eta) \triangleleft f) \bullet \alpha_{f,g,i}$ are equal,
*  for each $\eta\colon f \Rightarrow g\colon a \to b$ and $b \overset{h}\to c \overset{i}\to d$, the vertical composites $\alpha_{g,h,i} \bullet (i \triangleright (h \triangleright \eta))$ and $((i \circ h) \triangleright \eta) \bullet \alpha_{f,h,i}$ are equal,
*  for each $\eta\colon f \Rightarrow g\colon a \to b$ and $\theta\colon h \Rightarrow i\colon b \to c$, the vertical composites $(i \triangleright \eta) \bullet (\theta \triangleleft f)$ and $(\theta \triangleleft g) \bullet (h \triangleright \eta)$ are equal,
*  for each $f\colon a \to b$, the vertical composites $\lambda_f \bullet \bar{\lambda}_f\colon f \Rightarrow f$ and $\bar{\lambda}_f \bullet \lambda_f\colon f \circ \id_a \Rightarrow f \circ \id_a$ equal the appropriate identity $2$-morphisms,
*  for each $f\colon a \to b$, the vertical composites $\rho_f \bullet \bar{\rho}_f\colon f \Rightarrow f$ and $\bar{\rho}_f \bullet \rho_f\colon \id_b \circ f \Rightarrow \id_b \circ f$ equal the appropriate identity $2$-morphisms,
*  for each $a \overset{f}\to b \overset{g}\to c \overset{h}\to d$, the vertical composites $\alpha_{f,g,h} \bullet \bar{\alpha}_{f,g,h}\colon (h \circ g) \circ f \Rightarrow (h \circ g) \circ f$ and $\bar{\alpha}_{f,g,h} \bullet \alpha_{f,g,h}\colon h \circ (g \circ f) \Rightarrow h \circ (g \circ f)$ equal the appropriate identity $2$-morphisms,
*  for each $a \overset{f}\to b \overset{g}\to c$, the vertical composite $(\lambda_g \triangleleft f) \bullet \alpha_{f,\id_b,g}$ equals the whiskering $g \triangleright \rho_f$, and
*  for each $a \overset{f}\to b \overset{g}\to c \overset{h}\to d \overset{i}\to e$, the vertical composites $((\alpha_{g,h,i} \triangleleft f) \bullet \alpha_{f,h \circ g,i}) \bullet (i \triangleright \alpha_{f,g,h})$ and $\alpha_{g \circ f,h,i} \bullet \alpha_{f,g,i \circ h}$ are equal.

It is quite possible that there are errors or omissions in this list, although they should be easy to correct.  The point is not that one would *want* to write out the definition in such elementary terms (although apparently I just did anyway) but rather that one *can*.


## Examples

* Any [[strict 2-category]] is a bicategory in which the unitors and associator are identities.  This includes [[Cat]], [[MonCat]], the algebras for any strict [[2-monad]], and so on, at least as classically conceived.

* Categories, [[anafunctor]]s, and natural transformations, which is a more appropriate definition of [[Cat]] in the absence of the [[axiom of choice]], form a bicategory that is not a strict 2-category.  Indeed, without the axiom of choice, the proper notion of bicategory is [[anabicategory]].

* [[ring|Rings]], [[bimodule]]s, and bimodule homomorphisms are the prototype for many similar examples.  Notably, we can generalize from rings to [[enriched category|enriched categories]].

* Objects, [[span]]s, and morphisms of spans in any category with [[pullback]]s also form a bicategory.

* The [[fundamental 2-groupoid]] of a space is a bicategory which is not necessarily strict (although it can be made strict fairly easily when the space is Hausdorff by quotienting by [[thin homotopy]], see [[path groupoid]] and [[fundamental infinity-groupoid]]). When the space is a CW-complex, there are easier and more computationally amenable equivalent strict 2-categories, such as that arising from the fundamental [[crossed complex]].


## Coherence theorems

One way to state the [[coherence theorem]] for bicategories is that every bicategory is [[equivalence of categories|equivalent]] to a strict $2$-category. This "strictification" is not obtained naively by forcing composition to be associative, but (at least in one construction) by freely adding new composites which are strictly associative.  Another way to state the coherence theorem is that every formal diagram of the constraints (associators and unitors) commutes.

Note that $n=2$ is the greatest value of $n$ for which every weak $n$-category is equivalent to a fully strict one; see [[semi-strict infinity-category]] and [[Gray-category]].

The proof of the coherence theorem is basically the same as the proof of the coherence theorem for [[monoidal categories]].  An abstract approach can be found in [[John Power|Power]]'s paper "A general coherence result."


## Terminology

Classically, "2-category" meant [[strict 2-category]], with "bicategory" used for the weak notion.  This led to the more general use of the prefix "2-" for strict (that is, strictly [[Cat]]-enriched) notions and "bi-" for weak ones.  For example, classically a "2-adjunction" means a Cat-enriched adjunction, consisting of two strict 2-functors $F,G$ and a strictly Cat-natural isomorphism of categories $D(F X, Y)\cong C(X, G Y)$, while a "biadjunction" means the weak version, consisting of two weak 2-functors and a pseudo natural equivalence $D(F X, Y)\simeq C(X, G Y)$.  Similarly for "2-equivalence" and "biequivalence," and "2-limit" and "bilimit."

We often use "2-category" to mean a strict or weak 2-category without prejudice, although we do still use "bicategory" to refer to the particular classical algebraic notion of weak 2-category.  We try to avoid the more general use of "bi-" meaning "weak," however.  For one thing, is it confusing; a "biproduct" could mean a weak [[2-limit]], but it could also mean an object which is both a product and a coproduct (which happens quite frequently in [[additive category|additive categories]]).

Moreover, in most cases the prefix is unnecessary, since once we know we are working in a bicategory, there is usually no point in considering strict notions at all.  Fully weak limits are really the only sensible ones to ask for in a bicategory, and likewise for fully weak adjunctions and equivalences.  Even in a strict 2-category, while we might need to say "strict" sometimes to be clear, we don\'t need to say "$2$-", since we know that we are not working in a mere category.  (Max Kelly pushed this point.)

When we do have a strict 2-category, however, other strict notions can be quite technically useful, even if our ultimate interest is in the weak ones.  This is somewhat analogous to the use of strict structures to model weak ones in [[homotopy theory]]; see [here](http://arxiv.org/abs/math/0702535) and [here](http://arxiv.org/abs/math/0607646) for good introductions to this sort of thing.


## Discussion

Discussion about the use of the term "weak enrichment" above is now at [[weak enrichment]].


[[!redirects bicategory]]
[[!redirects bicategories]]
