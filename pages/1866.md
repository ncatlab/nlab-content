
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

* [[K-theory classification of topological D-brane charge]]

  * [[differential K-theory]]

  * [[KK-theory]]

[[!include table of branes]]

## References 

### General

For a quick review see for instance

* {#Freed00} [[Daniel Freed]], example 2.10 _Dirac charge quantization and generalized differential cohomology_ ([arXiv](http://arxiv.org/abs/hep-th/0011220))

Discussion of the [[NSR-string|NSR]] [[string perturbation theory]] in RR-field background is in 

* {#BerensteinLeigh99} [[David Berenstein]], Robert Leigh, _Superstring Perturbation Theory and Ramond-Ramond Backgrounds_, Phys. Rev. D 60, 106002 (1999) ([arXiv:hep-th/9904104](https://arxiv.org/abs/hep-th/9904104))

### Self-duality and quadratic form
 {#ReferencesSelfDuality}

The [[self-dual higher gauge field]] nature (see there for more) in terms of a [[quadratic form]] on [[differential K-theory]] is discussed originally around

* {#MooreWitten99} [[Gregory Moore]], [[Edward Witten]], _Self-Duality, Ramond-Ramond Fields, and K-Theory_, JHEP 0005:032,2000 ([arXiv:hep-th/9912279](http://arxiv.org/abs/hep-th/9912279))

and ([Freed 00](#Freed00)) for [[type I superstring theory]], and for [[type II superstring theory]] in 

* {#Wittem} [[Edward Witten]], _Duality Relations Among Topological Effects In String Theory_, JHEP 0005:031,2000 ([arXiv:hep-th/9912086](http://arxiv.org/abs/hep-th/9912086))

* {#FreedHopkins00} [[Daniel Freed]], [[Michael Hopkins]], _On Ramond-Ramond fields and K-theory_, JHEP 0005 (2000) 044 ([arXiv:hep-th/0002027](http://arxiv.org/abs/hep-th/0002027))

* {#FMW00} D. Diaconescu, [[Gregory Moore]], [[Edward Witten]], _$E_8$ Gauge Theory, and a Derivation of K-Theory from M-Theory_, Adv.Theor.Math.Phys.6:1031-1134,2003 ([arXiv:hep-th/0005090](http://arxiv.org/abs/hep-th/0005090)), summarised in _A Derivation of K-Theory from M-Theory_ ([arXiv:hep-th/0005091](http://arxiv.org/abs/hep-th/0005091))

with more refined discussion in [[twisted differential K-theory|twisted differential]] [[KR-theory]] in

* {#DFM09} [[Jacques Distler]], [[Dan Freed]], [[Greg Moore]], _Orientifold Pr&#233;cis_ in: [[Hisham Sati]], [[Urs Schreiber]] (eds.) _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_ Proceedings of Symposia in Pure Mathematics, AMS (2011) ([arXiv:0906.0795](http://arxiv.org/abs/0906.0795), [slides](http://www.ma.utexas.edu/users/dafr/bilbao.pdf))

See at _[[orientifold]]_ for more on this. The relation to [[11d Chern-Simons theory]] is made manifest in

* {#BelovMooreII} Dmitriy Belov, [[Greg Moore]], _Type II Actions from 11-Dimensional Chern-Simons Theories_ ([arXiv:hep-th/0611020](http://arxiv.org/abs/hep-th/0611020))

Review is in 

* {#Szabo12} [[Richard Szabo]], section 3.6 and 4.6 of _Quantization of Higher Abelian Gauge Theory in Generalized Differential Cohomology_ ([arXiv:1209.2530](http://arxiv.org/abs/1209.2530))

### Irrational RR-charge
 {#IrrationalRRCharge}

An argument that RR-charge may occur in [[irrational number|irrational]] ratios is due to

* {#BDS00} [[Constantin Bachas]], [[Michael Douglas]], [[Christoph Schweigert]], around (2.8) of _Flux Stabilization of D-branes_, JHEP 0005:048, 2000 ([arXiv:hep-th/0003037](https://arxiv.org/abs/hep-th/0003037))

In a sequence of followup articles, authors found this problematic and tried to make sense of it:

* [[Washington Taylor]], _D2-branes in B fields_, JHEP 0007 (2000) 039 ([arXiv:hep-th/0004141](https://arxiv.org/abs/hep-th/0004141))

> In this article it was argued that the D0-brane charge arising from the integral over the D2-brane of the pullback of the B field is cancelled by the bulk contributions, but in this calculation it was implicitly assumed that the gauge field $C^{(1)}$ is constant. (from [Zhou 01](#Zhou01))

* Peter Rajan, _D2-brane RR-charge on $SU(2)$_, Phys.Lett. B533 (2002) 307-312 ([arXiv:hep-th/0111245](https://arxiv.org/abs/hep-th/0111245))

* {#Zhou01} Jian-Ge Zhou, _D-branes in B Fields_, Nucl.Phys. B607 (2001) 237-246 ([arXiv:hep-th/0102178](https://arxiv.org/abs/hep-th/0102178))

Observation that this paradox is resolved under [[schreiber:Hypothesis H]], at least for [[fractional D-branes]]:

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