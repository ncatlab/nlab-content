
<div class="rightHandSide toc">
[[!include topos theory - contents]]
</div>

# Topological locales
* tables of contents
{: toc}

## Idea

A topological (or spatial) locale is a [[locale]] that comes from a [[topological space]].  This is an [[extra property]] of locales, a property of having enough [[point of a locale|points]].


## Definitions

Let $X$ be a [[topological space]].  Then we may define a [[locale]], denoted $\Omega(X)$, whose [[frame of opens]] is precisely the [[frame]] of [[open subspaces]] of $X$.

A locale is __topological__, or __spatial__, if it is [[isomorphism|isomorphic]] to $\Omega(X)$ for some topological space $X$.

A locale $L$ has __enough points__ if, given any two opens $U$ and $V$ in $L$, $U = V$ if (hence iff) precisely the same [[point of a locale|points]] of $L$ belong to $U$ as belong to $V$.


## Properties

The following conditions are all logically equivalent on a [[locale]] $L$:

1.  $L$ is topological, as defined above.
2.  $L$ has enough points, as defined above.
3.  Given any two opens $U$ and $V$ in $L$, $U \leq V$ if (hence iff) every point of $L$ that belongs to $U$ also belongs to $V$.
4.  $L$ is isomorphic to $\Omega(pt(L))$, where $pt(L)$ is the [[space of points]] of $L$.
5.  The natural morphism $\eta_L\colon \Omega(pt(L)) \to L$ (the [[counit]] of the [[adjunction]] from [[Top]] and [[Loc]]) is an [[isomorphism]].

(It would be nice to state this as a theorem and put in a proof.)

Basically, what is going on here is that we have an [[idempotent adjunction]] from topological spaces to locales, and the topological locales comprise the image of this adjunction.  The corresponding condition on topological spaces is being [[sober space|sober]].

Therefore, the [[full subcategory]] of $Loc$ on the topological locales is [[equivalence of categories|equivalent]] to the full subcategory of $Top$ on sober spaces.


## Terminology

The terms 'topological locale' and 'spatial locale' can be confusing; they suggest a locale [[internalization|in]] [[Top]] or in some category [[Sp]] of spaces, which is not correct.  Instead, the adjective 'topological' and 'spatial' should be taken in the same vein as 'localic' in '[[localic topos]]' or 'topological' in 'topological [[convergence space|convergence]]'.  These two terms also suggest that the study of *other* locales is not part of [[topology]] or that these other locales are not [[spaces]], which is also incorrect.

The really clear term for a topological locale is 'locale with enough points to separate the opens', but 'locale with enough points' should be unambiguous.  However, it is still a bit long.  The shortest term, 'spatial locale', is probably also the most common.  Occasionally one sees 'spacial' instead of 'spatial', but this might just be a misspelling.


[[!redirects topological locale]]
[[!redirects topological locales]]
[[!redirects spatial locale]]
[[!redirects spatial locales]]
[[!redirects spacial locale]]
[[!redirects spacial locales]]
[[!redirects locale with enough points]]
[[!redirects locales with enough points]]
[[!redirects locale of opens]]
