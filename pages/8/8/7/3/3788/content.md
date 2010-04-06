## Idea

A **double functor** is a [[functor]] between [[double categories]].  Since if $C$ and $D$ are double categories, the only possible sort of functor $C\to D$ is a double functor, it is unambiguous to leave off the adjective and simply speak about "functors" between double categories.

However, just like [[2-functors]], double functors do come in different flavors: strict, pseudo/strong, lax, and oplax.  Moreover, these various flavors can be chosen more or less independently in the two directions of a double category (vertical and horizontal).  Thus we can have functors which are strict in both directions, strict in one direction and pseudo in the other, pseudo in both directions, strict in one direction and lax in the other, and so on.  (It's not clear whether lax+lax or lax+oplax are sensible, though.)

## Definitions

If $C$ and $D$ are strict double categories, i.e. [[internal categories]] in $Cat$, then a strict double functor $C\to D$ is simply an internal functor in $Cat$.  Thus, it takes objects, arrows of both sorts, and squares in $C$ to the same structures in $D$, preserving sources and targets and also preserving all identities and composites.

...

[[!redirects pseudo double functor]]
[[!redirects lax double functor]]
[[!redirects oplax double functor]]
[[!redirects double functors]]
[[!redirects pseudo double functors]]
[[!redirects lax double functors]]
[[!redirects oplax double functors]]
