
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

The _empty graph_ is the [[graph]] with [[empty set]] of [[vertices]] and [[empty set]] of [[edges]].

## Properties

The empty graph is the [[initial object]] in any reasonable [[category]] of [[graphs]] (such as a [[category of simple graphs]]).

The [[free category]] on the empty graph is the [[empty category]].

## Some notions of non-empty graphs

For concreteness let us consider the topos of [[quiver|quivers]]. The _inhabited_ graphs, i.e. those satisfying $\top\vdash \exists _x\top$ are precisely the graphs $G$ having an edge since the formula on the right is interpreted as the image of the composite $G\overset{id}{\hookrightarrow} G\to 1$ but $1$ being the loop graph and in order to validate the sequent, its loop must be contained in the image requiring an edge in the source. This notion of being inhabited is stronger than being non-empty $\neq\empty$ but weaker as _having a (global) element_ $1\to G$ which corresponds to graphs containing a loop. A _uninhabited_ graph satisfying $\exists x\top\vdash \bot$ is necessarily empty whence edgeless graphs with a node are internally neither inhabited nor uninhabited.

## Related concepts

[[!include empty objects -- contents]]



[[!redirects empty graphs]]