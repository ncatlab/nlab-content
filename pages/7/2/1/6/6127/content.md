
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

As shown in [[manifold structure of mapping spaces]], the space of [[smooth map]]s from a [[sequentially compact space|sequentially compact]] [[Frölicher space]] (or [[diffeological space|diffeological]] or Chen space) in to a [[smooth manifold]] is again a smooth manifold.  Its [[tangent space]] is straightforward to identify.  A tangent vector is an [[infinitesimal object|infinitesimal]] deviation of a smooth map; that is, it defines a direction in which to deform that map.  As a smooth map is determined by its values at points, when deforming a smooth map it is enough to explain how to deform each point.  Thus a tangent vector at $\alpha \colon S \to M$ defines, for each $p \in S$, a tangent vector at $\alpha(p) \in M$.  Thus we obtain a map $S \to T M$.  It is not unbelievable that this map is again smooth, whence we have:
\[
T C^\infty(S,M) \to C^\infty(S, T M).
\]
The claim of this page is that this is a [[diffeomorphism]], and further a [[vector bundle]] [[isomorphism]], where each is considered a vector bundle over $C^\infty(S, M)$.
