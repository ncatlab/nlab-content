

> For the *[[Haldane phase]]* see instead at *[[Heisenberg model]]*.

***


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Solid state physics
+-- {: .hide}
[[!include solid state physics -- contents]]
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

In [[solid state physics]], the *Haldane model* is a [[model (in theoretical physics)|model]] for effectively 2-[[dimension of a manifold|dimensional]] [[crystalline topological insulator|crystalline]] [[Chern insulators]] (ie. [[topological phases of matter]] "without [[symmetry protected topological phase|symmetry protection]]") -- thus exhibiting a *[[quantum anomalous Hall effect]]* -- obtained by starting with a simple [[model (in theoretical physics)|model]] for a [[graphene]]-like 2d [[semi-metal]] and then adding a [[mass term]] and [[interactions]] (similar to [[spin-orbit coupling]]) which [[symmetry breaking|break]] the [[time-reversal symmetry]] and the [[crystallographic point group|spatial inversion symmetry]].

## Definition


Consider the [[honeycomb lattice|honeycomb crystal lattice]] and consider the following three lattice sites $a_i \in \mathbb{R}^2$:


\begin{imagefromfile}
    "file_name": "HoneycombCrystalLattice.jpg",
    "width": 310,
    "unit": "px",
    "margin": {
        "top": -10,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "(from [DTC](#DTC))"
\end{imagefromfile}

### The graphene-like semi-metal model

The [[Hilbert space]] [[space of quantum states|of quantum states]] of the Haldane model is the [[direct sum]] of copies of $\mathbb{C}^2$ (regarded as the defining/[[fundamental representation]] of [[SU(2)]]) indexed by the sites in a Brillouin zone of this hexagonal lattice.

The un-deformed [[Bloch theory|Bloch]]-[[Hamiltonian]] at [[momentum]]/[[wave vector]] $k$ in the [[Brillouin torus]] $\widehat{\mathbb{T}}^2$ is

\[
  \label{GrapheneLikeHamiltonian}
  H_0(k)
  \;\coloneqq\;
  t_1
  \cdot
  \underoverset{i = 1}{3}{\sum}
  \;
  \big(
    cos(k \cdot a_i)
    \sigma_x 
    -
    \sigma_y
    sin(k \cdot a_i)
  \big)
  \,,
\]

where

1. $t_1 \in \mathbb{R}$ is some real parameter,

1. the [[sum]] ranges over the three unit cell sites shown above,

1. $k \cdot a_i$ denotes the canonical [[inner product]] (evaluation pairing) of the [[wave vector]] with a position space lattice vector,

1. $\sigma_x, \sigma_y, \sigma_z$ are the [[Pauli matrices]] acting as [[linear operators]] of the on-site copies of the [[SU(2)]]-[[linear representation|representation]] $\mathbb{C}^2$.

This undeformed Hamiltonian (eq:GrapheneLikeHamiltonian) is a simple but good model for the [[electronic band structure]] of a [[graphene]]-like 2-dimensional [[semi-metal]].

### Deformation by the Haldane mass term

Consider now also the following next-to-mearest neighbour site vectors $b_i \in \mathbb{R}^2$ in the above honeycomb lattice:


\begin{imagefromfile}
    "file_name": "NextNearNeighbSitesInHoneycLattice-220518.jpg",
    "width": 170,
    "unit": "px",
    "margin": {
        "top": -10,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "(from [DTC](#DTC))"
\end{imagefromfile}


The full [[Bloch theory|Bloch]]-[[Hamiltonian]] of the Haldane model is the deformation of $H_0(k)$ (eq:GrapheneLikeHamiltonian) by a [[mass term]] of the following form:

\[
  \label{HaldaneHamiltonian}
  H(k)
  \;\coloneqq\;
  H_0(k)
  \;+\;
  \underset{
    \mathrm{mass}\;\mathrm{term}
  }{
  \underbrace{
    \left(
       M
       \;+\; 
       2 t_2
       \underoverset{j = 1}{3}{\sum} 
       sin(k \cdot b_i)
    \right)
    \cdot
    \sigma_z
  }
  }
  \,,
\]

where

1. $t_2 \in \mathbb{R}$ is a second [[real number|real]] parameter

1. the sum is now over the above three next-to-nearest neighbour site vectors $b_i$.

Notice that (only) for $t_2 = 0$ this reduces to the deformation by a *constant* mass term (which is often understood as the default meaning of "[[mass term]]"):


\[
  \label{HaldaneHamiltonianForConstantMassTerm}
  H(k)_{t_2 = 0}
  \;=\;
  t_1
  \cdot
  \underoverset{i = 1}{3}{\sum}
  \;
  \big(
    cos(k \cdot a_i)
    \sigma_x 
    -
    \sigma_y
    sin(k \cdot a_i)
  \big)
  \;+\;
  \underset{
    \mathclap{
      \mathrm{constant}\;\mathrm{mass}\;\mathrm{term}
    }
  }{
  \underbrace{
    M 
    \sigma_z
  }
  }
  \,,
\]


## Properties

### Phase diagram
 {#PhaseDiagram}

First of all, the Haldane model 

* at *M = 0* constitutes a non-trivial [[graphene]]-like [[topological semi-metal]]-phase with *two* Dirac points.

\begin{imagefromfile}
    "file_name": "HaldanePhaseDiagram-220518.jpg",
    "float": "right",
    "width": 320,
    "unit": "px",
    "margin": {
        "top": -10,
        "bottom": -10,
        "right": 0, 
        "left": 30
    },
    "caption": "(graphics from [SS 22](#SS22))"
\end{imagefromfile}

  
For $M \neq 0$ and as the parameter $t_2$  (eq:HaldaneHamiltonian) increases, the Haldane model passes, consecutively,  through

1. at $0 \leq t_2/M \lt \frac{1}{3 \sqrt{3}}$ -- in particular where the *mass term is constant* (eq:HaldaneHamiltonianForConstantMassTerm) at $t_2 = 0$ --, a *topologically trivial* [[insulator]]-phase with [[Berry curvature]] concentrated (see [below](#BerryCurvature)) around the would-be Dirac points of the [[graphene]]-like [[semi-metal]] phase which has been gapped out by the constant [[mass term]];

1. at $t_2/M = \frac{1}{3 \sqrt{3}} \sim 0.19$ a non-trivial [[topological semi-metal]]-phase with a *single* band node;

1. at $\frac{1}{3\sqrt{3}} \lt t_2/M$ a *non-trivial* [[topological insulator]]-phase. 
 
   This is the non-trivial *[[Chern insulator]]*-phase of the Haldane model.






### Berry curvature
 {#BerryCurvature}

A curious property of the Haldane model and its cousins (see [Chang, Liu & MacDonald 2023  §II.A](QAH+system#ChangLiuMacDonald23)), possibly not shared by all 2d [[Chern insulators]], is that its [[Berry curvature]] is strongly localized around the (would-be) nodal [[Dirac points]], hence that the [[Berry connection]] is essentially a [[flat connection]] on the [[complement]] of a small [[neighbourhood retract]] of the (would-be) nodal points.

(eg. [Atteia 16, Sec. 2-3.4, p. 4](#Atteia16), [DTC](#DTC) [here](https://topocondmat.org/w4_haldane/haldane_model.html#gap-closings-are-sources-of-berry-curvature))

\begin{imagefromfile}
    "file_name": "BerryCurvatureInHaldaneModelFromAtteia-220518.jpg",
    "width": 620,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "(from [Atteia 16, Fig. 2.7](#Atteia16))"
\end{imagefromfile}

Concretely, the above graphics shows the Berry curvature in the Haldane model for constant mass term, hence in the case that the interaction paramater $t_2$ (eq:HaldaneHamiltonian) vanishes:

\begin{imagefromfile}
    "file_name": "BerryCurvatureInHaldaneModelFromDTC-220518.jpg",
    "width": 340,
    "unit": "px",
    "margin": {
        "top": -10,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "(from [DTC](#DTC))"
\end{imagefromfile}

Since blue and red coloring denotes [[Berry curvature]] of opposite [[sign]], the figure makes it plausibly manifest that the integrated [[Berry curvature]] -- and thus the [[first Chern class|first Chern number]] of the [[valence bundle]] -- *vanishes* for $M \neq 0$, $t_2 = 0$. This is the statement that the [[Chern insulator]]-phase of the Haldane model at $t_2 = 0$ is topologically trivial.

In constract, as $t_2/M \gt \frac{1}{3 \sqrt{3}}$, the [[Berry curvature]] is still concentrated around the would-be Dirac points, but now it has the same sign everywhere:

\begin{imagefromfile}
    "file_name": "PosBerryCurvInHaldaneModelFromDTC-220518.jpg",
    "width": 340,
    "unit": "px",
    "margin": {
        "top": -10,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "(from [DTC](#DTC))"
\end{imagefromfile}

This makes it clear that the [[integration|integral]] of the [[Berry curvature]] over the [[Brillouin torus]] -- hence the [[first Chern class|first Chern number]] of the [[valence bundle]] -- is [[positive number|positive]] in this phase. This is the statement that the [[Chern insulator]]-phase of the Haldane model at $t_2/M \gt \frac{1}{3\sqrt{3}}$ is non-trivial.  


### K-Theory classification?
 {#KTheoryClassification}


The established [[K-theory classification of topological phases of matter]] asserts that ([[twisted equivariant K-theory|twisted equivariant]]) [[topological K-theory]] of gapped [[valence bundles]] over a full [[Brillouin torus]] classifies [[crystalline topological insulator|crystalline]] [[topological insulator]]-phases. For the non-[[symmetry protected topological phases|symmetry protected]] phases relavant for the Haldane model, this is the [[KU-theory]]-classification of [[Chern insulators]].

There has not been much systematic discussion of how to generalize this statement to a classification of [[topological semi-metal]]-phases in some flavor of [[topological K-theory]]. But the [above](#PhaseDiagram) phase behavior of of the Haldane model under deformation by *constant* [[mass terms]] (i.e. at $t_2 = 0$) supports the conjecture that topological semi-metal phases are classified by the (twisted, equivariant) *flat* [[differential K-theory]] of the [[complement]] $\widehat{T}^2 \setminus \{k_1, \cdots, k_N\}$ of the $N$ nodal points $\vec k := k_1, k_2, \cdots, k_N$ inside the [[Brillouin torus]].

Namely, under this assumption the relevant K-theory charges form the following [[double complex]] of [[exact sequences]]:


\begin{imagefromfile}
    "file_name": "SemimetalDoubleSESinKTheory-220519.jpg",
    "width": 750,
    "unit": "px",
    "margin": {
        "top": -10,
        "bottom": -10,
        "right": 0, 
        "left": 30
    },
    "caption": "(graphics from [SS 22](#SS22))"
\end{imagefromfile}


(To see that the boundary of this diagram is as shown, use the [[stable homotopy type]] of the punctured [[torus]] as shown [there](torus#AsAHomotopyType).)

Here the squiggly dashed arrow indicates the mathematical lifting problem which accurately encodes the above statement that topological charges associated to accidental/spurious band nodes (those which actually make for a trivial semi-metal phase, in that there exists a constant [[mass term]] that gaps out the node crossings), give rise to local Berry curvatures whose global topological charge cancels out and thus implies that also the globally gapped phase is topologically trivial:

\begin{imagefromfile}
    "file_name": "LiftingSemimetalDoubleSESinKTheory-220519.jpg",
    "width": 500,
    "unit": "px",
    "margin": {
        "top": -10,
        "bottom": -10,
        "right": 0, 
        "left": 30
    },
    "caption": "(graphics from [SS 22](#SS22))"
\end{imagefromfile}

This accurately reflects what is seen [above](#PhaseDiagram) in the phase diagram of the Haldane mode, for constant mass terms $M$ (which are those that correspond to passage to $\mathrm{K}^{-1}$, by [[Karoubi K-theory]]) but in the absence of interactions ($t_2 = 0$).

\linebreak



## Related concepts

* [[quantum anomalous Hall effect]]

* [[topological phase of matter]]

* [[K-theory classification of topological phases of matter]]

* [[Kane-Mele model]]

## References

### Theory

The original article:

* [[Duncan Haldane]], *Model for a Quantum Hall Effect without Landau Levels: Condensed-Matter Realization of the "Parity Anomaly"*, Phys. Rev. Lett. **61** (1988) 2015-2018 &lbrack;[doi:10.1103/PhysRevLett.61.2015](https://doi.org/10.1103/PhysRevLett.61.2015)&rbrack;

see also 

* Doru Sticlet, Frederic Piéchon, [[Jean-Noël Fuchs]], Pavel Kalugin, Pascal Simon, Section 2.B.1 (pp. 3) of: *Geometrical engineering of a two-bands Chern insulator in two dimensions with arbitrary topological index*, Phys. Rev. B **85** 165456 (2012) &lbrack;[arXiv:1201.6613](https://arxiv.org/abs/1201.6613), [doi:10.1103/PhysRevB.85.165456](https://doi.org/10.1103/PhysRevB.85.165456)&rbrack;


Review:

* *Online course on topology in condensed matter*, *Haldane model, Berry curvature, and Chern number* (2015-) &lbrack;[topocondmat.org/w4_haldane/haldane_model.html](https://topocondmat.org/w4_haldane/haldane_model.html)&rbrack;

* {#Atteia16} [[Jonathan Atteia]], *Topology and electronic transport in Dirac systems under irradiation* (2016) &lbrack;[tel:02426217](https://tel.archives-ouvertes.fr/tel-02426217), [pdf](https://tel.archives-ouvertes.fr/tel-02426217/document)&rbrack;

* {#Vanderbilt18} [[David Vanderbilt]],  Section 5.1.1 of: *Berry Phases in Electronic Structure Theory -- Electric Polarization, Orbital Magnetization and Topological Insulators*, Cambridge University Press (2018) ([doi:10.1017/9781316662205](https://doi.org/10.1017/9781316662205))

* [[Tudor D. Stanescu]], Section 7.2.1 of: *Introduction to Topological Quantum Matter & Quantum Computation*, CRC Press 2020 ([ISBN:9780367574116](https://www.routledge.com/Introduction-to-Topological-Quantum-Matter--Quantum-Computation/Stanescu/p/book/9780367574116)) 

* [[Jérôme Cayssol]], [[Jean-Noël Fuchs]], Section IV.C of: *Topological and geometrical aspects of band theory*, J. Phys. Mater. **4** (2021) 034007 ([arXiv:2012.11941](https://arxiv.org/abs/2012.11941), [doi:10.1088/2515-7639/abf0b5](https://doi.org/10.1088/2515-7639/abf0b5))

Modified Haldene model for [[Chern insulators]]:

* Doru Sticlet, [[Frédéric Piéchon]], [[Jean-Noël Fuchs]], Pavel Kalugin, Pascal Simon, *Geometrical engineering of a two-bands Chern insulator in two dimensions with arbitrary topological index*, Phys. Rev. B **85** 165456 (2012) &lbrack;[arXiv:1201.6613](https://arxiv.org/abs/1201.6613), [doi:10.1103/PhysRevB.85.165456](https://doi.org/10.1103/PhysRevB.85.165456)&rbrack;

* [[Marwa Mannaï]], [[Jean-Noël Fuchs]], [[Frédéric Piéchon]], [[Sonia Haddad]], *Stacking-induced Chern insulator* &lbrack;[arXiv:2208.02491](https://arxiv.org/abs/2208.02491)&rbrack;



Much of the above material follows:

* {#DTC} Delft Topology Course team, *[Haldane model, Berry curvature, and Chern number](https://topocondmat.org/w4_haldane/haldane_model.html#first-try)*

Some of the above material is taken from:

* {#SS22} [[Hisham Sati]], [[Urs Schreiber]]: *[[schreiber:Anyonic topological order in TED K-theory]]*

### Experiment

Realization in [[experiment]]:

* {#JMDLUGE14} Gregor Jotzu, Michael Messer, Rémi Desbuquois, Martin Lebrat, Thomas Uehlinger, Daniel Greif,  Tilman Esslinger:

  *Experimental realization of the topological Haldane model with ultracold fermions*, Nature **515** (2014) 237–240  &lbrack;[doi:10.1038/nature13915](https://doi.org/10.1038/nature13915)&rbrack;


[[!redirects Haldane models]]

