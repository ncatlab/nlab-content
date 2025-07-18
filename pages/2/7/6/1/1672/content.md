
# $\sigma$-Ideals
* table of contents
{: toc}

## Idea

A $\sigma$-ideal is a collection of sets (either [[subsets]] of an ambient set or [[pure sets]]) that are considered 'small' in some fashion.  Unlike the notion of 'small' in [[small category]], this is not expected to be closed under most infinitary operations, but it *is* expected to be closed under [[countable set|countably]] infinitary operations, in particular under countable [[union]].

If we use 'large' sets instead, then we have a $\delta$-filter.


## Definitions

Let $X$ be a [[set]].  Then a $\sigma$-ideal on $X$ is a collection $\mathcal{I}$ of [[subsets]] of $X$ such that:
1.  If $A \subset B$ and $B \in \mathcal{I}$, then $A \in \mathcal{I}$;
2.  If $A_1, A_2, \ldots \in \mathcal{I}$, then there exists $B$ such that $B \in \mathcal{I}$ and $\bigcup_i A_i \subseteq B$; in light of (1), $B$ may be assumed to be the [[union]] $\bigcup_i A_i$ itself.
3.  Some set belongs to $\mathcal{I}$; in light of (1), the [[empty set]] $\empty \in \mathcal{I}$.

A __[[base]]__ of a $\sigma$-ideal is any collection satisfying (2,3); a base is precisely what generates a $\sigma$-ideal by closing under subsets.  A __[[subbase]]__ of a $\sigma$-ideal is any collection at all; a subbase generates a base by closing under countable unions.

Instead of a set, $X$ may easily be a [[proper class]]; then the elements of $\mathcal{I}$ may be restricted to subclasses that are actually sets.  One may take $X$ to be the class of all [[pure sets]]; from the perspective of [[material set theory]], this actually includes the general case above.

As defined above, a $\sigma$-ideal $\mathcal{I}$ is a subset of the [[power set]] (or power class) $\mathcal{P}X$; we can just as easily make $\mathcal{I}$ a subset of any [[complete lattice]] $\mathcal{L}$.  Actually, it works just as well if $\mathcal{L}$ if replaced by a sup-[[semilattice]] with all countablary [[supremum|suprema]], or probably even more generally (see [[ideal]] for some idea of how to do that).  Note the grammar: a $\sigma$-ideal *in* $L$ but *on* $X$ (which is the same as *in* $\mathcal{P}X$).

Dually, a __$\delta$-[[filter]]__ on $X$ is a collection $\mathcal{F}$ of [[subsets]] of $X$ such that:
1.  If $A \subset B$ and $A \in \mathcal{F}$, then $B \in \mathcal{F}$;
2.  If $A_1, A_2, \ldots \in \mathcal{F}$, then there exists $B$ such that $B \in \mathcal{F}$ and $B \subseteq \bigcap_i A_i$; in light of (1), $B$ may be assumed to be the [[intersection]] $\bigcap_i A_i$ itself.
3.  Some set belongs to $\mathcal{F}$; in light of (1), the [[improper subset]] $X \in \mathcal{F}$.

Using [[de Morgan duality]], $\delta$-filters and $\sigma$-ideals are essentially the same; we have
$$ \mathcal{F} = \{ A \subseteq X \;|\; \neg{A} \in \mathcal{I} \} $$
and vice versa.  In [[constructive mathematics]], however, they are not equivalent.  Also, the two notions are not equivalent when $X$ is a [[proper class]].


## Examples

*  The power set of $X$ is both a $\sigma$-ideal and a $\delta$-filter on $X$; it is the _improper $\sigma$-ideal_ on $X$.  (Compare [[proper ideal]].)
*  The [[null sets]] in a [[measure space]] $X$ form a $\sigma$-ideal on $X$, while the [[full sets]] form the corresponding $\delta$-filter.
*  The [[meager subspace|meagre sets]] in a [[topological space]] $X$ form a $\sigma$-ideal on $X$, while the comeagre sets form the corresponding $\delta$-filter.
*  The [[pure sets]] form a $\sigma$-ideal on (or, equivalently in this case, in) the class of all pure sets; actually, this collection is closed under arbitrary unions rather than merely countablary unions, so we may call it a _complete ideal_.


## Properties

Of course, any $\sigma$-ideal in an [[ideal]].  A $\sigma$-ideal is a $\sigma$-[[sigma-ring|ring]] in its own right.  In fact, a $\sigma$-ideal on $X$ is precisely simultaneously an ideal in and a sub-$\sigma$-ring of $\mathcal{P}X$.  Dual results hold for $\delta$-filters.


[[!redirects sigma-ideal]]
[[!redirects sigma-ideals]]
[[!redirects σ-ideal]]
[[!redirects σ-ideals]]
[[!redirects ∞-ideal]]
[[!redirects ∞-ideals]]

[[!redirects delta-filter]]
[[!redirects delta-filters]]
[[!redirects ∞-filter]]
[[!redirects ∞-filters]]
