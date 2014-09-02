
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The notion of _orthogonal spectrum_ in [[stable homotopy theory]] is a variant of that of _[[spectrum]]_. An orthogonal spectrum is a sequence of [[pointed topological spaces]] $\{X_n\}_{n \in \mathbb{N}}$ equipped with maps $X_n \wedge S^1 \longrightarrow X_{n+1}$ from the [[suspension]] of one into the next, but such that the $n$th [[topological space]] is equipped with an [[action]] of the [[orthogonal group]] $O(n)$ and such that all the induced structure maps 

$$
  X_n \wedge S^k \longrightarrow X_{n+k}
$$

are all $O(n)\times O(k)$-[[equivariance|equivariant]], hence are [[action]] [[homomorphisms]].

## Properties

### Relation to the cobordism hypothesis

A [[connective spectrum]] is equivalently a grouplike [[E-∞ space]], hence a [[Picard ∞-groupoid]]. As such it is an [[(∞,0)-category]] of [[fully dualizable objects]]. By the [[cobordism hypothesis]] this means that it is equipped with an $O(n)$-[[∞-action]] for all $n$, coming from the action $O(n)$ on the [[framed manifold|n-framings]] of the point in the [[(∞,n)-category of cobordisms]]. This $O(n)$-action is that which is encoded by the definition of orthogonal spectrum ([Lurie 09, example 2.4.15](#Lurie09)).




### Relation to global equivariant stable homotopy theory

Since orthogonal spectra are by definition equipped with orthogonal group [[actions]], they serve as models for [[equivariant homotopy theory]] "for all groups at once", called _[[global stable homotopy theory]]_.

## Related concepts

* [[symmetric spectrum]]

* [[global equivariant stable homotopy theory]]

## References

Orhtogonal spectra were introduced in 

* [[Michael Mandell]], [[Peter May]], [[Stefan Schwede]], and [[Brooke Shipley]],  _Model categories of diagram spectra_, 1998

* [[Michael Mandell]], [[Peter May]], _Equivariant orthogonal spectra and
S-modules_. Preprint, April 29, 2000, ([K-theory Preprint Archives](http://www.math.uiuc.edu/K-theory/0408/))


Reviews include

* Knut Berg, _Orthogonal spectra_ ([pdf](http://folk.uio.no/rognes/theses/orthogonal.pdf))

See also

* {#Lurie09} [[Jacob Lurie]], _[[On the Classification of Topological Field Theories]]_, Current Developments in Mathematics Volume 2008 (2009), 129-280 ([arXiv:0905.0465](http://arxiv.org/abs/0905.0465))


[[!redirects orthogonal spectra]]