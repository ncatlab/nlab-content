

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{: toc}

## Definition of Ho(Cat)

**Ho(Cat)** is a name for the [[homotopy category]] of [[Cat]].  That is, $Ho(Cat)$ is the [[category]]

* whose objects are ([[small category|small]]) categories, and
* whose morphisms are [[natural isomorphism]] classes of [[functors]].

This is an instance of a general construction which, given a [[2-category]], or more generally an [[n-category]], produces a [[1-category]] with the same objects and whose morphisms are [[equivalence]] classes of 1-morphisms in the original $n$-category.  Sometimes this is called the 1-[[truncation]] and denoted $\tau_1$.

It can also be viewed as an instance of the homotopy category of a [[model category]] (or more generally a [[category with weak equivalences]]).  The category $Ho(Cat)$ as defined above is equivalent to the category obtained from $Cat$ by forcing all [[equivalences of categories]] to be isomorphisms (by [[localization|localizing]]).  This is for the same reason that the category $hTop$ of [[topological spaces]] and [[homotopy]] classes of [[continuous maps]] is equivalent to the category obtained from $Top$ by inverting the homotopy equivalences (namely, the existence of [[cylinder objects]] and/or [[path objects]]).  Indeed, a [[cylinder object]] for a category $C$ is the [[product category]] $C \times I$ where $I$ is the category with two objects 0 and 1 and an isomorphism $0 \to 1$.  It is not difficult to see that an isomorphism of functors is the same as a [[homotopy]] of functors with the respect to the [[canonical model structure]] on $Cat$.

## Subcategories of Ho(Cat)

Some notable full subcategories of $Ho(Cat)$ include

* $Ho(Gpd)$, the homotopy category of the category [[Gpd]] of [[groupoids]].  Note that this is equivalent to the homotopy category of (unbased) [[homotopy 1-types]].
* The category whose objects are [[groups]] and whose morphisms are [[conjugacy class]]es of [[group homomorphism]]s.  This can be identified with the full subcategory of $Ho(Gpd)$ whose objects are the connected groupoids.  This category sometimes arises in the study of [[gerbes]].


## Ho(Cat)-categories

Like the homotopy category of any model category, $Ho(Cat)$ has [[products]] and [[coproducts]], and is in particular a [[cartesian monoidal category]].  Therefore, we can talk about categories [[enriched category|enriched over]] $Ho(Cat)$.  Such a "$Ho(Cat)$-category" consists of

* a collection of objects $x,y,z$
* for each pair of objects, a category $C(x,y)$
* for each object $x$, an objects $id_x\in C(x,x)$
* for each triple of objects, a functor $C(y,z)\times C(x,y)\to C(x,z)$

such that the usual associativity and unit diagrams for an enriched category commute up to isomorphism.  The difference between a $Ho(Cat)$-category and a [[bicategory]] is that in a $Ho(Cat)$-category, *no coherence axioms* are required of the [[associator]] and [[unitor]] isomorphisms; they are merely required to *exist*.  Thus a $Ho(Cat)$-category can be thought of as an "incoherent bicategory."  In particular, any bicategory has an underlying $Ho(Cat)$-category.

Although $Ho(Cat)$-categories are not very useful, there are some interesting things that can be said about them.  For instance:

* Any $Ho(Cat)$-category which is equivalent, as a $Ho(Cat)$-category, to a bicategory, is itself in fact a bicategory.
* Any [[2-functor]] between bicategories which induces an equivalence of underlying $Ho(Cat)$-categories is in fact itself an equivalence of bicategories (or "biequivalence").

An example of a $Ho(Cat)$-category that does not come from any bicategory is sketched in [this MathOverflow answer](https://mathoverflow.net/a/346613).


## Other limits and colimits {#OtherLimits}

Although $Ho(Cat)$ has products and coproducts, like most homotopy categories it is not well-endowed with other [[limits]].

This section historically used the [[cospan]]

$$\array{&& \mathbb{Z}/3 \\ && \downarrow^j \\ \mathbb{Z}/2 & \underset{i}{\to} & S_3}$$

to demonstrate that $Ho(Cat)$ fails to have [[pullbacks]].
However, the pullback of this particular diagram does, in fact, exist in $Ho(Cat)$, as shown in [this MathOverflow answer](https://mathoverflow.net/a/512698/160838).

## Related concepts

* [[canonical model structure]]

* [[Ho(CombModCat)]]

[[!include categories of categories - contents]]


category: category
