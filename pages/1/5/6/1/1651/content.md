
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

## Definition

A [[topological space]] is called **locally path-connected** if it has a [[basis of the topology|basis]] of [[path-connected space|path-connected]] [[neighbourhoods]]. In other words, if for every point $x$ and [[neighbourhood]] $V \ni x$, there exists a path-connected neighbourhood $U \subset V$ that contains $x$.



## Properties

+-- {: .num_lemma #InLocallyPathConnectedSpaceThePathConnectedComponentsAreOpen}
###### Lemma

Let $X$ be a locally path connected space. Then the path connected component $P_x \subset X$ over any point $x \in X$ is an [[open set]]. 

=--

+-- {: .proof}
###### Proof

It is sufficient to show that every point $y \in P_x$ has a [[neighbourhood]] $U_y$ which is still contained in $P_x$. But by local path connectedness, $y$ has a neighbourhood $V_y$ which is path connected. It follows by concatenation of paths that $V_y \subset P_x$.

=--


A locally path-connected space is [[connected space|connected]] if and only if it is [[path-connected topological space|path-connected]].  


+-- {: .num_prop #ForLocallyPathConnectedTheConnectedComponentsCoincideWithThePathConnectedComponents}
###### Proposition

The [[connected components]] of a locally path-connected space are the same as its path-connected components.

=--

+-- {: .proof}
###### Proof

A path connected component is always connected ([this lemma](connected+space#ConnectedPathConnectedSpace)), and in a locally path-connected space is it also open (lemma \ref{InLocallyPathConnectedSpaceThePathConnectedComponentsAreOpen}).
This means that every path-connected component is also connected.


Conversely, it is now sufficient to see that every connected component is path-connected. Suppose it were not, then it would be covered by 
more than one disjoint non-empty path-connected components. 
But by lemma \ref{InLocallyPathConnectedSpaceThePathConnectedComponentsAreOpen} these
would be all open. This would be in contradiction with the assumption that 
$U$ is connected. Hence we have a [[proof by contradiction]].

=--

## Examples

+-- {: .num_example #LocallyPathConnectedEuclideanSpace}
###### Examples
**([[Euclidean space]] is locally path-connected)**

For $n \in \mathbb{N}$ then [[Euclidean space]] $\mathbb{R}^n$ (with its [[metric topology]]) is locally path-connected, since each [[open ball]] is [[path-connected topological space]].

Similarly the [[open intevals]], [[closed intervals]] and [[half-open intervals]], regarded as [[topological subspaces]] of the [[Euclidean space|Euclidean]] [[real line]], are locally path connected.

=--

+-- {: .num_example}
###### Example
**(open subspace of locally path-connected space is locally path connected)**


Every [[open subset|open]] [[subspace]] of a locally path connected topological space is itself locally path connected.

=--

+-- {: .num_example #LocallyPathConnectedCircle}
###### Example
**([[circle]] is locally path-connected)**

The [[Euclidean space|Euclidean]] [[circle]] 

$$
  S^1 = \left\{ x \in \mathbb{R}^2 \;\vert\;  {\Vert x\Vert} = 1\right\}
  \subset \mathbb{R}^2
$$

is locally path connected.

=--

+-- {: .proof}
###### Proof

By definition of the [[subspace topology]] and the defining [[topological base]] of the [[Euclidean plane]], a [[base for a topology|base for the topology]] of $S^1$ is given by the [[images]] of [[open intervals]] under the [[local homeomorphism]]

$$
  (cos(-), sin(-)) \;\colon\; \mathbb{R}^1 \to S^1
  \,.
$$

But these open intervals are locally path connected by example \ref{LocallyPathConnectedEuclideanSpace}, and in fact they are, evidently [[path-connected topological space]].

=--


## Related concepts

The condition is a necessary assumption in the 

* [[fundamental theorem of covering spaces]]

in the form of the condition for

* [[semi-locally simply connected topological spaces]]

[[!redirects locally path-connected space]]
[[!redirects locally path-connected spaces]]
[[!redirects locally path connected space]]
[[!redirects locally path connected spaces]]
[[!redirects locally path-connected topological space]]
[[!redirects locally path-connected topological spaces]]

[[!redirects locally path-connected]]
[[!redirects locally path connected]]
