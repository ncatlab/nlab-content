
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

# Contents
* table of contents
{: toc}

## Idea

A _Wilson loop_ or _Wilson line_ is an [[observable]] in (both classical and quantum) [[gauge theory]] obtained from the [[holonomy]] of the [[gauge field|gauge]] [[connection on a bundle|connection]]. 

Hence if the gauge connection is given by a globally defined 1-form $A$, then the __Wilson loop__ along a closed [[loop]] $C$ is the trace of the [[Dyson formula|path-ordered exponential]]

$$
  W_C = Tr(\mathcal{P}exp(i\oint_C A_\mu d x^\mu))
$$

where $\mathcal{P}$ is the "path-ordering operator" and $A_\mu$ are the components of the connection. 

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


## Related entries

* [[flux tube]]

* [[Polyakov gauge-string duality]]

* [['t Hooft operator]]

* [[Wilson surface]]

## References

### General

* [[Kenneth Wilson]], _Confinement of quarks_, Physical Review __D 10__ (8): 2445. [doi](http://dx.doi.org/10.1103/PhysRevD.10.2445) (1974)

* [[Yuri Makeenko]], *Methods of contemporary gauge theory*, Cambridge Monographs on Math. Physics, Cambridge University Press (2002) &lbrack;[doi:10.1017/CBO9780511535147]( https://doi.org/10.1017/CBO9780511535147), [gBooks](http://books.google.com/books?id=9W-W2w75ulAC)&rbrack;

* Wikipedia [Wilson loop](http://en.wikipedia.org/wiki/Wilson_loop)

* R. Giles, _Reconstruction of gauge potentials from Wilson loops_, Physical Review __D 24__ (8): 2160, [doi](http://dx.doi.org/10.1103/PhysRevD.24.2160)

* A. Andrasi, J. C. Taylor, _Renormalization of Wilson operators in Minkowski space_, Nucl. Phys. B516 (1998) 417, [hep-th/9601122](http://arxiv.org/abs/hep-th/9601122)

* Amit Sever, Pedro Vieira, Luis F. Alday, Juan Maldacena, [[Davide Gaiotto]], _An Operator product expansion for polygonal null Wilson loops_, [arxiv.org/abs/1006.2788](http://arxiv.org/abs/1006.2788)

On super-[[Wilson lines]] via [[integration over supermanifolds]]:

* C.A. Cremonini, [[Pietro Grassi]], S. Penati, _Supersymmetric Wilson Loops via Integral Forms_ ([arXiv:2003.01729](https://arxiv.org/abs/2003.01729))

### In Chern-Simons theory

See at [[perturbative quantization of 3d Chern-Simons theory]]/[[Vassiliev knot invariants]].

Relation between [[Dehn surgery]] and [[Wilson loop observables]] in [[Chern-Simons theory]]:

* E. Guadagnini, _Surgery rules in quantum Chern-Simons field theory_, Nuclear Physics B
Volume 375, Issue 2, 18 May 1992, Pages 381-398 (<a href="https://doi.org/10.1016/0550-3213(92)90037-C">doi:10.1016/0550-3213(92)90037-C</a>)

* Boguslaw Broda, _Chern-Simons theory on an arbitrary manifold via surgery_ ([arXiv:hep-th/9305051](https://arxiv.org/abs/hep-th/9305051))


The [[Poisson bracket]] of Wilson line observables in [[3d Chern-Simons theory]] was obtained in 

* W. Goldman, _Invariant functions on Lie groups and Hamiltonian flow of surface
group representations_, Inventiones Math., 85 (1986), 263&#8211;302.

For more see 

* {#GelcaUribe10b} [[Razvan Gelca]], [[Alejandro Uribe]], section 4 of _Quantum mechanics and non-abelian theta functions for the gauge group $SU(2)$_ ([arXiv:1007.2010](http://arxiv.org/abs/1007.2010))


In [[Chern-Simons theory as a topological string theory]]:

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

* A. P. Balachandran, S. Borchardt, and A. Stern, _Lagrangian And Hamiltonian Descriptions of Yang-Mills Particles_, Phys. Rev. D 17 (1978) 3247&#8211;3256

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
