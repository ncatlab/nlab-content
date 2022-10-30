
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


## Relation to monadic descent

Ordinary [[Grothendieck fibration]]s correspond to [[pseudofunctor]]s to [[Cat]], by the [[Grothendieck construction]] and hence to [[stack|prestacks]]. For these one may consider [[descent]].

If the fibration is even a bifibration, there is a particularly elegant algebraic way to encode its decent properties; this is [[monadic descent]]. The [[Benabou–Roubaud theorem]] characterizes descent properties for bifibrations.

## Related concepts

* [[Grothendieck fibration]]

* [[Beck-Chevalley condition]]

[[!redirects bifibrations]]
