+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

**shrinkable map** $\Rightarrow$ [[Dold fibration]]

#Contents#
* automatic table of contents goes here
{:toc}

## Definition

A _shrinkable map_ $p:X \to Y$ in the [[category]] [[Top]] is a map with a section $s:Y \to X$ such that $s\circ p:X \to X$ is vertically homotopic to $id_X$ (i.e. is homotopic to $\id_X$ in the slice category $Top/Y$). In particular, a shrinkable map is a homotopy equivalence. 

## Properties

Every shrinkable map is a [[Dold fibration]].

## Examples

**Example:**(Segal) Let $U_i \to Y$ be a [[numerable open cover]]. Then the [[geometric realization]] of the [[Cech nerve]] $N\check{C}(U_i)$ comes with a canonical map $|N\check{C}(U_i)| \to Y$ which is shrinkable.

There are extensions of this to other categories with a notion of homotopy.

## References

This definition is due to Dold, in his 1963 _Annals_ paper _Partitions of unity in the theory of fibrations_.

[[!redirects shrinkable]]