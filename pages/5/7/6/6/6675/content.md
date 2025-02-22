
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
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



#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

The idea of *topological quantum computation* is to implement [[quantum computation]] on [[quantum systems]] whose dynamics is described by [[topological quantum field theory]] (TQFT), so that the defining invariance of TQFTs under local perturbations implements protection of the [[quantum coherence]] by fundamental physical principles, instead of after the fact by [[quantum error correction]].
 

\linebreak

### General idea 
 {#GeneralIdea}


\linebreak


**The Problem of Contemporary Quantum Computing.**

Common quantum computing architectures 

> (such as based on [superconducting qbits](superconductivity#SuperconductingQBitsReferences), [[trapped-ion quantum computing|trapped ions]], [spin resonance](nuclear+magnetic+resonance#SpinResonanceQBitsReferences), ...)

suffer from an intrinsic tension:

1. [[quantum gates]] are **implemented via [[interaction]]** between [[subsystems]],

1. but [[quantum coherence|coherence]] requires **avoiding interaction**.

> (cf. [Waintal 2024, p3](quantum+computing#Waintal24) or [CCEHRSZ 07](quantum+computation#CCEHRSZ07) p 272: "*Quantum logic gates involving two atomic qubits must overcome the problem of the short range coherent interaction of neutral atoms, while maintaining atom confinement and suppressing decoherence. The main challenge is to perform the gate sufficiently fast compared to typical decoherence and relaxation times.*")

This problem haunts contemporary [NISQ](quantum+computation#ReferencesNISQ) devices (cf. [HHT 23](quantum+computation#HHT23)), 

whence the "Quantum Winter" (cf. [McKenzie 24](quantum+computation#McKenzie2024)).

\linebreak

**The bold idea of Topological Quantum Computing** is to cut this Gordian knot:

Find **quantum gates operating without interaction**!

Can this work? In principle: Yes! 

> (By a phenomenon known as the "[[quantum adiabatic theorem]]".)

\linebreak

For this we need a quantum system (say a crystalline [[quantum material]]) 

with the following properties:

1. **ground states degenracy**:

   even when completely frozen at [[absolute zero]] [[temperature]]

   the system has more than one state to be in (even up to phase)

   > (Meaning: The [[Hilbert space]] $\mathscr{H}$ of [[quantum states]] with [[energy]] [[eigenvalue]] $E = 0$ is of [[dimension of a vector space|dimension]] $\geq 2$.)

2. an **energy gap** $\epsilon \gt 0$:

   every excitation of the ground state has energy larger than $\epsilon$

   so that ([[light]]) [[quanta]] impacting the material have **no interaction** as long as they carry energy $\lt \epsilon$.

   > (Meaning: The material's [[Hamiltonian]] has a [[spectral gap]] above the [[ground state]].)
  
3. {#ControlParameters} **control parameters**:

   the above properties hold for a range of [[continuous function|continuously]] tunable parameters

   such as [[strain]] or [[voltage]] applied to the crystal

   > (Meaning: We have [[vector bundle]] of [[ground state]] [[Hilbert spaces]] $\mathscr{H}_p$ over a [[topological space]] $P$ of parameter values $p \in P$.)

\linebreak

**Adiabatic Transformation of Ground States.**

Under these conditions:

* after cooling such a system to its ground state,

* sufficiently slow ("[[quantum adiabatic theorem|adiabatic]]") variation of the external parameters

* does not excite the system: it *remains* in a ground state

* but **the different ground states may transform into each other**

  > (Meaning: Each parameter path $\gamma \,\colon\, p \to p'$ induces a [[Berry phase]] [[unitary operator]] $U_\gamma \,\colon\, \mathscr{H}_p \xrightarrow{\;} \mathscr{H}_{p'}$.)


\linebreak

This is part of a general phenomenon of [[quantum physics]]:

While [[quantum fluctuations]] are a little like [[thermodynamics|thermal]] fluctuations

one key difference is that they remain present at [[absolute zero]].

> (Compare *[[quantum phase transitions]]*.)


\linebreak

Such operations on ground states are called **[holonomic quantum gates](adiabatic+quantum+computation#ReferencesGeometricPhaseGates)**.

> (From "[[holonomy]]" for the [[parallel transport]] of a [[Berry connection]] along [[loops]].)

These are **protected from external [[noise]]** quanta of energy $\lt \epsilon$

**but** may still be sensitive no **[[noise]] in the parameter paths**.

\linebreak

**Topological invariance.**

To overcome this last issue, look for such quantum systems which *in addition* have:

1. **parameter topology**

   The parameter space has "holes", in that

   some closed parameter paths cannot continuously be deformed to constant paths.

   > (Meaning: The [[fundamental group]] of parameter space is non-[[trivial group|trivial]].)

1. **local parameter independence**

   All parameter paths with the same endpoints

   that are continuous deformations of each other

   yield the same transformation on ground states.

   > (Meaning: The [[Berry connection]] is [[flat connection|flat]].)

[[quantum material|Quantum materials]] with all these properties are **[[topological order|topologically ordered]]**;

the resulting adiabatic quantum processes are **[[topological quantum computation|topological quantum gates]]**.

\linebreak

In principle, such topological quantum gates are:

1. protected against external [[noise]] quanta of [[energy]] $\lt \epsilon$, *and*

2. protected against any [[noise]] in the parameter path.

In fact, the quantum operation induced by a parameter variation will

*depend only on the discrete data* of 

**how much the path winds around the holes** of parameter space

<center>
<a href="https://arxiv.org/pdf/2303.02382#page=21">
<img src="/nlab/files/TopologicalGateSchematics.jpg" width="740">
</a>
</center>

\linebreak

This way, 

topological quantum architecture may in principle 

(be necessary to) solve the problem of quantum computing.

> (cf. [Sau 2017](#Sau17), [Das Sarma 2022](topological+quantum+computation#DasSarma22))

\linebreak

So far this is the **theory behind topological quantum gates**.

On the one hand it is extremely general: 

* any kind of topologically parameterized quantum system could do.

On the other hand it is very ambitious: 

* suitable such system have yet to be devised in the labs.

\linebreak

But the range of possibilities has hardly been explored,

most attention has been given to a single approach:

* braiding of anyonic defects in position space.

\linebreak

That's what we discuss [next](#IdeaViaAnyonBraiding). 


\linebreak







### Via anyon braiding
 {#IdeaViaAnyonBraiding}


In specialization of the [above general idea](#GeneralIdea), the  

original proposal due to [Kitaev 2003](#Kitaev03) and [FKLW 2003](#FreedmanKitaevLarsenWang03) (which has become canonized in the literature) is to envision 

* an effectively 2-dimensional [[quantum material]]  (such as an atomic monolayer similar to [[graphene]]),

* with some *[[defect]] points* of sorts (whose expected nature in real materials remains vague at this point),

* whose positions constitute the [above parameters](#ControlParameters), hence whose parameter space is a [[configuration space of points]] in the plane.

The  [[motion group|motion]] in such a parameter space is a [[braid]] (of "[[worldlines]]" of defect points) and 

if this acts non-trivially on the material's ground states by [[quantum adiabatic theorem|adiabatic]] transformations, 

then one refers to these defects as **[[defect]] [[anyons]]**:

<center>
<a href="https://arxiv.org/pdf/2411.00628#page=7">
<img src="/nlab/files/AnyonBraidingSchematics.jpg" width="600">
</a>
</center>

> (graphics from [[schreiber:Topological QBits in Flux-Quantized Supergravity|SS24]])

\linebreak

**Status of anyonic quantum computation.**

Experimentally, 

at least *[abelian anyons](#FocusOnAbelianAnyons)* 

> (whose [[braid representation]] factors through a [[representation of the symmetric group]]) 

[are seen](braid+group+statistics#ExperimentalRealization) in [[fractional quantum Hall effect|fractional quantum Hall systems]], 

though their controlled movement along the above lines seems out of reach. 

\linebreak

{#ChernSimonsTheory} Theoretically, 

such defect anyons are expected to be [[effective field theory|effectively described]] by 

some kind of [[Chern-Simons theory]]/[[Reshetikhin-Turaev construction|Reshetikhin-Turaev theory]]

> (and hence ultimately classified by [[modular tensor categories]]),

though attempts to derive some of these expectations from microscopic physics are rare.

> (A more microscopic argument for anyonic defects not in position-space but in "reciprocal" momentum-space -- the [[Brillouin torus]] --, appearing there as the familiar [[band nodes]] of [[topological semimetals]], is made in [[schreiber:Anyonic topological order in TED K-theory|SS23]].)

\linebreak

**The open problem of strongly-coupled quantum systems.**

A general problem on both of these fronts is that 

anyonic [[topological order]] is supposed to arise in [[strongly correlated systems]] which, like 

all [[non-perturbative field theory|non-perturbative physics]], remains ill-understood in general.

\linebreak

The directly analogous problem in [[particle physics]],

where the the [[energy gap]] is known as the *[[mass gap]]*,

has been termed a [Millennium Problem](https://en.wikipedia.org/wiki/Millennium_Prize_Problems) by the [Clay Math Institute](https://www.claymath.org/)

> (cf. the [Mass Gap Problem](mass gap#ReferencesMassGapProblem))

\linebreak

One plausible approach on this front is to find 

**[[geometric engineering of quantum field theory|geometric engineering]]** of anyonic [[topological order]] on [[M-branes]] 

or their **[[AdS-CFT in condensed matter physics|holographic dual]]** [[D=11 supergravity|bulk gravity]].

> (cf. [CGK20](topological+order#CGK20), [SS24](topological+order#SS24)) 



\linebreak

**Loosely related approaches.**

Much attention in the 2010s had been given to claims of experimental detection of anyons in the form of "[[Majorana zero modes]]" (MZMs) -- but these claims [seem not to hold water](Majorana+zero+mode#But). In any case, these MZMs are by design stuck at the end of nanowires and hence are not movable and in particular not braidable in the above sense.

More recently the idea of *[quantum *simulation* of anyons](quantum+simulation+OfAnyons)* on ordinary quantum hardware has found more attention, though the relevance of this, if any, to the original idea of quantum-error protection by fundamental physical principles may remain to be discussed.

\linebreak


**Topological quantum protocols.**

Topological quantum computation protocols with defect anyons are often assumed to start by creating anyon/anti-anyon pairs out of the "anyon [[vacuum]]", then braid their worldlines and finally annihilate them again --- so that the total process is described by a [[link]] which, when regarded as a [[Wilson loop]], may be understood as parameterizing a [[quantum observable]] of the [[Chern-Simons theory]] mentioned [above](#ChernSimonsTheory):


\begin{imagefromfile}
    "file_name": "TQCOnAnyonsIdea.jpg",
    "width": 600,
    "unit": "px",
    "margin": {
        "top": -10,
        "bottom": -10,
        "right": 0, 
        "left": 10
    },
    "caption": "Adapted from [Rowell & Wang 18](#RowellWang18), [Rouabah 20](#Rouabah20)"
\end{imagefromfile}

\linebreak

In any case, in this scheme the topological [[quantum gates]] are encoded by [[braid group]]-elements and are executed by [[actions]] through [[braid representations]] on the [[space of quantum states]]:


\begin{imagefromfile}
    "file_name": "QuantumGatesAsBraidGroupRepresentations.jpg",
    "width": 600,
    "unit": "px",
    "margin": {
        "top": -10,
        "bottom": -10,
        "right": 0, 
        "left": 10
    },
    "caption": "(from Sati-Schreiber 21)"
\end{imagefromfile}


\begin{imagefromfile}
    "file_name": "QuantumBraidGateI.jpg",
    "width": 600,
    "unit": "px",
    "margin": {
        "top": -0,
        "bottom": -10,
        "right": 0, 
        "left": 10
    },
    "caption": "(from [Lahtinen-Pachos 17](#LahtinenPachos17))"
\end{imagefromfile}

\linebreak

**Topological Quantum Compilation.**

This means that quantum gates based on anyon braiding are (going to be) quite different from the [standard](quantum+logic+gate#Examples) [[quantum gates]] traditionally considered in [[qbit]]-based [[quantum circuits]].

{#BraidImplementingCNotGate} For example, the following lengthy braid has been proposed &lbrack;[Hormozi, Zikos, Bonesteel & Simon (2007)](#HormoziZikosBonesteelSimon07)&rbrack; as a possible topological implementation of a *single* [[CNOT gate]]:

<center>
<img src="https://ncatlab.org/nlab/files/BraidImplementingCNOTGate.jpg" width="800">
</center>

Hence if and when such topological quantum hardware becomes available, a major issue on the quantum software side will be the *[[quantum compilation|compilation]]* of [[quantum algorithms]] to the exotic-seeming machine-level gates (cf. *[topological quantum compilation](/nlab/show/Solovay-Kitaev+theorem#ReferencesInTopologicalQuantumComputation)*). 

It [has been argued](certified+programming#ReferencesForQuantumProgrammingLanguages) that the complexity of this process will make its [[certified programming|formal verification]] a practical necessity.



\linebreak


### Extended TQC?

It may be interesting to note that:

* ([[pure braid group|pure]]) [[braid group representations]] are equivalently degree-1 [[cocycles]] in the [[non-abelian cohomology]] of the [[configuration space of points]] (ordered) in the [[Euclidean plane]],;

* as such, [[braid representations]] are the first stage in a sequence that continues with [[weight systems]] on [[horizontal chord diagrams]], these being the [[complex cohomology]] in higher degree of the [[configuration space of points]] (ordered) in Euclideam 3-space (see at *[[weight systems are cohomology of loop space of configuration space]]*):

\begin{imagefromfile}
    "file_name": "BraidRepresentationsAndWeightSystemsAnalogy.jpg",
    "width": 700,
    "unit": "px",
    "margin": {
        "top": -10,
        "bottom": -10,
        "right": 0, 
        "left": 10
    },
    "caption": "from Sati-Schreiber 2021"
\end{imagefromfile}

Here 

* $Conf_N(\mathbb{R}^2) \simeq K( PBr(N), 1 ) \simeq B PBr(n)$ is an [[Eilenberg-MacLane space]]/[[classifying space]] for the [[pure braid group]]

* $Conf_N(\mathbb{R}^3)$ is a [[simply connected topological space|simply connected]] higher [[homotopy type]]:

This means that while every individual loop in $Conf_N(\mathbb{R}^3)$ is homotopically trivial (all "braid-gates" are equivalent) there is now non-trivial structure in higher-dimensional deformation families of braids (which is absent in $Conf_N(\mathbb{R}^2)$). Such structure would be reflected by [[extended TQFT]].


## Related concepts

* [[quantum Hall effect]]

* [[anyons]]

* [[topological order]]

* [[topological phase of matter]]

* [[quantum computation]]

  * [[adiabatic quantum computation]]

  * [[measurement-based quantum computation]]



## References
  {#References}

### Need for topological protection
  {#ReferencesNeedForTopologicalProtection}

Highlighting the need for topological stabilization mechanisms:


* [Freedman, Kitaev, Larsen & Wang 2003](#FreedmanKitaevLarsenWang03):
  > "the chief advantage of anyonic \[topological quantum\] computation would be physical error correction: An error rate scaling like $e^{- \alpha \ell}$, where $\ell$ is a length scale, and $\alpha$ is some positive constant. In contrast, the “presumptive” qubit-model of quantum computation, which repairs errors combinatorically, requires a fantastically low initial error rate (about $10^{-4}$) before computation can be stabilized. \[...\]
  > To reduce this model to engineering, very significant obstacles must be overcome: \[...\] Although these challenges are daunting, they are, perhaps, less difficult than a head-on assault on the accuracy threshold in the quantum circuit model.

* {#Sau17} [[Jay Sau]], *A Roadmap for a Scalable Topological Quantum Computer*, [Physics **10** 68 (2017)](https://physics.aps.org/articles/v10/68)
  > "small machines are unlikely to uncover truly macroscopic quantum phenomena, which have no classical analogs. This will likely require a scalable approach to quantum computation. &lbrack;...&rbrack; based on &lbrack;...&rbrack; topological quantum computation (TQC) as envisioned by [[Alexei Kitaev]] and [[Michael Freedman]] &lbrack;...&rbrack; The central idea of TQC is to encode [[qubits]] into states of [[topological phases of matter]]. Qubits encoded in such states are expected to be topologically protected, or robust, against the 'prying eyes' of the environment, which are believed to be the bane of conventional quantum computation."

* {#DasSarma22} [[Sankar Das Sarma]], *Quantum computing has a hype problem*, [MIT Technology Review (March 2022)](https://www.technologyreview.com/2022/03/28/1048355/quantum-computing-has-a-hype-problem/)
  > "The qubit systems we have today are a tremendous scientific achievement, but they take us no closer to having a quantum computer that can solve a problem that anybody cares about. \[...\] What is missing is the breakthrough \[...\] bypassing [[quantum error correction]] by using far-more-stable qubits, in an approach called topological quantum computing."



[[!include topological quantum computation with anyons -- references]]



[[!include anyons in the quantum Hall effect -- references]]





[[!include anyons in topological superconductors -- references]]



[[!redirects topological quantum computing]]

[[!redirects topological quantum computation]]


[[!redirects topological quantum computer]]
[[!redirects topological quantum computers]]


