
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--


# Bicategories
* table of contents
{:toc}

## Idea

A **bicategory** is a particular [[algebraic definition of higher category|algebraic]] notion of _weak [[2-category]]_ (in fact, the earliest to be formulated, and still the one in most common use).  The idea is that a bicategory is a category _[[weak enrichment|weakly enriched]]_ over [[Cat]]: the [[hom-objects]] of a bicategory are [[hom-category|hom-categories]], but the associativity and unity laws of [[enriched category|enriched categories]] hold only up to coherent isomorphism. 

For information on [[morphisms]] of bicategories, see [[pseudofunctor]]. 


## Definition

A **bicategory** $B$ consists of

*  A [[collection]] of __[[objects]]__ $x,y,z,\dots$, also called __$0$-cells__;
*  For each pair of $0$-cells $x,y$, a [[category]] $B(x,y)$, whose objects are called __[[morphisms]]__ or __$1$-cells__ and whose morphisms are called __[[2-morphisms]]__ or __$2$-cells__;
*  For each $0$-cell $x$, a distinguished $1$-cell $1_x\in B(x,x)$ called the __[[identity morphism]]__ or __identity $1$-cell__ at $x$;
*  For each triple of $0$-cells $x,y,z$, a functor ${\circ}\colon B(y,z)\times B(x,y) \to B(x,z)$ called __[[horizontal composition]]__;
*  For each pair of $0$-cells $x,y$, [[natural isomorphisms]] called __[[unitors]]__: $\left(
\begin{array}{rcl}
f&\mapsto&f \circ 1_x\\
\theta&\mapsto&\theta \circ 1_{1_x}
\end{array}
\right)  \cong id_{B(x,y)} \cong \left(
\begin{array}{rcl}
f&\mapsto&1_y\circ f\\
\theta&\mapsto&1_{1_y} \circ \theta
\end{array}
\right):B(x,y)\rightarrow B(x,y)$
*  For each quadruple of $0$-cells $w,x,y,z$, a natural isomorphism called the __[[associator]]__ between the two functors from $B(y,z) \times B(x,y) \times B(w,x)$ to $B(w,z)$ built out of ${\circ}$

such that

*  The [[pentagon identity]] is satisfied by the [[associators]];
*  And the triangle identity is satisfied by the [[unitors]].

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
*  for each $a,b,c$, $f,g\colon a \to b$, $h\colon b \to c$, and $\eta\colon f \Rightarrow g$, a _left whiskering_ $h \triangleleft \eta \colon h \circ f \Rightarrow h \circ g$,
*  for each $a,b,c$, $f\colon a \to b$, $g,h\colon b \to c$, and $\eta\colon g \Rightarrow h$, a _right whiskering_ $\eta \triangleright f\colon g \circ f \Rightarrow h \circ f$,
*  for each $f\colon a \to b$, a _left unitor_ $\lambda_f\colon \id_b \circ f \Rightarrow f$, and an _inverse left unitor_ $\bar{\lambda}_f\colon f \Rightarrow \id_b \circ f$,
*  for each $f\colon a \to b$, a _right unitor_ $\rho_f\colon f \circ \id_a \Rightarrow f$ and an _inverse right unitor_ $\bar{\rho}_f\colon f \Rightarrow f \circ \id_a$, and
*  for each $a \overset{f}\to b \overset{g}\to c \overset{h}\to d$, an _associator_ $\alpha_{h,g,f}\colon (h \circ g) \circ f \Rightarrow h \circ (g \circ f)$ and an _inverse associator_ $\bar{\alpha}_{h,g,f}\colon h \circ (g \circ f) \Rightarrow (h \circ g) \circ f$,

such that

*  for each $\eta\colon f \Rightarrow g\colon a \to b$, the vertical composites $\eta \bullet \Id_f$ and $\Id_g \bullet \eta$ both equal $\eta$,
*  for each $f \overset{\eta}\Rightarrow g \overset{\theta}\Rightarrow h \overset{\iota}\Rightarrow i\colon a \to b$, the vertical composites $\iota \bullet (\theta \bullet \eta)$ and $(\iota \bullet \theta) \bullet \eta$ are equal,
*  for each $a \overset{f}\to b \overset{g}\to c$, the whiskerings $\Id_g \triangleright f$ and $g \triangleleft \Id_f$ both equal $\Id_{g \circ f }$,
*  for each $f \overset{\eta}\Rightarrow g \overset{\theta}\Rightarrow h\colon a \to b$ and $i\colon b \to c$, the vertical composite $(i \triangleleft \theta) \bullet (i \triangleleft \eta)$ equals the whiskering $i \triangleleft (\theta \bullet \eta)$,
*  for each $f\colon a \to b$ and $g \overset{\eta}\Rightarrow h \overset{\theta}\Rightarrow i\colon b \to c$, the vertical composite $(\theta \triangleright f) \bullet (\eta \triangleright f)$ equals the whiskering $(\theta \bullet \eta) \triangleright f$,
*  for each $\eta\colon f \Rightarrow g\colon a \to b$, the vertical composites $\lambda_g \bullet (\id_b \triangleleft \eta)$ and $\eta \bullet \lambda_f$ are equal,
*  for each $\eta\colon f \Rightarrow g\colon a \to b$, the vertical composites $\rho_g \bullet (\eta \triangleright \id_a)$ and $\eta \bullet \rho_f$ are equal,
*  for each $a \overset{f}\to b \overset{g}\to c$ and $\eta\colon h \Rightarrow i\colon c \to d$, the vertical composites $\bar{\alpha}_{i,g,f} \bullet (\eta \triangleright (g \circ f))$ and $((\eta \triangleright g) \triangleright f) \bullet \bar{\alpha}_{h,g,f}$ are equal,
*  for each $f\colon a \to b$, $\eta\colon g \Rightarrow h\colon b \to c$, and $i\colon c \to d$, the vertical composites $\bar{\alpha}_{i,h,f} \bullet (i \triangleleft (\eta \triangleright f))$ and $((i \triangleleft \eta) \triangleright f) \bullet \bar{\alpha}_{i,g,f}$ are equal,
*  for each $\eta\colon f \Rightarrow g\colon a \to b$ and $b \overset{h}\to c \overset{i}\to d$, the vertical composites $\bar{\alpha}_{i,h,g} \bullet (i \triangleleft (h \triangleleft \eta))$ and $((i \circ h) \triangleleft \eta) \bullet \bar{\alpha}_{i,h,f}$ are equal,
*  for each $\eta\colon f \Rightarrow g\colon a \to b$ and $\theta\colon h \Rightarrow i\colon b \to c$, the vertical composites $(i \triangleleft \eta) \bullet (\theta \triangleright f)$ and $(\theta \triangleright g) \bullet (h \triangleleft \eta)$ are equal,
*  for each $f\colon a \to b$, the vertical composites $\lambda_f \bullet \bar{\lambda}_f\colon f \Rightarrow f$ and $\bar{\lambda}_f \bullet \lambda_f\colon \id_b \circ f \Rightarrow \id_b \circ f$ equal the appropriate identity $2$-morphisms,
*  for each $f\colon a \to b$, the vertical composites $\rho_f \bullet \bar{\rho}_f\colon f \Rightarrow f$ and $\bar{\rho}_f \bullet \rho_f\colon f \circ \id_a \Rightarrow f \circ \id_a$ equal the appropriate identity $2$-morphisms,
*  for each $a \overset{f}\to b \overset{g}\to c \overset{h}\to d$, the vertical composites $\bar{\alpha}_{h,g,f} \bullet \alpha_{h,g,f}\colon (h \circ g) \circ f \Rightarrow (h \circ g) \circ f$ and $\alpha_{h,g,f} \bullet \bar{\alpha}_{h,g,f}\colon h \circ (g \circ f) \Rightarrow h \circ (g \circ f)$ equal the appropriate identity $2$-morphisms,
*  for each $a \overset{f}\to b \overset{g}\to c$, the vertical composite $(\rho_g \triangleright f) \bullet \bar{\alpha}_{g,\id_b,f}$ equals the whiskering $g \triangleleft \lambda_f$, and
*  for each $a \overset{f}\to b \overset{g}\to c \overset{h}\to d \overset{i}\to e$, the vertical composites $((\bar{\alpha}_{i,h,g} \triangleright f) \bullet \bar{\alpha}_{i,h \circ g,f}) \bullet (i \triangleleft \bar{\alpha}_{h,g,f})$ and $\bar{\alpha}_{i \circ h,g,f}\bullet \bar{\alpha}_{i,h,g \circ f} $ are equal.

It is quite possible that there are errors or omissions in this list, although they should be easy to correct.  The point is not that one would *want* to write out the definition in such elementary terms (although apparently I just did anyway) but rather that one *can*.


## Examples

* Any [[strict 2-category]] is a bicategory in which the unitors and associator are identities.  This includes [[Cat]], [[MonCat]], the algebras for any strict [[2-monad]], and so on, at least as classically conceived.

* A [[monoidal category]] $M$ may be regarded as a bicategory $B M$ with a single object $\bullet$. The objects $A$ of $M$ become 1-cells $[A]: \bullet \to \bullet$ of $B M$; these are composed across the 0-cell $\bullet$ using the definition $[A] \circ_0 [B] = [A \otimes B]$, using the monoidal product $\otimes$ of $M$. The identity 1-cell $\bullet \to \bullet$ is $[I]$, where $I$ is the monoidal unit of $M$. The morphisms $f: A \to B$ become 2-cells $[f]: [A] \to [B]$ of $B M$. The associativity and unit constraints of the monoidal category $M$ transfer straightforwardly to associativity and unit data of the bicategory $B M$. The construction is a special case of [[delooping]] (see there). 

* Categories, [[anafunctor]]s, and natural transformations, which is a more appropriate definition of [[Cat]] in the absence of the [[axiom of choice]], form a bicategory that is not a strict 2-category.  Indeed, without the axiom of choice, the proper notion of bicategory is [[anabicategory]].

* [[ring|Rings]], [[bimodule]]s, and bimodule homomorphisms are the prototype for many similar examples.  Notably, we can generalize from rings to [[enriched category|enriched categories]].

* Objects, [[span]]s, and morphisms of spans in any category with [[pullback]]s also form a bicategory.

* The [[fundamental 2-groupoid]] of a space is a bicategory which is not necessarily strict (although it can be made strict fairly easily when the space is Hausdorff by quotienting by [[thin homotopy]], see [[path groupoid]] and [[fundamental infinity-groupoid]]). When the space is a CW-complex, there are easier and more computationally amenable equivalent strict 2-categories, such as that arising from the fundamental [[crossed complex]].


## Coherence theorems
{#Coherence}

One way to state the [[coherence theorem]] for bicategories is that every bicategory is [[equivalence of categories|equivalent]] to a strict $2$-category. This "strictification" is not obtained naively by forcing composition to be associative, but (at least in one construction) by freely adding new composites which are strictly associative.  Another way to state the coherence theorem is that every formal diagram of the constraints (associators and unitors) commutes.

Note that $n=2$ is the greatest value of $n$ for which every weak $n$-category is equivalent to a fully strict one; see [[semi-strict infinity-category]] and [[Gray-category]].

The proof of the coherence theorem is basically the same as the proof of the [[coherence theorem for monoidal categories]].  An abstract approach can be found in [[John Power|Power]]'s paper "A general coherence result."

The strictification [[adjunction]] between bicategories and strict 2-categories can be expressed in terms of [[3-categories]]; see [Campbell](#Campbell18).


## Terminology

Classically, "2-category" meant [[strict 2-category]], with "bicategory" used for the weak notion.  This led to the more general use of the prefix "2-" for strict (that is, strictly [[Cat]]-enriched) notions and "bi-" for weak ones.  For example, classically a "2-adjunction" means a Cat-enriched adjunction, consisting of two strict 2-functors $F,G$ and a strictly Cat-natural isomorphism of categories $D(F X, Y)\cong C(X, G Y)$, while a "biadjunction" means the weak version, consisting of two weak 2-functors and a pseudo natural equivalence $D(F X, Y)\simeq C(X, G Y)$.  Similarly for "2-equivalence" and "biequivalence," and "2-limit" and "bilimit."

We often use "2-category" to mean a strict or weak 2-category without prejudice, although we do still use "bicategory" to refer to the particular classical algebraic notion of weak 2-category.  We try to avoid the more general use of "bi-" meaning "weak," however.  For one thing, is it confusing; a "biproduct" could mean a weak [[2-limit]], but it could also mean an object which is both a product and a coproduct (which happens quite frequently in [[additive category|additive categories]]).

Moreover, in most cases the prefix is unnecessary, since once we know we are working in a bicategory, there is usually no point in considering strict notions at all.  Fully weak limits are really the only sensible ones to ask for in a bicategory, and likewise for fully weak adjunctions and equivalences.  Even in a strict 2-category, while we might need to say "strict" sometimes to be clear, we don\'t need to say "$2$-", since we know that we are not working in a mere category.  (Max Kelly pushed this point.)

When we do have a strict 2-category, however, other strict notions can be quite technically useful, even if our ultimate interest is in the weak ones.  This is somewhat analogous to the use of strict structures to model weak ones in [[homotopy theory]]; see [here](http://arxiv.org/abs/math/0702535) and [here](http://arxiv.org/abs/math/0607646) for good introductions to this sort of thing.


## Related concepts

* [[category]]

* **bicategory**

  [[(infinity,2)-category]]

* [[double bicategory]] (and at [[double category#double_bicategories|double category]])

* [[tricategory]]

* [[tetracategory]]

* [[n-category]]

* [[(infinity,n)-category]]

* [[pseudofunctor]]

* [[monoidal bicategory]]

* [[closed bicategory]]


Discussion about the use of the term "weak enrichment" above is at _[[weak enrichment]]_.

## References

* [[Jean Bénabou]], Introduction to Bicategories, _Lecture Notes in Mathematics 47_, Springer (1967), pp.1-77. ([doi](http://dx.doi.org/10.1007/BFb0074299))

See also the references at [[2-category]].

* [[A. J. Power]],  _A general coherence result._
J. Pure Appl. Algebra 57 (1989), no. 2, 165&#8211;173. [doi:10.1016/0022-4049(89)90113-8](http://dx.doi.org/10.1016/0022-4049%2889%2990113-8) [MR0985657](http://www.ams.org/mathscinet-getitem?mr=985657)

* {#Campbell18} [[Alexander Campbell]], _How strict is strictification?_, [arxiv](https://arxiv.org/abs/1802.07538)
 
Formalization in [[homotopy type theory]] (see also at [[internal category in homotopy type theory]]):

* [[Benedikt Ahrens]], Dan Frumin, Marco Maggesi, Niels van der Weide, _Bicategories in Univalent Foundations_ ([arXiv:1903.01152](https://arxiv.org/abs/1903.01152))

[[!redirects bicategory]]
[[!redirects bicategories]]

[[!redirects coherence theorem for bicategories]]
