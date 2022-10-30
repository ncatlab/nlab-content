[[!redirects Reissner-Nordstrom spacetime]]


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Gravity
+--{: .hide}
[[!include gravity contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The Reissner-Nordstr&#246;m solution to the [[equations of motion]] of [[Einstein-Maxwell theory]] describes the [[spacetime]] outside of a [[electric charge|electrically charged]] (and/or [[magnetic charge|magnetically charged]]) point [[mass]], hence describes a _charged_ [[black hole]].

## Metric

For [[mass]] $M$, [[electric charge]] $Q$ and [[magnetic charge]] $P$ the [[pseudo-Riemannian metric]] for the Reissner-Nordstr&#246;m spacetime is, in [[polar coordinates]] $(t,r,\phi,\theta)$ on $\mathbb{R}^4 - \{0\} = \mathbb{R} \times \mathbb{R}_{\gt 0} \times S^2$, given by

$$
  ds^2_{M,Q,P} \coloneqq - H d t^2 + H^{-1} d r^2 + r^2 ds_{S^2}^2
$$

where

$$
  H \coloneqq 1 - G \frac{M}{r} + G \frac{Q^2 + P^2}{r^2}
  \,.
$$

The corresponding [[Faraday tensor]]/electromagnetic [[field strength]] [[curvature|curvature 2-form]] is

$$
  F = \frac{Q}{r^2} d t \wedge d r + P \sin(\theta) d\theta \wedge d\phi
  \,.
$$

> (check sign)

## Horizons

The function $H$ above vanishes at

$$
  r_{\pm} 
    \coloneqq 
  \tfrac{G}{2}\left(
    M \pm \sqrt{M^2 - 4 (P^2 + Q^2)}
  \right)
  \,.
$$

The larger of the two solutions is an [[event horizon]], the other is a [[Cauchy horizon]]. In the case that they coincide, for $M = 2sqrt{Q^2 + P^2}$, one speaks of an [[extremal black hole]].

## Related concepts

* [[no-hair theorem]]

[[!include charged and rotating black holes -- table]]

## References

Review includes

* Mammadov, _Reissner-Nordstr&#246;m metric_ ([pdf](http://gmammado.mysite.syr.edu/notes/RN_Metric.pdf))
 
* Wikipedia, _[Reissner-Nordstr&#246;m metric](https://en.wikipedia.org/wiki/Reissner&#8211;Nordstr&#246;m_metric)_



[[!redirects charged black hole]]
[[!redirects charged black holes]]