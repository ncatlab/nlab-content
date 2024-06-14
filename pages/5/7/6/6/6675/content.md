
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
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

In _topological quantum computation_ one aims to make use of [[quantum systems]] described by [[topological quantum field theory]] for [[quantum computation]], the idea being that the defining invariance of [[TQFTs]] under small deformations implements an intrinsic *fault tolerance* of the quantum computer against [[noise]] and [[decoherence]] (see also at *[[quantum error correction]]*).

### On Anyons in 2+1 d

The standard paradigm for potentially realizing topological quantum computation in practice ([Kitaev 03](#Kitaev03), [Freedman, Kitaev, Larsen & Wang03](#FreedmanKitaevLarsenWang03))
considers [[adiabatic quantum computation|adiabatic]] [[braiding]] of [defect anyons](braid+group+statistics#AsBraidingOfDefects) in effectively 2-dimensional [[quantum materials]], such as in the [[quantum Hall effect]] and [[effective field theory|effectively described]] by some kind of [[Chern-Simons theory]]/[[Reshetikhin-Turaev construction|Reshetikhin-Turaev theory]]:


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

Here topological [[quantum gates]] are encoded by [[braid group]]-elements 
and are executed by [[actions]] through [[braid representations]] on the [[space of quantum states]]:


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
    "caption": "From Sati-Schreiber 21"
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
    "caption": "From [Lahtinen & Pachos 17](#LahtinenPachos17)"
\end{imagefromfile}


### Extended TQC?

It is interesting to note that:

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

* [[Jay Sau]], *A Roadmap for a Scalable Topological Quantum Computer*, [Physics **10** 68 (2017)](https://physics.aps.org/articles/v10/68)

  > "small machines are unlikely to uncover truly macroscopic quantum phenomena, which have no classical analogs. This will likely require a scalable approach to quantum computation. &lbrack;...&rbrack; based on &lbrack;...&rbrack; topological quantum computation (TQC) as envisioned by [[Alexei Kitaev]] and [[Michael Freedman]] &lbrack;...&rbrack; The central idea of TQC is to encode [[qubits]] into states of [[topological phases of matter]]. Qubits encoded in such states are expected to be topologically protected, or robust, against the 'prying eyes' of the environment, which are believed to be the bane of conventional quantum computation."

* {#DasSarma22} [[Sankar Das Sarma]], *Quantum computing has a hype problem*, [MIT Technology Review (March 2022)](https://www.technologyreview.com/2022/03/28/1048355/quantum-computing-has-a-hype-problem/)

  > "The qubit systems we have today are a tremendous scientific achievement, but they take us no closer to having a quantum computer that can solve a problem that anybody cares about. $[\cdots]$ What is missing is the breakthrough $[\cdots]$ bypassing [[quantum error correction]] by using far-more-stable qubits, in an approach called topological quantum computing."



[[!include topological quantum computation with anyons -- references]]



[[!include anyons in the quantum Hall effect -- references]]





[[!include anyons in topological superconductors -- references]]




[[!redirects topological quantum computing]]

[[!redirects topological quantum computation]]


[[!redirects topological quantum computer]]
[[!redirects topological quantum computers]]


