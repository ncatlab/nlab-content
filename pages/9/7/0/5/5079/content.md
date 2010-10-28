
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A **progroup** is a [[pro-object]] in the [[category]] [[Grp]] of [[groups]].  In other words, it is a formal [[cofiltered limit]] of groups.

## Surjective progroups versus localic groups

Of course, the category [[Grp]] is [[complete category|complete]], but in general a progroup represented by some cofiltered diagram of groups is not equivalent to the actual limit of that diagram in $Grp$.  However, [[profinite groups]] (i.e. cofiltered systems of *finite* groups) can be identified with actual limits of finite groups if we take those limits, not in $Grp$, but in the larger category $TopGrp$ of [[topological groups]].  The resulting topological groups are precisely those with [[Stone space|Stone]] topologies.

We can generalize this further to arbitrary pro-groups with surjective transition maps, if instead of [[Top]] we take the limit in the category [[Loc]] of [[locales]].

{#EquivalentCharacterizations}
+--{: .un_prop}
###### Proposition

The following are equivalent for a [[localic group]] $G$:
1. $G$ is a cofiltered limit of [[discrete group]]s (considered as discrete localic groups)
1. $G$ is a cofiltered limit of discrete groups with [[surjection|surjective]] transition maps.
1. The [[open subset|open]] [[normal subgroup]]s of $G$ form a [[neighborhood]] [[topological base|base]] at the identity $e\in G$.
=--
+--{: .proof}
###### Proof

This can be found in ([Moerdijk](#Moerdijk)).

=--

+--{: .un_defn}
###### Definition

A localic group with these properties is called **prodiscrete**.

=--

We may as well assume that any surjective progroup is indexed on a directed [[poset]].  If $(G_i)_{i\in I}$ is such an inverse system, then the localic group $G=\lim_i G_i$ is presented by the following [[posite]].  The elements of the underlying poset are pairs $(x,i)$ where $x\in G_i$, with $(x,i)\le (y,j)$ when $i\le j$ and $f_{ij}(x)=y$.  The coverings are given as follows: for any $j$, the element $(x,i)$ is covered by the family of all $(z,k)$ such that $k\le j$ and $(z,k)\le (x,i)$.

+--{: .un_defn}
###### Definition

A **surjective progroup** is a progroup whose cofiltered diagram consists of [[surjection]]s.

=--

By a fundamental fact about [[locales]], if $G$ is prodiscrete and represented as the limit of a system with surjective transition maps, then the legs $G\to G_i$ of the limiting cone are also surjective (i.e. they are represented by injective [[frame]] homomorphisms).  This is false for limits of topological spaces.

+--{: .un_theorem}
###### Theorem

The category of prodiscrete localic groups is equivalent to the category of surjective progroups.

=--
+--{: .proof}
###### Proof

In view of the [above proposition](#EquivalentCharacterizations) it suffices to show that for surjective progroups $(G_i)$ and $(H_j)$, with prodiscrete localic limits $G$ and $H$, we have
$$Hom_{LocGrp}(G,H) \cong \lim_j \colim_i Hom_{Grp}(G_i,H_j).$$
But since $H = \lim_j H_j$, we have $Hom_{LocGrp}(G,H) \cong \lim_j Hom_{LocGrp}(G,H_j)$.  Thus it suffices to show that any map from $G$ to a [[discrete group]] $K$ (such as $H_j$) factors through some essentially unique $G_i$.

But if $f\colon G\to K$ is such a map, then $ker(f)$ is an open normal subgroup of $G$.  And if $p_i\colon G\to G_i$ are the projections, then the [[kernel]]s $ker(p_i)$ are a neighborhood base at $e$, so we have $ker(p_i)\subseteq ker(f)$ for some $i$, hence $f$ factors through $G/ker(p_i)$.  Finally, this last is isomorphic to $G_i$, since $p_i\colon G\to G_i$ is an open surjection of locales.

=--

Any [[localic group]] $G$ has a [[classifying topos]] consisting of continuous $G$-sets, i.e. discrete locales with a $G$-action.  In general, the resulting [[functor]]
$$ LocGrp \to Topos $$
is not an [[embedding]] into [[Topos]], but it can be shown to be so when restricted to prodiscrete localic groups.  One can also characterize the toposes that are sheaves on a prodiscrete localic group as the [[Galois topos|Galois toposes]].

Most of these results have corresponding facts for pro-[[groupoids]] and prodiscrete localic groupoids.

## References

* [[Ieke Moerdijk]], *Prodiscrete groups and Galois toposes*
{#Moerdijk}

[[!redirects progroups]]
[[!redirects pro-group]]
[[!redirects pro-groups]]
[[!redirects prodiscrete localic group]]
[[!redirects prodiscrete localic groups]]
