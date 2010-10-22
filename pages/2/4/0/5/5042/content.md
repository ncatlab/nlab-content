
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

The [[model category]] structure on the category $dgLie_k$ of [[dg-Lie algebra]]s over a commutative [[ring]] $k \superset \mathbb{Q}$ has

* fibrations the surjective maps

* weak equivalences the [[quasi-isomorphism]]s.

This is a [[simplicial model category]] with respect to the [[sSet]]-[[hom functor]]

$$
  dgLie(\mathfrak{g}, \mathfrak{g})
  :=
  ([k] \mapsto Hom_{dgLie}(\mathfrak{g} , \Omega^\bullet(\Delta^k) \otimes\mathfrak{h}))
  \,,
$$

where 

* $\Omega^\bullet(\Delta^k)$ is the [[dg-algebra]] of polynomial [[differential form]]s on the $k$-[[simplex]];

* $\Omega^\bullet(\Delta^k)\otimes \mathfrak{h}$ is the canonical dg-Lie algebra structure on the tensor product.

## Properties

There is a [[Quillen equivalence]] to the [[model structure on dg-coalgebras]].


## References

This goes back to appendix B of

* [[Dan Quillen]], _Rational homotopy theory_ , Annals of Math., 90(1969), 205&#8211;295.

For more discussion see

* [[Vladimir Hinich]], _Homological algebra of homotopy algebras_ , Comm. in algebra, 25(10)(1997), 3291&#8211;3323.

* [[Vladimir Hinich]], _DG coalgebras as formal stacks_ ([arXiv:math/9812034](http://arxiv.org/abs/math/9812034))