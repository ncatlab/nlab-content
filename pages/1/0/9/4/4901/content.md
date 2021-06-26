
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### Mapping space
+--{: .hide}
[[!include mapping space - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}

## Idea

A _derived loop space_ is a [[free loop space object]] in [[derived geometry]].

## Definition

Let $T$ be an [[(∞,1)-algebraic theory]] and $C \subset T Alg_\infty^{op}$ an [[(∞,1)-site]] of [[Isbell duality|formal duals]] of $\infty$-algebras over $T$. Then the [[(∞,1)-topos]] $\mathbf{H} = (\infty,1) Sh(C)$ encodes [[derived geometry]] modeled on $T$. 

A **derived loop space** is a [[free loop space object]] in such $\mathbf{H}$.

More specifically, if $T$ is an ordinary [[Lawvere theory]], regarded as a 1-truncated $(\infty,1)$-theory, then $T Alg_{\infty}$ are its simplicial algebras. There is a canonical embedding $T Alg^{op} \hookrightarrow T Alg_\infty^{op}$ of the ordinary algebras into the $\infty$-algebras, so that we may regard $X \in T Alg^{op}$ as an object of $\mathbf{H}$. Then the _derived loop space_ of $X$ is its [[free loop space object]] computed in $\mathbf{H}$.

The point is that the derived loop space of an ordinary $X \in T Alg^{op}$ in general is a significantly richer object than the free loop space object of $X$ as computed just in the underived $(\infty,1)$-topos $(\infty,1)Sh(T Alg^{op})$. In fact, since $X$ is 0-[[truncated]] in $(\infty,1)Sh(T Alg^{op})$, it coincides with its free loop space object there, but the derived loop space does not.

## Function complexes on derived loop spaces: Hochschild homology

The function complex on the derived loop space $\mathcal{L}X$ is the [[Hochschild homology]] complex of $C(X)$. See there for further details. In particular see the section _[Hochschild cohomology -- As function algebra on the derived loop space](Hochschild%20cohomology#HochschildChainComplex)_.



Also see [[free loop space object]] for more information.

## Related concepts

* [[loop space object]], [[free loop space object]],

  * [[delooping]]

  * [[loop space]], [[free loop space]], 

  * [[formal loop space]], **derived loop space**

  * [[derived microlocalization]]

  * [[inertia orbifold]]

* [[suspension object]]

  * [[suspension]]


## References

The relevance of derived loop spaces was amplified in a series of articles by [[David Ben-Zvi]] and [[David Nadler]],

* [[David Ben-Zvi]], [[David Nadler]],

  * _Loop Spaces and Langlands Parameters_ ([arXiv:0706.0322](http://arxiv.org/abs/0706.0322)) 

  * _Integral Transforms and Drinfeld Centers in Derived Algebraic Geometry _ ([arXiv:0805.0157](http://arxiv.org/abs/0805.0157))

  * _Loop Spaces and Connections_ ([arXiv:1002.3636](http://arxiv.org/abs/1002.3636))

    This article uses To&#235;n's theory of [[function algebras on ∞-stacks]] for showing that the function complex on a derived loop space $\mathcal{L}X$ is under mild conditions the [[Hochschild homology]] complex of $X$ hence by [[Hochschild-Kostant-Rosenberg theorem]] the collection of [[Kähler differential]] forms on $X$, and that the functions on $\mathcal{L}X$ that are invariant under the canonical $S^1$-[[action]] on $\mathcal{L}X$ are the _closed_ forms. This also gives a geometric interpretation of the old observation by [[Maxim Kontsevich]] and others, that the differential and grading on the de Rham complex may be understood as induced from automorphisms of the [[odd line]].

  * _Loop Spaces and Representations_ ([arXiv:1004.5120](http://arxiv.org/abs/1004.5120))


[[!redirects derived loop spaces]]
