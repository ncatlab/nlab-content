
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

+-- {: .num_lemma #SeparationByNeighbourhoodsOfPointsFromCompactSubsetsInHausdorffSpaces}
###### Lemma
**(compact subspaces in Hausdorff spaces are separated by neighbourhoods from points)**

Let

1. $(X,\tau)$ be a [[Hausdorff topological space]];

1. $Y \subset X$ a [[compact topological space|compact]] [[subspace]].


Then for every $x \in X \backslash Y$ there exists

1. an [[open neighbourhood]] $U_x \supset \{x\}$;

1. an open neighbourhood $U_Y \supset Y$

such that

* they are still disjoint: $U_x \cap U_Y = \emptyset$.

=--

As a direct consequence [[compact subspaces of Hausdorff spaces are closed]].

+-- {: .proof}
###### Proof

By the assumption that $(X,\tau)$ is Hausdorff, we find for every point $y \in Y$ disjoint open neighbourhoods $U_{x,y} \supset \{x\}$ and $U_y \supset \{y\}$. By the nature of the [[subspace topology]] of $Y$, the restriction of all the $U_y$ to $Y$ is an [[open cover]] of $Y$:

$$
  \left\{
    (U_y \cap Y) \subset Y
  \right\}_{y \in Y}
  \,.
$$

Now by the assumption that $Y$ is compact, there exists a finite subcover, hence a [[finite set]] $S \subset Y$ such that

$$
  \left\{
    (U_y \cap Y) \subset Y
  \right\}_{y \in S \subset Y}
$$

is still a cover.

But the finite intersection

$$
  U_x \coloneqq \underset{s \in S \subset Y}{\cap} U_{x,s}
$$

of the corresponding open neighbourhoods of $x$ is still open, and by construction it is disjoint from all the $U_{s}$, hence also from their union

$$
  U_Y \coloneqq \underset{s \in S \subset Y}{\cup}  U_s
  \,.
$$


Therefore $U_x$ and $U_Y$ are two open subsets as required.

=--


