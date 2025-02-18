+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

Let $(X, \tau)$ be a [[topological space]], and $x \in X$ a point. A _neighborhood base_ at $x$ is a collection $\{U_i \subset X\}_{i \in I}$ of [[neighbourhoods]] of $x$ such that every [[neighborhood]] $W$ of $x$ (which WLOG we may assume open) contains some $U_i$:

$$
  \underset{ { W \underset{\text{open}}{\subset} X } \atop { W \supset \{x\} }   }{\forall}
  \left(
    \underset{i \in I}{\exists}
    \left(
       U_i \subset W
    \right)
  \right)
  \,.
$$

## Related concepts

* [[base of a topology]]

* [[locally compact topological space]]

## References

See also

* Wikipeda, _[Neighbourhood system -- Basis](https://en.wikipedia.org/wiki/Neighbourhood_system#Basis)_

[[!redirects local base]]
[[!redirects local basis]]
[[!redirects local bases]]

[[!redirects neighborhood bases]]
[[!redirects neighborhood basis]]

[[!redirects neighbourhood base]]
[[!redirects neighbourhood bases]]
[[!redirects neighbourhood basis]]

[[!redirects base of neighbourhoods]]
[[!redirects basis of neighbourhoods]]
[[!redirects bases of neighbourhoods]]

[[!redirects base of neighborhoods]]
[[!redirects basis of neighborhoods]]
[[!redirects bases of neighborhoods]]

[[!redirects fundamental system of neighborhoods]]
[[!redirects fundamental systems of neighborhoods]]
[[!redirects fundamental system of neighbourhoods]]
[[!redirects fundamental systems of neighbourhoods]]
