
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

Generally, the term _Mackey functor_ refers to an [[additive functor]] from (a [[subcategory]] of) a [[category of correspondences]] (in a [[disjunctive category]] $\mathcal{C}$) to possibly any other [[additive category]] which however usually is the "base" abelian category. More generally the term now refers to the fairly obvious [[homotopy theory|homotopy theoretic]] or [[higher category theory|higher categorical]] refinements of this concept.

Therefore the concept of Mackey functors is similar to that of [[sheaves with transfer]] and as such appears (implicitly) in the discussion of [[motives]] (explicitly e.g. in [Kahn-Yamazaki 11, section 2](#KahnYamazaki11), where $\mathcal{C}$ is a category of suitable [[schemes]]. Much more relevant references are: [this article of Weibel](#Weibel05) and Voevodsky's seminal article defining his triangulated category of motives, specifically [Section 3.4](#Voevodsky00) about geometrical 0-motives).

Specifically, the concept was introduced and named as such in the context of [[representation theory]] ([Dress 71](#Dress71)) and [[equivariant homotopy theory]]/[[equivariant cohomology]] ([May 96](#May96)). Here the underlying [[category of correspondences]] is that in [[finite set|finite]] [[G-sets]], called the _[[Burnside category]]_.  

The [[equivariant homotopy groups]] $\pi_n(E)$ of a (genuine) [[G-spectrum]] $E$ organize into a Mackey functor on the [[Burnside category]] with values in [[abelian groups]]. This plays a key role in the [[equivariant Whitehead theorem]].  In fact, genunine [[G-spectra]] themselves are equivalent to Mackey [[(∞,1)-functors]] from the [[Burnside category]] to the [[(∞,1)-category of spectra]] ([GuillouMay 11](#GuillouMay11), [Barwick 14](#Barwick14)).


## Definition

### In higher category theory
We follow the account in ([Barwick 14](#Barwick14)), which incarnates a perspective of ([Lindner 76](#Lindner76)) in higher category theory.

Let $\mathcal{C}$ be a [[disjunctive (∞,1)-category]] and write $\Span(\mathcal{C})$ for the [[(∞,1)-category of correspondences]] in $\mathcal{C}$ and let $\mathcal{A}$ be an [[(∞,1)-category]] with finite products.

Then an _$\mathcal{A}$-valued semi-Mackey functor_ on $\mathcal{C}$ is a product-preserving functor

$$
  M \;\colon\; \Span(\mathcal{C}) \longrightarrow \mathcal{A}
  \,.
$$
If $\mathcal{A}$ is additive, we say that $M$ is a **Mackey functor**.

Notice that this means that $M$ is in particular:


1. a covariant [[(∞,1)-functor]] $(-)_\ast \colon\mathcal{C} \to \mathcal{A}$;

1. a contravariant [[(∞,1)-functor]], hence  $(-)^\ast \colon\mathcal{C}^{op} \to \mathcal{A}$;

1. satisfy the [[Beck-Chevalley condition]].

In order to understand the Beck-Chevalley condition, note that disjunctiveness of $\mathcal{C}$ implies that $\Span(\mathcal{C})$ is [[semiadditive (∞,1)-category|semiadditive]]. 

(More generally one may specify suitably chosen sub-$(\infty,1)$-categories $\mathcal{C}^\dagger, \mathcal{C}_\dagger \subset \mathcal{C}$ and restrict $\Span(\mathcal{C})$ to [[correspondences]] whose left leg is in $\mathcal{C}_\dagger$ and whose right leg is in $\mathcal{C}^\dagger$ ([Barwick 14, section 5](#Barwick14)).)

### In representation theory

In order to recover the original definition of [Dress 71](#Dress71), we fix $G$ a finite group, and we let $\mathbb{F}_G$ be the (disjunctive) category of finite $G$-sets.
Then, the above definition specializes to $G$ by defining $G$-Mackey functors as product-preserving functors

$$
   M \;\colon\; \Span(\mathbb{F}_G) \longrightarrow \mathcal{A}
  \,.
$$ 

$\Span(\mathbb{F}_G)$ has [[biproducts]] given by disjoint unions of finite $G$-sets;
when $\mathcal{A}$ is a [[semiadditive category]], such a functor may be decompiled into

1. a covariant functor $(-)_\ast \colon \mathcal{O}_G \to \mathcal{A}$ and

2. a contravariant functor $(-)^\ast \colon \mathcal{O}_G^{\op} \to \mathcal{A}$, subject to the conditions that
 
3. there exists a non-natural isomorphism $(-)_\ast \simeq (-)^\ast$, and

4. writing $R^H_J$ for the contravariant effect of in inclusion $J \subset H$ and $I^H_J$ for the covariant effect, $M$ satisfies the double coset formula
$$
  R_J^H I_K^H(-) \simeq \bigoplus_{x \in [J\backslash H/K]} I_{J \cap ^x K}^J R_{J^x \cap K}^{K}(-)
$$
for all $J,K \subset H$, where $^x K \coloneqq xKx^{-1}$.


## Examples

### In representation theory

For $\mathcal{A}$ taken to be (the [[derived category]]) of an [[abelian category]] (or better: postcomposed with a [[homological functor]] ) this definition reduces ([Barwick 14](#Barwick14)) to that of Mackey functors as originally defined in ([Dress 71](#Dress71)).
Fixing $G$ a finite group, we acquire the following examples (see section 3.2 of [Blumberg 17](#Blumberg17)).

1. Let $R \in \mathcal{A}$ be an object in $\mathcal{A}$. Then, the **constant Mackey functor** $\underline{R}$ assigns $R$ to every transitive $G$-set, whose restriction maps are all the identity, and whose transfer maps $G/H \rightarrow G/K$ are multiplication by $\left| H/K \right|$.

2. The **Burnside Mackey functor** $A(G)$ is defined by letting $A(G)([G/H])$ be the [[Grothendieck group]] of the cocartesian symmetric monoidal category of finite $H$-sets, with restriction and transfer given by restriction and induction, respectively.

3. The **representation Mackey functor** $R(G)$ is defined by letting $R(G)([G/H])$ be the [[Grothendieck group]] of the symmetric monoidal category of finite-dimensional $H$-representations,  with restriction and transfer given by restriction and induction,  respectively.

### Additive completion of semi-Mackey functors
{#AdditiveCompletion}
The free commutative monoid functor $\mathrm{Fr}\colon \mathcal{C} \rightarrow \mathrm{CMon}(\mathcal{C})$ is the unit of an adjunction whose left adjoint includes the category of (small) [[[biproduct|semiadditive categories]] into [[cartesian product|categories with products]];
specifically, given $\mathcal{B}$ a [[semiadditive category]], postcomposition with $\mathrm{Fr}$ induces an equivalence
\[
  \mathrm{Fun}^\times(\mathcal{B}, \mathcal{C}) \xrightarrow{\sim} \mathrm{Fun}^{\times} (\mathcal{B}, \mathrm{CMon}(\mathcal{C})),
\]
and in particular, it induces an equivalence
\[
  \mathrm{sMack}(\mathcal{C}) \simeq \mathrm{sMack}(\mathrm{CMon}(\mathcal{C}).
\]
We define _Mackey functors in $\mathcal{C}$_ to be the subcategory
\[
  \mathrm{Mack}(\mathcal{C}) \coloneqq \mathrm{sMack}(\mathrm{CGrp}(\mathcal{C})) \subset \mathrm{sMack}(\mathrm{CMon}(\mathcal{C})) \simeq \mathrm{sMack}(\mathcal{C})
\]

We then have the following.

\begin{proposition}
  Mackey functors form a [[reflective subcategory]] of semi-Mackey functors. 
\end{proposition}

This follows formally from the fact that the [[group completion]] functor $(-)_{\simeq}\colon \mathrm{CGrp}(\mathcal{C}) \subset \mathrm{CMon}(\mathcal{C})$ is compatible with products;
in particular, given $M$ a semi-Mackey functor, the value of $M_{\simeq}$ at the orbit $G/H$ is the [[group completion]] $M(G/H)_{\simeq}$, and the restrictions and transfers are gotten by group completing the restrictions and transfers of $M$.

### Equivariant spectra 
 {#EquivariantSpectra}

Let $G$ be a [[finite group]]. Let $\mathcal{C}= \mathbb{F}_G$ be the category of finite [[G-sets]]. Then $Corr_1(\mathcal{C})$ is essentially what is called the [[Burnside category]] of $G$ (possibly after abelianizing/stabilizing the hom-spaces suitably, but as ([Barwick 14](#Barwick14)) highlights, this is unnecessary when one is mapping out of this into something abelian/stable, as is the case here).

For $G$ finite, Mackey functors on $\mathcal{C}$ are equivalent to  genuine [[G-spectra]] ([Guillou-May 11, theorem 0.1](#GuillouMay11), [Barwick 14, below example B.6](#Barwick14)) (Notice that this equivalence does not in general hold if $G$ is not a finite group.)



(...)
 
For $E$ a [[genuine G-spectrum]], the corresponding spectral Mackey functor is given by the [[fixed point spectra]] of $E$

$$
  G/H \mapsto E(G/H) =  [\Sigma^\infty_+ G/H, E]^G \simeq E^H
  \,,
$$

where on the right we have the $G$-equivariant [[mapping spectrum]] from the [[equivariant suspension spectrum]] of the [[transitive action|transitive]] [[G-set]] $G/H$ to $E$.

(e.g. ([Guillou-May 11, remark 2.5](#GuillouMay11)), see also ([Schwede 15, p. 16](#Schwede15)) for restriction and section 4 culminating on p. 37 for transfer and compatibility).

Further, the corresponding abelian-group valued Mackey functor is

$$
  \pi_n(E) \colon G/H \mapsto [G/H_+\wedge S^n, X]_G
  \,,
$$

where now on the right we have just the [[homotopy classes]] of maps, i.e. the morphisms in the [[equivariant stable homotopy category]] (e.g. [Greenlees-May 95, p. 43](#GreenleesMay95))


(...)

### Group (co)homology
Given $U$ a $\mathbb{Z}[G]$-module, the cohomology $H^n(G,U)$, homology $H_n(G,U)$, and tate cohomology $\widehat H^n(G,U)$ form Mackey functors under the usual restriction and transfers (or corestriction).
See example 53.3 of [Thévenaz](#Thevenaz)

### Ideal class groups
Let $F$ be a field with $E/F$ a finite Galois extension and write $G \coloneqq \mathrm{Gal}(E/F)$.
Write $\mathrm{Cl}(E^H)$ for the ideal class group of $E^H$.
Then, extension of scalars yields a restriction map $\mathrm{Cl}(E^H) \rightarrow \mathrm{Cl}(E^K)$ and norm maps yield a map $\mathrm{Cl}(E^K) \rightarrow \mathrm{Cl}(E^H)$ satisfying a double coset formula;
together, these form a Mackey functor.
See example 53.12 of [Thévenaz](#Thevenaz).


## Cohomology with coefficients in a Mackey functor
 {#Cohomology}

We discuss [[cohomology]] of [[topological G-spaces]] with [[coefficients]]
in a Mackey functor, following notation and conventions as in ([May 96, sections IX, X](#May96)). See also ([Greenlees-May 95, p. 9](#GreenleesMay95)).


+-- {: .num_defn #CohomologyOfGSpace}
###### Defininition

For $X$ a [[pointed object|pointed]] [[G-CW complex]], define the [[chain complex]] $C_\bullet(X)$ of Mackey functors to be given by the stable [[equivariant homotopy groups]] of the quotient spaces $X^{\bullet}/X^{\bullet-1}$:

$$
  C_n(X) \coloneqq \pi_n(X^n/X^{n-1})
  \,,
$$

Then for $A$ any Mackey functor, the ordinary cohomology of $X$ with [[coefficients]] in $A$ is the [[cochain cohomology]] of the complex of homs of Mackey functors $C_n(X) \to A$:

$$
  H_G^n(X,A) \coloneqq H^n( Hom(C_\bullet(X), A) )
  \,.
$$

More generally, for $V$ a G-[[representation]], the $(n-V)$-[[RO(G)-grading|RO(G)-graded]] cohomology of $X$ with coefficients in $A$ is

$$
  H_G^{n-V}(X,A) = H_G^n(S^V \wedge X,A)
  \,.
$$
 
=--

([May 96, section X.4 def. 4.1, def. 4.2 ](#May96))

+-- {: .num_remark}
###### Remark

The corresponding [[reduced cohomology]] $\tilde H^n(-,A)$ is represented by maps into the [[Eilenberg-MacLane space|Eilenberg-MacLane G-space]]:

$$
  \tilde H^n(X,A) \simeq [X,K(A,n)]_G
  \,.
$$

=--

([Greenlees-May 95](#GreenleesMay95))


+-- {: .num_remark}
###### Remark

For this kind of cohomology, there is equivariant [[Serre spectral sequence]] ([Kronholm 10](#Kronholm10)).

=--

## Related concepts

* [[Tambara functor]]

## References

### Plain Mackey functors

The original article is

* {#Dress71} A. W. M. Dress, _Notes on the theory of representations of finite groups. Part I: The Burnside ring of a finite group and some AGN-applications, Bielefeld_, 1971, 

The span perspective is due to

* {#Lindner76} Harald Lindner, _A remark on Mackey-functors_, 1976 ([pdf](https://people.math.rochester.edu/faculty/doug/otherpapers/lindner.pdf))

Reviews and surveys:

* {#Blumberg17} [[Andrew Blumberg]], section 3.2 of _The Burnside category_, 2017 ([pdf](https://www.ma.utexas.edu/users/a.debray/lecture_notes/m392c_EHT_notes.pdf), [GitHub](https://github.com/adebray/equivariant_homotopy_theory))

* {#tomDieck87} [[Tammo tom Dieck]], Section II.9 of: _[[Transformation Groups]]_, de Gruyter 1987  ([doi:10.1515/9783110858372]( https://doi.org/10.1515/9783110858372))


* {#GreenleesMay95} [[John Greenlees]], [[Peter May]], _Equivariant stable homotopy theory_, in I.M. James (ed.), _Handbook of Algebraic Topology_ , pp. 279-325. 1995. ([pdf](http://www.math.uchicago.edu/~may/PAPERS/Newthird.pdf))

* {#May96} [[Peter May]], section IX.4 of _Equivariant homotopy and cohomology theory_ CBMS Regional Conference Series in Mathematics, vol. 91, Published for the Conference Board of the Mathematical Sciences, Washington, DC, 1996. With contributions by M. Cole, G. Comezana, S. Costenoble, A. D. Elmenddorf, J. P. C. Greenlees, L. G. Lewis, Jr., R. J. Piacenza, G. Triantafillou, and S. Waner. ([pdf](http://www.math.rochester.edu/u/faculty/doug/otherpapers/alaska1.pdf))

* {#Schwede15} [[Stefan Schwede]], around p. 16 of _[[Lectures on Equivariant Stable Homotopy Theory]]_, 2015 ([pdf](http://www.math.uni-bonn.de/people/schwede/equivariant.pdf))


*  Peter Webb, _A Guide to Mackey Functors_ ([pdf](http://www.math.rochester.edu/people/faculty/doug/otherpapers/WebbMF.pdf))


* [[Michael Hill]], [[Michael Hopkins]], [[Douglas Ravenel]], section 4 of _The Arf-Kervaire problem in algebraic topology: Sketch of the proof_ ([[HHRKervaire.pdf:file]])

  (with an eye towards application to the [[Arf-Kervaire invariant problem]])

* [[Megan Shulman]], chapter 2 of _Equivariant local coefficients and the $RO(G)$-graded cohomology of classifying spaces_ ([arXiv:1405.1770](http://arxiv.org/abs/1405.1770))

* {#Thevenaz} Jacques Thévenaz, chapter 8 of _$G$-algebras and modular representation theory_ ([pdf](https://infoscience.epfl.ch/server/api/core/bitstreams/403da7d5-c09b-40a9-9fd3-609d43f67517/content))


See also

* [[Tammo tom Dieck]], _Transformation groups_, Studies in Mathematics, vol. 8, Walter de Gruyter, Berlin, New York, 1987, x + 311 pp., 

* Serge Bouc, chapter 1 of _Green Functors and G-sets_, LNM 1671 (1997; paperback 2008) [doi:10.1007/BFb0095821](http://dx.doi.org/10.1007/BFb0095821)

* [[Tammo tom Dieck]], Equivariant homology and Mackey functors, Mathematische Annalen __206__, no.1, pp. 67--78, 1973 [doi:10.1007/BF01431529](http://dx.doi.org/10.1007/BF01431529)

* {#GreenleesMay95} [[John Greenlees]], [[Peter May]], appendix A of _Generalized Tate cohomology_, Mem. Amer. Math. Soc. 113 (1995) no 543 ([pdf](http://www.math.rochester.edu/people/faculty/doug/otherpapers/GM-Tate-543.pdf))


* D. Tambara, _The Drinfeld center of the category of Mackey functors_, J. Algebra __319__, 10, pp. 4018-4101 (2008) [doi:10.1016/j.jalgebra.2008.02.011](http://dx.doi.org/10.1016/j.jalgebra.2008.02.011),

* Elango Panchadcharam, _Categories of Mackey Functors_, PhD thesis, Macquarie Univ. 2006

* {#Kronholm10} [[William Kronholm]], _The $RO(G)$-graded Serre spectral sequence_, Homology Homotopy Appl. Volume 12, Number 1 (2010), 75-92. ([pdf](http://www.swarthmore.edu/NatSci/wkronho1/serre.pdf), [Euclid](https://projecteuclid.org/euclid.hha/1296223823)),

For Mackey functors [[enriched]] over [[closed category|closed]] [[multicategories]]:

* [[Niles Johnson]], [[Donald Yau]], _Homotopy Theory of Enriched Mackey Functors_ ([arXiv:2212.04276](https://arxiv.org/abs/2212.04276))

Relation of Mackey functors to [[sheaves with transfer]] in the theory of [[motives]]:

* {#KahnYamazaki11} [[Bruno Kahn]], Takao Yamazaki, _Voevodsky's motives and Weil reciprocity_, Duke Mathematical Journal 162, 14 (2013) 2751-2796 ([arXiv:1108.2764](http://arxiv.org/abs/1108.2764))

* {#Weibel05} Weibel, Charles. _Transfer functors on k-algebras._ Journal of Pure and Applied Algebra 201.1-3 (2005): 340-366

* {#Voevodsky00} Voevodsky, Vladimir. _Triangulated categories of motives over a field._ Cycles, transfers, and motivic homology theories 143 (2000): 188-238.

[[categorification|Categorification]] to Mackey [[2-functors]] is discussed found in 

* [[Paul Balmer]], [[Ivo Dell'Ambrogio]], _Mackey 2-functors and Mackey 2-motives_, ([arXiv:1808.04902](https://arxiv.org/abs/1808.04902))

### Spectral Mackey functors

See the [[Spectral Mackey functor theorem]]. The general concept of spectral Mackey functors

* {#Barwick14} [[Clark Barwick]], _Spectral Mackey functors and equivariant algebraic K-theory (I)_, Adv. Math., 304:646–727,  2017 ([doi:10.1016/j.aim.2016.08.043](https://doi.org/10.1016/j.aim.2016.08.043), [arXiv:1404.0108](http://arxiv.org/abs/1404.0108))

* {#Barwick15} [[Clark Barwick]], [[Saul Glasman]], Jay Shah, _Spectral Mackey functors and equivariant algebraic K-theory (II)_ ([arXiv:1505.03098](http://arxiv.org/abs/1505.03098))

* {#Glasman15} [[Saul Glasman]], _Stratified categories, geometric fixed points and a generalized Arone-Ching theorem_ ([arXiv:1507.01976](https://arxiv.org/abs/1507.01976), [talk notes pdf](http://www-users.math.umn.edu/~sglasman/strattalk.pdf))

#### In equivariant stable homotopy theory

The construction of [[equivariant stable homotopy theory]] in terms of spectral Mackey functors is originally due to 

* {#GuillouMay11} [[Bert Guillou]], [[Peter May]],  _Models of $G$-spectra as presheaves of spectra, ([arXiv:1110.3571](http://arxiv.org/abs/1110.3571))

* [[Bert Guillou]], [[Peter May]], _Permutative $G$-categories in equivariant infinite loop space theory_, Algebr. Geom. Topol. 17 (2017) 3259-3339 ([arXiv:1207.3459](http://arxiv.org/abs/1207.3459))

* {#Nardin12} [[Denis Nardin]], section 2.6 and appendix A of _Stability and distributivity over orbital ∞-categories_, 2012 ([hdl.handle.net/1721.1/112895]( http://hdl.handle.net/1721.1/112895), [pdf](https://www.math.univ-paris13.fr/~nardin/thesis.pdf))

The generalization of [[K-theory of permutative categories]] to spectral Mackey functors is discussed in

* {#BohmannOsorno14} [[Anna Marie Bohmann]], [[Angélica Osorno]], _Constructing equivariant spectra via categorical Mackey functors_, Algebraic & Geometric Topology 15.1 (2015): 537-563 ([arXiv:1405.6126](http://arxiv.org/abs/1405.6126))

#### In Goodwillie calculus

Discussion of [[Goodwillie calculus]] via [[spectral Mackey functors]]

* {#Glasman16} [[Saul Glasman]], _Goodwillie calculus and Mackey functors_  ([arXiv:1610.03127](https://arxiv.org/abs/1610.03127))




[[!redirects Mackey functors]]

[[!redirects spectral Mackey functor]]
[[!redirects spectral Mackey functors]]
