A _directed limit_ (or _codirected limit_) is a [[limit]] of a functor whose [[source]] is a downward-[[direction|directed set]].  The [[duality|dual]] notion is that of _[[directed colimit]]_, a [[colimit]] of a functor whose source is an upward-directed set.

Note that the terminology varies.  Especially in algebra, a directed limit may be called a '[[projective limit]]' or '[[inverse limit]]'; it\'s also possible to distinguish these so that an inverse limit may have an arbitrary (possibly undirected) [[partial order|poset]] as its source.  On the other hand, both terms are often used for arbitrary [[limit]]s as an alternative to the 'co-' method of distinction.  (The corresponding dual terms are '[[inductive limit]]' and '[[direct limit]]', with no 'co-' even though these are [[colimit]]s.)

Directed (co)limits were studied in algebra (as projective and inductive limits) before the general notion of limit in category theory.  The elementary definition still seen there follows.

# Definition #

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

# In algebra #

A projective limit in algebra is usually defined as a [[subobject|subalgebra]] of a [[cartesian product]].  To be precise, ${\textstyle \lim \atop \textstyle \longleftarrow}_i A_i$ consists of those elements $(x_i)_{i: I}$ of $\prod_{i: I} A_i$ such that:
$$ x_i = f_ij(x_j) .$$
This can be seen as a special case of the construction of an arbitrary limit out of [[product]]s and [[equalizer]]s.

# Examples #

A [[ring]] $ K [ [ x ] ] $ of formal [[power series]] (for $K$ a [[field]]) is a projective limit of the rings $K[x]/x^n$ (for $n$ a [[natural number]]).  Here, $C$ is the category of rings, $I$ is the directed set of natural numbers, $A_i = K[x]/x^i$, and $f_{ij}: A_j \to A_i$ is induced by the quotient map $K[x] \to K[x]/x^i$ (which must be proved well defined on $K[x]/x^j$ for $i \leq j$).

Similarly, a ring $\mathbf{Z}_p$ of $p$-[[adic integer]]s (for $p$ a [[prime number]]) is a projective limit of the rings $\mathbf{Z}/p^n$.

A set of infinite [[sequence]]s is a projective limit of sets of finite sequences (which, at the level of [[set]]s, includes the above examples).

# Discussion #

This is from when this page was at [[projective limit]].

+--{+ .query}
[[Zoran Skoda]] This depends on an author. For us in algebraic geometry, projective limit is what you call limit. It does NOT need to be and often it isn't over directed set. Many in old school of topology put that 
assumption. Some ask it to be cofiltered. But most do not ask any. It was funny when at Evanston at homotopy theory conference somebody gave a talk (name privately) inducing laughter in the audience by saying I will use old terms projective and inductive limit instead of limit and colimit, because there are two many dualizations in this business already so one gets easily confused (as if taking new name for co in some cases does simplicification to the confusion).

_Toby_:  Does the paragraph above satisfy you, Zoran?

_Zoran_: No, some people use term directed limit for a limit over directed set. This is precise if you prefer to assert the subtle subdivisions, and nobody questions this term (just some do not use it). As far as projective limit vs. limit the choice is now the matter of school. Many CATEGORY THEORY books define projective limit as a limit in general. For example Bucur-Deleanu influentiable category book is using only terms projective limit and inductive limit. 

_Toby_:  Some people say 'directed limit'?  That would be confusing, since I would tend to misread that as 'direct limit' (which is a colimit, of course, unfortunately).

Is it accurate to say that the school that uses 'projective limit' in the most general sense developed out of algebra, where 'projective limit' was first used as in the section on algebra below?

I want to describe the terminology accurately, but at the same time, I think it\'s fair to talk about those things that apply only to projective limits in the strictest sense.  (Actually there is more, in algebra at least, that applies only to inductive limits in the strictest sense.)

We can discuss this at [[limit]], if you\'d prefer.

_Zoran_: I think the categorical properties and existence statements (for all categories, not just some specific examples) of directed limits and cofiltered limits are mostly the same, and cofiltered limits and filtered colimits are more natural place to discuss. As far as talking about just the case which is specific to directed limits only in specific categories, like categories of algebras over a monad in sets, or category of topological spaces, why not having separate entry just for such things.
You are right that directed may be confused with direct. I never confused them when reading such articles but you are right, I never thought of this. It is cheap enough to say a limit over a directed set, or even "over a net".  

I do not know how much it is true that it is algebra tradition. Who else was using categorical limits  until recently -- category theorists, algebraists and topologists. In topology words inverse limit and direct limit were used in classical days and now everybody is suddenly after Quillen era well educated in saying colimit so that changed. Traditional fields of algebra just change a bit slowlier. I mean people doing ring theory or group theory. But as soon as you do a more modern topic like operad you learn from new school. So the tradition is time dependent. 

_Toby_:  Well, it\'s not the language that I learnt, but I agree that 'directed (co)limit' is a pretty good word, and maybe it\'s just as well if 'direct limit' falls out of use.  So I\'m OK to move this material to [[directed limit]] (and move the material at [[inductive limit]] to [[directed colimit]]), leaving this page as a redirect.  But I\'ll make a note at [[latest changes]] and wait a while, in case somebody else wants to speak up.

By the way ---and maybe you already know this---, 'slowlier' is not an English word, at least not in formal writing; you have to say 'more slowly' instead.  (It\'s fine here, but I thought that you should know.)

[[Mike Shulman|Mike]]: If you don't like "directed limit," then by analogy with "cofiltered limit," the term "codirected limit" naturally suggests itself.  (-:

I agree (I think this is what Zoran is saying?) that it would be better if this page just says "projective limit is an older/alternate term for a (possibly codirected) [[limit]], as contrasted with inductive limit which means a (possibly directed) [[colimit]]," with the material about limits over codirected posets on a separate page.

_Toby_:  OK, if Mike agrees, then I\'ll do it.  I think that I\'ll put stuff at [[directed limit]] but actually discuss both concepts there.
=--


[[!redirects codirected limit]]