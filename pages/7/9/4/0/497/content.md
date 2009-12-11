
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

In [[logic]], the principle of **excluded middle** states that every [[truth value]] is either true or false. (This is sometimes called the 'axiom' or 'law' of excluded middle, either to emphasise that it is or is not optional; 'principle' is a relatively neutral term.) One of the many meanings of [[classical logic]] is to emphasise that this principle holds in the logic; in contrast, it fails in [[intuitionistic logic]].

The principle of excluded middle (hereafter, PEM), as a statement about truth values themselves, is accepted by nearly all mathematicians; those who doubt or deny it are a distinct minority, the [[constructive mathematics|constructivists]]. However, when one [[internalization|internalises]] mathematics in categories other than [[Set|the category of sets]], there is no doubt that excluded middle often fails internally. See the examples listed at [[internal logic]]. (Those categories in which excluded middle holds are called [[Boolean category|Boolean]]; in general, the adjective 'Boolean' is often used to indicate the applicability of PEM.)

## PEM versus AC 

Excluded middle can be seen as a very weak form of the [[axiom of choice]] (a slightly more controversial principle, doubted or denied by a slightly larger minority, and true internally in even fewer categories).  In fact, the following are equivalent.

1. The principle of excluded middle.
1. [[finite set|Finitely indexed]] sets are [[projective object|projective]] (in fact, it suffices 2-indexed sets to be projective).
1. [[finite set|Finite sets]] are [[choice object|choice]] (in fact, it suffices for 2 to be choice).

(Here, a set $A$ is **finite** or **finitely-indexed** (respectively) if, for some natural number $n$, there is a bijection or surjection (respectively) $\{0, \ldots, n - 1\} \to A$.)

The proof is as follows.  If $p$ is a truth value, then divide $\{0,1\}$ by the equivalence relation where $0 \equiv 1$ iff $p$ holds.  Then we have a surjection $2\to A$, whose domain is $2$ (and in particular, finite), and whose codomain $A$ is finitely-indexed.  But this surjection splits iff $p$ is true or false, so if either $2$ is choice or $2$-indexed sets are projective, then PEM holds.

On the other hand, if PEM holds, then we can show by induction that if $A$ and $B$ are choice, so is $A\sqcup B$ (add details).  Thus, all finite sets are choice.  Now if $n\to A$ is a surjection, exhibiting $A$ as finitely indexed, it has a section $A\to n$.  Since a finite set is always projective, and any retract of a projective object is projective, this shows that $A$ is projective.

In particular, the axiom of choice implies PEM.  This argument, due originally to Diaconescu, can be internalized in any [[topos]]. However, other weak versions of choice such as [[countable choice]] (any surjection to a countable set (which for this purpose is any set isomorphic to the set of natural numbers) has a section), [[dependent choice]], or even [[COSHEP]] do not imply PEM. In fact, it is often claimed that axiom of choice is *true* in constructive mathematics (by the BHK interpretation of predicate logic), leading to much argument about exactly what that means.

category: foundational axiom