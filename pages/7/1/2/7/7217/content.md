
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Definition

Every [[strict 2-category]] $K$ with finite [[strict 2-limits]] and finite strict 2-colimits becomes a [[model category]] (or, rather, its underlying 1-category does) in a canonical way, where:

* The weak equivalences are the [[equivalences]].

* The fibrations are the morphisms that are representably [[isofibrations]], i.e. the morphisms $e\to b$ such that $K(x,e)\to K(x,b)$ is an isofibration for all $x\in K$.

* The cofibrations are determined.

We call it the **2-trivial model structure**, as it is a 2-categorical analogue of the [[trivial model structure]] on any 1-category.  It can be said to regard $C$ as an [[(∞,1)-category]] with only trivial [[k-morphisms]] for $k \geq 3$.


## Properties

* Every object is fibrant and cofibrant.

* In [[Cat]], this produces the [[canonical model structure]].

* In the 2-category of spaces, continuous functions and homotopy classes of homotopies, this produces the [[model structure on topological spaces#Hurewicz (or Strøm) Model Structure|Hurewicz model structure]].

* By duality, any such category has another model structure, with the same weak equivalences but where the cofibrations are the iso-cofibrations and the fibrations are determined.  In $Cat$, the two model structures are the same.

* If $T$ is an [[accessible functor|accessible]] [[strict 2-monad]] on a [[locally finitely presentable category|locally finitely presentable]] [[strict 2-category]] $K$.  Then the category $T Alg_s$ of strict $T$-[[algebra over a monad|algebras]] admits a [[transferred model structure]] from the 2-trivial model structure on $K$.  The cofibrant objects therein are the [[flexible algebra]]s.

## References

* [[Steve Lack]], *Homotopy-theoretic aspects of 2-monads*, [arXiv](http://arxiv.org/abs/math.CT/0607646)

[[!redirects trivial model structure on a 2-category]]
[[!redirects trivial model structure for a 2-category]]
