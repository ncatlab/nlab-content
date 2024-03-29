
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The notion of _cofibration_ is [[duality|dual]] to that of _[[fibration]]_. See there for more details.

A _cofibration_ is a member of a distinguished *class of cofibrations* in one of the several setups in [[homotopy theory]]:

* [[model category|Quillen categories]] of models for homotopy theory

* the [[category with cofibrations|categories with cofibrations]] of Baues

* [[Waldhausen categories]]

In traditional [[topology]], one usually means a [[Hurewicz cofibration]]. 

In [[category theory]] and [[descent theory]], Grothendieck however introduced a notion of cofibered category or cofibration, whose definition is categorically dual to that of a [[fibered category]] and based on the generalization of the universal property of coCartesian squares; however it does not correspond to the extension property in topology, but to a lifting property, like for [[fibration]]s. For that reason, Gray suggested (and this is to some extent adopted in $n$lab) to call such categories [[opfibration]]s. In the [[quasicategory|quasicategorical]] setup, the generalizations of fibered categories are called [[Cartesian fibration]]s, and the generalizations of op/co-fibered categories are called coCartesian fibrations. 
In the $1$-categorical setup, the coCartesian arrows in op/co-fibrations are indeed the ones which complete coCartesian squares in the special and most important case of [[domain opfibration]]s.


## Examples
 {#Examples}

* [[relative cell complex]] inclusions are the cofibrations in the [[classical model structure on topological spaces]]

* closed [[Hurewicz cofibration]] are the cofibrations in  in the [[Strøm's model category]] on  [[Top]]

* [[monomorphisms]] are the cofibrations in [[Cisinski model structures]] such as the [[classical model structure on simplicial sets]]

## Stability properties

Cofibrations are _usually_ defined in such a way that they are stable at least under the following operations in the category under consideration

 * composition 
 * pushouts of spans at least one of whose legs is a cofibration

(Please mind the precise definitions of the category you are using. 
Also compare the stability properties of the dual notion [[fibration]].)

## Related concepts

* [[fibration]]
* [[resolution]]
* [[cofibrant object]]
* [[codiscrete cofibration]]


[[!redirects cofibration]]
[[!redirects cofibrations]]
[[!redirects Cofibrations]]

