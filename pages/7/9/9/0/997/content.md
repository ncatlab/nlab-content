
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Definition


A __cogenerator__ in a [[category]] $C$ is an [[object]] $S$ such that the [[functor]] $h_S = C(-,S) : C^{\mathrm{op}} \to \mathrm{Set}$ is [[faithful functor|faithful]]. This means that for any pair $g_1,g_2\in C(X,Y)$, if they are indistinguishable by morphisms to $S$ in the sense that
$$ \forall (\theta: Y \to S),\; \theta \circ g_1 = \theta \circ g_2 ,$$
then $g_1 = g_2$.

One often extends this notion to a __cogenerating family__ of objects, which is a (usually [[small category|small]]) set $\mathcal{S} = \lbrace S_a, a\in A\rbrace$ of objects in $C$ such that the family $C(-,S_a)$ is jointly faithful. This means that for any pair $g_1,g_2\in C(X,Y)$, if they are indistinguishable by morphisms to $\mathcal{S}$ in the sense that
$$ \forall (a: A),\; \forall (\theta: Y \to S_a),\; \theta \circ g_1 = \theta \circ g_2 ,$$
then $g_1 = g_2$.



## Examples

In [[Set]], the set of [[truth value]]s is a cogenerator.  More generally, in any [[well-pointed topos]], the [[subobject classifier]] is a cogenerator.


The existence of a small (co)generating family is one of the conditions in one version of the [[adjoint functor theorem]].


## Related concepts

* [[generator]]

* **cogenerator**


[[!redirects cogenerators]]

[[!redirects cogenerating set]]