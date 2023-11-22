
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--


#Content#
* table of contents 
{:toc}

## Idea

The concept of a _$2$-vector space_ is supposed to be a [[vertical categorification|categorification]] of the concept of a [[vector space]]. As usual in the game of 'categorification', this requires us to think deeply about what an ordinary vector space really is, and then attempt to categorify that idea. 

### What is a vector space?

There are at least three distinct conceptual roles which vectors and vector spaces play in mathematics:

1. A vector is a _column of numbers_. This is the way vector spaces appear in quantum mechanics, sections of line bundles, elementary linear algebra, etc. 

1. A vector is a _direction in space_. Vector spaces of this kind are often the infinitesimal data of some global structure, such as tangent spaces to manifolds, Lie algebras of Lie groups, and so on.

1. A vector is an element of a [[module]] over the base [[ring]]/[[field]].

The first of these may be thought of as motivating the notion of  

* [Kapranov-Voevodsky $2$-vector space](#KV2VectorSpace) 

the second the notion of

* [Baez-Crans $2$-vector spaces](#BaezCrans2VectorSpaces)

the third the notion of

* [$2$-Modules](#AbstractApproach).


### Kapranov&#8211;Voevodsky $2$-vector spaces
 {#KV2VectorSpace}

These were introduced in [Kapranov & Voevodsky 1991](#KapranovVoevodsky91).


The idea here is that just as a vector space can be regarded as a [[module]] over the [[ground field]] $k$, a $2$-vector space $W$ should be a [[category]] which is a [[monoidal category module]] with some nice properties (such as being an abelian category) over a suitable [[monoidal category]] $V$ which plays the role of the categorified ground field. There is then an obvious [[bicategory]] of such module categories.

In fact, Kapranov and Voevodsky defined a **Kapranov--Voevodsky $2$-vector space** as an abelian $\Vect$-module category equivalent to $\Vect^n$ for some $n$.

While this definition makes a lot of sense it does not give an abstract characterization of 2-vector spaces. That is, it is hardly different to simply defining a 2-vector space as a category equivalent to $Vect^n$.

Because Kapranov--Voevodsky $2$-vector spaces categorify the idea of a vector space as a 'state-space' of a system, they are the notion of $2$-vector space which feature on the right hand side of extended TQFTs (functors from higher [[cobordism]] categories to higher vector spaces).

An example of a Kapranov--Voevodsky $2$-vector space is $Rep(G)$, the category of [[representations]] of a finite group $G$. 

### Baez&#8211;Crans $2$-vector spaces
 {#BaezCrans2VectorSpaces}

These were explicitly described in [Baez & Crans 2004](#BaezCrans04).


A **Baez--Crans $2$-vector space** is defined as a [[internal category|category internal]] to [[Vect]]. They categorify the idea of a vector as a 'direction in space', and crop up when considering the _infinitesimal directions_ of a structure, such as in higher [[Lie theory]]. In fact, (following for instance from an extension of the [[Dold-Kan correspondence|Dold-Kan theorem]] by Brown and Higgins), [[strict omega-category|strict omega-categories]] internal to $\Vect$ are equivalent to chain complexes in non-negative degree and can be regarded as strict $Disc(k)$-$\infty$-modules. This allows to conceive much of [[homological algebra]] and many of the structures appearing in higher [[Lie theory]] -- for instance the definition of $L_\infty$-[[L-infinity-algebra|algebras]], as being about $\infty$-vector spaces. Regarding a chain complex as an $\infty$-vector space is useful conceptually for understanding the meaning of some constructions on chain complexes, while of course chain complexes themselves are well suited for direct computation with the $\infty$-vector spaces which they are equivalent to. (See also the remark about different notions of 2-vector spaces further below.)

They were also independently introduced and studied [Forrester-Barker (2004)](#Forrester-Barker).

## $2$-modules and $2$-linear maps as algebras and bimodules
 {#AbstractApproach}

It is possible to conceive of 2-vector spaces of the Kapranov--Voevodsky and Baez--Crans type from a single unified perspective. Namely, by regarding the [[ground field]] itself as a [[discrete category]] we can think of it as a [[monoidal category]]. A $Disc(k)$-module category is a category whose space of objects and space of morphisms are both $k$-modules &#8211; ordinary vector spaces! &#8211; such that all structure morphisms (source, target, identity, composition) respect the $k$-action &#8211; hence are linear maps. These are categories internal to $\Vect_k$ which are equivalent to chain complexes of vector spaces concentrated in degree 0 and 1.

In other words, a Baez--Crans $2$-vector space can be thought of as a Kapranov--Voevodsky $2$-vector space, if one 'categorifies' the ground field by simply regarding it as a discrete monoidal category. 

For $V$ a general symmetric [[closed monoidal category]] the full bicategory of all [[monoidal category modules]] over $V$ is in general hard to get under control, but what is more tractable is the sub-bicategory which may be addressed as the bicategory of $V$-modules _with basis_ namely the category $V-Mod$ in the sense of [[enriched category theory]] with

* objects are categories $C$ [[enriched category|enriched over]] $V$, to be thought of as placeholders for their categories of [[modules]], $Mod_C := [C,V]$

* morphisms $C \to D$ are [[bimodules]] $C^{op}\otimes D \to V$;

* $2$-morphisms are natural transformations.

Notice that all $V$-categories $Mod_C$ of modules over a $V$-category $C$ are naturally [[copower|tensored]] over $V$ and hence are [[monoidal category modules]] over $V$. In analogy to how a vector space $W$ (a $k$-module) is equipped with a basis by finding a set $S$ such that $W \simeq [S,k]$, we can think of a general [[monoidal category module]] $W$ over $V$ to be equipped with a basis by providing an [[equivalence]] $W \simeq [C,V]$, for some $V$-category $C$. In this sense $V-Mod$ is the category of $V$ 2-vector spaces with basis.

All of the examples on this page are special cases of this one.

### $\Vect$-enriched categories

According to the above a $Vect$-[[enriched category]] $C$ can be regarded as a basis for the $Vect$-module $Mod_C = [C,Vect]$. A $Vect$-enriched category is just an  [[algebroid]]. If it has a single object it is an [[algebra]] and $Mod_C$ is the familiar category of modules over an algebra.

Notice that, by the very definition of [[Morita equivalence]], two algebras (algebroids) have equivalent module categories, and hence can be regarded as different bases for the same $\Vect$ $2$-vector space, iff they are Morita equivalent.

$Vect$-enriched categories as models for 2-vector spaces appear in 

* Jacob Lurie, _On the classification of topological field theories_ ([pdf](http://www.math.harvard.edu/~lurie/papers/cobordism.pdf)) (see example 1.2.4)

* B. To&#235;n, G. Vezzosi, _A note on Chern character, loop spaces and derived algebraic geometry_, ([arXiv](http://arxiv.org/abs/0804.1274), p. 6)

$2$-vector spaces in the sub-bicategory of algebras ($Vect$-enriched categories with a single object), bimodules and intertwiners are discussed in

* U. Schreiber, _AQFT from $n$-functorial QFT_ ([arXiv](http://arxiv.org/abs/0806.1079)) (appendix A)

and 

* U. Schreiber and K. Waldorf, _Connections on non-abelian gerbes and their holonomy_ ([arXiv](http://arxiv.org/abs/0808.1923))

Some blog discussion of this point is at [2-Vectors in Trodheim](http://golem.ph.utexas.edu/category/2007/11/2vectors_in_trondheim.html). 

### $Ch(Vect)$-enriched categories

More generally one can replace vector spaces by complexes of vector spaces and consider $Ch(Vect)\Mod$ as a model for the $2$-category of $2$-vector spaces (with basis): its objects are [[dg-category|dg-categories]].

It is argued in

* B. To&#235;n, G. Vezzosi, _A note on Chern character, loop spaces and derived algebraic geometry_, ([arXiv](http://arxiv.org/abs/0804.1274), p. 6)

that the generalization from $Vect\Mod$ to $Ch(Vect)\Mod$ is necessary to have a good notion of higher sheaves of sections of 2-vector bundles, i.e. of higher coherent sheaves.


### Revisiting Kapranov&#8211;Voevodsky 2-vector spaces

Upon further restriction of $\Vect\Mod$ to 2-vector spaces whose basis is a _discrete category_, namely a set $S$ (or the $Vect$-enriched category over $S$ which has just the [[ground field]] object sitting over each element of $S$) one arrives at $Vect$-modules of the form

$$
  [S, Vect] = Mod_{k^n} \simeq (Vect)^n
$$

(where $k^n$ denotes the algebra of diagonal $n\times n$-matrices). These are precisely Kapranov--Voevodsky $2$-vector spaces.


### Elgueta $2$-vector spaces

Another notion of 2-vector space which also includes Kaparanov--Voevodsky as particular instances is given in

* Josep Elgueta, _Generalized 2-vector spaces and general linear 2-groups_ ([arXiv](http://arxiv.org/abs/math/0606472))

The idea is to categorify the construction of a vector space as the space of finite linear combinations of elements in any set $S$. Instead of $S$, we start now with any category $C$, and take first the free $k$-linear category generated by $C$, and next the additive completion of this. Kapranov--Voevodsky $2$-vector spaces are recovered when $C$ is discrete. In some cases this gives nonabelian and even non-[[Karoubian category|Karoubian]] (i.e., nonidempotent complete) categories. This is the case, for instance, when we take as $C$ the one-object category defined by the additive monoid of natural numbers. The 2-vector space this category generates can be identified with the category of free $k[T]$-modules, which is nonKaroubian.


### Infinite-dimensional K-V 2-vector spaces

We can regard the objects of the $n$-dimensional  Kapranov--Voevodsky $2$-vector space $Vect^n$ &#8211; which are $n$-tuples of vector spaces &#8211; as vector bundles over the finite set of $n$ elements. This has an obvious generalization to vector bundles over any topological space &#8211; in terms of modules these are the finitely generated projective modules of the algebra of continuous functions on this space. So categories of vector bundles can be regarded as infinite-dimensional 2-vector spaces. For the case that the underlying topological space is a _measure space_ such infinite dimensional K-V 2-vector spaces have been studied in

* John C. Baez, Aristide Baratin, [[Laurent Freidel]], Derek K. Wise, _Infinite-dimensional representations of 2-groups_ ([arXiv](https://arxiv.org/abs/0812.4969)) 


### Using a modular tensor category

The relevance of module categories as models for 2-vector spaces was apparently first realized in the context of [[conformal field theory]], where the monoidal category $V$ in question is a [[modular tensor category]]. A result by Victor Ostrik showed that _all_ $V$-module categories are equivalent to $Mod_A$ for $A$ some one-object $V$-enriched category (i.e., an algebra internal to $V$) in

* V. Ostrik, _Module Categories, weak Hopf Algebras and Modular Invariants_ ([arXiv](http://arxiv.org/abs/math.QA/0111139), [blog](http://golem.ph.utexas.edu/string/archives/000717.html))


## 2-Modules as modules over a 2-ring

One can go further and derive the identification of 2-modules and 2-linear maps with algebras and bimodules from a more fundamental notion of modules over [[2-rings]]. For the moment see there at
_[2-ring -- Compatibly monoidal presentable categories](2-rig#CompatiblyMonoidalPresentableCategories)_ for more details.

## Remark on the different notions of $2$-vector spaces

As the above list shows, there are 2-vector spaces of very different kind. There is not *the* notion of 2-vector space which is the universal right answer. Different notions of vector spaces are applicable and useful in different situations.  This can be regarded as nothing but a more pronounced incarnation of the fact that already ordinary vector space appear in different flavors which are useful in different situations (real vector spaces, complex vector spaces, vector spaces over a [[finite field]], etc.)

For instance $Disc(k)$-module categories are crucial for higher [[Lie theory]] but 2-bundles with fibers $Disc(k)$-module categories are comparatively boring as far as general 2-bundles go, as they are essentially complexes of ordinary vector bundles. See 

* [[Nils. A. Baas]], Marcel B&#246;kstedt, Tore August Kro, _Two-Categorical Bundles and Their Classifying Spaces_, J. K-Theory, 10 (2012) 299 - 369, with a preliminary version at  ([arXiv](http://arxiv.org/abs/math/0612549))

## $2$-Hilbert spaces##

2-vector spaces have to a large extent been motivated by and applied in (2-dimensional) [[quantum field theory]]. In that context it is usually not the concept of a plain vector space which needs to be categorified, but that of a Hilbert space. 

2-Hilbert spaces as a $\Hilb$-[[enriched category|enriched categories]] with some extra properties were discribed in

* John Baez, _Higher-Dimensional Algebra II: 2-Hilbert Spaces_ ([arXiv](http://arxiv.org/abs/q-alg/9609018)) .

In applications one often assumes these 2-Hilbert spaces to be [[semisimple algebra|semisimple]] in which case such a 2-Hilbert space is a Kapranov--Voevodsky $2$-vector space equipped with extra structure.

A review of these ideas of 2-Hilbert spaces as well as applications of 2-Hilbert spaces to finite group representation theory are in

* Bruce Bartlett, _On unitary 2-representations of finite groups and topological quantum field theory_ ([arXiv](http://arxiv.org/abs/0901.3975))

## Properties

### Tannaka duality

[[!include structure on algebras and their module categories - table]]
  


## Related concepts

* [[vector space]]

* [[module category]], ("[[actegory]]")

* **2-vector space**, [[2-representation]]

  * [[2-ring]]

  * [[2Mod]]

  * [[2-vector bundle]]

  * _[[TwoVect]]_ is a Mathematica software package for computer algebra with 2-vector spaces

* [[n-vector space]]


## References

### As $n$-tuples of vector spaces
 {#ReferencesAsnTuplesOfvectorSpaces}

The notion of 2-vector spaces as $n$-tuples of vector spaces is due to

* {#KapranovVoevodsky91} [[Mikhail Kapranov]], [[Vladimir Voevodsky]], *$2$-categories and Zamolodchikov tetrahedra equations* in *Algebraic groups and their generalization: quantum and infinite-dimensional methods*, University Park, PA (1991) (eds: W. J. Haboush and B. J. Parshall), Proc. Sympos. Pure Math. 56 (Amer. Math. Soc., Providence RI 1994), pp. 177-259 &lbrack;[pdf](https://www.math.ias.edu/vladimir/sites/math.ias.edu.vladimir/files/1994_Kapranov_Voevodsky.pdf)&rbrack;


### As 2-term chain complexes
 {#ReferencesAsTwoTermChainComplexes}

The notion of 2-vector spaces as 2-term [[chain complexes]] is due to

* {#BaezCrans04} [[John C. Baez]], [[Alissa S. Crans]], §3 of: *Higher-Dimensional Algebra VI: Lie 2-Algebras*, Theor. Appl. Categor. **12** (2004) 492-528 &lbrack;[arXiv:math/0307263](https://arxiv.org/abs/math/0307263)&rbrack;

and used in

* {#Forrester-Barker} [[Magnus Forrester-Barker]], *Representations of Crossed Modules and $Cat^1$-Groups*, PhD thesis U. Wales Bangor (2004) &lbrack;[pdf](http://www.maths.bangor.ac.uk/research/ftp/theses/forrester-barker.pdf)&rbrack;



### As algebras with bimodules between them
 {#ReferencesAsAlgebrasWithBimodules}

The notion of 2-vector spaces with 2-linear maps between them as algebras with bimodules between them (subsuming the definition in [Kapranov & Voevodsky 1991](#KapranovVoevodsky91) as the special case of algebras that are [[direct sums]] of the [[ground field]]) is due to 

* [[Urs Schreiber]], §A of: *AQFT from n-functorial QFT*, Commun. Math. Phys. **291** (2009) 357-401 &lbrack;[arXiv:0806.1079](https://arxiv.org/abs/0806.1079), [doi:10.1007/s00220-009-0840-2](https://doi.org/10.1007/s00220-009-0840-2)&rbrack;

following earlier discussion in 

* [[Urs Schreiber]], *[2-vectors in Trondheim](https://golem.ph.utexas.edu/category/2006/10/topology_in_trondheim_and_kro.html)* (2006)

* [[Urs Schreiber]], *[Topology in Trondheim and Kro, Baas & Bökstedt on 2-vector bundles](https://golem.ph.utexas.edu/category/2007/11/2vectors_in_trondheim.html)* (2007)

which is picked up in 

* [[Urs Schreiber]], [[Konrad Waldorf]], §4.4 of: *Connections on non-abelian Gerbes and their Holonomy*, Theory Appl. Categ., **28** 17 (2013)  476-540 &lbrack;[arXiv:0808.1923](https://arxiv.org/abs/0808.1923), [tac:28-17](http://www.tac.mta.ca/tac/volumes/28/17/28-17abs.html)&rbrack;

and further developed into a theory of [[2-vector bundles]] (via algebra bundles with bundles of bimodules between them) in:

* {#KristelLudewigWaldorf22} [[Peter Kristel]], [[Matthias Ludewig]], [[Konrad Waldorf]], *The insidious bicategory of algebra bundles* &lbrack;[arXiv:2204.03900](https://arxiv.org/abs/2204.03900)&rbrack;

Essentially the same notion also appears, apparently independently, in:

* {#FreedHopkinsTeleman09} [[Daniel S. Freed]], [[Michael J. Hopkins]], [[Jacob Lurie]], [[Constantin Teleman]], §7.1 with Ex. 2.13 in: *[[Topological Quantum Field Theories from Compact Lie Groups]]* &lbrack;[arXiv:0905.0731](https://arxiv.org/abs/0905.0731)&rbrack;

The notion is reviewed in a list of "standard" definitions in [BDSPV15](#BDSPV15), without however referencing it.

See also at

* _[[geometry of physics]]: [[geometry of physics - modules]]_

the section on 2-modules.

### Further discussion

Review includes

* {#BDSPV15} [[Bruce Bartlett]], [[Christopher L. Douglas]], [[Chris Schommer-Pries]], [[Jamie Vicary]], *A bestiary of 2–vector spaces*, Appendix A in:  *Modular categories as representations of the 3-dimensional bordism 2-category* &lbrack;[arXiv:1509.06811](https://arxiv.org/abs/1509.06811)&rbrack;


Another definition of 2-modules over [[2-rings]] (see there for more) is in 

* {#CJF} [[Alexandru Chirvasitu]], [[Theo Johnson-Freyd]], _The fundamental pro-groupoid of an affine 2-scheme_, Applied Categorical Structures, Vol 21, Issue 5 (2013), pp. 469–522. ([DOI](http://dx.doi.org/10.1007/s10485-011-9275-y), [arXiv:1105.3104](http://arxiv.org/abs/1105.3104))
 

A treatment of [[2-representations]] of [[Lie 2-groups]] is in

* Zhen Huan, _2-Representations of Lie 2-groups and 2-Vector Bundles_ ([arXiv:2208.10042](https://arxiv.org/abs/2208.10042))


[[!redirects 2-vector spaces]]

[[!redirects 2-module]]
[[!redirects 2-modules]]
