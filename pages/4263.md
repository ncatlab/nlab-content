+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# Spatial locales
* tables of contents
{: toc}

## Idea

A spatial locale is a [[locale]] that comes from a [[topological space]].  This is an [[extra property]] of locales, a property of having enough [[point of a locale|points]].


## Definitions

Let $X$ be a [[topological space]].  Then we may define a [[locale]], denoted $\Omega(X)$, whose [[frame of opens]] is precisely the [[frame]] of [[open subspaces]] of $X$.

A locale is __spatial__ if it is [[isomorphism|isomorphic]] to $\Omega(X)$ for some topological space $X$.

A locale $L$ has __enough points__ if, given any two opens $U$ and $V$ in $L$, $U = V$ if (hence iff) precisely the same [[point of a locale|points]] of $L$ belong to $U$ as belong to $V$.


## Properties

The following conditions are all logically equivalent on a [[locale]] $L$:

1.  $L$ is spatial, as defined above.
2.  $L$ has enough points, as defined above.
3.  Given any two opens $U$ and $V$ in $L$, $U \leq V$ if (hence iff) every point of $L$ that belongs to $U$ also belongs to $V$.
4.  $L$ is isomorphic to $\Omega(pt(L))$, where $pt(L)$ is the [[space of points]] of $L$.
5.  The natural morphism $\eta_L\colon \Omega(pt(L)) \to L$ (the [[counit]] of the [[adjunction]] from [[Top]] and [[Loc]]) is an [[isomorphism]].

(It would be nice to state this as a theorem and put in a proof.)

Basically, what is going on here is that we have an [[idempotent adjunction]] from topological spaces to locales, and the spatial locales comprise the image of this adjunction.  The corresponding condition on topological spaces is being [[sober space|sober]].

Therefore, the [[full subcategory]] of $Loc$ on the spatial locales is [[equivalence of categories|equivalent]] to the full subcategory of $Top$ on sober spaces.


## Terminology

The term 'spatial locale' can be confusing; it suggests a locale [[internalization|in]] [[Top]] or in some category [[Sp]] of spaces, which is not correct.  Instead, the adjective 'spatial' should be taken in the same vein as 'localic' in '[[localic topos]]' or 'topological' in 'topological [[convergence space|convergence]]'.  These two terms also suggest that these other locales are not [[spaces]], which is incorrect.

The really clear term for a spatial locale is 'locale with enough points to separate the opens', but 'locale with enough points' should be unambiguous.  However, it is still a bit long.  Occasionally one sees 'spacial' instead of 'spatial'.

## Criteria for spatiality

1. Assuming the [[axiom of choice]], [[locally compact locales]] are spatial.
In particular, [[compact regular locales]] are locally compact, hence automatically spatial.
[[Coherent locales]] are also spatial.

2. More generally, the meet of a countable family of open sublocales (i.e., a $G_\delta$-sublocale) of a [[compact regular locale]] is spatial.

3. The completion of a [[uniform locale]] with a countable basis of uniformity is spatial.

4. [[Stonean local|Stonean locales]] are spatial.

## Related concepts

* [[spatial topos]], [[localic topos]]

* [[locale]]

* [[topological space]]

* [[ionad]]

* [[topos]]

[[!redirects topological locale]]
[[!redirects topological locales]]
[[!redirects spatial locales]]
[[!redirects spacial locale]]
[[!redirects spacial locales]]
[[!redirects locale with enough points]]
[[!redirects locales with enough points]]
[[!redirects locale of opens]]
[[!redirects locales of opens]]
[[!redirects locale of open subspaces]]
[[!redirects locales of open subspaces]]
[[!redirects locale of open subsets]]
[[!redirects locales of open subsets]]
[[!redirects locale of open sets]]
[[!redirects locales of open sets]]