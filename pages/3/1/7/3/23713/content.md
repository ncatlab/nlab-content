
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Solid state physics
+-- {: .hide}
[[!include solid state physics -- contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Generally, a *Berry phase* is a non-trivial phase picked up by a [[quantum state]] of definite [[energy]] under [[quantum adiabatic theorem|adiabatic]] changes of the [[quantum system]]'s [[Hamiltonian]] around a [[loop]] in its parameter space.

Specifically, in [[condensed matter theory]] and  for a [[crystal|crystalline]] material with a set of isolated (gapped) [[electronic band structure|electronic bands]], the [[partial derivatives]] along [[momentum]]-[[vectors]] of the corresponding [[Bloch states]], projected back onto these states, turn out to canonically define a [[connection on a vector bundle|connection]] [[differential 1-form|1-form]] on the [[vector bundles]] (over the [[Brillouin torus]]) which is spanned by these states. This is called a *Berry connection*, due to ([Berry 84](#Berry84), [Simon 83](#Simon83)). The [[parallel transport]] along this connection describes the change of [[Bloch states]] under the [[quantum adiabatic theorem|adiabatic]] change of their [[momentum]]/[[wave vector]].  The [[curvature 2-form]] of a Berry connection is accordingly called the *Berry curvature*.

The [[holonomy]] of such a Berry connection is called a *[[Berry phase]]*, in general, and a *[[Zak phase]]* ([Zak 89](#Zak89)) when evaluated along one of the non-trivial 1-[[cycles]] of the [[Brillouin torus]]. 

By default, this is understood to apply to the [[valence bundle]] of a [[crystal|crystalline]] material, but the construction works more generally. 

{#TopologicalOrder} If in the case of a gapped [[valence bundle]], hence a [[topological insulator]]-phase, the [[holonomy]] of the Berry connection is [[non-abelian group|non-abelian]] (which may happen, as originally highlighted in [Wilczek & Zee 84](#WilczekZee1984)) then one also says that the topological phase exhibits *[[topological order]]*.

For [[semimetals]] the Berry phases of the [[valence bundle]] around their nodal loci of [[codimension]] 2 are a measure for the [[obstruction]] to adiabatically deforming the semimetal such as to open its gap closures, hence to become a ([[topological insulator|topological]]) [[insulator]] (eg. [Vanderbilt 18, 5.5.2](#Vanderbilt18)).


## Examples

### Hall systems

In [[Hall systems]], Berry curvature:

* induces the [[anomalous Hall effect]] 

  (here this is Berry curvature on the "reciprocal space" [[Brillouin torus]] of quasi-[[momenta]] in a [[crystal|crystalline]] material),

* induces the [[anyon]] [braiding phase](quantum+Hall+effect#BraidingPhase) in [[fractional quantum Hall systems]] (see [here](Laughlin+wavefunction#BasicLaughlinStateWithQuasiHoles) at *[[Laughlin wavefunction]]*).


## Related concepts

* [[Berry's phase]] (needs to be merged)

* [[quantum adiabatic theorem]]

## References

### General

The original article:

* {#Berry84} [[Michael V. Berry]], *Quantal phase factors accompanying adiabatic changes*, Proc. R. Soc. Lond. A **392** (1984) 45–57 ([doi:10.1098/rspa.1984.0023](https://doi.org/10.1098/rspa.1984.0023), [jstor:2397741](https://www.jstor.org/stable/2397741))

The formulation in terms of [[connections]] on [[fiber bundles]] and their [[holonomy]]:

* {#Simon83} [[Barry Simon]], *Holonomy, the Quantum Adiabatic Theorem, and Berry's Phase*, Phys. Rev. Lett. **51** (1983) 2167 ([doi:10.1103/PhysRevLett.51.2167](https://doi.org/10.1103/PhysRevLett.51.2167))

Generalization to (connections with) [[non-abelian group|non-abelian]] [[holonomies]]:

* {#WilczekZee1984} [[Frank Wilczek]],  [[Anthony Zee]], *Appearance of gauge structure in simple dynamical systems*, Physical Review Letters **52** 24 (1984) 2111 $[$[doi:10.1103/PhysRevLett.52.2111](https://doi.org/10.1103/PhysRevLett.52.2111)$]$


The special case of Berry phases around the 1-cycles of a [[Brillouin torus]] -- [[Zak phases]]:

* {#Zak89} [[Joshua Zak]], *Berry’s phase for energy bands in solids*, Phys. Rev. Lett. **62** (1989) 2747 ([doi:10.1103/PhysRevLett.62.2747](https://doi.org/10.1103/PhysRevLett.62.2747))



Review and further discussion:

* [[Michael Berry]], *The quantum phase, five years after*, in: *Geometric phases in physics*,  Adv. Ser. Math. Phys. **5**, World Scientific (1989) 7--28 ([[Berry-FiveYearsAfter.pdf:file]], [doi:10.1142/0613](https://doi.org/10.1142/0613))

* Ming-Che Chang, Qian Niu, *Berry curvature, orbital moment, and effective quantum theory of electrons in electromagnetic fields*, J. Phys.: Condens. Matter **20** (2008) 193202 ([doi:10.1088/0953-8984/20/19/193202](https://iopscience.iop.org/article/10.1088/0953-8984/20/19/193202))

* Di Xiao, Ming-Che Chang, Qian Niu, *Berry Phase Effects on Electronic Properties*, Rev. Mod. Phys. **82** (2010) 1959-2007 ([arXiv:0907.2021](https://arxiv.org/abs/0907.2021), [doi:10.1103/RevModPhys.82.1959](https://doi.org/10.1103/RevModPhys.82.1959))

With focus on [[topological phases of matter]] ([[topological insulators]], [[semimetals]], etc.):

* {#Vanderbilt18} [[David Vanderbilt]],  *Berry Phases in Electronic Structure Theory -- Electric Polarization, Orbital Magnetization and Topological Insulators*, Cambridge University Press (2018) ([doi:10.1017/9781316662205](https://doi.org/10.1017/9781316662205))

* [[Jérôme Cayssol]], [[Jean-Noël Fuchs]], Section IV.C of: *Topological and geometrical aspects of band theory*, J. Phys. Mater. **4** (2021) 034007 ([arXiv:2012.11941](https://arxiv.org/abs/2012.11941), [doi:10.1088/2515-7639/abf0b5](https://doi.org/10.1088/2515-7639/abf0b5))

* [[Tudor D. Stanescu]], Chapter 2 of: *Introduction to Topological Quantum Matter & Quantum Computation*, CRC Press 2020 ([ISBN:9780367574116](https://www.routledge.com/Introduction-to-Topological-Quantum-Matter--Quantum-Computation/Stanescu/p/book/9780367574116)) 


See also:

* Wikipedia, *[Berry connection and curvature](https://en.wikipedia.org/wiki/Berry_connection_and_curvature)*

Berry curvature in momentum space is closely analogous to [[magnetic field|magnetic]] [[flux density]] -- the ordinary [[Lorentz force]]-term is analogous to "anomalous group velocity" term induced by Berry curvature:

* Y. D. Chong: *Berry's phase and the anomalous velocity of Bloch wavepackets*, Phys. Rev. B **81** (2010) 052303 &lbrack;[arXiv:0912.0716](https://arxiv.org/abs/0912.0716), [doi:10.1103/PhysRevB.81.052303](https://doi.org/10.1103/PhysRevB.81.052303)&rbrack;


* Michael Stone: *Berry Curvature, Spin, and Anomalous Velocity* &lbrack;[pdf](https://www.thp.uni-koeln.de/ESI-Web/slides/Stone.pdf)&rbrack;



### For anyon statistics

On [[anyon statistics|anyon phases]] (specifically in the [[quantum Hall effect]]) as [[Berry phases]] of a [[quantum adiabatic theorem|adiabatic]] transport of anyon positions:

* {#AvrosSchriefferWilczek84} [[Daniel P. Arovas]], [[John Robert Schrieffer]], [[Frank Wilczek]], _Fractional Statistics and the Quantum Hall Effect_, Phys. Rev. Lett. 53, 722 (1984) $[$[doi:10.1103/PhysRevLett.53.722](https://doi.org/10.1103/PhysRevLett.53.722)$]$


### Experimental observation

Experimental observation of [[Zak phases]]:

* Marcos Atala, Monika Aidelsburger, Julio T. Barreiro, Dmitry Abanin, Takuya Kitagawa, Eugene Demler, Immanuel Bloch: *Direct measurement of the Zak phase in topological Bloch bands*, Nature Physics **9** (2013) 795–800 ([doi:10.1038/nphys2790](https://doi.org/10.1038/nphys2790))

Proposal for experimental realization of [[Berry phases]] around [[codimension]]=2 nodal loci of (quantum simulations of time+space inversion symmetric) [[semi-metals]]:

* Dan-Wei Zhang, Y. X. Zhao, Rui-Bin Liu, Zheng-Yuan Xue, Shi-Liang Zhu, Z. D. Wang, *Quantum simulation of exotic PT-invariant topological nodal loop bands with ultracold atoms in an optical lattice*, Phys. Rev. A **93** (2016) 043617  ([arXiv:1601.00371](https://arxiv.org/abs/1601.00371), [doi:10.1103/PhysRevA.93.043617](https://doi.org/10.1103/PhysRevA.93.043617))

  > (see sec II.A, these authors stand out as mentioning the relevant [[KO-theory]])





[[!redirects Berry connections]]

[[!redirects Berry curvature]]
[[!redirects Berry curvatures]]

[[!redirects Berry phase]]
[[!redirects Berry phases]]

[[!redirects Zak phase]]
[[!redirects Zak phases]]


