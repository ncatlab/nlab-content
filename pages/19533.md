
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### &#201;tale morphisms
+--{: .hide}
[[!include etale morphisms - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A **formal immersion** $F$ of one [[smooth manifold]], $M$, into another, $N$, is an injective bundle map $T M \to T N.$  

That is, $F$ consists of a map $f:M \to N$ and a vector bundle map $F: T M\to T N$ covering $f$ such that the map $F|_{x}:T_x M \to T_{f(x)} N$ is  injective  for  every  point $x$ in $M$. $Imm^f(M,N)$ is the space of formal immersions.

## Relation to immersions

There is a natural map $Imm(M,N) \to Imm^f(M,N)$, sending an [[immersion of smooth manifolds|immersion]] $f$ to the injective bundle map $d f$. 

Smale and Hirsch established that when $M$ is compact, and also either $M$ is  _open_ (in the sense that the complement of the boundary has no compact component) or $dim(M) \lt dim(N)$, then the map $Imm(M,N) \to Imm^f(M,N)$ is a [[weak  homotopy equivalence]].

When combined with the result that $Imm^f(S^k,\mathbb{R}^{n+k}) \to Map(S^k, V_n(\mathbb{R}^{n+k}))$ can be shown to be a homotopy equivalence, where $V_n(\mathbb{R}^{n+k})$ is the Stiefel manifold of $n$-frames in $\mathbb{R}^{n+k}$, the previous result establishes that isotopy classes of immersions of $S^k$ into $\mathbb{R}^{n+k}$ are in bijection with $\pi_k V_n(\mathbb{R}^{n+k})$.


##References

* [[John Francis]], _The h-principle, lectures 1 and 2: overview_, ([pdf](https://sites.math.northwestern.edu/~jnkf/classes/hprin/1overview.pdf))