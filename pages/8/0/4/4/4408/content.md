
# $0$-sites
* table of contents
{: toc}

## Idea

A $0$-site is a [[decategorification]] of a [[site]] (which may also be called a $1$-site). For the [[categorification]], see [[infinity-site]].

Just as a site is a [[category]] with a [[coverage]], whose ([[set]]-valued) [[sheaves]] form a [[Grothendieck topos]], so a $0$-site is a [[poset]] with a coverage, whose $0$-sheaves ([[truth value]]-valued sheaves) form a [[locale]].

As locale theory serves as an approach to [[topology]] in which locales take the role traditionally held by [[topological spaces]], so $0$-sites take the role traditionally held by [[topological bases]].

A [[formal topology]] is a $0$-site equipped with a 'positivity' predicate.

In the rest of this article, by 'site' we mean a $0$-site.


## Definitions

Let $S$ be a [[meet-semilattice]].  (Actually, it is not necessary that the [[poset]] $S$ have *all* finitary [[meets]] but only *[[bounded meet|bounded]]* ones.  That is, if $v, w \leq u$ for some fixed $u$, then $v \wedge w$ must exist, but not otherwise.  Such a poset $S$ is a semilattice if and only if it has a [[top element]].  Compare the notion of [[locally cartesian category]].)

A __coverage__ on $S$ (properly a __$0$-coverage__) is a [[binary relation]] $\rhd$ between $S$ and its [[power set]] that satisfies these conditions:

*  If $u \rhd V$ and $v \in V$, then $v \leq u$;
*  If $u \rhd V$ and $w \leq u$, then $w \rhd \{ v \wedge w \;|\; v \in V \}$.

(Compare the conditions on a $1$-[[coverage]].)  Given an element $u$ of $S$ and a [[subset]] $V$ of $S$, if
$$ u \rhd V ,$$
then we say that $V$ is a __cover__ of $u$.

A __site__ (properly a __$0$-site__) is a semilattice (or locally cartesian poset) equipped with a coverage.

Given two sites $S$ and $T$, a __morphism of sites__ from $S$ to $T$ is a semilattice [[homomorphism]] $f\colon S \to T$ that respects covers in the sense that

*  If $u \rhd V$, then $f(u) \rhd \{ f(v) \;|\; v \in V \}$.

Note that if $S$ and $T$ are not semilattices (but may be only locally cartesian), then the condition that the [[function]] $f\colon S \to T$ be a homomorphism is replaced by these conditions:

*  If $u \leq v$ in $S$, then $f(u) \leq f(v)$ in $T$;
*  Given any $u$ in $T$, for some $v$ in $S$, we have $u \leq f(v)$; and
*  If $w \leq f(u), f(v)$ in $T$, then for some $x \leq u, v$ in $S$, we have $w \leq f(x)$.

(Compare the concept of [[flat functor]].)


## Sheaves

Given a site $S$, a __sheaf__ on $S$ (properly a __$0$-sheaf__; compare [[infinity-sheaf]]) is a [[subset]] $I$ of $S$ satisfying these conditions:

*  If $u \leq v$ and $v \in I$, then $u \in I$; and
*  If $u \rhd V$ and $V \subseteq I$, then $u \in I$.

(Compare the conditions on a $1$-[[sheaf]].)  The first condition alone states that $I$ is a __[[lower subset]]__ (a $0$-[[presheaf]]).

The sheaves on a site form a [[frame]] $Sh(S)$ under inclusion, which may alternately be interpreted as a [[locale]].

Every element of $S$ may be interpreted as a sheaf on $S$; given two elements $u,v$ of $S$, $u$ belongs to the __sheaf represented__ by $v$ if and only if $u \leq v$.

The frame of sheaves is given by a [[universal property]].  If $L$ is a frame, we make $L$ into a site using its canonical coverage (see the examples below).  Then the operation from elements of $S$ to sheaves on $S$ is a morphism of sites; furthermore, given any morphism of sites from $S$ to a frame $L$ (with its canonical coverage), there exists a unique frame [[homomorphism]] from $Sh(S)$ to $L$ that makes the obvious triangle commute.


## Interpretations

Given a site $S$, we may think of the elements of $S$ as __basic opens__ of a space which is generated from $S$ using its coverage, to produce a [[locale]].  Thus a site is precisely a __base__ for a locale.  See the example coming from a topological space below to see how this can work precisely for a [[topological locale]].

A coverage can be seen as a [[sequent]] calculus; the interpretation of
$$ u \rhd V $$
in topology is analogous to the interpretation of
$$ p \rhd Q $$
in [[logic]].  Note that we have a single proposition on the left but a set of propositions (interpreted [[disjunction|disjunctively]]) on the right, the reverse of an [[intuitionistic logic|intuitionistic]] sequent.


## Examples

Any semilattice (or locally cartesian poset) $S$ has a __canonical coverage__, in which

*  $u \rhd V$ if and only if $u$ is a [[join]] of $V$ in $S$.

(Compare the [[canonical coverage]] on a locally cartesian category.)  If $S$ is a frame equipped with its canonical coverage, then $Sh(S)$ is [[natural isomorphism|naturally isomorphic]] to $S$ itself.  (Recall that the [[topos of sheaves]] on a Grothendieck topos $S$ with its canonical coverage is naturally [[equivalence of categories|equivalent]] to $S$.)

Let $X$ be a [[topological space]], and let $S$ be a [[topological base]] of $X$.  Then $S$ is a semilattice under [[intersection]]; we make $S$ into a site by defining

*  $u \rhd V$ if and only if $u$ is the [[union]] of $V$ in $X$.

The frame generated by this site is [[natural isomorphism|naturally isomorphic]] to the [[frame of opens]] of $X$.  If $X$ is a [[sober space]], then this frame, interpreted as a [[locale]], may be identified with $X$.

The [[locale of real numbers]] is generated from the locally cartesian poset $S \coloneqq \mathbb{Q}^op \times \mathbb{Q}$, where $\mathbb{Q}$ is the usual poset of [[rational numbers]], equipped with the cartesian coverage given by

*  $(x,y) \rhd \empty$ whenever $x \geq y$;
*  $(w,z) \rhd \{(w,x),(y,z)\}$ whenever $w \leq y \lt x \leq z$; and
*  $(w,z) \rhd \{ (x,y) \;|\; w \lt x \lt y \lt z \}$.

(Often you will see $\infty$ added to $\mathbb{Q}$ in a description of this locale, which adds a top element to $S$, but this makes no difference in the end.)


## Use in predicative mathematics

We call a frame (or locale) $L$ __accessible__ if it is isomorphism to $Sh(S)$ for some [[small category|small]] site $S$.  In [[classical mathematics]], an accessible frame must be small, but this fails in [[predicative mathematics]].  (Conversely, any small frame is trivially accessible; take $S$ to be $L$ with its canonical coverage.)  Since many predicativists have philosophical objections to working with large objects at all, they may work prefer to work with small sites directly.  Whatever the philosophy, we may use the category of small sites in place of the category of accessible locales, or at any rate use this to prove that the latter category is essentially [[moderate category]].

[[formal topology|Formal topology]] is a programme for [[topology]] which is based on using small sites.  However, formal topologists also require a positivity predicate on their sites; the intended interpretation is that $u$ is positive iff (thinking of it as if it were a subset of a topological space) it is [[inhabited subset|inhabited]].  I need to figure out why this is necessary; it may be for predicativist or constructivist reasons (since the formal topologists are both at once).


## Non-locally cartesian sites

I am a little unsure about how to do this.  On the one hand, we can define a [[coverage]] on a category that is not locally cartesian with only a little extra trouble, and to do this analogously here would keep a coverage on an arbitrary [[poset]] $S$ as a relation between $S$ and its power set.  On the other hand, the logical interpretation of a site begs to be interpreted as a sequent in [[geometric logic]], so that the left hand side should be a [[list]]; that is, a coverage on $S$ should be realtion between the [[free monoid]] on $S$ and the power set.


## References

*  mostly _[[Stone Spaces]]_, but I tried to work out my own presentation


[[!redirects 0-site]]
[[!redirects 0-sites]]

[[!redirects 0-coverage]]
[[!redirects 0-coverages]]

[[!redirects morphism of 0-sites]]
[[!redirects morphisms of 0-sites]]
[[!redirects 0-site morphism]]
[[!redirects 0-site morphisms]]

[[!redirects 0-sheaf]]
[[!redirects 0-sheaves]]

[[!redirects frame of 0-sheaves]]
[[!redirects frames of 0-sheaves]]
[[!redirects frame of sheaves]]
[[!redirects frames of sheaves]]
[[!redirects locale of 0-sheaves]]
[[!redirects locales of 0-sheaves]]
[[!redirects locale of sheaves]]
[[!redirects locales of sheaves]]

[[!redirects localic base]]
[[!redirects localic bases]]
[[!redirects base of a locale]]
[[!redirects bases of a locale]]
[[!redirects bases of locales]]
