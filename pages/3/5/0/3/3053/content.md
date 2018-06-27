
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Definition

A **bifibration** of [[category|categories]] is a [[functor]]

$$
  E \to B
$$

that is both a [[Grothendieck fibration]] as well as an opfibration.

Therefore every morphism $f : b_1 \to b_2$ in a bifibration has both a push-forward $f_* : E_{b_1} \to E_{b_2}$ as well as a pullback $f^* : E_{b_2} \to E_{b_1}$.


## Examples

* For $C$ any [[category]] with [[pullback]]s, the [[codomain fibration]] $cod : [I,C] \to C$ is a bifibration.

* Dually, for $C$ any [[category]] with [[pushout]]s, the [[domain opfibration]] $dom : [I,C] \to C$ is a bifibration.

* The canonical functor [[Mod]] $\to $ [[CRing]] is a bifibration.

* The [[forgetful functor]] [[Top]] $\to$ [[Set]] is a bifibration. See also [[topological concrete category]].

* The [[forgetful functor]] [[Grpd]] $\to$ [[Set]] is a bifibration.

* The [[forgetful functor]] [[Cat]] $\to$ [[Set]] is a bifibration.

## Relation to monadic descent

Ordinary [[Grothendieck fibration]]s correspond to [[pseudofunctor]]s to [[Cat]], by the [[Grothendieck construction]] and hence to [[stack|prestacks]]. For these one may consider [[descent]].

If the fibration is even a bifibration, there is a particularly elegant algebraic way to encode its descent properties; this is [[monadic descent]]. The [[Benabou–Roubaud theorem]] characterizes descent properties for bifibrations.

## Relation to distributive laws

Fibrations and opfibrations on a category $C$ (or more generally an object of a suitable 2-category) are the algebras for a pair of pseudomonads.  If $C$ has pullbacks, there is a [[pseudo-distributive law]] between these pseudomonads, whose joint algebras are the bifibrations satisfying the [[Beck-Chevalley condition]]; see [(von Glehn)](#vonGlehn).

## Remark
A bifibration $F:E\to B$ such that $F^{op}:E^{op}\to B$ is a bifibration as well is called a [[trifibration]] (cf. Pavlovi&#263; 1990, p.315).

## Bifibration of model categories

In ([CagneMelli&egrave;s](#CagMell)) the authors develop a notion of **Quillen bifibration** which combines the two concepts of Grothendieck bifibration and [[Quillen model structure]], establishing conditions for when in a bifibration model structures on all the fibers and on the base combine to give one on the total category. 

## Bifibration of bicategories

The basic theory of [[2-fibrations]], fibrations of bicategories, is developed in ([Buckley](#Buckley)). One (unpublished) proposal by Buckley and Shulman, for a "2-bifibration", a bifibration of [[bicategories]], is a functor of bicategories that is both a 2-fibration and a 2-opfibration. This should correspond to a pseudofunctor into $2 Cat_{adj}$, just as for 1-categories.  There is a difference from this case, however, in that although a 2-fibration (corresponding to a "doubly contravariant" pseudofunctor $B^{coop} \to 2Cat$) has both cartesian lifts of 2-cells and 1-cells, a 2-opfibration (corresponding to a totally *covariant* pseudofunctor $B\to 2Cat$) has opcartesian lifts of 1-cells but still *cartesian* lifts of 2-cells.

## Related concepts

* [[Grothendieck fibration]]

* [[Beck-Chevalley condition]]

* [[hyperdoctrine]]

## References

* [[Paul-André Melliès]], [[Noam Zeilberger]], _Type refinement and monoidal closed bifibrations_, ([arXiv.1310.0263](http://arxiv.org/abs/1310.0263v1)).

* [[Dusko Pavlovic|Duško Pavlović]], _Categorical Interpolation: Descent and the Beck-Chevalley Condition without Direct Images_ , pp.306-325  in _Category theory Como 1990_, LNM **1488** Springer Heidelberg 1991.

* [[Tamara von Glehn]], *Polynomials and models of type theory*, [PhD thesis](https://www.repository.cam.ac.uk/handle/1810/254394)
 {#vonGlehn}

* [[Mitchell Buckley]], _Fibred 2-categories and bicategories_, ([arXiv:1212.6283](https://arxiv.org/abs/1212.6283)) {#Buckley}

* {#CagMell} [[Pierre Cagne]], [[Paul-André Melliès]], _On bifibrations of model categories_, ([arXiv:1709.10484](https://arxiv.org/abs/1709.10484))


[[!redirects bifibrations]]