> This page considers Picard groupoids in themselves. For the concept of [[Picard groupoid of a monoidal category]], see there.

#Contents#
* table of contents
{:toc}

##Introduction

+-- {: .num_defn}
###### Definition

A _Picard groupoid_ is a [[symmetric monoidal|strict symmetric monoidal]] [[category]] $(\mathcal{A}, \otimes, 1)$ in which every [[object]] and every [[morphism]] is strictly [[inverse|invertible]] with respect to $\otimes$; that is to say: there is, for every object $a$ of $\mathcal{A}$, an object $a^{-1}$ of $\mathcal{A}$ such that $a \otimes a^{-1} = 1$, and similarly for morphisms.

=--

+-- {: .num_defn}
###### Remark

The notion of a Picard groupoid [[categorification|categorifies]] that of an [[abelian group]]. Note in particular that $\oplus$ and $0$ equip the set of objects of $\mathcal{A}$ with the structure of an abelian group.

=--

+-- {: .num_defn}
###### Remark

The notion of a Picard groupoid can be weakened in two (or three) directions: the monoidal structure can be weak instead of strict (or just the symmetry part), and the invertibility criterion can be asked to hold only up to isomorphism. On this page, we shall, however, work with the fully strict notion.

=--

##2-category of Picard groupoids

Picard groupoids assemble into a [[strict 2-category]]. The objects are Picard groupoids, the 1-arrows are strict [[monoidal functor|monoidal functors]] (these necessarily preserve both the symmetry and the object inverses), and the 2-arrows are [[monoidal natural transformation|monoidal natural transformations]]. 

This strict 2-category admits a [[closed monoidal category|closed]] [[symmetric monoidal 2-category|(fully) strict symmetric monoidal structure]], which categorifies the usual closed monoidal structure of the category of abelian groups.  

##Additivity of the homotopy category of Picard groupoids

The _homotopy category_ of the category of Picard groupoids consists, roughly speaking, of Picard groupoids up to equivalence. Formally, we can obtain it by [[decategorifying]] the 2-category of Picard groupoids, namely identifying all 1-arrows which are 2-isomorphic, and throwing away the 2-arrows. 

The closed monoidal structure of the 2-category of Picard groupoids, together with the fact that the objects of a Picard groupoid define an abelian group under $\oplus$ and $0$, provides immediately an [[enriched category|enrichment]] of the homotopy category of Picard groupoids over abelian groups. Moreover, it is obvious that this category has all coproducts. Thus it is an additive category.

##Model for stable homotopy 1-types

Picard groupoids are well-known to model stable homotopy 1-types, at least if one adopts the weak version of the invertibility condition. This is a stable version of the 1-truncated [[homotopy hypothesis]]. 

## Related concepts

* [[monoidal groupoid]]

* [[2-group]]

[[!redirects Picard groupoids]]