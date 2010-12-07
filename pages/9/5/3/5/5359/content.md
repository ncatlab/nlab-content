
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

The definition is well-adapted to describing the [[(infinity,n)-category of cobordisms]] in the spirit of [[blob homology]].

## Definition

Let $n \in \mathbb{N}$ be a [[natural number]].

+-- {: .un_defn}
###### Definition (roughly)

A **blob $n$-category** $C$ is given by

* for every $k \in \mathbb{N}$ a [[functor]] 

  $$
    C_k : core(Balls_k) \to Set
  $$ 

  from the [[groupoid]] of [[topological space]]s [[homeomorphism|homeomorphic]] to a $k$-[[ball]] and [[homeomorphism]]s between them to [[Set]];

* for each $k$ a [[natural transformation]]
 
  $$
    \partial : C_k(X) \to \underset{\to}{C}_{k-1}(\partial X)
    \,,
  $$

  where 

  $$
    \underset{\to}{C}_{k-1}(X) := {\lim_\to}_{U \hookrightarrow S^{k-1}} C_{k-1}(U)
  $$

  is the [[colimit]] of $C_{k-1}$ over the category of open balls in the $(k-1)$-[[sphere]]


* for all balls $B = B_1 \cup_{B_1 \cap B_2} B_2$ and $E := \partial (B_1 \cap B_2)$ a natural transformation -- **composition**

  $$
    \circ : C(B_1) \times_{C(B_1 \cap B_2)} C(B_2) \to C(B)
  $$

  satisfying some compatibility conditions

* for all balls $X$, $D$ a natural map -- **identity** --

  $$
    C(X) \to C(X \times D)
  $$

  satisfying some compatibility conditions  

=--

## Examples

* Fundamental $n$-category of a topological space

  For $X$ a [[topological space]], let $\Pi_{\leq n}(X)$ be the blob $n$-category which sends a $k$-ball for $k \lt n$ to the set of [[continuous map]] of the ball into $X$, and an $n$-ball to the set of [[homotopy]]-classes of such maps, relative boundary.

  This is ([MorrisonWalker, example 6.2.1](#MorrisonWalker))).

* bordism $n$-category

  The blob $n$-category $Bord_n$ of $n$-dimensional [[cobordism]]s sends a $k$-ball $B$ for $k \lt n$ to the set of $k$-dimensional submanifolds $W \hookrightarrow B \times \mathbb{R}^\infty$ such that the projection $W \to B$ is transverse to $\partial B$. An $n$-ball is sent to homeomorphism classes rel boundary of such submanifolds.

  This is ([MorrisonWalker, example 6.2.6](#MorrisonWalker))).


## References

Section 6 of

* [[Scott Morrison]], [[Kevin Walker]], _The blob complex_, ([arxiv/1009.5025](http://arxiv.org/abs/1009.5025)) ([website](http://tqft.net/blobs))  
{#MorrisonWalker}
