
#Contents#
* automatic table of contents goes here
{:toc}


## Definition

A **bifibration** of [[category|categories]] is a [[functor]]

$$
  E \to B
$$

that is both a [[Grothendieck fibration]] as well as an opfibration.

Therefore every morphism $f : b_1 \to b_2$ in a bifibration has both a push-forward $f_* : E_{b_1} \to E_{b_2}$ as well as a pullback $f^* : E_{b_2} \to E_{b_1}$.


## Relation to monadic descent

Ordinary [[Grothendieck fibration]]s correspond to [[pseudofunctor]]s to [[Cat]], by the [[Grothendieck construction]] and hence to [[stack|prestacks]]. For these one may consider [[descent]].

If the fibration is even a bifibration, there is a particularly elegant algebraic way to encode its decent properties; this is [[monadic descent]]. The [[Benabou–Roubaud theorem]] characterizes descent properties for bifibrations.