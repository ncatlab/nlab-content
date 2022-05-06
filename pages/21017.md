
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
#### Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

### Double line notation

What is called _'t Hooft double line notation_ (following ['t Hooft 74](#tHooft74)) is the observation that for the [[fundamental representations]] $V$ of [[semisimple Lie algebras]] $\mathfrak{g}$. the [[Lie algebra weight system|Lie algebra weight]] of a $\mathfrak{g}$-[[Yang-Mills theory]] [[Feynman diagram]] with internal/[[virtual particle|virtual]] [[gluon]] lines is equivalent to one without any [[virtual particle|virtual]] [[gluon]]-lines, obtained by:

{#JacobiIdentity} 1) using the [[Jacobi identity]] to replace all internal gluon vertices by ([[linear combinations]] of) quark-gluon vertices

<center>
<img src="https://ncatlab.org/nlab/files/QuarkGluonJacobiIdentity.jpg" width="580">
</center>


{#MetricContractionOfFundamentalLieAction} 2)  replacing any remaining internal gluon line together with the [[quark]] [[interaction]] [[vertices]] at its ends (equivalently: an [[M2-brane 3-algebra]] [[tensor]])
by (a [[linear combination]] of) _double_ [[quark]]-lines , according to the following rules:

<center>
<img src="https://ncatlab.org/nlab/files/MetricActionContraction.jpg" width="600">
</center>

Here we are using the [[string diagram]]/[[Penrose notation]] from _[[metric Lie representations]]_; graphics from [[schreiber:Differential Cohomotopy implies intersecting brane observables|Sati-Schreiber 19c]].

{#Attribution} **Attribution.** In ['t Hooft 74](#tHooft74) this is observed for the [[unitary Lie algebra]] $\mathfrak{g} = \mathfrak{u}(N)$, in which case only the first summand of the expressions [above](#MetricContractionOfFundamentalLieAction) appears. The generalization to arbitrary [[semisimple Lie algebras]] is observed in [Cvitanović 76, Fig. 14](#Cvitanovic76), reviewed for [[special unitary Lie algebra|su(N)]], [[special orthogonal Lie algebra|so(N)]] and [[symplectic Lie algebra|sp(N)]] in [Cvitanović 08 (9.57), (10.13) and (12.9)](#Cvitanovic08) and for [[special linear Lie algebra|sl(N)]] and [[special orthogonal Lie algebra|so(N)]] in [Chmutov-Duzhin-Mostovoy 11, 6.2.6](#ChmutovDuzhinMostovoy11).
For the case $\mathfrak{so}(N)$ see also 
[Bar-Natan 95, Section 6.3](#BarNatan95) (with an eye towards [[Vassiliev knot invariants]]) and
[Cicuta 82](#Cicuta82), [Ita-Nieder-Oz 02, Figure 3](#ItaNiederOz02), [McGreevy-Swingle 08, Figure 10](#McGreevySwingle08) (with more discussion of the [[large N limit]]).

### Surface notation

Furthermore, one may regard the resulting double-line diagrams as a [[ribbon graph]] thickening of the original [[Feynman diagrams]], and  thus as [[surfaces]] [[manifold with boundary|with boundary]] and with markings on the [[boundary]].

In the case $\mathfrak{g} = \mathfrak{so}(N)$ this means that a single [[virtual particle|virtual]] [[gluon]] line is represented by the [[formal linear combination]] of a strip (marked [[disk]] and a twisted strip:

<center>
<img src="https://ncatlab.org/nlab/files/tHooftDoubleLineToSurfaces.jpg" width="600">
</center>

Using this on the reduction of internal gluon vertices by the [[Jacobi identity]] as [above](#JacobiIdentity) one finds that a single [[gluon]] vertex turns into the following linear combination of marked surfaces:

<center>
<img src="https://ncatlab.org/nlab/files/tHooftSurfacesForGluonVertex.jpg" width="700">
</center>

This construction respects the [[STU relation]] on [[Jacobi diagrams]] ([Bar-Natan 95, Theorem 10](#BarNatan95)):


<center>
<img src="https://ncatlab.org/nlab/files/AtHooftConstrictionII.jpg" width="650">
</center>

> graphics from [[schreiber:Differential Cohomotopy implies intersecting brane observables|Sati-Schreiber 19c]]

## Applications

### Large $N$ Limit and holography

One upshot of this double-line reformulation is that it makes the dependence of the [[Feynman amplitude]] on the [[natural number]] $N$ fully explicit, since a double line diagram simply contributes one factor of $N$ for each closed [[quark]] line (this being the [[trace]] over the [[fundamental representation]]).

In fact, by regarding the resulting double-line diagrams as a [[ribbon graph]] thickenings the original [[Feynman diagrams]], and regarding these [[ribbon graphs]] in turn as [[surfaces]], the $N$-dependence is proportional to the [[genus of a surface|genus]] of these surfaces.


One finds this way that in the _[[large N limit]]_, i.e. the [[limit of a sequence|limit]] where $N \to \infty$, precisely only the [[planar graphs]] contribute to the [[Yang-Mills theory]] [[Feynman amplitudes]], corresponding to  [[surfaces]] of [[genus]] 0 (i.e. [[tree level]] [[string scattering amplitudes]] see at _[[planar limit]]_ for more on this), while $1/N$-corrections correspond to higher [[worldsheet]] [[topology]].

Last not least, these [[surfaces]] have the interpretation of [[open string]] [[worldsheets]] of a [[string theory]] which is "[[duality in string theory|dual]]" to the original ([[super Yang-Mills theory|super]]) in the sense made precise by [[AdS-CFT duality]].


### Classification of weight systems

Later the same double line technique was used (without any reference to the earlier physics articles(?)) in [Bar-Natan 95, Section 6](#BarNatan95) for discussion of the classification of [[Lie algebra weight systems]] and [[stringy weight systems]] with an eye towards discussion of [[Vassiliev knot invariants]].

## References

The original article is:

* {#tHooft74} [[Gerard 't Hooft]], _A Planar Diagram Theory for Strong Interactions_, Nucl. Phys. B72 (1974) 461 ([spire:80491](http://inspirehep.net/record/80491), <a href="https://doi.org/10.1016/0550-3213(74)90154-0">doi:10.1016/0550-3213(74)90154-0</a>)

reviewed in

* [[Gerard 't Hooft]], _Large $N$_, workshop lecture ([hep-th/0204069](http://arxiv.org/abs/hep-th/0204069))

* Markus Gross, _Large $N$_, 2006 ([[GrossLargeN.pdf:file]])


Generalization to arbitrary [[semisimple Lie algebras]] ([[semisimple Lie groups]]) is due to:

* {#Cvitanovic76} [[Predrag Cvitanović]], _Group theory for Feynman diagrams in non-Abelian gauge theories_, Phys. Rev. D14 (1976) 1536-1553 ([doi:10.1103/PhysRevD.14.1536](https://doi.org/10.1103/PhysRevD.14.1536), [spire:108133](http://inspirehep.net/record/108133), [[CvitanovicWeights76.pdf:file]])

with a textbook account in

* {#Cvitanovic08} [[Predrag Cvitanović]], _Group Theory: Birdtracks, Lie's, and Exceptional Groups_, Princeton University Press July 2008 ([PUP](https://press.princeton.edu/books/paperback/9780691202983/group-theory), [birdtracks.eu](http://birdtracks.eu/), [pdf](http://www.birdtracks.eu/version9.0/GroupTheory.pdf))

Discussion in the context of [[Vassiliev invariants]] and the abstract classification of [[Lie algebra weight systems]] and [[stringy weight systems]]:

* {#BarNatan95} [[Dror Bar-Natan]], Section 6 of: _On the Vassiliev knot invariants_, Topology Volume 34, Issue 2, April 1995, Pages 423-472 (<a href="https://doi.org/10.1016/0040-9383(95)93237-2">doi:10.1016/0040-9383(95)93237-2</a>, [pdf](https://www.math.toronto.edu/drorbn/papers/OnVassiliev/OnVassiliev.pdf))

of which a textbook account is in

* {#ChmutovDuzhinMostovoy11} [[Sergei Chmutov]], [[Sergei Duzhin]], [[Jacob Mostovoy]], _Introduction to Vassiliev knot invariants_, Cambridge University Press, 2012 ([arxiv:1103.5628](http://arxiv.org/abs/1103.5628), [doi:10.1017/CBO9781139107846](https://doi.org/10.1017/CBO9781139107846))


Further discussion of the case of $\mathfrak{so}(N)$ in the context of the [[large N limit]]:

* {#Cicuta82} G.M. Cicuta, _Topological Expansion for $SO(N)$ and $Sp(2n)$ Gauge Theories_, Lett. Nuovo Cim. 35 (1982) 87 ([spire:177713](http://inspirehep.net/record/177713), [doi:10.1007/BF02754653](https://doi.org/10.1007/BF02754653))

* {#ItaNiederOz02} Harald Ita, Harald Nieder, [[Yaron Oz]], _Perturbative Computation of Glueball Superpotentials for $SO(N)$ and $USp(N)$_, JHEP 0301:018, 2003 ([arXiv:hep-th/0211261](https://arxiv.org/abs/hep-th/0211261))

* {#McGreevySwingle08} McGreevy, Swingle, _Large $N$ counting_, 2008 ([[GreevySwingle.pdf:file]])


