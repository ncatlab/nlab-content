
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition

The [[action]] of a [[topological group]] $G$ on a [[topological space]] $X$ is called _properly discontinuous_ if every point $x \in X$ has a [[neighbourhood]] $U_x$ such that the [[intersection]] $g(U_x) \cap U_x$ with its translate under the group action via some element $g \in G$ is [[inhabited set|non-empty]] only for the [[neutral element]] $e \in G$:

$$
  g(U_x) \cap U_x \neq \emptyset
  \phantom{AA}
  \Rightarrow
  \phantom{AA}
  g = e
$$

This is equivalent to the condition that the [[quotient space]] [[coprojection]] $X \longrightarrow X/G$ is a [[covering space]]-projection.

Therefore properly discontinuous actions are also called _covering space actions_ ([Hatcher](#Hatcher)).

## Related concepts

* [[proper action]]

* [[transitive action]], [[free action]], [[semi-free action]], [[regular action]]

* [[Clifford-Klein form]]


## References

* Jack Lee, chapter 12 of _Introduction to Topological Manifolds_

* Jack Lee, chapter 21 of _Introduction to Smooth Manifolds_

* Jack Lee, [MO comment](https://math.stackexchange.com/a/1083696/58526), Dec. 2014


* {#Hatcher} [[Alan Hatcher]], _[Algebraic Topology](https://www.math.cornell.edu/~hatcher/AT/ATpage.html)_

[[!redirects properly discontinuous actions]]

[[!redirects covering space action]]
[[!redirects covering space actions]]
