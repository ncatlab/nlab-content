
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

That is, $F$ consists of a [[smooth function]] $f \;\colon\; M \to N$ and a [[homomorphism]] of [[vector bundles]] $F \;\colon\; T M\to T N$ covering $f$ such that the [[linear function]] $F|_{x} \;\colon\; T_x M \to T_{f(x)} N$ is  an [[injective function]] for every point $x$ in $M$. 

Write $Imm^f(M,N)$ for the space of such formal immersions. There is a [[fibration]] over the space of smooth functions from $M$ to $N$, $Map^{sm}(M, N)$, forgetting the bundle homomorphism, whose [[fiber]] over $f$ is $Hom^{inj}_{Vect_M}(T M, f^{\ast}T N)$.

**Note**: Some authors define formal immersions in terms of continuous functions (e.g., [Laudenbach17, p. 6](#Laudenbach17)). However, the space $Map^{sm}(M, N)$ is homotopy equivalent to the space of all continuous functions, $Map(M, N)$, due to integrating against a smoothing kernel. 

## Relation to immersions

Since an actual [[immersion of smooth manifolds]] is a formal immersion where the [[bundle morphism]] in question is specifically taken to be the pointwise [[derivative]] $d f$,
there is a natural [[continuous function]] $Imm(M,N) \to Imm^f(M,N)$, sending an actual [[immersion of smooth manifolds|immersion]] $f$ to the formal immersion with injective bundle morphism $d f$. 

[[Stephen Smale]] and [[Morris Hirsch]] established that when $M$ is compact, and also either $M$ is  _open_ (in the sense that the complement of the boundary has no compact component) or $dim(M) \lt dim(N)$, then the map $Imm(M,N) \to Imm^f(M,N)$ is a [[weak  homotopy equivalence]]. This is an instance of the [[h-principle]].

When combined with the result that $Imm^f(S^k,\mathbb{R}^{n+k}) \to Map(S^k, V_k(\mathbb{R}^{n+k}))$ can be shown to be a homotopy equivalence, where $V_k(\mathbb{R}^{n+k})$ is the Stiefel manifold of $k$-frames in $\mathbb{R}^{n+k}$, the previous result establishes that isotopy classes of immersions of $S^k$ into $\mathbb{R}^{n+k}$ are in bijection with $\pi_k V_k(\mathbb{R}^{n+k})$. In the case where $k = 2$ and $n = 1$, we find that immersions of the [[2-sphere]] into $\mathbb{R}^3$ are classified by $\pi_2 V_2(\mathbb{R}^3)= \pi_2(SO(3))= 0$, in other words, all such immersions are  isotopic.  In  particular, $S^2$ can be turned inside-out ([[sphere eversion]]) inside $R^3$ by moving through a family of immersions.  


##References

* [[John Francis]], _The h-principle, lectures 1 and 2: overview_, ([pdf](https://sites.math.northwestern.edu/~jnkf/classes/hprin/1overview.pdf))

* [[Konrad Voelkel]], Helene Sigloch, _Homotopy sheaves and h-principles_, ([pdf](https://www.konradvoelkel.com/wp-content/uploads/homotopy-sheaves.pdf))

* {#Laudenbach17} Francois Laudenbach, _René Thom and an anticipated h-principle_, ([arXiv:1703.08108](https://arxiv.org/abs/1703.08108))

[[!redirects formal immersions of smooth manifolds]]