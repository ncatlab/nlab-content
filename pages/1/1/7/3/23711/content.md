

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

In [[condensed matter physics]], a *semi-metal* is a [[crystal|crystalline]] material whose [[electronic band structure]] is such that there is a sizeable gap between the [[valence band]] and the [[conduction band]] (as for an [[insulator]]) *except* over a [[submanifold]] of "nodal loci" inside the [[Brillouin torus]] which is of [[positive number|positive]] [[codimension]] $\geq 2$. 

(This terminology, which was established in the early 2000s, is meant to follow the  older terminology *[[semiconductor]]*, which refers to the case where there is globally a gap between valence and conduction band, but just a small one. Notice that a global and large gap corresponds to an [[insulator]], while the absence of a gap, hence the broad overlap of valence and conductions band, corresponds to a [[metal]]. Therefore a semi-metal behaves like an [[insulator]] for the bulk of its excitation modes, like a [[semiconductor]] for excitations close to the nodal loci, and almost like a [[meta]] for excitations right at the nodal loci.)

If the gap closure happens over an isolated point, one speaks of a *nodal point* proper, or more specifically of a *Dirac point* or *Weyl point*, indicating the "degeneracy" (multiplicity) of the [[energy]] [[eigenstates]] at the point (2 for Weyl, 4 for Dirac). If the gap closes over a 1-dimensional manifold (a [[curve]] or a [[circle]]) one speaks of a *nodal line*. 

Due to the gap on (a [[neighbourhood retract]] of) the [[complement]] of the nodal points/lines inside the [[Brillouin torus]], the [[Berry connection]] is well-defined away from the nodal loci, and it tends to be [[flat connection|flat]] in suitable hyperplanes there. It's [[holonomy]] around [[codimension]]=2 nodal loci (ie. around nodal lines in 3d materials and nodal points in effectively 2d materials such as [[graphene]], see also at *[[defect brane]]*) -- known as a *[[Berry phase]]* -- is then a property of the nodal locus alone, and to be interpreted as a measure for the "topological protection" of the gap over the nodal loci (e.g. [FWDF 16, II.B](#FWDF16), [Vanderbilt 18, 5.5.2](#Vanderbilt18)): Under adiabatic deformations of the material that do not excite modes above the gap, these nodal points may move and merge or split, but their total topological charge cannot change.

Therefore semi-metals with such non-trivial Berry phases are examples of [[topological phases of matter]], and are sometimes called *topological semi-metals*, for emphasis. In fact, if the topological charges of the nodal loci in a semi-metal do happen to be trivial, then it is (in the deformation class of) a fully gapped [[insulator]] and may then be a *[[topological insulator]]* (if the [[twisted equivariant K-theory|twisted equivariant]] [[topological K-theory]] class of its [[valence bundle]] is non-trivial).

The archetypical and original example of a semi-metal is *[[graphene]]*, where the gap closes over two [[Dirac points]]. (Or almost: a tiny [[spin-orbit coupling]] in graphene actually produces a tiny gap even at the would-be Dirac points, which however tends to be too small to be visible in practice. But if one will or would analyze graphene with an accuracy that does resolve this tiny gap-opening, then graphene will or would appear as a [[topological insulator]] instead of a semi-metal.)

After the synthesis of graphene, which is an effectively 2-dimensional material (an atomic mono-layer) much attention has shifted to the synthesis and understanding of 3-dimensional semi-metals.

## References


General textbook account:

* {#Vanderbilt18} [[David Vanderbilt]],  Section 5 of: *Berry Phases in Electronic Structure Theory -- Electric Polarization, Orbital Magnetization and Topological Insulators*, Cambridge University Press (2018) ([doi:10.1017/9781316662205](https://doi.org/10.1017/9781316662205))

For references on *[[graphene]]* see also there.

Discussion focusing on 3-dimensional semi-metals:

* A. A. Burkov, M. D. Hook, Leon Balents,  *Topological nodal semimetals*, Phys. Rev. B **84** (2011) 235126 ([arXiv:1110.1089](https://arxiv.org/abs/1110.1089), [doi:10.1103/PhysRevB.84.235126](https://doi.org/10.1103/PhysRevB.84.235126))

* Bohm-Jung Yang, Naoto Nagaosa, *Classification of stable three-dimensional Dirac semimetals with nontrivial topology*, Nature Communications **5** (2014) 4898  ([doi:10.1038/ncomms5898](https://doi.org/10.1038/ncomms5898))

* {#FWDF16} Chen Fang, Hongming Weng, Xi Dai, Zhong Fang, *Topological nodal line semimetals*, Chinese Phys. B **25** (2016) 117106 ([arXiv:1609.05414](https://arxiv.org/abs/1609.05414), [doi:10.1088/1674-1056/25/11/117106](https://doi.org/10.1088/1674-1056/25/11/117106))

* Jiaheng Li, Zetao Zhang, Chong Wang, Huaqing Huang, Bing-Lin Gu, Wenhui Duan,  *Topological semimetals from the perspective of first-principles calculations*, 
Journal of Applied Physics 128, 191101 (2020) ([doi:10.1063/5.0025396]( https://doi.org/10.1063/5.0025396))

Thoughts towards a mathematical formulation:

* [[Varghese Mathai]], [[Guo Chuan Thiang]], *Global topology of Weyl semimetals and Fermi arcs*, J. Phys. A: Math. Theor. **50** (2017) 11LT01 ([arXiv:1607.02242](https://arxiv.org/abs/1607.02242),  [doi:10.1088/1751-8121/aa59b2](https://doi.org/10.1088/1751-8121/aa59b2))


[[!redirects semi-metals]]

[[!redirects semimetal]]
[[!redirects semimetals]]

