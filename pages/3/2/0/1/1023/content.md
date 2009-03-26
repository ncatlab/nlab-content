An inductive limit is a [[colimit]] of a functor whose [[source]] is a [[direction|directed set]].  The [[duality|dual]] notion is that of a [[projective limit]].

Note that the terminology varies.  The most precise division can be made between _inductive limit_ where the source is a directed set (as here), _[[filtered colimit]]_ where the source is a [[filtered category]], _[[direct limit]]_ where the source is a [[partial order|poset]], and _colimit_ where the source is arbitrary.  However, many authors will simply take whichever term they learnt first and apply it to all situations.  In any given context, after all, there can be no confusion; the source is whatever it is.

These were studied in algebra before the general notion of colimit in category theory.  The elementary definition still seen there follows.

# Definition #

Let $C$ be a [[category]].

An __inductive system__ in $C$ consists of a [[direction|directed set]] $I$, a family $(A_i)_{i: I}$ of objects of $C$, and a family $(f_{ij}: A_i \to A_j)_{i \leq j: I}$ of morphisms, such that:
* $f_{ii}: A_i \to A_i$ is the [[identity]] on $A_i$;
* $f_{ik}: A_i \to A_k$ is the [[composition|composite]] $f_{ij} ; f_{jk}$.

Then an __inductive cone__ of this inductive system is an object $X$ and a family of __inductions__ $\iota_i: A_i \to X$ such that
$$ \iota_i = f_{ij} ; \iota_j .$$

Finally, an __inductive limit__ of the inductive system is an inductive cone ${\textstyle \lim \atop \textstyle \longrightarrow}_i A_i$ (where both $f$ and $\iota$ are suppressed in the notation, each in its own way) which is [[universal property|universal]] in that, given any inductive cone $X$, there exists a unique morphism $u: {\textstyle \lim \atop \textstyle \longrightarrow}_i A_i \to X$ such that
$$ \iota_i = \iota_i ; u $$
(where the left-hand $\iota$ is from the cone $X$ and the right-hand $\iota$ is from the limit).

Notice that an inductive system in $C$ consists precisely of a directed set $I$ and a (covariant) [[functor]] from $I$ (thought of as a category) to $C$, while an inductive cone or limit of such an inductive system is precisely a cocone or colimit of the corresponding functor.  So this is a special case of [[colimit]].

As with other colimits, an inductive limit, if any exists at all, is unique up to a given isomorphism, so we speak of [[generalized the|the]] inductive limit of a given inductive system.

# In algebra #

An inductive limit in algebra is usually defined as a [[quotient object|quotient]] of a [[disjoint union]].  To be precise, ${\textstyle \lim \atop \textstyle \longrightarrow}_i A_i$ is the disjoint union $\biguplus_{i: I} A_i$ with $x: A_i$ identified with $y: A_j$ if
$$ f_{ik}(x_i) = f_{ik}(x_j) $$
for some $k$.  Here it is important that $C$ is a [[concrete category]] and that $I$ is a directed set (rather than merely a [[partial order|poset]]); this construction doesn\'t generalise very well.