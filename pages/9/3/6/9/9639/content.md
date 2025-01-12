
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
#### Topological physics
+--{: .hide}
[[!include topological physics -- contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Idea
 {#Idea}

At sufficiently low temperature, [[quantum physics|quantum effects]] change the nature of the classical [[Hall effect]], in two ways:

1. in the *integral* quantum Hall effect, quantization of the [[energy]] into *Landau levels* of electrons that are circulating in a transverse [[magnetic field]] while confined to a plane, causes the [[Hall effect|Hall resistance]], which classically increases linearly with increasing external [[magnetic field]], to instead intermittently form constant "plateaus" as these get "filled" by electron states,

1. in the *fractional quantum Hall effect*, strong external magnetic field causes these Landau levels to be filled only partially and the strongly Coulomb-coupled electrons to form [[bound states]] "with" magnetic [[flux quantization|flux quanta]] that may exhibit effective *fractional* charge and, apparently, "fractional statistics" ([[anyon|anyonic]] [[braiding]] behaviour).


### Hall effect and Hall resistivity
 {#IdeaHallResistivity}

The setup of any *Hall effect* is a plane sheet of [[conductor|conducting]]  material placed in a transverse [[magnetic field]] (constant across the plane, directed perpendicular to it).

The *[[classical Hall effect]]* is the phenomenon that a [[voltage]] $V_x$ applied along the conducting sheet in some direction -- to be called the $x$-direction -- induces a *Hall voltage* $V_y$ in the *perpendicular* direction -- to be called the $y$-direction -- across the conducting sheet.

The cause of this effect is the [[Lorentz force]], exerted on the [[electrons]] by the [[magnetic field]], which is proportional in magnitude to the magnetic field and to the electron [[velocity]] but perpendicular in [[direction vector|direction]] to both the magnetic field and to their direction of motion.

Due to this force, the electrons which start to follow the applied voltage gradient quickly drift to one side of the conducting sheet until their mutual electrostatic repulsion there counterbalances the Lorentz force. At this point the electrons move straight along the applied voltage gradient, with the Lorentz force now exactly compensated by the Hall voltage due to the gradient in electron concentration.

For more details on the [[classical Hall effect]] see there; here we further just need the formulas for conductivity and resistivity:

Consider in the [[plane]] $\mathbb{R}^2$, with canonical [[coordinates]] $x$ and $y$, the

* [[electric field]]$\;$[[vector]] $\vec E$,

* [[electric current]]$\;$[[vector]] $\vec J$.

With the current running in the $x$-direction

$$
  \vec J 
  \;\coloneqq\;
  \left[
  \begin{array}{c}
    J_{x}
    \\
    0
  \end{array}
  \right]
$$

the statement of the classical Hall effect is that 

* not just the *longitudinal field* $E_x \neq 0$ 

but also 

* the *Hall field* $E_y \neq 0$. 

To say this more formally, recall that in a [[conductor]] the current $\vec J$ is a [[linear function]] of the field $\vec E$ with proportionality being the *[[conductivity]] [[tensor]]* $\sigma$, here a $2 \times 2$ [[matrix]], such that [[Ohm's law]] holds:

$$
  \vec J \,=\, \sigma \cdot \vec E
  \,.
$$

Assuming that the conducting sheet has no preferred direction, the conductivity tensor is of the form

$$
  \sigma
  \;=\;
  \left[
  \begin{array}{cc}
    \sigma_{x x} & \sigma_{x y}
    \\
    - \sigma_{x y} & \sigma_{xx}
  \end{array}
  \right]
$$

for $\sigma_{x x}, \sigma_{x y} \,\in\, \mathbb{R}$.

The corresponding *[[resistivity]] [[tensor]]* is  the [[inverse matrix]]  $rho = \sigma^{-1}$

\[
  \label{GenericResistivityTensor}
  \rho
  \;=\;
  \left[
  \begin{array}{cc}
    \rho_{x x} & \rho_{x y}
    \\
    - \rho_{x y} & \rho_{y y}
  \end{array}
  \right]
  \;=\;
  \tfrac{1}{
    \sigma_{x x}^2 + \sigma_{x y}^2
  }
  \left[
  \begin{array}{cc}
    \sigma_{x x} & -\sigma_{x y}
    \\
    \sigma_{x y} & \sigma_{x x}
  \end{array}
  \right]
  \,.
\]

in terms of which [[Ohm's law]] reads

$$
  \vec E \,=\, \rho \cdot \vec J
  \,.
$$


In this tensorial language, the classical Hall effect is the statement that for transverse magnetic field $B \gt 0$ the non-diagonal elements of the conductivity/resistivity tensors are non-vanishing, in that we have
\[
  \label{NonVanishingHallConductivity}
  \text{Hall conductivity}
  \;\;
  \sigma_{x y} \neq 0
  \;\;\;\;\;\;
  \text{and}
  \;\;\;\;\;\;
  \text{Hall resistance}
  \;\;
  \rho_{x y} \neq 0
  \,.
\]

In this case the basic matrix relation (eq:GenericResistivityTensor) is of some importance for understanding the measurement results in the integer quantum Hall effect [below](#IdeaIntegerQuantumHallEffect), since it implies the (maybe surprising-sounding) phenomenon that for non-vanishing Hall effect the *longitudinal conductivity and resistivity may jointly vanish*, see (eq:LongitudinalResistivityVanishesWithLongConductivity) below.



### Integer quantum Hall effect
  {#IdeaIntegerQuantumHallEffect}

At extremely low [[temperature]], low charge carrier density, 
and extreme thin-ness of the conducting sheet,
the above [[classical Hall effect]] exhibits modifications by [[quantum mechanics|quantum mechanical]] effects, due to the  fact that the [[energy]] of [[electrons]] in a transverse magnetic field is *quantized* into discrete units known as *Landau levels*. 

Since electrons are [[fermions]], the [[Pauli exclusion principle]] demands that in their [[ground state]] the electrons fill the available [[Fermi sea]] with one electron per available state, below a given energy, the "chemical potential". (Here, due to the strong external [[magnetic field]], all electrons may be assumed to have their [[spin]] aligned along this field, so that the states in question concern just the remaining electron [[momenta]].)
The larger the magnetic field, the more [[quantum states]] are comprised by one Landau level.

In the case that the electrons fill *exactly* $i \in \mathbb{N}$ Landau levels -- one speaks of *filling fraction $\nu = i$* --, the next excited state, needed for the transport of charge, is separated by the [[energy gap]] to the next Landau level, and hence at an integer number of exactly filled Landau levels the Hall system behaves like an [[insulator]] with vanishing longitudinal conductivity $\sigma_{x x} \sim 0$.

What is measured in experiments is the *longitudinal resistivity*, which --- by (eq:GenericResistivityTensor) with (eq:NonVanishingHallConductivity) --- also goes to zero at these points of exactly filled Landau levels:

\[
  \label{LongitudinalResistivityVanishesWithLongConductivity}
  R_x
  \coloneqq
  \rho_{x x}
  \;=\;
  \frac{
    \sigma_{x x}
  }{
    \sigma^2_{x x} + \sigma^2_{x y}
  }
  \;\;
  \underset{\sigma_{x x} \to 0}{\longrightarrow}
  \;\;
  0
  \,.
\]

But the hallmark of the integer quantum Hall effect is that this vanishing of the longitudinal (conductivity and hence) resistivity is observed *not just* right when the magnetic field strength is at the critical value $B = B_i$, but in a whole neighbourhood of these values, where at the same time the Hall resistivity $R_H \coloneqq \rho_{x y}$ is approximately constant and hence forms a "*Hall plateau*":

<center>
<img src="https://ncatlab.org/nlab/files/IntegerQuantumHallEffect.jpg" width="500">
</center>

Remarkably, the height of these Hall plateaus is an experimental constant to high precision, and is independent of the detailed nature of the underlying material, unaffected even by punching holes into the conducting sheet.

Yet more remarkably, the explanation for the horizontal extension of these plateaux is thought to be related to *impurities* in the material --- in an ideally pure conductor the quantum Hall effect is expected to be invisible! The idea is that, due to the impurities, the idealized picture of Landau levels applies only to some of the electrons in the sample, while others are "localized" at/by the imporitites; and as the magnetic field is varied it is only after the reservoir of localized electrons has changed energy levels that it becomes the turn of the "quantum Hall electrons".



### Fractional quantum Hall effect
 {#IdeaFQHE}

Even though the integer quantum Hall effect ([above](#IdeaIntegerQuantumHallEffect)) involves many electrons (a macroscopic number on the scale of the [[Avogadro constant]]),
which necessarily interact strongly via their mutual Coulomb force, for understanding the effect it turns out (as indicated above) to be sufficient to consider the energy of single electrons right at the [[Fermi sea]] surface of a filled Landau level as if they were "free" (non-interacting). That such a radical (and conceptually unjustified!) approximation works so well is surprising on a fundamental level, but is entirely common in traditional [[solid state physics]], notably in [[Landau's Fermi liquid theory]].

However, yet closer experimental analysis at yet smaller [[temperatures]] and electron densities shows that this approximation breaks down at some point, and that the strong interaction between the electrons makes them collectively behave in exotic ways.

Concretely, experiments show that Hall plateaus appear not just at integer filling levels, but (smaller) Hall plateaus appear also at certain [[rational number|rational]] filling fractions $\nu \in \mathbb{Q}$, notably at $\nu = 1/q$ for $q \in \mathbb{N}$, hence whenever the first Landau level is filled only *half* or *one-third*, etc.

This experimentally pbserved phenomenon is thus called the *fractional quantum Hall effect*.

Unfortunately, due to the general open problem of formulating and analyzing [[non-perturbative quantum field theory]], there is essentially no first-principles understanding of what causes the fractional quantum Hall effect! 

What people have come up with, instead, are:

1. *ad hoc* (mental) models of how the electrons form supposedly "[[bound states]]" with magnetic flux quanta: "**composite fermions**", 

   suggesting that the fractional quantum Hall effect is just the integer quantum Hall effect again, now not for plain electrons but for their exotic "fractional" [[quasi-particle]]/quasi-hole [[bound states]],

1. some educated guesses as to the [[quantum many-body physics|many-electron]] [[wavefunction]] describing the fractional Hall [[quantum state]] -- **[[Laughlin wavefunctions]]**,

   which, while just guessed, are confirmed well by experiment and have in practice become the effective theory for FQH systems,

1. some actual [[effective field theory|effectice]] [[quantum field theory]] description by variants of **[[abelian Chern-Simons theory]]**.

A neat account of the commonly accepted composite fermion picture is given by [Störmer 1999](#Störmer99):

> "In the [[fractional quantum Hall effect|FQHE]], the electrons assume an even more favorable state \[than in the IQHE\], unforeseen by theory, by conducting an elaborate, mutual, quantum-mechanical dance. Many-particle effects are extraordinarily challenging to address theoretically. \[...\] on occasion many-particle interactions become the essence of a physical effect. [[superconductivity|Superconductivity]] and [[superfluidity]] are of such intricate origin. To account for their occurrence one had to devise novel, sophisticated theoretical means. The emergence of the FQHE requires such a new kind of thinking. \[...\] 

> It was an important conceptual step to realize that an
impinging [[magnetic field]] $B$ could be viewed as creating
tiny whirlpools, so-called [[vortices]], in this lake of
charge—one for each [[flux quantization|flux quantum]] $\phi_0 = h/e$ of the magnetic field. \[...\] Casting electron-electron correlation in terms of vortex attachment facilitates the comprehension of this intricate many-particle behavior. Regarding the vortices as little whirlpools ultimately remains a crutch for visualizing something that has no classical analog. \[...\] 

\begin{imagefromfile}
    "file_name": "Stormer99-Fig14.jpg",
    "float": "right",
    "width": 360,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

> At magnetic fields higher than the $i = 1$ IQHE, the stronger magnetic field provides more flux quanta and hence there are more vortices than there are electrons. The Pauli principle is readily satisfied by placing one vortex onto each electron \[Fig. 14(a)\]—but there are more vortices available. The electron system can considerably reduce its electrostatic Coulomb energy by placing more vortices onto each electron \[Fig. 14(b)\]. More vortices on an electron generate a bigger surrounding whirlpool, pushing further away all fellow electrons, thereby reducing the repulsive energy. \[...\]

> Vortices are the expression of flux quanta in the 2D electron system, and each vortex can be thought of as
having been created by a flux quantum. Conceptually, it
is advantageous to represent the vortices simply by their
"generators", the flux quanta themselves. Then the placement of vortices onto electrons becomes equivalent to the attachment of magnetic flux quanta to the carriers. Electrons plus flux quanta can be viewed as new entities, which have come to be called composite particles, CPs. 

> As these objects move through the liquid, the flux quanta act as an invisible shield against other electrons. Replacing the system of highly interacting electrons by a system of electrons with such a "guard ring" -- compliments of the magnetic field -- removes most of the electron-electron interaction from the problem and leads to composite particles which are almost void of mutual interactions. It is a minor miracle that such a transformation from a very complex many-particle problem of well-known objects (electrons in a magnetic field) to a much simpler single-particle problem of rather complex objects (electrons plus flux quanta) exists and that it was discovered.

> CPs act differently from bare electrons. All of the external magnetic field has been incorporated into the particles via flux quantum attachment to the electrons. Therefore, from the perspective of CPs, the magnetic field has disappeared and they no longer are subject to it. They inhabit an apparently field-free 2D plane. Yet more importantly, the attached flux quanta change the character of the particles from fermions to bosons and back to fermions. \[...\]

\begin{imagefromfile}
    "file_name": "Stormer99-Fig16.jpg",
    "float": "right",
    "width": 360,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


> {#StormerOnThirdFractionModel} As the magnetic field deviates from exactly $\nu = 1/3$ filling to higher fields, more vortices are being created (Fig. 16). They are not attached to any electrons, since this would disturb the symmetry of the condensed state. The amount of charge deficit in any of these vortices amounts to exactly 1/3 of an electronic charge. These quasiholes (whirlpool in the electron lake) are effectively positive charges as compared to the negatively charged electrons. An analogous argument can be made for magnetic fields slightly below $\nu = 1/3$ and the creation of quasielectrons of negative charge $e/3$. Quasiparticles can move freely through the 2D plane and transport electrical current. They are the famous 1/3 charged particles of the FQHE that have been observed by various experimental means \[...\]. 

> Plateau formation in the FQHE arises, in analogy to plateau formation in the IQHE from potential fluctuations and the resulting localization of carriers. In the case of the FQHE the carriers are not electrons, but, instead, the bizarre fractionally charged quasiparticles.

> &lbrack;end of excerpt from [Störmer 1999](#Störmer99)&rbrack;


\linebreak

## Properties

### As a topological insulator

The bulk/edge behaviour in a quantum Hall effect is is that of a [[topological insulator]]. (While topological insulator materials typically show this behaviour without the need of a strong magnetic field.)

(...)

## Related concepts

* [[Hall effect]]

* [[Laughlin wavefunction]]

* [[spin Hall effect]], [[quantum spin Hall effect]]

* [[braid group statistics]], [[anyon]]

* [[topological insulator]]

* [[topological quantum computation]]


## References

### General

Review:

* {#vonKlitzing86} [[Klaus von Klitzing]], _The quantized Hall effect_, Rev. Mod. Phys. **58** 519 (1986) &lbrack;[doi:10.1103/RevModPhys.58.519](https://doi.org/10.1103/RevModPhys.58.519)&rbrack;

* Richard E. Prange, [[Steven M. Girvin]] (eds.): *The Quantum Hall Effect*, Graduate Texts in Contemporary Physics, Springer (1986, 1990) &lbrack;[doi:10.1007/978-1-4612-3350-3](https://doi.org/10.1007/978-1-4612-3350-3)&rbrack;



* Tapash Chakraborty, Pekka Pietiläinen: *The Quantum Hall Effects -- Integral and Fractional*, Springer Series in Solid State Sciences (1995) \[<a href="https://doi.org/10.1007/978-3-642-79319-6">doi:10.1007/978-3-642-79319-6</a>\]

* Daijiro Yoshioka: *The Quantum Hall Effect*, Springer (2002) \[<a href="https://doi.org/10.1007/978-3-662-05016-3">doi:10.1007/978-3-662-05016-3</a>\]

* Benoît Douçot, [[Vincent Pasquier]], Bertrand Duplantier, Vincent Rivasseau (eds.): *The Quantum Hall Effect -- Poincaré Seminar 2004*, Progress in Mathematical Physics, Springer (2005) \[<a href="https://doi.org/10.1007/3-7643-7393-8">doi:10.1007/3-7643-7393-8</a>\]

* {#Tong16} [[David Tong]]: *The Quantum Hall Effect*, lecture notes (2016) &lbrack;[arXiv:1606.06687](https://arxiv.org/abs/1606.06687), [course webpage](https://www.damtp.cam.ac.uk/user/tong/qhe.html), [pdf](http://www.damtp.cam.ac.uk/user/tong/qhe/qhe.pdf), [[Tong-QuantumHallEffect.pdf:file]]&rbrack;

* _The quantum Hall effect_ &lbrack;[pdf](http://www.tezu.ernet.in/rctp2015/SR%20On%20quantum%20Hall%20effect.pdf)&rbrack;

Discussion via Newton-Cartan theory:

* William Wolf, James Read, Nicholas Teh, *Edge modes and dressing fields for the Newton-Cartan quantum Hall effect* &lbrack;[arXiv:2111.08052](https://arxiv.org/abs/2111.08052)&rbrack;


See also:

* Wikipedia, _[Quantum Hall effect](https://en.wikipedia.org/wiki/Quantum_Hall_effect)_, 

* Wikipedia _[Fractional quantum Hall effect](http://en.wikipedia.org/wiki/Fractional_quantum_Hall_effect)_


### Integral quantum Hall effect

#### Experiment

Original experimental detection:

* [[Klaus von Klitzing]], G. Dorda, M. Pepper: _New Method for High-Accuracy Determination of the Fine-Structure Constant Based on Quantized Hall Resistance_, Phys. Rev. Lett. **45**  (1980) 494 &lbrack;[doi:10.1103/PhysRevLett.45.494](https://doi.org/10.1103/PhysRevLett.45.494)&rbrack;

* M. A. Paalanen, D. C. Tsui, A. C. Gossard: _Quantized Hall effect at low temperatures_, Phys. Rev. B **25** 5566(R) (1982) &lbrack;[doi:10.1103/PhysRevB.25.5566](https://doi.org/10.1103/PhysRevB.25.5566)&rbrack;


#### Theory

While an intuitive understanding for the quantization of the Hall conductance has been given in

* [[Robert B. Laughlin]], *Quantized Hall conductivity in two dimensions*, Phys. Rev. B **23** 5632(R) (1981) &lbrack;[doi:10.1103/PhysRevB.23.5632](https://journals.aps.org/prb/abstract/10.1103/PhysRevB.23.5632)&rbrack;

a theoretical derivation of the effect was obtained only much later in

* [[Matthew Hastings]], [[Spyridon Michalakis]], _Quantization of Hall conductance for interacting electrons without averaging assumptions_, Commun. Math. Phys., 334:433–471, (2015) &lbrack;[arXiv:0911.4706](https://arxiv.org/abs/0911.4706), [doi:10.1007/s00220-014-2167-x](https://doi.org/10.1007/s00220-014-2167-x)&rbrack;

with closely related results in

* Alessandro Giuliani, Vieri Mastropietro, Marcello Porta, _Universality of the Hall conductivity in interacting electron systems_, Commun. Math. Phys. **349** (2017) 1107–1161 &lbrack;[arXiv:1511.04047](https://arxiv.org/abs/1511.04047), [doi:10.1007/s00220-016-2714-8](https://doi.org/10.1007/s00220-016-2714-8)&rbrack;

Review of this theory behind the quantum Hall effect:

* [[Joseph E. Avron]], Daniel Osadchy, Ruedi Seiler: _A topological look at the quantum Hall effect_, Physics Today __56__ 8 (2003) 38–42 &lbrack;[doi:10.1063/1.1611351](http://dx.doi.org/10.1063/1.1611351)&rbrack;

* [[Joseph E. Avron]], _Why is the Hall conductance quantized?_ (2017) &lbrack;[pdf](http://web.math.princeton.edu/~aizenman/OpenProblems_MathPhys/17_Avron.pdf), [[AfronQuantumHallEffect.pdf:file]]&rbrack;

* [[Spyridon Michalakis]], _Why is the Hall conductance quantized?_, Nature Reviews Physics **2** (2020) 392–393 &lbrack;[doi:10.1038/s42254-020-0212-6](https://doi.org/10.1038/s42254-020-0212-6)&rbrack;

* S. Klevtsov, X. Ma, G. Marinescu, P. Wiegmann, _Quantum Hall effect and Quillen metric_ Commun. Math. Phys. **349** (2017) 819–855 &lbrack;[doi:10.1007/s00220-016-2789-2](https://doi.org/10.1007/s00220-016-2789-2)&rbrack;



### Fractional quantum Hall effect


#### General


Review and survey of the FQHE:

* {#Störmer99} [[Horst L. Störmer]]: *Nobel Lecture: The fractional quantum Hall effect*, Rev. Mod. Phys. **71** (1999) 875 \[<a href="https://doi.org/10.1103/RevModPhys.71.875">doi:10.1103/RevModPhys.71.875</a>\]

* {#Laughlin99} [[Robert B. Laughlin]]: *Nobel Lecture: Fractional quantization*, Rev. Mod. Phys. **71** 4 (1999) 863 &lbrack;[doi:10.1103/RevModPhys.71.863](https://doi.org/10.1103/RevModPhys.71.863), [pdf](https://www.nobelprize.org/uploads/2018/06/laughlin-lecture.pdf)&rbrack;


* [[Steven M. Girvin]]: *Introduction to the Fractional Quantum Hall Effect*, S&eacute;minaire Poincar&eacute; **2** (2004) 53–74, reprinted in *The Quantum Hall Effect*, Progress in Mathematical Physics **45**, Birkhäuser (2005)  &lbrack;[pdf](http://www.bourbaphy.fr/girvin.pdf), [doi:10.1007/3-7643-7393-8_4](https://doi.org/10.1007/3-7643-7393-8_4)&rbrack;

* [[Peter Fulde]], §14.2 in: *Correlated Electrons in Quantum Matter*, World Scientific (2012) &lbrack;[doi:10.1142/8419](https://doi.org/10.1142/8419), [pdf](https://www.pks.mpg.de/fileadmin/user_upload/MPIPKS/group_pages/Electronic_Correlations/BOOK_Aktualisierung_Oct19.pdf)&rbrack;


* [[Bertrand I. Halperin]], [[Jainendra K. Jain]] (eds.): *Fractional Quantum Hall Effects -- New Developments*, World Scientific (2020) \[<a href="https://doi.org/10.1142/11751">doi:10.1142/11751</a>\]

* D. E. Feldman, [[Bertrand I. Halperin]]: *Fractional charge and fractional statistics in the quantum Hall effects*, Rep. Prog. Phys. **84** (2021) 076501 \[<a href="https://doi.org/10.1088/1361-6633/ac03aa">doi:10.1088/1361-6633/ac03aa</a>, [arXiv:2102.08998](https://arxiv.org/abs/2102.08998)\]

* [[Tudor D. Stanescu]], *Effective theory of Abelian fractional quantum Hall liquids*, Section 6.2.1 of: *Introduction to Topological Quantum Matter & Quantum Computation*, CRC Press (2020) &lbrack;[ISBN:9780367574116](https://www.routledge.com/Introduction-to-Topological-Quantum-Matter--Quantum-Computation/Stanescu/p/book/9781032126524)&rbrack;


See also:

* Wikipedia, *[Fractional Quantum Hall Effect](https://en.wikipedia.org/wiki/Fractional_quantum_Hall_effect)*


A quick review of the description via [[abelian Chern-Simons theory]] with further pointers is in the introduction of:

* Spencer D. Stirling, _Abelian Chern-Simons theory with toral gauge group, modular tensor categories, and group categories_, &lbrack;[arXiv:0807.2857](http://arxiv.org/abs/0807.2857)&rbrack;


Realization via [[AdS/CFT in condensed matter physics]]:

* Mitsutoshi Fujita, Wei Li, [[Shinsei Ryu]], [[Tadashi Takayanagi]], *Fractional Quantum Hall Effect via Holography: Chern-Simons, Edge States, and Hierarchy*, JHEP 0906:066 (2009) &lbrack;[arXiv:0901.0924](https://arxiv.org/abs/0901.0924)&rbrack;

#### Experiment

Observation of the FQHE in $GaAS$:

* D. C. Tsui, [[Horst L. Stormer]], A. C. Gossard: *Two-Dimensional Magnetotransport in the Extreme Quantum Limit*, Phys. Rev. Lett. **48** (1982) 1559 \[<a href="https://doi.org/10.1103/PhysRevLett.48.1559">doi:10.1103/PhysRevLett.48.1559</a>\]

in [[graphene]]:

* Xu Du, Ivan Skachko, Fabian Duerr, Adina Luican, Eva Y. Andrei: *Fractional quantum Hall effect and insulating phase of Dirac electrons in graphene*, Nature **462** 192 (2009) \[<a href="https://doi.org/10.1038/nature08522">doi:10.1038/nature08522</a>, [arXiv:0910.2532](https://arxiv.org/abs/0910.2532)\]

* Kirill I. Bolotin, Fereshte Ghahari, Michael D. Shulman, [[Horst L. Stormer]], Philip Kim: *Observation of the Fractional Quantum Hall Effect in Graphene*, Nature **462** (2009) 196–199 \[<a href="https://doi.org/10.1038/nature08582">doi:10.1038/nature08582</a>, [arXiv:0910.2763](https://arxiv.org/abs/0910.2763)\]

in oxide interfaces:

* A. Tsukazaki et al.: *Observation of the fractional quantum Hall effect in an oxide*, Nature Materials **9** (2010) 889–893 \[<a href="https://doi.org/10.1038/nmat2874">doi:10.1038/nmat2874</a>\]

in $CdTe$:

* B. A. Piot, J. Kunc, M. Potemski, D. K. Maude, C. Betthausen, A. Vogl, D. Weiss, G. Karczewski, T. Wojtowicz: *Fractional quantum Hall effect in $CdTe$*, PhysRev B. **82** (2010) 081307 (R) \[<a href="https://doi.org/10.1103/PhysRevB.82.081307">doi:10.1103/PhysRevB.82.081307</a>, [arXiv:1006.0908](https://arxiv.org/abs/1006.0908)\]




#### Phenomenological models
  {#ReferencesMicroscopicModelsForFQHE}

Phenomenological models for the fractional quantum Hall effect:

The original [[Laughlin wavefunction]]:

* [[Robert B. Laughlin]], *Anomalous Quantum Hall Effect: An Incompressible Quantum Fluid with Fractionally Charged Excitations*, Phys. Rev. Lett. **50** (1983) 1395 &lbrack;[doi:10.1103/PhysRevLett.50.1395](https://doi.org/10.1103/PhysRevLett.50.1395)&rbrack;

The Halperin multi-component model:

* [[Bertrand I. Halperin]]: *Theory of the Quantized Hall Conductance*, Helvetica Physica Acta **56** (1983) 75-102 \[<a href="https://doi.org/10.5169/seals-115362">doi:10.5169/seals-115362</a>, [[Halperin-TheoryOfQHE.pdf:file]]\]


The Haldane-Halperin model:

* [[F. Duncan M. Haldane]]: *Fractional Quantization of the Hall Effect: A Hierarchy of Incompressible Quantum Fluid States*, Phys. Rev. Lett. **51** (1983) 605 \[<a href="https://doi.org/10.1103/PhysRevLett.51.605">doi:10.1103/PhysRevLett.51.605</a>\]

* [[Bertrand Halperin]]: *Statistics of Quasiparticles and the Hierarchy of Fractional Quantized Hall States*, Phys. Rev. Lett. **52** (1984) 1583 \[<a href="https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.52.1583">doi:10.1103/PhysRevLett.52.1583</a>\]

The composite-fermion model (CF) which explains the FQHE as the [[integer quantum Hall effect]] not of the bare electrons but of [[quasi-particles]] which they form (for reasons not explained by the model):

* [[Jainendra K. Jain]]: *Composite-fermion approach for the fractional quantum Hall effect*, Phys. Rev. Lett. **63** (1989) 199 \[<a href="https://doi.org/10.1103/PhysRevLett.63.199">doi:10.1103/PhysRevLett.63.199</a>\]

* [[Jainendra K. Jain]]: *Microscopic theory of the fractional quantum Hall effect*, Adv. Phys. **41** (1992) 105-146 \[<a href="https://doi.org/10.1080/00018739200101483">doi:10.1080/00018739200101483</a>\]

* [[Jainendra K. Jain]]: *Composite Fermions*, Cambridge University Press (2007) \[<a href="https://doi.org/10.1017/CBO9780511607561">doi:10.1017/CBO9780511607561</a>\]

Introducing **[[abelian Chern-Simons theory]]** to the picture:

* Ana Lopez, [[Eduardo Fradkin]]: *Fractional quantum Hall effect and Chern-Simons gauge theories*, Phys. Rev. B **44** (1991) 5246 \[<a href="https://doi.org/10.1103/PhysRevB.44.5246">doi:10.1103/PhysRevB.44.5246</a>\]

* [[Xiao-Gang Wen]], [[Anthony Zee]]: *Classification of Abelian quantum Hall states and matrix formulation of topological fluids*, Phys. Rev. B **46** (1992) 2290 &lbrack;[doi:10.1103/PhysRevB.46.2290](https://doi.org/10.1103/PhysRevB.46.2290)&rbrack;


Further discussion:

* [[Jainendra K. Jain]]: *A note contrasting two microscopic theories of the fractional quantum Hall effect*, Indian J of Phys **88** (2014) 915-929 \[<a href="https://doi.org/10.1007/s12648-014-0491-9">doi:10.1007/s12648-014-0491-9</a>, [arXiv:1403.5415](https://arxiv.org/abs/1403.5415)\]

* C.-C Chang, [[Jainendra K. Jain]]: *Microscopic origin of the next generation fractional quantum Hall effect*, Phys. Rev. Lett. **92** (2004) 196806 \[<a href="https://doi.org/10.1103/PhysRevLett.92.196806">doi:10.1103/PhysRevLett.92.196806</a>, [arXiv:cond-mat/0404079](https://arxiv.org/abs/cond-mat/0404079)\]

Discussion highlighting the lack of microscopic explanation of these phenomenological models:

* [[Janusz E. Jacak]]: *Topological approach to electron correlations at fractional quantum Hall effect*, Annals of Physics **430** (2021) 168493 \[<a href="https://doi.org/10.1016/j.aop.2021.168493">doi:10.1016/j.aop.2021.168493</a>\]
> &lbrack;p 3:&rbrack; "Though the Laughlin function very well approximates the true ground state at $\nu = \tfrac{1}{q}$, the physical mechanism of related correlations and of the whole hierarchy of the FQHE remained, however, still obscure."

> "The so-called HH (Halperin–Haldane) model of consecutive generations of Laughlin states of anyonic quasiparticle excitations from the preceding Laughlin state has been abandoned early because of the rapid growth of the daughter quasiparticle size, which quickly exceeded the sample size."

>  "the Halperin multicomponent theory and of the CF model advanced the understanding of correlations in FQHE, however, on a phenomenological level only. CFs were assumed to be hypothetical quasi-particles consisting of electrons and flux quanta of an auxiliary fictitious magnetic field pinned to
them. The origin of this field and the manner of attachment of its flux quanta to electrons have been neither explained nor discussed."



[[!include abelian Chern-Simons for fractional quantum Hall effect -- references ]]



[[!include quantum Hall effect via noncommutative geometry -- references]]



[[!include anyons in the quantum Hall effect -- references]]



[[!include supersymmetry in fractional quantum Hall systems -- references]]





### In string/M-theory

On [[geometric engineering]] of aspects of the quantum Hall effect on [[M5-brane]] [[worldvolumes]] via an effective [[noncommutative geometry]] induced by a constant [[B-field]] [[flux density]]:

* [[Simeon Hellerman]], [[Leonard Susskind]]: *Realizing the Quantum Hall System in String Theory* \[<a href="https://arxiv.org/abs/hep-th/0107200">arXiv:hep-th/0107200</a>\]









category: physics

[[!redirects quantum Hall effects]]

[[!redirects fractional quantum Hall effect]]
[[!redirects fractional quantum Hall effects]]

[[!redirects integer quantum Hall effect]]
[[!redirects integer quantum Hall effect]]

[[!redirects quantum Hall material]]
[[!redirects quantum Hall materials]]

[[!redirects fractional quantum Hall system]]
[[!redirects fractional quantum Hall systems]]

