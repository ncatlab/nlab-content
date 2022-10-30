
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

The notion of _$n$-plectic form_ is a generalization of the notion of [[symplectic form]] to [[differential forms]] of more than two arguments. This is considered in [[higher symplectic geometry]], specifically: in [[multisymplectic geometry]].

## Definition

+-- {: .num_defn}
###### Definition

For $X$ a [[smooth manifold]] and $n \in \mathbb{N}$, $n \geq 1$, a [[differential form]] $\omega$ on $X$ is **$n$-plectic**
if 

1. it is an $n$-forms, $\omega \in \Omega^n(X)$;

1. it is closed: $d_{dR} \omega = 0$;

1. it is non-degenerate in that the [[contraction]] map

   $$
     \iota_{(-)}\omega : \Gamma(T X) \to \Omega^{n-1}(X)
   $$

   has trivial [[kernel]].

=--

+-- {: .num_remark}
###### Remark

This definition has an evident generalization to the case where also $X$ is allowed to be a "higher" generalization of a smooth manifold, namely a [[smooth ∞-groupoid]] or [[L-∞ algebroid]]. See [[higher symplectic geometry]] for more on this case.

=--

## References

See the references at [[multisymplectic geometry]].

For instance definition 2.1 in 

* [[Chris Rogers]], _Higher symplectic geometry_ PhD thesis ([arXiv](http://arxiv.org/abs/1106.4068)).


[[!redirects multisymplectic form]]

