

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
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--



# Contents
* table of contents
{: toc}

## Idea
 {#Idea}

In [[solid state physics]], by a *symmetry protected topological* (SPT, [Gu & Wen 09](#GuWen09), [PBTO 09](#PBTO09)) *[[phase of matter]]* one means a [[topological phase of matter]] which is in some sense $G$-*[[equivariance|equivariantly]]* non-trivial, in that it cannot be [[quantum adiabatic theorem|adiabatically]] deformed to a trivial phase *while respecting some* $G$-[[symmetry]].

Since, if one forgets (theoretically) the $G$-[[equivariance]], a $G$-equivariantly non-trivial SPT may be trivial as a plain [[topological phase of matter|topological phase]], one may regard the $G$-symmetry as "protecting" the SPT phase from decaying, whence the terminology "symmetry protected".

In other words:

1. distinct SPT phases with a given symmetry cannot be [[quantum adiabatic theorem|adiabatically]] deformed into each other, in particular not without going through a [[phase transition]], *if* the whole deformation preserves the symmetry;

1. but they may possibly be transformed into each other this way if the symmetry is [[broken symmetry|broken]] during the deformation.


There are the following special classes of symmetry groups $G$ to which this applies (as well as to any of their [[semidirect product group|semidirect]] combinations):

1. $G$ may be a **spatial** symmetry, namely a [[subgroup]] of the [[crystallographic group]] of the underlying [[crystal|crystalline]] material;

1. $G$ may be a **non-spatial** symmetry which acts not on the position but on the "internal degrees of freedom" of the substance (the [[electron]]'s [[quantum states]] that are propagating in the crystal lattice of [[atomic nuclei]]) and includes

   1. **CPT**-symmetries ([[charge]] reversal, parity reversal and [[time reversal symmetry]])

   1. **internal** or **on-site** symmetries, which transform "internal degrees of freedom" (of [[electrons]]), located over each atomic site in the crystal (for example [[spin]]-exchange symmetry turning an [[electron]]'s [[spin]] state $\vert \uparrow \rangle$ into $\vert \downarrow \rangle$).


\begin{remark}
**(terminology)**
\linebreak
Beware that some authors insist on using the specific term "SPT" only for items further down in this list. 

For instance the claim below that SPT's are "classified by [[group cohomology]]" applies only to the last item. The first two items, for the case of free fermion systems at least, are expected to have a classification in [[twisted equivariant K-theory|twisted equivariant]] [[topological K-theory]] (see at [[K-theory classification of topological phases of matter]]). The relation between these two cases/proposals seems not to have been discussed yet in any substance (but check a later version of this entry for more...)

Moreover, sometimes authors insist that the underlying plain topological phase of an "SPT" *must* be trivial. This makes good sense in view of the meaning of "protected" but can lead to clumsy verbiage when used generally.

Finally beware that some of the literature says "symmetry protected *topological order*", which however was later changed to "symmetry protected *trivial order*" --  which however does not seem to convey the key point much anymore.
\end{remark}

 
(...)

> Leftover:

Using the notion of [[quantum entanglement]], we can say that SPT states are short-range [[entanglement|entangled states]] with a symmetry.  
Using the notion of [[topological order]], we can say that SPT states are symmetric states with trivial [[topological order]].


## Examples

The first example of SPT order is the Haldane phase of spin-1 chain ([Haldane 83](#Haldane83)). It is a SPT phase protected by the $SO(3)$ spin [[rotation group]] symmetry. Another example of SPT order is the [[topological insulator]] of non-interacting fermions, a SPT phase protected by U(1) and time reversal symmetry.

## Properties

### Classification by group cohomology 

In [CGLW 11](#CGLW11) it is claimed (motivation is offered in [CLW 11, Sec. V](#CLW11))
that the bosonic SPT orders are described by [[group cohomology]]: **d+1D SPT states with on-site symmetry $G$ are labeled by the elements in group cohomology class $H^{d+1} [G, U(1)]$.** It was also claimed that the fermionic SPT orders are described by a kind of group super-cohomology theory. 

X.-G. Wen:

> So the group (super-)cohomology theory may allow us to classify all SPT orders even for interacting systems, which include interacting topological insulator/superconductor.


### In free fermion systems

Free fermion system can also have non-trivial SPT phases, such as [[topological insulator]]s and topological superconductors. Those free fermion SPT phases are classified by [[twisted equivariant K-theory|twisted equivariant]] [[topological K-theory]] (see at *[[K-theory classification of topological phases of matter]]*).

## Related concepts

* [[protection from quantum corrections]]





## References

Related entries: [[TQFT]], [[topological order]], [[group cohomology]], [[entanglement]]

#### Reviews

* [SPT order](http://en.wikipedia.org/wiki/Symmetry_protected_topological_order)

#### Classification for bosonic SPT phases

Discussion via [[higher dimensional WZW models]] and claim of classification via [[group cohomology]]:

* {#CLW11} Xie Chen, Zheng-Xin Liu, and [[Xiao-Gang Wen]], *Two-dimensional symmetry-protected topological orders and their protected gapless edge excitations*, Phys. Rev. B **84** (2011) 235141 $[$[doi:10.1103/PhysRevB.84.235141](https://doi.org/10.1103/PhysRevB.84.235141), [https://arxiv.org/abs/1106.4752](arXiv:1106.4752)$]$

* {#CGLW11} Xie Chen, [[Zheng-Cheng Gu]], Zheng-Xin Liu, [[Xiao-Gang Wen]], _Symmetry protected topological orders and the group cohomology of their symmetry group_, Phys. Rev. B **87** (2013) 155114  $[$[arXiv:1106.4772](http://arxiv.org/abs/1106.4772)$]$

* Xie Chen, [[Zheng-Cheng Gu]], Zheng-Xin Liu, [[Xiao-Gang Wen]], *Symmetry protected topological orders and the group cohomology of their symmetry group*,  Science **338** (2012) 1604-1606 ([arXiv:10.1103/PhysRevB.87.155114](https://doi.org/10.1103/PhysRevB.87.155114)) 


Classification for free fermion SPT phases:

* {#FreedMoore12} [[Daniel S. Freed]], [[Gregory Moore|Gregory W. Moore]], _Twisted equivariant matter_, Annales Henri Poincar&#233; December 2013, Volume 14, Issue 8, pp 1927&#8211;2023 [arxiv/1208.5055](http://arxiv.org/abs/1208.5055) (uses [[equivariant K-theory]])

* Alexei Kitaev, _Periodic table for topological insulators and superconductors_, Proc. L.D.Landau Memorial Conf. "Advances in Theor. Physics", June 22-26, 2008, Chernogolovka, Russia, [arxiv/0901.2686](http://arxiv.org/abs/0901.2686) (uses [[K-homology]], [[Bott periodicity]] etc.)


#### Early discovery articles

* {#GuWen09} [[Zheng-Cheng Gu]], [[Xiao-Gang Wen]], *Tensor-Entanglement-Filtering Renormalization Approach and Symmetry Protected Topological Order*, Phys. Rev. B **80** 155131 (2009) $[$[arXiv:0903.1069](https://arxiv.org/abs/0903.1069), [doi:10.1103/PhysRevB.80.155131](https://doi.org/10.1103/PhysRevB.80.155131)$]$


* {#PBTO09} Frank Pollmann, Erez Berg, Ari M. Turner, Masaki Oshikawa, *Symmetry protection of topological order in one-dimensional quantum spin systems*, Phys. Rev. B **85** 075125 (2012) $[$[arXiv:0909.4059](https://arxiv.org/abs/0909.4059), [doi:10.1103/PhysRevB.85.075125](https://doi.org/10.1103/PhysRevB.85.075125)$]$

* Xie Chen, Zheng-Xin Liu, [[Xiao-Gang Wen]], 2D symmetry protected topological orders and their protected gapless edge excitations Phys. Rev. B 84, 235141 (2011); 

* Zheng-Cheng Gu, [[Xiao-Gang Wen]], [Symmetry-protected topological orders for interacting fermions -- fermionic topological non-linear sigma-models and a group super-cohomology theory](http://arxiv.org/abs/1201.2648)

#### Examples

The 1d Haldane phase:

* {#Haldane83} [[Duncan Haldane]], *Continuum dynamics of the 1-D Heisenberg antiferromagnet: Identification with the $O(3)$ nonlinear sigma model*, Physics Letters A **93** 9 (1983) 464-468 $[$<a href="https://doi.org/10.1016/0375-9601(83)90631-X">doi:10.1016/0375-9601(83)90631-X</a> $]$

Examples with [[braid group]] effects:

* [[Michael Levin]], [[Zheng-Cheng Gu]], *Braiding statistics approach to symmetry-protected topological phases*, Phys. Rev. B **86** (2012) 115109 ([doi:10.1103/PhysRevB.86.115109](https://doi.org/10.1103/PhysRevB.86.115109))

and with [[loop braid group]]-effects:

* Chao-Ming Jian, Xiao-Liang Qi, *Layer Construction of 3D Topological States and String Braiding Statistics*, Phys. Rev. X **4** (2014) 041043 $[$[doi:10.1103/PhysRevX.4.041043](https://doi.org/10.1103/PhysRevX.4.041043)$]$

and with both:

* Zhen Bi, Yi-Zhuang You, Cenke Xu, *Anyon and loop braiding statistics in field theories with a topological $\Theta$ term*, Phys. Rev. B **90** (2014) 081110(R)  ([doi:10.1103/PhysRevB.90.081110](https://doi.org/10.1103/PhysRevB.90.081110))



#### Other articles

* [[Michael Levin]], Zheng-Cheng Gu, Braiding statistics approach to symmetry-protected topological phases, Phys. Rev. B 86, 115109 (2012), arXiv:1202.3120.

* Yuan-Ming Lu, Ashvin Vishwanath, Theory and classification of interacting 'integer' topological phases in two dimensions: A Chern-Simons approach, Phys. Rev. B 86, 125119 (2012), arXiv:1205.3156.

* [[Davide Gaiotto]], [[Theo Johnson-Freyd]], _Symmetry protected topological phases and generalized cohomology_ $[$[arxiv/1712.07950](https://arxiv.org/abs/1712.07950)$]$

* Yizhi You, Trithep Devakul, F. J. Burnell, Titus Neupert, *Higher order symmetry-protected topological states for interacting bosons and fermions*, Phys. Rev. B **98** (2018) 235102  ([arXiv:1807.09788v2](https://arxiv.org/abs/1807.09788), [doi:10.1103/PhysRevB.98.235102](https://doi.org/10.1103/PhysRevB.98.235102))


#### Conference and seminar cycles

* seminar in Koeln [Topological states of matter](http://www.thp.uni-koeln.de/trebst/Lectures/2012-TopoSeminar.html)

* Topological Phases of Matter: Simons Center, June 10-14, 2013, videos [available](http://scgp.stonybrook.edu/archives/3464)

* [[Alexei Kitaev]], _On the classification of short-range entangled states_, [video](http://scgp.stonybrook.edu/archives/7874)

[[!redirects symmetry protected topological phases]]

[[!redirects symmetry protected trivial order]]
[[!redirects symmetry protected trivial orders]]

[[!redirects symmetry-protected trivial order]]
[[!redirects symmetry-protected trivial orders]]

[[!redirects symmetry protected topological order]]
[[!redirects symmetry protected topological orders]]

[[!redirects symmetry-protected topological order]]
[[!redirects symmetry-protected topological orders]]

[[!redirects SPT phase]]
[[!redirects SPT phases]]

[[!redirects SPT]]
[[!redirects SPTs]]

[[!redirects SPT state]]
[[!redirects SPT states]]

[[!redirects SPT order]]
[[!redirects SPT orders]]

