
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

First of all, by the Hausdorff property there exists for each $c \in C$ disjoint open neighbourhods $U_{x,c} \supset \{x\}$ and $U_c \supset \{c\}$. As $c$ ranges, the latter clearly form an open cover $\{U_c \subset X\}_{c \in C}$ of $C$, and so the union

$$
  \{U_c \subset X\}_{c \in C} \,\cup\, X \backslash C
$$

is an open cover of $X$. By paracompactness of $(X,\tau)$, there exists a locally finite refinement, and by [this lemma](locally+finite+cover#LocallyFiniteRefinementImpliesLocallyFiniteCoverWithOriginalIndexSet) we may assume its elements to share the original index set and be contained in the original elements of the same index. Hence 

$$
  \{V_c \subset U_c \subset  X\}_{c \in C}
$$

is a locally finite collection of subsets, such that 

$$
  U_C \coloneqq \underset{c \in C}{\cup} V_c
$$

is an open neighbourhood of $C$.


Now by definition of local finiteness there exists an open neighbourhood $W_x \supset \{x\}$ and a finite subset $K \subset C$ such that 

$$
  \underset{c \in C \backslash K}{\forall}( W_x \cap V_c = \emptyset )
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
       U_{x,k}
     \right)
  \right)
  \,.
$$

which is an open neighbourhood of $x$, by the finiteness of $K$.

It thus only remains to see that

$$
  U_x \cap U_C = \emptyset
  \,.
$$

But this holds because the only $V_{c}$ that intersect $W_x$ are the $V_{k} \subset U_{k}$ for $k \in K$ and each of these is by construction disjoint from $U_{x,k}$ and hence from $U_x$.

This establishes that $(X,\tau)$ is regular. Now we prove that it is normal. For this we use the same approach as before:

Let $C,D \subset X$ be two disjoint closed subsets. We need to produce disjoint open neighbourhoods for these.

By the previous statement of regularity, we may find for each $c \in C$ disjoint open neighbourhoods $U_c \supset \{c\}$ and $U_{D,c} \supset D$. Hence the union

$$
  \left\{
    U_c \subset X
  \right\}_{c \in C}
  \cup
  X \backslash C
$$ 

is an open cover of $X$, and thus by paracompactness has a locally finite refinement, whose elements we may, again by [this lemma](locally+finite+cover#LocallyFiniteRefinementImpliesLocallyFiniteCoverWithOriginalIndexSet), assume to have the same index set as before and be contained in the previous elements with the same index. Hence we obtain a locally finite collection of subsets

$$
  \{ V_c \subset U_c \subset X \}_{c \in C}
$$

such that

$$
  U_{C}
   \coloneqq
  \underset{c \in C}{\cup} V_c
$$

is an open neighbourhood of $C$.

It is now sufficient to see that every point $d \in D$ has an open neighbourhood $U_d$ not intersecting $U_C$, for then 

$$
  U_D \coloneqq \underset{d \in D}{\cup} U_d
$$

is the required open neighbourhood of $D$ not intersecting $U_C$.

Now by local finiteness of $\{V_c \subset X\}_{c \in C}$, every $d \in D$ has an open neighbourhood $W_d$ such that there is a finite set $K_d \subset C$ so that 

$$  
  \underset{c \in C \backslash K_d}{\forall}
  \left(
     V_c \cap W_d = \emptyset
  \right)
  \,.
$$

Accordingly the intersection

$$
  U_d 
    \coloneqq  
  W_d 
   \cap 
  \left(
    \underset{c \in K_d \subset C}{\cap} U_{D,c}
  \right)
$$

is still open and disjoint from the remaining $V_k$, hence disjoint from all of $U_C$.

=--

## Related statement

* [[metric spaces are paracompact]]

* [[locally compact and sigma-compact spaces are paracompact]]

* [[second-countable regular spaces are paracompact]]

* [[regular Lindelöf spaces are paracompact]]

* [[Hausdorff spaces are sober]]

* [[compact subspaces of Hausdorff spaces are closed]]

* [[closed subspaces of compact Hausdorff spaces are equivalently compact subspaces]]

* [[CW-complexes are paracompact Hausdorff spaces]]

* [[Hausdorff spaces are sober]]

* [[maps from compact spaces to Hausdorff spaces are closed and proper]]

* [[continuous images of compact spaces are compact]]

* [[paracompact Hausdorff spaces equivalently admit subordinate partitions of unity]]



[[!redirects Dieudonné's theorem]]

