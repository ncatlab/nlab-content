[[!redirects closed subsets of compact spaces are compact]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Statement

+-- {: .num_prop #ClosedSubsetsOfCompactSpacesAreCompact}
###### Proposition

Let $(X,\tau)$ be a [[compact topological space]], and let $Y \subset X$ be a  [[closed subspace|closed]] [[topological subspace]]. Then also $Y$ is [[compact topological space|compact]].

=--

+-- {: .proof}
###### Proof

Let $\{V_i \subset Y\}_{i \in I}$ be an [[open cover]] of $Y$. We need to show that this has a finite sub-cover.

By definition of the [[topological subspace|subspace topology]], there exist open subsets $U_i$ of $X$ with 

$$
  V_i = U_i \cap Y
  \,.
$$

By the assumption that $Y$ is closed, the [[complement]] $X \setminus Y$ is an open subset of $X$, and therefore

$$
  \{ X \setminus Y \subset X\} \cup \{ U_i \subset X \}_{i \in I}
$$

is an [[open cover]] of $X$. Now by the assumption that $X$ is compact, this latter cover has a finite subcover,
hence there exists a [[finite set|finite]] [[subset]] $J \subset I$ such that 

$$
  \{ X \setminus Y \subset X\} \cup \{ U_i \subset X \}_{i \in J \subset I}
$$

is still an open cover of $X$, hence in particular intersects to a finite open cover of $Y$. 
But since $Y \cap ( X \setminus Y ) = \empty$, it follows that indeed

$$
  \{V_i \subset Y\}_{i \in J \subset I}
$$

is a cover of $Y$, and in indeed a finite subcover of the original one.

=--


## Related statements

* [[compact subspaces in Hausdorff spaces are separated by neighbourhoods from points]]

* [[open subspaces of compact Hausdorff spaces are locally compact]]

* [[compact subspaces of Hausdorff spaces are closed]]

* [[closed subspaces of compact Hausdorff spaces are equivalently compact subspaces]]

* [[compact Hausdorff spaces are normal]]

* [[a CW-complex is a Hausdorff space]]

* [[Hausdorff implies sober]]

* [[maps from compact spaces to Hausdorff spaces are closed and proper]]

* [[continuous images of compact spaces are compact]]
