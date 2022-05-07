
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--


#Contents
* table of contents
{:toc}


## Idea

Where a system of [[quantum mechanics]] is specified by

* a [[Hilbert space]] $\mathcal{H}$;

* a [[hermitean operator]] $H$  on $\mathcal{H}$ -- the [[Hamiltonian]];

a system of _supersymmetric quantum mechanics_ has 

* a [[super Hilbert space]] $\mathcal{H}$;

* an odd [[linear operator]] $D$ in $\mathcal{H}$, the [[supercharge]]

* such that $D \circ D = H$ is the [[Hamiltonian]].

If we regard the Hamiltonian as the generator of the [[Poincare Lie algebra]] in one dimension -- the  [[super translation Lie algebra]] --, then the graded commutator $[D,D] = 2 H$ is the [[supersymmetry]] extension to the [[super Poincaré Lie algebra]] in super-dimension $(1|1)$.

The data of a system of supersymmetric quantum mechanics may also be formalized in terms of a [[spectral triple]].

## Properties


### Relation to spinning particles
 {#RelationToSpinningParticles}

A simple but often underappreciated fact is that the [[worldline theory]] of any [[spinning particle]] is supersymmetric, and hence is supersymmetric quantum mechanics, _on the [[worldline]]_. In this sense relativistic supersymmetric quantum mechanics is not the exception but the rule, it is something exhibited by every [[fermion]] in the world. See at _[spinning particle -- Worldline supersymmetry](spinning+particle#WorldlineSupersymmetry)_for more on this. 

Of course the bulk of the literature considers non-relativistic supersymmetric quantum mechanics. That is much less relevant in nature. 


### Relation to index theory
 {#RelationToIndexTheory}

Another fairly simple but very deep fact is that the [[partition function]] of a supersymmetric [[quantum mechanical system]], namely the [[supertrace]] of its propagator, is equivalently what in mathematics (in [[index theory]]) is called the [[index]] of the supercharge regarded as a [[Fredholm operator]]. See the references [below](#ReferencesRelationToIndexTheory) for more on this.

This relation is at the heart of a deep and ubiquituous role that supersymmetric quantum mechanics plays in the [[mathematics]] of [[K-theory]] and related topics (and vice versa). For a general abstract discussion of why there is such a relation see also at _[super algebra -- Abstract idea](super+algebra#AbstractIdea)_ and at _[[super line 2-bundle]]_.

### Relation to Morse theory

For the moment see [below](#ReferencesRelationToMorseTheory).

### Relation to superstrings
 {#RelationToSuperstrings}

Supersymmetric quantum mechanics was introduced or at least became famous with ([Witten 82](#Wittem82)). As explained at the end of ([Witten 85](#Witten85)), [[Edward Witten|Witten]] had come to consider this while looking at the point particle limit of the [[superstring]] [[sigma-model]]. The superstring sigma-model is a kind of supersymmetric quantum mechanics on [[loop space]] (see also at [[2-spectral triple]]) and ordinary supersymmetric quantum mechanics is obtained from this in the limit of vanishing loop size (see e.g [Schreiber 04](#Schreiber04)). Under this identification the above discussion of [[index theory]] translates to Witten's interpretation of the universal [[elliptic genus]] as what is now known as the _[[Witten genus]]_ (see there for more).

One way to make this rigorously precise would be to realize the [[Dirac-Ramond operator]] of the [[superstring]] as an actual [[Dirac operator on smooth loop space]] (the string's [[Wheeler superspace]]), as originally suggested in ([Witten 87b](#Witten87b)).


## Related entries

* [[hadron supersymmetry]]

* [[Morse theory]]

* [[index]]

* [[(1,1)-dimensional Euclidean field theories and K-theory]]
  

## References
 {#References}

### General
  {#ReferencesGeneral}

A fairly comprehensive survey and discussion of supersymmetric quantum mechanics as such, with emphasis on its relation to [[spectral geometry]] ("[[noncommutative geometry]]") is in

* {#FGR96} [[Jürg Fröhlich]], Oiver Grandjean, [[Andreas Recknagel]], _Supersymmetric quantum theory and (non-commutative) differential geometry_, Commun.Math.Phys. 193 (1998) 527-594 ([arXiv:hep-th/9612205](http://arxiv.org/abs/hep-th/9612205))

and with more emphasis on the relation to the [[superstring]] ([[2-spectral triples]]) in section 7 of:

* {#FGR97} [[Jürg Fröhlich]], Oliver Grandjean, [[Andreas Recknagel]], _Supersymmetric quantum theory, non-commutative geometry, and gravitation_  Lecture Notes Les Houches (1995) ([arXiv:hep-th/9706132](http://arxiv.org/abs/hep-th/9706132)).

Another survey is

* Fred Cooper, Avinash Khare, Uday Sukhatme, _Supersymmetry and Quantum Mechanics_ Physics Reports Volume 251 (1995), 267-385. ([arXiv:hep-th/9405029](http://arxiv.org/abs/hep-th/9405029))


On [[supersymmetric quantum mechanics]] in the perspective of [[supergeometry]] ([[integration over supermanifolds]], [[picture changing operators]]):

* [[Leonardo Castellani]], [[Roberto Catenacci]], [[Pietro Grassi]], _Super Quantum Mechanics in the Integral Form Formalism_, Ann. Henri Poincaré (2018) 19: 1385 ([arXiv:1706.04704](https://arxiv.org/abs/1706.04704))


### Relation to Morse theory
 {#ReferencesRelationToMorseTheory}

Supersymmetric quantum mechanics gained attention with the work

* {#Witten82} [[Edward Witten]], _Supersymmetry and Morse theory_  J. Differential Geom. Volume 17, Number 4 (1982), 661-692. ([Euclid](http://projecteuclid.org/euclid.jdg/1214437492), [pdf](http://www.cimat.mx/~gil/docencia/2012/teoria_de_morse/witten_supersymmetry_and_morse_theory.pdf), [spire](http://inspirehep.net/record/176416?ln=de))

which showed that [[Morse theory]] may be equivalently interpreted as the study of [[supersymmetry|supersymmetric]] [[vacua]] in supersymmetric quantum mechanics, and  which was part of what gained Witten the [Fields medal 1990](http://159.226.47.99:8080/general/prize/medal/1990.htm). In this article a certain family of deformations of [[superparticles]] on a [[Riemannian manifold]] are considered and the supersymmetric ground states are shown to be given by the [[Morse theory]] of the deformation function. 

For a survey of the relation to Morse theory see for instance

* [[Gábor Pete]], section 2 of _Morse theory_, lecture notes 1999-2001   ([pdf](http://www.math.bme.hu/~gabor/morse.pdf))

* Rohit Jain, _Supersymmetric Schr&#246;dinger operators with applications to Morse theory_ ([pdf](http://www.ma.utexas.edu/users/rjain/SUSY.pdf))

This deformed supersymmetric quantum mechanics arises as the point-particle limit of the [[type II superstring]] regarded as [[quantum mechanics]] on the [[smooth loop space]] (the string's [[Wheeler superspace]]), a relation that is stated more explicitly in 

* {#Witten85} [[Edward Witten]], from p. 92 (32 of 39) on in: _Global anomalies in string theory_, in: W. Bardeen and A. White (eds.). _Symposium on Anomalies_, Geometry, Topology_, pp. 61&#8211;99. World Scientific, 1985  ([[WittenGlobalAnomaliesInStringTheory.pdf:file]], [spire:214913](https://inspirehep.net/literature/214913))

and then in

* {#Witten87b} [[Edward Witten]], _The Index Of The Dirac Operator In Loop Space_ Proc. of Conf. on Elliptic Curves and Modular Forms in Algebraic Topology Princeton (1986) ([spire](http://inspirehep.net/record/245523))

The relation between the 2d [[SCFT]] describing the [[type II superstring]] and this deformed supersymmetric quantum mechanics on [[smooth loop space]] has been further explored in 

* {#Schreiber04} [[Urs Schreiber]], _On deformations of 2d SCFTs_, JHEP 0406:058,2004 ([arXiv:hep-th/0401175](http://arxiv.org/abs/hep-th/0401175))




### Relation to index theory
 {#ReferencesRelationToIndexTheory}

The relation of the [[partition function]] of supersymmetric quantum mechanics to [[index theory]] was suggested in unpublished work of [[Edward Witten]] and formulated in

* [[Luis Alvarez-Gaumé]], _Supersymmetry and the Atiyah-Singer index theorem_, Comm. Math. Phys. Volume 90, Number 2 (1983), 16-173. ([Euclid](http://projecteuclid.org/euclid.cmp/1103940278))
 {#AlvarezGaume83}

* [[Ezra Getzler]], _Pseudodifferential operators on supermanifolds and the Atiyah-Singer index theorem_, Comm. Math. Phys. 92 (1983), 163-178. ([pdf](http://math.northwestern.edu/~getzler/Papers/1103940796.pdf))
 {#Getzler83}

* [[D. Quillen]], _Superconnections and the Chern character_, Topology 24 (1985), no. 1, 89&#8211;95, ([doi](https://doi.org/10.1016/0040-9383%2885%2990047-3)); 

* [[Varghese Mathai]], [[Daniel Quillen]], _Superconnections, Thom classes, and equivariant differential forms_. Topology 25 (1986), no. 1, 85&#8211;110; 

*  [[Ezra Getzler]], _A short proof of the Atiyah-Singer index theorem_, Topology 25 (1986), 111-117 ([pdf](http://math.northwestern.edu/~getzler/Papers/local.pdf))
 {#Getzler86}

* [[D. Quillen]], _Superconnection character forms and the [[Cayley transform]]_, Topology 27 (1988), no. 2, 211&#8211;238

### In String theory 
  {#InStringTheory}

The [[superstring]]'s supersymmetric quantum mechanics on [[smooth loop space]] (the string's [[Wheeler superspace]]) motivated the subject in

* {#Witten85} [[Edward Witten]], from p. 92 (32 of 39) on in: _Global anomalies in string theory_, in: W. Bardeen and A. White (eds.). _Symposium on Anomalies_, Geometry, Topology_, pp. 61&#8211;99. World Scientific, 1985  ([[WittenGlobalAnomaliesInStringTheory.pdf:file]], [spire:214913](https://inspirehep.net/literature/214913))

* {#Witten87b} [[Edward Witten]], _The index of the Dirac operator in loop space_ Proc. of Conf. on Elliptic Curves and Modular Forms in Algebraic Topology Princeton (1986) ([spire](http://inspirehep.net/record/245523))

and is further explored in:

* {#Schreiber04} [[Urs Schreiber]], _On deformations of 2d SCFTs_, JHEP 0406:058, 2004 ([arXiv:hep-th/0401175](http://arxiv.org/abs/hep-th/0401175))


For supersymemtric quantum mechanics of [[D0-branes]] see:

* _[[BFSS matrix model]]_, _[[BMN matrix model]]_

Discussion of [[M-theory on Calabi-Yau 5-folds]] in terms of [[supersymmetric quantum mechanics]]:

* [[Alexander Haupt]], [[Andre Lukas]], [[Kellogg Stelle]], _M-theory on Calabi-Yau Five-Folds_, JHEP 0905:069, 2009 ([arXiv:0810.2685](https://arxiv.org/abs/0810.2685))


