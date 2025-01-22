
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

In [[solid state physics|solid state]] [[quantum physics]], a  *Laughlin wavefunction* is a certain Ansatz for an [[quantum many-body physics|n-particle]] [[wavefunction]] which is meant to capture at least aspects of [[ground states]] with [[anyon|anyonic]] properties, such as of [[fractional quantum Hall systems]].

The issue is that the strongly-coupled electron dynamics, that is thought to be responsible for the [[fractional quantum Hall effect]], cannot be solved -- not even approximately --- by existing theory (cf. the problem of [[non-perturbative quantum field theory]]). To make up for this, the Laughlin wavefunction is an *educated guess* -- jargon: *trial wavefunction* -- as to what the [[ground states]] of these systems should approximately look like to some approximation --- a guess that turns out to agree accurately with [[experiment]]. As such, the Laughlin wavefunction has come to be regarded as the standard effective theory of fractional quantum Hall systems (but there is criticism of this consensus, cf. [Mikhailov 2024](#Mikhailov24)).


### Basic Laughlin wavefunction on the plane
 {#BasicLaughlinWavefunctionOnThePlane}

The basic Laughlin wavefunction &lbrack;[Laughlin 1983 (6-7)](#Laughlin83), cf. [Laughlin 1999 (21)](#Laughlin99)&rbrack;, for $N$ spin-less (in practice really: *spin-polarized* by a strong transversal [[magnetic field]]) [[fermions]] ([[electrons]], constrained to move) in a [[plane]], at [[odd number|odd]] "*Landau level filling fraction*" 

$$
  q  \,\in\, 2\mathbb{N} + 1
  \,,
$$

is the [[complex numbers|complex]]-valued [[function]] on the [[configuration space of points|configuration space of $N$ ordered points]] in the [[plane]] --- to be thought of as the [[complex plane]] with canonical [[holomorphic function|holomorphic]] [[coordinate function]] $z$ ---, given (up to [[normalization]], which we may and do disregard throughout) by

\[
  \label{BasicLaughlinState}
  \Psi_{La}\big(
    z_1, \cdots, z_N
  \big)
  \;\coloneqq\;
  \textstyle{\prod_{i \lt j}}
  (z_i - z_j)^q
  \;
  \exp\big(
    -
    \tfrac{1}{4 \ell_B^2} 
    \textstyle{\sum_i} {\vert z_i\vert}^2
  \big)
  \,.
\]

Here the [[absolute value]] of and hence the [[probability density]] encoded by

* the **second factor** drops quickly where the particles are farther away from their center of mass (here: the origin in the complex plane) than the *magnetic length*

  $$
    \ell_B \,\coloneqq\,
    \sqrt{
      \frac
        { \hbar c }
        { {\vert e \vert} B }
    }
  $$

  (where $B$ denotes the given external [[magnetic field|magnetic]] [[field strength]] while the other constants are [[physical units]]: $\hbar$ is [[Planck's constant]], $c$ is the [[speed of light]], and $e$ is the [[electric charge]] of an [[electron]]),

* while that of the **first factor** tends to zero wherever any pair of particles approaches each other. 

Hence the particles in this [[quantum state]] are most likely to be found all close to the origin but still spread out not to be too close to each other: The image is that of a little *droplet*, and one speaks also of *quantum fluid droplets* in this context.

Moreover, if or since the first factor (the *Jastrow polynomial*) is actually an odd power (the $q$th power) of the [[Vandermonde determinant]]

$$
  vd(z_\bullet) 
  \;\coloneqq\; 
  \textstyle{\underset{i \lt j}{\prod}} 
  (z_i - z_j)
  \,,
$$

which itself is skew-symmetric under [[permutation]] of the particle positions (see [there](Vandermonde+determinant#SkewSymemtryUnderSwappingVariables)), so is the Laughlin state, as it must be for a [[quantum many body physics|many-]][[fermion]] [[wavefunction]], by the [[Pauli exclusion principle]].

Due to these basic properties, the Laughlin wavefunction is a plausible Ansatz for any localized [[bound state]] of [[fermions]]. But on top of this, the power of $q$ to which the [[Vandermonde determinant]] is taken makes these particles support "$q$-fractional" quasi-particle/hole excitations, see [below](#BasicLaughlinStateWithQuasiHoles).

 
### Basic Moore-Read wavefunction on the plane

At [[even number|even]] filling fraction 

$$
  q  \,\in\, 2 \mathbb{N}
  \,,
$$ 

the Laughlin Ansatz needs modification, since here the even power of the [[Vandermonde determinant]] would be symmetric under particle exchange and hence not describe the intended [[Fermions]].

A further educated guess suggests to multiply, at even filling fraction, the Laughlin wavefunction by some other factor which *is* skew-symmetric in the particule positions. The *Moore-Read wavefunction* &lbrack;[Moore & Read 1991 (5.1)](#MooreRead91)&rbrack; is the result of choosing this factor to be the *[[Pfaffian]]* $pf(-)$ of the [[matrix]] of inverse [[distances]] between pairs of particles 

> (For the [[Pfaffian]] to be defined in this situation, we must consider an [[even number]] $N$ of electrons. But in the practice of the [[fractional quantum Hall effect]], $N$ is a humongous "macroscopic" number on the scale of the [[Avogadro constant]], and hence may be assumed to be [[even number|even]] without any conceivable restriction of practical generality.)

-- whence often known as *the Pfaffian state*:


\[
  \label{BasicMooreReadState}
  \Psi_{MR}\big(
    z_1, \cdots, z_N
  \big)
  \;\coloneqq\;
  pf
  \left(
    \tfrac
      { 1 }
      { z_{\bullet_1} - z_{\bullet_2} }
  \right)
  \textstyle{\prod_{i \lt j}}
  (z_i - z_j)^q
  \,
  \exp\big(
    - 
    \tfrac{1}{4 \ell_B^2} 
    \textstyle{\sum_i} {\vert z_i\vert}^2
  \big)
  \,.
\]

That the [[Pfaffian]] of the (inverse) distance matrix is indeed skew-symmetric is readily seen in its [[Berezinian integral]]-formulation (see [there](Pfaffian#InTermOfBerezinianIntegrals)). That formulation also reveals a kind of [[supersymmetry]] between the Laughlin and the Moore-Read wavefunctions:


### Supersymmetry between Laughlin- and Moore&Read-wavefunctions
 {#SupersymmetryBetweenLaughlinAndMooreReadStates}

Consider the [[supermanifold]] ("[[super Cartesian space|Cartesian]] [[superspace]]") version $\mathbb{C}^{1 \vert 1}$ of the [[complex plane]], with canonical holomorphic *super*-coordinates $(z,\theta)$. This carries the [[structure]] of a [[super Lie group]], namely of the complex [[super translation group]], whose group operation is (see [there](super-translation+group#eq:GroupLawIn1D)):

$$
  (z_i, \theta_i)
  +
  (z_j, \theta_j)
  \;=\;
  \big(
    z_i + z_j + \theta_i \theta_i
    ,\,
    \theta_i + \theta_j
  \big)
  \,,
  \;\;\;\;
  -(z, \theta) = (-z, -\theta)
  \,.
$$


Via this super-translation structure, the basic Laughlin state (eq:BasicLaughlinState) lifts to [[superspace]] as

\[
  \label{BasciSuperLaughlinWavefunction}
  \Psi_{sLa}\big(
    (z_1, \theta_1), 
    \cdots
    (z_N, \theta_N)
  \big)
  \;\coloneqq\;
  \textstyle{\prod_{i \lt j}}
  \,
  \big(
    z_i - z_j 
    - \theta_i \theta_j
  \big)^q
  \,
   exp\Big(
     -\frac{1}{4}
     \textstyle{\sum_i} {|z_i|}^2
  \Big)
  \,.
\]

This super-Laughlin wavefunction unifies the basic Laughlin state (eq:BasicLaughlinState) with the basic Moore&Read-state (eq:BasicMooreReadState) in the sense of [[superfields]]:

* the ordinary Laughlin wavefunction (eq:BasicLaughlinState) is its lowest component (the [[coefficient]] of $\theta_i = 0$ for all $i$), 

* the Moore&Read state (eq:BasicMooreReadState) is the top component (the [[coefficient]] of $\theta_1 \cdot \theta_2 \cdots \theta_N$) -- since, by [the Berezinian presentation of the Pfaffian](Pfaffian#PfaffianAsBerezinianIntegral), we have:

$$
  \begin{array}{l}
    \textstyle{\int}
    \left(
      \textstyle{\prod_i} \mathrm{d}\theta_i
    \right)
    \,
    \underset{i \lt j}{\prod}
    ( z_i - z_j  - \theta_i \theta_j )^q
    \\
    \;=\;
    \textstyle{\int} 
    \left(
      \textstyle{\prod_i} \mathrm{d}\theta_i
    \right)
    \,
    \textstyle{\underset{i \lt j}{\prod}}
    \Big(
      ( z_i - z_j )^q
      \,
      \exp\big(
        -q\, ( z_i - z_j )^{-1} \, \theta_i \theta_j
      \big)
      \,
    \Big)
    \\
    \;=\;
    \textstyle{\int} 
    \left(
      \textstyle{\prod_i} \mathrm{d}\theta_i
    \right)
    \,
    \Big(
      \textstyle{\underset{i \lt j}{\prod}}
      ( z_i - z_j )^q
    \Big)
    \Big(
      \textstyle{\underset{i \lt j}{\prod}}
      \exp\big(
        -q\, ( z_i - z_j )^{-1} \, \theta_i \theta_j
      \big)
    \Big)
    \\
    \;=\;
    \Big(
      \textstyle{\underset{i \lt j}{\prod}}
      ( z_i - z_j )^q
    \Big)
    \,
    \textstyle{\int} 
    \left(
      \textstyle{\prod_i} \mathrm{d}\theta_i
    \right)
    \,
    \Big(
      \textstyle{\underset{i \lt j}{\prod}}
      \exp\big(
        -q \, ( z_i - z_j )^{-1} \, \theta_i \theta_j
      \big)
    \Big)
    \\
    \;=\;
    \Big(
      \textstyle{\underset{i \lt j}{\prod}}
      ( z_i - z_j )^q
    \Big)
    \,
    \textstyle{\int} 
    \left(
      \textstyle{\prod_i} \mathrm{d}\theta_i
    \right)
    \,
    \exp\big(
      -q \, 
      \textstyle{\sum_{i \lt j}}
      ( z_i - z_j )^{-1} \, \theta_i \theta_j
    \big)
    \\
    \;=\;
    \left(-\tfrac{q}{2}\right)^{N/2}
    \,
    vd\big(z_\bullet\big)^q
    \,
    pf\left(
      \tfrac
        { 1 }
        { z_{\bullet_1} - z_{\bullet_2} }
    \right)
    \,.
  \end{array}
$$

This observation is due to [Hasebe 2008](#Hasebe08), cf. [Gromov, Martinec & Ryu 2020 (13)](#GromovMartinecRyu20).

To re-amplify how the "statistics" matches across this transformation:

\begin{remark}
  The [[Pfaffian]] $pf\Big( (z_{\bullet_1} - z_{\bullet_2})^{-1} \Big)$ changes sign when swapping any pair of [[variables]] $z_r \leftrightarrow z_s$ (which is manifest in the [Berezinian presentation](Pfaffian#InTermOfBerezinianIntegrals), where it corresponds to equivalently to swapping $\theta_r \leftrightarrow \theta_s$). 

But also the [[Vandermonde determinant]] changes sign when swapping pairs of variables (see [there](Vandermonde+determinant#SkewSymemtryUnderSwappingVariables)). 

This means that:

1. for odd filling fraction $q$:

   1. the ordinary [[Laughlin state]] is *skew-symmetric* in its arguments --- as befits the [[wavefunction]] of [[quantum many-body physics|multiple]] [[fermions]],

   1. the Pfaffian Moore-Read state is *symmetric* in its arguments --- as befits the [[wavefunction]] of [[quantum many-body physics|multiple]] [[bosons]].

1. for even filling fraction $q$ it is the other way around.
  
\end{remark}


### Basic Laughlin wavefunction with quasi-holes
 {#BasicLaughlinStateWithQuasiHoles}

The above Laughlin- and Moore-Read-wavefunctions are meant to model the [[ground states]] of [[fractional quantum Hall systems]] at *exact* Landau level-filling fraction $\nu = 1/q$ where, so the idea, every [[electron]] forms a kind of [[bound state]] with exactly $q$ [[quanta]] of [[magnetic flux]] (see [there](quantum+Hall+effect#IdeaFQHE)). 

But if then the [[magnetic field]] is increased by $n \in \mathbb{N}$ units of flux, a net total of $n$ flux quanta must remain un-paired with electrons. Still imagining that also these un-paired flux quanta are localized in the quantum Hall material, reflected in little [[vortices]] in the "electron fluid", they are imagined to correspond to "holes" (jargon "quasi-holes") in the electron fluid: points where electrons are forced to be *absent*.

A now common proposal for how to modify the basic Laughlin state (eq:BasicLaughlinState) to reflect the presence of $n$ such quasi-holes at positions $\xi_a \in \mathbb{C}$ is to mak these be the external parameters for a [[wavefunction]] of the form &lbrack;[Laughlin 1983 (13)](#Laughlin83)&rbrack;

\[
  \label{LaughlinStateWithQuasiHoles}
  \begin{array}{ccl}
  \psi
    ^{(\xi_1, \cdots, \xi_n)}
    _{La}(z_1, \cdots, z_N)
  &\coloneqq&
  \textstyle{\prod_a} \prod_{i} (z_i - \xi_a)
  \,
  \psi_{La}(z_1, \cdots, z_N)
  \\
  &=&
  \textstyle{\prod_a} \prod_{i} (z_i - \xi_a)
  \,
  \textstyle{\prod_{i \lt j}}
  (z_i - z_j)^q
  \;
  \exp\big(
    -
    \tfrac{1}{4 \ell_B^2} 
    \textstyle{\sum_i} {\vert z_i\vert}^2
  \big)
  \mathrlap{\,.}
  \end{array}
\]

Clearly, the [[probability density]] of this wavefunction vanishes whenever at least one of the electron positions $z_i$ coincides with one of the "electron hole" positions $\xi_a$, and there is non-vanishing [[angular momentum]] concentrated around these holes, as expected for electon-[[vortices]] centered at the $\xi_a$.

Beware that these holes at positions $\xi_a$ are not [[fundamental particles]] like the [[electrons]] at positions $z_i$. Instead, the $\xi_i$ are *external parameters*:
In a less guess-work heavy discussion one would consider the [[Hamiltonian]] of the fractional quantum Hall system parameterized by hole positions, and the above wavefunction (eq:LaughlinStateWithQuasiHoles) would be an approximation to its [[ground state]], also depending on these parameters.

As such, the hole positions $\xi_a$ are "not dynamical" as the electrons are, but may, at least in principle, be moved by forces from outside the system, by changing the [[Hamiltonian]] across its parameter space. Such an  *external parameter-movement* of a [[quantum system]] is described by the [[quantum adiabatic theorem]], which says that, in the suitable adiabatic limit, a rotation of one parameter $\xi_a$ around another will return the quantum state (eq:LaughlinStateWithQuasiHoles) to itself up to (an [[Aharonov-Bohm effect]] due to the [[magnetic field]] and) a *[[Berry phase]]*. This Berry phase is claimed to be &lbrack;[Arovas, Schrieffer & Wilczek 1984 (12)](#ArovasSchriefferWilczek84)&rbrack;
$$
  e^{
    2 \pi \mathrm{i} / q
  }
  \,,
$$
which means that away from the case of the [[integer quantum Hall effect]] where $q = 1$, the [[ground state]] wavefunction will *not quite return to itself* as its defect positions are rotated around each other, but only up to a phase.

Such fractional [[braiding]]-[[Berry phases]] of [[QFT with defects|defects]] under [[quantum adiabatic theorem|adiabatic]] movement are said to identify the defects as being (abelian) *[[anyons]]*.

Beware that [[quantum adiabatic theorem|adiabatic]] [[Berry phases]] of [[QFT with defects|defect]] parameters are conceptually different from "quantum statistics" of [[fundamental particles]] (even if most expositions will say otherwise, and even if the very term "anyon" suggests otherwise): For one, the wavefunction (eq:LaughlinStateWithQuasiHoles) is *symmetric* in the hole positions which, if these were positions of dynamical particles, would make them [[bosons]]. 

In particular, some of the quasi-hole positions may as well coincide, $\xi_a = \xi_b$. Noticing that the Laughlin wavefunction of $q$ *coincident* quasi-holes (at some position $\xi_a \coloneqq \xi \in \mathbb{C}$) among $N$ electrons equals the Laughlin wavefunction of $N + 1$ electrons with one held fixed at $\xi$:

$$
  \psi_{La}^{(\xi_1 = \xi, \cdots, \xi_q = \xi)}(
    z_1, \cdots, z_N)
  \;=\;
  \psi_{La}(
    \xi, z_1, \cdots, z_N
  )
$$

gives another view of how the quasi-holes are *$q$-fractional* objects as compared to the electrons.



\linebreak


## Related concepts

* [[quantum Hall effect]]

* [[conformal block]]


## References

### General

The Laughlin wavefunction is due to

* {#Laughlin83} [[Robert B. Laughlin]]: *Anomalous Quantum Hall Effect: An Incompressible Quantum Fluid with Fractionally Charged Excitations*, Phys. Rev. Lett. **50** (1983) 1395 &lbrack;[doi:10.1103/PhysRevLett.50.1395](https://doi.org/10.1103/PhysRevLett.50.1395)&rbrack;

and the argument for the [[anyon|anyonic]] nature of its quasi-hole excitations is due to

* {#ArovasSchriefferWilczek84} [[Daniel P. Arovas]], [[John Robert Schrieffer]], [[Frank Wilczek]], *Fractional Statistics and the Quantum Hall Effect*, Phys. Rev. Lett. **53** (1984) 722 \[<a href="https://doi.org/10.1103/PhysRevLett.53.722">doi:10.1103/PhysRevLett.53.722</a>\]


Review:

* {#Laughlin99} [[Robert B. Laughlin]]: *Nobel Lecture: Fractional quantization*, Rev. Mod. Phys. **71** 4 (1999) 863 &lbrack;[doi:10.1103/RevModPhys.71.863](https://doi.org/10.1103/RevModPhys.71.863), [pdf](https://www.nobelprize.org/uploads/2018/06/laughlin-lecture.pdf)&rbrack;

* [[Steven M. Girvin]], Section 2.1 of: *Introduction to the Fractional Quantum Hall Effect*, S&eacute;minaire Poincar&eacute; **2** (2004) 53–74, reprinted in *The Quantum Hall Effect*, Progress in Mathematical Physics **45**, Birkhäuser (2005)  &lbrack;[pdf](http://www.bourbaphy.fr/girvin.pdf), [doi:10.1007/3-7643-7393-8_4](https://doi.org/10.1007/3-7643-7393-8_4)&rbrack;

* [[Chetan Nayak]], [[Steven H. Simon]], [[Ady Stern]], [[Michael Freedman]], [[Sankar Das Sarma]], Section III.D.2.c (pp. 1125) of: *Non-Abelian Anyons and Topological Quantum Computation*, Rev. Mod. Phys. **80** 1083 (2008) &lbrack;[arXiv:0707.1888] (http://arxiv.org/abs/0707.1889)&rbrack;

* {#Cooper10} Nigel Cooper: *The Moore-Read Quantum Hall State: An Overview*, talk at *[Quantum Phenomena in
Low-Dimensional Materials and Nanostructures](https://www.lancaster.ac.uk/users/esqn/windsor10/)*, Windsor (2010) &lbrack;[pdf](https://www.lancaster.ac.uk/users/esqn/windsor10/lectures/cooper.pdf), [[Cooper-MooreReadState.pdf:file]]&rbrack;

* {#Tong16} [[David Tong]], Section 3.1 of: *The Quantum Hall Effect* (2016) &lbrack;[course webpage](https://www.damtp.cam.ac.uk/user/tong/qhe.html), [pdf](http://www.damtp.cam.ac.uk/user/tong/qhe/qhe.pdf), [[Tong-QuantumHallEffect.pdf:file]]&rbrack;

* Roman Remme, *The Laughlin Wavefunction*, talk notes (2017) &lbrack;[pdf](https://www.mathi.uni-heidelberg.de/~walcher/teaching/sose17/atqft/writeups/Roman.pdf), [[Remme-LaughlinWavefunction.pdf:file]]&rbrack;


See also:

* Wikipedia, *[Laughlin wavefunction](https://en.wikipedia.org/wiki/Laughlin_wavefunction)*


A "hierarchy" of Laughlin-like states:

* [[Bertrand I. Halperin]]: _Statistics of Quasiparticles and the Hierarchy of Fractional Quantized Hall States_, Phys. Rev. Lett. **52** (1984) 1583 \[<a href="https://doi.org/10.1103/PhysRevLett.52.1583">doi:10.1103/PhysRevLett.52.1583</a>\]

  Erratum, Phys. Rev. Lett. **52** (1984) 2390 \[<a href="https://doi.org/10.1103/PhysRevLett.52.2390.4">doi:10.1103/PhysRevLett.52.2390.4</a>\]

* {#Lan19} [[Tian Lan]], *Matrix formulation for non-Abelian families*, Phys. Rev. B **100** 241102 (2019) \[<a href="https://doi.org/10.1103/PhysRevB.100.241102">doi:10.1103/PhysRevB.100.241102</a>, [arXiv:1908.02599](https://arxiv.org/abs/1908.02599)\]

The pfaffian modification for even-fractional filling factor is due to

* {#MooreRead91} [[Gregory Moore]], [[Nicholas Read]]: *Nonabelions in the fractional quantum hall effect*, Nuclear Physics B **360** 2–3 (1991) 362-396 \[<a href="https://doi.org/10.1016/0550-3213(91)90407-O">doi:10.1016/0550-3213(91)90407-O</a>, [pdf](https://www.physics.rutgers.edu/~gmoore/MooreReadNonabelions.pdf)\]


Critical discussion:

* {#Mikhailov24} S. A. Mikhailov: *Toward a new theory of the fractional quantum Hall effect*, Nanomaterials **14** 2 (2024) 297 &lbrack;[arXiv:2206.05152](https://arxiv.org/abs/2206.05152), [doi:10.3390/nano14030297](https://doi.org/10.3390/nano14030297)&rbrack;




[[!include Laughlin wavefunctions as conformal blocks -- references]]



[[!include supersymmetry in fractional quantum Hall systems -- references]]





[[!redirects Laughlin wavefunctions]]

[[!redirects Laughlin state]]
[[!redirects Laughlin states]]

[[!redirects Moore-Read state]]
[[!redirects Moore-Read states]]

[[!redirects Moore-read wavefunction]]
[[!redirects Moore-Read wavefunctions]]





