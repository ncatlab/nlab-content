#Contents#
* the following line creates the automatic table of contents
{:toc}


## Idea ##
In the [[Haag-Kastler approach]] to [[quantum field theory]] one deals with [[local nets]] indexed by bounded open regions of [[Minkowski spacetime]]. An important axiom of this approach is that of causality, which says that observables localized in spacelike separated regions of spacetime commute.
A causal index set is an abstraction of the index set of bounded open regions that retains the relation induced by the concept of spacelike separation. It can be used to generalize the axiom of causality to nets with different or more general index sets as the one mentioned above. 

## Definition ##

A relation $\perp$ on an index set - that is an unbounded [[poset]] - $I$ is called a **causal disjointness relation** (and $a, b \in I$ are called causally disjoint if $a \perp b$) if the following properties are satisfied:

(i) $\perp$ is symmetric

(ii) $a \perp b$ and $c \lt b$ implies $a \perp c$

(iii) if $M \subset I$ is bounded from above, then $a \perp b$ for all $a \in M$ implies $sup M \perp b$.

(iv) for every $a \in I$ there is a $b \in I$ with $a \perp b$

A poset with such a relation is called a **causal index set**. 

## Examples ##
One example is explained in the Idea section.

Let $I$ be the final subspaces of an infinite dimensional, separable [[Hilbert space]]. Define $\perp$ by orthogonality of subspaces, then $(I, \perp)$ is a causal index set.

Let $X$ be an arbitrary set and $I$ be its [[power set]]. Set $M \perp N$ iff $M \cap N = \emptyset$, then this defines a causal disjointness relation. This is an example of a [[causal complement]].
 
[[!redirects causal index sets]]
[[!redirects causal disjointness relation]]
[[!redirects causal disjointness relations]]