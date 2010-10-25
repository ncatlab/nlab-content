
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _Steenrod-approximation theorem_ states mild conditions under which an extension of a [[smooth function]] on a [[closed subset]] by a [[continuous function]] may itself be improved to an extension by a smooth function.

This is a smooth enhancement of the [[Tietze extension theorem]].

## Statement

+-- {: .un_theorem }
###### Theorem


Let $X$ be a finite [[dimension]]al [[connected]] [[smooth manifold]] [[manifold with corners|with corners]]. Let $\pi : E \to X$ be a locally trivial [[Diff|smooth]]  [[bundle]] with a [[locally convex]] [[manifold]] $N$ as typical [[fiber]] and $\sigma : X \to E$ a [[continuous function|continuous]] [[section]].

If $L \subset X$ is a [[closed subset]] and $U \subset X$ is an [[open subset]] such that $\sigma$ is [[smooth function|smooth]] in a [[neighbourhood]] of $L \setminus U$, then:

1. for each open neighbourhood $O \of \Sigma(X)$ in $E$ there exists a section $\tau : X \to O$ 

   * which is smooth in a neighbourhood of $L$;

   * and which equals $\sigma$ on $X \setminus U$;

1. there exists a [[homotopy]] $F : [0,1] \times X \to O$ between $\sigma$ and $\tau$ such that

   * each $F(t,-)$ is a section of $\pi$;

   * for $(t,x) \in [0,1] \times (X \setminus U)$ we have $F(t,x) = \sigma(x) = \tau(x)$.

=--



## References

* [[Christoph Wockel]], _A Generalisation of Steenrod's Approximation Theorem_ Archivum mathematicum, Volume 45  No. 2 (2009) ([arXiv:0610252](http://arxiv.org/abs/math/0610252))

[[!redirects Steenrod approximation theorem]]