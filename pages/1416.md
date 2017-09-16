## Idea ##

If $C$ is a [[finitely complete category]] (a category with all [[finite limit]]s), then it\'s interesting to consider a left [[exact functor]] on $C$ (a functor that preserves all finite limits).  Even if $C$ lacks some finite limits, then this concept still makes sense, but it may not be the correct one.  Instead we use the stronger concept of a _flat functor_, which may be thought of as a functor that preserves all finite limits ---even the ones that don\'t exist yet!

## Definition ##

A [[functor]] $F: C \rightarrow D$ is __flat__ if each for each object $d \in D$, the [[comma category]] $(d / F)$ is [[filtered category|filtered]].

## Properties ##

If $F$ is flat, then it preserves any finite limits that exist in $C$.  A partial converse holds: if $C$ has enough finite limits and $F$ preserves these, then $F$ is flat.

If $\mathcal{E}$ is a [[cocomplete category]] and $F: C \rightarrow D$ is flat, then the functor $(- \otimes F) : [C^op,Set] \rightarrow \mathcal{E}$ (the left [[Kan extension]] of $F$ along the [[Yoneda embedding]]) preserves all finite limits (and now all finite limits exist).

A similar statement holds when $C$ is a [[site]] and we extend a co[[continuous functor]] $F$ to $Sh(C)$.  But a cocontinuous functor from $Sh(C)$ preserving finite limits is (almost) the same thing as (the inverse image part of) a [[geometric morphism]].  So cocontinuous flat functors out of a site $C$ characterise (almost) geometric morphisms into $Sh(C)$.  This can be very useful when a [[Grothendieck topos]] has a presentation by a particularly simple site.