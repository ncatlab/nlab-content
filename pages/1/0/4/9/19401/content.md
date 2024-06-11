
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

* [[John M. Lee]], chapter 12 of: _Introduction to topological manifolds_, Graduate Texts in Mathematics **202**, Springer (2000) &lbrack;ISBN: 0-387-98759-2, 0-387-95026-5&rbrack;
Second edition: Springer (2011) &lbrack;ISBN:978-1-4419-7939-1, [doi:10.1007/978-1-4419-7940-7](https://doi.org/10.1007/978-1-4419-7940-7), errata [pdf](https://sites.math.washington.edu/~lee/Books/ITM/errata.pdf)&rbrack;

* {#Lee12} [[John M. Lee]], chapter 21 of: *Introduction to Smooth Manifolds*, Springer (2012) &lbrack;[doi:10.1007/978-1-4419-9982-5](https://doi.org/10.1007/978-1-4419-9982-5), [book webpage](https://sites.math.washington.edu/~lee/Books/ISM/), [pdf](https://math.berkeley.edu/~jchaidez/materials/reu/lee_smooth_manifolds.pdf)&rbrack;


* [[John Lee]], [MO comment](https://math.stackexchange.com/a/1083696/58526) (Dec. 2014)


* {#Hatcher} [[Alan Hatcher]], _[Algebraic Topology](https://www.math.cornell.edu/~hatcher/AT/ATpage.html)_

[[!redirects properly discontinuous actions]]

[[!redirects covering space action]]
[[!redirects covering space actions]]
