
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

This is similar to [[ETop∞Grpd]], which models cohesion in the form of [[Euclidean topology]].


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

## References

The corresponding 1-[[cohesive topos]] over locally _connected_ topological spaces was considered in

* {#Johnstone11} [[Peter Johnstone]], example 1.5 of _Remarks on punctual local connectedness_, Theory and Applications of Categories, Vol. 25, 2011, No. 3, pp 51-63 ([web](http://www.tac.mta.ca/tac/volumes/25/3/25-03abs.html))

A decent account of the above $\infty$-topos is in prepation by [[David Carchedi]]...

[[!redirects locally contractible topological ∞-groupoid]]
[[!redirects LCTop∞Grpd]]

[[!redirects locally contractible topological infinity-groupoids]]
[[!redirects locally contractible topological ∞-groupoids]]