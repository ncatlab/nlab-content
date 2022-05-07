
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Higher category theory
+-- {: .hide}
[[!include higher category theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

For morphisms between [[dualizable objects]] in a [[symmetric monoidal category]] there is a notion of _[[trace]]_. More generally, for a [[fully dualizable object]] $V$ in a [[symmetric monoidal (∞,n)-category]] $\mathcal{C}^\otimes$ there is a notion of $k$-dimensional trace for each $k \leq n$ and indeed for each diffeomorphism type of a [[closed manifold]].

The [[cobordism theorem]] says that a [[monoidal (∞,n)-functor]] $Z \colon Bord_n \to \mathcal{C}^\otimes$ from the [[(∞,n)-category of cobordisms]] picks a [[fully dualizable object]] $V \coloneqq Z(\ast) \in \mathcal{C}$ and then sends the $k$-[[sphere]] $S^k$ to the $k$-dimensional higher trace of the identity on $X$:

$$
  tr_{S^k}(id_{id_{ \cdots id_V}}) \in \Omega^k \mathcal{C}
  \,.
$$


This are the "round traces". More generally the [[cobordism theorem]] gives a higher dimensional trace of the "shape" of any [[closed manifold]] $\Sigma$ of [[dimension]] $k$ on any [[fully dualizable object]] $X$

$$
  tr_{\Sigma}(id_V) \in \Omega^k \mathcal{C}
$$

and for every $k$-manifold with [[boundary]] $\partial \Sigma$ the relative trace is a morphism

$$
  (1 \stackrel{tr_{\Sigma}(V)}{\longrightarrow} tr_{\partial \Sigma}(id_V))
  \in 
  Hom_{\Omega^{k-1}\mathcal{C}}(1,tr_{\partial \Sigma}(id_V))
  \,.
$$

## Examples

Higher dimensional traces in a an [[(∞,n)-category of correspondences]] are give by higher [[span traces]]. Those of the shape of [[Riemann surfaces]] are spelled out for instance in ([lpqft](#lpqft)).

## Related concepts

* [[trace]]

* [[bicategorical trace]]

* [[span trace]]

* [[opetopic type theory]]

## References

* [[David Ben-Zvi]], [[David Nadler]], _Secondary Traces_ ([arXiv:1305.7177](http://arxiv.org/abs/1305.7177))

* [[David Ben-Zvi]], [[David Nadler]], _Nonlinear traces_ ([arXiv:1305.7175](http://arxiv.org/abs/1305.7175))

* {#lpqft} _[[schreiber:Local prequantum field theory]]_

[[!redirects higher traces]]

[[!redirects higher dimensional trace]]
[[!redirects higher dimensional traces]]

