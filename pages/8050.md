
# Null and full sets
* table of contents
{: toc}

([[null set|Null set]] redirects here; for the notion in set theory, see [[empty set]].)

## Idea

In [[measure theory]], a _null set_ is a [[subset]] of a [[measure space]] (or [[measurable space]]) that is so small that it can be neglected: it might as well be the [[empty subset]]; its measure is [[zero]].  Similarly, a _full set_ is a subset that is so large that it might as well be the [[improper subset]] (the entire space).  One also says that a null set has _null measure_ and a full set has _full measure_.

Traditionally, full sets are not usually referred to explicitly; in [[classical mathematics]], they are simply the [[complements]] of null sets.  However, they are often referred to implicitly through such terminology as 'almost everywhere'.  Also, in [[constructive mathematics]], full sets are more fundamental than null sets; they are not simply the complements of the latter.


## Definitions

The definitions depend on the context.


### In a measure space

In a traditional [[measure space]], we have an abstract [[set]] $X$, a $\sigma$-[[sigma-algebra|algebra]] (or similar structure) $\mathcal{M}$ consisting of the [[measurable subsets]] of $X$, and a [[measure]] $\mu$ mapping each measurable set $A$ to a [[real number]] (or similar quantity) $\mu(A)$, the measure of $A$.

A measurable subset $B$ of $X$ is __full__ if, given any measurable set $A$, $\mu(A \cap B) = \mu(A)$; an arbitrary subset of $X$ is __full__ if it\'s a [[superset]] of a full measurable set.  [[de Morgan duality|Dually]], a measurable set $B$ is __null__ if, given any measurable set $A$, $\mu(A \cup B) = \mu(A)$; an arbitrary subset of $X$ is __null__ if it\'s a [[subset]] of a null measurable set.

Some equivalent characterisations ([[constructive mathematics|constructively]] valid for measures on [[Cheng spaces]] except as stated):

*  A measurable set $B$ is null iff $\mu(C) = 0$ for every measurable subset of $B$.
*  If $\mu$ is a [[positive measure]], then a measurable set $B$ is null iff $\mu(B) = 0$.
*  If $\mu$ is a [[finite measure]] with total measure $I$, then a measurable set $B$ is full iff $\mu(C) = I$ for every measurable superset of $B$.
*  If $\mu$ is both positive and finite (so a [[probability measure]] up to rescaling), then a measurable set $B$ is full iff $\mu(B) = I$.
*  If $\mu$ is [[complete measure|complete]], then every null set is measurable and every full set is measurable (which is basically the definition of 'complete') and consequently the preceding properties continue to hold when the adjective 'measurable' is removed.
*  Using [[excluded middle]], a set is null iff its complement is full, and a set is full iff its complement is null.  (Even constructively, if a set is null, then its complement is full.)
*  Even constructively, a measurable set is null iff its measurable complement (the complement in the algebraic structure of complemented pairs in a Cheng measurable space) is full, and a measurable set is full iff its measurable complement is null.


### In untraditional measurable spaces

Traditionally, a [[measurable space]] is simply an abstract [[set]] $X$ and a $\sigma$-[[sigma-algebra|algebra]] (or similar structure) $\mathcal{M}$ consisting of the [[measurable subsets]] of $X$.  There is no notion of null or full subsets of such a space.  However, there are two (essentially equivalent) variations of this concept in which null and full subsets do make sense.

One variation is to simply equip the space with a $\delta$-[[delta-filter|filter]] of measurable subsets, which are declared to be the full measurable subsets.  Then a general __full subset__ is a superset of a measurable full subset, and a __null subset__ is any set whose complement is full.  (Alternatively, equip the space with a $\sigma$-[[sigma-ideal|ideal]] of measurable subsets, which are declared to be the null measurable subsets.)  In particular, a [[localizable measurable space]] is a measurable space so equipped such that the [[Boolean algebra]] of measurable sets modulo null sets (or modulo full sets if this is done by identifying the full sets with $X$) is [[complete boolean algebra|complete]].

Another variation, used especially in [[constructive mathematics]], is a [[Cheng measurable space]].  This consists of a set $X$ equipped with a $\sigma$-semialgebra of [[disjoint subsets|disjoint]] *pairs* of subsets of $X$, declared to be the _complemented pairs_.  A set is measurable iff it appears as one component of a complemented pair.  A measurable subset is _full_ if it appears as one component of a complemented pair whose other component is [[empty subset|empty]], or equivalently (given the structure of the algebra of complemented pairs) if it is the [[union]] of the two components of any complemented pair.  Then a general __full subset__ is a superset of a measurable full subset, and a __null subset__ is any set whose complement is full.

These are actually equivalent concepts.  Given a measurable space equipped with a $\delta$-filter of measurable full subsets, define a complemented pair to be a pair of disjoint measurable subsets whose union is full.  Conversely, given a Cheng measurable space, the measurable subsets and measurable full subsets as defined above comprise a $\sigma$-algebra and a $\delta$-filter in it.  (But constructively, the algebra of measurable subsets, while closed under the appropriate operations, will generally not be a [[boolean algebra]].)


### In smooth manifolds

A subset $A$ of an $n$-dimensional [[smooth manifold]] $X$ is __null__ or __full__ (respectively) if its [[preimage]] under every [[coordinate chart]] is a null or full subset (respectively) of the chart\'s domain (which is an [[open subset]] of the [[Cartesian space]] $\mathbb{R}^n$) under [[Lebesgue measure]].

This is actually better behaved than it may at first seem.  If $A$ is [[open cover|covered]] by an [[atlas]] $(\phi_i\colon U_i \to X)_i$, then $A$ is null or full as soon as $\phi_i^*(A)$ is null/full in $U_i$ for every index $i$.  In particular, if $A$ is contained in a single coordinate chart (which is not very likely for a full set but fairly common for null sets), then it is sufficient to check its preimage under that one.  This fact depends on the smoothness and fails for [[topological manifolds]].

As we can define a [[measurable subset]] of a smooth manifold similarly, this means that every smooth manifold gives rise to a measurable space equipped with a $\delta$-filter of full subsets (and hence to a Cheng measurable space); this space is always localizable.

(Details?  Is $C^1$ sufficient?  Conversely, is paracompactness necessary to keep the covers manageable?)


## Logic of full/null sets

A property of elements of $X$ (given by a [[subset]] $S$ of $X$) can be considered modulo null sets.  We say that the property $\phi$ is true __almost everywhere__ or __almost always__ if it is true on some full set, that is if $\{X | \phi\}$ is full.  Dually, we say that $\phi$ is true __almost nowhere__ or __almost never__ if $\{X | \phi\}$ is null.  It is better to use the [[negation]] of 'almost nowhere', although the terminology for this is not really standard; say that $\phi$ is true __somewhere significant__ if $\{X | \phi\}$ is non-null.

Note that being true almost everywhere is a weakening of being true everywhere (given by the [[universal quantifier]] $\forall$), while being true somewhere significant is a strengthening of being true somewhere (given by the [[particular quantifier]] $\exists$).  Indeed we can build a logic out of these.  Use $\ess\forall i, \phi[i]$ or $\ess\forall \phi$ to mean that a [[predicate]] $\phi$ on $X$ is true almost everywhere, and use $\ess\exists i, \phi[i]$ or $\ess\exists \phi$ to mean that $\phi$ is true somewhere significant.  Then we have:
$$\forall \phi \;\Rightarrow\; \ess\forall \phi$$
$$\ess\exists \phi \;\Rightarrow\; \exists \phi$$
$$\ess\forall (\phi \wedge \psi) \;\Leftrightarrow\; \ess\forall \phi \wedge \ess\forall \psi$$
$$\ess\exists (\phi \wedge \psi) \;\Rightarrow\; \ess\exists \phi \wedge \ess\exists \psi$$
$$\ess\forall (\phi \vee \psi) \;\Leftarrow\; \ess\forall \phi \wedge \ess\forall \psi$$
$$\ess\exists (\phi \vee \psi) \;\Leftrightarrow\; \ess\exists \phi \vee \ess\exists \psi$$
$$\ess\forall \neg{\phi} \;\Leftrightarrow\; \neg\ess\exists \phi$$
and other analogues of theorems from [[predicate logic]].  Note that the last item listed requires [[excluded middle]] even though its analogue from ordinary predicate logic does not.

A similar logic is satisfied by '[[eventually]]' and its dual ('frequently') in [[filters]] and [[nets]].


[[!redirects negligible set]]
[[!redirects negligible sets]]
[[!redirects negligible subset]]
[[!redirects negligible subsets]]

[[!redirects null set]]
[[!redirects null sets]]
[[!redirects null subset]]
[[!redirects null subsets]]
[[!redirects null measure]]
[[!redirects set of null measure]]
[[!redirects sets of null measure]]
[[!redirects subset of null measure]]
[[!redirects subsets of null measure]]

[[!redirects full set]]
[[!redirects full sets]]
[[!redirects full subset]]
[[!redirects full subsets]]
[[!redirects full measure]]
[[!redirects set of full measure]]
[[!redirects sets of full measure]]
[[!redirects subset of full measure]]
[[!redirects subsets of full measure]]

[[!redirects almost everywhere]]
[[!redirects almost nowhere]]
[[!redirects somewhere significant]]
