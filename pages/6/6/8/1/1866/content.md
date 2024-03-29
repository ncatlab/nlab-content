
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
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


##  Idea 

The _RR field_ or _Ramond--Ramond field_ is a [[gauge theory|gauge field]] appearing in  [[supergravity|10-dimensional type II supergravity]].

Mathematically the RR field on a space $X$ is a [[cocycle]] in [[differential K-theory]] -- or rather, in full generality, in [[twisted differential K-theory|twisted differential]] [[KR-theory]] subject to a [[self-dual higher gauge field]] constrained encoded by a quadratic form defining an [[11-dimensional Chern-Simons theory]] on twisted differential KR cocycles.

Accordingly, the [[field strength]] of the RR field, i.e. the image of the [[differential cohomology|differential K-cocycle]] in deRham cohomology, is an inhomogeneous even or odd differential form


* in [[type IIA string theory]]
  $$
    F_{RR} = R_0 + R_2 + \cdots
  $$

* in [[type IIB string theory]]
  $$
    F_{RR} = R_1 + R_3 + \cdots
  $$

The components of this are sometimes called the RR forms. 

In the presence of a nontrivial [[Kalb–Ramond field]] the RR field is [[twisted cohomology|twisted]]: a cocycle in the corresponding [[twisted K-theory]].

Moreover, the RR field is constrained to be a [[self-dual higher gauge theory|self-dual]] differential K-cocycle in a suitable sense.

[[!include electric-magnetic duality -- table]]

The RR field derives its name from the way it shows up when the [[supergravity]] theory in question is derived as an effective background theory in [[string theory]]. From the [[sigma-model]] perspective of the string the RR field is the condensate of fermionic 0-mode excitations of the type II superstring for a particular choice of boundary conditons called the _Ramond_ boundary condititions. Since these boundary conditions have to be chosen for _two_ spinor components, the name appears twice. 

## Related concepts

* [[RR-field tadpole]]

* [[D-brane charge]]

* [[Hanany-Witten effect]]

* [[K-theory classification of D-brane charge]]

  * [[differential K-theory]]

  * [[KK-theory]]

[[!include table of branes]]

## References 

### General

Early discussion in relation to [[D-branes]]:

* [[Joseph Polchinski]], *Dirichlet-Branes and Ramond-Ramond Charges*, Phys. Rev. Lett. **75** (1995) 4724-4727 &lbrack;[arXiv:hep-th/9510017](https://arxiv.org/abs/hep-th/9510017), [doi:10.1103/PhysRevLett.75.4724](https://doi.org/10.1103/PhysRevLett.75.4724)&rbrack;

Review in the context of the [[K-theory classification of D-brane charge]]:

* {#Freed00} [[Daniel Freed]], example 2.10 in: *Dirac charge quantization and generalized differential cohomology_*, Surveys in Differential Geometry, Int. Press, Somerville (2000) 129-194  &lbrack;[arXiv:hep-th/0011220](http://arxiv.org/abs/hep-th/0011220), [doi:10.4310/SDG.2002.v7.n1.a6](https://dx.doi.org/10.4310/SDG.2002.v7.n1.a6), [spire:537392](https://inspirehep.net/literature/537392)&rbrack;

Discussion of the [[NSR-string|NSR]] [[string scattering amplitudes|string perturbation theory]] in RR-field [[background field|background]]:

* {#BerensteinLeigh99} [[David Berenstein]], [[Robert Leigh]], _Superstring Perturbation Theory and Ramond-Ramond Backgrounds_, Phys. Rev. D **60** (1999) 106002 &lbrack;[arXiv:hep-th/9904104](https://arxiv.org/abs/hep-th/9904104)&rbrack;


### Self-duality and quadratic form
 {#ReferencesSelfDuality}

[[self-duality for pregeometric RR-fields -- references]]

The [[self-dual higher gauge field]] nature (see there for more) in terms of a [[quadratic form]] on [[differential K-theory]] is discussed originally around

* {#MooreWitten99} [[Gregory Moore]], [[Edward Witten]], _Self-Duality, Ramond-Ramond Fields, and K-Theory_, JHEP 0005:032,2000 ([arXiv:hep-th/9912279](http://arxiv.org/abs/hep-th/9912279))

and ([Freed 00](#Freed00)) for [[type I superstring theory]], and for [[type II superstring theory]] in 

* {#Witten00} [[Edward Witten]], _Duality Relations Among Topological Effects In String Theory_, JHEP 0005:031 (2000) &lbrack;[arXiv:hep-th/9912086](http://arxiv.org/abs/hep-th/9912086), [doi:10.1088/1126-6708/2000/05/032](https://doi.org/10.1088/1126-6708/2000/05/032)&rbrack;

* {#FreedHopkins00} [[Daniel Freed]], [[Michael Hopkins]], *On Ramond-Ramond fields and K-theory*, JHEP 0005 (2000) 044 &lbrack;[arXiv:hep-th/0002027](http://arxiv.org/abs/hep-th/0002027)&rbrack;

* {#FMW00} [[Duiliu-Emanuel Diaconescu]], [[Gregory Moore]], [[Edward Witten]], *$E_8$ Gauge Theory, and a Derivation of K-Theory from M-Theory*, Adv. Theor. Math. Phys. **6** (2003) 1031-1134 &lbrack;[arXiv:hep-th/0005090](http://arxiv.org/abs/hep-th/0005090)&rbrack;, summarised in _A Derivation of K-Theory from M-Theory_ &lbrack;[arXiv:hep-th/0005091](http://arxiv.org/abs/hep-th/0005091)&rbrack;

with more refined discussion in [[twisted differential K-theory|twisted differential]] [[KR-theory]] in

* {#DFM09} [[Jacques Distler]], [[Dan Freed]], [[Greg Moore]], _Orientifold Pr&#233;cis_ in: [[Hisham Sati]], [[Urs Schreiber]] (eds.) _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_, Proceedings of Symposia in Pure Mathematics, AMS (2011) &lbrack;[arXiv:0906.0795](http://arxiv.org/abs/0906.0795), [slides](http://www.ma.utexas.edu/users/dafr/bilbao.pdf)&rbrack;

See at _[[orientifold]]_ for more on this. The relation to [[11d Chern-Simons theory]] is made manifest in

* {#BelovMooreII} Dmitriy Belov, [[Greg Moore]], _Type II Actions from 11-Dimensional Chern-Simons Theories_ &lbrack;[arXiv:hep-th/0611020](http://arxiv.org/abs/hep-th/0611020)&rbrack;

Review is in 

* {#Szabo12} [[Richard Szabo]], section 3.6 and 4.6 of: _Quantization of Higher Abelian Gauge Theory in Generalized Differential Cohomology_ &lbrack;[arXiv:1209.2530](http://arxiv.org/abs/1209.2530)&rbrack;

Discussion of [[Lagrangian densities]] for [[type II supergravity]] making the nature of the [[pregeometric RR-fields]] and their [[self-dual higher gauge theory|self-duality]] manifest:

* [[Gianguido Dall'Agata]], [[Kurt Lechner]], [[Mario Tonin]], *$D=10$, $N=IIB$ Supergravity: Lorentz-invariant actions and duality*, JHEP 9807:017 (1998) &lbrack;[arXiv:hep-th/9806140](https://arxiv.org/abs/hep-th/9806140), [doi:10.1088/1126-6708/1998/07/017](https://doi.org/10.1088/1126-6708/1998/07/017)&rbrack;

* [[Eric Bergshoeff]], [[Renata Kallosh]], [[Tomas Ortin]], [[Diederik Roest]], [[Antoine Van Proeyen]], *New Formulations of D=10 Supersymmetry and D8-O8 Domain Walls*, Class. Quant. Grav. **18** (2001) 3359-3382 &lbrack;[arXiv:hep-th/0103233](https://arxiv.org/abs/hep-th/0103233), [doi:10.1088/0264-9381/18/17/303](https://doi.org/10.1088/0264-9381/18/17/303)&rbrack;

* [[Karapet Mkrtchyan]], [[Fridrich Valach]], *Democratic actions for type II supergravities*, Phys.Rev.D **107** 6 (2023) 066027 &lbrack;[arXiv:2207.00626](https://arxiv.org/abs/2207.00626), [doi:10.1103/PhysRevD.107.066027](https://doi.org/10.1103/PhysRevD.107.066027)&rbrack;


### Irrational RR-charge
 {#IrrationalRRCharge}

An argument that RR-charge may occur in [[irrational number|irrational]] ratios is due to

* {#BDS00} [[Constantin Bachas]], [[Michael Douglas]], [[Christoph Schweigert]], around (2.8) of _Flux Stabilization of D-branes_, JHEP 0005:048, 2000 ([arXiv:hep-th/0003037](https://arxiv.org/abs/hep-th/0003037))

In a sequence of followup articles, authors found this problematic and tried to make sense of it:

* [[Washington Taylor]], _D2-branes in B fields_, JHEP 0007 (2000) 039 ([arXiv:hep-th/0004141](https://arxiv.org/abs/hep-th/0004141))

> In this article it was argued that the D0-brane charge arising from the integral over the D2-brane of the pullback of the B field is cancelled by the bulk contributions, but in this calculation it was implicitly assumed that the gauge field $C^{(1)}$ is constant. (from [Zhou 01](#Zhou01))

* Peter Rajan, _D2-brane RR-charge on $SU(2)$_, Phys.Lett. B533 (2002) 307-312 ([arXiv:hep-th/0111245](https://arxiv.org/abs/hep-th/0111245))

* {#Zhou01} Jian-Ge Zhou, _D-branes in B Fields_, Nucl.Phys. B607 (2001) 237-246 ([arXiv:hep-th/0102178](https://arxiv.org/abs/hep-th/0102178))

Observation that this paradox is resolved under [[Hypothesis H]], at least for [[fractional D-branes]]:

* [[Simon Burton]], [[Hisham Sati]], [[Urs Schreiber]], *[[schreiber:Lift of fractional D-brane charge to equivariant Cohomotopy theory|Lift of fractional D-brane charge to equivariant Cohomotopy theory]]*, J Geom  Phys **161** (2021) 104034 ([doi:10.1016/j.geomphys.2020.104034](https://doi.org/10.1016/j.geomphys.2020.104034), [arXiv:1812.09679]([arXiv:1812.09679](https://arxiv.org/abs/1812.09679))




[[!redirects RR fields]]

[[!redirects RR-field]]
[[!redirects RR-fields]]

[[!redirects Ramond-Ramond field]]
[[!redirects Ramond–Ramond field]]
[[!redirects Ramond--Ramond field]]

[[!redirects Ramond-Ramond fields]]
[[!redirects Ramond–Ramond fields]]
[[!redirects Ramond--Ramond fields]]


[[!redirects RR-charge]]