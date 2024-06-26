[[!redirects N=4 D=4 super Yang-Mills theory]]
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The [[super Yang-Mills theory]] in [[dimension]] 4 with the 
maximum number $N = 4$ of [[supersymmetries]].

[[!include superconformal symmetry -- table]]


## Properties of 4d SYM

### Conformal invariance

$N=4$ $D=4$ SYM is an [[SCFT]].

### Closed expressions for physical observables
 {#ClosedExpressionsForPhysicalObservables}

Among all [[gauge theory]] [[Lagrangians]] that of $N=4$, $D = 4$ SYM is special in several ways, in particular of course in that it is conformally invariant and in that it has maximal [[supersymmetry]]; and ultimately by the fact that it is the [[Kaluza-Klein mechanism|KK-reduction]] of the very special [[6d (2,0)-superconformal QFT]] and related by [[AdS-CFT|AdS7-CFT6 duality]] to the very special theory of [[11-dimensional supergravity]]/[[M-theory]].

Accordingly, it is to be expected that the [[quantum observables]] of $N=4$, $D = 4$ SYM satisfy special relations that make them more tractable than the observables of a generic [[gauge theory]], in particular by having closed-form expressions.
Indeed, such relations have been and are being uncovered in the last years, in particular in what is called the _[[planar limit]]_ of the theory, where [[scattering amplitudes]] are dominated by [[Feynman diagrams]] that can be given the structure of planar [[graphs]].

This includes notably the following phenomena:

1. The [[operator spectrum]] of the dilatation operator (the part of the [[stress-energy tensor]] which induces conformal transformations) can be expressed in closed form, indeed when regarded as a [[Hamiltonian]] it defines an [[integrable system]] equivalent to [[spin chain]] models. This has been used in particular to explicitly check aspects of the conjectured [[AdS-CFT duality]] of $N=4$, $D= 4$ SYM with [[type II string theory]] on [[anti de Sitter spacetimes]]. See the review ([Beisert et al](#Beisert)).

1. Certain [[scattering amplitudes]] called _maximally helicity violating amplitudes_ ("[[MHV amplitudes]]") simplify drastically as compared to the generic situation and in fact are controled by a certain [[twistor string theory]] whose [[target space]] is a [[twistor space]]. See ([Monteiro](#Monteiro)) for a review.

1. Generally, the [[scattering amplitudes]] of the theory in the planar limit have certain closed-form combinatorial expressions. See ([Arkani-Hamed et al](#Arkani-Hamed)).

Such "exact solutions" of the theory are of interest in that even though N=4, D=4 SYM is very different from [[phenomenology|phenomenologically viable]] models such that [[QCD]] in the [[standard model of particle physics]] in that it is highly (super-)symmetric and conformal, it is still similar enough (being a nonabelian [[gauge theory]] [[minimal coupling|minimally coupled]] to [[fermions]]) that one can or can hope to deduce from these exact results approximate information about these less symmetric theories. 

In other words, because understanding [[observables]] in [[QCD]]/[[Yang-Mills theory]] in general is difficult, going to special points in the space of all such theories -- such as the point of N=4, D=4 SYM -- may be hoped to yield a tractable approximation. For more on this way of studying [[QCD]] and other realistic theories by studying instead their highly symmetric but phenomenologically unrealistic siblings, see also at _[[string theory results applied elsewhere]]_.


### Holography, AdS-CFT

$N=4$ $d=4$ SYM is supposed to be related under the [[AdS/CFT correspondence]] to [[type II superstring theory]] [[Kaluza-Klein mechanism|compactified]] on a 5-[[sphere]] to an asymptotically [[anti de Sitter spacetime]].

[[!include gauge theory from AdS-CFT -- table]]


### Twistor space formulation

There is a natural reformulation of the theory using [[twistor]] [[field (physics)|fields]]. See the references [below](#ReferencesTwistorSpace). And see at _[[twistor string theory]]_.

### Topological twists

There is a topological twist of 4d SYM to a [[TQFT]] -- the [[Kapustin-Witten TQFT]]. Its [[S-duality]] is supposed to contain [[geometric Langlands duality]] as a special case.

See at _[[topologically twisted D=4 super Yang-Mills theory]]_.

## Related concepts

* [[D=4 Yang-Mills theory]]

* [[super Yang-Mills theory]]

  * [[N=1 D=4 super Yang-Mills theory]]

  * [[N=2 D=4 super Yang-Mills theory]]

  * [[N=4 D=3 super Yang-Mills theory]]

  * [[D=5 super Yang-Mills theory]]

  * [[topologically twisted D=4 super Yang-Mills theory]]


[[!include table of branes]]


## References

### General

* [[Riccardo D'Auria]], [[Pietro Fré]], A. J. da Silva, *Geometric structure of $N=1$, $D=10$ and $N=4$, $D=4$ super Yang-Mills theory*, Nuclear Physics B **196** 2 (1982) 205-239 &lbrack;<a href="https://doi.org/10.1016/0550-3213(82)90036-0">doi:10.1016/0550-3213(82)90036-0</a>&rbrack;

  > (in [[D'Auria-Fré formulation of supergravity|D'Auria-Fré formulation]])



Discussion of [[D=4 N=4 SYM]] with emphasis on [[multi-trace operators]]:

* P. J. Heslop, [[Paul Howe]], _Aspects of $\mathcal{N}$=4 SYM_, JHEP 0401 (2004) 058 ([arXiv:hep-th/0307210](https://arxiv.org/abs/hep-th/0307210))

[[superconformal group|Superconformal]] invariance of $\mathcal{N}=4$, $D=4$ SYM can be shown with the result of 

* Robert Leigh, [[Matthew Strassler]], _Exactly Marginal Operators and Duality in Four Dimensional $\mathcal{N}=1$ Supersymmetric Gauge Theory_ ([arXiv:hep-th/9503121](http://arxiv.org/abs/hep-th/9503121))

(after regarding it as $\mathcal{N}=1$ SYM with three adjoint chiral [[superfield]]s).


Introductions in view of [[single trace operators]] as [[spin chain]] [[integrable systems]] in the [[AdS/CFT correspondence]]:

* Joseph A. Minahan _Review of AdS/CFT Integrability, Chapter I.1: Spin Chains in $\mathcal{N}=4$ Super Yang-Mills_ ([arXiv:1012.3983](http://arxiv.org/abs/1012.3983))

More recent results are in 

* Simon Caron-Huot, _Superconformal symmetry and two-loop amplitudes in planar N=4 super Yang-Mills_ ([arXiv:1105.5606](http://arxiv.org/abs/1105.5606))

### Matrix model description


On the [[BMN matrix model]] as a [[KK-compactification]] of [[D=4 N=4 super Yang-Mills theory]] on the [[3-sphere]]:

* [[Nakwoo Kim]], [[Thomas Klose]], [[Jan Plefka]], _Plane-wave Matrix Theory from N=4 Super Yang-Mills on $\mathbb{R} \times S^3$_, Nucl. Phys. B671:359-382, 2003 ([arXiv:hep-th/0306054](https://arxiv.org/abs/hep-th/0306054))

Using the [[KK-compactification]] of [[D=4 N=4 super Yang-Mills theory]] to the [[BMN matrix model]] for [[lattice gauge theory]]-computations in [[D=4 N=4 SYM]] and for numerical checks of the [[AdS-CFT correspondence]]:

* Masazumi Honda, [[Goro Ishiki]], Sang-Woo Kim, Jun Nishimura, Asato Tsuchiya, _Direct test of the AdS/CFT correspondence by Monte Carlo studies of N=4 super Yang-Mills theory_, JHEP 1311 (2013) 200 &lbrack;[arXiv:1308.3525](https://arxiv.org/abs/1308.3525)&rbrack;


### Planar sector, integrability, MHV amplitudes

A comprehensive discussion of the [[integrability]] related to anomalous dimension in the planar sector is in 

* [[Niklas Beisert]] et al., _Review of AdS/CFT Integrability, An Overview_ 
Lett. Math. Phys. vv, pp (2011), ([arXiv:1012.3982](http://arxiv.org/abs/1012.3982)).
 {#Beisert}

A review of [[MHV amplitudes]] is in 

* Gustavo Machado Monteiro, _MHV Tree Amplitudes in Super-Yang-Mills and in Superstring Theory_ (2010) ([pdf](http://www.ift.unesp.br/posgrad/gustavo.pdf))
  {#Monteiro}

Discussion of special properties of [[scattering amplitudes]] in the planar sector is in

* [[Nima Arkani-Hamed]], Jacob L. Bourjaily, Freddy Cachazo, Alexander B. Goncharov, Alexander Postnikov, Jaroslav Trnka, _Scattering Amplitudes and the Positive Grassmannian_ ([arXiv:1212.5605](http://arxiv.org/abs/1212.5605))
 {#Arkani-Hamed}

For mathematical background see

* Alexander Postnikov, _Total positivity, Grassmannians, and networks_ ([arXiv:math/0609764](http://arxiv.org/abs/math/0609764))

### Twistor space formulation
 {#ReferencesTwistorSpace}

The [[twistor]] space formulation of $N=4$ $D = 4$ SYM was originally found from the [[B-model]] [[string theory]] in 

* [[Edward Witten]], _Perturbative Gauge Theory As A String Theory In Twistor Space_, Commun. Math. Phys. 252:189-258,2004 ([arXiv:hep-th/0312171/](http://arxiv.org/abs/hep-th/0312171/))

A comprehensive discussion is in 

* Rutger Boels, Lionel Mason, David Skinner, _Supersymmetric Gauge Theories in Twistor Space_, JHEP 0702:014,2007 ([arXiv:hep-th/0604040](http://arxiv.org/abs/hep-th/0604040))

See also ([Monteiro](#Monteiro)) below.

### Scattering amplitudes

For the moment see at 

* _[[scattering amplitude]]_ 

and also at

* _[[motivic multiple zeta values]]_.


### Relation to number theory

Relating the [[abc conjecture]] to [[D=4 N=4 super Yang-Mills theory]]:

* [[Yang-Hui He]], Zhi Hu, Malte Probst, James Read, _Yang-Mills Theory and the ABC Conjecture_,  International Journal of Modern Physics A Vol. 33, No. 13, 1850053 (2018)  ([arXiv:1602.01780](https://arxiv.org/abs/1602.01780), [doi:10.1142/S0217751X18500537](https://doi.org/10.1142/S0217751X18500537))


[[!redirects N=4 D=4 SYM]]

[[!redirects N=4 D=4 sYM]]

[[!redirects D=4 N=4 SYM]]
[[!redirects D=4 N=4 super Yang-Mills]]

