
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

There are a number of slightly different definitions in the literature, this page will try to give a general overarching definition. 

+-- {: .num_prop }
###### Definition

A [[topological groupoid]] $X_1 \stackrel{\overset{s}{\to}}{\underset{t}{\to}} X_0$ is called **locally compact** if the maps $s$ and $t$ are [[locally proper]] [[open maps]].

=--

This is far more general than is usually assumed. One can additionally assume that either $X_1$ is locally compact or $X_0$ is locally compact, or that $X_0$ is Hausdorff or $X_1$ is locally Hausdorff, or that $X_1$ is [[sigma-compact]]

One usually wants to place a [[Haar system on a locally compact groupoid|Haar system]] on a locally compact groupoid. The obvious topological requirement of local compactness is further refined in order to make such a system of measures well-behaved.

## Examples

* Any finite-dimensional [[Lie groupoid]] is locally compact
* The action groupoid of a [[locally compact group]] on a [[locally compact topological space]] is (?should be) a locally compact groupoid.

## References

An early reference is

* Jean Renault, _A Groupoid Approach to C*-Algebras_, Lecture Notes in Mathematics **793** (1980) doi:[10.1007/BFb0091072](https://doi.org/10.1007/BFb0091072)

A version where Hausdorffness is weakened so that only the space of objects is Hausdorff is

* Jean-Louis Tu, _Non-Hausdorff groupoids, proper actions and K-theory_, Documenta Mathematica, Vol. 9 (2004) pp565-597, [journal page](https://www.math.uni-bielefeld.de/documenta/vol-09/26.html), arXiv:[math/0403071](https://arxiv.org/abs/math/0403071)