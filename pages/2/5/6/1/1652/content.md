
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A [[topological space]] $X$ is _(semi-)locally simply connected_ if every [[neighborhood]] of a point has a subneighbourhood in which [[loops]] based at the point in the subneighborhood can be contracted in $X$. It is similar to but weaker than the condition that every neighborhood of a point has a subneighborhood that is [[simply connected]]. This latter condition is called _local simple-connectedness_. 

## Definition

A [[topological space]] $X$ is **semi-locally simply-connected** if it has a basis of [[neighbourhood]]s $U$ such that the inclusion $\Pi_1(U) \to \Pi_1(X)$ of [[fundamental groupoid]]s factors through the canonical functor $\Pi_1(U) \to codisc(U)$ to the [[codiscrete groupoid]] whose objects are the elements of $U$. The condition on $U$ is equivalent to the condition that the homomorphism $\pi_1(U, x) \to \pi_1(X, x)$ of [[fundamental group]]s induced by inclusion $U \subseteq X$ is trivial. 

* A semi-locally simply connected space need not be locally simply connected. For a simple counterexample, take the cone on the [[Hawaiian earring space]].

## Examples


+-- {: .num_example #LocallySimplyConnectedCircle}
###### Example
**([[circle]] is locally simply connected)**

The [[Euclidean space|Euclidean]] [[circle]] 

$$
  S^1 
   \;=\; 
  \big\{ 
    x \in \mathbb{R}^2 
    \;\big\vert\;  
    {\Vert x\Vert} = 1
  \big\}
  \;\subset\; 
  \mathbb{R}^2
$$

is locally simply connected

=--

+-- {: .proof}
###### Proof

By definition of the [[subspace topology]] and the defining [[topological base]] of the [[Euclidean plane]], a [[base for a topology|base for the topology]] of $S^1$ is given by the [[images]] of [[open intervals]] under the [[local homeomorphism]]

$$
  \big(cos(-), sin(-)\big) 
    \;\colon\; 
  \mathbb{R}^1 \longrightarrow S^1
  \,.
$$

But these open intervals are simply connected ([this example](fundamental+group#EuclideanSpaceFundamentalGroup)).

=--

* A semi-locally simply connected space need not be locally simply connected. For a simple counterexample, take the cone on the [[Hawaiian earring space]]. 

## Application 

Semi-local simple connectedness is the crucial condition needed to have a good theory of [[covering space]]s, to the effect that the topos of permutation representations of the fundamental groupoid of $X$ is equivalent to the category of covering spaces of $X$.

This is the _[[fundamental theorem of covering spaces]]_, see there for more.

## In topos theory

For a [[topos]]-theoretic notion of locally $n$-connected see [[locally n-connected (infinity,1)-topos]].

## Related concepts

* [[locally path-connected topological space]]


[[!redirects semi-locally simply-connected topological spaces]]

[[!redirects semi-locally simply connected space]]
[[!redirects semi-locally simply connected spaces]]
[[!redirects semi-locally simply-connected space]]
[[!redirects semi-locally simply-connected spaces]]
[[!redirects semi-locally simply connected topological space]]
[[!redirects semi-locally simply connected topological spaces]]
[[!redirects semi-locally simply-connected topological space]]
[[!redirects semi-locally simply-connected topological spaces]]

[[!redirects semilocally simply connected space]]
[[!redirects semilocally simply connected spaces]]
[[!redirects semilocally simply-connected space]]
[[!redirects semilocally simply-connected spaces]]
[[!redirects semilocally simply connected topological space]]
[[!redirects semilocally simply connected topological spaces]]
[[!redirects semilocally simply-connected topological space]]
[[!redirects semilocally simply-connected topological spaces]]

[[!redirects locally simply connected space]]
[[!redirects locally simply connected spaces]]

[[!redirects locally simply-connected space]]
[[!redirects locally simply-connected spaces]]

[[!redirects locally simply connected topological space]]
[[!redirects locally simply connected topological spaces]]

[[!redirects locally simply-connected topological space]]
[[!redirects locally simply-connected topological spaces]]