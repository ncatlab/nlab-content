
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Fields and quanta
+--{: .hide}
[[!include fields and quanta - table]]
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

What is called _[[chiral perturbation theory]]_ in [[quantum field theory]] of [[nuclear physics]] is the [[effective field theory]] of [[quantum chromodynamics]] in the [[confinement|confined]] sector, where the [[effective field theory|effective]] [[field (physics)|fields]] are [[hadrons]]: 

* [[light meson|light]]$\;$[[scalar mesons]] appear as the [[Goldstone bosons]] of the [[spontaneous symmetry breaking|spontaneously broken]] [[chiral symmetry]] (see below),  

* [[vector mesons]] appear as [[gauge fields]] of a [[hidden local symmetry]],

* [[baryons]] (specifically [[nuclei]]) appear as [[solitons]] in the meson-fields (called [[Skyrmions]]), 

* [[heavy mesons]] appear as further [[field (physics)|fields]]. 

Hence some authors also speak of _[[quantum hadrodynamics]]_.

More concretely, chiral perturbation theory is [[perturbation theory]] not in the [[coupling constant]] of [[QCD]], but in the [[masses]] of the [[light quarks]], which in practice means: of the [[up quark]] and the [[down quark]] and possibly also of the [[strange quark]], with masses $m_u$, $m_d$ and $m_s$, respectively.

As such, the point about which [[perturbation theory|perturbations]] are considered in chiral perturbation theory of QCD is that of vanishing [[quark]] masses, hence the [[limit of a sequence|limit]] $ m_u, m_s, m_d \rightarrow 0 $.

{#ProtonMass} Notice that the [[proton]] [[mass]] (the characteristic scale of [[QCD]] witnessing its [[confinement]]/[[mass gap]]-property, see e.g. [Roberts 21](proton#Roberts21)) is much larger than the [[sum]] of its [[constituent quarks]]

$$
  m_p \gg 2 m_u + m_d
  \,,
$$

suggesting that $m_u, m_d \to 0$ is a good limit around which to inspect the [[hadron|hadronic]] [[bound states]] of [[QCD]].

{#LagrangianInCPTLimit} But since only the quark mass term in the [[Lagrangian density]] of [[QCD]] mixes the two [[Weyl spinor|chiralities]] of quarks, its [[Lagrangian density]] in this massless limit is the sum of a term that only contains the left-chiral quark spinors, and an analogous summand that only contains the right-chiral quark spinors (e.g. [Ecker 95, (2.1)](#Ecker95)):

$$
  \mathcal{L}^0_QCD 
  \;=\; 
  \sum_{l=u,d,s} 
  \big(
    \bar{q}^l_L i (\slash{D} + \slash{A}) q^l_L 
    +
    \bar{q}^l_R i (\slash{D} + \slash{A}) q^l_R
  \big)
  - 
  \frac{1}{4}G_{a \mu v}G^{\mu v}_a 
$$

(here $q$ denotes the [[quark]] [[Dirac field]] with left and right [[chiral fermion|chiral]] [[Weyl spinor]] components $q_L$ and $q_R$, $\slash{D}$ denotes the [[Dirac operator]], $A$ the [[gluon]] [[field (physics)|field]] (in [[Feynman slash notation]]), and $G$ the [[field strength]] of the [[gluon]] [[field]] $A$ -- see at *[[Yang-Mills theory]]* for more).

Moreover, all two ([[up quark|up]] and [[down quark|down]]) or even all three (if including [[strange quark|strange]]) [[flavour (particle physics)|flavours]] of quarks enter each of these two spinor-chiral summands symmetrically, such that each of them has [[SU(2)]] or respectively [[SU(3)]] [[global symmetry]], [[action|acting]] by mixing the quark flavours. This yields a total [[direct product group|direct product]] [[symmetry group]] 

$$
  G = SU(N_f)_L \times SU(N_f)_R
  \,,
$$

where $N_f \in \{ 2,3 \}$ is the [[number]] of [[flavour (particle physics)|flavours]] of [[light quarks]] that are being considered, and where the subscripts indicate the left/right-handed [[chiral spinor]]-components of quarks whose [[flavour (particle physics)|flavours]] are being mixed by these [[group]] [[actions]]. This [[symmetry group]] is hence also called _chiral symmetry_. Accordingly, its [[symmetry breaking]] to the [[diagonal morphism|diagonal]] [[subgroup]]

$$
  SU(N_f)_V
  \;\subset\;
  SU(N_f)_L \times SU(N_f)_R
$$

(the subscript "$V$" is for "vector") either explicitly by [[positive number|positive]] [[quark]] [[masses]] or [[spontaneous symmetry breaking|spontaneously]] by a [[vacuum expectation value]] $\langle \bar q q\rangle = \langle \bar q_L q_R\rangle + \langle \bar q_R q_L\rangle$, is called _[[chiral symmetry breaking]]. This is the origin of the term _chiral perturbation theory_.

Additionally, the application of [[noether's theorem]] to the classical global symmetry of the lagrangian density in the chiral limit yields $ 2 \times (8+1) = 18 $ conserved currents, via the method of [[Gell-Mann]] and [[Levy]]. Namely, the promotion of the [[global symmetry]] inherent in the lagrangian density to a [[local symmetry]] allows us to identify these conserved [[noether currents]] 

$$
  J^\mu_a = \frac{\partial \delta \mathcal{L}}{\partial \partial_\mu \epsilon_a}
  \partial_{\mu} J^{\mu}_a = \frac{\partial \delta \mathcal{L}}{\partial \epsilon_a}
$$



(...)

## Properties

### Relation to the Skyrme model

* [[Dmitri Diakonov]], [[Victor Petrov]], _Exotic baryon resonances in the Skyrme model_ ([arXiv:0812.1212](https://arxiv.org/abs/0812.1212), [doi:10.1142/9789814704410_0004](https://doi.org/10.1142/9789814704410_0004)), Chapter 3 in: _[[The Multifaceted Skyrmion]]_, World Scientific 2016 ([doi:10.1142/9710](https://doi.org/10.1142/9710))

> It is astounding that [[Tony Skyrme|Skyrme]] had suggested [[Skyrmion|his model]] as early as in 1961 before it has been generally accepted that [[pions]] are (pseudo) [[Goldstone bosons]] associated with the [[spontaneous symmetry breaking|spontaneous breaking]] of [[chiral symmetry]], and of course long before [[QCD|Quantum Chromodynamics (QCD)]] has been put forward as the microscopic theory of [[strong nuclear force|strong interactions]].

> The revival of the Skyrme idea in 1983 is [due to Witten](Skyrmion#Witten83) who explained the _raison d'ˆetre_ of the [[Skyrmion|Skyrme model]] from the viewpoint of [[QCD]]. In the [[chiral perturbation theory|chiral limit]] when the [[light quark]] masses $m_u$, $m_d$, $m_s$ tend to zero, such that the octet of the pseudoscalar mesons [[pion|π]], [[kaon|K]] , η become nearly massless (pseudo) [[Goldstone bosons]], they are the lightest degrees of freedom of [[QCD]]. The [[effective field theory|effective]] chiral Lagrangian (EχL) for pseudoscalar mesons, understood as an infinite expansion in the derivatives of the pseudoscalar (or chiral) fields, encodes, in principle, full information about QCD. The famous two-term Skyrme Lagrangian can be understood as a low-energy truncation of this infinite series. Witten has added an important four-derivative [[WZW-term|Wess–Zumino term]] to the original Skyrme Lagrangian and pointed out that the overall coefficient in front of the EχL is proportional to the number of quark [[color charge|colours]] $N_c$.

> $[...]$

> Soon after Witten's work it has been realized that it is possible to bring the Skyrme model and the Skyrmion even closer to QCD and to the more customary language of constituent quarks. It has been first noticed $[$[6](#DiakonovEides83), [7a](#DharWadia84), [7b](#DarShankarWadia85), [8](#DiakonovPetrov86)$]$ that a simple chiral invariant Lagrangian for massive (constituent) quarks $Q$ interacting with the octet chiral field $\pi_A$ $(A = 1, ..., 8)$,

> $$\mathcal{L} = \overline{Q} \left( \partial\!\!\!\!/ - M e^{ \tfrac{i \pi^A \lambda^A \gamma_5}{F_\pi}  }  \right) Q$$

> induces, via a quark loop in the external pseudoscalar fields (see Fig. 3.1), the EχL whose lowest-derivative terms coincide with the Skyrme Lagrangian, including
automatically the Wess–Zumino term, with the correct coefficient!

<center>
<img src="https://ncatlab.org/nlab/files/DiakonovPetrovQuarkLoop.jpg" width="600">
</center>

> $[...]$

> The condition that the winding number of the trial field is unity needs to be imposed to get a deeply bound state, that is to guarantee that the baryon number is unity. $[$[9](#DiakonovPetrovPobylitsa88)$]$ The Skyrmion is, thus, nothing but the **mean chiral field binding quarks in a baryon**.

<center>
<img src="https://ncatlab.org/nlab/files/DiakonovPetrovMeanField.jpg" width="600">
</center>

\linebreak

* {#DiakonovEides83} [[Dmitri Diakonov]], Michael I. Eides, _Chiral Lagrangian from a functional integral over quarks_, JETP Letters 38.7 (1983): 433-436 ([pdf](http://jetpletters.ac.ru/ps/1483/article_22635.pdf), [[DiakonovEides83.pdf:file]])

* {#DharWadia84} A. Dhar, Spenta R. Wadia, _Nambu—Jona-Lasinio Model: An Effective Lagrangian for Quantum Chromodynamics at Intermediate Length Scales_, Phys. Rev. Lett. 52, 959 (1984) ([doi:10.1103/PhysRevLett.52.959](https://doi.org/10.1103/PhysRevLett.52.959))

* {#DarShankarWadia85} Avinash Dhar, R. Shankar, Spenta R. Wadia, _Nambu–Jona-Lasinio–type effective Lagrangian: Anomalies and nonlinear Lagrangian of low-energy, large-N QCD_, Phys. Rev. D 31, 3256 (1985) ([doi:10.1103/PhysRevD.31.3256](https://doi.org/10.1103/PhysRevD.31.3256))

* {#DiakonovPetrov86} [[Dmitri Diakonov]], [[Victor Petrov]], _A theory of light quarks in the instanton vacuum_, Nuclear Physics B Volume 272, Issue 2, 21 July 1986, Pages 457-489 (<a href="https://doi.org/10.1016/0550-3213(86)90011-8">doi:10.1016/0550-3213(86)90011-8</a>)

* {#DiakonovPetrovPobylitsa88} [[Dmitri Diakonov]], [[Victor Petrov]], P.V. Pobylitsa, _A Chiral Theory of Nucleons_, Nucl. Phys. B306 (1988) 809 ([spire:247700](http://inspirehep.net/record/247700), <a href="https://doi.org/10.1016/0550-3213(88)90443-9">doi:10.1016/0550-3213(88)90443-9</a>)


### Baryon Chiral Perturbation Theory

The QCD vacuum breaks chiral symmetry down to the diagonal subgroup of SU(3), $U(3)_v$, whereby 8 massless [[Goldstone boson | goldstone bosons]] appear, each of which are coupled via $F_0$ to the conserved axial-vector current. The physics of these [[Goldstone boson | goldstone bosons]], which are themselves the pion fields, describe the low energry [[effective field theory]] known as [[chiral perturbation theory]]. In this low energy structure of QCD, heavy quarks do not play a role since their degrees of freedom are frozen at low energies. However, when the baryon fields are treated as heavy static [[fermions]] in the expansion of the physical vacuum state of QCD, one can write the effective theory in terms of baryon fields with a definite velocity, $B_v$. In the heavy baryon limit, the most general Lagrangian at leading-order is
$$
  L_v^0 = iTr\overline{B}_v(v*\mathscr{D})B_v + 2DTr\overline{B}_v S_v^\mu \{A_\mu,B_v\} + 2FTr\overline{B}_v S_v^\mu \{A_\mu,B_v\} + \frac{1}{4}f^2Tr\partial_{\mu}\Sigma\partial^\mu \Sigma^\dagger + aTrM(\Sigma + \Sigma^\dagger)
$$   

### Partially Quenched Chiral Perturbation Theory

In [[Lattice QCD]], it is notoriously difficult to include the loops of [[light quarks]]. One remedy to this problem is to approximate the fermion determinant of a Dirac operator $D$, which is proportional to the summation of external sources interacting with one internal [[fermion loop]]. The partially quenched prescription includes the determinant but with [[sea quark]] masses $\ggg$ those of the valence quarks. The simulation of partially quenched QCD (PQQCD) on the lattice can yield information about QCD itself by utilizing [[chiral perturbation theory]]. The formulation of XPT in PQQCD is difficult compared to the unquenched case (standard formulation) due to the lack of a physical [[hilbert space]].  


* S.R.Sharpe and N.Shoresh, _Partially quenched chiral perturbation theory without Phi0_, Phys. Rev. D 64, 114510 (2001), doi:10.1103/PhysRevD.64.114510, ([arXiv:hep-lat/0108003](https://arxiv.org/abs/hep-lat/0108003v1))

* Claude W. Bernard and Maarten F. L. Golterman, _Partially quenched gauge theories and an application to staggered fermions_, Phys. Rev. D 49, 486 – Published 1 January 1994, ([doi:10.1103/486] (https://doi.org/10.1103/PhysRevD.49.486))


### Random Matrix Theory and Chiral Symmetry

It has been posited that the statistics of the low-lying eigenvalues of the QCD [[Dirac operator]] can be described by a [[random matrix theory]] with the global symmetries of the QCD [[partition function]]. 

* J.J.M. Verbaarschot and T.Wettig, _Random matrix theory and chiral symmetry in QCD_, Ann. Rev. Nucl. Part. Sci. 50, 343-410 (2000), doi:10.1146/annurev.nucl.50.1.343, ([arXiv:hep-ph/0003017 [hep-ph]](https://arxiv.org/abs/hep-ph/0003017v2)).

* J.C. Osborn, D.Toublan and J.J.M.Verbaarschot, _From chiral random matrix theory to chiral perturbation theory_, Nucl. Phys. B 540, 317-344 (1999), doi:10.1016/S0550-3213(98)00716-0 ([arXiv:hep-th/9806110](https://arxiv.org/abs/hep-th/9806110v2)).

## Related concepts

[[!include effective field theories of nuclear physics -- contents]]

* [[confinement]]

* [[chiral symmetry breaking]]

* [[hadron]]

  * [[meson]]

  * [[baryon]]

* [[chiral partner]]

* [[quark bag model]], [[Cheshire cat principle]]


* [[hadron supersymmetry]], [[hadron Kaluza-Klein theory]]

  * [[flavor brane]]

* [[leptonic decay]]

* [[holographic QCD]]

## References

### Introduction and review

* [[Jürg Gasser]], _The QCD Vacuum and Chiral Symmetry_, In: Vautherin D., Lenz F., Negele J.W. (eds.) _Hadrons and Hadronic Matter_, NATO ASI Series (Series B: Physics), vol 228. Springer 1990 ([doi:10.1007/978-1-4684-1336-6_4](https://doi.org/10.1007/978-1-4684-1336-6_4))

* [[Gerhard Ecker]], _The standard model at low energies_, Czech. J. Phys. 44:405-430, 1995 ([arXiv:hep-ph/9309268](https://arxiv.org/abs/hep-ph/9309268))

* {#Ecker95} [[Gerhard Ecker]], *Chiral Perturbation Theory*, Prog. Part. Nucl. Phys. 35:1-80, 1995 ([arXiv:hep-ph/9501357](https://arxiv.org/abs/hep-ph/9501357))

* [[Antonio Pich]], _Chiral Perturbation Theory_ ([arXiv:hep-ph/9502366](https://arxiv.org/abs/hep-ph/9502366))

* [[Maciej Nowak]], [[Mannque Rho]], [[Ismail Zahed]], _[[Chiral Nuclear Dynamics]]_,  World Scientific 1996 ([doi:10.1142/1681](https://doi.org/10.1142/1681))

* Volker Koch, _Aspects of Chiral Symmetry_, Int. J. Mod. Phys. E6 (1997) 203-250 ([arXiv:nucl-th/9706075](https://arxiv.org/abs/nucl-th/9706075))

* Barry R. Holstein, _A Brief Introduction to Chiral Perturbation Theory_, Czech. J. Phys. 50S4:9-23, 2000 ([arXiv:hep-ph/9911449](https://arxiv.org/abs/hep-ph/9911449))

* [[Stefan Scherer]], _Introduction to Chiral Perturbation Theory_, Adv. Nucl. Phys. 27 (2003) 277 ([arXiv:hep-ph/0210398](https://arxiv.org/abs/hep-ph/0210398))

* [[Stefan Scherer]], Matthias R. Schindler, _A Chiral Perturbation Theory Primer_ ([arXiv:hep-ph/0505265](https://arxiv.org/abs/hep-ph/0505265))


* [[Véronique Bernard]], [[Ulf-G. Meissner]], _Chiral perturbation theory_, Ann. Rev. Nucl. Part. Sci.57:33-60, 2007 ([arXiv:hep-ph/0611231](https://arxiv.org/abs/hep-ph/0611231))

* [[Gerhard Ecker]], _Status of chiral perturbation theory_, PoS Confinement 8:025, 2008 ([arXiv:0812.4196](https://arxiv.org/abs/0812.4196))

* Johan Bijnens, _Chiral perturbation theory in the meson sector_, PoS CD09:031, 2009 ([arXiv:0909.4635](https://arxiv.org/abs/0909.4635))

* Johan Bijnens, _Status of Strong ChPT_, PoS EFT09 (2009) 022 ([spire:818610](http://inspirehep.net/record/818610/))

* {#MachleidtEntem11} [[Rupert Machleidt]], [[David Rodríguez Entem]], _Chiral effective field theory and nuclear forces_, Phys. Rept. 503:1-75, 2011 ([arXiv:1105.2919](https://arxiv.org/abs/1105.2919), [doi:10.1016/j.physrep.2011.02.001](https://doi.org/10.1016/j.physrep.2011.02.001))

* [[Franco Strocchi]], §8 of: _An Introduction to Non-Perturbative Foundations of Quantum Field Theory_, Oxford University Press (2013) &lbrack;[doi:10.1093/acprof:oso/9780199671571.001.0001](https://doi.org/10.1093/acprof:oso/9780199671571.001.0001)&rbrack;

  (in a context of [[non-perturbative quantum field theory]])


* {#Brambilla14} Brambilla et al., Sections 3-4 in: _[[QCD and strongly coupled gauge theories - challenges and perspectives]]_, Eur Phys J C Part Fields. 2014; 74(10): 2981  ([arXiv:1404.3723](https://arxiv.org/abs/1404.3723), [doi:10.1140/epjc/s10052-014-2981-5](https://link.springer.com/article/10.1140%2Fepjc%2Fs10052-014-2981-5))


* Yong-Liang Ma, Masayasu Harada, Section II.B of: _Lecture notes on the Skyrme model_ ([arXiv:1604.04850](https://arxiv.org/abs/1604.04850), [spire:1448311](https://inspirehep.net/literature/1448311))


* [[Franz Gross]], [[Eberhard Klempt]] et al., Section 6.2 of: *50 Years of Quantum Chromodynamics*, EJPC &lbrack;[arXiv:2212.11107](https://arxiv.org/abs/2212.11107)&rbrack;



See also:

* Wikipedia, _[Chiral perturbation theory](https://en.wikipedia.org/wiki/Chiral_perturbation_theory)_ 

As [[quantum hadrodynamics]]:

* Brian D. Serot, _Quantum hadrodynamics_, Rept.Prog.Phys. 55 (1992) 1855-1946, ([spire:333292](http://inspirehep.net/record/333292), [doi:10.1088/0034-4885/55/11/001](https://doi.org/10.1088/0034-4885/55/11/001))

* Brian D. Serot, John Dirk Walecka, _Recent Progress in Quantum Hadrodynamics_, Int. J. Mod. Phys. E6:515-631, 1997 ([arXiv:nucl-th/9701058](https://arxiv.org/abs/nucl-th/9701058))


Via the [[S-matrix]]/[[scattering amplitudes]] of [[mesons]]:

* Andrea Guerrieri, Joao Penedones, Pedro Vieira, _S-matrix Bootstrap for Effective Field Theories: Massless Pions_ ([arXiv:2011.02802](https://arxiv.org/abs/2011.02802))

* Eef van Beveren, George Rupp, _Modern meson spectroscopy: the fundamental role of unitarity_ ([arXiv:2012.03693](https://arxiv.org/abs/2012.03693))




### Original articles

* [[Sidney Coleman]], [[Julius Wess]], [[Bruno Zumino]], _Structure of Phenomenological Lagrangians. I_, Phys. Rev. 177, 2239 (1969) ([doi:10.1103/PhysRev.177.2239](https://doi.org/10.1103/PhysRev.177.2239))

* [[Curtis Callan]], Jr., [[Sidney Coleman]], [[Julius Wess]], [[Bruno Zumino]], _Structure of Phenomenological Lagrangians. II_, Phys. Rev. 177, 2247 (1969) ([doi:10.1103/PhysRev.177.2247](https://doi.org/10.1103/PhysRev.177.2247))

* {#Weinberg79} [[Steven Weinberg]], _Phenomenological Lagrangians_, Physica A: Statistical Mechanics and its Applications Volume 96, Issues 1–2, April 1979, Pages 327-340 (<a href="https://doi.org/10.1016/0378-4371(79)90223-1">doi:10.1016/0378-4371(79)90223-1</a>)

* {#tHooft1980} [[Gerard 't Hooft]], *Naturalness, Chiral Symmetry, and Spontaneous Chiral Symmetry Breaking* In: G. 'Hooft et al., *Recent Developments in Gauge Theories*, NATO Advanced Study Institutes Series **59**, Springer (1980) &lbrack;[doi:10.1007/978-1-4684-7571-5_9](https://doi.org/10.1007/978-1-4684-7571-5_9)&rbrack;

* [[Jürg Gasser]], [[Heinrich Leutwyler]], _Quark masses_, Physics Reports Volume 87, Issue 3, July 1982, Pages 77-169 (<a href="https://doi.org/10.1016/0370-1573(82)90035-7">doi:10.1016/0370-1573(82)90035-7</a>)

* [[Jürg Gasser]], [[Heinrich Leutwyler]], _Chiral Perturbation Theory: Expansions in the Mass of the Strange Quark_, Nucl. Phys. B 250 (1985) 465-516, ([spire:200027](https://inspirehep.net/literature/200027), <a href="https://doi.org/10.1016/0550-3213(85)90492-4">doi:10.1016/0550-3213(85)90492-4</a>))


* [[Jürg Gasser]], [[Heinrich Leutwyler]], _Chiral perturbation theory to one loop_, Annals of Physics Volume 158, Issue 1, November 1984, Pages 142-210 (<a href="https://doi.org/10.1016/0003-4916(84)90242-2">doi:10.1016/0003-4916(84)90242-2</a>)


* [[Gerard 't Hooft]], _How instantons solve the $U(1)$ problem_, Physics Reports Volume 142, Issue 6, September 1986, Pages 357-387 (<a href="https://doi.org/10.1016/0370-1573(86)90117-1">doi:10.1016/0370-1573(86)90117-1</a>)

* [[Heinrich Leutwyler]], _On the Foundations of Chiral Perturbation Theory_, Annals Phys. 235 (1994) 165-203 ([arXiv:hep-ph/9311274](https://arxiv.org/abs/hep-ph/9311274))

At higher order:

* Nils Hermansson-Truedsson, _Chiral Perturbation Theory at NNNLO_ ([arXiv:2006.01430](https://arxiv.org/abs/2006.01430))



Specifically for [[kaon]] decay:

* V. Cirigliano, [[Gerhard Ecker]], [[Helmut Neufeld]], [[Antonio Pich]], J. Portoles, _Kaon Decays in the Standard Model_, Rev. Mod. Phys. 84 (2012) 399 ([arXiv:1107.6001](https://arxiv.org/abs/1107.6001))

Further discussion of [[phenomenology]]:

* Prabal Adhikari, Jens O. Andersen, _Quark and pion condensates at finite isospin density in chiral perturbation theory_ ([arXiv:2003.12567](https://arxiv.org/abs/2003.12567))

* Bryan W. Lynn, Brian J. Coffey, Kellen E. McGee, Glenn D. Starkman, _Nuclear matter as a liquid phase of spontaneously broken semi-classical $SU(2)_L \times SU(2)_R$ chiral perturbation theory: Static chiral nucleon liquids_ ([arXiv:2004.01706](https://arxiv.org/abs/2004.01706))

See also


* Yu-Jia Wang, Feng-Kun Guo, Cen Zhang, Shuang-Yong Zhou, _Generalized positivity bounds on chiral perturbation theory_ ([arXiv:2004.03992](https://arxiv.org/abs/2004.03992))


* Lukas Graf, Brian Henning, Xiaochuan Lu, Tom Melia, Hitoshi Murayama, _2, 12, 117, 1959, 45171, 1170086, ...: A Hilbert series for the QCD chiral Lagrangian_ ([arXiv:2009.01239](https://arxiv.org/abs/2009.01239))






[[!include Skyrme hadrodynamics with vector mesons -- references]]



[[!include Skyrme hadrodynamics with heavy mesons -- references]]



[[!include WZW term of QCD chiral perturbation theory -- references]]


[[!include baryon chiral perturbation theory -- references]]


### Applications to lattice QCD

Application to [[lattice QCD]]:

* {#Sharpe:2006pu} S.R.Sharpe, Applications of Chiral Perturbation theory to lattice QCD, ILFTN Workshop on "Perspectives in Lattice QCD", Nara, Japan, Oct 31-Nov 11 2005, 2006 ([arXiv:hep-lat/0607016](https://arxiv.org/abs/hep-lat/0607016v2))







### Inclusion of leptons

On [[chiral perturbation theory]] including [[leptons]]:



* M. Knecht, [[Helmut Neufeld]], H. Rupertsberger, P. Talavera, _Chiral Perturbation Theory with Virtual Photons and Leptons_, Eur. Phys. J. C12:469-478, 2000 ([arXiv:hep-ph/9909284](https://arxiv.org/abs/hep-ph/9909284))


* [[Helmut Neufeld]], _Chiral Perturbation Theory with Photons and Leptons_, PiN Newslett. 15:189-192, 1999 ([arXiv:hep-ph/9912462](https://arxiv.org/abs/hep-ph/9912462))

Specifically in relation to the [[Skyrme model]]:

* [[Eric D'Hoker]], Edward Farhi, _The decay of the skyrmion_, Physics Letters B Volume 134, Issues 1–2, 5 January 1984, Pages 86-90 (<a href="https://doi.org/10.1016/0370-2693(84)90991-2">doi:10.1016/0370-2693(84)90991-2</a>)







### Antisymmetric tensor representation for vector mesons
 {#ReferencesAntisymmetricTensorRepOfVectorMesons}

The formulation of vector mesons in "antisymmetric tensor representation":

Original articles:

* [[Jürg Gasser]], [[Heinrich Leutwyler]], Appendix C of: _Chiral perturbation theory to one loop_, Annals of Physics Volume 158, Issue 1, November 1984, Pages 142-210 (<a href="https://doi.org/10.1016/0003-4916(84)90242-2">doi:10.1016/0003-4916(84)90242-2</a>)

* [[Gerhard Ecker]], [[Jürg Gasser]], [[Antonio Pich]], E. DeRafael, Sec 3 and Appendix A in: _The role of resonances in chiral perturbation theory_, Nuclear Physics B
Volume 321, Issue 2, 24 July 1989, Pages 311-342 (<a href="https://doi.org/10.1016/0550-3213(89)90346-5">doi:10.1016/0550-3213(89)90346-5</a>)

Relation between the vector- and the antisymmetric tensor-representation of vector mesons:

* Karol Kampf, Jiri Novotny, Jaroslav Trnka, _On different lagrangian formalisms for vector resonances within chiral perturbation theory_, Eur. Phys. J. C50:385-403, 2007 ([arXiv:hep-ph/0608051](https://arxiv.org/abs/hep-ph/0608051))

See also


* V. Dmitrašinović, around (11) in: _Axial baryon number nonconserving antisymmetric tensor four-quark effective interaction_, Phys. Rev. D 62, 096010 (2000) ([doi:10.1103/PhysRevD.62.096010](https://doi.org/10.1103/PhysRevD.62.096010))

Further application of the antisymmetric tensor representation of vector mesons to [[quantum hadrodynamics]]:

* [[Stefan Leupold]], Carla Terschlusen, _Towards an effective field theory for vector mesons_, Talk presented at the 50th International Winter Meeting on Nuclear Physics, 23-27 January 2012, Bormio ([arXiv:1206.2253](https://arxiv.org/abs/1206.2253))

* Carla Terschlusen, [[Stefan Leupold]], M. F. M. Lutz, _Electromagnetic transitions in an effective chiral Lagrangian with the eta-prime and light vector mesons_, Eur. Phys. J. A 48, 190 (2012) ([arXiv:1204.4125](https://arxiv.org/abs/1204.4125))



[[!redirects chiral symmetry breaking]]

[[!redirects chiral symmetry]]
[[!redirects chiral symmetries]]





