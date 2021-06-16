
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

+-- {: .num_theorem #ParacompactHausdorffEquivalentToexistenceOfParititionsOfUnity}
###### Theorem

Assuming the [[axiom of choice]] then:

Let $(X,\tau)$ be a topological space that is $T_1$ (meaning [[singletons]] are [[closed subsets]]; see [[separation property]]). Then the following are equivalent:

1. $(X,\tau)$ is [[paracompact topological space|paracompact]] and [[Hausdorff space|Hausdorff]].

1. Every [[open cover]] of $(X,\tau)$ admits a subordinate [[partition of unity]] (def. \ref{PartitionOfUnity}).

=--

We give the **proof** [below](#ParacompactHausdorffEquivalentToexistenceOfParititionsOfUnityProof).

## Background

+-- {: .num_defn #LocallyFiniteCover}
###### Definition
**([[locally finite cover]])**

Let $(X,\tau)$ be a [[topological space]].

An [[open cover]] $\{U_i \subset X\}_{i \in I}$ of $X$ is called  _locally finite_ if for all point $x \in X$, there exists a  [[neighbourhood]] $U_x \supset \{x\}$ such that it [[intersection|intersects]] only finitely many elements of the cover, hence such that  $U_x \cap U_i \neq \emptyset$ for only a [[finite number]] of $i \in I$.

=--

+-- {: .num_defn #RefinementOfOpenCovers}
###### Definition
**([[refinement]] of [[open covers]])


Let $(X,\tau)$ be a [[topological space]], and let $\{U_i \subset X\}_{i \in I}$ be a [[open cover]].
 
Then a _[[refinement]]_ of this open cover is a set of open subsets $\{V_j \subset X\}_{j \in J}$ which is still an [[open cover]] in itself and such that for each $j \in J$ there exists an $i \in I$ with $V_j \subset U_i$.

=--

+-- {: .num_defn #ParacompactSpace}
###### Definition
**([[paracompact topological space]])**

A [[topological space]] $(X,\tau)$ is called _[[paracompact topological space|paracompact]]_ if every [[open cover]] of $X$ has a [[refinement]] (def. \ref{RefinementOfOpenCovers}) by a [[locally finite open cover]] (def. \ref{LocallyFiniteCover}).

=--


+-- {: .num_defn #PartitionOfUnity}
###### Definition
**([[partition of unity]])**

Let $(X,\tau)$ be a [[topological space]], and let $\{U_i \subset X\}_{i \in I}$ be an [[open cover]]. Then a _[[partition of unity]] subordinate to the cover_ is

* a [[set]] $\{f_i\}_{i \in I}$ of [[continuous functions]]

  $$
    f_i \;\colon\; X \longrightarrow [0,1]
  $$

  (where $[0,1] \subset \mathbb{R}$ is equipped with the [[subspace topology]] of the [[real numbers]] $\mathbb{R}$  regarded as the 1-dimensional [[Euclidean space]] equipped with its [[metric topology]]); 

such that with 

$$
  Supp(f_i) \coloneqq Cl\left( f_i^{-1}( (0,1] ) \right)
$$

denoting the [[support]] of $f_i$ (the [[topological closure]] of the subset of points on which it does not vanish) then

1. $\underset{i \in I}{\forall} \left( Supp(f_i) \subset U_i \right)$;
  
1. $\left\{ Supp(f_i) \subset X \right\}_{i \in I}$  is a [[locally finite cover]] (def. \ref{LocallyFiniteCover});

1. $\underset{x \in X}{\forall} \left(  \underset{i \in I}{\sum} f_i(x) = 1 \right)$.

=--

+-- {: .num_remark }
###### Remark

Due to the second clause in def. \ref{PartitionOfUnity}, the [[sum]] in the third clause involves only a [[finite number]] of elements not equal to zero, and therefore is well defined.

=--

## Proof

The non-trivial direction to be shown is:

+-- {: .num_prop #OpenCoverOfParacompactHausdorffSpaceAdmitsPartitionOfUnity}
###### Proposition

If $(X,\tau)$ is a [[paracompact topological space]], then for every [[open cover]] $\{U_i \subset X\}_{i \in I}$ there is a subordinate [[partition of unity]] (def. \ref{PartitionOfUnity}).

=--

We give the proof [below](#OpenCoverOfParacompactHausdorffSpaceAdmitsPartitionOfUnityProof).

The following says that if there exists a [[locally finite cover|locally finite]] [[refinement]] of a cover, then in fact there exists one with the same index set as the original cover.

+-- {: .num_lemma #LocallyFiniteRefinementInducesLocallyFiniteWithSameIndexSet}
###### Lemma

Let $(X,\tau)$ be a [[topological space]], let $\{U_i \subset X\}_{i \in I}$ be an [[open cover]], and let $(\phi \colon J \to I), \{V_j \subset X\}_{j \in J})$, be a [[refinement]] to a [[locally finite cover]].

Then  $\left\{ W_i \subset X \right\}_{i \in I}$ with 

$$
  W_i 
    \;\coloneqq\;
  \left\{
    \underset{j \in \phi^{-1}(\{i\})}{\cup} V_j
  \right\}
$$

is still a [[refinement]] of $\{U_i \subset X\}_{i \in I}$ to a [[locally finite cover]].

=--


+-- {: .proof}
###### Proof

It is clear by construction that $W_i \subset U_i$, hence that we have a [[refinement]]. We need to show local finiteness.

Hence consider $x \in X$. By the assumption that $\{V_j \subset X\}_{j \in J}$ is locally finite, it follows that there exists an [[open neighbourhood]] $U_x \supset \{x\}$ and a [[finite set|finite]] [[subset]] $K \subset J$ such that 

$$
  \underset{j \in J\backslash K}{\forall} \left( U_x \cap V_j = \emptyset \right)
  \,.
$$

Hence by construction 

$$
  \underset{i \in I\backslash \phi(K)}{\forall} \left( U_x \cap W_i = \emptyset \right)
  \,.
$$

Since the [[image]] $\phi(K) \subset I$ is still a [[finite set]], this shows that $\{W_i \subset X\}_{i \in I}$ is locally finite.


=--


+-- {: .num_lemma #PatchesOfOpenCoverOfNormalSpaceMayBeMadeSmallerSoThatTheirClosuresAreContained}
###### Lemma
**([[shrinking lemma]])**

Let $X$ be a [[topological space]] which is [[normal topological space|normal]] and let $\{U_i \subset X\}_{i \in I}$ be a [[locally finite cover|locally finite]] [[open cover]].

Assuming the [[axiom of choice]] then:

There exists another open cover $\{V_i \subset X\}_{i \in I}$ such that the [[topological closure]] $Cl(V_i)$ of its elements is contained in the original patches:

$$
  \underset{i \in I}{\forall}
  \left(
     V_i \subset Cl(V_i) \subset U_i
  \right)
  \,.
$$

=--

+-- {: .proof #OpenCoverOfParacompactHausdorffSpaceAdmitsPartitionOfUnityProof}
###### Proof
of prop. \ref{OpenCoverOfParacompactHausdorffSpaceAdmitsPartitionOfUnity}

By paracmpactness of $X$, for every open cover there exists a locally finite refinement $\{U_i \subset X\}_{i \in I}$, and by lemma \ref{LocallyFiniteRefinementInducesLocallyFiniteWithSameIndexSet} we may assume 
that this has same index set. It is now sufficient to show that this locally finite cover $\{U_i \subset X\}_{i \in I}$ admits a subordinate partition of unity, since this will then also be  subordinate to the original cover.


Since [[paracompact Hausdorff spaces are normal]] we may
apply lemma \ref{PatchesOfOpenCoverOfNormalSpaceMayBeMadeSmallerSoThatTheirClosuresAreContained} to the given locally finite open cover $\{U_i \subset X\}_i$, to obtain a smaller locally finite open cover $\{V_i \subset X\}_{i \in I}$, and then apply the lemma once more to that result to get a yet small open cover  $\{W_i \subset X\}_{i \in I}$, so that now

$$
  \underset{i \in I}{\forall}
  \left(
     W_i \subset Cl(W_i) \subset V_i \subset Cl(V_i) \subset U_i
  \right)
  \,.
$$

It follows that for each $i \in I$ we have two disjoint [[closed subsets]], namely the [[topological closure]] $Cl(W_i)$ and the [[complement]] $X \backslash V_i$

$$
  Cl(W_i) \cap X\backslash V_i = \emptyset
  \,.
$$

Now since [[paracompact Hausdorff spaces are normal]], [[Urysohn's lemma]] says that there exist [[continuous functions]]

$$
  h_i \;\colon\; X \longrightarrow [0,1]
$$

with the property that

$$
  h_i( Cl(W_i) ) = \{1\}
  \,,
  \phantom{AAA}
  h_i( X \backslash V_i ) = \{0\}
  \,.
$$

This means in particular that $h_i^{-1}((0,1]) \subset V_i$ and hence that 

$$
  Supp(h_i) =  Cl(h_i^{-1}((0,1])) \subset Cl(V_i) \subset U_i
  \,.
$$

By construction, the set of function $\{h_i\}_{i \in I}$ already satisfies conditions 1) and 2) of the three conditions on a partition of unity subordinate to $\{U_i \subset X\}_{i \in I}$ from def. \ref{PartitionOfUnity}.
It just remains to normalize these functions so that they indeed sum to unity. To that end, consider the continuous function

$$
  h \;\colon\; X \longrightarrow [0,1]
$$

defined on $x \in X$ by

$$
  h(x) \coloneqq \underset{i \in I}{\sum} h_i(x)
  \,.
$$

Notice that the [[sum]] on the right has only a [[finite number]] of non-zero summands, due to the local finiteness of the cover, so that this is well-defined.

Moreover, notice that

$$
  \underset{x \in X}{\forall} \left(  h(x) \neq 0  \right)
$$

because $\{Cl(W_i) \subset X\}_{i \in I}$ is a cover so that there is $i_x \in I$ with $x \in Cl(W_{i_x})$, and since $h_i(Cl(W_{i_x})) = \{1\}$, by the above.

Hence it makes sense to define

$$
  f_i \;\coloneqq\;  h_i/h
  \,.
$$

This is now manifestly such that $\underset{i \in I}{\sum} f_i = 1$, and so 

$$
  \left\{
     f_i
  \right\}_{i \in I}
$$

is a partition of unity as required.


=--


+-- {: .proof #ParacompactHausdorffEquivalentToexistenceOfParititionsOfUnityProof}
###### Proof
of theorem \ref{ParacompactHausdorffEquivalentToexistenceOfParititionsOfUnity}

In one direction, assume that every open cover $\{U_i \subset X\}_{i \in I}$ admits a subordinate partition of unity $\{f_i\}_{i \in I}$. Then by definition (def. \ref{PartitionOfUnity}) $\{ Int(Supp(f)_i)  \subset X\}_{i \in I}$ is a locally finite open cover refining the original one, so $X$ is paracompact. Moreover, since $X$ is $T_1$, for any distinct points $x, y \in X$ there is a cover consisting of the open sets $\neg \{x\}, \neg \{y\}$ (the [[complements]] of the singletons). If $f_x, f_y$ is a subordinate partition of unity (with $f_x$ supported on $\neg \{x\}$, and similarly for $f_y$), then $f_x(x) = 0$ and $f_y(y) = 0$. Then from $f_x + f_y \equiv 1$ we derive $f_x(y) = 1$, whereupon $\{z \in X: f_x(z) \lt 1/2\}$ and $\{z \in X: f_x(z) \gt 1/2\}$ are disjoint open neighborhoods containing $x$ and $y$ respectively. Hence $X$ is Hausdorff. 

The other direction is the statement of prop. \ref{OpenCoverOfParacompactHausdorffSpaceAdmitsPartitionOfUnity}.

=--

## Related statements

* [[paracompact Hausdorff spaces are normal]]

* [[compact spaces equivalently have converging subnet of every net]]

* [[Hausdorff spaces are sober]]

* [[compact subspaces of Hausdorff spaces are closed]]

* [[closed subspaces of compact Hausdorff spaces are equivalently compact subspaces]]

* [[a CW-complex is a Hausdorff space]]

* [[Hausdorff implies sober]]

* [[maps from compact spaces to Hausdorff spaces are closed and proper]]

* [[continuous images of compact spaces are compact]]

* [[colimits of paracompact Hausdorff spaces]]
