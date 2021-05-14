
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
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--



#Context#
* table of contents
{:toc}

## Idea

A _Boardman-Vogt resolution_ or _W-construction_ is a particular choice of cofibrant [[resolution]] of [[topological operads]] (or [[simplicial operads]] or similar). It is closely related to the operation of forming the [[dendroidal homotopy coherent nerve]]. Its restriction to [[Top]]-[[enriched categories]] / [[simplicial categories]] is accordingly closely related to the ordinary [[homotopy coherent nerve]].

The construction is a variant of the _[[free operad]]_ construction, where the free composites of operations are further labeled by "distances" such that for vanishing distance the free composite is replaced with the actual composite.

The original Boardman-Vogt resolution over [[Top]] generalizes naturally to a cofibrant [[resolution]] in the [[model structure on operads]] for operads enriched over any suitable [[monoidal model category]] that is equipped with a suitable [[comonoid|comonoidal]] [[interval object]]. In this general form the construction subsumes

* the W-construction on topological operads ([BoardmanVogt](#BoardmanVogt));

* the cobar-bar resolution of chain complex operads ([GezlerJones](#GetzlerJones), [GinzburgKapranov](#GinzburgKapranov));

* the Godement simplicial resolution ([Godement](#Godement))



## Definition  {#Definition}

### Over $Top$

Over [[Top]] the BV-resolution works as follows:

for $P$ a [[topological operad]], its [[free operad]] $F_*(P)$ has as $n$-ary operations all [[trees]] with $n$ inputs, with each vertex of valence $k+1$ labeled by an element in $P(k)$. Composition is given by grafting of trees.

The operad $W(P)$ is obtained from this by in addition 

* labeling the inner edges of any tree by [[real number]]s $\ell \in [0,1]$;

* identifying trees one of whose edges has length 0 with the tree with that edge removed and with the correspnding operad-operation labels composed.

* equipping the set of labeled trees with the corresponding quotient of the product topology, to make it into a [[topological space]].

There is an evident operad morphism $F_*(P) \to W(P)$ obtained by regarding each edge of a tree as being of length 1, and there is an evident morphism $W(P) \to P$ obtained by forgetting all trees and sending their operad-operation-labels to their composite. 

The composition

$$
  F_*(P) \to W(P) \to P
$$

is the [[unit of an adjunction|counit]] of the [[free functor|free]]/forgetful [[adjunction]] between operads and their underlying [[collection]]s and if $P$ is degreewise sufficiently nice, this factors that counit as a cofibration followed by a weak equivalence and exhibits $W(P)$ as a cofibrant [[resolution]] of $P$.


### General

Write $\mathbb{T}$ for the [[groupoid]] of planar [[trees]] and non-planar [[isomorphism]].

Fix a suitable [[interval object]] $H$, as described at [[model structure on operads]].

For $T$ a [[tree]], write

$$
  H(T) := \bigotimes_{e \in E(T)}H
  \,,
$$

where the tensor product runs over all _internal_ edges of $T$. For $D \subset E(T)$ a subset of internal edges, let

$$
  H_D(T) = \bigotimes_{ E(T)\setminus D} H
  \,.
$$

The acyclic cofibration $0 \to H$ induces an acyclic cofibration

$$
  H_D(T) \hookrightarrow H(T)
$$

and, by the [[pushout-product axiom]], an acyclic cofibration

$$
  H^-(T) := \coprod_{D \neq \emptyset} H_D(T) \hookrightarrow H(T)
  \,.
$$

In a similar fashion, for $P$ an operad, write $P(T)$ for the tensor product of one copy of its objects of $n$-ary operation for each $n$-ary vertex in $T$, and $P^-(T)$ for the coproduct over all such tensor products where at least one, maybe more, _unary_ vertices are omitted. Also the canonical

$$
  P^-(T) \hookrightarrow P(T)
$$

is a cofibration. Consider for each $T$ the [[pushout]]

$$
  \array{
    H^-(T) \otimes P^-(T) &\to& H^-(T) \otimes P(T)
    \\
    \downarrow && \downarrow
    \\
    H(T) \otimes P^-(T) &\to&
    (H \otimes P)^-(T)
  }
  \,.
$$

This induces a univesal morphism

$$
  (H \otimes P)^-(T) \to H(T) \otimes P(T)
$$

and by the [[pushout-product axiom]] in the [[monoidal model category]] $\mathcal{E}$ this, too, is a cofibration.

+-- {: .un_defn}
###### Definition

Define $W(H,P)$ by induction. Start with setting

$$
  W_0(H,P) := P
  \,.
$$

Assume that in each induction step we are given morphisms

$$
  (H(S) \otimes P(S)) \otimes_{Aut(S)} I[\Sigma_n] \to W_{k-1}(H,P)(n)
$$

for all trees $S$ with less than $k$ internal edges. Using the  composition operation in the operad $P$ to compose two operation when the edge connecting them carries no $H$-label, we obtain from this a morphism

$$
  \alpha_T^- : (H \otimes P)^-(T) \otimes_{Aut(T)} I[\Sigma_n] \to W_{k-1}(H,P)(n)
$$


Then in the induction step we define for each $k \in \mathbb{N}$ the object $W_n(H,P)$ by the [[pushout]]

$$
  \array{
     \coprod_{[T], T \in \mathbb{T}(n,k)}
      (H \otimes P)^-(T)
      \otimes_{Aut(T)}
       I[\Sigma_n]
     &\stackrel{\coprod \alpha_T^-}{\to}&
     W_{k-1}(H,P)(n)
     \\
     \downarrow && \downarrow
     \\
     \coprod_{[T], T \in \mathbb{T}(n,k)}
      (H \otimes P)(T)
      \otimes_{Aut(T)}
       I[\Sigma_n]
     &\stackrel{\coprod \alpha_T^-}{\to}&
     W_{k}(H,P)(n)
  }
 \,,
$$

where $\mathbb{T}$ is the subcategory of trees with precisely $n$ inputs and $k$ internal edges.

The bottom morphism we feed back into the induction procedure.

This gives a sequence of collections, and the W-resolution is its [[colimit]]

$$
  W(H,P) := {\lim_{\to}}_k W_k(H,P)
  \,.
$$  

=--

One shows that this collection naturally carries the structure of an operad, etc. pp.

+-- {: .un_remark}
###### Remark

The object $(H \otimes P)(T)$ is to be thought of as the space whose points are tuples consisting of one operation in $P$ per vertex in $T$, of that arity, and of labels in $H$ assigned to the inner edges in $T$.

The object $(H \otimes P)^-(T)$ is a similar space, but where some of the labels on the inner edges are omitted. 

The above pushout identifies points that contain lables of inner edges that are 0 with points in one $W$-stratum below where that edge (or rather its label) is simply omitted and the corresponding operations composed.

=--



## Examples

* [[Jim Stasheff]]'s [[A-∞ operad]] is the relative Boardman-Vogt resolution $W([0,1], I_* \to Assoc)$ of [[Assoc]] in [[Top]] where $I_*$ is the operad for [[pointed object]]s ([Berger-Moerdijk](#BergerMoerdijkAlgebras)).


## References

The W-construction on topological operads is in

* {#BoardmanVogt} [[Michael Boardman]] and [[Rainer Vogt]], _Homotopy invariant algebraic structures on topological spaces_ , Lect. Notes Math. 347 (1973).


The cobar-bar resolution of chain complex operads is in

* {#GetzlerJones} [[Ezra Getzler]], J.D.S. Jones, _Operads, homotopy algebra, and iterated integrals for double loop spaces_ , (1995) 


* {#GinzburgKapranov} [[Victor Ginzburg]], [[Mikhail Kapranov]], _Koszul duality for operads_ , Duke Math. J. 76 (1994) 203&#8211;272.


The Godement simplicial resolution is in

* {#Godement} R. Godement, _Topologie alg&#233;brique et th&#233;orie des faisceaux_ , no. 13, Publ. Math. Univ. Strasbourg, Hermann, Paris, 1958.


The generalization to [[operad]]s enriched in any monoidal category with a suitable interval object is in

*{#BergerMoerdijkResolution}  [[Clemens Berger]], [[Ieke Moerdijk]], _The Boardman-Vogt resolution of operads in monoidal model categories_ , Topology 45 (2006), 807&#8211;849. ([pdf](http://math.unice.fr/~cberger/BV.pdf))


* {#BergerMoerdijkAlgebras} [[Clemens Berger]], [[Ieke Moerdijk]], _Resolution of coloured operads and rectification of homotopy algebras_ ([arXiv:math/0512576](http://arxiv.org/abs/math/0512576))


The Boardman-Vogt-resolution for the operad for [[local nets of observables]] in [[homotopical algebraic quantum field theory]] ([Benini-Schenkel-Woike 17](homotopical+algebraic+quantum+field+theory#BeniniSchenkelWoike17)) is discussed in

* {#Yau18} [[Donald Yau]], _Homotopical Quantum Field Theory_ ([arXiv:1802.08101](https://arxiv.org/abs/1802.08101))


[[!redirects Boardman-Vogt resolutions]]

[[!redirects W-construction]]
[[!redirects W-constructions]]

[[!redirects relative Boardman-Vogt resolution]]


[[!redirects relative Boardman-Vogt resolutions]]