
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

Confinement (e.g [Espiru 94](#Espiru94)) is the (expected) phenomenon in [[Yang-Mills theory]] generally and especially in [[quantum chromodynamics]] that the fundamental [[quarks]], which the [[Yang-Mills theory|YM]]/[[QCD]]-[[Lagrangian density]] actually describes, must form [[baryon|baryonic]] [[bound state|bound states]] which are neutral under the color charge -- the [[mesons]] and [[hadron|hadrons]] ([[proton|protons]], [[neutron|neutrons]]). Hence confinement in particular concerns the emergence and existence of [[atomic nuclei]], hence of ordinary [[matter]], which is not manifest at all in the [[quark]]-model. In order to prove, via [[QCD]] itself, that the potential energy of a colorless package of [[quarks]] tends to infinity as the distance between them grows, one must probe the long-range regime of the quark-quark interaction, in which the methods of [[perturbative quantum field theory|Feynman perturbation theory]] fail. 

Part of the issue is that confinement is a [[non-perturbative effect]] (e.g [Espiru 94](#Espiru94)) outside the range of validity of [[perturbative quantum field theory]].


[[!include open problem of confinement -- references]]



## Potential solutions

### Via Skyrmions and D4-brane models
 {#ViaSkyrmions}

A good qualitative and moderate quantitative explanation of confinement in [[quantum chromodynamics]] is found in [[intersecting D-brane models]], specifically in the [[Witten-Sakai-Sugimoto model]] which [[geometric engineering of QFT|geometrically engineers]] [[QCD]] on [[D4-D8 brane bound states]].

([Witten 98](#Witten98), followed up on in [Sakai-Sugimoto 04](Ads/QCD#SakaiSugimoto04), [Sakai-Sugimoto 05](Ads/QCD#SakaiSugimoto05))

<center>
<img src="https://ncatlab.org/nlab/files/SakaiSugimotoModel.jpg" width="600">
</center>

> graphics grabbed from [Erlich 09, section 1.1](Ads/QCD#Erlich09)


<center>
<img src="https://ncatlab.org/nlab/files/IntersectingBranesSSWModel.jpg" width="700">
</center>

> graphics grabbed from [Rebhan 14](Ads/QCD#Rebhan14)



In this [[Witten-Sakai-Sugimoto model]] for [[non-perturbative effect|strongly coupled]] [[QCD]] the [[hadrons]] in [[QCD]] correspond to [[string theory|string-theoretic]]-phenomena in the [[bulk field theory]]:

1. the [[mesons]] ([[bound states]] of 2 [[quarks]]) correspond to [[open strings]] in the bulk, whose two endpoints on the [[asymptotic boundary]] correspond to the two quarks

1. [[baryons]] ([[bound states]] of $N_c$ [[quarks]]) appear in two different but equivalent ([Sugimoto 16, 15.4.1](Ads/QCD#Sugimoto16)) guises:

   1. as [[wrapped brane|wrapped]] [[D4-branes]] with $N_c$ [[open strings]] connecting them to the [[D8-brane]]

      ([Witten 98b](Ads/QCD#Witten98b), [Gross-Ooguri 98, Sec. 5](Ads/QCD#GrossOoguri98), [BISY 98](Ads/QCD#BISY98), [CGS98](Ads/QCD#CGS98))

   1. as [[skyrmions]] 

      ([Sakai-Sugimoto 04, section 5.2](Ads/QCD#SakaiSugimoto04), [Sakai-Sugimoto 05, section 3.3](Ads/QCD#SakaiSugimoto05), see [Bartolini 17](Ads/QCD#Bartolini17)). 

For review see [Sugimoto 16](Ads/QCD#Sugimoto16), also [Rebhan 14, around (18)](Ads/QCD#Rebhan14).

<center>
<img src="https://ncatlab.org/nlab/files/BaryonsAsD4Branes.jpg" width="700">
</center>

> graphics grabbed from [Sugimoto 16](Ads/QCD#Sugimoto16)


Equivalently, these baryon states are the [[Yang-Mills instantons]] on the [[D8-brane]] giving the [[D4-D8 brane bound state]] ([Sakai-Sugimoto 04, 5.7](Ads/QCD#SakaiSugimoto04)) as a special case of the general situation for [[Dp-D(p+4)-brane bound states]] (e.g. [Tong 05, 1.4](Dp-D%28p%2B4%29-brane+bound+state#Tong05)).

Strictly speaking, since the number of [[color charge|colors]] in [[quantum chromodynamics]] is not [[large N limit|large]] ($N_c = 3$), an accurate formulation of such [[holographic QCD]] requires understanding [[small N corrections]]:

<center>
<a href="https://ncatlab.org/schreiber/files/Schreiber-MTheoryMathematics2020-v200126.pdf#page=8">
<img src="https://ncatlab.org/schreiber/files/ProblemQCDToProblemM230120.jpg" width="670">
</a>
</center>

For more on this see at

* _[[AdS/QCD correspondence]]_

and at

* _[[skyrmion]]_ .

### In $\mathcal{N}=2$ super Yang-Mills theory via Seiberg-Witten theory
  {#InN2SYM}

While confinement in plain [[Yang-Mills theory]] is still waiting for mathematical formalization and [[proof]] (see [Jaffe-Witten](#JaffeWitten)), there is a variant of [[Yang-Mills theory]] with more [[symmetry]], namely [[supersymmetry]], where the phenomenon has been giving a decent argument, namely in [[N=2 D=4 super Yang-Mills theory]] ([Seiberg-Witten 94](#SeibergWitten94)). 

Also a strategy for a proof for [[N=1 D=4 super Yang-Mills theory]] has been proposed, see [below](#ForN1SYMViaMTheoryOnG2Manifolds).






### In $\mathcal{N} = 1$ super Yang-Mills theory via M-theory on $G_2$-manifolds
 {#ForN1SYMViaMTheoryOnG2Manifolds}

An idea for a strategy towards a proof of confinement in [[N=1 D=4 super Yang-Mills theory]] via two different but conjecturally equivalent realizations as [[M-theory on G₂-manifolds]] has been given in [Atiyah-Witten 01, section 6](#AtiyahWitten01), review is in [Acharya-Gukov 04, section 5.3](#AcharyaGukov04).

The idea here is to consider a [[KK-compactification]] of [[M-theory]] on [[fibers]] which are [[G₂-manifolds]] that locally around a special point 
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

Now the lore of [[M-theory on G₂-manifolds]] predicts that [[KK-compactification]]

1.  on $X_{1,\Gamma}$ yields a 4d theory without massless fields (since there are no massless modes on the [[covering space]] $S^3$ of $X_{1,\Gamma}$)

1. on the [[ADE-singularity]] $X_{2,\Gamma}$ yields [[non-abelian group|non-abelian]] [[Yang-Mills theory]] in 4d coupled to [[chiral fermions]].

So in the first case a [[Yang-Mills mass gap]] is manifest, while non-abelian gauge theory is not visible, while in the second case it is the other way around.

But if there were an argument that [[M-theory on G₂-manifolds]] is in fact equivalent for compactification both on $X_{1,\Gamma}$ and on $X_{2,\Gamma}$. To the extent that this is true, it looks like an argument that could demonstrate confinement in non-abelian 4d gauge theory.

This approach is suggested in [Atiyah-Witten 01, pages 84-85](#AtiyahWitten01). An argument that this equivalence is indeed the case is then provided in sections 6.1-6.4, based on an argument in [Atiyah-Maldacena-Vafa 00](#AtiyahMaldacenaVafa00) 


### Via Calorons
 {#ViaCalorons}

It has been argued that, after [[Wick rotation]], confinement may be derived from the behaviour of [[instantons]] ([Schaefer-Shuryak 96, section III D](#SchaeferShuryak96)), or rather their [[thermal field theory|positive temperature]]-incarnations as _[[calorons]]_, [Greensite 11, section 8.5](#Greensite11):

> it is natural to wonder if [[confinement]] could be derived from some [[semiclassical approximation|semiclassical]] treatment of [[Yang–Mills theory]] based on the [[instanton]] solutions of [[nonabelian group|non-abelian]] [[gauge theories]]. The [[BPST instanton|standard]] [[instantons]], introduced by Belavin et al. ([40](BPST-instanton#BelavinPolyakovSchwartzTyupkin75)), do not seem to work; their [[field strengths]] fall off too rapidly to produce the desired  magnetic  disorder  in  the  vacuum.  

> In  recent years, however, it has been realized that instanton solutions at [[thermal field theory|finite temperature]], known as _[[calorons]]_, might do the job. These caloron solutions were introduced independently by Kraan and van Baal ([41](caloron#KraanVanBaal98), [42](caloron#KraanVanBaal98b)) and Lee and Lu ([43](caloron#LeeLu98)) (KvBLL), and they have the remarkable property of containing [[monopole]] constituents which may, depending on the type of [[caloron]], be widely separated.

> $[...]$

> The [[caloron]] idea is probably the most promising current version of [[monopole]] [[confinement]] in pure non-abelian gauge theories, but it is  basically  (in certain [[gauge fixing|gauges]]) a superposition of [[monopoles]] with spherically  symmetric abelian fields, and this leads to the same questions raised in connection with monopole Coulomb gases.

See also at _[[glueball]]_.





## Related concepts

* [[asymptotic freedom]]

* [[quantization of Yang-Mills theory]]

* [[proton spin crisis]], [[proton radius problem]]

* [[QCD cosmology]]

* [[gapped Hamiltonian]]

[[!include effective field theories of nuclear physics -- contents]]



## References

### In Yang-Mills theory
 {#ReferencesInYangMillsTheory}

#### General

* {#Wilson74} [[Kenneth Wilson]],  *Confinement of quarks*, Phys. Rev. D **10** 2445 (1974) &lbrack;[doi:10.1103/PhysRevD.10.2445](https://doi.org/10.1103/PhysRevD.10.2445)&rbrack;

Early demonstration of confinement by [[Monte Carlo simulation]] of [[lattice field theory]] (and demonstration that $SU(2)$-[[gauge theory]] in 4d does *not* confine, as it should be):

* {#Creutz79} [[Michael Creutz]], *Confinement and the Critical Dimensionality of Space-Time*, Phys. Rev. Lett. **43**  (1979) 553 &lbrack;[doi:10.1103/PhysRevLett.43.553](https://doi.org/10.1103/PhysRevLett.43.553)&rbrack; 

Textbook accounts:

* [[Alexander Polyakov]], Chapter V of: *Gauge Fields and Strings*, Routledge, Taylor and Francis (1987, 2021) &lbrack;[doi:10.1201/9780203755082](https://doi.org/10.1201/9780203755082), [oapen:20.500.12657/50871](https://library.oapen.org/handle/20.500.12657/50871)&rbrack;


* [[David Griffiths]], chapter 8 of: _Introduction to Elementary Particles_ 2nd ed., Wiley-VCH  (2008) &lbrack;[pdf] (https://www.physics.utah.edu/~belz/phys5110/Griffiths.pdf), [pdf](https://mikefragugliacom.wordpress.com/wp-content/uploads/2016/12/introduction-to-elementary-particles-gnv64.pdf), <a href="https://en.wikipedia.org/wiki/Introduction_to_Elementary_Particles_(book)">Wikipedia entry</a>&rbrack;

* {#Greensite11} Jeff Greensite, _An Introduction to the Confinement Problem_, Lecture Notes in Physics, Volume 821, 2011 ([doi:10.1007/978-3-642-14382-3](https://link.springer.com/book/10.1007%2F978-3-642-14382-3))

* Robert Iengo, section 9.1 of _Quantum Field Theory_ ([pdf](http://iopscience.iop.org/chapter/978-1-6432-7053-1/bk978-1-6432-7053-1ch9.pdf))

* D. Bugg (ed.), _Hadron Spectroscopy and the Confinement Problem_, Proceedings of a NATO Advanced Study Institute, Plenum Press 1996  ([doi:10.1007/978-1-4613-0375-6](https://www.springer.com/cn/book/9780306453038))


* [[Yakov Shnir]], Section 9 of: *Magnetic Monopoles*, Springer 2005 ([ISBN:978-3-540-29082-7](https://www.springer.com/gp/book/9783540252771))

  > (in view of [[Yang-Mills monopoles]])

Introductions and surveys:

* Yuri L. Dokshitzer, around section 1.2 of _QCD Phenomenology_ ([arXiv:hep-ph/0306287](https://arxiv.org/abs/hep-ph/0306287))

* {#Espiru94} D. Espriu, section 7 of _Perturbative QCD_ ([arXiv:hep-ph/9410287](http://arxiv.org/abs/hep-ph/9410287))

* Erhard Seiler, _The Confinement Problem_ ([pdf](http://physik.uni-graz.at/~dk-user/talks/Seiler20081113-14.pdf))

* Roman Pasechnik, Michal Šumbera, *Different faces of confinement*, Universe 7 (2021) 9, 330 ([arXiv:2109.07600](https://arxiv.org/abs/2109.07600), [doi:10.3390/universe7090330](https://doi.org/10.3390/universe7090330))

See also: 

* Wikipedia, _[Color confinement](http://en.wikipedia.org/wiki/Color_confinement)_

* _[What is Strongly-Coupled Quantum Chromodynamics?](https://ensnaredinvacuum.wordpress.com/2015/02/11/what-is-strongly-coupled-quantum-chromodynamics/)_

* *[[Prospects in Theoretical Physics 2023 -- Understanding Confinement]]*, IAS (2023) 

A formulation of confinement as an open problem of mathematical physics, together with many references, is in 

* {#JaffeWitten} [[Arthur Jaffe]], [[Edward Witten]], _Quantum Yang-Mills theory_ ([pdf](http://www.claymath.org/millennium/Yang-Mills_Theory/yangmills.pdf))
 

Other technical reviews:

* G. M. Prosperi, _Confinement and bound states in QCD_ ([arXiv:hep-ph/0202186](http://arxiv.org/abs/hep-ph/0202186))

* {#DHMMNVW19} Christian Drischler, Wick Haxton, Kenneth McElvain, Emanuele Mereghetti, Amy Nicholson, Pavlos Vranas, André Walker-Loud, _Towards grounding nuclear physics in QCD_ ([arxiv:1910.07961](https://arxiv.org/abs/1910.07961))

* [[Urko Reinosa]], *Aspects of confinement within non-Abelian gauge theories*, lectures at *[QCD Masterclass, Saint-Jacut-de-la-Mer, June 2023](https://indico.cern.ch/event/1174608/)* &lbrack;[arXiv:2404.06118](https://arxiv.org/abs/2404.06118)&rbrack;


See also:

* [[Yuri A. Simonov]], *The fundamental scale of QCD* ([arXiv:2103.08223](https://arxiv.org/abs/2103.08223))

* Duifje Maria van Egmond, Urko Reinosa, Julien Serreau, Matthieu Tissier, 
*A novel background field approach to the confinement-deconfinement transition* ([arXiv:2104.08974](https://arxiv.org/abs/2104.08974))

* Erich Poppitz, *Notes on Confinement on $\mathbb{R}^3 \times S^1$: From Yang-Mills, super-Yang-Mills, and QCD(adj) to QCD(F)* ([arXiv:2111.10423](https://arxiv.org/abs/2111.10423))

Recognition of [[instantons]] and confinement in [[lattice gauge theory]] via [[topological data analysis]] ([[persistent homology]]):

* Daniel Spitz, Julian M. Urban, Jan M. Pawlowski, *Confinement in non-Abelian lattice gauge theory via persistent homology* &lbrack;[arXiv:2208.03955](https://arxiv.org/abs/2208.03955)&rbrack;

In relation to [[conformal symmetry]] and [[AdS-CFT duality]] (see also at *[[AdS-QCD]]*):

* {#KPV22} M. Kirchbach, T. Popov, J.-A. Vallejo, *The Conformal-Symmetry -- Color-Neutrality Connection in Strong Interaction* &lbrack;[arXiv:2208.06484](https://arxiv.org/abs/2208.06484)&rbrack;

* Canberk Güvendik, Thomas Schaefer, Mithat Ünsal, *The metamorphosis of semi-classical mechanisms of confinement: From monopoles on $\mathbb{R}^3 \times S^1$ to center-vortices on $\mathbb{R}^2 \times T^2$* &lbrack;[arXiv:2405.13696](https://arxiv.org/abs/2405.13696)&rbrack;

* E. G. Timoshenko, *Boundary Effects and Confinement in the Theory of Nonabelian Gauge Fields*, PhD thesis (1995) &lbrack;[arXiv:2405.13189](https://arxiv.org/abs/2405.13189)&rbrack;

See also:

* M.S. Lukashov, Yu.A. Simonov, *New ideas in nonperturbative QCD -- I* &lbrack;[arXiv:2406.05584](https://arxiv.org/abs/2406.05584)&rbrack;

* J.L. Alonso, C. Bouthelier-Madre, J. Clemente-Gallardo, D. Martínez-Crespo: *An axion-like mechanism for confinement in QCD* &lbrack;[arXiv:2211.01047](https://arxiv.org/abs/2211.01047)&rbrack;




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


Further developments:

* _Dimensional Transmutation by Monopole Condensation in QCD_ ([arXiv:1206.6936](http://arxiv.org/abs/1206.6936))


Discussion of confinement via an interacting field vacuum

* {#Rafelski90} [[Johann Rafelski]], _Vacuum structure -- An Essay_, in pages 1-29 of H. Fried, Berndt Müller (eds.) _Vacuum Structure in Intense Fields_, Plenum Press 1990 ([GBooks](https://books.google.de/books?id=5uXcBwAAQBAJ&pg=PA14&lpg=PA14&dq=confinement+%22interacting+vacuum%22&source=bl&ots=xPGYJ-JOc-&sig=AoYbqWQeNRMg6hMSRZjJ3nzq8B0&hl=en&sa=X&ved=0ahUKEwjIgK68-tnYAhVCESwKHThMDykQ6AEIKTAA#v=onepage&q=confinement%20%22interacting%20vacuum%22&f=false))

See also:

* {#Simonov18} [[Yuri A. Simonov]], _Field Correlator Method for the confinement in QCD_, Phys. Rev. D 99, 056012 (2019) ([arXiv:1804.08946](https://arxiv.org/abs/1804.08946), [doi:10.1103/PhysRevD.99.056012](https://doi.org/10.1103/PhysRevD.99.056012))



### In super-insulators
 {#ReferencesInSuperInsulators}

An experimentally accessible analog of confinement is observed in [[superinsulators]], where the role of [[quark]]-[[pairs]] is played by [[Cooper pairs]]:

* [[M. Cristina Diamantini]], [[Carlo A. Trugenberger]], Valeri M. Vinokur: *Confinement and Asymptotic Freedom with Cooper pairs*, Nature Comm. Phys. **1** 77 (2018) &lbrack;[arXiv:1807.01984](https://arxiv.org/abs/1807.01984), [doi:10.1038/s42005-018-0073-9](https://doi.org/10.1038/s42005-018-0073-9)&rbrack;

* [[M. Cristina Diamantini]], [[Carlo A. Trugenberger]]: *Superinsulators: a toy realization of QCD in condensed matter*, Ch. 23 in *Roman Jackiw -- 80th Birthday Festschrift*, World Scientific (2020) 275-286 &lbrack;[arXiv:2008.12541](https://arxiv.org/abs/2008.12541)&rbrack;

Review:

* [[Carlo A. Trugenberger]]: *Superinsulators, Bose Metals and High-$T_c$ Superconductors: The Quantum Physics of Emergent Magnetic Monopoles*, World Scientific (2022) &lbrack;[arXiv:10.1142/12688](https://doi.org/10.1142/12688)&rbrack;


* [[Carlo A. Trugenberger]]: *Superinsulation: Magnetic Monopoles and Electric Confinement in Condensed Matter*, [talk at](CQTS##TrugenbergerFeb2025) [[CQTS]] (Feb 2025) &lbrack;slides:[[Trugenberger-CQTSFeb2025.pdf:file]]&rbrack;





### In super-Yang-Mills theory
 {#ReferencesInSuperYangMillsTheory}

Confinement in [[N=2 D=4 super Yang-Mills theory]] or [[super QCD]] by a version of the [[Yang-Mills monopole|monopole]] condensation &lbrack;['t Hooft 75](#Hooft75), [Mandelstam 76](#Mandelstam76)&rbrack; was demonstrated in

* {#SeibergWitten94} [[Nathan Seiberg]], [[Edward Witten]], _Monopole Condensation, And Confinement In N=2 Supersymmetric Yang-Mills Theory_,  	Nucl.Phys.B426:19-52,1994; Erratum-ibid.B430:485-486,1994 ([arXiv:hep-th/9407087](http://arxiv.org/abs/hep-th/9407087))

* {#SeibergWitten94b} [[Nathan Seiberg]], [[Edward Witten]], _Monopoles, Duality and Chiral Symmetry Breaking in N=2 Supersymmetric QCD_,  	Nucl.Phys.B431:484-550,1994 ([arXiv:hep-th/9408099](http://arxiv.org/abs/hep-th/9408099))
  
Reviews with discussion of the impact on confinement in plain YM:

* {#Yung00} Alexei Yung, _What Do We Learn about Confinement from the Seiberg-Witten Theory_ &lbrack;[arXiv:hep-th/0005088](http://arxiv.org/abs/hep-th/0005088)&rbrack;

* [[Michael Dine]], *On the Possibility of Demonstrating Confinement in Non-Supersymmetric Theories by Deforming Confining Supersymmetric Theories* &lbrack;[arXiv:2211.17134](https://arxiv.org/abs/2211.17134)&rbrack;

* [[Michael Dine]]: *Larkin Award Colloquium*, University of Santa Cruz, (Dec 2024) &lbrack;video:[YT](https://youtu.be/k34YTIBWMNk)&rbrack;

See also:

* Michele Della Morte, Benjamin Jäger, Francesco Sannino, Justus Tobias Tsang, Felix P. G. Ziegler, *The spectrum of QCD with one flavour: A Window for Supersymmetric Dynamics* &lbrack;[arXiv:2302.10514](https://arxiv.org/abs/2302.10514)&rbrack; 



[[!include Polyakov gauge-string duality -- references]]




### Confinement via AdS/QCD correspondence

[Polyakov's ideas](#PolyakovGaugeStringDualityReferences) were eventually picked up by discussion of confinement in the [[AdS-QCD correspondence]]; see there for many references, including:

* {#Witten98} [[Edward Witten]], _Anti-de Sitter Space, Thermal Phase Transition, And Confinement In Gauge Theories_, Adv. Theor. Math. Phys.2:505-532, 1998 ([arXiv:hep-th/9803131](https://arxiv.org/abs/hep-th/9803131))

* [[David Berman]], Maulik K. Parikh, _Confinement and the AdS/CFT Correspondence_, Phys.Lett. B483 (2000) 271-276 ([arXiv:hep-th/0002031](https://arxiv.org/abs/hep-th/0002031))

* Henrique Boschi Filho, _AdS/QCD and confinement_, Seminar at t_Workshop on Strongly Coupled QCD: The confinement problem_ (November 2011) &lbrack;[pdf](http://www.if.ufrj.br/~boschi/pesquisa/seminarios/AdS_QCD_Confinement_UERJ_2011.pdf), [[Filho-AdSQCDConfinement.pdf:file]]&rbrack;

* [[Edward Witten]], *Some Milestones in the Study of Confinement*, talk at *[[Prospects in Theoretical Physics 2023 -- Understanding Confinement]]*, IAS (2023) &lbrack;[web](https://www.ias.edu/video/some-milestones-study-confinement), [YT](https://youtu.be/TvIz-6YOdKs)&rbrack;

> [40:13](https://youtu.be/TvIz-6YOdKs?t=2413): "Personally, I think [[AdS/QCD|this setup]] really implies that pure [[Yang-Mills theory|$SU(N)$ gauge theory]] is [[gauge-string duality|dual]] to a [[string theory]]. The 'only' problem is that to get the pure gauge theory we need to make a relevant deformation and then take the limit that the deformation parameter is large..."



### In M-theory on $G_2$-manifolds

An idea for how to demonstrate confinement in models of [[M-theory on G₂-manifolds]] is given in 

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

[[!redirects deconfinement]]
[[!redirects color deconfinement]]
[[!redirects colour deconfinement]]

