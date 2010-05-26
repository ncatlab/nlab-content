
#Contents#
* automatic table of contents goes here
{:toc}

>David Roberts: I need to clarify point finiteness vs local finiteness of a partition of unity.

## Definition

Let $X$ be a [[topological space]]. A (locally finite) **partition of unity** on $X$ is a collection $\{u_j\}_J$ of [[continuous function]]s $u_j:X \to [0,1]$, $j\in J$ such that

 1. $\sum_J u_j(x) = 1$ for all $x\in X$
 2. For each $x\in X$, there is only a finite number of $j\in J$ such that $u_j(x) \neq 0$ (point finiteness condition).

A partition of unity defines an [[open cover]] of $X$, consisting of the open sets $u_j^{-1}(0,1]$. Call this the **induced cover**.

Sometimes (rarely) the condition that $\{u_j\}_J$ is point finite is dropped. In this case we refer to a _non-point finite_ partition of unity (see [[red herring principle]]).

Given a [[cover]] $\mathcal{U} = \{U_j\}_{j\in J}$ of a [[topological space]] (open or closed or neither), the partition of unity $\{u_j\}_J$ is **subordinate** to $\mathcal{U}$ if for all $j\in J$,
$$
\overline{u_j^{-1}(0,1]} \subset U_j.
$$
+-- {: .query}
[[David Roberts]]: I know this is standard usage, but it is a bit strange, because then $\{u_j\}$ is not subordinate to $\{u_j^{-1}(0,1]\}$, the open cover it defines. I know the definition is used so that the cover $\mathcal{U}$ doesn't need to be open, but it is a slight failing in my opinion.
=--

## From a non-point finite partition of unity to a partition of unity

> (Need some write up here D.R.)

**Definition:** A collection of functions $\mathcal{U} = \{u_i : X \to [0,1]\}$ such that every $x\in X$ is in the support of some $u_i$. Then $\mathcal{U}$ is called _locally finite_ if the cover $u_i^{-1}(0,1]$ (i.e. the induced cover) is [[locally finite cover|locally finite]].

**Proposition:** (Mather, 1965) Let $\{u_i\}_J$ be a non-point finite partition of unity. Then there is a locally finite partition of unity $\{v_i\}_{i\in J}$ such that the induced cover of the latter is a refinement of the induced cover of the former.

This implies that (loc. finite) [[numerable covers]] are cofinal in induced covers arising from collections of functions as in the definition. In particular, given the [[Milnor classifying space]] $\mathcal{B}^M G$ of a [[topological group]] $G$, which comes with a countable family of 'coordinate functions' $\mathcal{B}^M G \to [0,1]$, has a numerable cover. This is shown by Dold to be a trivialising cover for the universal bundle constructed by Milnor, and so the universal bundle is [[numerable bundle|numerable]].

## Applications 

Partitions of unity can be used in constructing maps from spaces to [[geometric realization]]s of [[simplicial spaces]] (incl. simplicial sets) - for example a [[classifying map]] for a $G$-[[bundle]] where $G$ is a [[Lie group]].

[[Paracompact spaces]] have the property that every open cover has a subordinate partition of unity.

[[Normal spaces]] have the property that every [[locally finite cover]] has a subordinate partition of unity. (apparently - need to check this)

The last two are actually characterisations of paracompact resp. normal spaces (reference Bourbaki, Topology Generale I think)

## References

A. Dold, _Partitions of unity in the theory of fibrations_, Ann. of Math. 78. (1963), 223-255.

M. Mather, _Paracompactness and partitions of unity_, PhD thesis, Cambridge (1965).

[[!redirects partitions of unity]]
[[!redirects Partitions of unity]]
[[!redirects Partition of unity]]