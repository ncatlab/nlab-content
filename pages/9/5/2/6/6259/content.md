+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The standard [[action functional]] for the [[higher U(1)-gauge field]] given by a [[circle n-bundle with connection]] $(P, \nabla)$ over a [[pseudo-Riemannian manifold|(pseudo)]] [[Riemannian manifold]] $(X,g)$ is 

$$
  \nabla \mapsto \int_X F_\nabla \wedge \star_g F_{\nabla}
  \,,
$$

where $F_\nabla$ is the [[curvature]] $(n+1)$-form. If the [[dimension]] 

$$
  dim X = 4 k + 2 
$$

then the [[Hodge star]] operator squares to $+1$ (Lorentzian signature) or $-1$ (Euclidean signature) on $\Omega^{k+1}(X)$. Therefore it makes sense in these dimensions to impose the _self-duality_ or _chirality_ constraint

$$
  \pm F_\nabla = \star F_\nabla
  \,.
$$

With this duality constraint imposed, one speaks of **self-dual higher gauge fields** or **chiral higher gauge fields** or **higher gauge fields with self-dual curvature**. (These are a higher degree/dimensional generalization of what in [[Yang-Mills theory]] are called [[Yang-Mills instanton]] field configurations.)

Since imposing the self-duality constraint on the fields that enter the above [[action functional]] makes that functional vanish identically, self-dual higher gauge theory is notorious for being subtle in that either it does not have a [[Lagrangian field theory]] description, or else a somewhat intricate indirect one (e.g. [Witten 96, p. 7](#Witten96), [Belov-Moore 06a](#BelovMooreI)). But instead one may regard the self-duality condition rather as part of the quantum theory ([Witten 96, p.8](#Witten96), [Witten 99, section 3](#Witten99) [DMW 00b, page 3](#MW00)), namely as a choice of [[polarization]] of the [[phase space]] of an unconstrained theory in one dimension higher. By such as "[[holographic principle]]" the [[partition function]] of the self-dual theory on an $X$ of dimension $4 k +2$ is given by the [[state]] (wave function) of an abelian  [[higher dimensional Chern-Simons theory]] in dimension $4 k + 3$.

The way this works is understood in much mathematical detail for $k = 0$, see at _[[AdS3-CFT2 and CS-WZW correspondence]]_. Motivated by this it has been proposed and studied in a fair bit of mathematical detail for $k = 1$ ([Witten 96](#Witten96), [[Quadratic Functions in Geometry, Topology, and M-Theory|Hopkins-Singer 02]]), see at _[[M5-brane]]_ and _[[6d (2,0)-superconformal QFT]]_ and [AdS7/CFT6](AdS-CFT#AdS7CFT6). In both these cases the [[higher gauge fields]] are [[cocycle]]s in [[ordinary differential cohomology]]. In ([DMW 00](#MW00), [Belov-Moore 06b](#BelovMooreII)) it is suggested that similarly taking the self-dual fields to be cocycles in ([[differential K-theory|differential]]) [[complex K-theory]] produces the [[RR-fields]] of [[type II superstring theory]] in dimension 10.


## Definition (outline)
 {#Definition}

The [[holographic principle|holographic]] definition of self-dual abelian higher gauge field theory in dimension $4k+2$ given in ([Witten 96](#Witten96), [Witten 99](#Witten99)) is in outline the following.

Imagine the self-dual $2k$-form [[field (physics)|field]] on $\Sigma$ to be coupled to [[sources]] given by $(2k+1)$-form gauge fields, hence by [[cocycles]] in [[ordinary differential cohomology]] $[\Sigma, \mathbf{B}^{2k+1}\mathbb{G}^\times_{conn}]$ of degree $(2k+2)$. One may try to write down a [[Lagrangian]] for this coupling (and that is what is discussed in ([Belov-Moore 06I](#BelovMooreI))) and the resulting [[partition function]] is then locally a function of the [[source fields]], hence a function on the [[intermediate Jacobian]] $[\Sigma, \mathbf{B}^{2k+1}\mathbb{G}^\times_{conn}]$ and globally (since the [[action functional]] will not be strictly [[gauge invariance|gauge invariant]]) a holomorphic [[section]] of a certain [[holomorphic line bundle]] on that space.

However, no choice of [[Lagrangian]] will enforce a strictly self-dual gauge field (the anti-self dual component will remain in the space of fields, hence the partition function will depend on it). Therefore the idea is to turn this around, reject the idea that self-dual higher gauge theory is directly itself a [[Lagrangian quantum field theory]], and instead _define_ the partition function of the self-dual higher gauge theory (and thereby, indirectly, the self-dual higher gauge theory itself!) as being a certain section of a certain line bundle on the [[intermediate Jacobian]].

The question then is: which line bundle? Some plausibility arguments show that it must be a [[Theta characteristic]] bundle, hence a [[square root]] of the [[canonical bundle]] on the [[intermediate Jacobian]].  These have 1-dimensional spaces of holomorphic sections ([[theta functions]]) and hence any choice of that already uniquely fixes the would-be [[partition function]], too, up to a choice of global factor. (For that reason later authors often regard the partition function as a line bundle, somewhat abusing the terminology.)

The claim then is that the correct choice of [[Theta characteristic]] to use is a [[quadratic refinement]] of the [[intersection pairing]] (the [[Beilinson-Deligne cup-product]])

$$
  [\Sigma, \mathbf{B}^{2k+1}\mathbb{G}^\times_{conn}]
  \times
  [\Sigma, \mathbf{B}^{2k+1}\mathbb{G}^\times_{conn}]
  \stackrel{\cup}{\longrightarrow}
  [\Sigma, \mathbf{B}^{4k+3}\mathbb{G}^\times_{conn}]
  \stackrel{\int}{\longrightarrow}
  \mathbf{B}\mathbb{G}^\times_{conn}
  \,.
$$

Such [[quadratic refinement]] turns out to be given for $k = 0$ by a [[Spin structure]] (leading to "[[Spin Chern-Simons theory]]") and for $k =1$ by a [[Wu structure]] (and the latter case is the actual example of interest in ([Witten 96](#Witten96))). This is what the central theorem of ([[Quadratic Functions in Geometry, Topology, and M-Theory|Hopkins-Singer 02]]) establishes rigorously.

One notices now that while the self-dual $(4k+2)$-dimensional gauge field theory thus itself is not a [[Lagrangian quantum field theory]], it arises [[holographic principle|holographically]] form a field theory in dimension $4k+3$ that is, namely the [[intersection pairing]] above is the [[Lagrangian]] for [[higher dimensional Chern-Simons theory]] and the [[holomorphic line bundle]] which it gives rise to on the [[intermediate Jacobian]], is the [[prequantum line bundle]] of Chern-Simons theory, whose holomorphic sections are its [[quantum states]] (see at _[[quantization of Chern-Simons theory]]_). From this perspective the [[square root]] [[quadratic refinement]] is the [[metaplectic correction]] in the [[geometric quantization]] of Chern-Simobs theory.

This kind of relation

| self-dual $(4k+2)$d gauge theory |   | $(4k+3)$d Chern-Simons theory |
|---|---|---|
| [[sources]] | $\leftrightarrow$ |  [[field (physics)|fields]] |
| [[partition function]]/[[correlator]] | $\leftrightarrow$ | [[wavefunction]]/[[quantum state]] |
| [[conformal blocks]] | $\leftrightarrow$ | [[space of quantum states]] |

is the hallmark of the [[holographic principle]].


## Properties

### Holographic relation to higher Chern-Simons theory

#### Idea and examples

Generally, [[higher dimensional Chern-Simons theory]]
in dimension $4k+3$ (for $k \in \mathbb{N}$) is [[holographic principle|holographically]] related to self-dual higher gauge theory in dimension $4k+2$ (at least in the abelian case). 

* $(k=0)$: ordinary 3-dimensional [[Chern-Simons theory]] is related to a [[string]] [[sigma-model]] on its boundary;

* $(k=1)$: [[7-dimensional Chern-Simons theory]] is related to a [[fivebrane]] model on its boundary;

* $(k=2)$: [[11-dimensional Chern-Simons theory]] (of [[field (physics)|fields]] which are [[cocycles]] in ([[twisted differential K-theory|twisted differential]]) [[complex K-theory]]) is related to a parts of a [[type II string theory]] on its boundary (or that of the space-filling [[D9-brane]], if one wishes) ([Belov-Moore 06b](#BelovMooreII)).


#### Conformal structure from polarization
 {#ConformalStructureFromPolarization}

We indicate why [[higher dimensional Chern-Simons theory]] is -- if holographically related to anything -- holographically related to [[self-dual higher gauge theory]].

The [[phase space]] of [[higher dimensional Chern-Simons theory]] in [[dimension]] $4k+3$ on $\Sigma \times \mathbb{R}$ can be identified with the space of [[curvature|flat]] $2k+1$-forms on $\Sigma$. The [[presymplectic form]] on this space is given by the pairing

$$
  (\delta B_1, \delta B_2) \mapsto
  \int_\Sigma \delta B_1 \wedge \delta B_2
$$

obtained as the [[integration of differential forms]] over $\Sigma$ of the [[wedge product]] of the two forms.

The [[geometric quantization]] of the theory requires that we choose a [[polarization]] of the [[complexification]] of this space (split the space of forms into "[[canonical coordinates]]" and their "[[canonical momenta]]"). 

One way to achieve this is to choose a [[conformal structure]] on $\Sigma$. The corresponding [[Hodge star operator]]

$$
  \star : \Omega^{2k+1}(\Sigma) \to \Omega^{2k+1}(\Sigma)
$$

provides the polarization by splitting into self-dual and anti-self-dual forms: 

notice that (by [this Formula](Hodge+star+operator#eq:HodgeSquareOnRiemannian) formulas at [[Hodge star operator]]) we have on mid-dimensional forms

$$
  \star \star B = (-1)^{(2k+1)(4k+3)} B
  = - B
  \,.
$$

Therefore it provides a [[complex structure]] on $\Omega^{2k+1}(\Sigma) \otimes \mathbb{C}$.

We see that the symplectic structure on the space of forms can equivalently be rewritten as

$$
  \begin{aligned}
    \int_X B_1 \wedge B_2
    & = - \int_X B_1 \wedge \star \star B_2 
  \end{aligned}
  \,.
$$

Here on the right now the [[Hodge star operator|Hodge inner product]] of $B_1$ with $\star B_2$ appears, which is invariant under applying the Hodge star to both arguments.

We then decompose $\Omega^{2k+1}(\Sigma)$ into the $\pm i$-[[eigenspace]]s of $\star$: say $B \in \Omega^{2k+1}(\Sigma)$ is  _imaginary self-dual_ if

$$
  \star B = i B
$$

and _imaginary anti-self-dual_ if

$$
  \star B = - i B
  \,.
$$

Then for imaginary self-dual $B_1$ and $B_2$ we find that the symplectic pairing is

$$
  \begin{aligned}
    (B_1, B_2)
    &=
    -i \int_X B_1 \wedge \star B_2
    \\
    & =
    -i \int_X (\star B_1) \wedge \star (\star B_2)
    \\
    & =    
    +i \int_X B_1 \wedge \star B_2
  \end{aligned} 
  \,.
$$

Therefore indeed the symplectic pairing vanishes on the self-dual and on the anti-selfdual forms. Evidently these provide a decomposition into [[Lagrangian subspaces]].

(See also at _[[Serre duality]]_.)


Therefore a [[state]] of higher Chern-Simons theory on $\Sigma$ may locally be thought of as a function of the self-dual forms on $\Sigma$. Under holography this is (therefore) identified with the [[correlator]] of a [[self-dual higher gauge theory]] on $\Sigma$.

### Partition function
 {#PartitionFunction}

By the above discussion (...) the [[partition function]] of self-dual higher gauge theory is given by (a multiple of) the unique [[holomorphic section]] of a [[square root]] of the [[line bundle]] classified by the [[secondary intersection pairing]]. ([Witten 96](#Witten96), [Hopkins-Singer](#HopkinsSinger)).

### Cohomological description

[[!include moduli of higher lines -- table]]

## Examples

### Chiral boson in 2d (on the string)
 {#ChiralBosonin2d}

For $k = 0$ the self-dual theory abelian is that of a [[scalar field]] $\phi$ on a real-2-dimensional surface $\Sigma$ such that $\mathbf{d}\phi$ is self-dual. For any [[complex structure]] on $\Sigma$, making it a [[complex torus]], this makes $\phi$ a "chiral" boson, in the sense of a chiral half of the $U(1)$-[[WZW model]].

Original discussion is due to [Srivastava 1989](#Srivastava89), [GGR 1992](#GGR92). A quick review as a warm-up for the higher dimensional case is in  [Witten 96, section 2](#Witten96). More discussion is in [GBMNV](#GBMNV) [Miao & Müller-Kirsten 2000](#MiaoMüller-Kirsten00), see also the references at _[[AdS3-CFT2 and CS-WZW correspondence]]_.


### Chiral 2-form in 6d (on the M5-brane)

The [[worldvolume]] theory of the [[M5-brane]], the
[[6d (2,0)-superconformal QFT]], contains a self-dual 2-form field. Its [AdS7-CFT6 holographic](AdS-CFT#AdS7CFT6) description by 7-dimensional Chern-Simons theory is due to ([Witten 96](#Witten96)).


[[!include relation between 5d Maxwell theory and self-dual 3-forms in 6d -- section]]


### RR-Fields in 10d (on the "9-brane")
 {#RRFieldsin10d}

The [[RR-field]] in [[type II string theory]] (by the idea of [[K-theory classification of D-brane charge]]) are meant to be self-dual as [[cocycles]] in ([[differential K-theory|differential]]) [[topological K-theory]] (cf. at *[[pre-metric electromagnetism]]* the *[section on RR-fields](pre-metric+electromagnetism#RRFieldInGravitationalBackground)*).

The proper discussion of these fields hence involves generalizing the above story from [[ordinary cohomology]] and [[principally polarized variety|principally polarized]] [[intermediate Jacobians]] to an analog in [[Whitehead-generalized cohomology]] such as [[topological K-theory]] and an appropriate generalized form of intermediate Jacobians (cf. *[[Hodge-filtered differential cohomology]]*).

(Of course one may, as a warmup, "approximate" K-theory classes on a 10-manifold by integral cohomology lifts of the degree-5 component of their [[Chern character]] and hence discuss that as abelian self-dual higher gauge theory in dimension 10. This is discussed in ([Witten 99, section 4](#Witten99))).

The relevant analog of the [[intermediate Jacobian]] for K-theory on a 10-manifold is naturally taken to be

$$
  K(X)\otimes_{\mathbb{Z}} \mathbb{R}/ K(X)
$$

(where the action is via the [[Chern character]]/realification $K \to K \otimes \mathbb{R}$).


This is proposed and discussed in ([Witten 99, section 4.3](#Witten99), [Moore-Witten 99, section 3](#MooreWitten99), [DMW 00, section 7.1](#MW00), [Belov-Moore 06b, section 5](#BelovMooreII), [MPS 11](#MSP11)): 

where for ordinary cohomology the ([[quadratic refinement]] of the) [[intersection product]] (= [[Deligne-Beilinson cup product]] followed by [[fiber integration in ordinary differential cohomology]]) provided the [[symplectic structure]]/[[polarized variety|polarization]] of the intermediate Jacobian, here it is tensoring of [[Dirac operators]] followed by [[fiber integration in differential K-theory]], hence the [[index of a Dirac operator|index]] map in K-theory.

See at _[intermediate Jacobian -- For complex K-theory](intermediate+Jacobian#ForComplexKTheory)_.


## Related concepts

[[!include square roots of line bundles - table]]

* [[non-Lagrangian field theory]]

* [[Perry-Schwarz action]]

* [[Kervaire invariant]]

* [[bosonization]]

* [[higher dimensional Chern-Simons theory]]

* [[holographic principle]], [[AdS-CFT]]

* [[dual graviton]]

## References

### General

Original articles on the general issue include

* {#HenneauxTeitelboim88} [[Marc Henneaux]], [[Claudio Teitelboim]], _Dynamics of chiral (self-dual) $p$-forms_, Physics Letters B **206** 4 (1988) 650-654 &lbrack;<a href="https://doi.org/10.1016/0370-2693(88)90712-5">doi:10.1016/0370-2693(88)90712-5</a>&rbrack;

* {#PastiSorokinTonin06} [[Paolo Pasti]], [[Dmitri Sorokin]], [[Mario Tonin]], _On Lorentz Invariant Actions for Chiral P-Forms_, Phys.Rev. D55 (1997) 6292-6298 ([arXiv:hep-th/9611100](https://arxiv.org/abs/hep-th/9611100))

* {#Witten99} [[Edward Witten]], _Duality Relations Among Topological Effects In String Theory_, JHEP 0005:031,2000 ([arXiv:hep-th/9912086](http://arxiv.org/abs/hep-th/9912086))

* {#BelovMooreI} Dmitriy Belov, [[Greg Moore]], _Holographic Action for the Self-Dual Field_ &lbrack;[arXiv:hep-th/0605038](http://arxiv.org/abs/hep-th/0605038)&rbrack;

Surveys include

* [[Greg Moore]], _A Minicourse on Generalized Abelian Gauge Theory, Self-Dual Theories, and Differential Cohomology_, Lectures at Simons Center for Geometry and Physics (2011) ([pdf](http://www.physics.rutgers.edu/~gmoore/SCGP-Minicourse.pdf))

* {#Szabo12} [[Richard Szabo]], _Quantization of Higher Abelian Gauge Theory in Generalized Differential Cohomology_ &lbrack;[arXiv:1209.2530](http://arxiv.org/abs/1209.2530)&rbrack;

An approach based on [[supergeometry]]:

* [[C. A. Cremonini]], [[Pietro Grassi]], _Self-Dual Forms in Supergeometry I: The Chiral Boson_ ([arXiv:2012.10243](https://arxiv.org/abs/2012.10243))


### For the M5-sigma model

The [[sigma-model]] description of the (single) M5-brane of [[Green-Schwarz action functional]]-type was found in covariant form in 

* {#BLNPST97} [[Igor Bandos]], [[Kurt Lechner]], [[Alexei Nurmagambetov]], [[Paolo Pasti]], [[Dmitri Sorokin]], [[Mario Tonin]], _Covariant Action for the Super-Five-Brane of M-Theory_, Phys. Rev. Lett. 78 (1997) 4332-4334 ([arXiv:hep-th/9701149](http://arxiv.org/abs/hep-th/9701149))

* {#PST97} [[Paolo Pasti]], [[Dmitri Sorokin]] and M. Tonin, _Covariant Action for a D=11 Five-Brane with the Chiral Field_, Phys. Lett. B398 (1997) 41 ([arXiv:hep-th/9701037](https://arxiv.org/abs/hep-th/9701037))

following

* [[Paul Townsend]], section 3.3 of _D-branes from M-branes_, Phys. Lett. B373 (1996) 68-75 ([arXiv:hep-th/9512062](https://arxiv.org/abs/hep-th/9512062))

  (which did not yet have the [[Hopf-Wess-Zumino term]])

and following the non-covariant form of the [[self-dual higher gauge field|self-duality mechanism]] ([[Perry-Schwarz action]]) of

* {#PerrySchwarz96} [[Malcolm Perry]], [[John Schwarz]], _Interacting Chiral Gauge Fields in Six Dimensions and Born-Infeld Theory_, Nucl. Phys. B489 (1997) 47-64 ([arXiv:hep-th/9611065](http://arxiv.org/abs/hep-th/9611065))

* {#Schwarz97} [[John Schwarz]], _Coupling a Self-Dual Tensor to Gravity in Six Dimensions_, Phys.Lett.B395:191-195,1997

* [[Mina Aganagic]], [[Jaemo Park]], Costin Popescu, [[John Schwarz]], _World-Volume Action of the M Theory Five-Brane_ ([arXiv:hep-th/9701166](http://arxiv.org/abs/hep-th/9701166))

Discussion in the [[superembedding approach]];

* {#HoweSezgin97} [[Paul S. Howe]], [[Ergin Sezgin]], _$D=11$, $p=5$_, Phys. Lett. B **394** (1997) 62-66 &lbrack;[arXiv:hep-th/9611008](https://arxiv.org/abs/hep-th/9611008), <a href="https://doi.org/10.1016/S0370-2693(96)01672-3">doi:10.1016/S0370-2693(96)01672-3</a>&rbrack;

* {#Sorokin99} [[Dmitri Sorokin]], Section 5.2 of _Superbranes and Superembeddings_, Phys. Rept. **329** (2000) 1-101 &lbrack;[arXiv:hep-th/9906142](http://arxiv.org/abs/hep-th/9906142)&rbrack;

Amplification that the resulting B-field on the M5-brane is *not naively* self-dual:

* {#HoweSezginWest97} [[Paul S. Howe]], [[Ergin Sezgin]], [[Peter C. West]], *The six-dimensional self-dual tensor*, Physics Letters B **400** 3–4 (1997) 255-259 &lbrack;<a href="https://doi.org/10.1016/S0370-2693(97)00365-1">doi:10.1016/S0370-2693(97)00365-1</a>&rbrack;


Discussion of the equivalence of these superficially different action functionals is in 

* [[Igor Bandos]], [[Kurt Lechner]], [[Alexei Nurmagambetov]], [[Paolo Pasti]], [[Dmitri Sorokin]], [[Mario Tonin]], _On the equivalence of different formulations of the M Theory five--brane_, Phys. Lett. B408 (1997) 135-141 ([arXiv:hep-th/9703127](http://arxiv.org/abs/hep-th/9703127))






### For ordinary $U(1)$-higher gauge fields / ordinary differential cohomology

Self-duality for higher abelian gauge fields (in [[ordinary differential cohomology]]):

Original reference on self-dual/chiral fields include

* [[Xavier Bekaert]], [[Marc Henneaux]], _Comments on Chiral $p$-Forms_,  Int. J. Theor. Phys. 38:1161-1172, 1999 ([arXiv:hep-th/9806062](http://arxiv.org/abs/hep-th/9806062))

* [[Mans Henningson]], [[Bengt Nilsson]], Per Salomonson, _Holomorphic factorization of correlation functions in (4k+2)-dimensional (2k)-form gauge theory_ ([arXiv:hep-th/9908107](http://arxiv.org/abs/hep-th/9908107))

* [[Mans Henningson]], _The quantum Hilbert space of a chiral two-form in $d = 5 + 1$ dimensions_ ([arxiv:hep-th/0111150](http://arxiv.org/abs/hep-th/0111150))

The chiral boson in 2d:

* {#Srivastava89} Prem P. Srivastava, *Quantization of self-dual field revisited*, Phys. Rev. Lett. **63** (1989) 2791 &lbrack;[doi:10.1103/PhysRevLett.63.2791](https://doi.org/10.1103/PhysRevLett.63.2791)&rbrack;

* {#GGR92} H. O. Girotti, M. Gomes, and V. O. Rivelles, *Chiral bosons through linear constraints*, Phys. Rev. D **45** (1992) R3329(R) &lbrack;[doi:10.1103/PhysRevD.45.R3329](https://doi.org/10.1103/PhysRevD.45.R3329)&rbrack;

* {#GBMNV} [[Luis Alvarez-Gaumé]], [[Jean-Benoit Bost]], [[Greg Moore]], Philip Nelson, [[Cumrun Vafa]], _Bosonization On Higher Genus Riemann Surfaces_, Commun. Math. Phys. 112 (1987) 503 &lbrack;[doi:10.1007/BF01218489](https://doi.org/10.1007/BF01218489), [pdf](https://core.ac.uk/download/pdf/76393468.pdf)&rbrack; 

* {#MiaoMüller-Kirsten00} Yan-Gang Miao and H. J. W. Müller-Kirsten, *Self-duality of various chiral boson actions*, Phys. Rev. D **62** (2000) 045014 &lbrack;[doi:10.1103/PhysRevD.62.045014](https://doi.org/10.1103/PhysRevD.62.045014)&rbrack;


A quick exposition of the basic idea is in

* [[Jacques Distler]], _Actions for self-dual gauge fields_ ([blog](http://golem.ph.utexas.edu/~distler/blog/archives/000809.html))


A precise formulation of the phenomenon in terms of [[ordinary differential cohomology]] and [[differential K-theory]]:

* [[Daniel Freed]], [[Greg Moore]], [[Graeme Segal]], *The Uncertainty of Fluxes*, Commun. Math. Phys. **271**  (2007) 247-274 &lbrack;[arXiv:hep-th/0605198](http://arxiv.org/abs/hep-th/0605198), [doi:10.1007/s00220-006-0181-3](https://doi.org/10.1007/s00220-006-0181-3)&rbrack;

* [[Daniel Freed]], [[Greg Moore]], [[Graeme Segal]], *Heisenberg Groups and Noncommutative Fluxes*,  Annals Phys. **322** (2007) 236-285 &lbrack;[arXiv:hep-th/0605200](http://arxiv.org/abs/hep-th/0605200), [doi:10.1016/j.aop.2006.07.014](https://doi.org/10.1016/j.aop.2006.07.014)&rbrack;

* {#BBSS15} [[Christian Becker]], [[Marco Benini]], [[Alexander Schenkel]], [[Richard Szabo]], _Abelian duality on globally hyperbolic spacetimes_, Commun. Math. Phys. **349** (2017) 361-392 &lbrack;[arXiv:1511.00316](https://arxiv.org/abs/1511.00316), [doi:10.1007/s00220-016-2669-9](https://doi.org/10.1007/s00220-016-2669-9)&rbrack;

The idea of describing self-dual higher gauge theory by [[holography]] with abelian [[higher dimensional Chern-Simons theory]] in one dimension higher originates in 

* {#Witten96} [[Edward Witten]], _Five-Brane Effective Action In M-Theory_, J. Geom. Phys. **22** (1997) 103-133 &lbrack;<a href="https://doi.org/10.1016/S0393-0440(97)80160-X">doi:10.1016/S0393-0440(97)80160-X</a>, [arXiv:hep-th/9610234](http://arxiv.org/abs/hep-th/9610234)&rbrack;
 
* [[Edward Witten]], _Duality Relations Among Topological Effects In String Theory_, JHEP 0005:031 (2000) &lbrack;[doi:10.1088/1126-6708/2000/05/031](https://doi.org/10.1088/1126-6708/2000/05/031), [arXiv:hep-th/9912086](http://arxiv.org/abs/hep-th/9912086)&rbrack;


Conceptual aspects of this are also discussed in section 6.2 of 

* S. L. Lyakhovich, [[A. A. Sharapov]], _Quantizing non-Lagrangian gauge theories: an augmentation method_, JHEP 0701 047 (2007) &lbrack;[arXiv:hep-th/0612086](http://arxiv.org/abs/hep-th/0612086)&rbrack;

Motivated by this the [[ordinary differential cohomology]] of self-dual fields had been discussed in 

* {#HopkinsSinger} [[Mike Hopkins]], [[Isadore Singer]], _[[Quadratic Functions in Geometry, Topology, and M-Theory]]_

Discussion of [[S-duality]] in 6d self-dual higher gauge theory via [[non-commutative geometry|non-commutative]]-deformation:

* {#MathaiSati14} [[Varghese Mathai]], [[Hisham Sati]], _Higher abelian gauge theory associated to gerbes on noncommutative deformed M5-branes and S-duality_, J. Geom. Phys. 92:240-251, 2015 ([arXiv:1404.2257](https://arxiv.org/abs/1404.2257))

 
Discussion of the [[conformal blocks]] and [[geometric quantization]] of self-dual higher gauge theories is in 

* [[Kiyonori Gomi]], _An analogue of the space of conformal blocks in $(4k+2)$-dimensions_ ([pdf](http://www.math.kyoto-u.ac.jp/~kgomi/papers/acb.pdf))


For the case of nonabelian self-dual 1-form gauge fields see the references at _[[Yang-Mills instanton]]_.

Another proposal for a Lagrangian for self-dual higher gauge fields, at the cost of an unusual kinds of decoupled [[auxiliary fields]]:

* {#Sen20} [[Ashoke Sen]], *Self-dual forms: Action, Hamiltonian and Compactification*,  Journal of Physics A: Mathematical and Theoretical, **53** 8 (2020) &lbrack;[arXiv:1903.12196](https://arxiv.org/abs/1903.12196), [doi:10.1088/1751-8121/ab5423](https://doi.org/10.1088/1751-8121/ab5423)&rbrack;

Enhancement to [[superspace]] (in [[D'Auria-Fre formulation of supergravity]]):

* [ACDGMNRT22](#ACDGMNRT22)

Further discussion:

* [[Neil Lambert]], _$(2,0)$ Lagrangian Structures_, Physics Letters B **798** (2019) 134948 &lbrack;[arXiv:1908.10752](https://arxiv.org/abs/1908.10752), [doi;10.1016/j.physletb.2019.134948](https://doi.org/10.1016/j.physletb.2019.134948)&rbrack;

* [[Pichet Vanichchapongjaroen]]: *Covariant M5-brane action with self-dual 3-form*, J. High Energ. Phys. **2021** 39 (2021) &lbrack;<a href="https://doi.org/10.1007/JHEP05(2021)039">doi:10.1007/JHEP05(2021)039</a>, [arXiv:2011.14384](https://arxiv.org/abs/2011.14384)&rbrack;
  > (attention to the non-linearity of the self-duality on M5)

* {#Hull23} [[Chris Hull]], *Covariant Action for Self-Dual $p$-Form Gauge Fields in General Spacetimes*, J. High Energ. Phys. **2024** 11 (2024) &lbrack;[arXiv:2307.04748](https://arxiv.org/abs/2307.04748), <a href="https://doi.org/10.1007/JHEP04(2024)011">doi:10.1007/JHEP04(2024)011</a>&rbrack;

* Sujiphat Janaun, Anajak Phonchantuek, Pichet Vanichchapongjaroen, *Nonlinear chiral forms in the Sen formulation* &lbrack;[arXiv:2404.05380](https://arxiv.org/abs/2404.05380)&rbrack;

* [[Dominik Rist]], [[Christian Saemann]], Miro van der Worp: *Towards an M5-Brane Model III: Self-Duality from Additional Trivial Fields*,  J. High Energ. Phys. **2021** 36 (2021) &lbrack;<a href=" https://doi.org/10.1007/JHEP06(2021)036">doi:10.1007/JHEP06(2021)036</a>, [arXiv:2012.09253](https://arxiv.org/abs/2012.09253)&rbrack;

* {#ACDGMNRT22}  [[Laura Andrianopoli]], [[C. A. Cremonini]], [[Riccardo D'Auria]], [[Pietro A. Grassi]], [[Riccardo Matrecano]], [[Ruggero Noris]], [[Lucrezia Ravera]], [[Mario Trigiante]], *M5-brane in the superspace approach*, Phys. Rev. D **106** 2 (2022) 026010 &lbrack;[arXiv:2206.06388](https://arxiv.org/abs/2206.06388), [doi:10.1103/PhysRevD.106.026010](https://doi.org/10.1103/PhysRevD.106.026010)&rbrack;
  > (lifted to [[superspace]] in the [[D'Auria-Fré-Regge formulation of supergravity]])

* [[Chris Hull]], [[Neil Lambert]]: *Quantising Chiral Bosons On Riemann Surfaces* &lbrack;[arXiv:2508.02865](https://arxiv.org/abs/2508.02865)&rbrack;

* Aviral Aggarwal, Subhroneel Chakrabarti, Madhusudhan Raman: *Monopoles, Clarified* &lbrack;[arXiv:2504.16673](https://arxiv.org/abs/2504.16673)&rbrack;
  > (in relation to [[magnetic monopoles]])

* Jessica Hutomo, [[Kurt Lechner]], [[Dmitri P. Sorokin]]: *On non-linear chiral 4-form theories in $D=10$* &lbrack;[arXiv:2509.14351](https://arxiv.org/abs/2509.14351)&rbrack;



### For RR-fields / differential K-theory

[[!include self-duality for pregeometric RR-fields -- references]]


### For the 11d supergravity C-field


[[!include self-duality for pregeometric C-field -- references]]

 



[[!redirects self-dual higher gauge theories]]

[[!redirects higher self-dual gauge theory]]
[[!redirects higher self-dual gauge theories]]

[[!redirects self-dual higher gauge field]]
[[!redirects self-dual higher gauge fields]]

[[!redirects higher self-dual gauge field]]
[[!redirects higher self-dual gauge field]]

[[!redirects self-dual gauge theory]]
[[!redirects self-dual gauge theories]]

[[!redirects self-dual field theory]]



[[!redirects chiral boson]]
[[!redirects chiral bosons]]

