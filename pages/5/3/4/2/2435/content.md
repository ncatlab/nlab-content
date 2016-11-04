
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
####supergeometry and superalgebra
+--{: .hide}
[[!include supergeometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

The category $S Vect$ of [[super vector space]]s is the [[symmetric monoidal category]] which as a [[monoidal category]] is the ordinary monoidal category of $\mathbb{Z}_2$-[[graded vector space]]s for which

$$
  (V \otimes W)^{ev} := V^{ev}\otimes W^{ev} \oplus
    V^{odd} \otimes W^{odd}
$$

and

$$
  (V \otimes W)^{odd} := V^{ev}\otimes W^{odd} \oplus
    V^{odd} \otimes W^{ev}
$$


but equipped with the _unique non-trivial_ symmetric monoidal structure 

$$
  V \otimes W \stackrel{\sigma_{V,W}}{\to}
  W \otimes V
$$

that is given on homogeneously graded elements $v,w$ of degree $|v|, |w| \in \mathbb{Z}_2$ as


$$
  v \otimes w \mapsto (-1)^{|v| |w|} w \otimes v
  \,.
$$

## Properties

* [[monoids]] in $S Vect$ are [[super algebras]].

* [[manifolds]] modeled on $S Vect$ are [[supermanifolds]]

* etc.

## Related concepts

* [[Deligne's theorem on tensor categories]] says that all suitable [[tensor categories]] of subexponential growth have a [[fiber functor]] to $sVect$ and are equivalent to [[categories of representations]] of affine algebraic [[supergroups]].

[[!redirects sVect]]
[[!redirects SuperVect]]