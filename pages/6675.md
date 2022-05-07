
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
considers manipulations of [[anyon]] [[topological defects]] in effectively 2-dimensional [[quantum materials]], such as in the [[quantum Hall effect]] and effectively described by some kind of [[Chern-Simons theory]]/[[Reshetikhin-Turaev construction|Reshetikhin-Turaev theory]]:


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
    "caption": "Adapted from [Rowell & Wang 17](#RowellWang17), [Rouabah 20](#Rouabah20)"
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

* [[quantum Hall effect]], [[anyons]]

* [[topological phase of matter]]

## References


[[!include topological quantum computation with anyons -- references]]



[[!include anyons in the quantum Hall effect -- references]]





[[!include anyons in topological superconductors -- references]]




[[!redirects topological quantum computing]]

[[!redirects topological quantum computation]]


[[!redirects topological quantum computer]]
[[!redirects topological quantum computers]]


