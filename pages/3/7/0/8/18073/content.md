
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

## Statement

+-- {: .num_prop #Statement}
###### Proposition

Assuming [[excluded middle]], then: 

Every [[Hausdorff topological space]] is a [[sober topological space]].

More specifically, in a Hausdorff topological space
the [[irreducible closed subspaces]] 
are precisely the [[singleton]] [[subspaces]].

=--

+-- {: .proof #TheProof}
###### Proof

The second statement clearly implies the first. To see the second
statement, suppose that $F$ is an irreducible closed subspace which
contained two distinct points $x \neq y$. Then by the Hausdorff property
there are disjoint neighbourhoods $U_x, U_y$, and hence it would follow that the relative [[complements]] $F \setminus U_x$ and $F \setminus U_y$ were distinct proper closed subsets of
$F$ with

$$
  F = (F \setminus U_x) \cup (F \setminus U_y)
$$

in contradiction to the assumption that $F$ is irreducible. 

This [[proof by contradiction|proves by contradiction]] that every irreducible closed subset is a singleton. 
Conversely, generally the [[topological closure]] of every singleton is irreducible closed.

=--

## Strictness of implication

There are many examples of sober spaces which are not Hausdorff. For example, the spectrum of a ring which is not zero-dimensional is sober but not Hausdorff.

Any Hausdorff space is not only [[sober]], but also $T_1$. However, even the converse to this fails. [For example](https://en.wikipedia.org/wiki/Sober_space), let $X$ be the real line with a new point $p$ added, topologized such that any open set in the real line is open, and any cofinite set containing $p$ is open. Then $X$ is sober and $T_1$ but not Hausdorff.


## Related entries

* [[schemes are sober]]

* [[compact Hausdorff spaces are normal]]

* [[a CW-complex is a Hausdorff space]]

* [[continuous images of compact spaces are compact]]

* [[maps from compact spaces to Hausdorff spaces are closed and proper]]

* [[closed subsets of compact spaces are compact]]

* [[compact subspaces of Hausdorff spaces are closed]]

* [[closed subspaces of compact Hausdorff spaces are equivalently compact subspaces]]



## References

* Topospaces, _[Hausdorff implies sober](https://topospaces.subwiki.org/wiki/Hausdorff_implies_sober)_

[[!redirects Hausdorff spaces are sober]]

[[!redirects every Hausdorff space is a sober space]]
[[!redirects every Hausdorff topological space is a sober topological space]]
