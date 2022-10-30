
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

_Linear type theory_ is the [[linear logic]]-version of [[type theory]]. In the definition of ([Seely 89, prop. 1.5](#Seely89)), following ([Girard 87](#Girard87)), this is the [[internal language]] of/has [[categorical semantics]] in [[star-autonomous categories]]. 

But more generally _linear type theory_ came to refer to the internal [[type theory]] of any possibly-non-[[cartesian monoidal category|cartesian]] [[symmetric monoidal category|symmetric]] [[closed monoidal category]]. Indeed, this general notion still faithfully follows the original motivation for the term "linear" as introduced in ([Girard 87](#Girard87)), since the non-cartesianness of the [[tensor product]] means the absence of a [[diagonal]] map and hence the impossibility of [[functions]] to depend on more than a single (linear) copy of their [[variables]].

The [[dependent type theory]]-version of linear type theory should be _[[dependent linear type theory]]_.

Linear (dependent) type theory can be argued to be the proper [[type theory]] for [[quantum logic]]. In this context the linearity of the type theory, hence the absence of [[diagonal maps]] in its [[categorical semantics]], corresponds to the [[no-cloning theorem]] in [[quantum physics]].

## Properties

### Categorical semantics

(...)

In [[star-autonomous categories]].



| Conjunctive operator | [[de Morgan duality]]  | Disjunctive operator |
| -------------------- | - | -------------------- |
| $\top$               |   | $0$                  |
| $1$                  |   | $\bot$               |
| $\&$                 |   | $\oplus$             |
| $\otimes$            |   | $\parr$              |
| $^\bot$              |   | $^\bot$              |
| $\bigwedge$          |   | $\bigvee$            |
| $!$                  |   | $?$                  |

(...)

### The canonical co-modality

The original axiomatics for [[linear type theory]] in ([Girard 87](#Girard87)) contain in addition to the structures corresponding to a ([[star-autonomous category|star-autonomous]]) [[symmetric monoidal category|symmetric]] [[closed monoidal category]] a certain (co-)[[modality]] traditionally denoted "$!$". 
In ([Benton 95](#Benton95), [Bierman 95](#Bierman95))
it is noticed (reviewed in ([Barber 97, p. 21 (26)](#Barber97))) that a natural [[categorical semantics]] for this modality identifies it with the [[comonad]] that is induced from a [[strong monoidal adjunction]]

$$
  (\Sigma \dashv R)
  \;\colon\;
  \mathcal{C}
  \stackrel{\overset{\Sigma}{\leftarrow}}{\underset{R}{\longrightarrow}}
  S
$$

between the [[closed monoidal category|closed]] [[symmetric monoidal category]] $\mathcal{C}$ wich interprets the given [[linear type theory]] and a [[cartesian monoidal category]] $S$.

If there is only the [[strong monoidal functor]] $\Sigma \;\colon\; S \longrightarrow \mathcal{C}$ without possibly a [[right adjoint]], then ([Barber 97, p. 21 (27)](#Barber97)) speaks of the _structural fragment_ of [[linear type theory]].

In ([Ponto-Shulman 12](#PontoShulman12)) it is observed that this in turn is canonically induced if $\mathcal{C} \simeq \mathcal{C}_\ast$ is the linear type theory over the trivial context of a [[dependent linear type theory]]/[[indexed closed monoidal category]] with category of contexts being $S$. See at _[dependent linear type theory -- Properties -- Canonical co-modality](http://ncatlab.org/nlab/show/dependent+linear+type+theory#TheCanonicalComodality)_ for more on this.

## Related concepts

* [[modal type theory]]

* [[geometric homotopy type theory]]

* [[stable homotopy type]]

## References

The orginal notion of [[linear logic]] was introduced in 

*  [[Jean-Yves Girard]], _Linear logic_,   Theoretical Computer Science 50:1, 1987.  ([pdf](http://iml.univ-mrs.fr/~girard/linear.pdf))
 {#Girard87}

A review is in

* [[Jean-Yves Girard]], part III of _[[Lectures on Logic]]_, European Mathematical Society 2011
 {#Girard11}


The [[categorical semantics]] of linear type theory in [[star-autonomous categories]] was first described in 

*  [[R. A. G. Seely]],  _Linear logic, $\ast$-autonomous categories and cofree coalgebras_, _Contemporary Mathematics_ 92, 1989.  ([[SeelyLinearLogic.pdf:file]], [ps.gz](http://www.math.mcgill.ca/rags/nets/llsac.ps.gz))
 {#Seely89}

(but see also the first non-syntactic, mathematical categorical model in the same volume)

* V. de Paiva, _The Dialectica Categories_, _Contemporary Mathematics_ 92, 1989. ([web] (http://www.cs.bham.ac.uk/~vdp/publications/dial87.pdf)) 

and reviewed/further discussed in

* Gavin M. Bierman, _What is a categorical model of intuitionistic linear logic? ([web] (http://research.microsoft.com/en-us/um/people/gmb/papers/tlca95.pdf))

* Andrew Graham Barber, _Linear Type Theories, Semantics and Action Calculi_, 1997 ([web](http://www.lfcs.inf.ed.ac.uk/reports/97/ECS-LFCS-97-371/&#8206;), [pdf](http://www.lfcs.inf.ed.ac.uk/reports/97/ECS-LFCS-97-371/ECS-LFCS-97-371.pdf))
 {#Barber97}

* [[Paul-André Melliès]] , _Categorial Semantics of Linear Logic_, in _Interactive models of computation and program behaviour_, Panoramas et synth&#232;ses 27, 2009 ([pdf](http://www.pps.univ-paris-diderot.fr/~mellies/papers/panorama.pdf))

The interpretation of Girard's $!$-modality as the [[comonad]] induced from a [[monoidal adjunction]] between the closed [[symmetric monoidal category]] and a [[cartesian closed category]] is due to

* G. Bierman, _On Intuitionistic Linear Logic_ PhD thesis, Computing
Laboratory, University of Cambridge, 1995
 {#Bierman95}

* N. Benton, _A mixed linear and non-linear logic; proofs, terms and
models_, In _Proceedings of Computer Science Logic_ '94, vol. 933 of
Lecture Notes in Computer Science. Verlag, June 1995. 
 {#Benton95}

Interpretation of this in [[dependent linear type theory]] is in 

* [[Kate Ponto]], [[Mike Shulman]], _Duality and traces for indexed monoidal categories_, Theory and Applications of Categories, Vol. 26, 2012, No. 23, pp 582-659 ([arXiv:1211.1555](http://arxiv.org/abs/1211.1555))
 {#PontoShulman12}


Further discussion of linear type theory is for instance in

* _Capter 7, Linear type theory_ [pdf](http://www.cs.cmu.edu/~fp/courses/linear/handouts/lintt.pdf)

* Anders Schack-Nielsen, Carsten Sch&#252;rmann, _Linear contextual modal type theory_ [pdf](http://www.itu.dk/~carsten/papers/lcmtt.pdf)

* Bernardo Toninho, Lu&#237;s Caires, Frank Pfenning, _Dependent Session Types via Intuitionistic Linear Type Theory_ [pdf](http://ctp.di.fct.unl.pt/~lcaires/papers/dstypes.pdf)

* Iliano Cervesato, [[Frank Pfenning]], _A Linear Logical Framework_, 1996, ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.21.1152))

Discussion of application of linear logic to [[quantum logic]], [[quantum computing]] and generally to [[quantum physics]] includes

* [[Vaughan Pratt]], _Linear logic for generalized quantum mechanics_, in Proc. of _Workshop on Physics and Computation (PhysComp'92)_ ([pdf](http://boole.stanford.edu/pub/ql.pdf), [web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.137.7817))

* [[Ross Duncan]], _Types for quantum mechanics_, 2006 ([pdf](http://homepages.ulb.ac.be/~rduncan/papers/rduncan-thesis.pdf))

* Gianpiero Cattaneo, Maria Luisa Dalla Chiara, Roberto
Giuntini and Francesco Paoli, section 9 of _Quantum Logic and Nonclassical Logics_, p. 127 in  Kurt Engesser, Dov M. Gabbay, Daniel Lehmann (eds.) _Handbook of Quantum Logic and Quantum Structures: Quantum Logic_, 2009 North Holland
  {#CCGP09}


* Ugo Dal Lago, Claudia Faggian, _On Multiplicative Linear Logic, Modality and Quantum Circuits_ ([arXiv:1210.0613](http://arxiv.org/abs/1210.0613))


Discussion of linear type theory without [[units]] is in 

* [[Robin Houston]], _Linear Logic without Units_ ([arXiv:1305.2231](http://arxiv.org/abs/1305.2231))

Discussion of [[inductive types]] in the context of linear type theory is in 

* St&#233;phane Gimenez, _Towards Generic Inductive Constructions in
Systems of Nets_ ([pdf](http://www.imn.htwk-leipzig.de/WST2013/papers/paper_16.pdf))


[[!redirects linear type theories]]

[[!redirects linear type]]
[[!redirects linear types]]

[[!redirects linear homotopy type]]
[[!redirects linear homotopy types]]