[[!redirects equivalence relations]]
[[!redirects equivalence class]]
[[!redirects equivalence classes]]
[[!redirects partition]]
[[!redirects partitions]]
[[!redirects setoid]]
[[!redirects setoids]]

An __equivalence relation__ on a set $S$ is a binary [[relation]] $\equiv$ on $S$ that is:
* [[reflexive relation|reflexive]]: $x \equiv x$ for all $x: S$;
* [[symmetric relation|symmetric]]: $x \equiv y$ if $y \equiv x$; and
* [[transitive relation|transitive]]: $x \equiv z$ if $x \equiv y \equiv z$.

(One can also define it as a relation that is both reflexive and [[euclidean relation|euclidean]].)  The [[de Morgan duality|dual]] of an equivalence relation is an [[apartness relation]].

A __setoid__ is a set equipped with an equivalence relation.

Equivalently, a setoid is a [[enriched category|groupoid enriched]] over the [[cartesian monoidal category]] of [[truth value]]s.  Then an equivalence relation on $S$ is a way of making $S$ into the set of objects of such a groupoid.

A __[[congruence]]__ is an [[internalization|internal]] equivalence relation.

It may well be useful to consider several possible equivalence relations on a given set.  When considering a single equivalence relation once and for all, however, it is common to take the [[quotient set]] $S/{\equiv}$ and use that instead.  As a groupoid, any setoid is [[equivalence of categories|equivalent]] to a [[set]] in this way.

Setoids are still important in [[foundations]] of mathematics where quotient sets don\'t always exist and the above equivalence cannot be carried out.  However, arguably this is a terminological mismatch, and such people should say 'set' where they say 'setoid' and something else (such as '[[preset]]', '[[type]]', or '[[completely presented set]]') where they say 'set'.  (See page 9 of [these lecture notes](http://www.cs.chalmers.se/Cs/Research/Logic/TypesSS05/Extra/palmgren.pdf).)
