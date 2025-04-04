

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Simons theory
+--{: .hide}
[[!include infinity-Chern-Simons theory - contents]]
=--
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Topological physics
+--{: .hide}
[[!include topological physics -- contents]]
=--
=--
=--



\tableofcontents

## Idea

By *abelian Chern-Simons theory* one means [[Chern-Simons theory]] with [[abelian group|abelian]] [[gauge group]] (typically the [[circle group]] or a [[torus]]-[[product group|product]] of copies of these).

One major application of abelian Chern-Simons theory is as an [[effective field theory]] of the [[fractional quantum Hall effect]].


## Properties

### Space of quantum states
 {#SpaceOfQuantumStates}

For abelian Chern-Simons theory with $N$ [[gauge fields]] $(A_i)_{i = 1}^N$ and [[Lagrangian density]] of the form (using [[Einstein summation convention]]) $K^{i j} A_i \wedge \mathrm{d} A_j$, for $K$ an $N \times N$ *even* [[integer]] [[symmetric matrix]] (the diagonal entries are [[even numbers]]), the [[dimension of a vector space|dimension]] of the [[Hilbert space|Hilbert]] [[space of quantum states]] $\mathscr{H}_g$ (obtained by [[geometric quantization]], cf. *[[quantization of D=3 Chern-Simons theory]]*) over an [[orientation|orientable]] [[surface]] of [[genus of a surface|genus]] $g$ is the [[absolute value]] of the [[determinant]] of $K$ raised to the $g$th [[exponent|power]]:

$$ 
  dim(\mathscr{H}_g)
  \;=\;
  \left\vert det(K)\right\vert^g
  \,.
$$

(for $g = 1$ this is [Wesolowski, Hosotani & Ho 1994 (3.25)](#WesolowskiHosotaniHo94), for  $N=1$ see [Manoliu 1998a p 40](#Manoliu98a), for general $N$ this goes back to [Wen & Zee 1992 (1.2)](#WenZee92Classification), recalled in [Fradkin 2013 (14.23)](#Fradkin13), [Belov & Moore 2005 p 26](#BelovMoore05)).

For the [[modular group]]-[[group action|action]] on these state spaces see at *[[integer Heisenberg group]]* the section *[Modular automorphisms](integer+Heisenberg+group#ModularAutomorphisms)* (there for $g=1$).


{#DegeneracyOnNonOrientableSurface} For a *non-*orientable surface with $k$ crosscaps, it is 

$$ 
  dim(\mathscr{H}_k)
  \;=\;
  \left\vert det(K)\right\vert^{k-1}
  \,.
$$

(e.g. [arXiv:1509.03920](https://arxiv.org/abs/1509.03920) (73))



\linebreak


### Abelian Chern-Simons as effective QFT for FQH systems
 {#AbelianCSTheoryAsEffectiveQFTForFRactionalQuantumHall}

The following is a streamlined digest of the traditional argument and Ansatz &lbrack;originally culminating in [Zee 1995](#Zee95), [Wen 1995](#Wen95), more recently highlighted by [Witten 2016 pp 30](#Witten16), [Tong 2016 §5](#Tong16)&rbrack; for [[abelian Chern-Simons theory]] at [[level (Chern-Simons theory)|level]] $k \in \mathbb{N}$ as an [[effective field theory]] for [[fractional quantum Hall systems]] at filling fraction $\nu = 1/k$.


\linebreak


#### Preliminaries

Consider a [[spacetime]] $\Sigma$ of [[dimension of a manifold|dimension]] $1 + 2$, to be thought of as the [[worldvolume]] of the conducting sheet that hosts the [[fractional quantum Hall system]].

On this spacetime, the electric [[current density]] is a [[differential 2-form]] $J$.

Note that the corresponding electric current [[vector field]] $\vec J$ is characterized by its [[tensor contraction|contraction]] into the given [[volume form]] $dvol$ being equal to the density 2-form

$$
  J \;=\; dvol\big(\, \vec J, \cdots \big)
  \,,
$$

and that the conservation law for $\vec J$, hence the vanishing of its [[divergence]] is equivalent to the density 2-form being [[closed differential form]]:

\[
  \label{CurrentConservationLaw}
  div \vec J \;=\; 0
  \;\;\;\;\;\;
  \Leftrightarrow
  \;\;\;\;\;\;
  \mathrm{d} J \;=\; 0
  \,.
\]

We write $A$ for the [[vector potential]] 1-form on $\Sigma$ which encodes the [[background field|background]] [[electromagnetic field]], and $F \,=\, \mathrm{d}A$ for its [[field strength]], the [[Faraday tensor]]. Since we regard this as a fixed [[background field]], we do not (need to) consider the Maxwell [[Lagrangian density]] $L_{YM} \,\coloneqq\, F \wedge \star F$.

But we do (need to) consider the interaction term between the electromagnetic field and the electric current density, which is 

\[
  \label{ElectricInteractionTerm}
  L_{int} \,\coloneqq\, A \wedge J
  \,.
\]

Here we assume that $A$ is globally defined, in fact we shall assume that $\Sigma$ has vanishing [[de Rham cohomology]] in degree=2,

\[
  \label{AssumingdeRham2CohomologyVanishes}
  H^2_{dR}(\Sigma) \;=\; 0
  \,.
\]

This means we are focused on the local nature of fields, not on their global properties, as (for better or worse) usual for [[Lagrangian field theory]].
 
\linebreak


#### The Ansatz

**The auxiliary gauge potential.**
With the assumption (eq:AssumingdeRham2CohomologyVanishes) also the conserved current density (eq:CurrentConservationLaw) admits a [[coboundary]], a [[differential 1-form]] to be denoted $a$:

$$
  J \,=\, \mathrm{d}a
  \,.
$$

The central Ansatz of the approach is to *think of this 1-form as an effective dynamical gauge field for the FQH dynamics*.

\linebreak

**The Lagrangian density.** This in turn suggests that the effective [[Lagrangian density]] should be the sum of

1. the interaction term (eq:ElectricInteractionTerm) already mentioned, which thus specializes to

   $$
     L_{int} \;=\; A \wedge J \;=\; A \wedge \mathrm{d}a
     \,,
   $$

1. a further interaction term for $a$, now regarded as a gauge potential, to its own current density $j$, to be thought of as the current of FQH [[quasi-particles]] (or quasi-holes)

   $$
     L_{quas} \;=\; a \wedge j
   $$

1. a dynamical term for $a$ itself, where the only sensible choice is the [[Chern-Simons theory|Chern-Simons form]] at [[level (Chern-Simons theory)|level]] $k$

   $$
     L_{CS} \;=\; k \tfrac{1}{2} a \wedge \mathrm{d}a
     \,.
   $$

In total, the traditional Ansatz for the effective Lagrangian density for "single layer" FQH systems at filling fraction $1/k$ is hence:

\[
  \label{TheEffectiveLagrangianDensity}
  L 
  \,\coloneqq\,
  k \tfrac{1}{2}\, a\wedge \mathrm{d}a
  \,-\,
  A \wedge 
  \underset{J}{
    \underbrace{
      \mathrm{d}a
    }
  }
  \,+\,
  a \wedge j
  \,.
\]

&lbrack;[Wen 1995 (2.11)](#Wen95)&rbrack;

\linebreak

**The equation of motion.**
The [[Euler-Lagrange equation]] [[equation of motion|of motion]] for the effective gauge field $a$ induced by (eq:TheEffectiveLagrangianDensity) is simply

\[
  \label{EquationOfMotion}
  \frac{\delta L}{\delta A}
  \;=\;
  0
  \;\;\;\;\;\;\;\;\;\;
  \Leftrightarrow
  \;\;\;\;\;\;\;\;\;\;
  J
    \,=\,
  \tfrac{1}{k}\Big(
    F - j
  \Big)
  \,.
\]

> (This means in particular that if, on topologically non-trivial $\Sigma$, one were to insist (which is not a logical necessity) to subject the effective gauge field $a$ to [[Dirac charge quantization]] (as $A$ is), then the ordinary electromagnetic field would have to be assumed to carry magnetic charge being a multiple of $k$.)

\linebreak

#### Reproducing FQH phenomena

**Recovering the Hall conductivity.**
The first plausibility check on the effective model is to observe that its equation of motion (eq:EquationOfMotion) implies the correct Hall conductivity relation for a [[fractional quantum Hall system]] at filling fraction $1/k$:

Namely assuming that the electric field is oriented in the $y$-direction, so that the [[Faraday tensor]] is of the form (cf [there](Maxwell's+equations#InTermsOfFaradayTensor)):

$$
  F 
  \;=\;
  E_y \mathrm{d}t \wedge \mathrm{d}y
  +
  B \mathrm{d}x\wedge \mathrm{d}y
$$

and assuming that the quasi-particles are stationary, so that 

$$
  j 
    \;\propto\; 
  dvol(\partial_0) 
    \;\propto\; 
  \mathrm{d}x \wedge \mathrm{d}y
  \mathrlap{\,,}
$$

the temporal component of the equation of motion (eq:EquationOfMotion) becomes

$$
  J_x \;=\; \tfrac{1}{k} E_y
$$

which is the correct form of the *Hall field* $E_y$ for given longitudinal current $J_X$ at filling fraction $\nu = 1/k$ -- see [there](quantum+Hall+effect#eq:HeightOfFractionalHallPlateaux).

> (Following [Zee 1995 (4.5)](#Zee95), later authors &lbrack;[Witten 2016 §2.3](#Witten16), [Tong 2016 p 161](#Tong16)&rbrack; deduce this in a more roundabout way, by first inserting the equation of motion back into the Lagrangian density and then varying that with respect to $A$. It seems that this unnecessary step is brought about by first tacitly renaming "$J$" to "$f$" and then forgetting that this was just a renaming.)

\linebreak

**Recovering the fractional quasi-particles.**
Second, the spatial component of the equation of motion (eq:EquationOfMotion) says that (1.) the magnetic flux quanta and (2.) the quasi-particles contribute their $k$th fraction to the total charge density:

$$
  J_0 \;=\; \tfrac{1}{k}(B - j_0)
  \,.
$$

Here 

* statement (1) reflects exactly the composite fermion model, where at $k$th filling fraction each electron is bound to $k$ quanta of magnetic flux 

* statement (2) is the desired property of quasi-holes to have $k$th fractional charge.


\linebreak

This largely concludes the traditional justification for the effective abelian Chern-Simons theory (eq:TheEffectiveLagrangianDensity).


\linebreak





## Related concepts

* [[Chern-Simons theory]]

* [[quantization of D=3 Chern-Simons theory]]

* [[fractional quantum Hall effect]]

* [[integer Heisenberg group]]



## References

### General

* Michiel Bos, [[V. Parameswaran Nair]]: *$U(1)$ Chern-Simons theory and $c=1$ conformal blocks*, Physics Letters B **223** 1 (1989) 61-66 \[<a href="https://doi.org/10.1016/0370-2693(89)90920-9">doi:10.1016/0370-2693(89)90920-9</a>\]

* [[Alexios P. Polychronakos]]: *Abelian Chern-Simons theories in $2+1$ dimensions*, Annals of Physics **203** 2 (1990) 231-254 \[<a href="https://doi.org/10.1016/0003-4916(90)90171-J">doi:10.1016/0003-4916(90)90171-J</a>\] 

* [[Sergio Albeverio]], J. Schäfer: *Rigorous Approach to Abelian Chern-Simons Theory*, in *Groups and Related Topics*, Mathematical Physics Studies **13**,  Springer (1992) 143-152 &lbrack;[doi:10.1007/978-94-011-2801-8_12](https://doi.org/10.1007/978-94-011-2801-8_12)&rbrack;

* {#WesolowskiHosotaniHo94} D. Wesolowski, Y. Hosotani, C.-L. Ho: *Multiple Chern-Simons Fields on a Torus*,  	Int. J. Mod. Phys. A **9** (1994) 969-989 &lbrack;[arXiv:hep-th/9302121](https://arxiv.org/abs/hep-th/9302121), [doi:10.1142/S0217751X94000443](https://doi.org/10.1142/S0217751X94000443)&rbrack;


* G. Giavarini, C. P. Martin, F. Ruiz Ruiz: *Abelian Chern-Simons theory as the strong large-mass limit of topologically massive abelian gauge theory: the Wilson loop*, Nucl.Phys. B **412** (1994) 731-750 &lbrack;[arXiv:hep-th/9309049](https://arxiv.org/abs/hep-th/9309049), <a href="https://doi.org/10.1016/0550-3213(94)90397-2">doi:10.1016/0550-3213(94)90397-2</a>, [pdf](https://inis.iaea.org/collection/NCLCollectionStore/_Public/25/053/25053343.pdf)&rbrack;

* {#Manoliu98a} Mihaela Manoliu: *Abelian Chern-Simons theory*, J. Math. Phys. **39** (1998) 170-206 &lbrack;[arXiv:dg-ga/9610001](https://arxiv.org/abs/dg-ga/9610001), [doi:10.1063/1.532333](https://doi.org/10.1063/1.532333)&rbrack;

* {#Manoliu98b} Mihaela Manoliu: *Abelian Chern-Simons theory. II: A functional integral approach*, J. Math.Phys. **39** (1998) 207-217 &lbrack;[doi:10.1063/1.532312](https://doi.org/10.1063/1.532312)&rbrack;

* {#BelovMoore05} Dmitriy Belov, [[Gregory W. Moore]]: *Classification of abelian spin Chern-Simons theories* &lbrack;[arXiv:hep-th/0505235](https://arxiv.org/abs/hep-th/0505235)&rbrack;
  > (with focus on refinement to [[Spin Chern-Simons theory]])

* Spencer D. Stirling: *Abelian Chern-Simons theory with toral gauge group, modular tensor categories, and group categories*, PhD thesis, Austin (2008) &lbrack;[arXiv:0807.2857](http://arxiv.org/abs/0807.2857), [pdf](http://www.spencerstirling.com/papers/thesis_official.pdf), [ProQuest](https://www.proquest.com/docview/304474017?pq-origsite=gscholar&fromopenview=true&sourcetype=Dissertations%20&%20Theses)&rbrack;

* [[Lisa Jeffrey]], Brendan McLellan: *Eta-Invariants and Anomalies in $U(1)$ Chern-Simons Theory* &lbrack;[arXiv:1004.2913](https://arxiv.org/abs/1004.2913)&rbrack;


* Diego Delmastro, [[Jaume Gomis]]: *Symmetries of Abelian Chern-Simons Theories and Arithmetic*, J. High Energ. Phys. **2021** 6 (2021) &lbrack;<a href="https://doi.org/10.1007/JHEP03(2021)006">doi:10.1007/JHEP03(2021)006</a>, [arXiv:1904.12884](https://arxiv.org/abs/1904.12884)&rbrack;

* Han-Miru Kim, Philippe Mathieu, Michail Tagaris, Frank Thuillier: *$U(1)^n$ Chern-Simons theory: partition function, reciprocity formula and CS-duality* &lbrack;[arXiv:2409.10734](https://arxiv.org/abs/2409.10734)&rbrack;


Via the [[Reshetikhin-Turaev construction]]:

* Enore Guadagnini, Francesco Mancarella: *Abelian link invariants and homology*, J. Math. Phys. **51** (2010) 062301 &lbrack;[arXiv:1004.5211](https://arxiv.org/abs/1004.5211)&rbrack;

* Philippe Mathieu, Frank Thuillier: *Abelian Turaev-Virelizier theorem and $U(1)$ BF surgery formulas* &lbrack;[arXiv:1706.01845](https://arxiv.org/abs/1706.01845)&rbrack;


Many general reviews of [[Chern-Simons theory]] have a section focused on the abelian case, for instance:

* [[Gregory Moore]], §2 in: *Introduction to Chern-Simons Theories*, TASI lecture notes (2019) &lbrack;[pdf](https://www.physics.rutgers.edu/~gmoore/TASI-ChernSimons-StudentNotes.pdf), [[Moore-IntroChern-Simons.pdf:file]]&rbrack;

* David Grabovsky, §1 in: *Chern–Simons Theory in a Knotshell* (2022) &lbrack;[pdf](https://web.physics.ucsb.edu/~davidgrabovsky/files-notes/CS%20and%20Knots.pdf), [[Grabovsky-CSTheory.pdf:file]]&rbrack;


On the [[light-cone quantization]] of abelian Chern-Simons theory:

* Prem P. Srivastava: *Light-Front Dynamics of Chern-Simons Systems* &lbrack;[arXiv:hep-th/9412239](https://arxiv.org/abs/hep-th/9412239)&rbrack;

* L. R. U. Manssur: *Canonical Quantization of Chern-Simons on the Light-Front*, Phys. Lett. B **480** (2000) 229-236 &lbrack;[arXiv:hep-th/9910127v1](https://arxiv.org/abs/hep-th/9910127), <a href="https://doi.org/10.1016/S0370-2693(00)00380-4">doi:10.1016/S0370-2693(00)00380-4</a>&rbrack;

On [[boundary conditions]] and line-[[defect field theory|defects]] in abelian Chern-Simons theory and on the corresponding ground state degeneracy ([[topological order]]) on [[surfaces]] with ("gapped") [[boundary of a manifold|boundaries]]:

* [[Anton Kapustin]], [[Natalia Saulina]]: *Topological boundary conditions in abelian Chern-Simons theory*, Nucl. Phys. B **845** (2011) 393-435 &lbrack;[arXiv:1008.0654](https://arxiv.org/abs/1008.0654), [doi:10.1016/j.nuclphysb.2010.12.017](https://doi.org/10.1016/j.nuclphysb.2010.12.017)&rbrack;

* {#KapustinSaulina} [[Anton Kapustin]], [[Natalia Saulina]],  §3 in: *Surface operators in 3d TFT and 2d Rational CFT*, in: [[Hisham Sati]], [[Urs Schreiber]] (eds.), *[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]*, Proceedings of Symposia in Pure Mathematics **83**, AMS (2011) &lbrack;[arXiv:1012.0911](http://arxiv.org/abs/1012.0911), [ams:pspum-83](https://bookstore.ams.org/pspum-83)&rbrack;

* [Levin 2013](#Levin13)

* [[Anton Kapustin]]: *Ground-state degeneracy for abelian anyons in the presence of gapped boundaries*, Phys. Rev. B **89** (2014) 125307  &lbrack;[arXiv:1306.4254](https://arxiv.org/abs/1306.4254), [doi:10.1103/PhysRevB.89.125307](https://doi.org/10.1103/PhysRevB.89.125307)&rbrack;

* [[Juven C. Wang]], [[Xiao-Gang Wen]]: *Boundary Degeneracy of Topological Order*, Phys. Rev. B **91** (2015) 125124 &lbrack;[doi:10.1103/PhysRevB.91.125124](https://doi.org/10.1103/PhysRevB.91.125124), [arXiv:1212.4863](https://arxiv.org/abs/1212.4863)&rbrack;

* Jackson R. Fliss, Xueda Wen, Onkar Parrikar, Chang-Tse Hsieh, Bo Han, Taylor L. Hughes, Robert G. Leigh: *Interface Contributions to Topological Entanglement in Abelian Chern-Simons Theory*, JHEP 09 (2017) 056 &lbrack;[arXiv:1705.09611](https://arxiv.org/abs/1705.09611), <a href="https://doi.org/10.1007/JHEP09(2017)056">doi:10.1007/JHEP09(2017)056</a>&rbrack;


and with [[fermion|fermionic]] [[boundary field theory|boundary]] [[2d CFT]]:

* Kohki Kawabata, Tatsuma Nishioka, Takuya Okuda, Shinichiro Yahagi: *Fermionic CFTs from topological boundaries in abelian Chern-Simons theories* &lbrack;[arXiv:2502.08084](https://arxiv.org/abs/2502.08084)&rbrack;





Discussion via [[locally covariant AQFT|locally covariant]] [[algebraic quantum field theory]]:

* [[Claudio Dappiaggi]], [[Simone Murro]], [[Alexander Schenkel]]: *Non-existence of natural states for Abelian Chern-Simons theory*, J. Geom. Phys. **116** (2017) 119-123 &lbrack;[arXiv:1612.04080](https://arxiv.org/abs/1612.04080), [arXiv:10.1016/j.geomphys.2017.01.015](https://doi.org/10.1016/j.geomphys.2017.01.015)&rbrack;


On [[lattice gauge theory|lattice formulation]] of abelian Chern-Simons theory:

* Kai Sun, Krishna Kumar, [[Eduardo Fradkin]]: *Discretized Abelian Chern-Simons gauge theory*, Phys. Rev. B **92** (2015) 115148 &lbrack;[doi:10.1103/PhysRevB.92.115148](https://doi.org/10.1103/PhysRevB.92.115148)&rbrack;

* [[Theodore Jacobson]], [[Tin Sulejmanpasic]]: *Modified Villain formulation of abelian Chern-Simons theory*, Phys. Rev. D **107** (2023) 125017 &lbrack;[arXiv:2303.06160](https://arxiv.org/abs/2303.06160), [doi:10.1103/PhysRevD.107.125017](https://doi.org/10.1103/PhysRevD.107.125017)&rbrack;

and its canonical [[quantization of D=3 Chern-Simons theory|quantization]]:

* [[Theodore Jacobson]], [[Tin Sulejmanpasic]]: *Canonical quantization of lattice Chern-Simons theory*, High Energ. Phys. **2024** (2024) 87 &lbrack;[arXiv:2401.09597](https://arxiv.org/abs/2401.09597), <a href="https://doi.org/10.1007/JHEP11(2024)087">doi:10.1007/JHEP11(2024)087</a>&rbrack;




In relation to the [[dilogarithm]]:

* [[Daniel S. Freed]], [[Andrew Neitzke]]: *The dilogarithm and abelian Chern-Simons*, J. Differential Geom. **123**  2  (2023) 241-266 &lbrack;[arXiv:2006.12565](https://arxiv.org/abs/2006.12565), [doi:10.4310/jdg/1680883577](https://projecteuclid.org/journals/journal-of-differential-geometry/volume-123/issue-2/The-dilogarithm-and-abelian-ChernSimons/10.4310/jdg/1680883577.short)&rbrack;

On unoriented manifolds:

* Ippo Orii: *On dimensions of $(2+1)D$ abelian bosonic topological systems on unoriented manifolds* &lbrack;[arXiv:2502.13532](https://arxiv.org/abs/2502.13532)&rbrack;

Coupled to a [[Higgs field]]:

* Yoonbai Kim, O-Kab Kwon, Hanwool Song, Chanju Kim: *Inhomogeneous Abelian Chern-Simons Higgs Model with New Inhomogeneous BPS Vacuum and Solitons* &lbrack;[arXiv:2409.11978](https://arxiv.org/abs/2409.11978)&rbrack;






[[!include abelian Chern-Simons for fractional quantum Hall effect -- references]]


### Abelian Maxwell-Chern-Simons theory for superconductivity

Coupling the Chern-Simons term to 1+2D [[Maxwell theory]] for an effective description of [[superconductivity]]:

* [[M. Cristina Diamantini]], P. Sodano, [[Carlo A. Trugenberger]]: *Gauge Theories of Josephson Junction Arrays*, Nucl. Phys. B **474** (1996) 641-677 \[<a href="https://doi.org/10.1016/0550-3213(96)00309-4">doi:10.1016/0550-3213(96)00309-4</a>, [arXiv:hep-th/9511168](https://arxiv.org/abs/hep-th/9511168)\]

(...)

### For baryons in $N_f=1$ QCD

On [[baryons]] in [[flavor (particle physics)|$N_f = 1$]] [[QCD]] as [[quantum Hall effect|quantum Hall droplets]] [[effective quantum field theory|effectively described]] by abelian Chern-Simons theory:

* [[Zohar Komargodski]]: *Baryons as Quantum Hall Droplets* &lbrack;[arXiv:1812.09253](https://arxiv.org/abs/1812.09253)&rbrack;

* Yong-Liang Ma, [[Maciej A. Nowak]], [[Mannque Rho]], [[Ismail Zahed]], *Baryon as a Quantum Hall Droplet and the Quark-Hadron Duality*, Phys. Rev. Lett. **123** (2019) 172301 &lbrack;[doi:10.1103/PhysRevLett.123.172301](https://doi.org/10.1103/PhysRevLett.123.172301)&rbrack;

* Kentaro Nishimura, Naoki Yamamoto, Ryo Yokokura: *Quantum Hall liquids in high-density QCD* &lbrack;[arXiv:2410.07665](https://arxiv.org/abs/2410.07665)&rbrack;






[[!redirects abelian Chern-Simons theories]]

[[!redirects U(1)-Chern-Simons theory]]
[[!redirects U(1)-Chern-Simons theories]]
