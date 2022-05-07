


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Solid state physics
+-- {: .hide}
[[!include solid state physics -- contents]]
=--
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The [[AdS-CFT correspondence]] applies _exactly_ only to a few highly symmetric [[quantum field theories]], notably to [[N=4 D=4 super Yang-Mills theory]]. However, it does not completely break away from these special points in field theory space, but applies in some approximation and/or with suitable modifications on the [[gravity]]-side of the correspondence.

For instance [[quantum chromodynamics]] (one sector of the [[standard model of particle physics]]) is crucially different from but still similar enough to [[N=4 D=4 super Yang-Mills theory]] that some of its [[observables]], in particular otherwise intractable [[non-perturbative effects]], have been argued to be usefully approximated by [[AdS-CFT]]-type dual [[gravity]]-observables, for instance the [[shear viscosity]] of the [[quark-gluon plasma]]. This is hence also called the _[[AdS/QCD correspondence]]_.

Similarly, as far as systems in [[condensed matter physics]] are described well by some [[effective field theory]], one may ask whether this, in turn, is usefully related to [[gravity]] on some [[anti de-Sitter spacetime]] and use this to study the solid state system, notably its [[non-perturbative effects]].

[[Andreas Karch]] writes [here](http://www.math.columbia.edu/~woit/wordpress/?p=9426#comment-226376):

> These anomalous transport coefficients have first been calculated in AdS/CFT. The relevant references are [8], [9] and [10] in the Son/Surowka paper. In the AdS/CFT calculations these particular transport coefficients only arise due to Chern-Simons terms, which are the bulk manifestation of the field theory anomalies. At that point it was obvious to many of us that there should be a purely field theory based calculation, only using anomalies, that can derive these terms. Son and Surowka knew about this. They were sitting next door to me when they started these calculations. Many of us tried to find these purely field theory based arguments and failed. Son and Surowka succeeded.

> If you ask anyone serious about applying AdS/CFT to strongly coupled field theories why they are doing this, they would (hopefully) give you an answer along the lines of "AdS/CFT provides us with toy models of strongly coupled dynamics. While the field theories that have classical AdS duals are rather special, we can still learn important qualitative insights and find new ways to think about strongly coupled field theories." Once AdS/CFT stumbles on a new phenomenon in these solvable toy models, we want to go back to see whether we can understand it without the crutch of having to rely on AdS/CFT. Any result that only applies in theories with holographic dual is somewhat limited in its applications. In this sense, anomalous transport is a poster child for what AdS/CFT can be used for: a new phenomenon that had been missed completely by people studying field theory gets uncovered by studying these toy models. Once we knew what to look for, a purely field theoretic argument was found that made the AdS/CFT derivation obsolete.

> This is applied AdS/CFT as it should be. Solvable examples exhibit new connections which then can be proven to be correct more generally and are not limited to the toy models that were used to uncover them.

Similarly [Hartnoll-Lucas-Sachdev 16, p. 8](#HartnollLucasSachdev16):

> Our main objective here
is to make clear that explicit examples of the duality are
known in various dimensions and that they are found by
using string theory as a bridge between quantum field
theory and gravity.

## Properties

### Description by tensor networks

Discussion of [[renormalization]] and [[entangled states]]  of [[non-perturbative effects]] in [[solid state physics]] proceeds via [[tensor networks]] ([Swingle 09](#Swingle09), [Swingle 13](#Swingle13)) and the resulting discovery of the relation to [[holographic entanglement entropy]].

In this context, a _[[tensor network]]_ is a _[[string diagram]] [[concept with an attitude|with an attitude]], in that it is (just) a [[string diagram]], but with 

1. the [[tensor product]] of all its external [[objects]] regarded as a [[space of states]] of a [[quantum system]];

1. the [[element]] in that [[tensor product]] defined by the string diagram regarded a a [[state]] ([[wave function]]) of that quantum system.

For instance, if $\mathfrak{g}$ is a [[metric Lie algebra]] (with [[string diagram]]-notation as shown [there](metric+Lie+algebra#Definition)), and with each [[tensor product]]-power of its [[dual vector space]] regarded as [[Hilbert space]], hence as a [[space of quantum states]], via the given [[inner product]] on $\mathfrak{g}$, then an example of a _tree tensor network state_ is the following:

<center>
<img src="https://ncatlab.org/nlab/files/TensorNetworkStateFromMetricLieAlgebra.jpg" width="300">
</center>

The [[quantum states]] arising this way are generically highly [[entangled state|entangled]]: roughly they are the more entangled the more [[vertices]] there are in the corresponding tensor network.

Tree tensor network states in the form of [[Bruhat-Tits trees]] play a special role in the [[AdS/CFT correspondence]], either as

1. a kind of [[lattice QFT]]-approximation to an actual [[boundary field theory|boundary]] [[CFT]] [[quantum state]], 

1. as the [[p-adic geometry|p-adic geometric]] incarnation of [[anti de Sitter spacetime]] in the [[p-adic AdS/CFT correspondence]],

1. as a reflection of actual [[crystal]]-site quantum states in [[AdS/CFT in solid state physics]]:

<center>
<img src="https://ncatlab.org/nlab/files/BruhatTitsTreeTensorNetworkStateFromMetricLie.jpg" width="300">
</center>

> graphics from [[schreiber:Differential Cohomotopy implies intersecting brane observables|Sati-Schreiber 19c]]

For [[Bruhat-Tits tree]] [[tensor network states]] one finds that the [[holographic entanglement entropy]] of the tensor subspace associated with an [[interval]] on the [[boundary]] becomes proportional, for large number of [[vertices]], to the [[hyperbolic space|hyperbolic]] bulk boundary [[length]] of the segment of the tree network that ends on this interval, according to the [[Ryu-Takayanagi formula]] ([PYHP 15, Theorem 2](#PYHP15)). For more on this see [below](#ForHolographicEntanglementEntropy).

## Related concepts

* [[strange metal]]

* [[superconductor]]

* [[Sachdev-Ye-Kitaev model]]

* [[quark-gluon plasma]]


## References

### General


Textbooks:

* [[Jan Zaanen]], Yan Liu, Ya-Wen Sun, [[Koenraad Schalm]], _Holographic Duality in Condensed Matter Physics_, Cambridge University Press 2015 ([doi:10.1017/CBO9781139942492]( https://doi.org/10.1017/CBO9781139942492))

* {#HartnollLucasSachdev16} [[Sean Hartnoll]], [[Andrew Lucas]], [[Subir Sachdev]], _Holographic quantum matter_, MIT Press 2018 ([arXiv:1612.07324](https://arxiv.org/abs/1612.07324), [publisher](https://mitpress.ublish.com/book/holographic-quantum-matter))



Reviews and lectures:

* [[Sean Hartnoll]], _Lectures on holographic methods for condensed matter physics_, Class. Quant. Grav. 26:224002, 2009 ([arXiv:0903.3246](https://arxiv.org/abs/0903.3246))

* [[John McGreevy]], *Holographic duality with a view toward many-body physics*, Adv. High Energy Phys. 723105 (2010) ([arXiv:0909.0518](https://arxiv.org/abs/0909.0518))

* A. Pires, _AdS/CFT correspondence in condensed matter_ ([arXiv:1006.5838](http://arxiv.org/abs/1006.5838))

* [[Subir Sachdev]], _Condensed matter and AdS/CFT_ ([arXiv:1002.2947](http://arxiv.org/abs/1002.2947))

* K. Schalm and R. Davison, _A simple introduction to AdS/CFT
and its application to condensed matter physics_,  D-ITP Advanced Topics in Theoretical Physics Fall 2013, ([[SchalmDavisonAdSCFT.pdf:file]])

* Andrea Amoretti, _Condensed Matter Applications of AdS/CFT: Focusing on strange metals_, 2017 ([spire:1610363](http://inspirehep.net/record/1610363), [[AmorettiStrangeMetals.pdf:file]])

* Hong Liu, Julian Sonner, _Quantum many-body physics from a gravitational lens_, Nature Rev.Phys. 2 (2020) 11, 615-633 ([arXiv:2004.06159](https://arxiv.org/abs/2004.06159), [doi:10.1038/s42254-020-0225-1](https://doi.org/10.1038/s42254-020-0225-1))


More pointers:

* [[Jan Zaanen]], _[Anti-de-Sitter/Condensed Matter Theory](https://www.lorentz.leidenuniv.nl/zaanen/wordpress/research/anti-de-sittercondensed-matter/)_



### Application to quantum chromodynamics

Discussion of [[quantum chromodynamics]] via [[AdS/CFT in condensed matter physics]] (see also at [[AdS/QCD]]):

* Yuri V. Kovchegov, _AdS/CFT applications to relativistic heavy ion collisions: a brief review_ ([arXiv:1112.5403](http://arxiv.org/abs/1112.5403))

* {#SantiagodeCompostela18} _[Holography and Extreme Chromodynamics](http://igfae.usc.es/~holoquark2018/)_, Santiago de Compostela, July 2018

### Application to superconductivity

Discussion of [[superconductivity]] via [[AdS/CFT in condensed matter physics]]:

* [[Sean Hartnoll]], [[Christopher Herzog]], [[Gary 
 Horowitz]], _Building an AdS/CFT superconductor_, Phys. Rev. Lett. 101:031601, 2008 ([arXiv:0803.3295](https://arxiv.org/abs/0803.3295))

* Alberto Salvio, _Superconductivity, Superfluidity and Holography_ ([arXiv:1301.0201](http://arxiv.org/abs/1301.0201))

* Rong-Gen Cai, Li Li, Li-Fang Li, Run-Qiu Yang, _Introduction to Holographic Superconductor Models_, Sci China-Phys Mech Astron, 2015, 58(6):060401 ([arXiv:1502.00437](https://arxiv.org/abs/1502.00437))

On [[strange metals]], high $T_c$-[[superconductors]] and [[AdS/CMT duality]]:

* [[Jan Zaanen]], _Planckian dissipation, minimal viscosity and the transport in cuprate strange metals_, SciPost Phys. 6, 061 (2019) ([arXiv:1807.10951](https://arxiv.org/abs/1807.10951))



### Application to quasicrystals

Discussion of [[asymptotic boundaries]] of [[hyperbolic space|hyperbolic]] [[tensor networks]] as conformal [[quasicrystals]]:

* Latham Boyle, Madeline Dickens, Felix Flicker, _Conformal Quasicrystals and Holography_, Phys. Rev. X 10, 011009 (2020) ([arXiv:1805.02665](https://arxiv.org/abs/1805.02665))

* Alexander Jahn, Zoltán Zimborás, Jens Eisert, _Central charges of aperiodic holographic tensor network models_ ([arXiv:1911.03485](https://arxiv.org/abs/1911.03485))

### Relation to $p$-adic AdS/CFT correspondence

Proposed realization of aspects of [[p-adic AdS/CFT correspondence]] in [[solid-state physics]]:

* Gregory Bentsen, Tomohiro Hashizume, Anton S. Buyskikh, Emily J. Davis, Andrew J. Daley, [[Steven Gubser]], Monika Schleier-Smith, _Treelike interactions and fast scrambling with cold atoms_, Phys. Rev. Lett. 123, 130601 (2019) ([arXiv:1905.11430](https://arxiv.org/abs/1905.11430))

[[!include topological phases of matter via K-theory -- references]]



[[!redirects AdS/CFT in condensed matter physics]]

[[!redirects AdS/CFT correspondence in codensed matter physics]]
[[!redirects AdS-CFT correspondence in codensed matter physics]]

[[!redirects AdS/CMT]]
[[!redirects AdS-CMT]]

[[!redirects AdS/CMT duality]]
[[!redirects AdS-CMT duality]]

[[!redirects AdS/CMT correspondence]]
[[!redirects AdS-CMT correspondence]]

[[!redirects AdS/CFT in solid state physics]]
[[!redirects AdS-CFT in solid state physics]]
[[!redirects AdS/CFT correspondence in solid state physics]]
[[!redirects AdS-CFT correspondence in solid state physics]]

[[!redirects AdS/CFT duality in solid state physics]]




