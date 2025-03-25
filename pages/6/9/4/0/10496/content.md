
> This entry is about topological orders of materials in [[condensed matter physics]]. For topological orders of directed acyclic graphs in [[graph theory]], see [[linear extension of a partial order]]. 

***

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

In [[solid state physics]], by *topological order* ([Wen 89](#Wen89),  [Wen & Niu 90](#WenNiu90), [Wen 91](#Wen91), [93](#Wen93), [95](#Wen95), [Gu & Wen 09, p. 2](#GuWen09), [Chen, Gu & Wen 10](#ChenGuWen2010)) one refers to a phenomenon that may (but need not) be exhibited by [[quantum materials]] that are in a [[topological phase of matter]]. Hence there is an implication

$$
  \text{topological order}
  \;\;\;\;\;\;\;\;\;
  \Rightarrow
  \;\;\;\;\;\;\;\;\;
  \text{topological phase}
  \,,
$$

but not the other way around.

Specifically, the [[ground state]] of a topologically ordered material is rich in structure (besides being topologically stable), which need not be the case for a general topological phase. In particular a topologically ordered ground state is "degenerate" (a standard but somewhat unfortunate jargon in this context: it really refers to the *[[energy]]* [[eigenvalues]] being degenerate) in that there is a $\geq 2$-dimensional Hilbert space of [[quantum states]] that all have the same lowest energy (within experimentally relevant approximation). 

Moreover, for this to qualify as topologically ordered, one typically demands that in its degenerate ground state the system may exhibit "[[anyon|anyonic]] [[defects]]". A popular more succinct way of making this somewhat more precise is to say that the [[dynamics]] of (the [[electrons]] in) a topologically ordered material, when restricted to the energy=0 ground states, is a [[topological field theory]] equal or akin to a [[Chern-Simons theory]] with [[Wilson line]]-insertions: these Wilson lines being the [[worldlines]] of the [[anyon]]-[[defects]]. 

In short then, topological order is meant to be that aspect of [[topological phases of matter]] which is related to the existence of [[anyons]] in the material, in one way or other. Via this relation, topological order is closely related to considerations in [[topological quantum computation]].


### Via degenerate anyonic ground states
 {#ViaDegenerateAnyonicGroundStates}

The definition is traditionally a little vague, but the hallmark of a *topological order* is meant to be the presence, in a [[topological phase of matter|topological phase]], of some or preferably all of the following phenomena ([Gu & Wen 09, p. 2](#GuWen09), called the "modern day philosopher's stone" in [Tsvelik 2014b](parafermion#Tsvelik14b)):

1. degenerate [[ground state]] ([Wen 89, p. 4](#Wen89), [Wen 95, Sec. 1.1](#Wen95));  

1. [[Berry connection]] with [[non-abelian group|non-abelian]] [[holonomy]];

1. [[anyon]] excitations/defects whose [[wavefunctions]] constitute [[braid group representations]] ("[[anyon statistics|fractional statistics]]").

The original articles ([Wen 89](#Wen89),  [Wen & Niu 90](#WenNiu90), [Wen 91](#Wen91), [93](#Wen93), [95](#Wen95)) proposed to declare that [[topological phase of matter|topological phases]] with distinct ground state degeneracy exhibit distinct topological order. The demand that also the [[Berry connection]] should be non-abelian for there to be a topological order seems to appear first in [Wen 91 review](#Wen91Review) (then also [Gu & Wen 09, p. 2](#GuWen09)). Or maybe the claim is rather that two distinct topological orders may have the same ground state degeneracy but be distinguished by their Berry connections.


\begin{remark}\label{RelationBetweenDefiningConditions}
**(relation between these conditions)**
\linebreak
By "degenerate ground state" one just means that the sub-[[Hilbert space]] of [[quantum states]] (for crystalline materials these are the quantum states of  [[electrons]] in the crystal lattice of [[atomic nuclei]]) of those that have the lowest possible [[energy]], has [[dimension of a vector space|dimension]] $\geq 2$.

{#RelationToSRE} (It has been proposed that the presence of "[[short-range entanglement]]" in [[quantum materials]] implies that the ground state Hilbert space is 1-dimensional. In this sense, the condition that the ground state be degenerate implies that there is *no* "[[short-range entanglement]]" if there is "topological order".)

Since (by [[Bloch-Floquet theory]]) the quantum states of these electrons form the [[space of sections]] of the Bloch bundle, and since (by assumption of a [[topological phase of matter|topological phase]]) the ground state involves sections only of the gapped [[sub-bundle]] which is called the *[[valence bundle]]*, this is closely related to the valence bundle having [[rank of a vector bundle|rank]] $\geq 2$.

(In making these statement there is some tacit switching between single-electron theory and its [[second quantization]] involved, sorting out of which would be necessary for being more precise about these matters.)

But since the [[Berry connection]] is a [[connection on a vector bundle|connection]] on the [[valence bundle]], it can have non-abelian [[holonomy]] (namely in [[unitary group|U(n)]] for $n \geq 2$) only if the bundle's rank is $\geq 2$.

Similarly, the presence of [[anyons]] broadly means that there are families of [[quantum adiabatic theorem|adiabatic defomrations]] of the material which have the effect of transforming the [[ground state]] by [[linear operators]] forming a [[braid group representation]]. This is most interesting when the representation is non-abelian, which again requires that the Hilbert space of ground states that it is represented on has dimension $\geq 2$. 

However, there are also non-trivial "abelian anyons", namely braid group representations which are just complex 1-dimensional, and -- even if not as interesting as their non-abelian cousins -- these are counted as perfectly valid instances of the concept of anyons (in fact it was first a struggle and then a breakthrough to detect abelian anyons in [[experiment]]). Some authors, especially those using the language of [[fusion categories]] to speak about anyons, require of a "topological order" only that it contains anyons and possibly just abelian anyons, in which case it is maybe not so clear whether the ground state needs to be degenerate and/or the Berry connection be non-abelian.
  
\end{remark}

### Via topological entanglement entropy
 {#ViaTopologicalEntanglementEntropy}

It is now thought that some/all of the [above](#ViaDegenerateAnyonicGroundStates) characteristics may be captured [[quantum information theory|quantum information theoretically]] in terms of the [[entanglement entropy]] of the [[ground state]]:

The non-degeneracy of the ground state is related to *absence* of "[[short-range entanglement]]";
and the existence of anyon excitations is related to the *presence* of "[[long-range entanglement]]" ([Chen, Gu & Wen 10, Sec. 5](#ChenGuWen2010)) witnessed by a non-vanishing *[[topological entanglement entropy]]* ([Kitaev & Preskill 2006](entanglement+entropy#KitaevPreskill06), [Levin & Wen 2006](entanglement+entropy#LevinWen06)).  

Often one sees topological order being related also to (1) *strong interaction* and/or (2) *strong quantum correlation* ([Wen 91 review](#Wen91Review)) between the electrons (while the classical [[electron band theory]] that gives rise to the widely-accepted [[K-theory classification of topological phases of matter]] assumes that it is sensible to *neglect* the interaction of electrons between each other and only retain their interaction to an effective Coulomb [[background field]]).

{#BewareOfCorrelation} Beware that the use of the term "correlation" in the context of topological order (cf. [Wen 91 review ](#Wen91Review)) is always meant as "quantum correlation" and specifically as "non-classical quantum correlation"  and as such used as a synonym for *[[quantum entanglement]]* (cf. [ZCZW 19, §1.5](#ZCZW19) and generally [Luo & Luo 03, p. 3](entanglement#LuoLuo03)). In contrast, long-range *classical correlation* is indicative of *non-topological* [[Landau theory]]-phases and hence the opposite of what is relevant here. 
 
Together with the entanglement-theoretic characterization just mentioned, the logic here seems to be the following sequence of schematic implications:

\begin{tikzcd}[
  column sep=12pt,
  row sep=-2pt,
]
  \mathrlap{
    \mbox{
      \hspace{-2cm}
      topological phase with...
    }
  }
  \\
    \fbox{
      \begin{tabular}{c}
      strong/long-range
      \\
      interaction
      \end{tabular}
    }
    \ar[r, Rightarrow]
    &
    \fbox{
      \begin{tabular}{c}
      strong/long-range
      \\
      quantum correlation
      \end{tabular}
    }
    \ar[r, Leftrightarrow]
    &
    \fbox{
      \begin{tabular}{c}
        long-range 
        \\
        entanglement
      \end{tabular}
    }
    \ar[r, Rightarrow]
    &
    \fbox{
      \begin{tabular}{c}
        topological 
        \\
        entanglement 
        \\
        entropy
      \end{tabular}
    }
    \ar[r, Leftrightarrow]
    &
    \fbox{
      \begin{tabular}{c}
      topological
      \\
      order
      \end{tabular}
    }
    \ar[r, Leftrightarrow]
    &
    \fbox{
      \begin{tabular}{c}
      anyons
      \end{tabular}
    }
\end{tikzcd}

> (diagram adapted from [SS22](#SatiSchreiber22))

The first steps in this sequence is intuitively plausible and widely expected to hold (eg. [Lu & Viyah 2022, p. 1](entanglement+entropy#LuVijay22)) but not currently derivable from first principles ([Zaanen, Liu, Sun & Schalm 2015, p. 527](entanglement+entropy#ZaanenLiuSunSchalm15)):
 
If the [[electromagnetic field|Coulomb]] interaction between the electrons -- which by itself is certainly strong and long-range -- cannot be neglected (hence if the averaging- or screening-effects that make [[electron band theory]] work do not apply) then this strong interaction makes the electrons in the ground state be correlated with each other, one way or other, across non-negligible distances; and quantum mechanically this leads to the ground state's entanglement entropy having long-range contributions, which,  essentially by definition, means that it has a constant contribution by the *topological* entanglement entropy.

## Examples
 {#Examples}

> under construction

* [[quantum Hall effect]]

* [[non-abelian anyon|non-Abelian quantum Hall state]] (see [Wikipedia](http://en.wikipedia.org/wiki/Anyon#Non-abelian_anyons))

* [[chiral spin state|chiral]] [[spin liquid]] (see [Wikipedia](http://en.wikipedia.org/wiki/Topological_order#Chiral_spin_states))

* [[Z2 topological order|$\mathbb{Z}/2$]] [[spin liquid]] (see [Wikipedia](http://en.wikipedia.org/wiki/Quantum_spin_liquid#Realizations_of_.28stable.29_RVB_states))

* [[toric code]]


## Related concepts

* [[topological state of matter]], 

  * [[quantum Hall effect]]

* [[TQFT]], [[Chern-Simons theory]]

* [[string-net model]]

* [[quantum computing]]

* [[modular tensor category]]

* [[entanglement]]



## Literature


### Original articles
 {#OriginalArticles}

The proposal that ground state degeneracy is a signature of "topological order":

* {#Wen89} [[Xiao-Gang Wen]], *Vacuum degeneracy of chiral spin states in compactified space*, Phys. Rev. B **40** (1989) 7387(R) $[$[doi:10.1103/PhysRevB.40.7387](https://doi.org/10.1103/PhysRevB.40.7387)$]$

* {#WenNiu90} [[Xiao-Gang Wen]],  Q. Niu, *Ground-state degeneracy of the fractional quantum Hall states in the presence of a random potential and on high-genus Riemann surfaces*, Phys. Rev. B **41** (1990) 9377 $[$[doi:10.1103/PhysRevB.41.9377](https://doi.org/10.1103/PhysRevB.41.9377)$]$

* {#Wen91} [[Xiao-Gang Wen]], *Non-Abelian statistics in the fractional quantum Hall states*, Phys. Rev. Lett. **66** (1991) 802 &lbrack;[doi:10.1103/PhysRevLett.66.802](https://doi.org/10.1103/PhysRevLett.66.802), [pdf](https://xgwen.mit.edu/sites/default/files/documents/nab.pdf)&rbrack;

* {#Wen93} [[Xiao-Gang Wen]], *Topological order and edge structure of $\nu = 1/2$ quantum Hall state*, Phys. Rev. Lett. **70** (1993) 355 \[<a href="https://doi.org/10.1103/PhysRevLett.70.355">doi:10.1103/PhysRevLett.70.355</a>\]

* {#Wen95} [[Xiao-Gang Wen]], *Topological orders and Edge excitations in FQH states*, Advances in Physics **44** (1995) 405 \[<a href="https://doi.org/10.1080/00018739500101566">doi:10.1080/00018739500101566</a>, [arXiv:cond-mat/9506066](https://arxiv.org/abs/cond-mat/9506066)\]
  > (relating to [[effective field theory|effective]] [[abelian Chern-Simons theory]] for [[FQH systems]])

The additional requirement that the Berry connection be non-abelian (and/or the presence of anyons):

* {#GuWen09} [[Zheng-Cheng Gu]], [[Xiao-Gang Wen]], p. 2 of:  *Tensor-Entanglement-Filtering Renormalization Approach and Symmetry Protected Topological Order*, Phys. Rev. B **80** 155131 (2009) $[$[arXiv:0903.1069](https://arxiv.org/abs/0903.1069), [doi:10.1103/PhysRevB.80.155131](https://doi.org/10.1103/PhysRevB.80.155131)$]$

Suggestion that [[topological order]] goes along with [[long-range entanglement]]:

* {#ChenGuWen2010} [[Xie Chen]], [[Zheng-Cheng Gu]], [[Xiao-Gang Wen]], Section V of: _Local unitary transformation, long-range quantum entanglement, wave function renormalization, and topological order_ Phys. Rev. B **82** 155138 (2010) $[$[arXiv:1004.3835](http://arxiv.org/abs/1004.3835), [doi:10.1103/PhysRevB.82.155138](https://doi.org/10.1103/PhysRevB.82.155138)$]$ 


### Review


* {#Wen91Review} [[Xiao-Gang Wen]], *Topological orders and Chern-Simons theory in strongly correlated quantum liquid*,  International Journal of Modern Physics B **05** 10 (1991)  1641-1648 $[$[doi:10.1142/S0217979291001541](https://doi.org/10.1142/S0217979291001541)$]$

* [[Jason Alicea]], [[Matthew Fisher]], [[Marcel Franz]], [[Yong-Baek Kim]],  *Strongly Interacting Topological Phases*, report on Banff workshop [15w5051](http://www.birs.ca/events/2015/5-day-workshops/15w5051) (2015) &lbrack;[pdf](https://www.birs.ca/workshops/2015/15w5051/report15w5051.pdf), [[AliceaEtAl-InteractingTopPhases.pdf:file]]&rbrack;

* [[Xiao-Gang Wen]], *Zoo of quantum-topological phases of matter*, Rev. Mod. Phys. **89** 41004 (2017) &lbrack;[arXiv:1610.03911](https://arxiv.org/abs/1610.03911), [doi:10.1103/RevModPhys.89.041004](https://doi.org/10.1103/RevModPhys.89.041004)&rbrack;


Textbook accounts:

* {#ZCZW19} [[Bei Zeng]], [[Xie Chen]], [[Duan-Lu Zhou]], [[Xiao-Gang Wen]]: 

  *Topological Order and Long-Range Entanglement*, Part III of: *[[Quantum Information Meets Quantum Matter]] -- From Quantum Entanglement to Topological Phases of Many-Body Systems*, Quantum Science and Technology (QST), Springer (2019) $[$[arXiv:1508.02595](https://arxiv.org/abs/1508.02595), [doi:10.1007/978-1-4939-9084-9](https://doi.org/10.1007/978-1-4939-9084-9)$]$

* [[Tudor D. Stanescu]], Section 6.2 of: *Introduction to Topological Quantum Matter & Quantum Computation*, CRC Press (2020) &lbrack;[ISBN:9780367574116](https://www.routledge.com/Introduction-to-Topological-Quantum-Matter--Quantum-Computation/Stanescu/p/book/9781032126524)&rbrack;

* Masaki Oshikawa, Yong Baek Kim, Kirill Shtengel, [[Chetan Nayak]], Sumanta Tewari, *Topological degeneracy of non-Abelian states for dummies*, Annals of Physics **322** 6 (2007) 1477-1498 &lbrack;[doi:10.1016/j.aop.2006.08.001](https://doi.org/10.1016/j.aop.2006.08.001), [arXiv:cond-mat/0607743](https://arxiv.org/abs/cond-mat/0607743)&rbrack;


Further review:

* [[Chetan Nayak]], [[Steven H. Simon]], [[Ady Stern]], [[Michael Freedman|M. Freedman]], [[Sankar Das Sarma]], _Non-Abelian anyons and topological quantum computation_, Rev Mod Phys __80__:3 (Aug 2008) 1083&#8211;1159 [MR2009g:81041](http://www.ams.org/mathscinet-getitem?mr=2443722) [doi](http://dx.doi.org/10.1103/RevModPhys.80.1083)

* [[Xiao-Gang Wen]], _An introduction of topological order_ (2009) &lbrack;[pdf slides](http://dao.mit.edu/~wen/talks/09QHtop.pd), [article](http://dao.mit.edu/~wen/topartS3.pdf)&rbrack;

* [[Philip Ball]], *Making the world from topological order*, National Science Review **6** 2 (2019) 227–230 &lbrack;[doi:10.1093/nsr/nwy116](https://doi.org/10.1093/nsr/nwy116)&rbrack;
  > (an interview with [[Xiao-Gang Wen]])

* V. Yu. Irkhin, Yu. N. Skryabin, *Topological states in strongly correlated systems*, Journal of Superconductivity and Novel Magnetism, **35** 8 (2022) 2141-2151 &lbrack;[arXiv:2209.04336](https://arxiv.org/abs/2209.04336), [doi:10.1007/s10948-022-06251-3](https://doi.org/10.1007/s10948-022-06251-3)&rbrack;


See also:

* Wikipedia: [topological order](http://en.wikipedia.org/wiki/Topological_order)

### Early discovery articles

* [[Xiao-Gang Wen]]: *Vacuum Degeneracy of Chiral Spin State in Compactified Spaces*, Phys. Rev. B **40** 7387 (1989) \[<a href="https://doi.org/10.1103/PhysRevB.40.7387">doi:10.1103/PhysRevB.40.7387</a>\]

* [[Xiao-Gang Wen]]: *Topological Orders in Rigid States*, Int. J. Mod. Phys. B **4** 239 (1990) \[<a href="https://doi.org/10.1142/S0217979290000139">doi:10.1142/S0217979290000139</a>, [pdf](https://xgwen.mit.edu/sites/default/files/documents/topo.pdf)\]

* [[Xiao-Gang Wen]], Qian Niu:  *Ground state degeneracy of the FQH states in presence of random potential and on high genus Riemann surfaces*, Phys. Rev. B **41** 9377 (1990) \[<a href="https://doi.org/10.1103/PhysRevB.41.9377">doi:10.1103/PhysRevB.41.9377</a>\]

* E. Keski-Vakkuri, [[Xiao-Gang Wen]]: *Ground state structure of hierarchical QH states on torus and modular transformation*,
Int. J. Mod. Phys. B **7** 4227 (1993) \[<a href="https://doi.org/10.1142/S0217979293003644">doi:10.1142/S0217979293003644</a>, [arXiv:hep-th/9303155](https://arxiv.org/abs/hep-th/9303155)\]


### Examples of topologically ordered materials

Definite examples of topologically ordered materials remain somewhat elusive, but a few candidates have been discussed.

> &lbrack;[Manning-Coe & Bradlyn 2023](#Manning-CoeBradlyn23):&rbrack; outside of the [[fractional quantum Hall effect]], the connection between the microscopic Hamiltonian for interacting electrons and the topological order of the ground state remains elusive.

* {#Manning-CoeBradlyn23} Dmitry Manning-Coe, Barry Bradlyn, *Ground state stability, symmetry, and degeneracy in Mott insulators with long range interactions*, Phys. Rev. B **108** 165136 (2023) &lbrack;[arXiv:2306.00221](https://arxiv.org/abs/2306.00221), [doi:10.1103/PhysRevB.108.165136](https://doi.org/10.1103/PhysRevB.108.165136)&rbrack;


Argument that [[superconductors]] are actually topologically ordered phases:

* [[Thors Hans Hansson]], Vadim Oganesyan, S. L. Sondhi, *Superconductors are topologically ordered*, Annals Of Physics **313** 497 (2004) &lbrack;[arXiv:cond-mat/0404327](https://arxiv.org/abs/cond-mat/0404327), [doi:10.1016/j.aop.2004.05.006](https://doi.org/10.1016/j.aop.2004.05.006)&rbrack;



On [[topological semimetals]] with degenerate ground states:

* Huaiming Guo, Yongfei Jia, *Interaction-driven phases in a Dirac Semimetal: Exact Diagonalization Results*, J. Phys.: Condens. Matter **26** 475601 (2014) &lbrack;[arXiv:1402.4274](https://arxiv.org/abs/1402.4274), [doi:10.1088/0953-8984/26/47/475601](https://doi.org/10.1088/0953-8984/26/47/475601)&rbrack;

On [[topological semimetals]] which gap to topologically ordered phases:

* Chong Wang, Lei Gioia, [[Anton A. Burkov]], *Fractional Quantum Hall Effect in Weyl Semimetals*, Phys. Rev. Lett. **124** 096603 (2020) &lbrack;[doi:10.1103/PhysRevLett.124.096603](https://doi.org/10.1103/PhysRevLett.124.096603)&rbrack;

* Manisha Thakurathi, [[Anton A. Burkov]], *Theory of the fractional quantum Hall effect in Weyl semimetals*, Phys. Rev. B **101** 235168 (2020) &lbrack;[doi:10.1103/PhysRevB.101.235168](https://doi.org/10.1103/PhysRevB.101.235168), [arXiv:2005.13545](https://arxiv.org/abs/2005.13545)&rbrack;

  > "while we focused on fully gapped states \[...\] it also makes sense to consider gapless strongly correlated states with the same property. Such states may be accessed easily within the formalism, presented above

* Dan Sehayek, Manisha Thakurathi, [[Anton A. Burkov]], *Charge density waves in Weyl semimetals*, Phys. Rev. B **102** 115159 (2020) &lbrack;[doi:10.1103/PhysRevB.102.115159](https://doi.org/10.1103/PhysRevB.102.115159)&rbrack;

* Jinmin Yi, Xuzhe Ying, Lei Gioia, [[Anton A. Burkov]], *Topological order in interacting semimetals*, Phys. Rev. B **107** 115147 (2023) &lbrack;[arXi:2301.03628](https://arxiv.org/abs/2301.03628), [doi:10.1103/PhysRevB.107.115147](https://doi.org/10.1103/PhysRevB.107.115147)&rbrack;

* Hongshuang Liu, Jiashuo Liang, Taiyu Sun, Liying Wang: *Recent progress in topological semimetal and its realization in Heusler compounds*, Materials Today Physics
**41** (2024) 101343 &lbrack;[doi:10.1016/j.mtphys.2024.101343](https://doi.org/10.1016/j.mtphys.2024.101343)&rbrack;





### Other articles

On detection of [[topological order]] by observing [[modular transformations]] on the [[ground state]]:

* [[Zhuan Li]], [[Roger S. K. Mong]], *Detecting topological order from modular transformations of ground states on the torus*, Phys. Rev. B **106** (2022) 235115 &lbrack;[doi:10.1103/PhysRevB.106.235115](https://doi.org/10.1103/PhysRevB.106.235115), [arXiv:2203.04329](https://arxiv.org/abs/2203.04329)&rbrack;

On [[thermodynamics|thermodynamic]] stability of topological order:

* {#NussinovOrtiz08} [[Zohar Nussinov]], [[Gerardo Ortiz]]: *Autocorrelations and Thermal Fragility of Anyonic Loops in Topologically Quantum Ordered Systems*, Phys. Rev. B **77** x (2008) Phys. Rev. B 77, 064302 \[<a href="https://doi.org/10.1103/PhysRevB.77.064302">doi:10.1103/PhysRevB.77.064302</a>, [arXiv:0709.2717](https://arxiv.org/abs/0709.2717), [arXiv:0709.2717](https://arxiv.org/abs/0709.2717)\]

* [[Zohar Nussinov]], [[Gerardo Ortiz]]: *Symmetry and Topological Order*, Proceedings of the National Academy of Sciences **106** 40 (2009) 16944-16949 \[<a href="https://doi.org/10.1073/pnas.0803726105">doi:10.1073/pnas.0803726105</a>, [arXiv:cond-mat/0605316](https://arxiv.org/abs/cond-mat/0605316)\]

* [[Zohar Nussinov]], [[Gerardo Ortiz]]: *A symmetry principle for Topological Quantum Order*, Annals of Physics **324** 5 (2009) 977-1057 \[<a href="https://doi.org/10.1016/j.aop.2008.11.002">doi:10.1016/j.aop.2008.11.002</a>, [arXiv:cond-mat/0702377](https://arxiv.org/abs/cond-mat/0702377)\]

* [[Zohar Nussinov]], [[Gerardo Ortiz]]: *Sufficient symmetry conditions for Topological Quantum Order*, PNAS **106** 40 (2009) 16944-16949 \[<a href="https://doi.org/10.1073/pnas.080372610">doi:10.1073/pnas.080372610</a>\]


See also:

* [[Davide Gaiotto]], [[Anton Kapustin]], _Spin TQFTs and fermionic phases of matter_, [arxiv/1505.05856](http://arxiv.org/abs/1505.05856)

* [[Nicholas Read]], [[Subir Sachdev]], _Large-$N$ expansion for frustrated quantum antiferromagnets_, Phys. Rev. Lett. 66 1773 (1991) (on $Z_2$ topological order)

* [[Xiao-Gang Wen]], _Mean Field Theory of Spin Liquid States with Finite Energy Gap and Topological orders_, Phys. Rev. B 44 2664 (1991). (on $Z_2$ topological order)

* [[Xiao-Gang Wen]], [Non-Abelian Statistics in the FQH states](http://dao.mit.edu/~wen/pub/nab.pdf)
Phys. Rev. Lett. 66, 802 (1991).

* Moore, Gregory; Read, Nicholas. _Nonabelions in the fractional quantum hall effect_  Nuclear Physics B 360 (2&#8211;3): 362 (1991).

* [[Xiao-Gang Wen]] and Yong-Shi Wu, [_Chiral operator product algebra hidden in certain FQH states_](http://dao.mit.edu/~wen/pub/nabdw.pdf)
Nucl. Phys. B419, 455 (1994).

* [[Alexei Kitaev]], _Fault-tolerant quantum computation by anyons_, Annals of Physics __303__:1, January 2003; _Anyons in an exactly solved model and beyond_, Annals of Physics __321__:1, January 2006

* [[Michael Levin]], [[Xiao-Gang Wen]], _String-net condensation: A physical mechanism for topological phases_, Phys. Rev. B, 71, 045110 (2005).

* A. Kitaev, C. Laumann, _Topological phases and quantum computation_, [arXiv/0904.2771](http://arxiv.org/abs/0904.2771)

* Alexei Kitaev, John Preskill, _Topological entanglement entropy_, Phys. Rev. Lett. __96__, 110404 (2006)
* Levin M. and Wen X-G., _Detecting topological order in a ground state wave function_, Phys. Rev. Letts.,96(11), 110405, (2006)


* Jan Carl Budich, Bj&#246;rn Trauzettel, _From the adiabatic theorem of quantum mechanics to topological states of matter_, physica status solidi (RRL) 7, 109 (2013) [arXiv:1210.6672](http://arxiv.org/abs/1210.6672)

* {#WilczekZee1984} [[Frank Wilczek]],  [[Anthony Zee]], *Appearance of gauge structure in simple dynamical systems*, Physical Review Letters **52** 24 (1984) 2111 $[$[doi:10.1103/PhysRevLett.52.2111](https://doi.org/10.1103/PhysRevLett.52.2111)$]$


* {#JamadagniWeimer20} Amit Jamadagni, Hendrik Weimer, _An Operational Definition of Topological Order_ ([arXiv:2005.06501](https://arxiv.org/abs/2005.06501))

* Nathanan Tantivasadakarn, Ashvin Vishwanath, Ruben Verresen, *A hierarchy of topological order from finite-depth unitaries, measurement and feedforward* &lbrack;[arXiv:2209.06202](https://arxiv.org/abs/2209.06202)&rbrack;



Discussion in "reciprocal momentum space" via [[twisted equivariant K-theory]]:

* {#SatiSchreiber22} [[Hisham Sati]], [[Urs Schreiber]]: *[[schreiber:Anyonic topological order in TED K-theory]]*, Reviews in Mathematical Physics **35** 03 (2023) 2350001 \[<a href="https://doi.org/10.1142/S0129055X23500010">doi:10.1142/S0129055X23500010</a>, [arXiv:2206.13563](https://arxiv.org/abs/2206.13563)\]

Discussion of [[quantum measurement]] of topologically ordered states:

* Yabo Li, Mikhail Litvinov, Tzu-Chieh Wei, *Measuring Topological Field Theories: Lattice Models and Field-Theoretic Description* &lbrack;[arXiv:2310.17740](https://arxiv.org/abs/2310.17740)&rbrack;





[[!include topological entanglement entropy -- references]]





[[!include anyonic topological order via braided fusion categories -- references]]



[[!include anyonic topological order on tori -- references]]



### Further resources

**Research groups:**

* Univ. of Maryland, [joint quantum institute](http://jqi.umd.edu/research/topological-matter)

* [Topology and correlation in condensed matter](http://tccm.pks.mpg.de) (Germany)

* [Center for topological matter](https://sites.google.com/site/ctmsrc) (Korea)

* [Microsoft Research Station Q](http://research.microsoft.com/en-us/labs/stationq) (KITP, Santa Barbara)

**Conference and seminar cycles:**

* seminar in Koeln [Topological states of matter](http://www.thp.uni-koeln.de/trebst/Lectures/2012-TopoSeminar.html)

* Topological Phases of Matter: Simons Center, June 10-14, 2013, videos [available](http://scgp.stonybrook.edu/archives/3464)

* CECAM 2013, Topological Phases in Condensed Matter and Cold Atom Systems: towards quantum computations [description](http://www.cecam.org/workshop-867.html)




[[!redirects topological order]]
[[!redirects topological orders]]
