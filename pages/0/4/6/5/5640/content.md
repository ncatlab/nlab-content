
> this page is under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _locally contractible topological ∞-groupoid_ is an [[∞-groupoid]] equipped with [[cohesive (∞,1)-topos|cohesion]] in the form of [[locally contractible topological space|locally contractible]] [[topology]].

The collection of all these cohesive $\infty$-groupoids forms a [[cohesive (∞,1)-topos]] $LCTop\infty Grpd$. 

This is similarr to [[ETop∞Grpd]], which models cohesibion in the form of [[Euclidean topology]].


## Definition

Let $CTop$ be some [[small category|small]] version (...details missing...) of the [[site]] of [[locally contractible topological space|locally contractible]] [[contractible topological spaces]] with [[continuous maps]] betwen them and equipped with the standard [[open cover]] [[coverage]].

This is a [[cohesive site]] (for the evident generalization of that definitions where Cech covers are generalized to hypercovers). The key axiom to check is that for $Y \to U$ a [[hypercover]] of $U \in CTop$ degreewise by a [[coproduct]] of contractibles, also the simplicial set $\lim_\to Y$ obtained by sending each contractible to a point is contractible. This follows as pointed out [on MO here](http://mathoverflow.net/a/187891/381).[^ack] 

[^ack]:Thanks to [[David Carchedi]] for highlighting this.

Define then 

$$
  LCTop\infty Grpd := Sh_{(\infty,1)}(CTop)
$$

to be the [[(∞,1)-category of (∞,1)-sheaves]] on $CTop$. 

This is an [[cohesive (∞,1)-topos]].

$$
  (\Pi \dashv Disc \dashv \Gamma \dashv coDisc) : LCTop\infty Grpd \to \infty Grpd
  \,.
$$

## Related concepts

* [[ETop∞Grpd]]



[[!redirects locally contractible topological ∞-groupoid]]
[[!redirects LCTop∞Grpd]]

[[!redirects locally contractible topological infinity-groupoids]]
[[!redirects locally contractible topological ∞-groupoids]]