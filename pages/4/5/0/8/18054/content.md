+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Model theory
+-- {: .hide}
[[!include model theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea
The _countable random graph_, also known as the _Rado graph_, is the "generic finite [[graph]]": it contains every finite graph as an induced subgraph, models the almost-sure first-order theory of the class of finite graphs, and is axiomatized by the _extension property_: given any two finite subsets of vertices, there exists a vertex not in either subset which is connected to all the points in one subset and disconnected from the other.

## Definition
The usual probabilistic construction is given by taking a countably infinite set of vertices and percolating the edges: for any pair of vertices, connect them with probability $\frac{1}{2}$; almost surely the end result will be _the_ countable random graph, which is unique up to isomorphism.

## Remarks
- The extension property implies that every formula in the random graph has infinite [[Vapnik–Chervonenkis dimension]].

- Here is an example of a way that the automorphisms of a first-order structure are not generally captured by its theory: a finite graph will almost surely have no nontrival automorphisms while the countable random graph is $\omega$-categorical and thus has infinitely many nontrivial automorphisms.

## Related concepts
[[omega-categorical structure]]

## References
- P.J. Cameron, [The Random Graph](http://math.ipm.ac.ir/combin/useful_material/Cameron-Rgraphs.pdf)

[[!redirects Rado graph]]
[[!redirects countable random graphs]]
