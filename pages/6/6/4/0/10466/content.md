
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
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

What is called _global equivariant homotopy theory_ is a variant of [[equivariant cohomology]] in [[homotopy theory]] where [[pointed object|pointed]] [[topological spaces]]/[[homotopy types]] are equipped with $G$-[[infinity-actions]] "for all [[compact Lie groups]] $G$ at once".

Sometimes this is referred to just as "global homotopy theory", leaving the equivariance implicit. There is also a [[stabilization|stable]] version involving [[spectra]] equipped with [[infinity-actions]], see at _[[global equivariant stable homotopy theory]]_.

More precisles, the _global equivariant homotopy category_ is the [[(∞,1)-category]] (or else its [[homotopy category of an (∞,1)-category|homotopy category]]) of [[(∞,1)-presheaves]] $PSh_\infty(Orb)$ on the global [[orbit category]] $Orb$ ([Henriques-Gepner 07, section 1.3](#HenriquesGepner07)), regarded as an [[(∞,1)-category]].

Here $Orb$ has as [[objects]] [[compact Lie groups]] and the [[(∞,1)-categorical hom-spaces]] $Orb(G,H) \coloneqq \Pi [\mathbf{B}G, \mathbf{B}H] $, where on the right we have the [[geometric realization of cohesive infinity-groupoids|fundamental (∞,1)-groupoid]] of the [[topological groupoid]] of [[group homomorphisms]] and [[conjugation|conjugations]].

## Properties

### Relation to $G$-CW-complexes

[[Elmendorf's theorem]] says that for fixed [[topological group]] $G$ we have 

$$
  PSh_\infty(Orb_G) \simeq Top^G([weak\; G-homotopy\,\, equivalences]^{-1})
  \,.
$$

### Relation to topological stacks

By the main theorem of ([Henriques-Gepner 07](#HenriquesGepner07)) the [[(∞,1)-presheaves]] on the global [[orbit category]] are equivalently "cellular" [[topological stacks]]/[[topological groupoids]] ("[[orbispaces]]"), we might write this as

$$
  ETopGrpd^{cell} = PSh_\infty(Orb)
  \,.
$$

(As such that global equivariant homotopy theory should be similar to [[ETop∞Grpd]]. Observe that this is a [[cohesive (∞,1)-topos]] with $\Pi$ such that it sends a topological [[action groupoid]] of a [[topological group]] $G$ acting on a [[topological space]] $X$ to the [[homotopy quotient]] $\Pi(X)//\Pi(G)$.)

The central theorem of ([Rezk 14](#Rezk14)) (using a slightly different definition than [Henriques-Gepner 07](#HenriquesGepner07)) is that $PSh_\infty(Orb)$ is a [[cohesive (∞,1)-topos]] with $\Gamma$ producing homotopy quotients.



## Related concepts

* [[global equivariant stable homotopy theory]]

## References

The global orbit category $Orb$ is considered in 

* {#HenriquesGepner07} [[André Henriques]], [[David Gepner]], _Homotopy Theory of Orbispaces_ ([arXiv:math/0701916](http://arxiv.org/abs/math/0701916))
  

Global unstable equivariant homotopy theory is discussed as a [[localization]] of the category of "orthogonal spaces" (the unstable version of [[orthogonal spectra]]) in chapter I of

* [[Stefan Schwede]], _Global homotopy theory_, 2013 ([pdf](http://www.math.uni-bonn.de/~schwede/global.pdf))

Discussion of the global equivariant homotopy theory as a [[cohesive (∞,1)-topos]] is in 

* {#Rezk14} [[Charles Rezk]], _[[Global Homotopy Theory and Cohesion]]_ (2014)

[[!redirects global homotopy theory]]

[[!redirects global equivariant homotopy category]]