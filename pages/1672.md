A $\sigma$-ideal is a collection of sets (either [[subset]]s of an ambient set or [[pure set]]s) that are considered 'small' in some fashion.  Unlike the notion of 'small' in [[small category]], this is not expected to be closed under most infinitary operations, but it *is* expected to be closed under [[countable set|countably]] infinitary operations, in particular under countable [[union]].


## Definitions

Let $X$ be a [[set]].  Then a $\sigma$-ideal on $X$ is a collection $\mathcal{I}$ of [[subset]]s of $X$ such that:
1.  If $A \subset B$ and $B \in \mathcal{I}$, then $A \in \mathcal{I}$;
1.  If $A_1, A_2, \ldots \in \mathcal{I}$, then there exists $B$ such that $B \in \mathcal{I}$ and $\bigcup_i A_i \subseteq B$; in light of (1), $B$ may be assumed to be the [[union]] $\bigcup_i A_i$ itself.
1.  Some set belongs to $\mathcal{I}$; in light of (1), the [[empty set]] $\empty \in \mathcal{I}$.

A __base__ of a $\sigma$-ideal is any collection satisfying (2,3); a base is precisely what generates a $\sigma$-ideal by closing under subsets.  A __subbase__ of a $\sigma$-ideal in any collection at all; a subbase generates a base by closing under countable unions.

Instead of a set, $X$ may easily be a [[proper class]]; then the elements of $\mathcal{I}$ may be restricted to subclasses that are actually sets.  One may take $X$ to be the class of all [[pure set]]s; from the perspective of material [[set theory]], this actually includes the previous examples.

As defined above, a $\sigma$-ideal $\mathcal{I}$ is a subset of the [[power set]] (or power class) $\mathcal{P}X$; we can just as easily make $\mathcal{I}$ a subset of any [[complete lattice]] $\mathcal{L}$.  Actually, it works just as well if $\mathcal{L}$ if replaced by a sup-[[semilattice]] with all countable [[supremum|suprema]], or probably even more generally (see [[ideal]] for some idea of how to do that).  Note the grammar: a $\sigma$-ideal *in* $L$ but *on* $X$ (which is the same as *in* $\mathcal{P}X$).


## Examples

*  The power set of $X$ is a $\sigma$-ideal on $X$; it is the _improper $\sigma$-ideal_ on $X$.
*  The null sets in a [[measure space]] $X$ form a $\sigma$-ideal on $X$.
*  The meagre sets in a [[topological space]] $X$ form a $\sigma$-ideal on $X$.
*  The [[pure set]]s form a $\sigma$-ideal on the class of all pure sets; actually, this collection is closed under arbitrary unions rather than merely countable unions, so we may call it a _complete ideal_.


## Properties

Of course, any $\sigma$-ideal in an [[ideal]].  A $\sigma$-ideal is a $\sigma$-[[sigma-ring|ring]] in its own right.  In fact, a $\sigma$-ideal on $X$ is precisely simultaneously an ideal in and a sub-$\sigma$-ring of $\mathcal{P}X$.