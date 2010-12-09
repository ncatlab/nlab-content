
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The notion of _blob $n$-category_ captures the notion of an [[n-category]] with all duals. It is formulated in the style of [[hyperstructure]]: without any distinction between source and targets.

The definition is well-adapted to describing the [[(∞,n)-category of cobordisms]] in the spirit of [[blob homology]].


## Definition

Let $n \in \mathbb{N}$ be a [[natural number]].

+-- {: .un_defn #BlobGraph}
###### Definition 

A **blob $n$-graph** $C$ is given by

* for every $k \in \mathbb{N}$ a [[functor]] 

  $$
    C_k : core(Ball_k) \to Set
  $$ 

  from the [[groupoid]] of [[topological space]]s [[homeomorphism|homeomorphic]] to a $k$-[[ball]] and [[homeomorphism]]s between them to [[Set]].

=--

We think of $C(B^k)$ as the set of [[k-morphism]]s in the $n$-graph $C$. This means that the [[geometric shape for higher structures]] used here is the [[globe]]. Therefore the term _blob_ . 

We define now a notion of composition on $k$-cells of a blob $n$-graph by induction over $k$. Given a blob $n$-graph with composition for $k$-cells, it can be extended from balls to arbitrary manifolds by the definition [extension to general shapes](#ExtensionToGeneralShapes) below.

+-- {: .un_defn}
###### Definition (roughly)

Say that a blob $n$-graph is a **blob $n$-graph with composition for 0-cells**. 

Assume we have a blob $n$-graph $C$ with composition for $(k-1)$-cells for $k \geq 1$. Then **composition of $k$-cells** on $C$ is a choice of the following structure

* a [[natural transformation]] -- **boundary restriction** 
  (source/target)
 
  $$
    \partial : C_k(X) \to \underset{\to}{C}_{k-1}(\partial X)
    \,,
  $$

  where on the right we have the extension to $(k-1)$ spheres of $C_{k-1}$
  described [below](#ExtensionToGeneralShapes);

* for all balls $B = B_1 \cup_{B_1 \cap B_2} B_2$ and $E := \partial (B_1 \cap B_2)$ a natural transformation -- **composition**

  $$
    \circ : C(B_1) \times_{C(B_1 \cap B_2)} C(B_2) \to C(B)
  $$

  satisfying some compatibility conditions

* for all balls $X$, $D$ a natural map -- **identity** --

  $$
    C(X) \to C(X \times D)
  $$

  satisfying some compatibility conditions.

=--

+-- {: .un_defn #ExtensionToGeneralShapes}
###### Definition (roughly)
**(extension to general shapes)**

For $C$ a blob $n$-graph with composition for $(k-1)$-cells and $X$ any $(k-1)$-[[dimension]]al [[manifold]] with $k \lt n$, define $\underset{\to}{C}_{k-1}(X)$ to be  the [[colimit]]

$$
  \underset{\to}{C}_{k-1}(X) := {\lim_{\to}}_{({\coprod_i U_i \to X})} 
   \left( fiber\;product\;of\;C_{k-1}(U_i)s\;over\;joint\;boundary\;labels \right)
$$

over the category of _permissible decompositions_ (...) of $X$, where the composition operation in $C$ is used to label refinements of permissible decompositions.

=--

This is ([MorrisonWalker, def. 6.3.2](#MorrisonWalker)).


## Examples

+-- {: .un_defn}
###### Definition

For $X$ a [[topological space]], its **fundamental blob $n$-category** $\Pi_{\leq n}(X)$ is the blob $n$-category which sends a $k$-ball for $k \lt n$ to the set of [[continuous map]] of the ball into $X$, and an $n$-ball to the set of [[homotopy]]-classes of such maps, relative boundary.

=--

This is ([MorrisonWalker, example 6.2.1](#MorrisonWalker))).

+-- {: .un_defn}
###### Definition

For $n \in \mathbb{N}$ the **blob $n$-category of $n$-dimensional [[cobordism]]s** $Bord_n$ is the blob $n$-category that sends a $k$-ball $B$ for $k \lt n$ to the set of $k$-dimensional submanifolds $W \hookrightarrow B \times \mathbb{R}^\infty$ such that the projection $W \to B$ is transverse to $\partial B$. An $n$-ball is sent to homeomorphism classes rel boundary of such submanifolds.

=--

This is ([MorrisonWalker, example 6.2.6](#MorrisonWalker))).


## References

Section 6 of

* [[Scott Morrison]], [[Kevin Walker]], _The blob complex_, ([arxiv/1009.5025](http://arxiv.org/abs/1009.5025)) ([website](http://tqft.net/blobs))  
{#MorrisonWalker}
