
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


# The empty space
* table of contents
{: toc}

## Definition

The **empty space** is the [[topological space]] with no points.  That is, it is the [[empty set]] equipped with its unique topology.


## Properties

### General

The empty space is the ([[strict initial object|strict]]) [[initial object]] in [[TopologicalSpaces]].  

It satisfies all [[separation axiom|separation]], [[compact space|compactness]], and countability conditions ([[separable space|separability]], [[first-countable space|first countability]], [[second-countable space|second-countability]]).  It is also both [[discrete space|discrete]] and [[indiscrete space|indiscrete]], a distinction it shares only with the [[point space]].


### Connectedness

Debate rages over whether the empty space is [[connected space|connected]] (and also [[path-connected space|path-connected]]).  With the common naive definitions that "a space is [[connected topological space|connected]] if it cannot be partitioned into two disjoint nonempty open subsets" and "a space is [[path-connected topological space|path-connected]] if any two points in it can be joined by a path," the empty space is trivially both connected and path-connected.

However, in some ways these definitions are too naive.  The question of whether the empty set is (path-)connected is analogous in many ways to the question of whether $1$ is [[prime number|prime]].  The above definitions are then analogous to saying that "a natural number $p$ is prime if any factor of it is either equal to $1$ or to $p$," according to which $1$ is prime---but there are better definitions that exclude $1$.

For instance, we may say that "$p$ is prime if it has exactly two factors, itself and $1$;" with this definition $1$ is not prime, since it has exactly _one_ factor.   Likewise, we may say that a space is (path-)connected if it has exactly one (path-)[[component]]; with this definition the empty space is not connected, since it has exactly _zero_ components.  (Lest you question that last statement, note that the correct definition of a (path-)component of a space $X$ is as an [[equivalence class]] of points of $X$ under some [[equivalence relation]].  There is a unique equivalence relation on the empty set, and it has _zero_ equivalence classes.)

Here are some other reasons why the empty space should not be considered (path-)connected:


* {#IfItwerePathConnectedDecompositionWouldFail} If the empty space were (path-)connected, unique decomposition into (path-)connected components would fail: $X \sqcup Y = \emptyset \sqcup X \sqcup Y = \dots$.  This is analogous to how if $1$ were a prime, then unique factorization into primes would fail: $6 = 2 \cdot 3 = 1 \cdot 2 \cdot 3 = 1 \cdot 1 \cdot 2 \cdot 3 = \dots$.

* In [[homotopy theory]], one defines a space $X$ to be $k$-connected if $\pi_i(X)$ is trivial (that is, has exactly one element) for $i \le k$.  When $k =0$ this says that $\pi_0(X)$ should have exactly one component---that is, that $X$ should be path-connected.  (Actually, this definition really only makes sense if we phrase it in terms of homotopy [[groupoids]]; homotopy _groups_ are only defined once we choose a basepoint, which is clearly impossible for the empty space.)

* Category-theoretically, one may say that a space $X$ is connected if the [[functor]] $hom(X,-)$ preserves [[coproducts]].  Since $\hom(\emptyset,-)$ is constant at the point, it certainly does not preserve coproducts.

* The statement that a product $X\times Y$ is connected if and only if its components $X$ and $Y$ are connected fails if the empty set is regarded as connected.

* A general result, e.g., in the theory of [[combinatorial species]], is that the [[logarithm]] of [[exponential]] [[generating functions]] of some type of objects should be the exponential generating function for the connected objects of that type. Since this logarithm has no constant term, this suggests the empty object should not count as connected. This result is also known in the physics literature as the linked-cluster theorem (see [this Prop.](geometry+of+physics+--+perturbative+quantum+field+theory#LogarithmEffectiveAction) at _[[geometry of physics -- perturbative quantum field theory]]_).

See [[too simple to be simple]] for general theory.

## Related concepts

[[!include empty objects -- contents]]

* [[Sierpinski space]]

* [[discrete space]]


[[!include universal constructions of topological spaces -- table]]


[[!redirects empty space]]
[[!redirects empty spaces]]

[[!redirects empty topological space]]
[[!redirects empty topological spaces]]
