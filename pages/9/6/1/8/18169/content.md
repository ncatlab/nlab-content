
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

+-- {: .num_defn #ParacompactHausdorffSpacesAreNormal}
###### Proposition
**(Dieudonn&#233;'s theorem)**

Every [[paracompact Hausdorff space]] is [[normal Hausdorff space|normal]].

In particular [[compact Hausdorff spaces are normal]].

=--

+-- {: .proof}
###### Proof

Let $(X,\tau)$ be a paracompact Hausdorff space

We first show that it is [[regular topological space|regular]]: To that end,
let $x \in X$ be a point, and let $C \subset X$ be a [[closed subset]] not containing $x$. We need to find disjoint open neighbourhoods $U_x \supset \{x\}$ and $U_C \supset C$.

First of all, by the Hausdorff property there exists for each $c \in C$ disjoint open neighbourhods $U_{x,c} \supset \{x\}$ and $U_c \supset \{c\}$. As $c$ ranges, the latter clearly form an open cover $\{U_c \subset X\}_{c \in C}$ of $C$, and so

$$
  \{U_c \subset X\}_{c \in C} \cup X \backslash C
$$

is an open cover of $X$. By paracompactness of $(X,\tau)$, there exists a locally finite refinement of $X$, and by [this lemma](locally+finite+cover#LocallyFiniteRefinementImpliesLocallyFiniteCoverWithOriginalIndexSet) we may assume its elements to share the original index set and be contained in the original elements. We discard all the elements of this refinement that do not intersect $C$ and this obtain a locally finite collection of open subsets

$$
  \{V_c \subset U_c \subset  X\}_{c \in C' \subset C}
$$

with 

$$
  C \subset \underset{c \in C}{\cup} V_c
  \;\,,
  \;\;\;
  \underset{c \in C'}{\forall} ( C \cap V_c \neq \emptyet)
$$

By definition this means that there exists an open neighbourhood $W_x \supset \{x\}$ and a finite subset $K \subset C'$ such that 
$\underset{c \in C \backslash K}{\forall}( W_x \cap V_c = \emptyset )$ while $\underset{k \in K \subset C}{\forall}( W_x \cap V_k \neq \emptyset )$. 

For each $k \in K$ choose a point

$$
  c_k \in C \cap V_k
  \,.
$$


Consider then 

$$
  U_x 
   \;\coloneqq\;
  W_x 
    \cap 
  \left( 
    \underset{k \in K}{\cap}
     \left(
       U_{x_{(c_k)}}
     \right)
  \right)
$$

and

$$
  U_C
   \;\coloneqq\;
  \underset{i \in I}{\cup} V_{i}
  \,.
$$

These are clearly open neighbourhoods of $\{x\}$ and of $C$, respectively. Moreover they are disjoint,

$$
  U_x \cap U_C = \emptyset
  \,.
$$

This is because only finitely many of the $V_i$ intersect $W_x$, by local finiteness, and those that do are the $V_{c_k} \subset U_{c_k}$ which by construction are each disjoint from $U_x$.

This estabishes that $(X,\tau)$ is regular. Now we prove that it is normal.

To this end, let now $C_1, C_2 \subset X$ be two disjoint closed subsets. We need to find disjoint open neighbourhoods for them.

By the previous discussion of regularity, we have for every $c \in C_1$ disjoint open beighbourhoods $U_{c} \supset \{c\}$ and U_{C_2,c}) \subset C_2$. Hence

$$
  \left\{
     U_c \subset X
  \right\}_{c \in C_1}
  \cup
  X \backslash C
$$

is an open  cover of $X$.

=--

## References

* TopoSpaces, _[Paracompact Hausdorff implies normal](https://topospaces.subwiki.org/wiki/Paracompact_Hausdorff_implies_normal)_

[[!redirects Dieudonné's theorem]]

