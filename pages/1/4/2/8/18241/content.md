
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Statement

+-- {: .num_prop #OpenClosedContinuousInjectionsAreEmbeddings}
###### Proposition
**(open/closed continuous injections are embeddings)**

A [[continuous function]] $f \colon (X, \tau_X) \to (Y,\tau_Y)$
which is

1. an [[injective function]]

1. an [[open map]] or a [[closed map]]

is a [[topological embedding]].

=--

+-- {: .proof}
###### Proof

If $f$ is injective, then the map onto its [[image]] $X \to f(X) \subset Y$ is a [[bijection]]. Moreover, it is still continuous with respect to the [[subspace topology]] on $f(X)$. Now a bijective continuous function is a homeomorphism precisely if it is an [[open map]] or a [[closed map]] (by [this prop.](homeomorphism#HomeoContinuousOpenBijection)). But the image projection of $f$ has this property, respectively, if $f$ does (by [this prop.](open+map#OpenClosedImageProjection)).

=--

## Related concepts

* [[proper maps to locally compact spaces are closed]]

* [[maps from compact spaces to Hausdorff spaces are closed and proper]]

* [[CW-complexes are Hausdorff spaces]]

* [[Hausdorff spaces are sober]], [[schemes are sober]]

* [[continuous image of a compact space is compact]]

* [[closed subsets of compact spaces are compact]]

* [[compact subspaces of Hausdorff spaces are closed]]

* [[closed subspaces of compact Hausdorff spaces are equivalently compact subspaces]]

* [[quotient projections out of compact Hausdorff spaces are closed precisely if the codomain is Hausdorff]]

* [[paracompact Hausdorff spaces are normal]]

* [[paracompact Hausdorff spaces equivalently admit subordinate partitions of unity]]

[[!redirects open injections are embeddings]]
[[!redirects open/closed injections are embeddings]]
[[!redirects closed/open injections are embeddings]]

