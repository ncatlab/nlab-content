
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
([BerezinLeites](BerezinLeites)).

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
  O_X(U) := \Gamma (\wedge^\bullet(E^*))
$$

is a supermanifold. This is usually denoted by $\Pi E$.

=--

+-- {: .num_example }
###### Example

In particular, let $\mathbb{R}^{p+q} \to \mathbb{R}^p$ be the trivial rank $q$ [[vector bundle]] on $\mathbb{R}^p$ then one writes

$$
  \mathbb{R}^{p|q} := \Pi (\mathbb{R}^{p+q} \to \mathbb{R}^p)
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

+-- {: .num_remark}
###### Remark

Nevertherless, the category of supermanifolds is far from being [[equivalence of categories|equivalent]] to that of [[vector bundles]]: a morphism of vector bundles translates to a morphism of supermanifolds that is strictly homogeneous in degrees, while a general morphism of supermanifolds need not be of this form.

=--

But we have the following useful characterization of morphisms of supermanifolds:

+-- {: .num_theorem #MorphismsOfSupermanifoldsByAlgebras}
###### Theorem

* There is a [[natural bijection]]

  $$
    SDiff(X,Y) \simeq SAlgebras(C^\infty(Y), C^\infty(X)),
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
([DeWitt 92](#DeWitt92)) and ([Rogers](#Rogers)).

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
  SuperSet := Sh(SuperPoint)
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


### Via functorial geometry

Discussion from the point of view of [[functorial geometry]]:

* [[Claudio Carmeli]], Lauren Caston, [[Rita Fioresi]], _Mathematical Foundations of Supersymmetry_, EMS Series of Lectures in Mathematics Volume: 15; 2011; 263 pp; ( [ISBN:978-3-03719-097-5](https://bookstore.ams.org/emsserlec-15/), [arXiv:0710.5742](https://arxiv.org/abs/0710.5742))

* {#HohnholdSolzTeichner11} [[Henning Hohnhold]], [[Stephan Stolz]], [[Peter Teichner]], _Super manifolds: an incomplete survey_, Bulletin of the Manifold Atlas (2011) 1&#8211;6 ([pdf](https://people.mpim-bonn.mpg.de/teichner/Math/ewExternalFiles/Survey-Journal.pdf))

* [[Henning Hohnhold]], [[Matthias Kreck]], [[Stephan Stolz]], [[Peter Teichner]], Sections 2-3 of: _Differential forms and 0-dimensional supersymmetric field theories_, Quantum Topology Volume 2, Issue 1 (2011) pp. 1–41 ([doi:10.4171/QT/12](http://dx.doi.org/10.4171/QT/12))


### As locally ringed spaces

* {#BerezinLeites} [[Felix Berezin]], D. A. Le&#301;tes, _Supermanifolds_, (Russian) Dokl. Akad. Nauk SSSR __224__ (1975), no. 3, 505--508; English transl.: Soviet Math. Dokl. __16__ (1975), no. 5, 1218--1222 (1976).
 

* I. L. Buchbinder, S. M. Kuzenko, _Ideas and methods of supersymmetry and supergravity; or A walk through superspace_

A more general variant of this in the spirit of [[locally algebra-ed topos|locally algebra-ed toposes]] is in

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

* {#DeWitt92} [[Bryce DeWitt]], _Supermanifolds_, Cambridge Monographs on Mathematical Physics, 1984
  

* {#Rogers} [[Alice Rogers]], Supermanifolds: Theory and Applications, World Scientific, (2007) 

Alice Rogers claims, in Chapter 1, that the smooth-manifold-of-(infinite-dimensional)-Grassmann-algebras approach (the "concrete approach") is identical to the sheaf-of-ringed-spaces approach (the "algebro-geometric" approach) and that this equivalence is shown in Chapter 8. DeWitt seems unsure of this, but is writing more than 20 years earlier, before the ringed-space approach has been fully developed.
 

### Other

Discussion with an eye towards [[supergravity]] is in 

* {#CastellaniDAuriaFre} [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fré]], section II.2.4 of _[[Supergravity and Superstrings - A Geometric Perspective]]_, World Scientific (1991)

Discussion with an eye on [[integration over supermanifolds]] is in

* [[Edward Witten]], _Notes On Supermanifolds and Integration_ ([arXiv:1209.2199](http://arxiv.org/abs/1209.2199))

Global properties are discussed in

* [[Louis Crane]], Jeffrey M. Rabin, _Global properties of supermanifolds_, Comm. Math. Phys. Volume 100, Number 1 (1985), 141-160. ([Euclid](http://projecteuclid.org/euclid.cmp/1103943340))

See also:

* [[Yuri Manin]], _Topics in noncommutative geometry_, Princeton Univ. Press 1991. 

* [[Pierre Deligne]], P. Etingof, [[Daniel Freed]], L. Jeffrey, D. Kazhdan, J. Morgan, D.R. Morrison and [[Edward Witten]] (eds.)  _[[Quantum Fields and Strings]], A course for mathematicians_, 2 vols. Amer. Math. Soc. Providence 1999. ([web version](http://www.math.ias.edu/qft))

* V. S. Varadarajan, _Supersymmetry for mathematicians: an introduction_, AMS and Courant Institute, 2004.

* [[Alberto S. Cattaneo]], Florian Schaetz, _Introduction to supergeometry_, [arxiv/1011.3401](http://arxiv.org/abs/1011.3401)

There are many books in [[physics]] on [[supersymmetry]] (most well known is by Wess and Barger from 1992), but they emphasise more on the [[supersymmetry algebra|supersymmetries]] rather than on (the superspace and) _supermanifolds_. They should therefore rather be listed under entry [[supersymmetry]].  

See also [pdf](http://www.math.uni-hamburg.de/home/sachse/handoutbatchelor.pdf)

[[!redirects supermanifolds]]


[[!redirects super manifold]]
[[!redirects super manifolds]]

[[!redirects super-manifold]]
[[!redirects super-manifolds]]

