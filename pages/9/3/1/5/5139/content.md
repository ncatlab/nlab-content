

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

## Definition

Given a [[stable (infinity,1)-category|stable]] [[symmetric monoidal (infinity,1)-category]] $C$, an **$E_\infty$-algebra** in $C$ is synonymous with a [[commutative monoid in a symmetric monoidal (infinity,1)-category|commutative monoid]] in $C$.
Most often $C$ is the [[(infinity,1)-category of chain complexes]] over a [[field]] or [[commutative ring]], or the [[stable (infinity,1)-category]] of [[spectra]] (see also [[E-infinity ring]]).

In terms of [[operads]], an $E_\infty$-algebra is an [[algebra over an operad]] for an [[E-∞ operad]].


## Realizations

### In chain complexes

$E_\infty$-algebras in [[chain complex|chain complexes]] are equivalent to those in abelian [[simplicial group|simplicial groups]].

For details on this statement see [[monoidal Dold-Kan correspondence]] and [[operadic Dold-Kan correspondence]].

The [[singular cohomology]] $H^*(X,\mathbb{Z})$ of a topological space
is a graded-commutative algebra over the integers, but the the [[singular cohomology|singular cochain]] complex $C^*(X,\mathbb{Z})$ is not: instead, it is an $E_\infty$-algebra.

A concrete construction of an $E_\infty$-algebra structure
on [[singular cochains]], and, more generally,
[[simplicial cochains]] of a [[simplicial set]]
can be found in [McClure and Smith](#MCO).
Their work gives a precise description of the involved __sequence operad__, which is an $E_\infty$-operad,
as well as its action on [[simplicial cochains]],
which involves a generalization of Steenrod's cup-$i$ products.
Recall that the cup-1 product controls the noncommutativity of
the ordinary [[cup product]]:
$$d(x\cup_1 y)=x\cup y-(-1)^{|x|\cdot|y|}y\cup x.$$
It can be defined using a formula similar to the one used
for the [[cup product]], and the higher operations
also have similar nature.

Remarkably, for [[simply connected]] spaces of [[finite type]] this $E_\infty$-algebra knows everything about the [[weak homotopy type]] of $X$.  In fact a stronger statement holds:

+-- {: .un_theorem}
###### Theorem

Finite type [[nilpotent spaces]] $X$ and $Y$ are [[weak equivalence|weakly homotopy equivalent]] if and only if the $E_\infty$-algebras $C^*(X,\mathbb{Z})$ and $C^*(Y,\mathbb{Z})$ are quasi-isomorphic.

=--

This was proved by [Mandell](#Mandell) in 2003.



### In topological spaces


+-- {: .un_theorem}
###### Theorem (May recognition theorem)

A [[connected space]] of the [[homotopy type]] of a [[CW-complex]] with a non-degenerate basepoint that has the [[homotopy type]] of a $k$-fold [[loop space]] for all $k \in \mathbb{N}$ admits the structure of an $E_\infty$-space.

=--


### In simplicial sets


+-- {: .un_theorem}
###### Theorem 


The [[model structure on algebras over an operad]] over [[E-∞ operad]]s in [[Top]] and in [[sSet]] are [[Quillen equivalence|Quillen equivalent]].

=--

This is in [BergerMoerdijk I](#BergerMoerdijkHomotopy), [BergerMoerdijk II](#BergerMoerdijkAlgebras).


### In spectra

An $E_\infty$-algebra in [[spectra]] is an [[E-∞ ring]].



### In $\infty$-stacks

See [[Ek-Algebras]].

### In $(\infty,n)$-categories

See _[[symmetric monoidal (∞,n)-category]]_.

## Related concepts

* [[A-∞ algebra]]

* [[Hopf E-∞ algebra]]

## References

* [[Peter May]], _The geometry of iterated loop spaces_ ([pdf](http://www.math.uchicago.edu/~may/BOOKS/gils.pdf))
{#May}

* {#MCO} [[James E. McClure]], [[Jeffrey H. Smith]], _Multivariable cochain operations and little $n$-cubes__,[arXiv](https://arxiv.org/abs/math/0106024), [Journal of the AMS 16:3 (2003), 681–704](https://doi.org/10.1090/S0894-0347-03-00419-3).

* [[Mike Mandell]], _Cochains and homotopy type_, Publ. Math. IHES (2006) 103: 213&#8211;246.  ([arXiv](https://arxiv.org/abs/math/0311016)) 
{#Mandell}

* [[Martin Markl]], Steve Shnider, [[Jim Stasheff]], _Operads in algebra, topology and physics_, Math. Surveys and Monographs __96__, Amer. Math. Soc. 2002.
{#MarklShniderStasheff}

In the context of [[(infinity,1)-operad]]s $E_\infty$-algebras are discussed in

* [[Jacob Lurie]], _[[Ek-Algebras]]_
{#Lurie}


A systematic study of [[model category]] structures on operads and their algebras is in

* [[Clemens Berger]], [[Ieke Moerdijk]], _Axiomatic homotopy theory for operads_ Comment. Math. Helv. 78 (2003), 805&#8211;831. ([arXiv:math/0206094](http://arxiv.org/abs/math/0206094))
{#BergerMoerdijkHomotopy}


The induced model structures and their properties on [[algebras over operads]] are discussed in

* [[Clemens Berger]], [[Ieke Moerdijk]], _Resolution of coloured operads and rectification of homotopy algebras_ ([arXiv:math/0512576](http://arxiv.org/abs/math/0512576))
{#BergerMoerdijkAlgebras}


[[!redirects E-infinity-algebra]]
[[!redirects E-infinity algebras]]
[[!redirects E-infinity-algebras]]

[[!redirects E-∞ algebra]]
[[!redirects E-∞ algebras]]

[[!redirects E-∞-algebra]]
[[!redirects E-∞-algebras]]

[[!redirects E-infinity monoid]]
[[!redirects E-infinity monoids]]

