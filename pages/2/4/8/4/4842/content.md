
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Knot theory
+-- {: .hide}
[[!include knot theory - contents]]
=--
=--
=--


# Vassiliev knot invariants
* table of contents
{: toc}

## Idea ##

The space of [[knots]] in the [[Euclidean space]] $\mathbb{R}^3$ (or in the [[3-sphere]] $S^3$) is an [[open subset|open]] [[submanifold]] of the [[smooth loop space]].  [[knot invariant|Knot invariants]] are [[locally constant functions]] on this manifold.  The [[complement]] of the space of knots is called the [[discriminant]] and consists of all [[singular knots]].

If we consider those singular knots with only a finite number of double points, we can build a [[cubical complex]] from this data.  The vertices in the complex are labelled by the isotopy classes of knots, and more generally the $n$-cubes by the isotopy classes of singular knots with $n$ double points (and a few other technical pieces of information).  The boundary operator resolves a double crossing either upwards or downwards according to the orientation at the crossing.

A **Vassiliev invariant** is simply a cubical morphism from this complex to an abelian group that vanishes above a certain degree.

## Definition ##

One does not need the language of cubical complexes to _define_ Vassiliev invariants.  Rather, there is a general method whereby a [[knot invariant]] can be extended to all [[singular knots]] with only finitely many double points (and no other singularities) using the [[Vassiliev skein relations]].


+-- {: .num_defn #vinv}
###### Definition

A **Vassiliev invariant** of degree (or order) $\le n$ is a knot invariant whose extension to singular knots (with double points) vanishes on all singular knots with more than $n$ double points.

=--

As is standard, it is of degree $n$ if it is of degree $\le n$ but not $\le n - 1$.  Vassiliev invariants are also called **finite type invariants**.


+-- {: .num_remark}
###### Remark


The degree of Vassiliev invariants defines a filtration on the space of knots (and more particularly, on the [[algebra of knots]]).  Two knots are $n$-equivalent if all the Vassiliev invariants of degree $\le n$ agree on them.  In particular, a knot that is $n$-equivalent to the unknot is said to be $n$-trivial.

=--

## Properties ##

A function which is constant on nonsingular knots may be extended to a Vassiliev invariant of degree 0 by applying the [[Vassiliev skein relations]], and conversely, any Vassiliev invariant of degree 0 must be constant on nonsingular knots.  Likewise, any Vassiliev invariant of degree 1 must be constant on nonsingular knots.

## Chord diagrams and weight systems ##

Any singular knot $f : S^1 \to \mathbb{R}^3$ with $n$ distinct double points $x_1,\dots,x_n \in \mathbb{R}^3$ gives rise to a [[chord diagram]] of order $n$, consisting of the circle $S^1$ with a chord connecting each pair of points $f^{-1}(x_1), \dots, f^{-1}(x_n)$.

The importance of this construction for singular knots comes from the fact that any finite type invariant determines a function on chord diagrams:

+-- {: .un_theorem}
######Theorem 

Let $v$ be a Vassiliev invariant of degree $\le n$.  Then the value of $v$ on a singular knot with $n$ distinct double points depends only on the chord diagram of the knot, and not on the knot itself.

=-- 

Conversely, one can ask which functions on chord diagrams come from finite type invariants.  The answer is that Vassiliev invariants (of degree $\le n$) can essentially be identified with _weight systems_ (of order $n$), which are functions on chord diagrams (of order $n$) satisfying two properties called the "1-term relation" (or "framing independence") and the "4-term relation": see Theorem 1 of [Bar-Natan 95](#BarNatan95) (or Theorem 6.2.13 of [Lando & Zvonkin](#LandoZvonkin)).

## Examples ##

1. The $n$th coefficient of the Conway polynomial is a Vassiliev invariant of order $\le n$.

## Related concepts ## 

* [[knot theory]]
* [[Jones polynomial]]
* [[Kontsevich integral]]
* [[singularity]] 



## References 

### General

The original articles are

* [[Viktor Vassiliev]], _Complements of discriminants of smooth maps: topology and applications_, Amer. Math. Soc. 1992. 

* {#Kontsevich93} [[Maxim Kontsevich]], _Vassiliev's knot invariants_, Advances in Soviet Mathematics, Volume 16, Part 2, 1993 ([pdf](http://pagesperso.ihes.fr/~maxim/TEXTS/VassilievKnot.pdf))


Review:

* {#BarNatan95} [[Dror Bar-Natan]], _On the Vassiliev knot invariants_, Topology Volume 34, Issue 2, April 1995, Pages 423-472 ([web](http://www.math.toronto.edu/~drorbn/papers/OnVassiliev/), <a href="https://doi.org/10.1016/0040-9383(95)93237-2">doi:10.1016/0040-9383(95)93237-2</a>)

* S. Chmutov, S. Duzhin, J. Mostovoy, _Introduction to Vassiliev knot invariants_ ([arxiv/1103.5628](http://arxiv.org/abs/1103.5628))

* {#LandoZvonkin} Sergei K. Lando and Alexander K. Zvonkin, Chapter 6 of: _Graphs on Surfaces and Their Applications_, Springer, 2004.

More literature is listed at

* [[Dror Bar-Natan]], Sergei Duzhin, _[Bibliography of Vassiliev Invariants](http://www.pdmi.ras.ru/~duzhin/VasBib/Long)_

See also

* Mathworld, _[Vassiliev invariant](http://mathworld.wolfram.com/VassilievInvariant.html)_

Concrete computations:

* Jan Kneissler, _On spaces of connected graphs I: Properties of Ladders_, Proc. Internat. Conf. "Knots in Hellas '98", Series on Knots and Everything, vol. 24 (2000), 252-273 ([arXiv:math/0301018](https://arxiv.org/abs/math/0301018))

* Jan Kneissler, _On spaces of connected graphs II: Relations in the algebra Lambda_, Jour. of Knot Theory and its Ramif. vol. 10, no. 5 (2001), 667-674 ([arXiv:math/0301019](https://arxiv.org/abs/math/0301019))

* Jan Kneissler, _On spaces of connected graphs III: The Ladder Filtration_, Jour. of Knot Theory and its Ramif. vol. 10, no. 5 (2001), 675-686 ([arXiv:math/0301020](https://arxiv.org/abs/math/0301020))

* [[Pierre Vogel]], _Algebraic structures on modules of diagrams_, Journal of Pure and Applied Algebra Volume 215, Issue 6, June 2011, Pages 1292-1339 ([pdf](https://webusers.imj-prg.fr/~pierre.vogel/diagrams.pdf))

### Relation to Jones polynomial:

Relation to the [[Jones polynomial]]:

* Joan S. Birman; Xiao-Song Lin, _Knot polynomials and Vassiliev's invariants_,  Inventiones mathematicae (1993) Volume: 111, Issue: 2, page 225-270 ([https://dml:144077](https://eudml.org/doc/144077))

Relation to other polynomial [[knot invariants]]:

* Myeong-Ju Jeong, Chan-Young Park, _Polynomial invariants and Vassiliev invariants_, Geom. Topol. Monogr. 4 (2002) 89-101 ([arxiv:math/0211045](https://arxiv.org/abs/math/0211045))




### As Chern-Simons amplitudes

Discussion of higher order Vassiliev invariants as [[Chern-Simons theory]]-[[correlators]], hence as [[configuration space of points|configuration space]]-[[integrals]] of [[wedge products]] of [[Chern-Simons propagators]] assigned to [[edges]] of [[Feynman diagrams]] in the [[graph complex]]:

* [Kontsevich 93, Section 5](#Kontsevich93)

* Daniel Altschuler, Laurent Freidel, _Vassiliev knot invariants and Chern-Simons perturbation theory to all orders_, Commun. Math. Phys. 187 (1997) 261-287 ([arxiv:q-alg/9603010](https://arxiv.org/abs/q-alg/9603010))


* [[Alberto Cattaneo]], Paolo Cotta-Ramusino, Riccardo Longoni, _Configuration spaces and Vassiliev classes in any dimension_, Algebr. Geom. Topol. 2 (2002) 949-1000 ([arXiv:math/9910139](https://arxiv.org/abs/math/9910139))

* [[Alberto Cattaneo]], Paolo Cotta-Ramusino, Riccardo Longoni, _Algebraic structures on graph cohomology_, Journal of Knot Theory and Its Ramifications, Vol. 14, No. 5 (2005) 627-640 ([arXiv:math/0307218](https://arxiv.org/abs/math/0307218))

Reviewed in:

* {#Volic13} [[Ismar Volić]], Section 4 of: _Configuration space integrals and the topology of knot and link spaces_, [Morfismos, Vol 17, no 2, 2013](https://fdocuments.co/amp/document/morfismos-vol-17-no-2-2013.html) ([arxiv:1310.7224](https://arxiv.org/abs/1310.7224))








category: geometry, topology

[[!redirects Vassiliev knot invariant]]
[[!redirects Vassiliev knot invariants]]


[[!redirects Vassiliev invariants]]

[[!redirects Vassiliev finite type invariants]]
[[!redirects Vassiliev finite type invariant]]
[[!redirects Vassiliev finite-type invariants]]
[[!redirects Vassiliev finite-type invariant]]
[[!redirects finite type invariants]]
[[!redirects finite type invariant]]
[[!redirects finite-type invariants]]
[[!redirects finite-type invariant]]