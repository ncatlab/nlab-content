

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topological physics
+--{: .hide}
[[!include topological physics -- contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Anyon braiding
 {#Idea}

In [[quantum physics]], *braid group statistics* or *anyon statistics* refers to an exotic phenomenon where the [[braiding]] of the [[worldlines]] of certain effective [[particles]] ("anyons") in an effectively 2+1-dimensional [[spacetime]] has the effect of transforming the [[quantum state]] of the total [[quantum system]] by [[unitary operators]] which constitute a [[linear representation]] of the [[braid group]] -- a *[[braid representation]]*.

Often this is motivated as a generalization of the [[boson]]- or [[fermion]]-"statistics" which enters the *[[spin-statistics theorem]]*, see [below](#AsGeneralizedBosonFermionStatistics). But in reality this effect is often encountered not for fundamental [[particles]]/quanta, but for *[[soliton|solitonic]]$\;$[[defects]]* such as [[vortices]], see [further below](#AsBraidingOfDefects).

The concept of anyons is particularly well motivated in [[solid state physics]], where effectively 2-dimensional [[quantum materials]] are common place (eg. [[graphene]]) or where particles may otherwise be constrained to move in a [[plane]], such as in the [[quantum Hall effect]]. There is a multitude of *[[model (in theoretical physics)|models]]* in [[condensed matter theory]] (mostly [[lattice models]], such as [[string-net models]]) which *theoretically* realize anyon braid group statistics, and there are some first [[experiment|experimental]] indications of anyonic phenomena in actual materials (see the references under *[Experimental Realization](#ExperimentalRealization)*) below.

Specifically, in the context of [[topological phases of matter]], the (potential) presence of anyons has come to be known as the case of *[[topological order]]*, see there for more. 

Besides general curiosity, much of the interest in anyonic braid group statistics lies in the fact that these [[braid representations]] are imagined to potentially serve as [[quantum gates]] in [[topological quantum computers]]. See there for more.






### As generalized boson/fermion statistics?
 {#AsGeneralizedBosonFermionStatistics}

In [[quantum field theory]], one speaks of the "statistics" of a [[particle]] species when referring to the [[linear representation]] that $n$-particle [[wavefunctions]] form under the the [[symmetric group]] $Sym(n)$ which [[permutation|permutes]] the $n$ particles.

While there is a rich [[representation theory of the symmetric group]],
the [[spin-statistics theorem]] says, when it applies, that for *[[field (physics)|field]] quanta* only the simplest two possibilities may occur:

* [[bosons]] (such as [[photons]]) transform under the [[trivial representation]] of $Sym(n)$,

* [[fermions]] (such as [[electrons]]) transform under the [[sign representation]] of $Sym(n)$.

  (see also at *[[Slater determinant]]*)

Now, the [[braid group]] on $n$ strands covers the symmetric group

$$
  Br(n)
  \twoheadrightarrow
  Sym(n)
$$

which allows one to regard any [[linear representation]] of the symmetric group also as a particular [[braid group representation]]. But by its definition, the [[braid group]] may be understood as the group of [[isotopy]]-classes of [[disjoint union|disjoint]] [[timelike]] [[worldlines]] in an effectively 2+1 dimensional [[spacetime]], with the group operation being [[concatenation]] of worldlines.

In this sense, one may imagine that *any* [[braid group representations]] may generalize the boson/fermion statistics in 2+1 dimensions. Texts typically suggest that this applies to *[[quasiparticle|quasiparticles]]*. 

The term *anyon* is a pun on this state of affairs that *any* statistics "in between" boson- and fermion-statistics may be allowed.

On the other hand, anyonic braiding is conceptually different from boson/fermion statistics -- if it were on the same footing then the [[spin-statistics theorem]] would *rule out* anyonic braiding. This is acknowledged by [Chen, Wilczek, Witten & Halperin 1989, p. 352](#ChenWilczekWittenHalperin89) (cf. also [Wilczek 1990, §I.2, pp. 1](#Wilczek90)):

> Once the [[permutation group]] is replaced by the [[braid group]], the simple construction of passing from the solution to the one-particle problems to the solution of many-particle problems, familiar from the free bosons and free fermions, does not work anymore. 



### As braiding of defects
 {#AsBraidingOfDefects}

In contrast to the popular motivation [above](#AsGeneralizedBosonFermionStatistics), many (most?) incarnations of the concept of anyons are [[non-perturbative effect|non-perturbative]] [[soliton|solitonic]] [[defects]] (of [[codimension]]=2), akin to *[[vortices]]* in fluids:

> *Anyonic particles are best viewed as a kind of topological defects that reveal non-trivial properties of the ground state.* $[$[Kitaev 2006, p. 4](#Kitaev06)$]$

>  *Anyons can arise in two ways: as localised excitations of an interacting
quantum Hamiltonian or as defects in an ordered system.*  $[$[Das Sarma, Freedman & Nayak 2015, p. 1](topological+quantum+computation#DasSarmaFreedmanNayak15)$]$

(Compare also the original discussions in [Goldin, Menikoff & Sharp 1981, §III](#GoldinMenikoffSharp81), [Wilczek 1982](#Wilczek82) & [Wilczek 1990, p. 5](#Wilczek90), which offer a quantum particle "[[bound state|bound]]" to a classical & infinite [[solenoid]] -- hence a 2d [[magnetic monopole]] [[defect]] -- as a decent model for an anyon.)

But [[defects]] are a kind of [[boundary conditions]], hence *external parameters* or *[[background fields]]* for the actual [[quantum field]]. 

Concretely, a widely appreciated proposal ([Moore & Read 1991](#MooreRead91), [Read & Rezayi 9199](#ReadRezayi99)) identifies anyonic ground state [[wavefunctions]] with [[conformal blocks]] of a [[2d CFT]] -- [[AdS3-CFT2 and CS-WZW correspondence|hence]] with [[Chern-Simons theory]] [[quantum states|states]] -- with prescribed poles at the location of the anyons.

Now the [[adiabatic theorem]] says that the sufficiently slow motion of such external parameters transforms the quantum [[ground state]] by [[unitary operators]] ("[[Berry phases]]"). This suggests that:

\begin{definition}\label{DefectBraiding}
**(adiabatic defect braiding)**
\linebreak
*Anyon braiding statistics is the [[braid group representation]] on a quantum [[ground state]] induced by [[adiabatic theorem|adiabatic]] [[braiding]] of [[TQFT|topological]] [[codimension]]=2 [[defects]] in their [[configuration space of points|configuration space]].*

Here 

1. for point-defects the "configuration space" is the [[configuration space of points]] in a [[surface]] (as touched upon already in [Leinaas & Myrheim 1977, pp. 22](#LeinaasMyrheim77), albeit briefly/vaguely), such as in the [[plane]], in which case its fundamental group is the [[braid group]];

1. "topological" is meant as in [[topological quantum field theory]]: The induced [[adiabatic theorem|adiabatic]] [[unitary transformation]] is demanded/assumed to depend only on the [[isotopy]]-class of the defect-[[worldlines]], hence only on the underlying [[braid group|braid]]-pattern.

\end{definition}



This notion of anyon "statistics" is at least tacitly implicit in much of the literature on anyons in [[topological quantum computation]], such as in the popular graphics depicting anyon [[worldlines]] as the [[Wilson lines]] in [[Chern-Simons theory]]. (see the graphics [below](#BraidingOfNodalPointsInMomentumSpace)).

Indeed, the effects of [[adiabatic theorem|adiabatic]] braiding of [[defects]] in [[quantum materials]] has been understood and discussed before and in parallel to the term "anyon" becoming established: [Mermin 1979](#Mermin79), [Lo & Preskill 1993](#LoPreskill93).

A concrete realistic example of defect anyons are [[vortex]] anyons see [below](#VortexAnyons).
But the notion of codimension=2 defects subsumes situations that are quite different from the [[quasiparticle]]-excitations imagined in traditional texts on anyons, such as:

* [anyonic band nodes](#AnyonicBandNodes)

* [defect branes](#DefectBranes).


### As a "fictitious" Aharonov-Bohm effect
 {#AsAFictitiousAharonovBohmEffect}

A concrete model for (defect) anyons was proposed in 
[Chen, Wilczek, Witten & Halperin 1989](#ChenWilczekWittenHalperin89):

The model there regards anyons as *a priori* [[free field|free]] [[fermions]], but equipped now with a non-local mutual [[interaction]] via a "fictitious gauge field" ([CWWH89, §2](#ChenWilczekWittenHalperin89)): 

Each of the particles is modeled as the singular source of a [[flat connection|flat]] [[circle bundle with connection|circle connection]] ([[vector potential]] with vanishing [[field strength]]), which hence exerts no [[Lorentz force]] but has the effect that globally each particle is subject to the same [[Aharonov-Bohm effect]] as would be caused by a tuple of infinite [[solenoids]] piercing through each of the particle's positions.

For emphases, from [CWWH89, p. 359](#ChenWilczekWittenHalperin89):

> Here the particles are to be regarded (in the absence of 
interactions) as fermions; the interaction then makes them anyons with statistical 
parameter ($\theta = \pi(1 - 1/ n$).

This construction has been advertized in several early reviews (e.g. [Wilczek 1990, §I.3](#Wilczek90) but seems not to have been developed since.



#### Vortex anyons
 {#VortexAnyons}


Specifically, *[[vortex]] anyons* are realized in [[Bose-Einstein condensates]] ([MPSS19](#MPSS19), following [PFCZ01](#PFCZ01)) and in (other) [[superfluids]] ([MMN21](#MMN21)). A more theoretical but instructive [[lattice model]] of vortex anyons is analyzed in detail in [Kitaev 2006](#Kitaev06).

Much attention in current efforts towards realizing [[topological quantum computation]] is being paid to anyons realized as [[Majorana zero modes]] [[bound state|bound]] to [[vortices]] ([Das Sarma, Freedman & Nayak 2015](topological+quantum+computation#DasSarmaFreedmanNayak15), cf. [MMBDRSC19](su2-anyon#MMBDRSC19))

{#BraidingOfNodalPointsInMomentumSpace} **Braiding of nodal points in momentum space** (graphics from [MMBDRSC19](su2-anyon#MMBDRSC19), [Fig. 1](https://www.nature.com/articles/s41467-019-10397-5.pdf#page=2)):

\begin{imagefromfile}
    "file_name": "MZMVortex-220530.jpg",
    "width": 440,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


#### Anyonic band nodes?
 {#AnyonicBandNodes}

Around 2020 the view has been emerging that also defects "in momentum/reciprocal space" may behave as anyonic defects under braiding in momentum space. This applies concretely to nodal points (where [[electron bands]] touch or cross) in the momentum space [[Brillouin torus]] of [[topological semi-metals]]:

> here are band crossing points, henceforth called [[vortices]] $[$[Ahnm Park & Yang 2019](#AhnParkYang19)$]$

> a new type non-Abelian "braiding" of nodal-line rings inside the momentum space $[$[Tiwari & Bzdušek 2020](#TiwariBzdusek20)$]$

\begin{imagefromfile}
    "file_name": "BraidingOfBandNodes-220529.jpg",
    "width": 500,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

> (graphics from [[schreiber:Topological Quantum Computation in TED-K|SS22]])


Curiously, these reciprocal/momemtum space anyons lend themselves to tractable laboratory manipulation in a way that has remained notoriously elusive for "position space" anyons:

> Our work opens up routes to readily manipulate Weyl nodes using only slight external parameter changes, paving the way for the practical realization of reciprocal space braiding $[$[CBSM22](#CBSM22)$]$,

specifically

> it is possible to controllably braid Kagome band nodes in monolayer $\mathrm{Si}_2 \mathrm{O}_3$ using strain and/or an external electric field $[$[PBMS22](#PBMS22)$]$,

leading to:

> new opportunities for exploring non-Abelian braiding of band crossing points (nodes) in reciprocal space, providing an alternative to the real space braiding exploited by other strategies. 

> Real space braiding is practically constrained to boundary states, which has made experimental observation and manipulation difficult; instead, reciprocal space braiding occurs in the bulk states of the band structures and we demonstrate in this work that this provides a straightforward platform for non-Abelian braiding. $[$[PBSM22](#PBSM22)$]$.





#### Defect branes
 {#DefectBranes}

In [[string theory]], *[[defect branes]]* are [[D-branes]] or [[M-branes]] of [[codimension]]=2, such as [[D7-branes]] in [[type IIB string theory]] or [[M5-brane]]-[[brane intersection|intersections]] on "[[3-brane in 6d|M3-branes]]" in [[M-theory]]. 

It has been suggest in [deBoer & Shigemori 2012, p. 65](defect+brane#deBoerShigemori12) that these could behave like anyons. This is further substantiated in [SS22](defect+brane#SS22). See [there](defect+brane#RelationToAnyons) for more.

\linebreak

## Related concepts

* [[boson]], [[fermion]]

* [[parastatistics]]

* [[su(2)-anyon]]

* [[unitary fusion category]]

* [[topological order]]

* [[topological quantum computation]]

* [[quantum Hall effect]]

## References

### General

The concept of [[anyons]] satisfying [[braid group statistics]] originated independently in

* {#LeinaasMyrheim77} J. M. Leinaas, J. Myrheim, _On the theory of identical particles_, _К теории тождествениых частиц_, Nuovo Cim B 37, 1–23 (1977) ([doi:10.1007/BF02727953](https://doi.org/10.1007/BF02727953))

* {#GoldinMenikoffSharp81} G. A. Goldin, R. Menikoff, D. H. Sharp, *Representations of a local current algebra in nonsimply connected space and the Aharonov–Bohm effect*, J. Math. Phys. **22** 1664 (1981) $[$[doi:10.1063/1.525110](https://doi.org/10.1063/1.525110)$]$ 

* {#Wilczek82} [[Frank Wilczek]], _Magnetic Flux, Angular Momentum, and Statistics_, Phys. Rev. Lett. 48, 1144, 1982 ([doi:10.1103/PhysRevLett.48.1144](https://doi.org/10.1103/PhysRevLett.48.1144))

Comprehensive accounts:

* {#Wilczek90} [[Frank Wilczek]], *Fractional Statistics and Anyon Superconductivity*, World Scientific (1990) $[$[doi:10.1142/0961](https://doi.org/10.1142/0961)$]$

* {#Kitaev06} [[Alexei Kitaev]], *Anyons in an exactly solved model and beyond*, Annals of Physics **321** 1 (2006) 2-111 $[$[doi:10.1016/j.aop.2005.10.005](https://doi.org/10.1016/j.aop.2005.10.005)$]$

The suggestion that the anyonic [[ground state]]-[[wavefunctions]] are essentially [[conformal blocks]] of [[2d CFT]] (notably for [[su(2)-anyons]]):

* {#MooreRead91} [[Gregory Moore]], [[Nicholas Read]], *Nonabelions in the fractional quantum hall effect*, Nuclear Physics B **360** 2–3 (1991) 362-396 $[$<a href="https://doi.org/10.1016/0550-3213(91)90407-O">doi:10.1016/0550-3213(91)90407-O</a>, [pdf](https://www.physics.rutgers.edu/~gmoore/MooreReadNonabelions.pdf)$]$

* {#ReadRezayi99} [[Nicholas Read]], [[Edward Rezayi]], *Beyond paired quantum Hall states: Parafermions and incompressible states in the first excited Landau level*, Phys. Rev. B **59** (1999) 8084 $[$[doi:10.1103/PhysRevB.59.8084](https://doi.org/10.1103/PhysRevB.59.8084)$]$

On [[superfluidity]]/[[superconductivity]] *of* [[anyons]]:

* {#ChenWilczekWittenHalperin89} Yi-Hong Chen, [[Frank Wilczek]], [[Edward Witten]], [[Bertrand Halperin]], *On Anyon Superconductivity*,  International Journal of Modern Physics B **03** 07 (1989) 1001-1067 (reprinted in [Wilczek 1990](#Wilczek90))  $[$[doi:10.1142/S0217979289000725](https://doi.org/10.1142/S0217979289000725), [[CWWH-AnyonSuperfluidity.pdf:file]]$]$

Rigorous discussion in terms of [[superselection sectors]] in [[algebraic quantum field theory]]:

* [[Klaus Fredenhagen]], Karl-Henning Rehren, [[Bert Schroer]], _Superselection sectors with braid group statistics and exchange algebras -- I: General theory_,   Comm. Math. Phys. Volume 125, Number 2 (1989), 201-226.  ([euclid:cmp/1104179464](http://projecteuclid.org/euclid.cmp/1104179464))

* [[Klaus Fredenhagen]], Karl-Henning Rehren, [[Bert Schroer]], _Superselection sectors with braid group statistics and exchange algebras -- II: Geometric aspects and conformal covariance_,  Reviews in Mathematical PhysicsVol. 04, No. spec01, pp. 113-157 (1992)  ([doi:10.1142/S0129055X92000170](https://doi.org/10.1142/S0129055X92000170) [pdf](ftp://ftp.theorie.physik.uni-goettingen.de/pub/papers/rehren/92/superselection_sectors_II_RMP.pdf))

* [[Jürg Fröhlich]], F. Gabbiani, _Braid statistics in local quantum theory_, Reviews in Mathematical Physics, Volume 2, Issue 03, pp. 251-353 (1990) ([doi:10.1142/S0129055X90000107](https://doi.org/10.1142/S0129055X90000107))_

Discussion in terms of [[modular tensor categories]] 

for abelian anyons:

* Liang Wang, [[Zhenghan Wang]], *In and around Abelian anyon models*, J. Phys. A: Math. Theor. **53** 505203 (2020) ([doi:10.1088/1751-8121/abc6c0](https://iopscience.iop.org/article/10.1088/1751-8121/abc6c0))



[[!include anyons in the quantum Hall effect -- references]]





[[!include anyons in topological superconductors -- references]]







### Experimental detection of anyons
 {#ExperimentalRealization}


While the occurrence of [[anyon]]-excitations in the [[quantum Hall effect]] is a robust theoretical prediction (see the references [above](#AnyonsInTheQuantumHallEffectReferences)), and while the quantum Hall effect itself has long been established in [[experiment]], the actual observation of anyons in these systems is subtle:

An early claim of the observation of non-abelian anyons seems to remain unconfirmed:

* Sanghun An, P. Jiang, H. Choi, W. Kang, S. H. Simon, L. N. Pfeiffer, K. W. West, K. W. Baldwin, _Braiding of Abelian and Non-Abelian Anyons in the Fractional Quantum Hall Effect_ ([arXiv:1112.3400](https://arxiv.org/abs/1112.3400))

The claimed observation of abelian anyons is apparently more securely established:

* H. Bartolomei, M. Kumar, R. Bisognin, A. Marguerite, J.-M. Berroir, E. Bocquillon, B. Plaçais, A. Cavanna, Q. Dong, U. Gennser, Y. Jin, G. Fève:

  *Fractional statistics in anyon collisions*, Science 368, 173-177 (2020) ([arXiv:2006.13157](https://arxiv.org/abs/2006.13157))

* James Nakamura, Shuang Liang, Geoffrey C. Gardner, Michael J. Manfra, _Direct observation of anyonic braiding statistics_, Nat. Phys. 16, 931–936 (2020). ([arXiv:2006.14115](https://arxiv.org/abs/2006.14115), [doi:10.1038/s41567-020-1019-1](https://doi.org/10.1038/s41567-020-1019-1))

* Bob Yirka, _Best evidence yet for existence of anyons_, PhysOrg News July 10, 2020  ([phys.org/news/2020-07](https://phys.org/news/2020-07-evidence-anyons.html))







[[!include defect anyons -- references]]








[[!include anyonic braiding in momentum space -- references]]








[[!include topological quantum computation with anyons -- references]]









[[!redirects braid statistics]]


[[!redirects anyon]]
[[!redirects anyons]]


[[!redirects anyon statistics]]

[[!redirects abelian anyon]]
[[!redirects abelian anyons]]

[[!redirects non-abelian anyon]]
[[!redirects non-abelian anyons]]
