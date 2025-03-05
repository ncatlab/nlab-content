
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Supergeometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A [[supermanifold]] is a [[space]] locally modeled on [[Cartesian space|Cartesian spaces]] and [[superpoints]].

There are different approaches to the definition and theory of supermanifolds in the literature. The definition 

* [As locally ringed spaces](#AsLocallyRingedSpace)

is popular. The definition 

* [As manifolds over superpoints](#OverSuperpoints)

has been argued to have advantages, see also the references at [[super ∞-groupoid]].


## As locally representable sheaves on super Cartesian spaces

See at _[[geometry of physics -- supergeometry]]_ the section _[Supermanifolds](geometry+of+physics+--+supergeometry#Supermanifolds)_.



## As locally ringed spaces
 {#AsLocallyRingedSpace}

We discuss a description of supermanifolds that goes back to 
([Berezin & Leites 1975](#BerezinLeites75)).

### Definition

+-- {: .num_defn #SupermanifoldLocallyRingedSpace}
###### Definition

A **supermanifold** $X$ of dimension $p|q$ is a
[[ringed space]] $(|X|, O_X)$ where

* the [[topological space]] $|X|$ is [[second countable space]], [[Hausdorff space]],

* $O_X$ is a [[sheaf]] of commutative [[super algebras]] that is locally on small enough open subsets $U \subset |X|$ isomorphic to one of the form $C^\infty(\mathbb{R}^p) \otimes \wedge^\bullet \mathbb{R}^q$.

A [[morphism]] of supermanifolds is a [[homomorphism]] of [[ringed spaces]] (...).

=--

Forgetting the graded part by projecting out the [[nilpotent ideal]] in $O_X$ (i.e. applying the [[bosonic modality]]) yields the underlying ordinary  [[smooth manifold]] $X_{red}$.

One just writes $C^\infty(X)$ for the [[super algebra]] $O_X(X)$ of global sections.

With the obvious morphisms of [[ringed space]] this forms the [[category]] [[SDiff]] of supermanifolds.

### Examples

* [[super Cartesian space]]

  * [[superpoint]]

    * [[odd line]]

+-- {: .num_example }
###### Example

For $E \to X$ a smooth finite-rank [[vector bundle]] the [[manifold]] $X$ equipped with the [[Grassmann algebra]] over $C^\infty(X)$ of the sections  of the dual bundle

$$
  O_X(U) \coloneqq \Gamma (\wedge^\bullet(E^*))
$$

is a supermanifold. This is usually denoted by $\Pi E$.

=--

+-- {: .num_example }
###### Example

In particular, let $\mathbb{R}^{p+q} \to \mathbb{R}^p$ be the trivial rank $q$ [[vector bundle]] on $\mathbb{R}^p$ then one writes

$$
  \mathbb{R}^{p|q} 
    \coloneqq 
  \Pi (\mathbb{R}^{p+q} \to \mathbb{R}^p)
$$

for the corresponding supermanifold.

=--


### Properties
 {#AsLocallyRingedSpacesProperties}

+-- {: .num_theorem #BatchelorTheorem}
###### Theorem
**(Batchelor's theorem)**

Every supermanifold is [[isomorphism|isomorphic]] to one of the form $\Pi E$ where $E$ is an ordinary smooth [[vector bundle]].

=--

([Batchelor 1979](#Batchelor79) reviewed in [Batchelor 1984, §1.13](#Batchelor84); [Rogers 2007, §8.2](#Rogers07), see also [Gawędzki 1977 §3 Thm 1 (p 342)](#Gawędzki77), [Manin 1988, §2 Thm 2 & Cor 7 (pp 188)](#Manin88))



+-- {: .num_remark}
###### Remark

Nevertherless, the category of supermanifolds is far from being [[equivalence of categories|equivalent]] to that of [[vector bundles]]: a morphism of vector bundles translates to a morphism of supermanifolds that is strictly homogeneous in degrees, while a general morphism of supermanifolds need not be of this form.

=--

But we have the following useful characterization of morphisms of supermanifolds:

+-- {: .num_theorem #MorphismsOfSupermanifoldsByAlgebras}
###### Theorem

* There is a [[natural bijection]]

  $$
    SDiff(X,Y) 
   \;\simeq\; 
   SAlgebras\big(C^\infty(Y), C^\infty(X)\big),
  $$

  so the contravariant embedding of supermanifolds into superalgebra is a [[full and faithful functor]].

* Composition with the standard coordinate functions on $\mathbb{R}^{p|q}$ yields an [[isomorphism]]

  $$
    SDiff(X, \mathbb{R}^{p|q})
    \simeq
    \underbrace{
    (C^\infty(X)^{ev} \times \cdots 
    \times C^\infty(X)^{ev})}_{p\; times}
    \times
    \underbrace{
      (C^\infty(X)^{odd} \times \cdots 
      \times C^\infty(X)^{odd})}_{q\; times}
  $$


=--

+-- {: .proof}
###### Proof

The first statement is a direct extension of the classical fact that [[smooth manifolds embed into formal duals of R-algebras]].
=--

## As manifolds modeled on Grassman algebras
 {#ModeledOnGrassmannAlgebra}

We discuss a description of supermanifolds that goes back to 
([DeWitt 92](#DeWitt92)) and ([Rogers 2007](#Rogers07)).

(...)

## As manifolds over the base topos on superpoints
 {#OverSuperpoints}

Let $SuperPoint$ be the [[category]] of [[superpoint|superpoints]]. And $Sh(SuperPoint) = PSh(SuperPoint)$ its [[presheaf topos]].

We discuss a definition of supermanifolds that characterizes them, roughly,  as manifolds over this [[base topos]]. See ([Sachse](#Sachse)) and the references at [[super ∞-groupoid]]. 

See also [this post](http://theoreticalatlas.wordpress.com/2013/07/26/john-huerta-supermanifolds/) at Theoretical Atlas. 


### Definition

+-- {: .num_defn }
###### Definition

Let 

$$
  SuperSet \coloneqq Sh(SuperPoint)
$$

be the [[sheaf topos]] over [[superpoints]]. Let

$$
  \mathbb{R} \in Ring(SuperSet)
$$

be the canonical [[continuum]] [[real line]] under the restricted [[Yoneda embedding]] of supermanifolds and equipped with its canonical internal algebra structure, hence by prop. \ref{MorphismsOfSupermanifoldsByAlgebras} the presheaf of algebras which sends a Grassmann algebra to its even subalgebra, as discussed at [[superalgebra]].

=--

+-- {: .num_defn }
###### Definition

A **superdomain** is an open subfunctor (...) of a [[locally convex vector space|locally convex]] $\mathbb{K}$-module.

=--

This appears as ([Sachse, def. 4.6](#Sachse)). 

We now want to describe supermanifolds as [[manifold|manifolds]] in $SuperSet$ modeled on superdomains.

Write [[SmoothMfd]] for the [[category]] of ordinary [[smooth manifold|smooth manifolds]].

+-- {: .num_defn #SupermanifoldOverSuperpoint}
###### Definition

A _supermanifold_ is a functor $X : SuperPoint^{op} \to SmoothMfd$ equipped with an equivalence class of [supersmooth atlases](#).

A [[morphism]] of supermanifolds is a [[natural transformation]] $f : X \to X'$, such that for each pair of [[chart|charts]] $u : U \to X$ and $u' : U' \to X'$ the [[pullback]]

$$
  \array{
    U \times_{X'} U' &&\stackrel{p'}{\to}&& U'
    \\
    {}^{\mathllap{p_1}}\downarrow & & && \downarrow^{\mathrlap{u'}}
    \\
    U &\stackrel{u}{\to}& X &\stackrel{f}{\to}& X'
  }
$$

can be equipped with the structture of a [Banach superdomain](#) such that $p_1$ and $p_2$ are supersmooth (...)

=--

This appears as ([Sachse, def. 4.13, 4.14](#Sachse)).

### Properties

+-- {: .num_prop}
###### Proposition

The categories of supermanifolds defined as locally ringed spaces, 
def. \ref{SupermanifoldLocallyRingedSpace} and as manifolds over superpoints,
def. \ref{SupermanifoldOverSuperpoint} are 
[[equivalence of categories|equivalent]].

=--

This appears as ([Sachse, theorem 5.1](#Sachse)). See section 5.2 there for a discussion of the relation to the [DeWitt-definition](#ModeledOnGrassmannAlgebra).



## Related concepts

* [[super-scheme]], [[spectral super-scheme]]

* [[integration over supermanifolds]]

* [[super vector bundle]] 

* [[complex supermanifold]], [[super Riemann surface]]

* [[superconnection]]

* [[superdifferential form]]

* [[superalgebra]], [[smooth superalgebra]]

* [[NQ-supermanifold]]

* [[super-orbifold]]


## References

### Via dual superalgebra

Via the [[formal dual|formally dual]] [[superalgebra]] of the super-[[function algebras]] on supermanifolds

* [[Felix A. Berezin]] (edited by [[Alexandre A. Kirillov]]): *Supermanifolds in General*, Ch. 4 in: *Introduction to Superanalysis*, Mathematical Physics and Applied Mathematics **9**, Springer (1987) &lbrack;[doi:10.1007/978-94-017-1963-6_5](https://doi.org/10.1007/978-94-017-1963-6_5)&rbrack; 

* {#Gawędzki77} [[Krzysztof Gawędzki]]: *Supersymmetries -- Mathematics of supergeometry*, Annales de l'I.H.P. **27** 4 (1977) 335-366 &lbrack;[numdam:AIHPA_1977__27_4_335_0](http://www.numdam.org/item/?id=AIHPA_1977__27_4_335_0), [dml:75963](https://eudml.org/doc/75963)&rbrack;



### Via functorial geometry

Discussion from the point of view of [[functorial geometry]]:

* [[Claudio Carmeli]], Lauren Caston, [[Rita Fioresi]], _Mathematical Foundations of Supersymmetry_, EMS Series of Lectures in Mathematics Volume: 15; 2011; 263 pp; ( [ISBN:978-3-03719-097-5](https://bookstore.ams.org/emsserlec-15/), [arXiv:0710.5742](https://arxiv.org/abs/0710.5742))

* {#HohnholdSolzTeichner11} [[Henning Hohnhold]], [[Stephan Stolz]], [[Peter Teichner]]: *Super manifolds: an incomplete survey*, Bulletin of the Manifold Atlas (2011) 1-6 &lbrack;[webpage](http://www.map.mpim-bonn.mpg.de/Super_manifolds:_an_incomplete_survey), [pdf](https://people.mpim-bonn.mpg.de/teichner/Math/ewExternalFiles/Survey-Journal.pdf), [[HST11-SupermanifoldsIncomplete.pdf:file]]&rbrack;

* [[Henning Hohnhold]], [[Matthias Kreck]], [[Stephan Stolz]], [[Peter Teichner]], Sections 2-3 of: _Differential forms and 0-dimensional supersymmetric field theories_, Quantum Topology **2** 1 (2011) 1–41 &lbrack;[doi:10.4171/QT/12](http://dx.doi.org/10.4171/QT/12), [pdf](https://people.mpim-bonn.mpg.de/teichner/Math/ewExternalFiles/DimZero.pdf)&rbrack;


### As locally ringed spaces

* {#BerezinLeites75} [[Felix A. Berezin]], [[Dimitry A. Leites]]: _Supermanifolds_, (Russian) Dokl. Akad. Nauk SSSR __224__ 3 (1975) 505-508; English transl.: Soviet Math. Dokl. __16__ 5 (1975) 1218-1222 &lbrack;[mathnet:dan39282](https://www.mathnet.ru/eng/dan39282)&rbrack;

* {#Batchelor79} [[Marjorie Batchelor]], *The structure of supermanifolds*, Trans. Amer. Math. Soc. **253** (1979) 329-338 &lbrack;[doi:10.1090/S0002-9947-1979-0536951-0](https://doi.org/10.1090/S0002-9947-1979-0536951-0)&rbrack;

* {#Leites80} [[Dimitry A. Leites]], *Introduction to the Theory of Supermanifolds*, Russ. Math. Surv. **35** 1 (1980) &lbrack;[doi:10.1070/RM1980v035n01ABEH001545](https://doi.org/10.1070/RM1980v035n01ABEH001545), [MathNet](https://www.mathnet.ru/php/archive.phtml?wshow=paper&jrnid=rm&paperid=3160),  [iop](https://iopscience.iop.org/article/10.1070/RM1980v035n01ABEH001545), [pdf](https://www.mathnet.ru/links/200982577ff2b02bc93b2a05da9ce149/rm3160_eng.pdf)&rbrack;

* {#Batchelor84} [[Marjorie Batchelor]], *Graded Manifolds and Supermanifolds* in: *Mathematical Aspects of Superspace*, NATO ASI Series **132**, Springer (1984) 91-134 &lbrack;[doi:10.1007/978-94-009-6446-4_4](https://doi.org/10.1007/978-94-009-6446-4_4)&rbrack;

* {#Manin88} [[Yuri Manin]], §4.1 in: *[[Gauge Field Theory and Complex Geometry]]*, Grundlehren der Mathematischen Wissenschaften **289**, Springer (1988) &lbrack;[doi:10.1007/978-3-662-07386-5](https://doi.org/10.1007/978-3-662-07386-5)&rbrack;

* I. L. Buchbinder, S. M. Kuzenko, *Ideas and methods of supersymmetry and supergravity; or A walk through superspace* CRC Press (1998) &lbrack;[ISBN:10.1201/9780367802530](https://library.oapen.org/handle/20.500.12657/50874)&rbrack;

* {#DeligneMorgan99} [[Pierre Deligne]], [[John Morgan]], Ch 2 in: _Notes on Supersymmetry (following [[Joseph Bernstein]])_, in: *[[Quantum Fields and Strings]], A course for mathematicians*, **1**, Amer. Math. Soc. Providence (1999) 41-97 &lbrack;[ISBN:978-0-8218-2014-8](https://bookstore.ams.org/qft-1-2-s), [web version](http://www.math.ias.edu/qft), [[DeligneMorgan-NotesOnSusy.pdf:file]]&rbrack;

* {#Mirković04} [[Ivan Mirković]], Sec 2 in: *Notes on Super Math*, in *[Quantum Field Theory Seminar](https://people.math.umass.edu/~mirkovic/0.SEMINARS/1.QFT/Fall.04.html)*, lecture notes (2004)  &lbrack;[pdf](https://people.math.umass.edu/~mirkovic/0.SEMINARS/1.QFT/1.SuperMath/8.pdf), [[Mirkovic-NotesOnSupermathematics.pdf:file]]&rbrack;

* Andrew James Bruce: *A First Look at Supersymmetry* &lbrack;[arXiv:2412.07799](https://arxiv.org/abs/2412.07799)&rbrack;
  > (exposition)


A more general variant of this in the spirit of [[locally algebra-ed topos|locally algebra-ed toposes]]:

* Alexander Alldridge, _A convenient category of supermanifolds_ ([arXiv:1109.3161](http://arxiv.org/abs/1109.3161))



### As manifolds over superpoints
 {#ReferencesOverSuperpoints}

The observation that the study of super-structures in mathematics is usefully regarded as taking place over the [[base topos]] on the [[site]] of [[super points]] has been made around 1984 in

* [[Albert Schwarz]], _On the definition of superspace_, Teoret. Mat. Fiz. (1984)  Volume 60,  Number 1, Pages 37&#8211;42, ([russian original pdf](http://www.mathnet.ru/links/b12306f831b8c37d32d5ba8511d60c93/tmf5111.pdf))

* [[Alexander Voronov]], _Maps of supermanifolds_ , Teoret. Mat. Fiz. (1984)  Volume 60,  Number 1, Pages 43&#8211;48

and in 

* V. Molotkov., _Infinite-dimensional $\mathbb{Z}_2^k$-supermanifolds_ , ICTP
preprints, IC/84/183, 1984.


A summary/review is in the appendix of

* {#KonechnySchwarz98} Anatoly Konechny, [[Albert Schwarz]], 

  _On $(k \oplus l|q)$-dimensional supermanifolds_, in: [[Julius Wess]], V. Akulov (eds.) _Supersymmetry and Quantum Field Theory_ (D. Volkov memorial volume) Lecture Notes in Physics, 509, Springer 1998 ([arXiv:hep-th/9706003](http://arxiv.org/abs/hep-th/9706003))

  Anatoly Konechny, [[Albert Schwarz]], _Theory of $(k \oplus l|q)$-dimensional supermanifolds_, Sel. math., New ser. 6 (2000) 471 - 486 ([doi:10.1007/PL00001396](https://doi.org/10.1007/PL00001396))
  

* [[Albert Schwarz]], I. Shapiro, _Supergeometry and Arithmetic Geometry_ ([arXiv:hep-th/0605119](http://arxiv.org/abs/hep-th/0605119))

A review with more emphasis on the relevant [[category theory]]/[[topos theory]] is in 

* {#Sachse} [[Christoph Sachse]], _A Categorical Formulation of Superalgebra and Supergeometry_ ([arXiv:0802.4067](http://arxiv.org/abs/0802.4067))


The site of formal duals not just to [[Grassmann algebras]] but to all super-[[infinitesimally thickened points]] is discussed in ([Konechny-Schwarz](#KonechnySchwarz)) above and also in

* L. Balduzzi, C. Carmeli, R. Fioresi, _The local functors of points of Supermanifolds_, Expositiones Mathematicae Volume 28, Issue 3, 2010, Pages 201-217 ([doi:10.1016/j.exmath.2009.09.005](https://doi.org/10.1016/j.exmath.2009.09.005), [arXiv:0908.1872](http://arxiv.org/abs/0908.1872))

### As manifolds modelled on Grassmann algebras

* Katsumi Yagi: *Super manifolds*, Osaka J. Math. **25** 4 (1988) 909-932 &lbrack;[euclid:ojm/1200781174](https://projecteuclid.org/journals/osaka-journal-of-mathematiacs/volume-25/issue-4/Super-manifolds/ojm/1200781174.full)&rbrack;

* {#DeWitt92} [[Bryce DeWitt]], *Supermanifolds*, Monographs on Mathematical Physics, Cambridge University Press (1984, 1992) &lbrack;[doi:10.1017/CBO9780511564000](https://doi.org/10.1017/CBO9780511564000)&rbrack;  

* {#Rogers07} [[Alice Rogers]], *Supermanifolds: Theory and Applications*, World Scientific (2007) &lbrack;[doi:10.1142/1878](https://doi.org/10.1142/1878)&rbrack;

  > ([Rogers 2007, Ch. 1](#Rogers07) that the smooth-manifold-of-(infinite-dimensional)-Grassmann-algebras approach (the "concrete approach") is identical to the sheaf-of-ringed-spaces approach (the "algebro-geometric" approach) and that this equivalence is shown in Chapter 8. DeWitt seems unsure of this, but is writing more than 20 years earlier, before the ringed-space approach has been fully developed.)
 
* [[Alice Rogers]], *Aspects of the Geometrical Approach to Supermanifolds*, in: *Mathematical Aspects of Superspace*, NATO ASI Series **132**, Springer (1984) 135-148 &lbrack;[doi:10.1007/978-94-009-6446-4_5](https://doi.org/10.1007/978-94-009-6446-4_5)&rbrack;



### Other


Discussion with an eye towards [[integration over supermanifolds]]:

* [[Edward Witten]], _Notes On Supermanifolds and Integration_ ([arXiv:1209.2199](http://arxiv.org/abs/1209.2199))

Discussion of global properties:

* [[Louis Crane]], [[Jeffrey M. Rabin]], _Global properties of supermanifolds_, Comm. Math. Phys. **100** 1 (1985) 141-160 &lbrack;[doi:10.1007/BF01212690](https://doi.org/10.1007/BF01212690), [euclid:cmp/1103943340](http://projecteuclid.org/euclid.cmp/1103943340)&rbrack;

See also:

* [[Yuri Manin]], _Topics in noncommutative geometry_, Princeton Univ. Press 1991. 

* [[Pierre Deligne]], P. Etingof, [[Daniel Freed]], L. Jeffrey, D. Kazhdan, J. Morgan, D.R. Morrison and [[Edward Witten]] (eds.)  _[[Quantum Fields and Strings]], A course for mathematicians_, 2 vols. Amer. Math. Soc. Providence 1999. ([web version](http://www.math.ias.edu/qft))

* {#Varadarajan04} [[Veeravalli Varadarajan]], *The Concept of a Supermanifold* and *Elementary Theory of Supermanifolds*, Chapters 2 and 4 in: _[[Supersymmetry for mathematicians]]: An introduction_, Courant Lecture Notes in Mathematics **11**, American Mathematical Society (2004) &lbrack;[doi:10.1090/cln/011](http://dx.doi.org/10.1090/cln/011)&rbrack;

* [[Alberto S. Cattaneo]], [[Florian Schaetz]], _Introduction to supergeometry_ &lbrack;[arxiv/1011.3401](http://arxiv.org/abs/1011.3401)&rbrack;

There are many books in [[physics]] on [[supersymmetry]] (most well known is by Wess and Barger from 1992), but they emphasise more on the [[supersymmetry algebra|supersymmetries]] rather than on (the superspace and) _supermanifolds_. They should therefore rather be listed under *[[supersymmetry]]*.  

See also [pdf](http://www.math.uni-hamburg.de/home/sachse/handoutbatchelor.pdf)




[[!include supergeometry of fermion fields -- references]]





[[!redirects supermanifolds]]


[[!redirects super manifold]]
[[!redirects super manifolds]]

[[!redirects super-manifold]]
[[!redirects super-manifolds]]

[[!redirects Batchelor's theorem]]

