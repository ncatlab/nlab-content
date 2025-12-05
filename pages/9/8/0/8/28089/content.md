
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Super-Algebra and Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
=--
=--

\tableofcontents

## Idea

A **supercategory** is a [[category]] [[enriched category|enriched]] in [[super vector spaces]] and even linear maps. Concretely, this means that a supercategory is a category in which:

- each $Hom(X,Y)$ carries the structure of a [[super vector space]], i.e. the structure of a vector space together with a decomposition $Hom(X,Y)\simeq Hom(X,Y)_{even}\oplus Hom(X,Y)_{odd}$ into an "even" part and an "odd" part,

- each composition map $\circ:Hom(Y,Z)\times Hom(X,Y)\to Hom(X,Z)$ is bilinear,

- the composition of two even or two odd morphisms is always even, and the composition of one even and one odd morphism is always odd.

A **superfunctor** between supercategories is similarly an [[enriched functor]], hence a [[functor]] that is linear on each hom-set and sends even morphisms to even morphisms and odd morphisms to odd morphisms.

Notions of **monoidal supercategories**, **2-supercategories** and **monoidal 2-supercategories** also exist and arise e.g. in the context of odd [[Khovanov homology]]; see ([Schelstraete & Vaz 2023](SchelstraeteVaz2023)).

## References

* {#BrundanEllis2017} [[Jonathan Brundan]], [[Alexander P. Ellis]], _Monoidal Supercategories_,  Communications in Mathematical Physics **351** (2017) 1045–1089 &lbrack;[arXiv:1603.05928](https://arxiv.org/abs/1603.05928), [doi:10.1007/s00220-017-2850-9](https://doi.org/10.1007/s00220-017-2850-9)&rbrack;
 * {#SchelstraeteVaz2023} [[Léo Schelstraete]], [[Pedro Vaz]], _Odd Khovanov homology and higher representation theory_, preprint &lbrack;[arXiv:2311.14394](https://arxiv.org/abs/2311.14394)&rbrack;

[[!redirects supercategories]]