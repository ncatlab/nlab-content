
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

## Statement

+-- {: .num_defn #CompactHausdorffSpacesAreNormal}
###### Proposition

Every [[compact Hausdorff topological space]] is a [[normal topological space]].

=--

In fact a stronger statement holds: [[paracompact Hausdorff spaces are normal]].


To prove this, consider the following lemma:

+-- {: .num_lemma #SeparationByNeighbourhoodsOfPointsFromCompactSubsetsInHausdorffSpaces}
###### Lemma
**(separation by neighbourhoods of points from compact subspaces in Hausdorff spaces)**

Let 

1. $(X,\tau)$ be a [[Hausdorff topological space]];

1. $Y \subset X$ a [[compact topological space|compact]] [[subspace]].


Then for every $x \in X \backslash Y$ there exists 

1. an [[open neighbourhood]] $U_x \supset \{x\}$;

1. an open neighbourhood $U_Y \supset Y$

such that

* they are still disjoint: $U_x \cap U_Y = \emptyset$.

=--

+-- {: .proof}
###### Proof
of lemma \ref{SeparationByNeighbourhoodsOfPointsFromCompactSubsetsInHausdorffSpaces}

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
  U_x \coloneqq \underset{s \in S \subset Y}{\bigcap} U_{x,s}
$$

of the corresponding open neighbourhoods of $x$ is still open, and by construction it is disjoint from all the $U_{s}$, hence in particular from their union

$$
  U_Y \coloneqq \underset{s \in S \subset Y}{\bigcup}  U_s
  \,.
$$


Therefore $U_x$ and $U_Y$ are two open subsets as required.

=--

+-- {: .proof}
###### Proof
of prop. \ref{CompactHausdorffSpacesAreNormal}

First we claim that $(X,\tau)$ is [[regular topological space|regular]]. To show this, we need to find for each point $x \in X$ and each disjoint closed subset $Y \in X$ dijoint open neighbourhoods $U_x \supset \{x\}$ and $U_Y \supset Y$. But since [[closed subspaces of compact spaces are compact]], the subset $Y$ is in fact compact, and hence this is in fact the statement of lemma \ref{SeparationByNeighbourhoodsOfPointsFromCompactSubsetsInHausdorffSpaces}.

Next to show that $(X,\tau)$ is indeed normal, we apply the idea of the proof of lemma \ref{SeparationByNeighbourhoodsOfPointsFromCompactSubsetsInHausdorffSpaces} once more: 

Let $Y_1, Y_2 \subset X$ be two disjoint closed subspaces. By the previous statement then for every point $y_1 \in Y$ we find disjoint open neighbourhoods $U_{y_1} \subset \{y_1\}$ and $U_{Y_2,y_1} \supset Y_2$. The union of the $U_{y_1}$ is a cover of $Y_1$, and by compactness of $Y_1$ there is a finite subset $S \subset Y$ such that 

$$
  U_{Y_1} \coloneqq \underset{s \in S \subset Y_1}{\bigcup} U_{y_1}
$$

is an open neighbourhood of $Y_1$ and 

$$
  U_{Y_2} \coloneqq \underset{s \in S \subset Y}{\bigcap} U_{Y_2,s}
$$

is an open neighbourhood of $Y_2$, and both are disjoint.

=--



## Related statements

* [[Hausdorff spaces are sober]]

* [[compact subspaces of Hausdorff spaces are closed]]

* [[closed subspaces of compact Hausdorff spaces are equivalently compact subspaces]]

* [[a CW-complex is a Hausdorff space]]

* [[Hausdorff implies sober]]

* [[maps from compact spaces to Hausdorff spaces are closed and proper]]

* [[continuous images of compact spaces are compact]]

* [[paracompact Hausdorff spaces equivalently admit subordinate partitions of unity]]

## References

* TopoSpaces, _[Compact Hausdorff implies normal](https://topospaces.subwiki.org/wiki/Compact_Hausdorff_implies_normal)_


