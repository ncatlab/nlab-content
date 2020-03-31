
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Fields and quanta
+--{: .hide}
[[!include fields and quanta - table]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

What is called _[[chiral perturbation theory]]_ in [[quantum field theory]] of [[nuclear physics]] is the [[effective field theory]] of [[quantum chromodynamics]] in the [[confinement|confined]] sector of light [[quarks]], where the effective [[field (physics)|fields]] are [[hadrons]] ([[mesons]] being [[gauge fields]] of a [[hidden local symmetry]], and [[baryons]]/[[nuclei]] being the [[fermions]]), whence one also speaks of _quantum hadrodynamics_.

This is thus [[perturbation theory]] not in the [[coupling constant]] of [[QCD]], but in the [[masses]] of the light quarks, which in practice means: of the [[up quark]] and the [[down quark]] and possibly also of the [[strange quark]].

As such, the point about which [[perturbation theory|perturbations]] are considered in chiral perturbation theory of QCD is that of vanishing [[quark]] masses. But since only the quark mass term in the [[Lagrangian density]] mixes the two [[Weyl spinor|chiralities]] of quarks, the Lagrangian in this massless limit is the sum of a term that only contains the left-chiral quark spinors, and an analogous summand that only contains the right-chiral  quark spinors.

Moreover, all two ([[up quark|up]] and [[down quark|down]]) or even all three (if including [[strange quark|strange]]) [[flavour (particle physics)|flavours]] of quarks enter each of these two spinor-chiral summands symmetrically, such that each of them has [[SU(2)]] or respectively [[SU(3)]] [[global symmetry]], [[action|acting]] by mixing the quark flavours. This yields a total [[direct product group|direct product]] [[symmetry group]] 

$$
  G = SU(N_f)_L \times SU(N_f)_R
  \,,
$$

where $N_f \in \{ 2,3 \}$ is the [[number]] of [[flavour (particle physics)|flavours]] of light [[quarks]] that are being considered, and where the subscripts indicate the left/right-handed [[chiral spinor]]-components of quarks whose [[flavour (particle physics)|flavours]] are being mixed by these [[group]] [[actions]]. This [[symmetry group]] is hence also called _chiral symmetry_. Accordingly, its [[symmetry breaking]] to the [[diagonal morphism|diagonal]] [[subgroup]]

$$
  SU(N_f)_V
  \;\subset\;
  SU(N_f)_L \times SU(N_f)_R
$$

(the subscript "$V$" is for "vector") either explicitly by [[positive number|positive]] [[quark]] [[masses]] or [[spontaneous symmetry breaking|spontaneously]] by a [[vacuum expectation value]] $\langle \bar q q\rangle = \langle \bar q_L q_R\rangle + \langle \bar q_R q_L\rangle$, is called _[[chiral symmetry breaking]]. This is the origin of the term _chiral perturbation theory_.

(...)

## Properties

### Relation to the Skyrme model

* [[Dmitri Diakonov]], [[Victor Petrov]], _Exotic baryon resonances in the Skyrme model_ ([arXiv:0812.1212](https://arxiv.org/abs/0812.1212), [doi:10.1142/9789814704410_0004](https://doi.org/10.1142/9789814704410_0004)), Chapter 3 in: _[[The Multifaceted Skyrmion]]_, World Scientific 2016 ([doi:10.1142/9710](https://doi.org/10.1142/9710))

> It is astounding that [[Tony Skyrme|Skyrme]] had suggested [[Skyrmion|his model]] as early as in 1961 before it has been generally accepted that [[pions]] are (pseudo) [[Goldstone bosons]] associated with the [[spontaneous symmetry breaking|spontaneous breaking]] of [[chiral symmetry]], and of course long before [[QCD|Quantum Chromodynamics (QCD)]] has been put forward as the microscopic theory of [[strong nuclear force|strong interactions]].

> The revival of the Skyrme idea in 1983 is [due to Witten](Skyrmion#Witten83) who explained the _raison d'ˆetre_ of the [[Skyrmion|Skyrme model]] from the viewpoint of [[QCD]]. In the [[chiral perturbation theory|chiral limit]] when the light [[quark]] masses $m_u$, $m_d$, $m_s$ tend to zero, such that the octet of the pseudoscalar mesons [[pion|π]], [[kaon|K]] , η become nearly massless (pseudo) [[Goldstone bosons]], they are the lightest degrees of freedom of [[QCD]]. The [[effective field theory|effective]] chiral Lagrangian (EχL) for pseudoscalar mesons, understood as an infinite expansion in the derivatives of the pseudoscalar (or chiral) fields, encodes, in principle, full information about QCD. The famous two-term Skyrme Lagrangian can be understood as a low-energy truncation of this infinite series. Witten has added an important four-derivative [[WZW-term|Wess–Zumino term]] to the original Skyrme Lagrangian and pointed out that the overall coefficient in front of the EχL is proportional to the number of quark [[color charge|colours]] $N_c$.

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


## Related concepts

* [[confinement]]

* [[chiral symmetry breaking]]

* [[quark bag model]], [[Cheshire cat principle]]

* [[hidden local symmetry]]

* [[vector meson dominance]]

* [[Walecka model]]

* [[holographic QCD]]

## References

### Introduction and review

* [[Jürg Gasser]], _The QCD Vacuum and Chiral Symmetry_, In: Vautherin D., Lenz F., Negele J.W. (eds.) _Hadrons and Hadronic Matter_, NATO ASI Series (Series B: Physics), vol 228. Springer 1990 ([doi:10.1007/978-1-4684-1336-6_4](https://doi.org/10.1007/978-1-4684-1336-6_4))

* Volker Koch, _Aspects of Chiral Symmetry_, Int. J. Mod. Phys. E6 (1997) 203-250 ([arXiv:nucl-th/9706075](https://arxiv.org/abs/nucl-th/9706075))


* Véronique Bernard, Ulf-G. Meißner, _Chiral perturbation theory_, Ann. Rev. Nucl. Part. Sci.57:33-60, 2007 ([arXiv:hep-ph/0611231](https://arxiv.org/abs/hep-ph/0611231))

* Véronique Bernard, _Chiral Perturbation Theory and Baryon Properties_, Prog. Part. Nucl. Phys. 60:82-160, 2008 ([arXiv:0706.0312](https://arxiv.org/abs/0706.0312))

* Gerhard Ecker, _Status of chiral perturbation theory_, PoS Confinement 8:025, 2008 ([arXiv:0812.4196](https://arxiv.org/abs/0812.4196))


* Johan Bijnens, _Chiral perturbation theory in the meson sector_, PoS CD09:031, 2009 ([arXiv:0909.4635](https://arxiv.org/abs/0909.4635))

* Johan Bijnens, _Status of Strong ChPT_, PoS EFT09 (2009) 022 ([spire:818610](http://inspirehep.net/record/818610/))

* {#MachleidtEntem11} [[Rupert Machleidt]], [[David Rodríguez Entem]], _Chiral effective field theory and nuclear forces_, Phys. Rept. 503:1-75, 2011 ([arXiv:1105.2919](https://arxiv.org/abs/1105.2919), [doi:10.1016/j.physrep.2011.02.001](https://doi.org/10.1016/j.physrep.2011.02.001))

See also:

* Wikipedia, _[Chiral perturbation theory](https://en.wikipedia.org/wiki/Chiral_perturbation_theory)_ 

As [[quantum hadrodynamics]]:

* Brian D. Serot, _Quantum hadrodynamics_, Rept.Prog.Phys. 55 (1992) 1855-1946, ([http://inspirehep.net/record/333292](http://inspirehep.net/record/333292), [doi:10.1088/0034-4885/55/11/001](https://doi.org/10.1088/0034-4885/55/11/001))


* Brian D. Serot, John Dirk Walecka, _Recent Progress in Quantum Hadrodynamics_, Int. J. Mod. Phys. E6:515-631, 1997 ([arXiv:nucl-th/9701058](https://arxiv.org/abs/nucl-th/9701058))




### Original articles

* [[Sidney Coleman]], [[Julius Wess]], [[Bruno Zumino]], _Structure of Phenomenological Lagrangians. I_, Phys. Rev. 177, 2239 (1969) ([doi:10.1103/PhysRev.177.2239](https://doi.org/10.1103/PhysRev.177.2239))

* [[Curtis Callan]], Jr., [[Sidney Coleman]], [[Julius Wess]], [[Bruno Zumino]], _Structure of Phenomenological Lagrangians. II_, Phys. Rev. 177, 2247 (1969) ([doi:10.1103/PhysRev.177.2247](https://doi.org/10.1103/PhysRev.177.2247))

* {#Weinberg79} [[Steven Weinberg]], _Phenomenological Lagrangians_, Physica A: Statistical Mechanics and its Applications Volume 96, Issues 1–2, April 1979, Pages 327-340 (<a href="https://doi.org/10.1016/0378-4371(79)90223-1">doi:10.1016/0378-4371(79)90223-1</a>)

* [[Jürg Gasser]], [[Heinrich Leutwyler]], _Chiral Perturbation Theory: Expansions in the Mass of the Strange Quark_, Nucl. Phys. B 250 (1985) 465-516, ([spire:200027](https://inspirehep.net/literature/200027), <a href="https://doi.org/10.1016/0550-3213(85)90492-4">doi:10.1016/0550-3213(85)90492-4</a>))


* [[Jürg Gasser]], [[Heinrich Leutwyler]], _Chiral perturbation theory to one loop_, Annals of Physics
Volume 158, Issue 1, November 1984, Pages 142-210 (<a href="https://doi.org/10.1016/0003-4916(84)90242-2">doi:10.1016/0003-4916(84)90242-2</a>)


* [[Gerard 't Hooft]], _How instantons solve the $U(1)$ problem_, Physics Reports Volume 142, Issue 6, September 1986, Pages 357-387 (<a href="https://doi.org/10.1016/0370-1573(86)90117-1">doi:10.1016/0370-1573(86)90117-1</a>)

* [[Heinrich Leutwyler]], _On the Foundations of Chiral Perturbation Theory_, Annals Phys. 235 (1994) 165-203 ([arXiv:hep-ph/9311274](https://arxiv.org/abs/hep-ph/9311274))


Specifically for [[kaon]] decay:

* V. Cirigliano, G. Ecker, H. Neufeld, A. Pich, J. Portoles, _Kaon Decays in the Standard Model_, Rev. Mod. Phys. 84 (2012) 399 ([arXiv:1107.6001](https://arxiv.org/abs/1107.6001))

Further discussion of [[phenomenology]]:

* Prabal Adhikari, Jens O. Andersen, _Quark and pion condensates at finite isospin density in chiral perturbation theory_ ([arXiv:2003.12567](https://arxiv.org/abs/2003.12567))




[[!include WZW term of QCD chiral perturbation theory -- references]]





[[!redirects chiral symmetry breaking]]

[[!redirects chiral symmetry]]
[[!redirects chiral symmetries]]

[[!redirects quantum hadrodynamics]]

