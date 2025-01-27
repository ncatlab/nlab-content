

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topological physics
+--{: .hide}
[[!include topological physics -- contents]]
=--
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Anyon braiding
 {#Idea}

In [[quantum physics]], *braid group statistics* or *anyon statistics* (sometimes: *plektons*) refers to an exotic phenomenon where the [[braiding]] of the [[worldlines]] of certain effective [[particles]] ("anyons") in an effectively 2+1-dimensional [[spacetime]] has the effect of transforming the [[quantum state]] of the total [[quantum system]] by [[unitary operators]] which constitute a [[linear representation]] of the [[braid group]] -- a *[[braid representation]]*.

Often this is motivated as a generalization of the [[boson]]- or [[fermion]]-"statistics" which enters the *[[spin-statistics theorem]]*, see [below](#AsGeneralizedBosonFermionStatistics). 

But the actual mathematical nature of anyons must be different from that of elements of [[boson]]/[[fermion]]-[[Fock spaces]] and often remains somewhat vague in existing discussions. One may recognize two different more concrete conceptualizations of *anyons* in the literature:

1. {#AnyonicQuanta} **anyonic quanta** much like [[boson]]/[[fermion]] [[quanta]] but subject to an additional global [[interaction]] by [[Aharonov-Bohm effect|Aharonov-Bohm phases]] due to a [[flat connection|flat]] *[[fictitious gauge field]]* which is sourced by and coupled to each of the quanta;

   > (this goes back to [Arovas, Schrieffer, Wilczek & Zee 1985](#ArovasSchriefferWilczekZee85), further developed in [Chen, Wilczek, Witten & Halperin 1989](#ChenWilczekWittenHalperin89), see [below](#AsAFictitiousAharonovBohmEffect))

1. {#AnyonicDefects} **anyonic defects** like [[vortices]] or other [[solitons]], whose position is a [[parameterized quantum system|classical parameter]] to the [[quantum system]], the *[[quantum adiabatic theorem|adiabatic movement]]* of which acts by [[Berry phases]] on the quantum [[ground state]].

    > (e.g. [Avros, Schrieffer & Wilczek 1984](#AvrosSchriefferWilczek84), see [further below](#AsBraidingOfDefects))



The concept of anyons is particularly well motivated in [[solid state physics]], where effectively 2-dimensional [[quantum materials]] are common place (eg. [[graphene]]) or where particles may otherwise be constrained to move in a [[plane]], such as in the [[quantum Hall effect]]. There is a multitude of *[[model (in theoretical physics)|models]]* in [[condensed matter theory]] (mostly [[lattice models]], such as [[string-net models]]) which *theoretically* realize anyon braid group statistics, and there are some first [[experiment|experimental]] indications of anyonic phenomena in actual materials (see the references under *[Experimental Realization](#ObservationOfAnyonsInFQH)*) below.

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

The term *anyon* (due to [Wilczek 1982b](#Wilczek82b)) is a pun on this state of affairs that *any* statistics "in between" boson- and fermion-statistics may be allowed.

On the other hand, anyonic braiding is conceptually different from boson/fermion statistics -- if it were on the same footing then the [[spin-statistics theorem]] would *rule out* anyonic braiding. This is acknowledged by [Chen, Wilczek, Witten & Halperin 1989, p. 352](#ChenWilczekWittenHalperin89) (cf. also [Wilczek 1990, §I.2, pp. 11](#Wilczek90)):

> Once the [[permutation group]] is replaced by the [[braid group]], the simple construction of passing from the solution to the one-particle problems to the solution of many-particle problems, familiar from the free bosons and free fermions, does not work anymore. 

\linebreak

### Braiding of anyonic quanta -- via "fictitious" AB-phases
 {#AsAFictitiousAharonovBohmEffect}

A concrete model for *[anyonic quanta](#AnyonicQuanta)* via otherwise [[free field|free]] [[fermions]] in 2d [[interaction|interacting]] through a [[flat connection|flat]] "[[fictitious gauge field]]" was proposed in [Arovas, Schrieffer, Wilczek & Zee 1985](#ArovasSchriefferWilczekZee85) and developed in
[Chen, Wilczek, Witten & Halperin 1989](#ChenWilczekWittenHalperin89) and [Iengo & Lechner 1992](#IengoLechner92) (the model has been advertized in early reviews, e.g. [Wilczek 1990, §I.3](#Wilczek90) and [Wilczek 1991](#Wilczek91), but seems not to have been developed much since):

This model regards anyons as *a priori* [[free field|free]] [[fermions]], but equipped now with a non-local mutual [[interaction]] via a "fictitious gauge field" ([CWWH89, §2](#ChenWilczekWittenHalperin89)), in that
each of the particles is modeled as the singular source of a [[flat connection|flat]] [[circle bundle with connection|circle connection]] (a [[vector potential]] with vanishing [[field strength]]), which hence exerts no [[Lorentz force]] but has the effect that globally each other particle is subject to the same [[Aharonov-Bohm effect]] as would be caused by a tuple of infinite [[solenoids]] piercing through each of the other particle's positions.

For emphasis, from [CWWH89, p. 359](#ChenWilczekWittenHalperin89):

> Here the particles are to be regarded (in the absence of 
interactions) as fermions; the interaction then makes them anyons with statistical 
parameter $\theta = \pi(1 - 1/n)$.

It follows ([Wu 1984](#Wu84), [Imbo, Imbo & Sudarshan 1990](#ImboImboSudarshan90)) that (quoting from [Fröhlich, Gabbiani & Marchetti 1990, p. 20](#FroehlichGabbianiMarchetti90)):

> If $\theta \in\!\!\!\!\!/ \frac{1}{2}\mathbb{Z}$ the [[space of quantum states|Hilbert space]] of [[anyon]] [[wave functions]] must be chosen to be a space of [[multi-valued functions]] with half-[[monodromies]] given by the [[complex phase|phase]] factors $exp(2 \pi \mathrm{i} \theta)$. Such wave functions can be viewed as single-valued functions on the [[universal cover]] $\widetilde M_n$ of $M_n$ &lbrack;the [[configuration space of points]]&rbrack.

Further discussion of anyon-[[wavefunctions]] as [[multi-valued functions]] on a [[configuration space of points]], hence [[equivariant functions]] on its [[universal cover]]: [BCMS93, §1](#BCMS93), [Mund & Schrader 1995](#MundSchrader93), [DFT97, §1](#DFT97) [Myrheim 1999](#Myrheim99), [DMV03](#DMV03), [Murthy & Shankar 2009](#MurthyShankar09)



Incidentally, the [[quasi-particle]]-excitations *of* (or *in*) a gas of such Aharonov-Bohm phased anyons are argued to be [[vortices]] ([CWWH89, p. 457](#ChenWilczekWittenHalperin89)):

> we are led to conclude that *in anyon superconductivity, charged quasi-particles and vortices do not constitute two separate sorts of elementary excitations - they are one and the same.*

This seamlessly leads over to:

\linebreak

### Braiding of anyonic defects -- via adiabatic Berry phases
 {#AsBraidingOfDefects}

In practice, many (most?) incarnations of the concept of anyons are *[anyonic defects](#AnyonicDefects)* -- [[non-perturbative effect|non-perturbative]] [[soliton|solitonic]] [[defects]] (of [[codimension]]=2), akin to *[[vortices]]* in fluids:

> *Anyonic particles are best viewed as a kind of topological defects that reveal non-trivial properties of the ground state.* &lbrack;[Kitaev 2006, p. 4](#Kitaev06)&rbrack;

>  *Anyons can arise in two ways: as localised excitations of an interacting
quantum Hamiltonian or as defects in an ordered system.*  &lbrack;[Das Sarma, Freedman & Nayak 2015, p. 1](topological+quantum+computation#DasSarmaFreedmanNayak15)&rbrack;

(Compare also the original discussions in [Goldin, Menikoff & Sharp 1981, §III](#GoldinMenikoffSharp81), [Wilczek 1982a](#Wilczek82a) & [Wilczek 1990, p. 5](#Wilczek90), which offer a quantum particle "[[bound state|bound]]" to a classical & infinite [[solenoid]] -- hence a 2d [[magnetic monopole]] [[defect]] -- as a decent model for an anyon.)

But [[defects]] are a kind of [[boundary conditions]], hence *external parameters* or *[[background fields]]* for the actual [[quantum field]]. 

Concretely, a widely appreciated proposal ([Moore & Read 1991](#MooreRead91), [Read & Rezayi 1999](#ReadRezayi99)) identifies anyonic ground state [[wavefunctions]] with [[conformal blocks]] of a [[2d CFT]] -- [[AdS3-CFT2 and CS-WZW correspondence|hence]] with [[Chern-Simons theory]] [[quantum states|states]] -- with prescribed poles at the location of the anyons.

Now the [[quantum adiabatic theorem]] says that the sufficiently slow motion of such external parameters transforms the quantum [[ground state]] by [[unitary operators]] ("[[Berry phases]]", see also at *[[adiabatic quantum computation]]*). This suggests ([Avros, Schrieffer & Wilczek 1984, p. 1](#AvrosSchriefferWilczek84),  [Freedman, Kitaev, Larsen & Wang 2003, pp. 6](#FreedmanKitaevLarsenWang03), [Nayak, Simon, Stern & Freedman 2008, §II.A.2 (p. 6)](#NayakSimonSternFreedman08), [Cheng, Galitski & Das Sarma 2011, p. 1](adiabatic+quantum+computation#ChengGalitskiDasSarma11)) that:

\begin{definition}\label{DefectBraiding}
**(adiabatic defect braiding)**
\linebreak
*Anyon braiding statistics is the [[braid group representation]] on a quantum [[ground state]] induced by [[adiabatic theorem|adiabatic]] [[braiding]] of [[TQFT|topological]] [[codimension]]=2 [[defects]] in their [[configuration space of points|configuration space]].*

Here 

1. for point-defects the "configuration space" is the [[configuration space of points]] in a [[surface]] (as briefly touched upon already in [Leinaas & Myrheim 1977, pp. 22](#LeinaasMyrheim77), [Wilczek 1982b, p. 959](#Wilczek82b)), such as in the [[plane]], in which case its fundamental group is the [[braid group]];

1. "topological" is meant as in [[topological quantum field theory]]: The induced [[adiabatic theorem|adiabatic]] [[unitary transformation]] is demanded/assumed to depend only on the [[isotopy]]-class of the defect-[[worldlines]], hence only on the underlying [[braid group|braid]]-pattern.

\end{definition}



This notion of anyon "statistics" is at least tacitly implicit in much of the literature on anyons in [[topological quantum computation]], such as in the popular graphics depicting anyon [[worldlines]] as the [[Wilson lines]] in [[Chern-Simons theory]]. (see the graphics [below](#BraidingOfNodalPointsInMomentumSpace)).

Indeed, the effects of [[adiabatic theorem|adiabatic]] braiding of [[defects]] in [[quantum materials]] has been understood and discussed before and in parallel to the term "anyon" becoming established: [Mermin 1979](#Mermin79), [Lo & Preskill 1993](#LoPreskill93).

A concrete realistic example of defect anyons are [[vortex]] anyons see [below](#VortexAnyons).
But the notion of codimension=2 defects subsumes situations that are quite different from the [[quasiparticle]]-excitations imagined in traditional texts on anyons, such as:

* [anyonic band nodes](#AnyonicBandNodes)

* [defect branes](#DefectBranes).






#### Vortex anyons
 {#VortexAnyons}


Specifically, *[[vortex]] anyons* are realized in [[Bose-Einstein condensates]] ([MPSS19](#MPSS19), following [PFCZ01](#PFCZ01)) and in (other) [[superfluids]] ([MMN21](#MMN21)). 

{#VorticesInAnyonCondensate} In fact, defect-type *vortex anyons* generically appear in [[condensates]] *of non-defect anyons* ([CDLR19](#CDLR19)):


\begin{imagefromfile}
    "file_name": "VorticesInAnyonCondensate.jpg",
    "width": 430,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "From [CDLR19](#CDLR19)"
\end{imagefromfile}




A theoretical model of vortex anyons in a [[Higgs field]] [[interaction|coupled to]] [[Chern-Simons theory]] is discussed in [Fröhlich & Marchetti 1988](#FroehlichMarchetti88).
An instructive [[lattice model]] of vortex anyons is analyzed in detail in [Kitaev 2006](#Kitaev06).

Much attention in current efforts towards realizing [[topological quantum computation]] is being paid to anyons realized as [[Majorana zero modes]] [[bound state|bound]] to [[vortices]] ([Das Sarma, Freedman & Nayak 2015](topological+quantum+computation#DasSarmaFreedmanNayak15), cf. [MMBDRSC19](su2-anyon#MMBDRSC19)). 

{#MayGeneralize} This situation may generalize to [[parafermion]]-[[su(2)-anyons]], where 

> each (anti)[[soliton]] carries [[parafermion]] zero mode which supplies
it with the non-Abelian statistics &lbrack;[Tsvelik 2014a](parafermion#Tsvelik2014a), [p. 2](https://arxiv.org/pdf/1404.2840.pdf#page=2), cf. [Borcherding 2018, pp. 3](parafermion#Borcherding18)&rbrack;.



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

> here are band crossing points, henceforth called [[vortices]] &lbrack;[Ahnm Park & Yang 2019](#AhnParkYang19)&rbrack;

> a new type non-Abelian "braiding" of nodal-line rings inside the momentum space &lbrack;[Tiwari & Bzdušek 2020](#TiwariBzdusek20)&rbrack;

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

> Our work opens up routes to readily manipulate Weyl nodes using only slight external parameter changes, paving the way for the practical realization of reciprocal space braiding &lbrack;[CBSM22](#CBSM22)&rbrack;,

specifically

> it is possible to controllably braid Kagome band nodes in monolayer $\mathrm{Si}_2 \mathrm{O}_3$ using strain and/or an external electric field &lbrack;[PBMS22](#PBMS22)&rbrack;,

leading to:

> new opportunities for exploring non-Abelian braiding of band crossing points (nodes) in reciprocal space, providing an alternative to the real space braiding exploited by other strategies. 

> Real space braiding is practically constrained to boundary states, which has made experimental observation and manipulation difficult; instead, reciprocal space braiding occurs in the bulk states of the band structures and we demonstrate in this work that this provides a straightforward platform for non-Abelian braiding. &lbrack;[PBSM22](#PBSM22)&rbrack;.





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

The concept of [[anyons]] satisfying [[braid group statistics]] originated independently in:

* {#LeinaasMyrheim77} [[Jon Magne Leinaas]], [[Jan Myrheim]], _On the theory of identical particles_, _К теории тождествениых частиц_, Nuovo Cim B 37, 1–23 (1977) ([doi:10.1007/BF02727953](https://doi.org/10.1007/BF02727953))

* {#GoldinMenikoffSharp81} G. A. Goldin, R. Menikoff, D. H. Sharp, *Representations of a local current algebra in nonsimply connected space and the Aharonov–Bohm effect*, J. Math. Phys. **22** 1664 (1981) &lbrack;[doi:10.1063/1.525110](https://doi.org/10.1063/1.525110)&rbrack; 

* {#Wilczek82a} [[Frank Wilczek]], _Magnetic Flux, Angular Momentum, and Statistics_, Phys. Rev. Lett. **48** (1982) 1144 (reprinted in [Wilczek 1990, p. 163-165](#Wilczek90)) &lbrack;[doi:10.1103/PhysRevLett.48.1144](https://doi.org/10.1103/PhysRevLett.48.1144)&rbrack;

The term *anyon* was introduced in:

* {#Wilczek82b} [[Frank Wilczek]], *Quantum Mechanics of Fractional-Spin Particles*, Phys. Rev. Lett. **49** (1982) 957 (reprinted in [Wilczek 1990, p. 166-168](#Wilczek90)) &lbrack;[doi:10.1103/PhysRevLett.49.957](https://doi.org/10.1103/PhysRevLett.49.957)&rbrack;

Identification of anyon phases (specifically in the [[quantum Hall effect]]) as [[Berry phases]] of an [[quantum adiabatic theorem|adiabatic transport]] of anyon positions:

* {#AvrosSchriefferWilczek84} [[Daniel P. Arovas]], [[John Robert Schrieffer]], [[Frank Wilczek]], _Fractional Statistics and the Quantum Hall Effect_, Phys. Rev. Lett. 53, 722 (1984) &lbrack;[doi:10.1103/PhysRevLett.53.722](https://doi.org/10.1103/PhysRevLett.53.722)&rbrack;



The "[[fictitious gauge field]]"-method for modelling anyons:

* {#ArovasSchriefferWilczekZee85} [[Daniel P. Arovas]], [[Robert Schrieffer]], [[Frank Wilczek]], [[Anthony Zee]], *Statistical mechanics of anyons*, Nuclear Physics B **251** (1985) 117-126 (reprinted in [Wilczek 1990, p. 173-182](#Wilczek90)) &lbrack;<a href="https://doi.org/10.1016/0550-3213(85)90252-4">doi:10.1016/0550-3213(85)90252-4</a>&rbrack;

* {#ChenWilczekWittenHalperin89} [[Yi-Hong Chen]], [[Frank Wilczek]], [[Edward Witten]], [[Bertrand Halperin]], *On Anyon Superconductivity*,  International Journal of Modern Physics B **03** 07 (1989) 1001-1067 (reprinted in [Wilczek 1990, p. 342-408](#Wilczek90))  &lbrack;[doi:10.1142/S0217979289000725](https://doi.org/10.1142/S0217979289000725), [[CWWH-AnyonSuperfluidity.pdf:file]]&rbrack;

* {#Wilczek91} [[Frank Wilczek]], *States of Anyon Matter*,  International Journal of Modern Physics B **05** 09 (1991) 1273-1312 &lbrack;[doi:10.1142/S0217979291000626](https://doi.org/10.1142/S0217979291000626)&rbrack;

and with specific emphasis on the resulting (abelian!) [[Chern-Simons theory]]:

* {#IengoLechner92} [[Roberto Iengo]], [[Kurt Lechner]], *Anyon quantum mechanics and Chern-Simons theory*, Physics Reports **213** 4 (1992) 179-269 &lbrack;<a href="https://doi.org/10.1016/0370-1573(92)90039-3">doi:10.1016/0370-1573(92)90039-3</a>&rbrack;



The suggestion that the anyonic [[ground state]]-[[wavefunctions]] are essentially [[conformal blocks]] of [[2d CFT]] (notably for [[su(2)-anyons]]):

* {#MooreRead91} [[Gregory Moore]], [[Nicholas Read]], *Nonabelions in the fractional quantum hall effect*, Nuclear Physics B **360** 2–3 (1991) 362-396 &lbrack;<a href="https://doi.org/10.1016/0550-3213(91)90407-O">doi:10.1016/0550-3213(91)90407-O</a>, [pdf](https://www.physics.rutgers.edu/~gmoore/MooreReadNonabelions.pdf)&rbrack;

* {#ReadRezayi99} [[Nicholas Read]], [[Edward Rezayi]], *Beyond paired quantum Hall states: Parafermions and incompressible states in the first excited Landau level*, Phys. Rev. B **59** (1999) 8084 &lbrack;[doi:10.1103/PhysRevB.59.8084](https://doi.org/10.1103/PhysRevB.59.8084)&rbrack;

More comprehensive accounts of anyons:

* {#Wilczek90} [[Frank Wilczek]], *Fractional Statistics and Anyon Superconductivity*, World Scientific (1990) &lbrack;[doi:10.1142/0961](https://doi.org/10.1142/0961)&rbrack;

* {#Kitaev06} [[Alexei Kitaev]], *Anyons in an exactly solved model and beyond*, Annals of Physics **321** 1 (2006) 2-111 &lbrack;[doi:10.1016/j.aop.2005.10.005](https://doi.org/10.1016/j.aop.2005.10.005)&rbrack;

* [[Eduardo Fradkin]], *Anyon superconductivity*, Chapter 11 in: *Field Theories of Condensed Matter Physics*, Cambridge University Press (2013) 414-431 &lbrack;ISBN: 9781139015509, [doi:10.1017/CBO9781139015509.013](https://doi.org/10.1017/CBO9781139015509.013)&rbrack;


See also:

* [[Martin Greiter]], [[Frank Wilczek]], *Fractional Statistics* &lbrack;[arXiv:2210.02530](https://arxiv.org/abs/2210.02530)&rbrack;

On the history of the concept:

* Gerald A. Goldin: *The Prediction of Anyons: Its History and Wider Implications*, SciPost Phys. Proc. **14** 005 (2023)  &lbrack;[arXiv:2212.12632](https://arxiv.org/abs/2212.12632), [doi: 10.21468/SciPostPhysProc.14.005](https://scipost.org/SciPostPhysProc.14.005)&rbrack;


Rigorous discussion in terms of [[superselection sectors]] in [[algebraic quantum field theory]]:

* {#FroehlichMarchetti88} [[Jürg Fröhlich]], [[Pieralberto Marchetti]], *Quantum field theory of anyons*, Lett. Math. Phys. **16** (1988) 347–358 (reprinted in [Wilczek 1990, p. 202-213](#Wilczek90)) &lbrack;[doi:10.1007/BF00402043](https://doi.org/10.1007/BF00402043)&rbrack;

* [[Jürg Fröhlich]], [[Fabrizio Gabbiani]], *Braid statistics in local quantum theory*, Reviews in Mathematical Physics, **2** 03 (1990) 251-353 &lbrack;[doi:10.1142/S0129055X90000107](https://doi.org/10.1142/S0129055X90000107)&rbrack;

* {#FroehlichGabbianiMarchetti90} [[Jürg Fröhlich]], [[Fabrizio Gabbiani]], [[Pieralberto Marchetti]], *Braid statistics in three-dimensional local quantum field theory*, in: H.C. Lee (ed.) *Physics, Geometry and Topology* NATO ASI Series, **238** Springer (1990)  &lbrack;[doi:10.1007/978-1-4615-3802-8_2](https://doi.org/10.1007/978-1-4615-3802-8_2), [[FroehlichGabbianiMarchetti-BraidStatistics.pdf:file]]&rbrack;

* [[Klaus Fredenhagen]], Karl-Henning Rehren, [[Bert Schroer]], _Superselection sectors with braid group statistics and exchange algebras -- I: General theory_,   Comm. Math. Phys. Volume 125, Number 2 (1989), 201-226.  ([euclid:cmp/1104179464](http://projecteuclid.org/euclid.cmp/1104179464))

* [[Klaus Fredenhagen]], Karl-Henning Rehren, [[Bert Schroer]], _Superselection sectors with braid group statistics and exchange algebras -- II: Geometric aspects and conformal covariance_,  Reviews in Mathematical PhysicsVol. 04, No. spec01, pp. 113-157 (1992)  ([doi:10.1142/S0129055X92000170](https://doi.org/10.1142/S0129055X92000170) [pdf](ftp://ftp.theorie.physik.uni-goettingen.de/pub/papers/rehren/92/superselection_sectors_II_RMP.pdf))

Discussion of anyon-[[wavefunctions]] as [[multi-valued functions]] on a [[configuration space of points]]:

* {#Wu84} [[Yong-Shi Wu]], *Multiparticle Quantum Mechanics Obeying Fractional Statistics*, Phys. Rev. Lett. **53** (1984) 111 &lbrack;[doi:10.1103/PhysRevLett.53.111](https://doi.org/10.1103/PhysRevLett.53.111), [pdf](https://core.ac.uk/download/pdf/276286925.pdf)&rbrack;

* [Fröhlich, Gabbiani & Marchetti 1990, p. 20](#FroehlichGabbianiMarchetti90)

* {#ImboImboSudarshan90} Tom Imbo, Chandni Shah Imbo, E. C. G. Sudarshan, *Identical particles, exotic statistics and braid groups*, Physics Letters B **234** 1–2, (1990) 103-107 &lbrack;<a href="https://doi.org/10.1016/0370-2693(90)92010-G">doi:10.1016/0370-2693(90)92010-G</a>, [pdf](https://lib-extopc.kek.jp/preprints/PDF/2000/0033/0033552.pdf)&rbrack;


* {#BCMS93} Garth A. Baker, Geoff S. Canright, Shashikant B. Mulay, Carl Sundberg, *On the spectral problem for anyons*, Communications in Mathematical Physics **153** (1993) 277–295 &lbrack;[doi:10.1007/BF02096644](https://doi.org/10.1007/BF02096644)&rbrack;

* {#MundSchrader93} J. Mund, [[Robert Schrader]], *Hilbert Spaces for Nonrelativistic and Relativistic "Free" Plektons (Particles with Braid Group Statistics)*, in *Advances in dynamical systems and quantum physics* (Capri, 1993), World Sci. (1995) 235–259 &lbrack;[arXiv:hep-th/9310054](https://arxiv.org/abs/hep-th/9310054)&rbrack;

  followed up by:

  [[Klaus Fredenhagen]], [[Matthias Gaberdiel]] and Stefan M. Rüger, *Scattering states of plektons (particles with braid group statistics) in 2+1 dimensional quantum field theory*, Communications in Mathematical Physics **175** (1996) 319–335 &lbrack;[doi:10.1007/BF02102411](https://doi.org/10.1007/BF02102411)&rbrack;

* {#DFT97} Gianfausto Dell'Antonio, Rodolfo Figari, Alessandro Teta: *Statistics in Space Dimension Two*, Letters in Mathematical Physics **40** (1997) 235–256 &lbrack;[doi:10.1023/A:1007361832622](https://doi.org/10.1023/A:1007361832622)&rbrack;

    

* {#Myrheim99} [[Jan Myrheim]], *Anyons*, p. 265-414 in: *Topological aspects of low dimensional systems*, Les Houches LXIX, Springer (1999) &lbrack;[doi:10.1007/3-540-46637-1](https://doi.org/10.1007/3-540-46637-1), [[Myrheim-Anyons.pdf:file]]&rbrack;

* {#MurthyShankar09} [[M.V.N. Murthy]], [[Ramamurti Shankar]], *Exclusion Statistics: From Pauli to Haldane* (1999, 2009) &lbrack;[dspace:123456789/334](https://dspace.imsc.res.in/xmlui/handle/123456789/334), [pdf](https://www.imsc.res.in/xmlui/bitstream/handle/123456789/334/MR120.pdf?sequence=1), [[MurthyShankar-ExclusionStatistics.pdf:file]]&rbrack;

* {#DMV03} G. Date, [[M.V.N. Murthy]], [[Radhika Vathsan]], *Classical and Quantum Mechanics of Anyons* &lbrack;[arXiv:cond-mat/0302019](https://arxiv.org/abs/cond-mat/0302019)&rbrack;

The topic of [[quantum measurement]] of non-abelian anyons is crucial to their identification in [[experiment]] but has received little attenion, exceptions being:

* {#BondersonShtengelSlingerland07} [[Parsa Bonderson]], [[Kirill Shtengel]], [[Joost Slingerland]], *Decoherence of Anyonic Charge in Interferometry Measurements*, Phys. Rev. Lett. **98** (2007) 070401 &lbrack;[doi:10.1103/PhysRevLett.98.070401](https://doi.org/10.1103/PhysRevLett.98.070401), [arXiv:quant-ph/0608119](https://arxiv.org/abs/quant-ph/0608119)&rbrack;

* {#BondersonShtengelSlingerland08} [[Parsa Bonderson]], [[Kirill Shtengel]], [[Joost Slingerland]], *Interferometry of non-Abelian Anyons*, Annals Phys. **323** (2008) 2709-2755 &lbrack;[doi:10.1016/j.aop.2008.01.012](https://doi.org/10.1016/j.aop.2008.01.012), [arXiv:0707.4206](https://arxiv.org/abs/0707.4206)&rbrack;

* [[Andrey Morozov]], *On measuring the topological charge of anyons* &lbrack;[arXiv:2403.07847](https://arxiv.org/abs/2403.07847)&rbrack;





[[!include anyonic topological order via braided fusion categories -- references]]




[[!include anyons in the quantum Hall effect -- references]]





[[!include anyons in topological superconductors -- references]]








[[!include defect anyons -- references]]








[[!include anyonic braiding in momentum space -- references]]








[[!include topological quantum computation with anyons -- references]]








[[!redirects braid statistics]]


[[!redirects anyon]]
[[!redirects anyons]]


[[!redirects anyon statistics]]

[[!redirects anyon braiding]]
[[!redirects anyonic braiding]]

[[!redirects abelian anyon]]
[[!redirects abelian anyons]]

[[!redirects non-abelian anyon]]
[[!redirects non-abelian anyons]]

