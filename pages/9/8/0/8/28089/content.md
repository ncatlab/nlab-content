
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

A **supercategory** is a [[category]] [[enriched category|enriched]] in [[super vector spaces]] and even linear maps.
While there is nothing supercommutative about supercategories themselves, they provide the structure necessary to define supercommutative variants of more advanced structures like monoidal categories, analogous to how super vector spaces are not supercommutative themselves but needed to define [[supercommutative algebras]].

## Definition
Supercategories are categories enriched over the category of super vector spaces and even linear maps.
Concretely, this means that a **supercategory** is a category in which:

  - each $Hom(X,Y)$ carries the structure of a [[super vector space]], i.e. the structure of a vector space together with a decomposition $Hom(X,Y)\simeq Hom(X,Y)_{even}\oplus Hom(X,Y)_{odd}$ into an "even" part and an "odd" part,

  - each composition map $\circ:Hom(Y,Z)\times Hom(X,Y)\to Hom(X,Z)$ is bilinear,

  - parity is additive under composition, i.e. the composition of two morphisms of the same parity is always even and the composition of two morphisms of different parities is always odd.

A **superfunctor** between supercategories is similarly an [[enriched functor]], hence a [[functor]] that is linear on each hom-set and sends even morphisms to even morphisms and odd morphisms to odd morphisms. A **supernatural transformation** $\lambda:\F\Rightarrow G$ between superfunctors $F,G:C\to D$ is however not an [[enriched natural transformation]], but a collection of morphisms $\lambda_X=\lambda_{X,even}+\lambda_{X,odd}\in Hom(F X,G X)=Hom(F X,G X)_{even}\oplus Hom(F X,G X)_{odd}$ such that 
$\lambda_{Y,p}\circ F f=(-1)^{|f|p}G f\circ\lambda_{X,p}$ for all homogeneous $f\in Hom(X,Y)$. Supernatural transformations are called even or odd iff all their components are even resp. odd, turning the space of all supernatural transformations into a super vector space itself. Only the even supernatural transformations correspond to enriched natural transformations.

## Properties

The fact that compositions of even morphisms are even means that even morphisms constitute a wide subcategory $\underline C$ of any supercategory $C$. Even though any supercategory can be turned into a category by just forgetting the enrichment, it is this subcategory $\underline C$ that is often viewed as the underlying category of $C$. The reason for this is that super-versions of structures on $C$ restrict to genuine such structures on $\underline C$, analogous to how supercommutative algebras restrict to commutative algebras on their even parts.

Supercategories and superfunctors form a (super-)category $SCat$. The symmetric monoidal product on the category of super vector spaces induces a monoidal product $\boxtimes$ on $SCat$; however, the nontrivial choice of braiding reflects itself in the fact that this product $C\boxtimes D$ is given by the supercategory in which objects and morphisms are pairs of objects resp. morphisms in $C$ and $D$ but morphisms are composed as $(f_1\otimes f_2)\circ(g_1\otimes g_2)=(-1)^{|f_2||g_1|}(f_1\circ g_1)\otimes(f_2\circ g_2)$.

## Examples

* The category $SVect$ of super vector spaces and all linear maps is a supercategory whose underlying category $\underline SVect$ is precisely the category of super vector spaces and even linear maps discussed at [[super vector space]] and taken as the base of enrichment here.
* A supercategory with a single object is simply a super vector space with a bilinear multiplication satisfying $|ab|=|a|+|b|$ on homogeneous elements, hence a [[super algebra]].
* For any two supercategories $C,D$, superfunctors $C\Rightarrow D$ and supernatural transformations between them form a supercategory.

## Monoidal supercategories
A **monoidal supercategory** is a supercategory with structure analogous to that of a [[monoidal category]], but defined over the monoidal product $\boxtimes$ on $SCat$ defined above.

## See also

A **strict 2-supercategory** is a category enriched over the monoidal category $SCat$ defined above. Notions of (weak) **2-supercategories** and **monoidal 2-supercategories** also exist and arise e.g. in the context of odd [[Khovanov homology]]; see ([Schelstraete & Vaz 2023](SchelstraeteVaz2023)).

## References

* {#BrundanEllis2017} [[Jonathan Brundan]], [[Alexander P. Ellis]], _Monoidal Supercategories_,  Communications in Mathematical Physics **351** (2017) 1045–1089 &lbrack;[arXiv:1603.05928](https://arxiv.org/abs/1603.05928), [doi:10.1007/s00220-017-2850-9](https://doi.org/10.1007/s00220-017-2850-9)&rbrack;
 * {#SchelstraeteVaz2023} [[Léo Schelstraete]], [[Pedro Vaz]], _Odd Khovanov homology and higher representation theory_, preprint &lbrack;[arXiv:2311.14394](https://arxiv.org/abs/2311.14394)&rbrack;

[[!redirects supercategories]]