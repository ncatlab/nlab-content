
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Mapping space
+--{: .hide}
[[!include mapping space - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea ##

As shown in [[manifolds of mapping spaces]], the space of [[smooth map]]s from a [[sequentially compact space|sequentially compact]] [[Froelicher space|Frölicher]] (or [[diffeological space|diffeological]] or [[Chen space|Chen]]) space is again a smooth manifold.  As such, its [[topology]] can be determined by considering how the [[coordinate chart|chart]]s are glued together.

In some cases, there is an easy method available to study the topology.  If the target manifold, say $M$, [[embedding|embeds]] as a [[submanifold]] of some [[convenient vector space]], say $V$, then $C^\infty(S,M)$ embeds as a submanifold of $C^\infty(S,V)$.  If the original embedding is as a closed submanifold, so is the embedding of mapping spaces.  This means that it is possible to propagate topological results down from $C^\infty(S,V)$ to $C^\infty(S,M)$.  Furthermore, if $M$ is a [[deformation retract]] of a neighbourhood of its image in $V$, then so is $C^\infty(S,M)$ in $C^\infty(S,V)$.

## Embeddings ##

+--{: .num_theorem #embedding}
###### Theorem
Let $g \colon M \to N$ be an embedding of smooth manifolds.  Let $S$ be a sequentially compact Fr&#246;licher space.  Then $C^\infty(S,g) \colon C^\infty(S,M) \to C^\infty(S,N)$ is an embedding of smooth manifolds.
=--


## Related entries

* [[compact-open topology]]

* [[differential topology of mapping spaces]]

  * [[C-k topology]]

