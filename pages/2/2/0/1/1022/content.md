A projective limit is a [[limit]] of a functor whose source is a [[direction|directed set]].

+--{+ .query}
[[Zoran Skoda]] This depends on an author. For us in algebraic geometry, projective limit is what you call limit. It does NOT need to be and often it isn't over directed set. Many in old school of topology put that 
assumption. Some ask it to be cofiltered. But most do not ask any. It was funny when at Evanston at homotopy theory conference somebody gave a talk (name privately) inducing laughter in the audience by saying I will use old terms projective and inductive limit instead of limit and colimit, because there are two many dualizations in this business already so one gets easily confused (as if taking new name for co in some cases does simplicification to the confusion). 
=--

These were studied in algebra before the general notion of limit in category theory.  The elementary definition still seen there follows.

# Definition #

Let $C$ be a [[category]].

A __projective system__ in $C$ consists of a [[direction|directed set]] $I$, a family $(A_i)_{i: I}$ of objects of $C$, and a family $(f_{ij}: A_j \to A_i)_{i \leq j: I}$ of morphisms, such that:
* $f_{ii}: A_i \to A_i$ is the [[identity]] on $A_i$;
* $f_{ik}: A_k \to A_i$ is the [[composition|composite]] $f_{ij} \circ f_{jk}$.

Then a __projective cone__ of this projective system is an object $X$ and a family of __projections__ $\pi_i: X \to A_i$ such that
$$ \pi_i = f_{ij} \circ \pi_j .$$

Finally, a __projective limit__ of the projective system is a projective cone ${\textstyle \lim \atop \textstyle \longleftarrow}_i A_i$ (where both $f$ and $\pi$ are suppressed in the notation, each in its own way) which is [[universal property|universal]] in that, given any projective cone $X$, there exists a unique morphism $u: X \to {\textstyle \lim \atop \textstyle \longleftarrow}_i A_i$ such that
$$ \pi_i = \pi_i \circ u $$
(where the left-hand $\pi$ is from the cone $X$ and the right-hand $\pi$ is from the limit).

Notice that a projective system in $C$ consists precisely of a directed set $I$ and a [[contravariant functor]] from $I$ (thought of as a category) to $C$, while a projective cone or limit of such a projective system is precisely a cone or limit of the corresponding functor.  So this is a special case of [[limit]].

As with other limits, a projective limit, if any exists at all, is unique up to a given isomorphism, so we speak of [[generalized the|the]] projective limit of a given projective system.

# In algebra #

A projective limit in algebra is usually defined as a [[subobject|subalgebra]] of a [[cartesian product]].  To be precise, ${\textstyle \lim \atop \textstyle \longleftarrow}_i A_i$ consists of those elements $(a_i)_{i: I}$ of $\prod_{i: I} A_i$ such that:
$$ a_i = f_ij(a_j) .$$
This can be seen as a special case of the construction of an arbitrary limit out of [[product]]s and [[equalizer]]s.