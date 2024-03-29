
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Statement

+-- {: .num_prop}
###### Proposition

Let $f \colon X \longrightarrow Y$ be a [[function]] between [[sets]]. Let $\{S_i \subset Y\}_{i \in I}$ be a set of [[subsets]] of $Y$. Then 

1. $f^{-1}\left( \underset{i \in I}{\cup}  S_i\right) = \left(\underset{i \in I}{\cup} f^{-1}(S_i)\right)$ (the [[pre-image]] under $f$ of a [[union]] of subsets is the union of the pre-images)

1. $f^{-1}\left( \underset{i \in I}{\cap}  S_i\right) \subset \left(\underset{i \in I}{\cap} f^{-1}(S_i)\right)$ (the [[pre-image]] under $f$ of the [[intersection]] of the subsets is the intersection of the pre-images).

=--

For details see at _[[interactions of images and pre-images with unions and intersections]]_.

## Related statements

* [[images preserve unions]]

* [[countable unions of countable sets are countable]]


[[!redirects pre-images preserve intersections]]
