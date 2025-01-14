
> This entry is about the theorem in [[logic]] which is often just called _Diaconescu's theorem_, but not to be confused with [[Diaconescu's theorem]] in [[topos theory]].

***

#Contents#
* table of contents
{:toc}

## Idea

The Diaconescu-Goodman–Myhill theorem ([Diaconescu 75](#Diaconescu75), [Goodman-Myhill 78](#GoodmanMyhill78)) states that the [[law of excluded middle]] may be regarded as a very weak form of the [[axiom of choice]].

## Statement

The following are equivalent:

1. The principle of [[excluded middle]].
1. [[finite set|Finitely indexed]] sets are [[projective object|projective]] (in fact, it suffices for 2-indexed sets to be projective).
1. [[finite set|Finite sets]] are [[choice object|choice]] (in fact, it suffices for 2 to be choice).

(Here, a [[set]] $A$ is **[[finite set|finite]]** or **finitely-indexed** (respectively) if, for some natural number $n$, there is a [[bijection]] or [[surjection]] (respectively) $\{0, \ldots, n - 1\} \to A$.)

## Proof

The [[proof]] is as follows.  If $p$ is a truth value, then divide $2 = \{0,1\}$ by the equivalence relation where $0 \equiv 1$ iff $p$ holds.  Then we have a surjection $2\to A$, whose domain is $2$ (and in particular, finite), and whose codomain $A$ is finitely-indexed.  But this surjection splits iff $p$ is true or false, so if either $2$ is choice or $2$-indexed sets are projective, then PEM holds.

On the other hand, if PEM holds, then we can show by induction that if $A$ and $B$ are choice, so is $A\sqcup B$ (add details).  Thus, all finite sets are choice.  Now if $n\to A$ is a surjection, exhibiting $A$ as finitely indexed, it has a section $A\to n$.  Since a finite set is always projective, and any retract of a projective object is projective, this shows that $A$ is projective.

In particular, the axiom of choice implies PEM.  This argument, due originally to [Diaconescu 75](#Diaconescu75), can be [[internalization|internalized]] in any [[topos]]. However, other weak versions of choice such as [[countable choice]] (any surjection to a countable set (which for this purpose is any set isomorphic to the set of natural numbers) has a section), [[dependent choice]], or even [[COSHEP]] do not imply PEM. In fact, it is often claimed that axiom of choice is *true* in constructive mathematics (by the BHK or [[Brouwer-Heyting-Kolmogorov interpretation]] of predicate logic), leading to much argument about exactly what that means.


## References

* {#Diaconescu75} [[Radu Diaconescu]], _Axiom of choice and complementation_, Proceedings of the American Mathematical Society 51:176-178 (1975) ([doi:10.1090/S0002-9939-1975-0373893-X](https://doi.org/10.1090/S0002-9939-1975-0373893-X))

* {#GoodmanMyhill78} N. D. Goodman J. Myhill, _Choice Implies Excluded Middle_, Zeitschrift fuer Mathematische Logik und Grundlagen der Mathematik 24:461 (1978)

Review includes

* {#McLarty96} [[Colin McLarty]], _Elementary Categories, Elementary Toposes_, Oxford University Press, 1996


See also 

* Wikipedia, _[Diaconescu' theorem](https://en.wikipedia.org/wiki/Diaconescu%27s_theorem)_

[[!redirects Diaconescu-Goodman–Myhill theorem]]
