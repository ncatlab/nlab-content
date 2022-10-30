
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
$$F\colon C(x,y) \to D(F(x), F(y))$$
between [[hom sets]] is [[bijective]].  "Full and faithful" is sometimes shortened to "fully faithful" or "ff."   See also [[full subcategory]].


## Properties

* Together with [[bo functor|bijective-on-objects functors]], fully faithful  functors form an [[bo-ff factorization system|orthogonal factorization system]] on $Cat$; see [[bo-ff factorization system]]. More invariantly, pair them with [[essentially surjective functor]]s to get a bicategorial factorization system.

* A [[fully faithful functor]] (hence a [[full subcategory]] inclusion) [[reflected limit|reflects]] all [[limits]] and [[colimits]].  This is evident from inspection of the defining [[universal property]].
 {#FullSubcategoryInclusionsReflectCoLimits}

* Fully faithful functors are closed under [[pushouts]] in [[Cat]].  For ordinary categories this was proven by [Fritch and Latch](#FL); for [[enriched categories]] it is proven in [Stanculescu, Prop. 3.1](#Stanculescu), and for [[(∞,1)-categories]] it is proven in [Simspon, Cor. 16.6.2](#Simpson).


## Generalizations

* For [[(∞,1)-category|(∞,1)-categories]] the corresponding notion of fully faithful functor is described at [[fully faithful (∞,1)-functor]].  This is part of a bigger pattern at work here which is indicated at [[stuff, structure, property]] and [[k-surjective functor]].

* Inside a [[2-category]] there is a "representable" notion of [[ff morphism]].

* There is also a notion of fully faithful functor in [[enriched category theory]], which in general is stronger than being an ff morphism in the 2-category of enriched categories.  But it can be expressed internally in any [[proarrow equipment]].


## Related concepts

* [[essentially surjective functor]]

* [[full functor]]

* [[faithful functor]]

* [[equivalence of categories]]

* [[full and faithful (∞,1)-functor]]

## References

* R. Fritsch, D. M. Latch, Homotopy inverses for nerve, Math. Z. 177 (1981), no. 2, 147&#8211;179
 {#FL}

* [[Alexandru E. Stanculescu]], Constructing model categories with prescribed fibrant objects, [arxiv](https://arxiv.org/abs/1208.6005)
 {#Stanculescu}

* [[Carlos Simpson]], [[Homotopy Theory of Higher Categories]]
 {#Simpson}


[[!redirects full and faithful functor]]
[[!redirects full and faithful functors]]
[[!redirects fully faithful functor]]
[[!redirects fully faithful functors]]

[[!redirects full and faithful]]
[[!redirects fully faithful]]
