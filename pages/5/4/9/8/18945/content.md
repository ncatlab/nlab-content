

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Graph theory
+-- {: .hide}
[[!include graph theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

In [[graph theory]] a _multigraph_ a particular type of [[graph]]. A multigraph is a [[set]] of [[vertices]] and for each unordered pair of distinct vertices a set of [[edges]] between these.

The terminology is used in distinction to 

1. _[[simple graphs]]_, which are multigraphs with at most one edge between any unordered pair of distinct vertices;

1. _[[pseudographs]]_, which are like multigraphs but admitted to have "[[loops]]" in the sense of [[edges]] between a vertex and itself.

Beware that the terminology is not completely consistent across different authors. Some authors may allows [[loops]] when they speak of multigraphs.

## Definition


More formally this means that a multigraph is

1. a [[set]] $V$ ("of [[vertices]]");

1. a [[set]] $E$ ("of [[edges]]");

1. a [[function]] $E \to \left\{ {\,\atop \,} \{v_1, v_2\} = \{v_2, v_1\} \;\vert\; v_1, v_2 \in V \,,\; v_1 \neq v_2 {\, \atop \,} \right\}$ (sending any [[edge]] to the unordered pair of distinct [[vertices]] that it goes between).

Specifically a [[finite graph|finite]] multigraph is, after choosing a [[linear order]] on its set of vertices, the same as

1. a [[natural number]] $v \in \mathbb{N}$ (the number of [[vertices]]);

1. for each $i \lt j \in \{1, \cdots, v\}$ a natural number $e_{i,j} \in \mathbb{N}$ (the number of [[edges]] between the $i$th and the $j$th vertex)

## Examples

* In [[perturbative quantum field theory]] the [[graphs]] underlying [[Feynman diagrams]] are [[finite graph|finite]] [[multigraphs]] (e.g. [Borinsky](#Borinsky)).

## References

Discussion with an eye towards [[Feynman diagrams]] includes

* {#Borinsky} Michael Borinsky, section 2.1.1 of _Algorithmization of the Hopf algebra of Feynman graphs_ ([pdf](http://www2.mathematik.hu-berlin.de/~kreimer/wp-content/uploads/BorinskyMaster.pdf))

See also

* Wikipedia, _[Multigraph](https://en.wikipedia.org/wiki/Multigraph)_

[[!redirects multigraphs]]

[[!redirects finite multigraph]]
[[!redirects finite multigraphs]]

