


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topological physics
+--{: .hide}
[[!include topological physics -- contents]]
=--
#### Solid state physics
+-- {: .hide}
[[!include solid state physics -- contents]]
=--
=--
=--


# Topological order
* table of contents
{: toc}


## Idea
 {#Idea}

In [[solid state physics]], by *topological order* one refers to a phenomenon that may (but need not) be exhibited by [[quantum materials]] that are in a [[topological phase of matter]]. Hence there is an implication

$$
  \text{topological order}
  \;\;\;\;\;\;\;\;\;
  \Rightarrow
  \;\;\;\;\;\;\;\;\;
  \text{topological phase}
  \,,
$$

but not the other way around.

The definition is traditionally a little vague, but the hallmark of a *topological order* is meant to be the presence, in a [[topological phase of matter|topological phase]], of some or preferably all of the following phenomena:

1. degenerate [[ground state]] (*no* "[[short-range entanglement]]");

1. [[Berry connection]] with [[non-abelian group|non-abelian]] [[holonomy]];

1. [[anyon]] excitations.


\begin{remark}\label{RelationBetweenDefiningConditions}
**(relation between these conditions)**
\linebreak
These above conditions are not exactly equivalent to each other (as far as they are well-defined at all), but closely related. For [[crystal|crystalline]] materials one can say the following, in more detail:

By "degenerate ground state" one just means that the sub-[[Hilbert space]] of [[quantum states]] (for crystalline materials these are the quantum states of  [[electrons]] in the crystal lattice of [[atomic nuclei]]) of those that have the lowest possible [[energy]], has [[dimension of a vector space|dimension]] $\geq 2$.

{#RelationToSRE} (It has been proposed that the presence of "[[short-range entanglement]]" in [[quantum materials]] implies that the ground state Hilbert space is 1-dimensional. In this sense, the condition that the ground state be degenerate implies that there is *no* "[[short-range entanglement]]" if there is "topological order".)

Since (by [[Bloch-Floquet theory]]) the quantum states of these electrons form the [[space of sections]] of the Bloch bundle, and since (by assumption of a [[topological phase of matter|topological phase]]) the ground state involves sections only of the gapped [[sub-bundle]] which is called the *[[valence bundle]]*, this is closely related to the valence bundle having [[rank of a vector bundle|rank]] $\geq 2$.

(In making these statement there is some tacit switching between single-electron theory and its [[second quantization]] involved, sorting out of which would be necessary for being more precise about these matters.)

But since the [[Berry connection]] is a [[connection on a vector bundle|connection]] on the [[valence bundle]], it can have non-abelian [[holonomy]] (namely in [[unitary group|U(n)]] for $n \geq 2$) only if the bundle's rank is $\geq 2$.

Similarly, the presence of [[anyons]] broadly means that there are families of [[quantum adiabatic theorem|adiabatic defomrations]] of the material which have the effect of transforming the [[ground state]] by [[linear operators]] forming a [[braid group representation]]. This is most interesting when the representation is non-abelian, which again requires that the Hilbert space of ground states that it is represented on has dimension $\geq 2$. 

However, there are also non-trivial "abelian anyons", namely braid group representations which are just complex 1-dimensional, and -- even if not as interesting as their non-abelian cousins -- these are counted as perfectly valid instances of the concept of anyons (in fact it was first a struggle and then a breakthrough to detect abelian anyons in [[experiment]]). Some authors, especially those using the language of [[fusion categories]] to speak about anyons, require of a "topological order" only that it contains anyons and possibly just abelian anyons, in which case it is maybe not so clear whether the ground state needs to be degenerate and/or the Berry connection be non-abelian.
  
\end{remark}

In other words (by a previous author of this entry):

Topological order is an order in quantum [[phase of matter]] which is beyond Landau [[symmetry breaking]] order. At long distance
and low energy (ie at macroscopic level), topological order is 
defined by [[topological degeneracy]] (see [Wikipedia](http://en.wikipedia.org/wiki/Topological_degeneracy)) of the ground states and the non-Abelian geometric phases (see [Wilczek & Zee, 1984](#WilczekZee1984)) obtained by deforming the degenerate ground states. The low energy effective theory of a
topologically ordered state is
 a [[topological quantum field theory]]. It has many universal properties that are (by definition) invariant under any small smooth deformations of space-time (or any small deformation of Hamiltonian). The excitations in a topologically ordered state typically have fractional or non-Abelian statistics (for most topological orders in 2+1D).
At microscopic level, topological order corresponds to patterns of long-range [[entanglement]] in the ground state defined by the [[local unitary transformation]]s (see [Chen et al, 2010](#ChenGuWen2010)).

Examples: [[quantum Hall effect]], [[non-abelian anyon|non-Abelian quantum Hall state]] (see [Wikipedia](http://en.wikipedia.org/wiki/Anyon#Non-abelian_anyons)), [[chiral spin state|chiral spin liquid]] (see [Wikipedia](http://en.wikipedia.org/wiki/Topological_order#Chiral_spin_states)), [[Z2 topological order|Z2 spin liquid]] (see [Wikipedia](http://en.wikipedia.org/wiki/Quantum_spin_liquid#Realizations_of_.28stable.29_RVB_states))

* applications in [[topological quantum computing]], study of [[entanglement]], classification of gapped quantum phases, etc. 



## Literature

Related entries: [[topological state of matter]], [[TQFT]], [[quantum computing]], [[quantum Hall effect]], [[modular tensor category]], [[entanglement]]

### Reviews

* Wikipedia: [topological order](http://en.wikipedia.org/wiki/Topological_order)

* [[Xiao-Gang Wen]], _Topological Orders and Edge Excitations in FQH States_,
Advances in Physics 44, 405 (1995). [cond-mat/9506066](http://arxiv.org/abs/cond-mat/9506066). 

* Chetan Nayak, Steven H. Simon, Ady Stern, [[Michael Freedman|M. Freedman]], Sankar Das Sarma, _Non-Abelian anyons and topological quantum computation_, Rev Mod Phys __80__:3 (Aug 2008) 1083&#8211;1159 [MR2009g:81041](http://www.ams.org/mathscinet-getitem?mr=2443722) [doi](http://dx.doi.org/10.1103/RevModPhys.80.1083)

* [[Xiao-Gang Wen]], _An introduction of topological order_ 2009 ([pdf slides](http://dao.mit.edu/~wen/talks/09QHtop.pd), [article](http://dao.mit.edu/~wen/topartS3.pdf))

* Michel Fruchart, David Carpentier, _An Introduction to Topological Insulators_, Comptes Rendus Physique 14 (2013) 779-815 ([arXiv:1310.0255](http://arxiv.org/abs/1310.0255))

### Early discovery articles

* [[Xiao-Gang Wen]], [_Vacuum Degeneracy of Chiral Spin State in Compactified Spaces_](http://dao.mit.edu/~wen/pub/dgn.pdf), Phys. Rev. B, 40, 7387 (1989).

* [[Xiao-Gang Wen]], [_Topological Orders in Rigid States_](http://dao.mit.edu/~wen/pub/topo.pdf), Int. J. Mod. Phys. B4, 239 (1990)

* [[Xiao-Gang Wen]] and Qian Niu,  [_Ground state degeneracy of the FQH states in presence of random potential and on high genus Riemann surfaces_](http://dao.mit.edu/~wen/pub/topWN.pdf), Phys. Rev. B41, 9377 (1990)

* E. Keski-Vakkuri and [[Xiao-Gang Wen]], [Ground state structure of hierarchical QH states on torus and modular transformation](http://dao.mit.edu/~wen/pub/kw.pdf)
Int. J. Mod. Phys. B7, 4227 (1993). 

### Other articles

* Davide Gaiotto, Anton Kapustin, _Spin TQFTs and fermionic phases of matter_, [arxiv/1505.05856](http://arxiv.org/abs/1505.05856)

* N. Read and Subir Sachdev, _Large-N expansion for frustrated quantum antiferromagnets_, Phys. Rev. Lett. 66 1773 (1991) (on $Z_2$ topological order)

* [[Xiao-Gang Wen]], _Mean Field Theory of Spin Liquid States with Finite Energy Gap and Topological orders_, Phys. Rev. B 44 2664 (1991). (on $Z_2$ topological order)

* [[Xiao-Gang Wen]], [Non-Abelian Statistics in the FQH states](http://dao.mit.edu/~wen/pub/nab.pdf)
Phys. Rev. Lett. 66, 802 (1991).

* Moore, Gregory; Read, Nicholas. _Nonabelions in the fractional quantum hall effect_  Nuclear Physics B 360 (2&#8211;3): 362 (1991).

* [[Xiao-Gang Wen]] and Yong-Shi Wu, [_Chiral operator product algebra hidden in certain FQH states_](http://dao.mit.edu/~wen/pub/nabdw.pdf)
Nucl. Phys. B419, 455 (1994).

* Alexei Yu. Kitaev, _Fault-tolerant quantum computation by anyons_, Annals of Physics __303__:1, January 2003; _Anyons in an exactly solved model and beyond_, Annals of Physics __321__:1, January 2006

* [[Michael Levin]], [[Xiao-Gang Wen]], _String-net condensation: A physical mechanism for topological phases_, Phys. Rev. B, 71, 045110 (2005).

* A. Kitaev, C. Laumann, _Topological phases and quantum computation_, [arXiv/0904.2771](http://arxiv.org/abs/0904.2771)

* Alexei Kitaev, John Preskill, _Topological entanglement entropy_, Phys. Rev. Lett. __96__, 110404 (2006)
* Levin M. and Wen X-G., _Detecting topological order in a ground state wave function_, Phys. Rev. Letts.,96(11), 110405, (2006)

* Xie Chen, Zheng-Cheng Gu, [[Xiao-Gang Wen]], _Local unitary transformation, long-range quantum entanglement, wave function renormalization, and topological order_ Phys. Rev. B 82, 155138 (2010), [arXiv](http://arxiv.org/abs/1004.3835)
  {#ChenGuWen2010}

* Jan Carl Budich, Bj&#246;rn Trauzettel, _From the adiabatic theorem of quantum mechanics to topological states of matter_, physica status solidi (RRL) 7, 109 (2013) [arXiv:1210.6672](http://arxiv.org/abs/1210.6672)

* [[zoranskoda:Kumar S. Gupta]], Amilcar Queiroz, _Anomalies and renormalization of impure states in quantum theories_, [arxiv/1306.5570](http://arxiv.org/abs/1306.5570)

* {#WilczekZee1984} Frank Wilczek & A. Zee (1984); Appearance of gauge structure in simple dynamical systems; Physical Review Letters 52 (24), 2111&#8211;2114; [pdf](http://ngs-11.physics.buffalo.edu/rashba/p2111_1.pdf).


* {#JamadagniWeimer20} Amit Jamadagni, Hendrik Weimer, _An Operational Definition of Topological Order_ ([arXiv:2005.06501](https://arxiv.org/abs/2005.06501))



### Research groups

* Univ. of Maryland, [joint quantum institute](http://jqi.umd.edu/research/topological-matter)

* [Topology and correlation in condensed matter](http://tccm.pks.mpg.de) (Germany)

* [Center for topological matter](https://sites.google.com/site/ctmsrc) (Korea)

* [Microsoft Research Station Q](http://research.microsoft.com/en-us/labs/stationq) (KITP, Santa Barbara)

### Conference and seminar cycles

* seminar in Koeln [Topological states of matter](http://www.thp.uni-koeln.de/trebst/Lectures/2012-TopoSeminar.html)

* Topological Phases of Matter: Simons Center, June 10-14, 2013, videos [available](http://scgp.stonybrook.edu/archives/3464)

* CECAM 2013, Topological Phases in Condensed Matter and Cold Atom Systems: towards quantum computations [description](http://www.cecam.org/workshop-867.html)


[[!redirects topological order]]
[[!redirects topological orders]]
