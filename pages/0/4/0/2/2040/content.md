
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

Generally, the term _Mackey functor_ refers to an [[additive functor]] from a ([[subcategory]] of) a [[category of correspondences]] (in a [[disjunctive category]] $\mathcal{C}$) to possibly any other [[additive category]] which however usually is the "base" abelian category. More generally the term now refers to the fairly obvious [[homotopy theory|homotopy theoretic]] or [[higher category theory|higher categorical]] refinements of this concept.

Therefore the concept of Mackey functors is similar to that of [[sheaves with transfer]] and as such appears (implicitly) in the discussion of [[motives]] (explicitly e.g. in [Kahn-Yamazaki 11, section 2](#KahnYamazaki11), where $\mathcal{C}$ is a category of suitable [[schemes]]).

Specifically, the concept was introduced and named as such in the context of [[representation theory]] ([Dress 71](#Dress71)) and [[equivariant homotopy theory]]/[[equivariant cohomology]] ([May 96](#May96)). Here the underlying [[category of correspondences]] is that in [[finite set|finite]] [[G-sets]], called the _[[Burnside category]]_.  

The [[equivariant homotopy groups]] $\pi_n(E)$ of a (genuine) [[G-spectrum]] $E$ organize into a Mackey functor on the [[Burnside category]] with values in [[abelian groups]]. This plays a key role in the [[equivariant Whitehead theorem]].  In fact, genunine [[G-spectra]] themselves are equivalent to Mackey [[(∞,1)-functors]] from the [[Burnside category]] to the [[(∞,1)-category of spectra]] ([GuillouMay 11](#GuillouMay11), [Barwick 14](#Barwick14)).


## Definition

We follow the modern account in ([Barwick 14](#Barwick14)).

Let $\mathcal{C}$ be a [[disjunctive (∞,1)-category]] and write $Corr_1(\mathcal{C})^\otimes$ for the [[(∞,1)-category of correspondences]] in $\mathcal{C}$, regarded as a [[symmetric monoidal (∞,1)-category]] with respect to its [[coproduct]] (which is a [[biproduct]] by disjunctiveness of $\mathcal{C}$).

Write $\mathcal{A} = $[[Spectra]]${}^{\oplus}$ for the [[(∞,1)-category of spectra]] regarded as a [[symmetric monoidal (∞,1)-category]] with respect to [[direct sum]].  More generally $\mathcal{A}$ could be any [[symmetric monoidal (∞,1)-category|symmetric monoidal]] [[stable (∞,1)-category]]

Then a (spectral) _Mackey functor_ on $\mathcal{C}$ is a [[monoidal (∞,1)-functor]] of the form


$$
  S \;\colon\; Corr_1(\mathcal{C})^\otimes \longrightarrow \mathcal{A}^{\oplus}
  \,.
$$

Notice that this means that $S$ is in particular


1. a covariant [[(∞,1)-functor]] $(-)_\ast \colon\mathcal{C} \to \mathcal{A}$;

1. a contravariant [[(∞,1)-functor]], hence  $(-)^\ast \colon\mathcal{C}^{op} \to \mathcal{A}$;

1. satisfying the [[Beck-Chevalley condition]].

(More generally one may specify suitably chosen sub-$(\infty,1)$-categories $\mathcal{C}^\dagger, \mathcal{C}_\dagger \subset \mathcal{C}$ and restrict $Corr_1$ to [[correspondences]] whose left leg is in $\mathcal{C}_\dagger$ and whose right leg is in $\mathcal{C}^\dagger$ ([Barwick 14, section 5](#Barwick14)).)


## Examples

### Dress' Mackey functors

For $\mathcal{A}$ taken to be (the [[derived category]]) of an [[abelian category]] (or better: postcomposed with a [[homological functor]] ) this definition reduces ([Barwick 14](#Barwick14)) to that of Mackey functors as originally defined in ([Dress 71](#Dress71)).


### Equivariant spectra 
 {#EquivariantSpectra}

Let $G$ be a [[finite group]]. Let $\mathcal{C}= G Set$ be its category of [[G-sets]]. Then $Corr_1(\mathcal{C})$ is essentially what is called the [[Burnside category]] of $G$ (possibly after abelianizing/stabilizing the hom-spaces suitably, but as ([Barwick 14](#Barwick14)) highlights, this is unnecessary when one is mapping out of this into something abelian/stable, as is the case here).

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

See also

* [[Tammo tom Dieck]], _Transformation groups_, Studies in Mathematics, vol. 8, Walter de Gruyter, Berlin, New York, 1987, x + 311 pp., 

* Serge Bouc, chapter 1 of _Green Functors and G-sets_, LNM 1671 (1997; paperback 2008) [doi:10.1007/BFb0095821](http://dx.doi.org/10.1007/BFb0095821)

* [[Tammo tom Dieck]], Equivariant homology and Mackey functors, Mathematische Annalen __206__, no.1, pp. 67--78, 1973 [doi:10.1007/BF01431529](http://dx.doi.org/10.1007/BF01431529)

* {#GreenleesMay95} [[John Greenlees]], [[Peter May]], appendix A of _Generalized Tate cohomology_, Mem. Amer. Math. Soc. 113 (1995) no 543 ([pdf](http://www.math.rochester.edu/people/faculty/doug/otherpapers/GM-Tate-543.pdf))


* D. Tambara, _The Drinfeld center of the category of Mackey functors_, J. Algebra __319__, 10, pp. 4018-4101 (2008) [doi:10.1016/j.jalgebra.2008.02.011](http://dx.doi.org/10.1016/j.jalgebra.2008.02.011)

* Elango Panchadcharam, _Categories of Mackey Functors_, PhD thesis, Macquarie Univ. 2006

* {#Kronholm10} [[William Kronholm]], _The $RO(G)$-graded Serre spectral sequence_, Homology Homotopy Appl. Volume 12, Number 1 (2010), 75-92. ([pdf](http://www.swarthmore.edu/NatSci/wkronho1/serre.pdf), [Euclid](https://projecteuclid.org/euclid.hha/1296223823))

Relation of Mackey functors to [[sheaves with transfer]] in the theory of [[motives]]:

* {#KahnYamazaki11} [[Bruno Kahn]], Takao Yamazaki, _Voevodsky's motives and Weil reciprocity_, Duke Mathematical Journal 162, 14 (2013) 2751-2796 ([arXiv:1108.2764](http://arxiv.org/abs/1108.2764))

[[categorification|Categorification]] to Mackey [[2-functors]] is discussed found in 

* [[Paul Balmer]], [[Ivo Dell'Ambrogio]], _Mackey 2-functors and Mackey 2-motives_, ([arXiv:1808.04902](https://arxiv.org/abs/1808.04902))

### Spectral Mackey functors

The general concept of spectral Mackey functors

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
