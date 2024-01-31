
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea 

The notion of **pseudomonoid** (sometimes also called a **monoidale**) in a [[monoidal 2-category]] is a [[categorification]] of the notion of a *[[monoid object]]* in a [[monoidal category]].

See [Street & Day (1997)](#StreetDay97)


The archetypical example are [[monoidal categories]], which are the pseudomonoids in the [[cartesian monoidal category|cartesian]] [[monoidal 2-category]] [[Cat]]. Similarly, [[monoidal enriched categories]] are pseudomonoids in [[VCat]].


Just as a monoid in a monoidal category $C$ can be equivalently defined as a [[monad]] in the corresponding one-object [[2-category]] $\mathbf{B}C$ (the [[delooping]] of $C$), so a pseudomonoid in a monoidal 2-category $C$ can equivalently be defined as a [[pseudomonad]] in the corresponding one-object [[3-category]] $\mathbf{B}C$.

## Variations

* A **map pseudomonoid** is a pseudomonoid whose multiplication and unit are [[bicategory of maps|maps]], i.e. [[left adjoints]].  This is a more appropriate notion for monoidal bicategories whose morphisms are [[profunctors]], since maps therein can be identified (modulo [[Cauchy completion]]) with [[functors]]. (However, it is typically better to work instead in a [[double category]], where one may distinguish between **tight pseudomonoids** and **loose pseudomonoids**.)

Other more special kinds of pseudomonoid are generalizations of special kinds of monoidal categories, including:

* braided pseudomonoids
* symmetric pseudomonoids
* balanced pseudomonoids
* closed pseudomonoids
* $\ast$-autonomous, a.k.a. [[Frobenius pseudomonoids]]
* compact closed (or autonomous) pseudomonoids

Eventually these should probably have their own pages.

## Properties

The 2-category of symmetric pseudomonoids in a symmetric monoidal 2-category has (weak) 2-coproducts given by the tensor product of underlying objects (analogously to how the category of [[commutative monoids]] in a monoidal category has coproducts given by the tensor product of the underlying objects).  This is proven in [Schaeppi, Appendix A](#Schaeppi).

## See also
* [[pseudoaction]]
* [[pseudomonad]]

## References 

* {#StreetDay97} [[Ross Street]], [[Brian Day]], *Monoidal bicategories and Hopf algebroids*, Advances in Mathematics, **129** 1 (1997) 99-157 &lbrack;[doi:10.1006/aima.1997.1649](https://doi.org/10.1006/aima.1997.1649)&rbrack;

* {#Schaeppi} Daniel Schäppi, *Ind-abelian categories and quasi-coherent sheaves*, [arXiv](https://arxiv.org/abs/1211.3678), 2014.

* Dominic Verdon, *Coherence for braided and symmetric pseudomonoids*, [arXiv](https://arxiv.org/abs/1705.09354).


[[!redirects pseudomonoid]]
[[!redirects pseudomonoids]]
[[!redirects pseudomonoid object]]
[[!redirects pseudomonoid objects]]
[[!redirects monoidale]]
[[!redirects monoidales]]
[[!redirects map pseudomonoid]]
[[!redirects map pseudomonoids]]

[[!redirects braided pseudomonoid]]
[[!redirects braided pseudomonoids]]
[[!redirects symmetric pseudomonoid]]
[[!redirects symmetric pseudomonoids]]
[[!redirects balanced pseudomonoid]]
[[!redirects balanced pseudomonoids]]
[[!redirects closed pseudomonoid]]
[[!redirects closed pseudomonoids]]
[[!redirects autonomous pseudomonoid]]
[[!redirects autonomous pseudomonoids]]
[[!redirects compact closed pseudomonoid]]
[[!redirects compact closed pseudomonoids]]

[[!redirects pseudo-monoid]]
[[!redirects pseudo-monoids]]
