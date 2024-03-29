
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

+-- {: .num_prop #CompactSubspacesOfHausdorffSpacesAreClosed}
###### Proposition

A [[compact subspace]] $K$ of a [[Hausdorff topological space]] $X$ is a [[closed subspace]].

=--

+-- {: .proof}
###### Proof

Let $x \in X \backslash K$ be any point of $X$ not contained in $K$. We need to show that there exists an [[open neighbourhood]] of $x$ in $X$ which does not [[intersection|intersect]] $K$.

By assumption that $X$ is Hausdorff, there exist for each $y \in K$ disjoint open neighbourhoods $y \subset U_y \subset X$ and $x \subset V_y \subset X$. Clearly the [[union]] of all the $U_y$ is an [[open cover]] of $K$

$$
  K \subset \underset{y \in K}{\cup} U_y
  \,.
$$

Hence by assumption that $K$ is compact, there exists a [[finite set|finite]] [[subset]] $S \subset K$ of points in $K$ such that the $U_s$ for $s \in S$ still cover $K$:


$$
  K \subset \underset{y \in S \subset K}{\cup} U_y
  \,.
$$

Since $S$ is finite, the intersection

$$
  U_x \coloneqq  \underset{y \in S \subset K}{\cap} V_y
$$

is still open, and by construction it is disjoint from all $U_y$ for $y \in S$, hence in particular disjoint from $K$, and it contains $x$. Hence $U_x$ is an open neighbourhood of $x$ as required.

=--

## Remarks

+-- {: .num_defn #NecessityOfHausdorffAssumption}
###### Remark

The statement of prop. \ref{CompactSubspacesOfHausdorffSpacesAreClosed} does not hold with the Hausdorff condition replaced by weaker [[separation axioms|separation assumptions]].

To see this, consider a [[dense subspace]] of a topological space. For instance the [[affine scheme]] [[Spec(Z)]] is $T_1$ but the conclusion of the proposition does not hold for the [[generic point]].

=--



## Related entries

* [[closed subsets of compact spaces are compact]]

* [[closed subspaces of compact Hausdorff spaces are equivalently compact subspaces]]

* [[continuous images of compact spaces are compact]]

* [[a CW-complex is a Hausdorff space]]

* [[Hausdorff implies sober]]

* [[maps from compact spaces to Hausdorff spaces are closed and proper]]

## References

* ProofWiki, _[Compact Subspace of Hausdorff Space is Closed](https://proofwiki.org/wiki/Compact_Subspace_of_Hausdorff_Space_is_Closed)_


