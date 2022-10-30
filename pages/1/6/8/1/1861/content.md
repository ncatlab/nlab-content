
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

Where [[homotopy groups]] are groups of [[homotopy classes]] of maps  out [[spheres]], $\pi_n(X)\coloneqq [S^n \to X]$, cohomotopy groups are groups of homotopy classes _into_ spheres, $\pi^n(X) \coloneqq [X \to S^n]$.

If instead one considers mapping into the [[stabilization]] of the spheres, hence into (some [[suspension spectrum|suspension]] of) the [[sphere spectrum]], then one speaks of _[[stable cohomotopy]]_. In other words, the [[generalized (Eilenberg-Steenrod) cohomology]] theory which is [[Brown representability theorem|represented]] by the [[sphere spectrum]] is _stable cohomotopy_.

In this vein, regarding terminology: the concept of [[cohomology]] (as discussed there) in the very general sense of [[non-abelian cohomology]], is about [[homotopy classes]] of maps _into_ any object $A$ (in some [[(∞,1)-topos]]). In this way, general non-abelian cohomology is sort of dual to homotopy, and hence might generally be called co-homotopy. This is the statement of _[[Eckmann-Hilton duality]]_. The duality between homotopy (groups) and co-homotopy proper may then be thought of as being the special case of this where $A$ is taken to be a sphere. 

## Properties

### Relation to Freudenthal suspension theorem

relation to the [[Freudenthal suspension theorem]] ([Spanier 49, section 9](#Spanier49))


### Smooth representatives

For $X$ a [[compact topological space|compact]] [[smooth manifold]], there is a [[smooth function]] $X \to S^n$ representing every cohomotopy class (with respect to the standard [[smooth structure]] on the [[sphere]] [[manifold]]).

## Examples

### Of 4-Manifolds
 {#On4Manifolds}

Let $X$ be a [[4-manifold]] which is [[connected topological space|connected]] and [[orientation|oriented]].

The [[Pontryagin-Thom construction]] gives for $n \in \mathbb{Z}$ the [[commuting diagram]] of sets

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

where $\pi^bullet$ denotes cohomotopy sets, $H^\bullet$ denotes [[ordinary cohomology]], $H_\bullet$ denotes [[ordinary homology]] and $\mathbb{F}_\bullet$ is [[normal bundle|normally]] [[framing|framed]] [[cobordism classes]] of [[normal bundle|normally]] [[framing|framed]] [[submanifolds]]. Finally $h^n$ is the operation of pullback of the generating integral cohomology class on $S^n$ (by the nature of [[Eilenberg-MacLane spaces]]):

$$
  h^n(\alpha) \;\colon\; X \overset{\alpha}{\longrightarrow} S^n \overset{generator}{\longrightarrow} B^n \mathbb{Z}
  \,.
$$

Now 

* $h^0$, $h^1$, $h^4$ are [[isomorphisms]]

* $h^3$ is an isomorphism is $X$ is "odd" in that it contains at least one closed oriented [[surface]] of odd self-intersection, otherwise $h^3$ becomes an isomorphism on a $\mathbb{Z}/2$-[[quotient group]] of $\pi^3(X)$ (which is a group via the [[group]]-[[structure]] of the [[3-sphere]] ([[special unitary group|SU(2)]]))

([Kirby-Melvin-Teichner 12](#KirbyMelvinTeichner12))

## Related concepts

* [[stable cohomotopy]]


## References

* Wikipedia, _[Cohomotopy group](http://en.wikipedia.org/wiki/Cohomotopy_group)_

* [[eom]], _[Cohomotopy group](https://www.encyclopediaofmath.org/index.php/Cohomotopy_group)_
 
* {#Spanier49} [[Edwin Spanier]], _Borsuk's Cohomotopy Groups_, Annals of Mathematics Second Series, Vol. 50, No. 1 (Jan., 1949), pp. 203-245 ([jstor](http://www.jstor.org/stable/1969362))

* [[Laurence Taylor]], _The principal fibration sequence and the second cohomotopy set_, Proceedings of the Freedman Fest, 235251, Geom. Topol. Monogr., 18, Coventry, 2012 ([arXiv:0910.1781](https://arxiv.org/abs/0910.1781))

* {#KirbyMelvinTeichner12} [[Robion Kirby]], [[Paul Melvin]], [[Peter Teichner]], _Cohomotopy sets of 4-manifolds_, GTM 18 (2012) 161-190 ([arXiv:1203.1608](https://arxiv.org/abs/1203.1608))

[[!redirects cohomotopy group]]
[[!redirects cohomotopy groups]]