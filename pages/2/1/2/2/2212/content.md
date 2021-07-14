
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea ##

A _cosimplicial algebra_ -- similarly a cosimplicial ring -- is a [[cosimplicial object]] in the category of [[algebra]]s (of [[ring]]s).

## Relation to differential graded algebras ##

Under the [[monoidal Dold–Kan correspondence]], cosimplicial algebras are essentially identified with [[differential graded algebra]]s in non-negative degree: the [[Moore complex|Moore cochain complex]] $C^\bullet(A)$ of a cosimplicial algebra $A$ is a [[differential graded algebra]] where the degreewise product on the cosimplicial algebra maps to the [[cup product]] operation that gives the [[monoid]] structure $C^\bullet(A)$.


## Model category structure ##

A standard [[model category]] structure on the category of cosimplicial rings is the following

* fibrations are the degreewise surjections

* weak equivalences are the morphisms that induce isomorphisms in [[cohomotopy]]

* cofibrations are defined by their left [[lifting property]].

For more see [[model structure on cosimplicial algebras]].

References are section 2.1 of

* [[Bertrand Toen]], _Affine stacks (Champs affines)_ ([arXiv:math/0012219](http://arxiv.org/abs/math/0012219)) .

and  [def 9.1, p. 18](http://arxiv.org/PS_cache/math/pdf/0306/0306289v3.pdf#page=18) of 

* Castiglioni, Cortinas, _Cosimplicial versus dg-rings_ ([arXiv](http://arxiv.org/abs/math/0306289))


## Examples 

* As cosimplcial algebras are [[duality|dual]] to simplicial spaces, each simplicial space $X$ gives rise to a cosimplicial algebra of functions on it. A list of examples is given at [[schreiber:Chevalley-Eilenberg algebra]].

## Related concepts

* [[cosimplicial abelian group]]

## References 

The model category structure on cosimplicial algebras is discussed in detail in: 

* [[Bertrand Toën]], Section 2.1 of: _Champs affines_, Selecta Math. new series **12** (2006), no. 1, 39-135 ([arXiv:math/0012219](https://arxiv.org/abs/math/0012219), [doi:10.1007/s00029-006-0019-z](https://doi.org/10.1007/s00029-006-0019-z))


The [[Quillen equivalence]] between cosimplicial algebras and cochain dg-algebras is discussed in

* Castiglioni, Cortinas, _Cosimplicial versus dg-rings_ ([arXiv](http://arxiv.org/abs/math/0306289))


A bit about cosimplicial algebras is in [section 7](http://atlas.mat.ub.es/personals/burgos/files/brbr.pdf#page=63) of

* Jos&#233; Burgos Gil, _The regulators of Beilinson and Borel_ ([pdf](http://atlas.mat.ub.es/personals/burgos/files/brbr.pdf))

This also discusses aspects of their image in [[dg-algebra]]s under the [[Moore complex]]-functor. See [[monoidal Dold-Kan correspondence]] for more on that.

[[!redirects cosimplicial ring]]

