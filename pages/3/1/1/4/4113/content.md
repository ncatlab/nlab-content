### Definition ###

A (locally finite) **partition of unity** is a collection $\{u_j\}_J$ of continuous functions $u_j:X \to [0,1]$, $j\in J$ such that

 1. $\sum_J u_j(x) = 1$ for all $x\in X$
 2. For each $x\in X$, there is only a finite number of $j\in J$ such that $u_j(x) \neq 0$ (local finiteness condition).

A partition of unity defines an [[open cover]] of $X$, consisting of the open sets $u_j^{-1}(0,1]$.

Sometimes (rarely) the condition that $\{u_j\}_J$ is locally finite is dropped.

Given a [[cover]] $\mathcal{U} = \{U_j\}_{j\in J}$ of a [[topological space]] (open or closed or neither), the partition of unity $\{u_j\}_J$ is **subordinate** to $\mathcal{U}$ if for all $j\in J$,
$$
\overline{u_j^{-1}(0,1]} \subset U_j.
$$
+-- {: .query}
[[David Roberts]]: I know this is standard usage, but it is a bit strange, because then $\{u_j\}$ is not subordinate to $\{u_j^{-1}(0,1]\}$, the open cover it defines. I know the definition is used so that the cover $\mathcal{U}$ doesn't need to be open, but it is a slight failing in my opinion.
=--

### Dold's trick ###

If one is given a non-locally finite partition of unity $\{u_j\}_J$, then often it can be refined into a locally finite partition of unity $\{v_j\}_J$. The open cover defined by $\{v_j\}_J$ then refines the open cover defined by $\{u_j\}_J$, and the former is [[locally finite cover|locally finite]].

### Applications ###

Partitions of unity can be used in constructing maps from spaces to [[geometric realization]]s of [[simplicial spaces]] (incl. simplicial sets) - for example a [[classifying map]] for a $G$-[[bundle]] where $G$ is a [[Lie group]].

[[Paracompact spaces]] have the property that every open cover has a subordinate partition of unity.

[[Normal spaces]] have the property that every [[locally finite cover]] has a subordinate partition of unity. (apparently - need to check this)

The last two are actually characterisations of paracompact resp. normal spaces (reference Bourbaki, Topology Generale I think)

[[!redirects partitions of unity]]
[[!redirects Partitions of unity]]
[[!redirects Partition of unity]]