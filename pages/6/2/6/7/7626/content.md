

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

## Idea
 {#Idea}

In [[quantum physics]], *braid group statistics* or *anyon statistics* refers to an exotic phenomenon where the [[braiding]] of the [[worldlines]] of certain effective [[particles]] ("anyons") in an effectively 2+1-dimensional [[spacetime]] has the effect of transforming the [[quantum state]] of the total [[quantum system]] by [[unitary operators]] which constitute a [[linear representation]] of the [[braid group]] -- a *[[braid representation]]*.

Often this is motivated as a generalization of the [[boson]]- or [[fermion]]-"statistics" which enters the *[[spin-statistics theorem]]*, see [below](#AsGeneralizedBosonFermionStatistics). But in reality this effect is often encountered not for fundamental [[particles]]/quanta, but for *[[soliton|solitonic]]$\;$[[defects]]*, see [further below](#AsBraidingOfDefects).

The concept of anyons is particularly well motivated in [[solid state physics]], where effectively 2-dimensional [[quantum materials]] are common place (eg. [[graphene]]) or where particles may otherwise be constrained to move in a [[plane]], such as in the [[quantum Hall effect]]. There is a multitude of *[[model (in theoretical physics)|models]]* in [[condensed matter theory]] (mostly [[lattice models]], such as [[string-net models]]) which *theoretically* realize anyon braid group statistics, and there are some first [[experiment|experimental]] indications of anyonic phenomena in actual materials (see the references under *[Experimental Realization](#ExperimentalRealization)*) below.

Specifically, in the context of [[topological phases of matter]], the (potential) presence of anyons has come to be known as the case of *[[topological order]]*, see there for more. 

Besides general curiosity, much of the interest in anyonic braid group statistics lies in the fact that these [[braid representations]] are imagined to potentially serve as [[quantum gates]] in [[topological quantum computers]]. See there for more.



### As generalized boson/fermion statistics
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




### As braiding of defects
 {#AsBraidingOfDefects}

In contrast to the traditional motivation [above](#AsGeneralizedBosonFermionStatistics), many (most?) incarnations of the concept of anyons are [[non-perturbative effect|non-perturbative]] [[soliton|solitonic]] [[defects]] (of [[codimension]]=2), akin to *[[vortices]]* in fluids. 

The effect of braiding of [[defects]] in [[quantum materials]] has been understood and discussed before the term "anyon" became established: [Mermin 1979](#Mermin79), [Lo & Preskill 1993](#LoPreskill93).
In [Kitaev 2006](#Kitaev06) it says explicitly:

> Anyonic particles are best viewed as a kind of topological defects that reveal non-trivial properties of the ground state. $[$p. 4$]$.

A concrete example of defect anyons are [[vortex]] anyons see [below](#VortexAnyons).

Of course, the notion of codimension=2 defects subsumes situations that are quite different from the [[quasiparticle]]-excitations imagined in traditional texts on anyons, such as:

* [anyonic band nodes](#AnyonicBandNodes)

* [defect branes](#DefectBranes).

#### Vortex anyons
 {#VortexAnyons}

Specifically, *[[vortex]] anyons* are realized in [[Bose-Einstein condensates]] ([MPSS19](#MPSS19), following [PFCZ01](#PFCZ01)) and in (other) [[superfluids]] ([MMN21](#MMN21)).

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

The concept of [[anyons]] satisfying [[braid group statistics]] goes back to:

* J. M. Leinaas, J. Myrheim, _On the theory of identical particles_, _К теории тождествениых частиц_, Nuovo Cim B 37, 1–23 (1977) ([doi:10.1007/BF02727953](https://doi.org/10.1007/BF02727953))

* {#Wilczek82} [[Frank Wilczek]], _Magnetic Flux, Angular Momentum, and Statistics_, Phys. Rev. Lett. 48, 1144, 1982 ([doi:10.1103/PhysRevLett.48.1144](https://doi.org/10.1103/PhysRevLett.48.1144))

Comprehensive account:

* {#Kitaev06} [[Alexei Kitaev]], *Anyons in an exactly solved model and beyond*, Annals of Physics **321** 1 (2006) 2-111 $[$[doi:10.1016/j.aop.2005.10.005](https://doi.org/10.1016/j.aop.2005.10.005)$]$


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
