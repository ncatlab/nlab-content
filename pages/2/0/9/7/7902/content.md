
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--



\tableofcontents


## Idea

A _Wilson loop_ or _Wilson line_ is an [[observable]] in (both classical and quantum) [[gauge theory]] obtained from the [[holonomy]] of the [[gauge field|gauge]] [[connection on a bundle|connection]]. 

Hence if the gauge connection is given by a globally defined 1-form $A$, then the __Wilson loop__ along a closed [[loop]] $C$ is the trace of the [[Dyson formula|path-ordered exponential]]

$$
  W_C 
    \;=\; 
  Tr\Big(
    \mathcal{P}exp\big(
      \mathrm{i}
      \textstyle{\oint_C} A_\mu d x^\mu
    \big)
  \Big)
  \mathrlap{\,,}
$$

where $\mathcal{P}$ is the "path-ordering operator" and $A_\mu$ are the components of the connection. 


## Examples

### In Chern-Simons theory

In $SU(2)$-[[Chern-Simons theory]] the Wilson line observables compute the [[Jones polynomial]] of the given curve. See there for more details.

### In Rozansky-Witten theory

+-- {: .num_prop #RozanskyWittenWilsonLoopOfUnknotIsSquareRootOfAHat}
###### Proposition
**([[Rozansky-Witten Wilson loop of unknot is A-hat genus|Rozansky-Witten Wilson loop of unknot is square root of A-hat genus]])**

For $\mathcal{M}^{4n}$ a [[hyperkähler manifold]] (or just a [[holomorphic symplectic manifold]]) the [[Rozansky-Witten invariant]] [[Wilson loop observable]] associated with the [[unknot]] in the [[3-sphere]] is the [[square root]] $\sqrt{{\widehat A}(\mathcal{M}^{4n})}$ of the [[A-hat genus]] of $\mathcal{M}^{4n}$.

=--

This is [Roberts-Willerton 10, Lemma 8.6](Rozansky-Witten+Wilson+loop+of+unknot+is+A-hat+genus#RobertsWillerton10), using the [[Wheels theorem]] and the [[Hitchin-Sawon theorem]].


## Properties

### Relation to 1d Chern-Simons theory

For $G$ a suitable [[Lie group]] (compact, semi-simple and simply connected) the Wilson loops of $G$-[[principal connections]] are equivalently the [[partition functions]] of a [[1-dimensional Chern-Simons theory]].

This appears famously in the formulation of [[Chern-Simons theory]] [with Wilson lines](Chern-Simons+theory#WithWilsonLineObservables). More detailes are at _[[orbit method]]_.

### As the universal Vassiliev invariant

The un-traced [[Wilson loop observable]] of [[perturbative quantization of 3d Chern-Simons theory|perturbative Chern-Simons theory]] is the [[universal Vassiliev invariant]] (see there for more):

<center>
<img src="https://ncatlab.org/nlab/files/UniversalWilsonLoopObservable.jpg" width="700">
</center>


<center>
<img src="https://ncatlab.org/nlab/files/TheGrandStoryOfVassilievKnotInvariants.jpg" width="800">
</center>


> from [[schreiber:Differential Cohomotopy implies intersecting brane observables|Sati-Schreiber 19c]]


### Relation to defects

Wilson loop insertions may be thought of or at least related to _defects_ in the sense of  _[[QFT with defects]]_.

### Duality with 't Hooft operators under S-duality and geometric Langlands

[[S-duality]] of 4d [[super Yang-Mills theory]] may exchange Wilson loop operators with [['t Hooft operators]], in an incarnation of the [[geometric Langlands correspondence]] ([Kapustin-Witten 06](#KapustinWitten06))

[[!include geometric Langlands QFT -- table]]





## Related entries

* [[flux tube]]

* [[Polyakov gauge-string duality]]

* [['t Hooft operator]]

* [[Wilson surface]]



## References

### General

* [[Kenneth Wilson]], _Confinement of quarks_, Physical Review __D 10__ (8): 2445. [doi](http://dx.doi.org/10.1103/PhysRevD.10.2445) (1974)

* [[Yuri Makeenko]], *Methods of contemporary gauge theory*, Cambridge Monographs on Math. Physics, Cambridge University Press (2002) &lbrack;[doi:10.1017/CBO9780511535147]( https://doi.org/10.1017/CBO9780511535147), [gBooks](http://books.google.com/books?id=9W-W2w75ulAC)&rbrack;

* Wikipedia: *[Wilson loop](http://en.wikipedia.org/wiki/Wilson_loop)*

* R. Giles, _Reconstruction of gauge potentials from Wilson loops_, Physical Review __D 24__ (8): 2160, [doi](http://dx.doi.org/10.1103/PhysRevD.24.2160)

* A. Andrasi, J. C. Taylor, _Renormalization of Wilson operators in Minkowski space_, Nucl. Phys. B516 (1998) 417, [hep-th/9601122](http://arxiv.org/abs/hep-th/9601122)

* Amit Sever, Pedro Vieira, Luis F. Alday, Juan Maldacena, [[Davide Gaiotto]], _An Operator product expansion for polygonal null Wilson loops_ &lbrack;[arxiv.org/abs/1006.2788](http://arxiv.org/abs/1006.2788)&rbrack;

On [[quantum measurement]] of Wilson loops: 

* [[David Beckman]], [[Daniel Gottesman]], [[Alexei Kitaev]], [[John Preskill]]: *Measurability of Wilson loop operators*, Phys. Rev. D **65** (2002) 065022 &lbrack;[arXiv:hep-th/0110205](https://arxiv.org/abs/hep-th/0110205), [doi:10.1103/PhysRevD.65.065022](https://doi.org/10.1103/PhysRevD.65.065022)&rbrack;


On super-[[Wilson lines]] via [[integration over supermanifolds]]:

* [[C. A. Cremonini]], [[Pietro Grassi]], S. Penati: _Supersymmetric Wilson Loops via Integral Forms_ ([arXiv:2003.01729](https://arxiv.org/abs/2003.01729))

### In Chern-Simons theory
 {#ReferencesInChernSimonsTheory}

> See also at *[[perturbative quantization of 3d Chern-Simons theory]]* and at *[[Vassiliev knot invariants]]*.

The [[Poisson bracket]] of Wilson line observables in [[3d Chern-Simons theory]] was obtained in:

* W. M. Goldman: _Invariant functions on Lie groups and Hamiltonian flow of surface group representations_, Inventiones Math. **85** (1986) 263-302 &lbrack;[doi:10.1007/BF01389091](https://doi.org/10.1007/BF01389091)&rbrack;

For more see:

* {#GelcaUribe10b} [[Razvan Gelca]], [[Alejandro Uribe]], section 4 of: _Quantum mechanics and non-abelian theta functions for the gauge group $SU(2)$_, Fundamenta Mathematicae **228** (2015) 97-137  &lbrack;[arXiv:1007.2010](http://arxiv.org/abs/1007.2010), [doi:10.4064/fm228-2-1](https://www.impan.pl/en/publishing-house/journals-and-series/fundamenta-mathematicae/all/228/2/88942/quantum-mechanics-and-nonabelian-theta-functions-for-the-gauge-group-rm-su-2)&rbrack;

Discussion of Wilson loop observables in [[abelian Chern-Simons theory]] via [[path integral]] arguments followed by [[renormalization]] (such as via [[framed link|framing]]):

* {#Polyakov88} [[Alexander Polyakov]]: *Fermi-Bose Transmutations induced by Gauge Fields*, Modern Physics Letters A **3** 3 (1988) 325-328 &lbrack;[doi:10.1142/S0217732388000398](https://doi.org/10.1142/S0217732388000398), [[Polyakov-MPA-1988.pdf:file]]&rbrack;

* {#Witten89} [[Edward Witten]], §2.1 in: *Quantum Field Theory and the Jones Polynomial*, Commun. Math. Phys. **121** 3 (1989) 351-399 &lbrack;[doi:10.1007/BF01217730](https://doi.org/10.1007/BF01217730), [euclid:cmp/1104178138](http://projecteuclid.org/euclid.cmp/1104178138), MR0990772 &rbrack;

* {#CosteMakowka90} Antoine Coste, Michel Makowka: *Abelian Chern-Simons theories on $S^3$*, Nuclear Physics B **342** 3 (1990) 721-736 \[<a href="https://doi.org/10.1016/0550-3213(90)90334-A">doi:10.1016/0550-3213(90)90334-A</a>\]

* {#GMR94} G. Giavarini, C. P. Martin, [[Fernando Ruiz Ruiz]]: *Abelian Chern-Simons theory as the strong large-mass limit of topologically massive abelian gauge theory: the Wilson loop*, Nuclear Physics B **412** (1994) 731-750 &lbrack;[arXiv:hep-th/9309049](https://arxiv.org/abs/hep-th/9309049), <a href="https://doi.org/10.1016/0550-3213(94)90397-2">doi:10.1016/0550-3213(94)90397-2</a>&rbrack;

* {#LeukertSchäfer96} Peter Leukert, Jörg Schäfer, §7 in: *A rigorous construction of abelian Chern-Simons path integrals using white noise analysis*,  Reviews in Mathematical Physics **08** 03  (1996) 445-456 &lbrack;[doi:10.1142/S0129055X96000147](https://doi.org/10.1142/S0129055X96000147)&rbrack;


* {#GuadagniniThuillier08} [[Enore Guadagnini]], [[Frank Thuillier]]: *Deligne-Beilinson cohomology and abelian links invariants*, SIGMA **4** (2008) 078 &lbrack;[arXiv:0801.1445](https://arxiv.org/abs/0801.1445), [doi:10.3842/SIGMA.2008.078](https://doi.org/10.3842/SIGMA.2008.078)&rbrack;

Review:

* {#Kaul99} [[Romesh K. Kaul]], section 3 of: *Topological Quantum Field Theories -- A Meeting Ground for Physicists and Mathematicians* &lbrack;[arXiv:hep-th/9907119](https://arxiv.org/abs/hep-th/9907119)&rbrack;

Discussion generalizing to the case of [[nonabelian group|nonabelian]] [[gauge groups]]:

* [[Atle Hahn]], section 9 of: *Chern–Simons theory on $\mathbb{R}^3$ in axial gauge: a rigorous approach*, Journal of Functional Analysis **211** 2 (2004) 483-507 &lbrack;[doi:10.1016/j.jfa.2004.01.006](https://doi.org/10.1016/j.jfa.2004.01.006)&rbrack;

* [[Atle Hahn]]: *The Wilson Loop Observables of Chern-Simons Theory on $\mathbb{R}^3$ in Axial Gauge*,  Commun. Math. Phys. **248** (2004) 467–499 &lbrack;[doi:10.1007/s00220-004-1097-4](https://doi.org/10.1007/s00220-004-1097-4), [inSpire:667450](https://inspirehep.net/literature/667450)&rbrack;

* [[Atle Hahn]]: *Chern–Simons models on $S^2 \times S^1$, torus gauge fixing, and link invariants I*, Journal of Geometry and Physics **53** 3 (2005) 275-314 &lbrack;[doi:10.1016/j.geomphys.2004.07.001](https://doi.org/10.1016/j.geomphys.2004.07.001)&rbrack;

* [[Atle Hahn]]: *Chern–Simons models on $S^2 \times S^1$, torus gauge fixing, and link invariants II*, Journal of Geometry and Physics **58** 9 (2008) 1124-1136 &lbrack;[doi:10.1016/j.geomphys.2008.03.013](https://doi.org/10.1016/j.geomphys.2008.03.013)&rbrack;

* [[Atle Hahn]]: *The non-Abelian Chern-Simons path integral on     in the torus gauge: a review* &lbrack;[arXiv:1805.00248](https://arxiv.org/abs/1805.00248)&rbrack;

Relation between [[Dehn surgery]] and [[Wilson loop observables]] in [[Chern-Simons theory]]:

* [[Enore Guadagnini]]: _Surgery rules in quantum Chern-Simons field theory_, Nuclear Physics B **375** 2 (1992) 381-398 &lbrack;<a href="https://doi.org/10.1016/0550-3213(92)90037-C">doi:10.1016/0550-3213(92)90037-C</a>&rbrack;

* Boguslaw Broda, _Chern-Simons theory on an arbitrary manifold via surgery_ ([arXiv:hep-th/9305051](https://arxiv.org/abs/hep-th/9305051))

In the context of [[Chern-Simons theory as a topological string theory]]:

* [[Hirosi Ooguri]], [[Cumrun Vafa]], _Knot Invariants and Topological Strings_, Nucl. Phys. B 577:419-438, 2000 ([arXiv:hep-th/9912123](https://arxiv.org/abs/hep-th/9912123))


[[!include Jones polynomial as Wilson loop observable -- references]]


[[!include Chern-Simons Wilson lines in AdS3-CFT2 -- references]]

### In QFT with defects

Relation to [[QFT with defects]] is discussed in

slide 17 of 

* [[Constantin Bachas]], _Conformal defects in/and String theory_ ([pdf](http://www.ggi.fi.infn.it/talks/talk106.pdf))

slide 5 of 

* [[Constantin Bachas]], _Conformal defects in gauged WZW models_ ([pdf](http://hep.physics.uoc.gr/conf09/TALKS/Bachas.pdf))



### As partition functions of 1d Chern-Simons theory

Expression of Wilson loops as [[partition functions]] of [[1-dimensional Chern-Simons theories]]  by the [[orbit method]] (as used notably in [[Chern-Simons theory]]) is in section 4 of 

* [[Chris Beasley]], _Localization for Wilson Loops in Chern-Simons Theory_, in J. Andersen, H. Boden, A. Hahn, and B. Himpel (eds.) _Chern-Simons Gauge Theory: 20 Years After_, AMS/IP Studies in Adv. Math., Vol. 50, AMS, Providence, RI, 2011. ([arXiv:0911.2687](http://arxiv.org/abs/0911.2687))

referring to 

* S. Elitzur, [[Greg Moore]], A. Schwimmer, [[Nathan Seiberg]], _Remarks on the Canonical Quantization of the Chern-Simons-Witten Theory_, Nucl. Phys. B 326 (1989) 108&#8211;134.

in the context of [[Chern-Simons theory]] and in more general gauge theory to

* [[A. P. Balachandran]], S. Borchardt, A. Stern: _Lagrangian And Hamiltonian Descriptions of Yang-Mills Particles_, Phys. Rev. D **17** (1978) 3247-3256 &lbrack;[doi:10.1103/PhysRevD.17.3247](https://doi.org/10.1103/PhysRevD.17.3247)&rbrack;

### In S-duality and relation to t Hoofts operators

* {#KapustinWitten06} [[Anton Kapustin]], [[Edward Witten]], _Electric-Magnetic Duality And The Geometric Langlands Program_, Communications in Number Theory and Physics Volume 1 (2007) Number 1 ([arXiv:hep-th/0604151](http://arxiv.org/abs/hep-th/0604151))

[[!redirects Wilson loop operator]]
[[!redirects Wilson loop operators]]




[[!redirects Wilson loop]]
[[!redirects Wilson loops]]
[[!redirects Wilson-loop]]
[[!redirects Wilson-loops]]

[[!redirects Wilson line]]
[[!redirects Wilson-line]]
[[!redirects Wilson lines]]
[[!redirects Wilson-lines]]

[[!redirects Wilson operator]]
[[!redirects Wilson operators]]

[[!redirects Wilson loop observable]]
[[!redirects Wilson loop observables]]

[[!redirects Wilson line observable]]
[[!redirects Wilson line observables]]
