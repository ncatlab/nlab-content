

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

## Idea

A _locally finite cover_ is a [[cover]] which in a suitable sense looks _locally_ like a [[finite cover]].

## Definition

+-- {: .num_defn #LocallyFiniteCover}
###### Definition
**(locally finite cover)**

Let $(X,\tau)$ be a [[topological space]].

A [[cover]] $\{U_i \subset X\}_{i \in I}$ of $X$ by [[subsets]] of $X$  is called  _locally finite_  if it is a [[locally finite set of subsets]], hence
if for all points $x \in X$, there exists a  [[neighbourhood]] $U_x \supset \{x\}$ such that it [[intersection|intersects]] only [[finite number|finitely many]] elements of the cover, hence such that  $U_x \cap U_i \neq \emptyset$ for only a [[finite number]] of $i \in I$.

If $\{U_i \subset X\}_{i \in I}$ is an [[open cover]], then it is called a _locally finite open cover_.

=--

+-- {: .num_remark #AlternativeCharacterizations}
###### Remark
**(alternative characterizations of local finiteness)**

Let  $X$ be a [[topological space]] and let $\{U_i \to X\}_{i \in I}$ be a [[cover]] by [[subsets]]. Then the following are equivalent:

1. $\{U_i \subset X\}_{i \in I}$ is locally finite (def. \ref{LocallyFiniteCover});

1. there exist an _[[open cover]]_ $\{V_j \subset X\}_{j \in J}$ such that for each $j \in J$ there is a [[finite number]] of $i \in I$ that $V_j$ intersects $U_i$.

This is because the various $V_i$ constitute open neighbourhoods for all points $x \in X$.

Moreover, suppose that $\{V_j \subset X\}_{j \in J}$ is a cover by any subsets (not necessarily open), but that it is itself a [[locally finite set of subsets]]. Then if for all $j \in J$ there are a finite number of $i \in I$ such that $U_i$ intersects $V_j$, it follows again that also $\{U_i \subset X\}_{i \in I}$ is locally finite.

This is because by the local finiteness of $\{V_j \subset X\}_{j \in J}$ we have for every point $x \in X$ an open neighbourhood $O_x \supset \{x\}$ which intersects only a finite number of the $V_j$, and since each of these intersects only a finite number of the $U_i$, in total also $O_x$ can only intersect a finite number of the $U_i$.


=--

## Properties


The following says that if there exists a [[locally finite cover|locally finite]] [[refinement]] of a cover, then in fact there exists one with the same index set as the original cover.

+-- {: .num_lemma #LocallyFiniteRefinementImpliesLocallyFiniteCoverWithOriginalIndexSet}
###### Lemma
**(locally finite refinement induces locally finite cover with original index set)**

Let $(X,\tau)$ be a [[topological space]], let $\{U_i \subset X\}_{i \in I}$ be an [[open cover]], and let $\{V_j \subset X\}_{j \in J}$, be a [[refinement]] to a [[locally finite cover]]. 

By definition of [[refinement]] we may [[axiom of choice|choose]] a [[function]] 

$$
  \phi \colon J \to I
$$

such that 

$$
  \underset{j \in J}{\forall}\left( V_j \subset U_{\phi(j)} \right)
  \,.
$$
Then  $\left\{ W_i \subset X \right\}_{i \in I}$ with 

$$
  W_i 
    \;\coloneqq\;
  \left\{
    \underset{j \in \phi^{-1}(\{i\})}{\cup} V_j
  \right\}
$$

is still a [[refinement]] of $\{U_i \subset X\}_{i \in I}$ to a locally finite cover.

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


+-- {: .num_lemma}
###### Lemma
**([[shrinking lemma]])**

Let $(X,\tau)$ be a [[normal topological space]], and let $\{U_i \subset X\}_{i \in I}$ be a [[locally finite cover|locally finite]] [[open cover]]. Then there exists a shrinking to a locally finite open cover $\{V_i \subset X\}_{i \in I}$ whose [[topological closure|closures]] $Cl(-)$ are still contained in the original cover:

$$
  V_i \subset Cl(V_i) \subset U_i
  \,.
$$

=--


## Related concepts


* [[locally finite set of subsets]]

* [[locally finite cell complex]]

* [[cover]], [[open cover]], 

* [[paracompact topological space]]

[[!redirects locally finite covers]]

[[!redirects locally finite open cover]]
[[!redirects locally finite open covers]]

[[!redirects locally finite closed cover]]
[[!redirects locally finite closed covers]]

[[!redirects locally finite family]]
[[!redirects locally finite families]]

[[!redirects locally finite]]
