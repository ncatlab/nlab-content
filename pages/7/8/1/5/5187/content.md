
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--


#Context#
* table of contents
{:toc}

## Idea

A _Boardman-Vogt resolution_ or _W-construction_ is a particular choice of cofibrant [[resolution]] of [[Top]]-[[operad]]s. It is closely related to the operation of forming a [[homotopy coherent nerve]].

This generalizes naturally to a cofibrant [[resolution]] in the [[model structure on operads]] of [[operad]]s enriched over any suitable [[monoidal model category]] that is equipped with a suitable [[comonoid]]al [[interval object]]. This general construction subsumes

* the W-construction on topological operads ([BoardmanVogt](#BoardmanVogt));

* the cobar-bar resolution of chain complex operads ([GezlerJones](#GetzlerJones), [GinzburgKapranov](#GinzburgKapranov));

* the Godement simplicial resolution ([Godement](#Godement))

Over [[Top]] the BV-resolution works as follows:

for $P$ a topological operad, its [[free operad]] $F_*(P)$ has as $n$-ary operations all [[tree]]s with $n$ inputs, with each vertex of valence $k+1$ labeled by an element in $P(k)$. Composition is given by [[grafting]] of trees.

The operad $W(P)$ is obtained from this by in addition 

* labeling the inner edges of any tree by [[real number]]s $\ell \in [0,1]$;

* identifying trees one of whose edges has length 0 with the tree with that edge removed and with the correspnding operad-operation labels composed.

There is an evident operad morphism $F_*(P) \to W(P)$ obtained by regarding each edge of a tree as being of length 1, and there is an evident morphism $W(P) \to P$ obtained by forgetting all trees and sending their operad-operation-labels to their composite. 

The composition

$$
  F_*(P) \to W(P) \to P
$$

is the counit of the [[free functor|free]]/forgetful [[adjunction]] between operads and their underlying [[collection]]s and if $P$ is degreewise sufficiently nice, this factors that counit as a cofibration followed by a weak equivalence and exhibits $W(P)$ as a cofibrant [[resolution]] of $P$.

## References

The W-construction on topological operads is in

* [[Michael Boardman]] and [[Rainer Vogt]], _Homotopy invariant algebraic structures on topological spaces_ , Lect. Notes Math. 347 (1973).
{#BoardmanVogt}

The cobar-bar resolution of chain complex operads is in

* [[Ezra Getzler]], J.D.S. Jones, _Operads, homotopy algebra, and iterated integrals for double loop spaces_ , (1995) 
{#GetzlerJones}

* [[Victor Ginzburg]], [[Mikhail Kapranov]], _Koszul duality for operads_ , Duke Math. J. 76 (1994) 203&#8211;272.
{#GinzburgKapranov}

The Godement simplicial resolution is in

* R. Godement, _Topologie alg&#233;brique et th&#233;orie des faisceaux_ , no. 13, Publ. Math. Univ. Strasbourg, Hermann, Paris, 1958.
{#Godement}

The generalization to [[operad]]s enriched in any monoidal category with a suitable interval object is in

* [[Clemens Berger]], [[Ieke Moerdijk]], _The Boardman-Vogt resolution of operads in monoidal model categories_ , Topology 45 (2006), 807&#8211;849. ([pdf](http://math.unice.fr/~cberger/BV.pdf))
{#BergerMoerdijkResolution}


[[!redirects Boardman-Vogt resolutions]]

[[!redirects W-construction]]
[[!redirects W-constructions]]