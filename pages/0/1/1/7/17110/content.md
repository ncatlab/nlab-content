
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

a [[manifold]] of [[dimension]] 4.

## Examples

* [[4-sphere]]

* [[spacetime]]

## Properties

#### Cohomotopy


Let $X$ be a [[4-manifold]] which is [[connected topological space|connected]] and [[orientation|oriented]].

The [[Pontryagin-Thom construction]] as [above](cohomotopy#RelationToCobordismGroup) gives for $n \in \mathbb{Z}$ the [[commuting diagram]] of sets

$$
  \array{
     \pi^n(X) 
       &\overset{\simeq}{\longrightarrow}&
     \mathbb{F}_{4-n}(X)
     \\
     {}^{ \mathllap{h^n} }
     \downarrow
       &&
     \downarrow^{ h_{4-n} }
     \\
     H^n(X,\mathbb{Z})
       &\underset{\simeq}{\longrightarrow}&
     H_{4-n}(X,\mathbb{Z})
     \,,
  }
$$

where $\pi^\bullet$ denotes [[cohomotopy]] sets, $H^\bullet$ denotes [[ordinary cohomology]], $H_\bullet$ denotes [[ordinary homology]] and $\mathbb{F}_\bullet$ is [[normal bundle|normally]] [[framing|framed]] [[cobordism classes]] of [[normal bundle|normally]] [[framing|framed]] [[submanifolds]]. Finally $h^n$ is the operation of pullback of the generating integral cohomology class on $S^n$ (by the nature of [[Eilenberg-MacLane spaces]]):

$$
  h^n(\alpha) \;\colon\; X \overset{\alpha}{\longrightarrow} S^n \overset{generator}{\longrightarrow} B^n \mathbb{Z}
  \,.
$$

Now 

* $h^0$, $h^1$, $h^4$ are [[isomorphisms]]

* $h^3$ is an isomorphism if $X$ is "odd" in that it contains at least one closed oriented [[surface]] of odd self-intersection, otherwise $h^3$ becomes an isomorphism on a $\mathbb{Z}/2$-[[quotient group]] of $\pi^3(X)$ (which is a group via the [[group]]-[[structure]] of the [[3-sphere]] ([[special unitary group|SU(2)]]))

([Kirby-Melvin-Teichner 12](#KirbyMelvinTeichner12))


## Related concepts

* [[Yang-Mills instanton]]

* [[Donaldson-Thomas invariants]]

* [[2-manifold]], [[3-manifold]], [[8-manifold]]

## References

All [[PL manifold|PL]] [[4-manifolds]] are _simple_ [[branched covers]] of the  [[4-sphere]]:

* {#Piergallini95} [[Riccardo Piergallini]], _Four-manifolds as 4-fold branched covers of $S^4$_, Topology Volume 34, Issue 3, July 1995 (<a href="https://doi.org/10.1016/0040-9383(94)00034-I">doi:10.1016/0040-9383(94)00034-I</a>, [pdf](https://core.ac.uk/download/pdf/82379618.pdf))

* {#IoriPiergallini02} Massimiliano Iori, [[Riccardo Piergallini]], _4-manifolds as covers of the 4-sphere branched over non-singular surfaces_, Geom. Topol. 6 (2002) 393-401 ([arXiv:math/0203087](https://arxiv.org/abs/math/0203087))

On [[cohomotopy]] of 4-manifolds:

* [[Daniel Freed]], [[Karen Uhlenbeck]], Appendix B of: _Instantons and Four-Manifolds_, Mathematical Sciences Research Institute Publications, Springer 1991 ([doi:10.1007/978-1-4613-9703-8](https://link.springer.com/book/10.1007/978-1-4613-9703-8))

* {#KirbyMelvinTeichner12} [[Robion Kirby]], [[Paul Melvin]], [[Peter Teichner]], _Cohomotopy sets of 4-manifolds_, GTM 18 (2012) 161-190 ([arXiv:1203.1608](https://arxiv.org/abs/1203.1608))



[[!redirects 4-manifolds]]