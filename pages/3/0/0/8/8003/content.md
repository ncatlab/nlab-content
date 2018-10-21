
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

To a [[permutative category]]  $C$ is naturally associated a [[Gamma-space]], hence a [[symmetric spectrum]]. The [[generalized (Eilenberg-Steenrod) cohomology]] theory [[Brown representability theorem|represented]] by this is called the 
_([[algebraic K-theory|algebraic]]) [[K-theory]]_ of (or represented by) $C$.

If the category is  even a [[bipermutative category]] then the corresponding [[K-theory of a bipermutative category]] in addition has [[E-infinity ring]] structure, hence is a [[multiplicative cohomology theory]].

## Definition
 {#Definition}

### Via topological group completion
 {#ViaTopologicalGroupCompletion}

For $\mathcal{C}$ a [[category]], write ${\vert \mathcal{C}\vert} \in$ [[classical model structure on simplicial sets|sSet]] $\simeq_{Qu}$ [[classical model structure on topological spaces|Top]] for its [[nerve]]/[[geometric realization]]. (Beware that this is often denoted $B C$, instead, but that notation clashes with that for [[delooping]], which we also need in the following.)

For $\mathcal{C}$ a [[permutative category]] its [[nerve]]/[[geometric realization]] $\vert \mathcal{C} \vert$ is naturally a [[topological monoid]] ([Quillen 70](#Quillen70) see e.g. [May 13, theorem 4.10](#May13)), hence admits a [[bar construction]]/[[classifying space]] $B {\vert \mathcal{C}\vert}$. The [[loop space]] of that

$$
  (\mathbb{K}\mathcal{C})_0
  \;\coloneqq\; 
  \Omega B {\vert C\vert}
  \,,
$$

being an [[∞-group]], may be regarded as the [[homotopy theory|homotopy theoretic]] [[group completion]] of the [[topological monoid]] ${\vert \mathcal{C}\vert}$. 

This is the degree-0 space in the _algebraic K-theory [[spectrum]] $\mathbb{K}\mathcal{C}$ of the permutative category_  $\mathcal{C}$ (see e.g. [May 13, def 4.11](#May13)).

By ([Dwyer-Kan 80, prop. 3.7, prop. 9.2, remark 9.7](#DwyerKan80)) the operation $\Omega B (-)$ is the [[derived functor]] of [[group completion]], so that this construction ought to be a model for the [[K-theory of a symmetric monoidal (∞,1)-category]].

In particular, under [[decategorification]], its [[group]] of [[connected components]] is the actual [[Grothendieck group]] $K(-)$ of the [[isomorphism classes]] of [[objects]] in $\mathcal{C}$:

$$
  \pi_0
  \left( 
    \mathbb{K} \mathcal{C}
  \right)
  \;\simeq\;
  K\left(
    \mathcal{C}/_\sim, \oplus 
  \right)
$$

(recalled e.g. in [Bohmann-Osorno 14, p. 14](#BohmannOsorno14)).

In particular for $R$ a [[topological ring]] one considers $C$ a [[skeletal category|skeleton]] of the [[groupoid]] of ([[finitely generated module|finitely generated]]) [[projective modules]] over $R$. Then the K-theory of $C$ is the [[algebraic K-theory]] of $R$ (e.g. [May 13, p. 25](#May13))

$$
  \mathbb{K}\left( R Mod^{fin}_{proj} \right)
  \;\simeq\;
  K R
  \,.
$$


### Via Gamma spaces

Write $FinSet^{*/}$ for the [[category]] of [[pointed objects|pointed]] [[finite sets]].

For $C$ a [[permutative category]], there is naturally a [[functor]]

$$
  \widebar {C}_{(-)}
  \;\colon\; 
  FinSet^{*/} \to Cat
$$

$$
  A \mapsto \widebar C_A
$$

such that (...).

([Elmendorf-Mandell, theorem 4.2](#ElmendorfMandell06))

Accordingly, postcomposition with the [[nerve]] $N : Cat \to sSet$ produces from $C$ a [[Gamma-space]] $N \widebar C$. To this corresponds a [[spectrum]] 

$$
  K^{Seg} C \coloneqq \{N \widebar C_{S_\bullet^n}\}
  \,.
$$ 

This is the _K-theory spectrum of $C$_.

([Elmendorf-Mandell, def. 4.3](#ElmendorfMandell06))

## Properties

### Monoidal functoriality

+-- {: .num_prop #MonoidalFunctoriality}
###### Proposition

The construction of K-theory spectra of permutative categories constitutes a [[multifunctor]]

$$
  \mathbb{K}
  \;\colon\;
  PermCat
    \longrightarrow
  Spectra
$$

between [[multicategories]] of [[permutative categories]] (under [[Deligne tensor product]]) and [[spectra]] (under [[smash product of spectra]]). 

Hence for a multilinear functor of permutative categories

$$
  F 
    \;\colon\;
  \mathcal{A}_1 \times \cdots \times \mathcal{A}_n
  \longrightarrow
  \mathcal{B}
$$

there is a compatibly induced morphism of K-[[spectra]] out of the [[smash product of spectra|smash product]]

$$
  \mathbb{K}(\mathcal{A}_1) 
    \wedge
    \cdots
    \wedge
  \mathbb{K}(\mathcal{A}_n)
  \longrightarrow
  \mathbb{K}(\mathcal{B})
  \,.
$$


This implies that the construction further extends to a [[2-functor]] from the [[2-category]] $PermCat Cat$ of [[enriched categories]] over the [[multicategory]] of [[permutative categories]] to that of [[enriched categories]] of [[spectra]]:

$$
  \mathbb{K}_\bullet
  \;\colon\;
  PermCat Cat \longrightarrow Spectra Cat
$$

which applies $\mathbb{K}$ to each [[hom-object]].

=--

([May 80, theorem 1.6, Theorem 2.1](#May80), [Elmendorf-Mandell 04, theorem 1.1](#ElmendorfMandell04), [Guillou 10, Theorem 1.1](#Guillou10)


## Examples
 {#Examples}

+-- {: .num_example #OrdinaryAlgebraicKTheoryFromPermutativeCategoryOfProjectiveModules}
###### Example
**(ordinary [[algebraic K-theory]])**

For $R$ a [[commutative ring]], let $\mathcal{C} = R Mod_{pr}$ its [[category of modules|category of]] [[finitely generated module|finitely generated]] [[projective modules]] regarded as a [[permutative category]]. Then 

$$
  K (R Mod^{pr}_{fin}) \;\simeq\; K R
$$ 

is the classical [[algebraic K-theory]] spectrum of the ring $R$. 

=--

(e.g. [Elmendorf-Mandell 04, p. 10](#ElmendorfMandell04)).


+-- {: .num_example #StableCohomotopyIsKTheoryOfFinSet}
###### Example
**([[stable cohomotopy]] is K-theory of [[FinSet]])**

Let $\mathcal{C} = $ [[FinSet]] be a [[skeleton]] of the category of [[finite sets]], regarded as a [[permutative category]]. Then 

$$
  K(FinSet) \;\simeq\; \mathbb{S}
$$

is the [[sphere spectrum]], hence represents the [[cohomology theory]] called _[[stable cohomotopy]]_.

=--

(due to [Segal 74, Prop. 3.5](#Segal74), see also [Priddy 73](#Priddy73))

+-- {: .num_remark #StableCohomotopyIsAlgebraicKTheoryOverFieldWithOneElement}
###### Remark
**([[stable cohomotopy]] as [[algebraic K-theory]] over the [[field with one element]])**

Since ([[pointed sets|pointed]]) [[finite sets]] may be regarded as the modules over the "[[field with one element]]" $\mathbb{F}_1$ (see [there](field+with+one+element#Modules)), 

$$
  \mathbb{F}_1 Mod
  \;=\;
  FinSet^{\ast/}
$$

one may read example \ref{StableCohomotopyIsKTheoryOfFinSet} in view of example \ref{OrdinaryAlgebraicKTheoryFromPermutativeCategoryOfProjectiveModules} as saying that [[stable cohomotopy]] is the algebraic K-theory of the [[field with one element]]:

$$
  K \mathbb{F}_1 \;=\; \mathbb{S}
  \,.
$$

This perspective is highlighted for instance in ([Deitmar 06, p. 2](#Deitmar06), [Guillot 06](#Guillot06)).

=--

## Related concepts

* [[K-theory of a bipermutative category]]

* [[algebraic K-theory of a symmetric monoidal (∞,1)-category]]

## References

* {#Quillen70} [[Daniel Quillen]], _Cohomology of groups_, Proceedings of the international congress of mathematics 1970

* {#Quillen} [[Daniel Quillen]], _On the group completion of a simplicial monoid_

* {#Priddy73} [[Stewart Priddy]], _Transfer, symmetric groups, and stable homotopy theory_, in _Higher K-Theories_, Springer, Berlin, Heidelberg, 1973. 244-255 ([pdf](https://link.springer.com/content/pdf/10.1007/BFb0067060.pdf))

* {#Segal74} [[Graeme Segal]], _Catgeories and cohomology theories_, Topology vol 13 (1974)  ([pdf](http://ncatlab.org/nlab/files/SegalCategoriesAndCohomologyTheories.pdf))
 
* [[Peter May]], _The spectra associated to permutative categories_, Topology 17 (1978) ([pdf](http://www.math.uchicago.edu/~may/PAPERS/23.pdf))

* {#May13} [[Peter May]], _$E_\infty$-Spaces, group completions, and permutative categories_, in [[Graeme Segal]] (ed.) _New Developments in Topology_, Cambirdge University Press 2013 ([pdf](http://www.math.uchicago.edu/~may/PAPERS/13.pdf), [doi:10.1017/CBO9780511662607.008](https://doi.org/10.1017/CBO9780511662607.008))

* {#May80} [[Peter May]], _Pairings of categories and spectra_, J. Pure Appl. Algebra, 19:299–346, 1980

* {#DwyerKan80} [[William Dwyer]], [[Daniel Kan]], _Simplicial localization of categories_, Journal of pure and applied algebra 17 (1980) 267-284

* [[Anthony Elmendorf]], [[Michael Mandell]], _Permutative categories as a model of connective stable homotopy_, in: [[Birgit Richter]] (ed.) _Structured Ring spectra_, Cambridge University Press (2004)

* {#ElmendorfMandell04} [[Anthony Elmendorf]], [[Michael Mandell]], _Rings, modules and algebras in infinite loop space theory_, Adv. in Math. 205 (2006), no. 1, 163-228 ([arXiv:math/0403403](https://arxiv.org/abs/math/0403403))
 
* {#ElmendorfMandell09} [[Anthony Elmendorf]], [[Michael Mandell]], _Permutative categories, multicategories, and algebraic K-theory_, Algebraic & Geometric Topology 9 (2009) 2391-2441 ([arXiv:0710.0082](http://arxiv.org/abs/0710.0082), [euclid:1513797088](https://projecteuclid.org/euclid.agt/1513797088))

* {#Guillou10} [[Bertrand Guillou]], _Strictification of categories weakly enriched in symmetric monoidal categories_, Theory Appl. Categ., 24:No. 20, 564–579, 2010.

The interpretation of [[stable cohomotopy]] as the algebraic K-theory over the [[field with one element]] is adopted in

* {#Deitmar06} [[Anton Deitmar]], _Remarks on zeta functions and K-theory over $\mathbb{F}_1$_ ([arXiv:math/0605429](https://arxiv.org/abs/math/0605429))

* {#Guillot06} [[Pierre Guillot]], _Adams operations in cohomotopy_ ([arXiv:0612327](https://arxiv.org/abs/math/0612327))

The generalization of K-theory of permutative categories to [[Mackey functors]] is discussed in

* {#BohmannOsorno14} [[Anna Marie Bohmann]], [[Angélica Osorno]], _Constructing equivariant spectra via categorical Mackey functors_, Algebraic & Geometric Topology 15.1 (2015): 537-563 ([arXiv:1405.6126](http://arxiv.org/abs/1405.6126))

Generalization to [[equivariant stable homotopy theory]] and [[G-spectra]] is discussed in 

* {#GuillouMay12} [[Bert Guillou]], [[Peter May]], around section 4.4 of  _Permutative $G$-categories in equivariant infinite loop space theory_ ([arXiv:1207.3459](http://arxiv.org/abs/1207.3459))



[[!redirects K-theory of permutative categories]]

[[!redirects algebraic K-theory of a permutative category]]
[[!redirects algebraic K-theory of permutative categories]]

[[!redirects K-theory spectrum of a permutative category]]
[[!redirects K-theory spectra of permutative categories]]
