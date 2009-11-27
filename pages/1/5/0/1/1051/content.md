# Directed limits
* tic
{: toc}


## Idea

A _directed limit_ (or _codirected limit_) is a [[limit]] of a functor whose [[source]] is a downward-[[direction|directed set]].  The [[duality|dual]] notion is that of _[[directed colimit]]_, a [[colimit]] of a functor whose source is an upward-directed set.

Note that the terminology varies.  Especially in algebra, a directed limit may be called a '[[projective limit]]' or '[[inverse limit]]'; it\'s also possible to distinguish these so that an inverse limit may have an arbitrary (possibly undirected) [[partial order|poset]] as its source.  On the other hand, both terms are often used for arbitrary [[limit]]s as an alternative to the 'co-' method of distinction.  (The corresponding dual terms are '[[inductive limit]]' and '[[direct limit]]', with no 'co-' even though these are [[colimit]]s.)

Directed (co)limits were studied in algebra (as projective and inductive limits) before the general notion of limit in category theory.  The elementary definition still seen there follows.


## Epxlicit definition #

Let $C$ be a [[category]].

A __projective system__ in $C$ consists of a [[direction|directed set]] $I$ (which we will write directed-upward as usual), a family $(A_i)_{i: I}$ of objects of $C$, and a family $(f_{ij}: A_j \to A_i)_{i \leq j: I}$ of morphisms, such that:
* $f_{ii}: A_i \to A_i$ is the [[identity morphism]] on $A_i$;
* $f_{ik}: A_k \to A_i$ is the [[composition|composite]] $f_{ij} \circ f_{jk}$.

Then a __projective cone__ of this projective system is an object $X$ and a family of __projections__ $\pi_i: X \to A_i$ such that
$$ \pi_i = f_{ij} \circ \pi_j .$$

Finally, a __projective limit__ of the projective system is a projective cone ${\textstyle \lim \atop \textstyle \longleftarrow}_i A_i$ (where both $f$ and $\pi$ are suppressed in the notation, each in its own way) which is [[universal property|universal]] in that, given any projective cone $X$, there exists a unique morphism $u: X \to {\textstyle \lim \atop \textstyle \longleftarrow}_i A_i$ such that
$$ \pi_i = \pi_i \circ u $$
(where the left-hand $\pi$ is from the cone $X$ and the right-hand $\pi$ is from the limit).

Notice that a projective system in $C$ consists precisely of a directed set $I$ and a [[contravariant functor]] from $I$ (thought of as a category) to $C$, while a projective cone or limit of such a projective system is precisely a cone or limit of the corresponding functor.  So this is a special case of [[limit]].

As with other limits, a projective limit, if any exists at all, is unique up to a given isomorphism, so we speak of [[generalized the|the]] projective limit of a given projective system.


## In algebra #

A projective limit in algebra is usually defined as a [[subobject|subalgebra]] of a [[cartesian product]].  To be precise, ${\textstyle \lim \atop \textstyle \longleftarrow}_i A_i$ consists of those elements $(x_i)_{i: I}$ of $\prod_{i: I} A_i$ such that:
$$ x_i = f_ij(x_j) .$$
This can be seen as a special case of the construction of an arbitrary limit out of [[product]]s and [[equalizer]]s.


## Examples #

A [[ring]] $ K [ [ x ] ] $ of formal [[power series]] (for $K$ a [[field]]) is a projective limit of the rings $K[x]/x^n$ (for $n$ a [[natural number]]).  Here, $C$ is the category of rings, $I$ is the directed set of natural numbers, $A_i = K[x]/x^i$, and $f_{ij}: A_j \to A_i$ is induced by the quotient map $K[x] \to K[x]/x^i$ (which must be proved well defined on $K[x]/x^j$ for $i \leq j$).

Similarly, a ring $\mathbf{Z}_p$ of $p$-[[adic integer]]s (for $p$ a [[prime number]]) is a projective limit of the rings $\mathbf{Z}/p^n$.

A set of infinite [[sequence]]s is a projective limit of sets of finite sequences (which, at the level of [[set]]s, includes the above examples).


[[!redirects codirected limit]]
[[!redirects directed limits]]
[[!redirects codirected limits]]