
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
#### Differential cohomology
+-- {: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

Confinement (e.g [Espiru 94](#Espiru94)) is the (expected) phenomenon in [[Yang-Mills theory]]/[[QCD]] that [[quark]]-excitations must form [[bound state|bound states]] which are neutral under the color charge -- such as the [[hadron|hadrons]] ([[proton|protons]], [[neutron|neutrons]]) and [[meson|mesons]].

Confinement is a [[non-perturbative effect]] (e.g [Espiru 94](#Espiru94)).

## Open problem
 {#OpenProblem}

While [[experiment]] as well as [[lattice gauge theory]]-computer simulation clearly show that confinement takes place, a real theoretical understanding is missing (see also at _[[mass gap problem]]_). Here are quotes from some references highlighting the open problem:

* {#Kutschke96} Robert Kutschke, section 3.1 _Heavy flavour spectroscopy_, in D. Bugg (ed.), _Hadron Spectroscopy and the Confinement Problem_, Proceedings of a NATO Advanced Study Institute, Plenum Press 1996  ([doi:10.1007/978-1-4613-0375-6](https://www.springer.com/cn/book/9780306453038))

> While it is generally believed that QCD is the correct fundamental theory of the strong interactions there are, as yet, no practical means to produce full QCD calculations of hadron masses and their decay widths.

* Jeff Greensite, _An Introduction to the Confinement Problem_, Lecture Notes in Physics, Volume 821, 2011 ([doi:10.1007/978-3-642-14382-3](https://link.springer.com/book/10.1007%2F978-3-642-14382-3))

> Because of the great importance of the standard model, and the central role it plays in our understanding of particle physics, it is unfortunate that, in one very important respect, we don’t really understand how it works. The problem lies in the sector dealing with the interactions of quarks and gluons, the sector known as Quantum Chromodynamics or QCD. We simply do not know for sure why quarks and gluons, which are the fundamental fields of the theory, don’t show up in the actual spectrum of the theory, as asymptotic particle states. There is wide agreement  about  what  must  be  happening  in  high  energy  particle  collisions:  the  formation of color electric flux tubes among quarks and antiquarks, and the eventual fragmentation of those flux tubes into mesons and baryons, rather than free quarks and gluons. But there is no general agreement about why this is happening, and that limitation exposes our general ignorance about the workings of non-abelian gauge theories in general, and QCD in particular, at large distance scales.

* {#Brambilla14} Brambilla et al.. _QCD and strongly coupled gauge theories: challenges and perspectives_, Eur Phys J C Part Fields. 2014; 74(10): 2981 ([doi:10.1140/epjc/s10052-014-2981-5](https://link.springer.com/article/10.1140%2Fepjc%2Fs10052-014-2981-5))

>  The success of the technique does not remove the challenge of understanding the non-perturbative aspects of the theory. The two aspects are
deeply intertwined. The Lagrangian of QCD is written in terms of quark and gluon degrees of freedom which become apparent at large energy but remain hidden inside hadrons in the low-energy regime. This confinement property is related to the increase of $\alpha_s$ at low energy, but it has never been
demonstrated analytically. 

> We have clear indications of the confinement of quarks into hadrons from both experiments and lattice QCD. Computations of the heavy quark–antiquark potential, for example, display a linear behavior in the quark–antiquark distance, which cannot be obtained in pure perturbation theory. Indeed the two main characteristics of QCD: confinement and the appearance of nearly massless pseudoscalar mesons, emergent from the spontaneous breaking of chiral symmetry, are non-perturbative phenomena whose precise understanding continues to be a target of research. 

> Even in the simpler case of gluodynamics in the absence of quarks, we do not have a precise understanding of how a gap in the spectrum is formed and the glueball spectrum is generated.


* J J Cobos-Martínez, _Non-perturbative QCD and hadron physics_ 2016  J. Phys.: Conf. Ser. 761 012036 ([doi:10.1088/1742-6596/761/1/012036](http://iopscience.iop.org/article/10.1088/1742-6596/761/1/012036))

> $[\cdots]$ the QCD Lagrangian does not by itself explain the data on strongly interacting matter, and it is not clear how the observed bound states, the hadrons, and their properties arise from QCD. Neither confinement  nor dynamical chiral symmetry breaking (DCSB) is apparent in QCD’s lagrangian, yet they play a dominant role in determining the observable characteristics of QCD. The physics of strongly interacting matter is governed by emergent phenomena such as these, which can only be elucidated through the use of non-perturbative methods in QCD [4, 5, 6, 7]

* {#INFN15} [Istituto Nazionale di Fisica Nucleare](https://web.infn.it/csn1/index.php/en/), _What Next: White Paper of the INFN-CSN1_ _Proposal for a long term strategy for accelerator based experiments_, Frascati Phys.Ser. 60 (2015) 1-302 (2015-05-29) ([spire:1374543](http://inspirehep.net/record/1374543/), [pdf](http://www.lnf.infn.it/sis/frascatiseries/Volume60/Volume60.pdf) ) chapter 7: _Hadron Physics and non-perturbative QCD
_  ([pdf](http://www.infn.it/csn1/White_paper_documents/NPQCD.pdf))

> Experimentally, there is a large number of facts that lack a detailed qualitative and quantitative explanation. The most spectacular manifestation of our lack of theoretical understanding of QCD is the failure to observe the elementary degrees of freedom, quarks and gluons, as free asymptotic states (color con- finement) and the occurrence, instead, of families of massive mesons and baryons (hadrons) that form approximately linear Regge trajectories in the mass squared. The internal, partonic structure of hadrons, and nucleons in particular, is still largely mysterious. Since protons and neutrons form almost all the visible matter of the Universe, it is of basic importance to explore their static and dynamical properties in terms of quarks and gluons interacting according to QCD dynamics. 


## Potential solutions

### Via Calorons
 {#ViaCalorons}

It has been argued that, after [[Wick rotation]], confinement may be derived from the behaviour of [[instantons]] ([Schaefer-Shuryak 96, section III D](#SchaeferShuryak96)), or rather their [[thermal field theory|positive temperature]]-incarnations as _[[calorons]]_, [Greensite 11, section 8.5](#Greensite11):

> it is natural to wonder if [[confinement]] could be derived from some [[semiclassical approximation|semiclassical]] treatment of [[Yang–Mills theory]] based on the [[instanton]] solutions of [[nonabelian group|non-abelian]] [[gauge theories]]. The [[BPST instanton|standard]] [[instantons]], introduced by Belavin et al. ([40](BPTS-instanton#BelavinPolyakovSchwartzTyupkin75)), do not seem to work; their [[field strengths]] fall off too rapidly to produce the desired  magnetic  disorder  in  the  vacuum.  

> In  recent years, however, it has been realized that instanton solutions at [[thermal field theory|finite temperature]], known as _[[calorons]]_, might do the job. These caloron solutions were introduced independently by Kraan and van Baal ([41](caloron#KraanVanBaal98), [42](caloron#KraanVanBaal98b)) and Lee and Lu ([43](caloron#LeeLu98)) (KvBLL), and they have the remarkable property of containing [[monopole]] constituents which may, depending on the type of [[caloron]], be widely separated.

> $[...]$

> The [[caloron]] idea is probably the most promising current version of [[monopole]] [[confinement]] in pure non-abelian gauge theories, but it is  basically  (in certain [[gauge fixing|gauges]]) a superposition of [[monopoles]] with spherically  symmetric abelian fields, and this leads to the same questions raised in connection with monopole Coulomb gases.

See also at _[[glueball]]_.

### Via AdS/QCD correspondence

For the moment see at _[[AdS/QCD correspondence]]_.

### In $\mathcal{N}=2$ super Yang-Mills theory via Seiberg-Witten theory
  {#InN2SYM}

While confinement in plain [[Yang-Mills theory]] is still waiting for mathematical formalization and [[proof]] (see [Jaffe-Witten](#JaffeWitten)), there is a variant of [[Yang-Mills theory]] with more [[symmetry]], namely [[supersymmetry]], where the phenomenon has been giving a decent argument, namely in [[N=2 D=4 super Yang-Mills theory]] ([Seiberg-Witten 94](#SeibergWitten94)). 

Also a strategy for a proof for [[N=1 D=4 super Yang-Mills theory]] has been proposed, see [below](#ForN1SYMViaMTheoryOnG2Manifolds).

### In $\mathcal{N} = 1$ super Yang-Mills theory via M-theory on $G_2$-manifolds
 {#ForN1SYMViaMTheoryOnG2Manifolds}

An idea for a strategy towards a proof of confinement in [[N=1 D=4 super Yang-Mills theory]] via two different but conjecturally equivalent realizations as [[M-theory on G2-manifolds]] has been given in [Atiyah-Witten 01, section 6](#AtiyahWitten01), review is in [Acharya-Gukov 04, section 5.3](#AcharyaGukov04).

The idea here is to consider a [[KK-compactification]] of [[M-theory]] on [[fibers]] which are [[G2-manifolds]] that locally around a special point 
are of the form

$$
  X_{1,\Gamma} 
  \;\coloneqq\;
  \big( S^3 / \Gamma \big) \times Cone\big(S^3\big)
  \phantom{AA}
  \text{or}
  \phantom{AA}
  X_{2,\Gamma} 
  \;\coloneqq\;
  S^3 \times Cone\big(S^3/\Gamma\big)
$$

where 

* $\Gamma$ is a [[finite subgroup of SU(2)]] that [[action|acts]] canonically by left-multiplication on $S^3 \simeq $ [[SU(2)]];

* $Cone(\cdots)$ denotes the [[metric cone]] construction.

This means that $X_{1,\Gamma}$ is a [[smooth manifold]], but $X_{2,\Gamma}$, as soon as $\Gamma$ is not the [[trivial group]], $\Gamma \neq 1$, is an [[orbifold]] with an [[ADE singularity]].

Now the lore of [[M-theory on G2-manifolds]] predicts that [[KK-compactification]]

1.  on $X_{1,\Gamma}$ yields a 4d theory without massless fields (since there are no massless modes on the [[covering space]] $S^3$ of $X_{1,\Gamma}$)

1. on the [[ADE-singularity]] $X_{2,\Gamma}$ yields [[non-abelian group|non-abelian]] [[Yang-Mills theory]] in 4d coupled to [[chiral fermions]].

So in the first case a [[mass gap]] is manifest, while non-abelian gauge theory is not visible, while in the second case it is the other way around.

But if there were an argument that [[M-theory on G2-manifolds]] is in fact equivalent for compactification both on $X_{1,\Gamma}$ and on $X_{2,\Gamma}$. To the extent that this is true, it looks like an argument that could demonstrate confinement in non-abelian 4d gauge theory.

This approach is suggested in [Atiyah-Witten 01, pages 84-85](#AtiyahWitten01). An argument that this equivalence is indeed the case is then provided in sections 6.1-6.4, based on an argument in [Atiyah-Maldacena-Vafa 00](#AtiyahMaldacenaVafa00) 

## Related concepts

* [[asymptotic freedom]]

* [[quantization of Yang-Mills theory]]

* [[proton spin crisis]]

## References


### In Yang-Mills theory
 {#ReferencesInYangMillsTheory}

#### General

* {#Wilson74} [[Kenneth Wilson]],  _Confinement of quarks, Phys. Rev. D10, 2445, 1974 ([doi:10.1103/PhysRevD.10.2445](https://doi.org/10.1103/PhysRevD.10.2445))


Textbook accounts include

* {#Greensite11} Jeff Greensite, _An Introduction to the Confinement Problem_, Lecture Notes in Physics, Volume 821, 2011 ([doi:10.1007/978-3-642-14382-3](https://link.springer.com/book/10.1007%2F978-3-642-14382-3))

* Robert Iengo, section 9.1 of _Quantum Field Theory_ ([pdf](http://iopscience.iop.org/chapter/978-1-6432-7053-1/bk978-1-6432-7053-1ch9.pdf))

* D. Bugg (ed.), _Hadron Spectroscopy and the Confinement Problem_, Proceedings of a NATO Advanced Study Institute, Plenum Press 1996  ([doi:10.1007/978-1-4613-0375-6](https://www.springer.com/cn/book/9780306453038))


Introductions and surveys include

* Yuri L. Dokshitzer, around section 1.2 of _QCD Phenomenology_ ([arXiv:hep-ph/0306287](https://arxiv.org/abs/hep-ph/0306287))

* {#Espiru94} D. Espriu, section 7 of _Perturbative QCD_ ([arXiv:hep-ph/9410287](http://arxiv.org/abs/hep-ph/9410287))

* Erhard Seiler, _The Confinement Problem_ ([pdf](http://physik.uni-graz.at/~dk-user/talks/Seiler20081113-14.pdf))

* Wikipedia, _[Color confinement](http://en.wikipedia.org/wiki/Color_confinement)_

Discussion includes

* _[What is Strongly-Coupled Quantum Chromodynamics?](https://ensnaredinvacuum.wordpress.com/2015/02/11/what-is-strongly-coupled-quantum-chromodynamics/)_

A formulation of confinement as an open problem of mathematical physics, together with many references, is in 

* {#JaffeWitten} [[Arthur Jaffe]], [[Edward Witten]], _Quantum Yang-Mills theory_ ([pdf](http://www.claymath.org/millennium/Yang-Mills_Theory/yangmills.pdf))
 

Other technical reviews include

* G. M. Prosperi, _Confinement and bound states in QCD_ ([arXiv:hep-ph/0202186](http://arxiv.org/abs/hep-ph/0202186))

#### Via monopole condensation
 {#ViaMonopoleCondensation}

An original suggestion that confinement in [[Yang-Mills theory]] may be understood via [[monopole]] [[condensate|condensation]] as a dual [[Meissner effect]] is due to 

* {#Hooft75} [[Gerard 't Hooft]], in Proceed.of the Europ.Phys.Soc. 1975, ed.by A.Zichichi (Editrice Compositori, Bologna, 1976), p.1225.

* {#Mandelstam76} S. Mandelstam, Phys.Rep. 23C (1976) 145;

(That this is indeed the case has not yet been demonstarted for plain Yang-Mills theory, but it was later shown for [[N=2 D=4 super Yang-Mills theory]] in ([Seiberg-Witten 94](#SeibergWitten94)). What this does or does not imply for the case of [[QCD]] is discussed in ([Yung 00](#Yung00)) ).


The relation to [[QCD instantons]]/[[monopole|monopoles]] in the [[QCD vacuum]] is discussed in  

* {#SchaeferShuryak96} T. Schaefer, [[Edward Shuryak]], section III D of _Instantons in QCD_, Rev. Mod. Phys.70:323-426,1998 ([arXiv:hep-ph/9610451](http://arxiv.org/abs/hep-ph/9610451))

and analogously (at [[thermal field theory|positive temperature]]) relation to _[[calorons]]_:

* [Greensite 11, section 8.5](#Greensite11)

* P. Gerhold, E.-M. Ilgenfritz, M. Müller-Preussker, _An $SU(2)$ KvBLL caloron gas model and confinement_, Nucl.Phys.B760:1-37, 2007 ([arXiv:hep-ph/0607315](https://arxiv.org/abs/hep-ph/0607315))

* {#LarsenShuryak14}  Rasmus Larsen, [[Edward Shuryak]], _Classical interactions of the instanton-dyons with antidyons_, Nucl. Phys. A **950**, 110 (2016) ([arXiv:1408.6563](https://arxiv.org/abs/1408.6563))

* {#LarsenShuryak15} Rasmus Larsen, [[Edward Shuryak]], _Interacting Ensemble of the Instanton-dyons and Deconfinement Phase Transition in the SU(2) Gauge Theory_, Phys. Rev. D 92, 094022, 2015 ([arXiv:1504.03341](https://arxiv.org/abs/1504.03341))

 

For further developments see

* _Dimensional Transmutation by Monopole Condensation in QCD_ ([arXiv:1206.6936](http://arxiv.org/abs/1206.6936))

### Interacting field vacuum

Discussion of confinement as a result of the [[interacting vacuum]] includes

* {#Rafelski90} [[Johann Rafelski]], _Vacuum structure -- An Essay_, in pages 1-29 of H. Fried, Berndt Müller (eds.) _Vacuum Structure in Intense Fields_, Plenum Press 1990 ([GBooks](https://books.google.de/books?id=5uXcBwAAQBAJ&pg=PA14&lpg=PA14&dq=confinement+%22interacting+vacuum%22&source=bl&ots=xPGYJ-JOc-&sig=AoYbqWQeNRMg6hMSRZjJ3nzq8B0&hl=en&sa=X&ved=0ahUKEwjIgK68-tnYAhVCESwKHThMDykQ6AEIKTAA#v=onepage&q=confinement%20%22interacting%20vacuum%22&f=false))

See also

* {#Simonov18} Yu. A. Simonov, _What is the confinement mechanism in QCD?_ ([arXiv:1804.08946](https://arxiv.org/abs/1804.08946))

### In super-Yang-Mills theory
 {#ReferencesInSuperYangMillsTheory}

Confinement in [[N=2 D=4 super Yang-Mills theory]] by a version of the monopole condensation of ([t Hooft 75](#Hooft75), [Mandelstam 76](#Mandelstam76)) was demonstrated in

* {#SeibergWitten94} [[Nathan Seiberg]], [[Edward Witten]], _Monopole Condensation, And Confinement In N=2 Supersymmetric Yang-Mills Theory_,  	Nucl.Phys.B426:19-52,1994; Erratum-ibid.B430:485-486,1994 ([arXiv:hep-th/9407087](http://arxiv.org/abs/hep-th/9407087))

* {#SeibergWitten94b} [[Nathan Seiberg]], [[Edward Witten]], _Monopoles, Duality and Chiral Symmetry Breaking in N=2 Supersymmetric QCD_,  	Nucl.Phys.B431:484-550,1994 ([arXiv:hep-th/9408099](http://arxiv.org/abs/hep-th/9408099))
  
Reviews with discussion of the impact on confinement in plain YM include

* {#Yung00} Alexei Yung, _What Do We Learn about Confinement from the Seiberg-Witten Theory_ ([arXiv:hep-th/0005088](http://arxiv.org/abs/hep-th/0005088))

### Under the AdS/CFT correspondence

Discussion in the context of the [[AdS-CFT correspondence]] is in

* [[David Berman]], Maulik K. Parikh, _Confinement and the AdS/CFT Correspondence_, Phys.Lett. B483 (2000) 271-276 ([arXiv:hep-th/0002031](https://arxiv.org/abs/hep-th/0002031))

* Henrique Boschi Filho, _AdS/QCD and confinement_, Seminar at the _Workshop on Strongly Coupled QCD: The confinement problem_, November 2011 ([pdf](http://www.if.ufrj.br/~boschi/pesquisa/seminarios/AdS_QCD_Confinement_UERJ_2011.pdf))

### In M-theory on $G_2$-manifolds

An idea for how to demonstrate confinement in models of [[M-theory on G2-manifolds]] is given in 

* {#AtiyahWitten01} [[Michael Atiyah]], [[Edward Witten]], section 6 of  _$M$-Theory dynamics on a manifold of $G_2$-holonomy_, Adv. Theor. Math. Phys. 6 (2001) ([arXiv:hep-th/0107177](http://arxiv.org/abs/hep-th/0107177))

based on 

* {#AtiyahMaldacenaVafa00} [[Michael Atiyah]], [[Juan Maldacena]], [[Cumrun Vafa]], _An M-theory Flop as a Large N Duality_, J.Math.Phys.42:3209-3220, 2001 ([arXiv:hep-th/0011256](https://arxiv.org/abs/hep-th/0011256))

See also 

* [[Bobby Acharya]], _Confining Strings from $G_2$-holonomy spacetimes_ ([arXiv:hep-th/0101206](https://arxiv.org/abs/hep-th/0101206))

For review see

* {#AcharyaGukov04} [[Bobby Acharya]], [[Sergei Gukov]], section 5.3 of _M theory and Singularities of Exceptional Holonomy Manifolds_, Phys.Rept.392:121-189,2004 ([arXiv:hep-th/0409191](https://arxiv.org/abs/hep-th/0409191))


[[!redirects confinement]]
[[!redirects color confinement]]
[[!redirects colour confinement]]