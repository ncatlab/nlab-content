


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc} 

## Idea

The [[generalized homology theory]] which is [[Brown representability theorem|represented]] by the [[sphere spectrum]] $\mathbb{S}$ is usually called _stable homotopy_, since the [[homology groups]] that it assigns to a suitable [[topological space]] $X$ are just the [[stable homotopy group]] of $X$:

$$
  H_\bullet(X,\mathbb{S})
  \;=\;
  \mathbb{S}_\bullet(X)
  \coloneqq
  \pi_\bullet\left( \mathbb{S} \wedge X_+  \right)
  \;=\;
  \simeq \pi_\bullet^{st}(X)
  \,.
$$

Hence the [[coefficient]] [[cohomology ring]] of stable homotopy homology theory (its value on the [[point]]) is the [[stable homotopy groups of spheres]]. This highlights that stable homotopy homology of any space $X$ is extremely hard, or impossible, to completely analyze, since this is true already for the coefficient ring over the point.

Beware that the term _[[stable homotopy theory]]_, which would seem to be the canonical name for this [[generalized homology theory]], traditionally refers instead to the general [[homotopy theory]] of [[spectra]]. The full term _stable homotopy homology theory_ is used for emphasis, but clunky in practice.

The [[duality|dual]] [[generalized (Eilenberg-Steenrod) cohomology|generalized cohomology theory]], co-represented by the [[sphere spectrum]], is called _[[stable cohomotopy theory]]_.

## Properties

### Relation to other homology theories

Along the canonical morphism of [[spectra]] $\mathbb{S} \to H R$ from the [[sphere spectrum]] to any [[Eilenberg-MacLane spectrum]] of a [[ring]] $R$ (which is the [[unit]] map of $H R$ in the [[(infinity,1)-category]] of [[E-infinity ring spectra]]) stable homotopy homology maps to [[ordinary homology]] with [[coefficients]] in $R$ (given notably by [[singular homology]]).

This is known as the _[[Hurewicz homomorphism]]_

More generally, for $E$ an [[E-infinity ring spectrum]], the unit $\mathbb{S} \to E$ induces a [[natural transformation]] from stable homotopy homology theory to the [[generalized homology theory]] co-represented by $E$. 

This is known as the _[[Boardman homomorphism]]_.


## Related concepts

* [[ordinary homology]]

* [[bordism homology theory]]

* [[stable cohomotopy theory]]

## References

* [[Akhil Mathew]], _Torsion exponents in stable homotopy and the Hurewicz homomorphism_, Algebr. Geom. Topol. 16 (2016) 1025-1041 ([arXiv:1501.07561](https://arxiv.org/abs/1501.07561))
