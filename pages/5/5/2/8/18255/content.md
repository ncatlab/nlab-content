
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Statement

+-- {: .num_prop #InjectiveProperMapsAreEquivalentlyTheClosedEmbeddings}
###### Proposition
**(injective proper maps to locally compact spaces are equivalently the closed embeddings)**

Let

1. $X$ be a [[topological space]]

1. $Y$ a [[locally compact topological space]]

1. $f \colon X \to Y$ be a [[continuous function]].

Then the following are equivalent

1. $f$ is an [[injective function|injective]] [[proper map]],

1. $f$ is a closed [[embedding of topological spaces]].

=--

+-- {: .proof}
###### Proof

In one direction, if $f$ is an injective proper map,
then since [[proper maps to locally compact spaces are closed]], it follows that $f$ is also  [[closed map]]. The claim then follows since [[closed injections are embeddings]], and since the image of a closed map is closed.

Conversely, if $f$ is a closed embedding, we only need to show that the embedding map is proper. So for $C \subset Y$ a [[compact subspace]], we need to show that the [[pre-image]] $f^{-1}(C) \subset X$ is also compact. But since $f$ is an injection (being an embedding), that pre-image is just the intersection $f^{-1}(C) \simeq C \cap f(X)$. By the nature of the [[subspace topology]], this is compact if $C$ is.

=--

## Related statements

* [[closed injections are embeddings]]

* [[proper maps to locally compact spaces are closed]]



