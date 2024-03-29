
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The notion of _$n$-plectic form_ is a generalization of the notion of [[symplectic form]] to [[differential forms]] of more than two arguments. This is considered in [[higher symplectic geometry]], specifically: in [[n-plectic geometry]]/[[multisymplectic geometry]].

## Definition

+-- {: .num_defn}
###### Definition

For $X$ a [[smooth manifold]] and $n \in \mathbb{N}$, $n \geq 1$, a [[differential form]] $\omega$ on $X$ is **$n$-plectic**
if 

1. it is an $(n+1)$-form, $\omega \in \Omega^{n+1}(X)$;

1. it is closed: $d_{dR} \omega = 0$;

1. it is non-degenerate in that the [[contraction]] map

   $$
     \iota_{(-)}\omega \;\colon\; \Gamma(T X) \to \Omega^{n}(X)
   $$

   has trivial [[kernel]].

=--

+-- {: .num_remark}
###### Remark

An 1-plectic form is equivalently a [[symplectic form]].

=--

+-- {: .num_remark}
###### Remark

If the last condition is dropped, then by analogy with [[presymplectic forms]] one may speak of a _pre-$n$-plectic_ form. Of course this is just a closed $(n+1)$-form, but as in the presymplectic case, the plectic-terminology indicates that one wants to regard it as input datum for [[higher geometric quantization]]. 

=--

+-- {: .num_remark}
###### Remark

This definition has an evident generalization to the case where also $X$ is allowed to be a "higher" generalization of a smooth manifold, namely a [[smooth ∞-groupoid]] or [[L-∞ algebroid]]. See [[higher symplectic geometry]] for more on this case.

=--

## References

See the references at _[[n-plectic geometry]]_ and at _[[multisymplectic geometry]]_.

For instance definition 2.1 in 

* [[Chris Rogers]], _Higher symplectic geometry_ PhD thesis ([arXiv](http://arxiv.org/abs/1106.4068)).

See also

* [[Domenico Fiorenza]], [[Chris Rogers]], [[Urs Schreiber]], _Higher geometric prequantum theory_ ([arXiv:1304.0236](http://arxiv.org/abs/1304.0236))



[[!redirects n-plectic forms]]

[[!redirects multisymplectic form]]

[[!redirects pre-n-plectic form]]
[[!redirects pre-n-plectic forms]]

[[!redirects pre-n-plectic manifold]]
[[!redirects pre-n-plectic manifolds]]

[[!redirects pre n-plectic manifold]]
[[!redirects pre n-plectic manifolds]]
