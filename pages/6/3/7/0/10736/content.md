
#Contents#
* table of contents
{:toc}

## Idea

Segal maps, named after [[Graeme Segal]], appear in the definition of the _[[Segal conditions]]_ on a [[simplicial object]].

In the context of [[higher category theory]] they 
were used by [[Charles Rezk]] to define [[Segal categories]] and [[complete Segal spaces]].

## Definition

Let $X$ be a [[bisimplicial set]].  Assume for simplicity that $X$ is [[fibrant]] with respect to the [[Reedy model structure]] on the [[functor category]] $[\Delta^{op}, SSet]$.  The **$n$-th Segal map** of $X$ is the canonical [[morphism]] of [[simplicial sets]]
  $$ X_n \to (X_1)^{\times_{X_0} (n)} = X_1 \times_{X_0} \cdots \times_{X_0} X_1. $$
Here the right-hand side is the [[limit]] of the diagram
  $$ X_1 \stackrel{d_1}{\to} X_0 \stackrel{d_0}{\leftarrow} X_1 \stackrel{d_1}{\to} \cdots \stackrel{d_1}{\to} X_0 \stackrel{d_0}{\leftarrow} X_1 $$
where there are $n$ copies of $X_1$.

More explicitly, this morphism is induced by the morphisms $a_i: X_n \to X_1$ ($0 \le i \le n-1$), which are induced by the morphisms $\alpha^i: [1] \to [n]$ in $\Delta$, the [[simplex category]], which map $0 \mapsto i$ and $1 \mapsto i+1$.

If $X$ is not [[Reedy model structure|Reedy fibrant]], then one must replace the [[limit]] above with a [[homotopy limit]].

## References

* [[Julie Bergner]], _Three models for the homotopy theory of homotopy theories_, Topology 46 (2007), 397-436, [arXiv:math/0504334](http://arxiv.org/abs/math/0504334).

[[!redirects Segal maps]]

[[!redirects Segal morphism]]
[[!redirects Segal morphisms]]