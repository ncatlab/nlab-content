
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

By the _Burnside category_ of a [[finite group]] $G$ one means either 

1. the [[category of correspondences]] in [[finite set|finite]] [[G-sets]] (Prop. \ref{PermutativeCategoryOfFiniteGSets} below)

1. or an abelianization of that

   1. either by [[group completion]] of its monoidal [[hom-groupoids]] to an [[additive category|additive]] [[1-category]] (Def. \ref{AdditiveBurnsideCategory} below);

   1. or by forming the [[K-theory of a permutative category]] of the [[hom-groupoids]] to a [[(∞,1)-category of spectra|spectra]]-[[enriched (∞,1)-category]] (Def. \ref{SpectralBurnsideCategory} below).

The plain _[[Burnside ring]]_ is the [[endomorphism ring]] of the [[terminal object|terminal]] [[G-set]] in the [[additive category|additive]] version of the category (Example \ref{BurnsideRingIsEndomorphismRingInBurnsideCategory} below).

The [[functors]]/[[additive functors]]/[[enriched (∞,1)-functors]] from the Burnside category to, in particular, the [[category of abelian groups]]/[[(∞,1)-category of spectra]] are called _[[Mackey functors]]_.

A [[functor]] out of the Burnside category is called a _[[Mackey functor]]_, specifically if it is an [[Ab]]-[[enriched functor]] to [[Ab]] out of the [[additive category]]-version of the Burnside category. A [[spectra]]-[[enriched functor]] out of the spectral Burnside category to [[Spectra]] is called a _[[spectral Mackey functor]]_, for emphasis. These spectral Mackey functors are [[equivalence of (infinity,1)-categories|equivalent]] to [[genuine G-spectra]].

## Definition
 {#Definition}

There are various incarnations of the Burnside category as [[enriched categories]], in varying degree of sophistication of the enriching "[[cosmos]]" are all induced from the canonical structure of [[permutative categories]] on the [[correspondences]] between two fixed [[finite set|finite]] [[G-sets]] (made explicit as Prop. \ref{PermutativeCategoryOfFiniteGSets} below). This yields the Burnside category as

1. _[enriched in permutative categories](#AsEnrichedInPermutativeCategories)_;

1. _[enriched in abelian groups](#AsEnrichedInabelianGroups)_;

1. _[enriched in spectra](#EnrichedInSpectra)_.

+-- {: .num_prop #PermutativeCategoryOfFiniteGSets}
###### Proposition
**(the [[permutative category]] of [[finite set|finite]] [[G-sets]])**

For $G$ be a [[finite group]], write $G FinSet_{sk}$ for the [[skeleton]] of the [[category]] of [[finite set|finite]] [[G-sets]]. 

Its [[objects]] may be identified with [[pairs]] $(n,\rho)$ consisting of a [[natural number]] $n$, reflecting the [[finite set]] $\{1,2, \cdots, n\}$, and a [[group homomorphism]] $\rho \;\colon\; G \longrightarrow S_n = Aut(\{1,2, \cdots, n\})$ from $G$ to the [[symmetric group]] on $n$ elements, reflecting the [[automorphism]] group of that finite set.

Its [[morphisms]] $(n_1,\rho_1) \overset{ f }{\longrightarrow} (n_2, \rho_2)$ are [[functions]] $f \;\colon\; \{1, 2, \cdots, n_1\} \longrightarrow \{1,2, \cdots, n_2\}$ that intertwine $\rho_1$ and $\rho_2$.

The [[coproduct]] $\sqcup$ of [[G-sets]] ([[disjoint union]]) makes this [[skeleton]] a [[permutative category]] $\big( G FinSet_{sk}, \sqcup \big)$.

In the same way its [[slice category]] over any object $X \in G FinSet_{sk}$ becomes a [[permutative category]] $\big( G FinSet_{sk}/_{X}, \sqcup \big)$ under disjoint union of [[domains]].

Similarly, the [[Cartesian product]] of finite $G$-sets can be restricted to these [[skeleta]] to produce [[bipermutative categories]] $\big( G FinSet_{sk}/_{X}, \sqcup, \times \big)$.

Finally, restriction to [[isomorphisms]] (passage to [[cores]]) yields the bipermutative [[groupoids]] $\big( Core(G FinSet_{sk})/_{X}, \sqcup, \times \big)$.

=--

(e.g. [Guillou-May 11, Def. 1.3](#GuillouMay11), [Bohmann-Osorno 14, Def. 1.4](#BohmannOsorno14))


### As enriched in permutative categories 
 {#AsEnrichedInPermutativeCategories}

+-- {: .num_defn #AdditiveBurnsideCategory}
###### Definition
**([[PermCat]]-[[enriched category|enriched]] [[Burnside category]])**

The [[(2,1)-category of correspondences]] $Corr(G FinSet)$ is [[equivalence of (infinity,1)-categories|equivalent]] to the [[(2,1)-category]] whose [[objects]] are the [[finite set|finite]] [[G-sets]] and whose [[hom-categories]] are the [[permutative category|permutative]] [[cores]] of [[skeleta]] of [[slice categories]] of [[G-sets]] from Def. \ref{PermutativeCategoryOfFiniteGSets}, over the [[Cartesian product]] of [[source]] and [[domain]] [[G-sets]]:

$$
  Corr(G FinSet)\big( S_1, S_2  \big)
  \;\simeq\;
  Core(G FinSet_{sk}/_{S_1 \times S_2})
  \,.
$$

This locally skeletal [[(2,1)-category]] is the _[[PermCat]]-[[enriched category|enriched]] Burnside category_ $G Burn_{pc}$_ 

It may be regarded as an [[enriched category]] over the [[multicategory]] [[PermCat]] of [[permutative categories]] (a $\mathbf{PC}$-cateory in the sense of [Guillout 10](#Guillout10)).


=--

([Guillou-May 11, Def. 1.6](#GuillouMay11), [Bohmann-Osorno 14, Def. 7.1, 7.2](#BohmannOsorno14))

### As enriched in abelian groups
 {#AsEnrichedInabelianGroups}

+-- {: .num_defn #AdditiveBurnsideCategory}
###### Definition
**(additive Burnside category)**

The _additive Burnside category_ $G Burn_{ad}$ of $G$ is the [[additive category]] obtained from the [[PermCat]]-[[enriched category|enriched]] Burnside category $G Burn_{pc}$ (Def. \ref{AdditiveBurnsideCategory}) under replacing each [[hom-object|hom]]-[[permutative category]] $Core(G FinSet_{sk}/_{S_1 \times S_2})$ with its [[Grothendieck group]], hence with the [[abelian group]] which is the [[group completion]] 

$$
  K \;\colon\; PermCat \overset{\text{iso classes}}{\longrightarrow} CMon \overset{K}{\longrightarrow} Ab
$$

of the [[commutative monoid]] of [[isomorphism classes]] of [[objects]] in $Core(G FinSet_{sk}/_{S_1 \times S_2})$, under [[disjoint union]]:


$$
  G Burn_{ab}
  \;\coloneqq\;
  K_{\bullet} G Burn_{pc}  
  \,.
$$

=--


+-- {: .num_example #BurnsideRingIsEndomorphismRingInBurnsideCategory}
###### Example
**([[Burnside ring]] is [[endomorphism ring]] of additive Burnside category)**

The [[endomorphism ring]] of the [[terminal object|terminal]] [[G-set]] (the [[point]] $\ast$ equipped with the, necessarily, [[trivial action]]) in the additive Burnside category (Def. \ref{AdditiveBurnsideCategory}) is the _[[Burnside ring]]_ $A(G)$:

$$
  End_{G Burn_{ad}}(\ast, \ast)
  \;\simeq\;
  A(G)
$$


=--



### As enriched in spectra
 {#EnrichedInSpectra}

+-- {: .num_defn #SpectralBurnsideCategory}
###### Definition
(**[[Spectra]]-[[enriched category|enriched]] [[Burnside category]])**

Since construction of [[K-theory spectra of permutative categories]] applies  [[hom-object]]-wise to [[PermCat]]-[[enriched categories]] ([this Prop.](multifunctor#MonoidalFunctoriality))

$$
  \mathbb{K}_\bullet
  \;\colon\;
  PermCat Cat \longrightarrow Spectra Cat
$$

the image of the [[PermCat]]-[[enriched category|enriched]] [[Burnside category]] $G \mathcal{E}$ from Def. \ref{AdditiveBurnsideCategory} under forming [[hom-object]]-wise the [[K-theory spectra of permutative categories]] yields a [[Spectra]]-[[enriched category]]

$$
  G Burn_{sp}
  \;\coloneqq\;
  \mathbb{K}_\bullet G Burn_{pc}  
  \,.
$$

This is called the _spectral Burnside category_.

=--

([Guillou-May 11, Def. 1.12](#GuillouMay11), [Bohmann-Osorno 14, Def. 7.3](#BohmannOsorno14))

## Properties

### Relation to $G$-Spectra

+-- {: .num_prop #GSpectraAreSpectralMackeyFunctors}
###### Proposition
**([[G-spectra]] are spectral presheaves on the spectral Burnside category)**

There is a [[zig-zag]] of [[Quillen equivalences]]

$$
  [ G Burn_{sp}, Spectra ]
  \;\simeq_{Qu}^{zigzag}\;
  G Spectra
$$

between the [[model structure on functors|model category of]] [[Spectra]]-[[enriched presheaves]] over the [[spectral Burnside category]] from Def. \ref{SpectralBurnsideCategory} ("[[spectral Mackey functors]]") and that of [[genuine G-spectra]].

This equivalence is such that the [[spectral Mackey functor]] corresponding to a fibrant [[G-spectrum]] $E$ assigns to the [[transitive action|transitive]] [[G-set]] $G/H$ the [[fixed point spectrum]] $E^H$:

$$
  G/H 
    \;\mapsto\; 
  E(G/H)
    \;\coloneqq\;
  [\Sigma^\infty_G G/H, E]^G
    \;\simeq\;
  E^H
  \,.
$$

=--

([GuillouMay 11, theorem 1.13, corollary 1.14, remark 2.5](#GuillouMay11)).



## Related concepts

* [[Burnside ring]]

* [[Mackey functor]], [[equivariant stable homotopy theory]]

* [[disjunctive (∞,1)-category]]

## References

Lecture notes include:

* {#Blumberg17} [[Andrew Blumberg]], section 3.1 of _The Burnside category_, 2017 ([pdf](https://www.ma.utexas.edu/users/a.debray/lecture_notes/m392c_EHT_notes.pdf), [GitHub](https://github.com/adebray/equivariant_homotopy_theory))

The spectrally-enriched version and its role in the equivalent description of [[G-spectra]] via [[spectral Mackey functors]] is due to

* {#GuillouMay11} [[Bert Guillou]], [[Peter May]], _Models of $G$-spectra as presheaves of spectra, ([arXiv:1110.3571](http://arxiv.org/abs/1110.3571))

A beautified review is given in

* {#BohmannOsorno14} [[Anna Marie Bohmann]], [[Angélica Osorno]], section 7 of _Constructing equivariant spectra via categorical Mackey functors_, Algebraic & Geometric Topology 15.1 (2015): 537-563 ([arXiv:1405.6126](http://arxiv.org/abs/1405.6126))

making use of

* {#Guillout10} [[Bertrand Guillou]], _Strictification of categories weakly enriched in symmetric monoidal categories_, Theory Appl. Categ., 24:No. 20, 564–579, 2010 ([TAC](http://www.tac.mta.ca/tac//volumes/24/20/24-20abs.html))


[[!redirects Burnside categories]]

[[!redirects spectral Burnside category]]
[[!redirects spectral Burnside categories]]

[[!redirects additive Burnside category]]
[[!redirects additive Burnside categories]]

