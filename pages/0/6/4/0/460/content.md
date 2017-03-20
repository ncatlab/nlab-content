
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

## Idea 

If $\mathcal{O}(X)$ is the topology on a [[topological space]] $X$, and if a map $\mathcal{O}(X) \to \mathcal{O}(1)$ that preserves finite meets and arbitrary joins is considered an instance of "seeing a point $1 \to X$", then $X$ is "sober" if every point we see is really there (i.e., is induced from a point = continuous map $1 \to X$), and if we never see double. 

## Definition

A [[topological space]] $X$ is **sober** if its [[points]] are exactly determined by its [[lattice of open subsets]].  Different equivalent ways to say this are:

* The [[continuous map]] from $X$ to the space of points of the [[locale]] that it gives rise to (see there for details) is a [[homeomorphism]].

* The [[function]] from points of $X$ to the _completely prime [[filters]]_ of its open-set lattice is a [[bijection]].

* (Assuming classical logic) $X$ is [[T0]] and every [[irreducible closed set]] (non-empty closed set that is not the [[union]] of any two non-empty closed sets) is the [[topological closure|closure]] of a (unique, by $T_0$) point.

In each case, half of the definition is that $X$ is $T_0$, the other half states that $X$ has __enough points__:

+-- {: .num_defn #EnoughPointsOfATopologicalSpace}
###### Definition

A [[topological space]] $X$ has _enough points_ if the following equivalent conditions hold:

* The [[continuous map]] from $X$ to the space of points of the [[locale]] that it gives rise to (see there for details) is a [[quotient space|quotient map]].

* The [[function]] from points of $X$ to the _completely prime [[filters]]_ of its [[lattice of open subsets|open-set lattice]] is a [[surjection]].

* (Assuming classical logic) every [[irreducible closed set]] (non-empty closed set that is not the union of any two non-empty closed sets) is the [[topological closure|closure]] of a point.

=--

## Properties

### Separation

* Sobriety is a [[separation property]] that is stronger than [[T0]], but incomparable with [[T1]].  With [[classical logic]], every [[Hausdorff space]] is sober (see at _[[Hausdorff implies sober]]_), but this can fail [[constructive mathematics|constructively]].

$$
  Hausdorff = T_2 \Rightarrow sober \Rightarrow T_0
$$

### Reflection

The [[category]] of sober spaces is [[reflective subcategory|reflective]] in the category of all topological spaces; the [[left adjoint]] is called the **soberification**.  This reflection is also induced by the [[idempotent adjunction]] between spaces and [[locales]]; thus sober spaces are precisely those spaces that are the space of points of some [[locale]], and the [[category]] of sober spaces is [[equivalence of categories|equivalent]] to the category of [[locales with enough points]]. 

### Enough points

A topological space has enough points in the sense of def. \ref{EnoughPointsOfATopologicalSpace} if and only if its $T_0$ quotient is sober.  The category of topological spaces with enough points is a [[reflective subcategory]] of the category [[Top]] of all topological spaces, and a topological space is [[T0]] iff this reflection is sober.


## Examples 

* With [[classical logic]], every [[Hausdorff space]] is sober, but this can fail [[constructive mathematics|constructively]]. See at _[[Hausdorff implies sober]]_.

* The topological space underlying any [[scheme]] is sober. See at _[[schemes are sober]]_.

## Non-examples

* Any nontrivial [[indiscrete space]] is not sober, since it is not $T_0$. More interestingly, the space $R^2$ with the [[Zariski topology]] is $T_1$ but not sober, since every subvariety is an irreducible closed set which is not the [[topological closure|closure]] of a point.  Its _soberification_ is, unsurprisingly, the [[scheme]] $Spec(R[x,y])$, which contains "generic points" whose closures are the subvarieties. 

The following non-example shows that sobriety is not a hereditary separation property, i.e., [[topological subspaces]] of sober spaces need not be sober:

* The [[Alexandroff topology]] on a [[poset]] is also not, in general, sober.  For instance, if $P$ is the infinite binary tree (the set of finite $\{0,1\}$-words ([[lists]]) with the "extends" preorder), then the soberification of its Alexandroff topology is [[Wilson space]], the space of finite or infinite $\{0,1\}$-words ([[streams]]).


## References

For instance around definition IX.3.2 of

* [[Saunders MacLane]], [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_
{#MacLaneMoerdijk}

* Sober spaces in the [$\pi$-base](http://topology.jdabbs.com/properties/73).

[[!redirects sober]]
[[!redirects sober topological space]]
[[!redirects sober topological spaces]]
[[!redirects sober topology]]
[[!redirects sober topologies]]
[[!redirects sober space]]
[[!redirects sober spaces]]

[[!redirects soberification]]
[[!redirects soberifications]]

[[!redirects topological space with enough points]]
[[!redirects topological spaces with enough points]]
