
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Background

+-- {: .num_defn #LocallyCompactSpace}
###### Definition
**([[locally compact topological space]])**

A [[topological space]] $X$ is called _[[locally compact topological space|locally compact]]_
if for every point $x \in X$ and every [[open neighbourhood]] $U_x \supset \{x\}$
there exists a smaller open neighbourhood $V_x \subset U_x$ whose [[topological closure]]
is [[compact topological space|compact]] and still contained in $U$:

$$
  \{x\} \subset V_x \subset \underset{\text{compact}}{Cl(V_x)} \subset U_x
  \,.
$$

=--



## Statement and proof

+-- {: .num_prop #OpenSubspacesOfCompactHausdorffSpacesAreLocallyCompact}
###### Proposition
**(open subspaces of compact Hausdorff spaces are locally compact)**

Every [[open subset|open]] [[topological subspace]] $X \underset{\text{open}}{\subset} K$
of a [[compact topological space|compact]]
[[Hausdorff space]] $K$ is a [[locally compact topological space]].

In particular every [[compact Hausdorff space]] itself is [[locally compact topological space|locally compact]].

=--

+-- {: .proof #ProofOfOpenSubspacesOfCompactHausdorffSpacesAreLocallyCompact}
###### Proof

Let $x \in X$ be a point and let $U_x \subset X$ an [[open neighbourhood]].  We need to produce a small open neighbourhood
whose closure is compact and still contained in $U_x$.

By the nature of the [[subspace topology]] there exists an open subset $V_x\subset K$ such that $U_x = X \cap V_x$.
Since $X$ is assumed to be open, it follows that $U$ is also open as a subset of $K$. 
Since [[compact Hausdorff spaces are normal]] it follows (by [this prop.](Introduction+to+Topology+--+1#T4InTermsOfTopologicalClosures)) that 
there exists a smaller open neighbourhood $W_x \subset K$ whose [[topological closure]] is still contained in $U_x$,
and since [[closed subspaces of compact spaces are compact]]:

$$
  \{x\} \subset W_x \subset \underset{\text{cpt}}{Cl(W_x)} \subset V_x \subset K
  \,.
$$

The intersection of this situation with $X$ is the required smaller compact neighbourhood $Cl(W_x) \cap X$:

$$
  \{x\} \subset W_x \cap X \subset \underset{\text{cpt}}{Cl(W_x)} \cap X \subset U_x \subset X
  \,.
$$


=--

+-- {: .num_remark}
###### Remark

Conversely, every locally compact Haudorff space $X$ arises as in prop. \ref{OpenSubspacesOfCompactHausdorffSpacesAreLocallyCompact}, since it may be considered an [[open subspace]] in its [[one-point compactification]] $X \sqcup \{\infty\}$. See there _[this example](one-point+compactification#LocallyCompatcHausdorffSpaceIsOpenSubspaceOfCompactHausdorffSpace)_.

=--

## Related statements

* [[closed subspaces of compact spaces are compact]]

* [[compact subspaces of Hausdorff spaces are closed]]

* [[closed subspaces of compact Hausdorff spaces are equivalently compact subspaces]]

* [[compact Hausdorff spaces are normal]]

* [[a CW-complex is a Hausdorff space]]

* [[Hausdorff implies sober]]

* [[maps from compact spaces to Hausdorff spaces are closed and proper]]

* [[continuous images of compact spaces are compact]]

[[!redirects locally compact Hausdorff spaces are equivalently open subspaces of compact Hausdorff spaces]]
