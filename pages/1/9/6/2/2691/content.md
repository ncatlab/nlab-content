<div class="rightHandSide toc">
[[!include model category theory - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea ##

By the dual [[Dold-Kan correspondence]] cochain complexes in non-negative degree are equivalent to [[cosimplicial object|cosimplicial]] abelian groups. Moreover, the [[monoidal Dold-Kan correspondence]] maps [[cosimplicial algebra]]s to [[dg-algebra]]s, but this is no longer an equivalence of ordinary categories. It should, however, be an equivalence of the full [[(∞,1)-category|(∞,1)-categories]] of these objects. This, in turn, should be modeled by a [[model category]] structures.

The model structure on dg-algebras is such a model.


## Definition ##

Write $dgAlg$ for the [[category]] of [[dg-algebra]]s over a [[field]] of characteristic 0.

+-- {: .un_defn}
###### Definition

The  **projective** [[model category]] structure on $dgAlg$ is given by setting:

* weak equivalences are the [[quasi-isomorphism]]s

* fibrations are the degreewise [[epimorphism|surjections]].

=--

+-- {: .un_prop }
###### Proposition

This indeed defines a [[model category]]. 

At least when restricted to (graded) commutative dg-algebras this is a [[cofibrantly generated model category]].

=--

+-- {: .proof}
###### Proof

See the references below.

=--


### Commutative vs. non-commutative dg-algebras ###

+-- {: .un_prop }
###### Observation


The [[stuff, structure, property|forgetful functor]]

$$
  F :  CdgAlg \to dgAlg
$$

from (graded-)commutative [[dg-algebra]]s to dg-algebras is the [[right adjoint]] part of a [[Quillen adjunction]]

$$
  Ab
  :
  dgAlg 
   \stackrel{\leftarrow}{\to}
  CdgAlg
  :
  F
$$

=--

+-- {: .proof}
###### Proof

The forgetful functor clearly preserves fibrations and cofibrations. It has a [[left adjoint]], the free abelianization functor $Ab$, which sends a [[dg-algebra]] $A$ to its quotient $A/[A,A]$.

=--


+-- {: .un_theorem }
###### Theorem

Let the ground [[ring]] $k$ be a [[field]] of characteritsic 0. Then every [[dg-algebra]] $A$ which has the structure of an [[algebra over an operad|algebra over]] the [[E-k-operad|E-∞ operad]] has a [[dg-algebra]] morphism $A \to A_c$ to a commutative dg-algebra $A_c$  which is

* a morphism of [[E-k-operad|E-∞ algebras]] (where $A_c$ has the obvious [[E-k-operad|E-∞ algebras]] structure)

* a weak weak equivalence in the model structure on dg-algebras (i.e. a [[quasi-isomorphism]] of the underlying cochain complexes).

=--

So this says that the weak equivalence classes of the commutative dg-algebras in the model category of all dg-algebras already exhaust the most general non-commutative but  homotopy-commutative dg-algebras.

+-- {: .proof}
###### Proof

This is in II.1.5 of 

* [[Igor Kriz]] and [[Peter May]], _Operads, algebras, modules and motives_ , Ast&eacute;risque No 233 (1995)

=--



## References ##



The cofibrantly generated model structure on **commutative** cochain [[dg-algebra]]s induced from the forgetful functor to cochain complexes is surveyed for instance on p. 6 of 

* [[Kathryn Hess]], _Rational homotopy theory: a brief introduction_ ([arXiv](http://arxiv.org/abs/math.AT/0604626))

A standard textbook reference is section V.3 of

* [[Sergei Gelfand]], [[Yuri Manin]], _Methods of homological algebra_, Springer

An original reference seems to be

* A. Bousfield, V. Gugenheim, _On PL deRham theory and rational homotopy type_ Memoirs of the AMS 179 (1976)


For general **non-commutative** (or rather: not necessarily graded-commutative) dg-algebras a model structure is given in

* J.F. Jardine, _[[JardineModelDG.pdf:file]]_ , Cyclic Cohomology and Noncommutative Geometry, Fields Institute Communications, Vol. 17, AMS (1997), 55-58. 

This is also the structure used in 

* J.L. Castiglioni G. Corti&#241;as, _Cosimplicial versus DG-rings: a version of the Dold-Kan correspondence_ ([arXiv](http://arxiv1.library.cornell.edu/abs/math/0306289v2))

where aspects of its relation to the [[model structure on cosimplicial rings]] is discussed. (See [[monoidal Dold-Kan correspondence]] for
more on this).


[[!redirects model structure on dg-rings]]
[[!redirects model structure on dg-algebra]]