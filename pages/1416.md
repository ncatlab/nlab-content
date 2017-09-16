A functor $F: C \rightarrow D$ is __flat__ if each for each object $d \in D$, the [[comma category]] $(d / F)$ is [[filtered category|filtered]].

This rather cryptic definition is really just an exactness property in disguise.  If $F$ is flat, then it preserves any finite limits that exist in $C$.  A partial converse holds: if $C$ has enough finite limits and $F$ preserves these, then $F$ is flat.

Flatness of a functor may be thought of as saying that $F$ preserves all finite limits, even the ones that don't exist yet.  More precisely, if $\mathcal{E}$ is co-complete and $F:C \rightarrow D$ is flat, then the functor
$(- \otimes F) : [C^op,Set] \rightarrow \mathcal{E}$
(the left [[Kan extension]] of $F$ along the Yoneda embedding) preserves all finite limits.   A similar statement holds when $(C,J)$ is a [[site]] and we extend a continuous functor $F$ to $Sh(C)$.

But a co-continuous functor from $Sh(C)$ preserving finite limits is (almost) the same thing as (the inverse image part of) a [[geometric morphism]].  So continuous flat functors out of a site $(C,J)$ characterise (almost) geometric morphisms into $Sh(C)$.  This can be very useful when a sheaf topos has a presentation by a particularly simple site.