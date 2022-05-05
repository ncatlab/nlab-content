
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

A **formal immersion** $F$ of one [[smooth manifold]], $M$, into another, $N$, is an injective [[bundle morphism]] $T M \to T N$ between their [[tangent bundles]].

That is, $F$ consists of a [[smooth function]] $f \;\colon\; M \to N$ and a [[homomorphism]] of [[vector bundle]] $F \;\colon\; T M\to T N$ covering $f$ such that the [[linear function]] $F|_{x} \;\colon\; T_x M \to T_{f(x)} N$ is  an [[injective function]]  for  every  point $x$ in $M$. 

Write $Imm^f(M,N)$ for the space of such formal immersions.

## Relation to immersions

Since an actual [[immersion of smooth manifolds]] is a formal immersion where the [[bundle morphism]] in question is specifically taken to be the pointwise [[derivative]] $d f$,
there is a natural [[continuous function]] $Imm(M,N) \to Imm^f(M,N)$, sending an actual [[immersion of smooth manifolds|immersion]] $f$ to the formal immersion with injective bundle morphism $d f$. 

Smale and Hirsch established that when $M$ is compact, and also either $M$ is  _open_ (in the sense that the complement of the boundary has no compact component) or $dim(M) \lt dim(N)$, then the map $Imm(M,N) \to Imm^f(M,N)$ is a [[weak  homotopy equivalence]].

When combined with the result that $Imm^f(S^k,\mathbb{R}^{n+k}) \to Map(S^k, V_k(\mathbb{R}^{n+k}))$ can be shown to be a homotopy equivalence, where $V_k(\mathbb{R}^{n+k})$ is the Stiefel manifold of $k$-frames in $\mathbb{R}^{n+k}$, the previous result establishes that isotopy classes of immersions of $S^k$ into $\mathbb{R}^{n+k}$ are in bijection with $\pi_k V_k(\mathbb{R}^{n+k})$.


##References

* [[John Francis]], _The h-principle, lectures 1 and 2: overview_, ([pdf](https://sites.math.northwestern.edu/~jnkf/classes/hprin/1overview.pdf))

[[!redirects formal immersions of smooth manifolds]]